---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Obtenga información sobre cómo la API de autenticación Web puede permitir que las aplicaciones web usen Windows Hello y FIDO2 para la autenticación de usuario.
title: 'Autenticación Web: Guía para desarrolladores'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: b8ff3769434c17b5508978c64b5d9c14e7e3bdaa
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941814"
---
# Autenticación Web y Windows Hello  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

La [API de autenticación Web](https://w3c.github.io/webauthn) en Microsoft Edge permite a las aplicaciones web usar [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) y [dispositivos de FIDO2 externo](https://fidoalliance.org/fido2) para la autenticación de usuarios, de modo que usted y sus usuarios puedan evitar todos los problemas y riesgos de la administración de contraseñas, entre los que se incluyen adivinación de contraseñas, suplantación de identidad y ataques de registro de claves.  La implementación actual de Microsoft Edge se basa en la recomendación candidata de la especificación de autenticación de Web.  

> [!IMPORTANT]
> En este tema se explica cómo probar Windows Hello y la autenticación FIDO2 con Microsoft Edge.  

Con la autenticación Web, el servidor envía un desafío de texto sin formato al explorador.  Una vez que Microsoft Edge puede comprobar el usuario a través de Windows Hello o de un dispositivo de FIDO2 externo, el sistema firmará el desafío con una clave privada que previamente se aprovisionó para este usuario y enviaba la firma de vuelta al servidor.  Si el servidor puede validar la firma con la clave pública que tiene para ese usuario y comprobar que el desafío es correcto, puede autenticar al usuario de forma segura.  Con la [Criptografía asimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como esta, la clave pública no tiene sentido por sí misma y la clave privada nunca se comparte.  Además, la clave privada nunca se puede mover de elementos seguros o sistemas modernos con hardware habilitado para TPM.  

Existen dos pasos básicos para usar la API de autenticación Web:  

1.  Registrar a un usuario con `create`  
1.  Autenticar al usuario con `get`  

La siguiente guía de desarrollo te guiará a través de este flujo con la [aplicación de ejemplo Webauthn](https://github.com/MicrosoftEdge/webauthnsample).  

## Registrar el usuario  

Actuando como proveedor de identidad, primero tendrá que crear una credencial de autenticación Web para su usuario con el `navigator.credentials.create` método.  Antes de registrar la credencial en el servidor, tendrá que confirmar la identidad del usuario.  Esto se puede hacer enviando al usuario una confirmación por correo electrónico o pidiéndole que use su método de inicio de sesión tradicional.  

El `create` método toma los siguientes parámetros:  

:::row:::
   :::column span="1":::
      **información de usuario de confianza**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      rp: {
          name: "WebAuthn Sample App",
          icon: "https://example.com/rpIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **información de la cuenta de usuario**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      user: {
          id: stringToArrayBuffer("some.user.id"),
          name: "bob.smith@contoso.com",
          displayName: "Bob Smith",
          icon: "https://example.com/userIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **parámetros criptográficos**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      pubKeyCredParams: [
          {
              //External authenticators support the ES256 algorithm
              type: "public-key",
              alg: -7                 
          }, 
          {
              //Windows Hello supports the RS256 algorithm
              type: "public-key",
              alg: -257
          }
      ],
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **parámetros de selección de autenticador**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      authenticatorSelection: {
          //Select authenticators that support username-less flows
          requireResidentKey: true,
          //Select authenticators that have a second factor (such as PIN, Bio)
          userVerification: "required",
          //Selects between bound or detachable authenticators
          authenticatorAttachment: "platform"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **otras opciones**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      //Select larger timeout values, as Microsoft Edge shows UI
      timeout: 50000,
      //an opaque challenge that the authenticator signs over
      challenge: challenge,
      //prevent re-registration by specifying existing credentials here
      excludeCredentials: [],
      //specifies whether you need an attestation statement
      attestation: "none" 
      ```  
   :::column-end:::
:::row-end:::  

Puede usar [los parámetros de creación de credenciales](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) para configurar las credenciales que desea crear.  En particular, puede optar por crear una credencial de Windows Hello si establece la opción en `authenticatorAttachment` `platform` o una credencial de itinerancia en un dispositivo de FIDO2 externo estableciendo `authenticatorAttachment` en `cross-platform` .  

Cuando usas el `create` método, Microsoft Edge primero pide al usuario que verifique su presencia escaneando su cara o huella digital, especificando un PIN o realizando una acción en un dispositivo FIDO2 externo.  Una vez completado este paso, el autenticador generará un par de claves de publicprivate y almacenará la clave privada.  Estas credenciales se crean por origen, por cuenta, y no se pueden extraer porque se almacenan de manera segura en el dispositivo de autenticación.  

La promesa resultante devuelve un [objeto de atestación](https://w3c.github.io/webauthn#sctn-attestation) que representa la nueva credencial.  El objeto de atestación contiene la clave pública de la credencial.  Enviará este objeto al servidor para validar autenticaciones futuras.  Antes de devolverlo al servidor, necesitará codificar en Base64 los datos sin procesar.  

**Cliente**  

```javascript
<script>
    navigator.credentials.create({
        publicKey: createCredentialOptions
    }).then(rawAttestation => {
        var attestation = {
            id: base64encode(rawAttestation.rawId),
            clientDataJSON: arrayBufferToString(rawAttestation.response.clientDataJSON),
            attestationObject: base64encode(rawAttestation.response.attestationObject)
        };
        return rest_put("/credentials", attestation);
    })
</script>
```  

El servidor debería entonces descodificar el objeto atestación, realizar pasos de verificación, extraer la clave pública de las credenciales y almacenarla para autenticaciones futuras.  Puede encontrar una lista detallada de los pasos en el [algoritmo de registro de credenciales](https://w3c.github.io/webauthn#registering-a-new-credential) en la especificación de webauthn.  

**Servidor**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## Autenticar al usuario  

Una vez que se crea la credencial en el cliente, la próxima vez que el usuario intente iniciar sesión en el sitio, podrá ofrecer su credencial de autenticación Web en lugar de una contraseña con una llamada a `navigator.credentials.get` .  

El `get` método toma el desafío como su único parámetro obligatorio.  El desafío es una secuencia opaca de bytes que el servidor enviará a un cliente para que inicie sesión con la clave privada del usuario.  Por ejemplo:  

**Servidor**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

Después de recuperar un desafío del servidor, deberá llamar a la API Get junto con [las opciones de solicitud de credenciales](https://w3c.github.io/webauthn#credentialrequestoptions-extension).  Microsoft Edge mostrará un mensaje para comprobar la identidad del usuario que usa Windows Hello o un dispositivo FIDO2 externo.  Una vez que se haya verificado el usuario, el desafío se firmará en el dispositivo TPM o FIDO2 y la promesa devolverá un [objeto de aserción](https://w3c.github.io/webauthn#authenticatorassertionresponse) que contiene la firma y otros metadatos que se enviarán al servidor.  

**Cliente**  

```javascript
    var credentialRequestOptions = {
        //specifies which credential IDs are allowed to authenticate the user
        //if empty, any credential can authenticate the users
        allowCredentials: allowCredentials,
        //an opaque challenge that the authenticator signs over
        challenge: challenge,
        //Select larger timeout values, as Microsoft Edge shows UI
        timeout: 50000
    };

    navigator.credentials.get({
        publicKey: credentialRequestOptions
    }).then(rawAssertion => {
        var assertion = {
            id: base64encode(rawAssertion.rawId),
            clientDataJSON: arrayBufferToString(rawAssertion.response.clientDataJSON),
            userHandle: base64encode(rawAssertion.response.userHandle),
            signature: base64encode(rawAssertion.response.signature),
            authenticatorData: base64encode(rawAssertion.response.authenticatorData)
        };
        return rest_put("/assertion", assertion);
    })
```  

Una vez que reciba la aserción en el servidor, tendrá que validar la firma para autenticar al usuario.  A continuación se muestra un ejemplo de código.  Puede encontrar una lista detallada de los pasos en el [algoritmo de verificación de aserción](https://w3c.github.io/webauthn#verifying-assertion) en la especificación de webauthn.  

**Servidor**  

```javascript
    var jwkToPem = require('jwk-to-pem')
    var crypto = require('crypto');

    ...

    // Using credential’s id attribute, look up the corresponding 
    // credential public key.
    var credential = await storage.Credentials.findOne({
        id: assertion.id
    });

    //Refer to sample to see how to verify client data and authenticator data

    ...

    //Using the credential public key from lookup, verify that sig is a valid
    //signature over the binary concatenation of authData and hash.
    var publicKey = credential.publicKeyJwk;
    var verify = (publicKey.kty === "RSA") ? crypto.createVerify('RSA-SHA256') : crypto.createVerify('sha256');
    verify.update(authData);
    verify.update(hash);
    if (!verify.verify(jwkToPem(publicKey), sig))
        throw new Error("Could not verify signature");

    //Verify signCount has increased or is zero 
    if (authenticatorData.signCount != 0 &&
        authenticatorData.signCount < credential.signCount) {
        throw new Error("Received signCount of " + authenticatorData.signCount +
            " expected signCount > " + credential.signCount);
    }
```  

## Notas de implementación  

### Plataformas compatibles  

*   La versión de recomendación candidata de la API de autenticación Web se puede usar desde Microsoft Edge a partir de EdgeHTML 18 \ (Windows Insider Preview versión 17713 o posterior \).  
*   La [versión prefija](https://blogs.windows.com/msedgedev/2016/04/12) de la API de autenticación Web se ha quitado y ya no está disponible.  
*   La API de autenticación Web aún no está disponible para las aplicaciones para UWP y PWAs.  
*   Internet Explorer no admite la API de autenticación Web.  

### Autenticadores compatibles  

Con la API de autenticación Web de Microsoft Edge, puedes autenticar a los usuarios con las siguientes tecnologías:  

*   **Windows Hello**  Habilita la autenticación en el dispositivo sin contraseñas con cara, huella dactilar o PIN  
*   **FIDO2**  Habilita la autenticación de itinerancia sin contraseñas con un dispositivo extraíble y una huella dactilar o un PIN  
*   **U2F**  Habilita la autenticación de factor sólido para sitios web que no están listos para migrar a un modelo sin contraseñas  

### Consideraciones especiales para Windows Hello  

Algunas cosas que debe tener en cuenta al usar el autenticador de Windows Hello:  

*   Puedes detectar si Windows Hello está disponible en tu PC llamando a la `isUserVerifyingPlatformAuthenticatorAvailable` API.  Obtén más información sobre esta API [aquí](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).  
*   Al crear una credencial para Windows Hello, debe establecer `authenticatorAttachment` para `platform` la mejor experiencia del usuario.
*   Windows Hello solo admite RS256 \ (ALG-257 \) como algoritmo de clave pública.  Asegúrese de especificar este algoritmo al crear una credencial.  
*   Para recibir una [declaración de atestación de TPM](https://w3c.github.io/webauthn#tpm-attestation), establece la atestación en "directo" al llamar a la `create` API.  La atestación de TPM es el mejor intento.  Solo los equipos con el TPM 2,0 devolverán una declaración de atestación de TPM, y el proceso de atestación podría producir un error por varias razones.  
*   Windows Hello emplea una variedad de formas para proteger las credenciales de usuario.  Para comprobar qué método se ha usado para proteger una credencial, consume el campo [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) en el objeto atestación que se ha devuelto durante la creación de la credencial.  A continuación se muestra la lista de AAGUIDs que Windows Hello puede devolver:   
    *   Autenticadores devueltos por software  
        *   Autenticador de software de Windows Hello:  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   Autenticador de software Windows Hello VBS:  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   El módulo de plataforma segura \ (TPM \) autenticadores revertidos  
        *   Autenticador de hardware de Windows Hello:  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   Autenticador de hardware Windows Hello VBS:  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### Superficie de la API  

*   Microsoft Edge tiene una implementación completa de la versión de recomendación candidata de la especificación de autenticación Web básica.  
*   La [extensión AppID](https://w3c.github.io/webauthn#sctn-appid-extension) es compatible.  
*   No se admite ninguna otra extensión.  

## Demos  

[Ejemplo de código de cliente y servidor](https://github.com/MicrosoftEdge/webauthnsample)  

[Demostración de Windows Hello Test Drive](https://webauthnsample.azurewebsites.net)  

## Estadístico  

[Autenticación Web: una API para obtener acceso a las credenciales de clave pública](http://w3c.github.io/webauthn)  
