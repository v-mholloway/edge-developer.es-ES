---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Obtenga información sobre cómo se puede usar la API de autenticación Web para permitir que las aplicaciones web usen biometría de Windows Hello para la autenticación de usuario.
title: 'Guía de desarrollo: autenticación Web'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: c49d181633ae1b2b35aa0f88287841d28e806f44
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572965"
---
# Autenticación Web y Windows Hello

La API de autenticación Web (anteriormente *FIDO 2,0* ) en Microsoft Edge permite a las aplicaciones web usar [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometría para la autenticación de usuarios, de modo que usted y sus usuarios puedan evitar todos los problemas y riesgos de la administración de contraseñas, entre los que se incluyen averiguaciones de contraseñas, suplantación de identidad y ataques de keylogging. La implementación actual de Microsoft Edge (*MS-* Fixed) se basa en un borrador anterior de la especificación de autenticación Web y es probable que cambie en el futuro. **En este tema se explica cómo probar la autenticación de Windows Hello con Microsoft Edge, así como el código de las actualizaciones del explorador.**

La API de autenticación Web es un estándar emergente establecido por la [Alianza de Fido](https://fidoalliance.org/) con el objetivo de ofrecer una manera interoperable de realizar la autenticación Web con Windows Hello y otros dispositivos biométricos en exploradores. La especificación de autenticación Web define dos escenarios de autenticación: menos de contraseña y dos factores. En el caso de que no haya contraseña, el usuario no tiene que iniciar sesión en la página web con un nombre de usuario o una contraseña, ya que puede iniciar sesión únicamente con Windows Hello. En el caso de dos factores, el usuario inicia sesión normalmente con un nombre de usuario y una contraseña, pero Windows Hello se usa como una comprobación de segundo factor para que la autenticación general sea más segura.

Con la autenticación Web combinada con Windows Hello, el servidor envía un desafío de texto sin formato al explorador. Una vez que Microsoft Edge puede comprobar el usuario a través de Windows Hello, el sistema firmará el desafío con una clave privada que previamente se aprovisionó para este usuario y enviaba la firma de vuelta al servidor. Si el servidor puede validar la firma con la clave pública que tiene para ese usuario y comprobar que el desafío es correcto, puede autenticar al usuario de forma segura. Con la [Criptografía asimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como esta, la clave pública no tiene sentido por sí misma y la clave privada nunca se comparte. Además, la clave privada nunca se puede mover desde sistemas modernos con hardware habilitado para TPM.

Existen dos pasos básicos para usar la API de autenticación Web:

**1. registrar a un usuario con `makeCredential`**

**2. autenticar al usuario con `getAssertion`**

El siguiente paso le guiará a través de este flujo mediante el [rellenador recomendado de webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js). El [código completo](https://github.com/adrianba/fido-snippets/) está disponible para este servidor y demostración de cliente. Las versiones del lado del servidor de [C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [php](https://github.com/adrianba/fido-snippets/tree/master/php)y [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) están disponibles.

## Registrar el usuario

Actuando como *proveedor de identidad*, primero deberá crear una credencial de autenticación Web para su usuario con la ventana. webauthn. método **makeCredential** . Antes de registrar la credencial en el servidor, tendrá que confirmar la identidad del usuario. Esto se puede hacer enviando al usuario una confirmación por correo electrónico o pidiéndole que use su método de inicio de sesión tradicional.

El método makeCredential toma los siguientes parámetros:
 - **información de la cuenta de usuario**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **parámetros criptográficos**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

La promesa resultante devuelve un objeto que representa la credencial que se enviará de vuelta al servidor para validar autenticaciones futuras:

**Cliente**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var email = '<%=user.email%>';
    var name = '<%=user.name%>';

    webauthn.makeCredential(userAccountInformation, cryptoParams)
        .then(function (creds) {
            document.getElementById('form-id').value = creds.credential.id;
            document.getElementById('form-pk').value = JSON.stringify(creds.publicKey);
            document.getElementById('form-email').value = email;
            document.getElementById('form-name').value = name;
            document.getElementById('theform').submit();
        }).catch(function (err) {
            // No acceptable authenticator or user refused consent. Handle appropriately.
            alert(err);
        });
</script>
```

Cuando use el método makeCredential, Microsoft Edge primero pedirá a Windows Hello que use la imagen del rostro o de huella dactilar para comprobar que el usuario es el mismo usuario que ha iniciado sesión en la cuenta de Windows. Una vez completado este paso, Microsoft Passport generará un par de claves pública y privada y almacenará la clave privada en el módulo de plataforma segura (TPM), el hardware de procesador criptográfico dedicado usado para almacenar las credenciales. Si el usuario no tiene un dispositivo habilitado para TPM, estas claves se almacenarán en el software. Estas credenciales se crean por origen, por cuenta de Windows, y no se pueden mover porque están ligadas al dispositivo. Esto significa que tendrás que asegurarte de que el usuario se registre para usar Windows Hello para cada dispositivo que usen.

## Autenticar al usuario

Una vez que se crea la credencial en el cliente, la próxima vez que el usuario intente iniciar sesión en el sitio, podrá ofrecer su firma con Windows Hello en lugar de una contraseña con una llamada a Window. webauthn. **getAssertion**.

El método getAssertion toma el *desafío* como su único parámetro obligatorio. El desafío es la cantidad generada al azar que el servidor enviará a un cliente para que inicie sesión con la clave privada del usuario. Por ejemplo:

**Servidor**

```
var crypto = require('crypto');

Strategy.prototype.generateChallenge = function() {
    return this.generateVerifiableString(crypto.randomBytes(32));
};

Strategy.prototype.generateVerifiableString = function(data) {
    // Create cipher using secret
    var d = new Buffer(data);
    var c = crypto.createCipher('aes192',new Buffer(this._secret));

    // Encrypt data
    c.update(d);

    // Hash results of encrypting data
    var hash = crypto.createHash('sha256');
    hash.update(c.final());

    // Combine original data with hash
    return d.toString('hex') + string_separator + hash.digest('hex');
};
```

Una vez que se realice la llamada getAssertion, Microsoft Edge mostrará el mensaje de Windows Hello, que verificará la identidad del usuario mediante biometría. Una vez que se haya verificado el usuario, el desafío se firmará en el TPM y la promesa devolverá un objeto de aserción que contiene la firma y otros metadatos que se enviarán al servidor:

**Cliente**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var challenge = '<%=challenge%>';

    webauthn.getAssertion(challenge)
    .then(function(assertion) {
      document.getElementById("form-id").value = assertion.credential.id;
      document.getElementById("form-type").value = assertion.credential.type;
      document.getElementById("form-data").value = assertion.clientData;
      document.getElementById("form-sig").value = assertion.signature;
      document.getElementById("form-authnr").value = assertion.authenticatorData;
      document.getElementById("form-challenge").value = challenge;
      document.getElementById("theform").submit();
    })
    .catch(function(err) {
      if(err && err.name) {
        document.getElementById("form-err").value = err.name;
      } else {
        document.getElementById("form-err").value = "unknown";
      }
      document.getElementById("theform").submit();
    });

</script>
```

Una vez que reciba la aserción en el servidor, tendrá que validar la firma para autenticar al usuario. Por ejemplo (en node. JS):

**Servidor**

```
var jwkToPem = require('jwk-to-pem')
var crypto = require('crypto');

var fidoAuthenticator = {
     validateSignature: function (publicKey, clientData, authnrData, signature, challenge) {
         // Make sure the challenge in the client data
         // matches the expected challenge
         var c = new Buffer(clientData, 'base64');
         var cc = JSON.parse(c.toString().replace(/\0/g,''));
         if(cc.challenge != challenge) return false;

         // Hash data with sha256
         const hash = crypto.createHash('sha256');
         hash.update(c);
         var h = hash.digest();

         // Verify signature is correct for authnrData + hash
         var verify = crypto.createVerify('RSA-SHA256');
         verify.update(new Buffer(authnrData,'base64'));
         verify.update(h);
         return verify.verify(jwkToPem(JSON.parse(publicKey)), signature, 'base64');
     }
};   
```

## Diferencias entre Microsoft Edge y las especificaciones

> [!NOTE]
> Al probar la API de autenticación Web con Windows Hello en Microsoft Edge, te recomendamos que uses el rellenador webauthn. js, como se muestra anteriormente, para evitar tener que contar las discrepancias que se enumeran aquí. Actualizaremos este polyfill por cada versión publicada importante de la especificación.


La implementación actual de Microsoft Edge se basa en un borrador anterior de la especificación de autenticación Web y es probable que cambie en compilaciones futuras y que la especificación evolucione. Las diferencias actuales son:

- Las API de Microsoft Edge son MS-prefijado.
- Microsoft Edge aún no admite credenciales externas como SerialKeys o dispositivos Bluetooth. La API actual está limitada a las credenciales incrustadas almacenadas en el TPM.
- La cuenta de usuario de Windows actualmente conectada debe estar configurada para admitir al menos un PIN y, preferiblemente, una cara o una biometría de huellas digitales. Esto garantiza que Windows pueda autenticar el acceso al TPM.
- La implementación de Microsoft Edge aún no admite la experiencia del selector de cuentas.
- En este momento se requiere un segundo parámetro de *filtros* que especifique el identificador de credencial para las llamadas a msCredentials. [getAssertion](https://msdn.microsoft.com/library/mt697640). Como tal, tendrá que almacenar la información del identificador de credenciales en almacenamiento local en el cliente, ya sea en indexDB o localStorage al crear las credenciales. Si un usuario elimina el historial de navegación, incluido el almacenamiento local, tendrá que volver a registrarse para usar Windows Hello la próxima vez que inicie sesión.
- Microsoft Edge no admite todas las opciones del borrador de especificación de autenticación de Web actual, como extensiones o tiempos de espera.

En este último punto, se destacan las diferencias específicas de Microsoft Edge en las siguientes definiciones de especificación de autenticación Web:

### Especificación W3C

```
partial interface Window {
    readonly attribute WebAuthentication webauthn; // msCredentials
};

interface WebAuthentication { // MSCredentials
    Promise <ScopedCredentialInfo> makeCredential (
        Account                                 accountInformation,
        sequence <ScopedCredentialParameters>   cryptoParameters,
        DOMString                               attestationChallenge, // Optional in Microsoft Edge
        optional unsigned long                  credentialTimeoutSeconds, // Not yet supported
        optional sequence <Credential>          blacklist, // Not yet supported
        optional WebAuthnExtensions             credentialExtensions // Not yet supported
    );

    Promise <WebAuthnAssertion> getAssertion (
        DOMString                        assertionChallenge,
        optional unsigned long           assertionTimeoutSeconds, // Not yet supported
        optional sequence <Credential>   whitelist, // Not yet supported
        optional WebAuthnExtensions      assertionExtensions // Not yet supported
    );
};

interface ScopedCredentialInfo { // MSAssertion
    readonly attribute Credential           credential;
    readonly attribute any                  publicKey;
    readonly attribute AttestationStatement attestation;
};

dictionary Account { // MSAccountInfo
    required DOMString rpDisplayName;
    required DOMString displayName;
    DOMString          name; // Not yet supported
    DOMString          id; // Not yet supported
    DOMString          imageUri; // Not yet supported
};

dictionary ScopedCredentialParameters { // MSCredentialParameters
    required CredentialType        type;
    required AlgorithmIdentifier   algorithm;
};

enum CredentialType { // MSCredentialType
    "ScopedCred" // Must be "FIDO_2_0" in Microsoft Edge
};

interface Credential { // MSCredentialSpec
    readonly attribute CredentialType type;
    readonly attribute DOMString      id;
};

dictionary WebAuthnExtensions { // Not supported
};
```



## Referencia de API

[MSCredentials](https://msdn.microsoft.com/library/mt697639)

[makeCredential](https://msdn.microsoft.com/library/mt697641)

[getAssertion](https://msdn.microsoft.com/library/mt697640)

## Demos

[Ejemplos de código de cliente y servidor](https://github.com/adrianba/fido-snippets/)

[Polyfill de webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[Demostración de Windows Hello Test Drive](https://testdrive-fido.azurewebsites.net/)

## Estadístico

[Autenticación Web: una API Web para acceder a las credenciales con ámbito 1](http://w3c.github.io/webauthn/)  
