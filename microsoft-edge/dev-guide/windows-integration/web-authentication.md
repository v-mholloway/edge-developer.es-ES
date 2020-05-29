---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Obtenga información sobre cómo la API de autenticación Web puede permitir que las aplicaciones web usen Windows Hello y FIDO2 para la autenticación de usuario.
title: 'Guía de desarrollo: autenticación Web'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: cb561ae4147a24489138263a83dd37bd6f599074
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573310"
---
# <span data-ttu-id="6ebc2-104">Autenticación Web y Windows Hello</span><span class="sxs-lookup"><span data-stu-id="6ebc2-104">Web Authentication and Windows Hello</span></span>

<span data-ttu-id="6ebc2-105">La [API de autenticación Web](https://w3c.github.io/webauthn) en Microsoft Edge permite a las aplicaciones web usar [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) y [dispositivos de FIDO2 externo](https://fidoalliance.org/fido2) para la autenticación de usuarios, de modo que usted y sus usuarios puedan evitar todos los problemas y riesgos de la administración de contraseñas, entre los que se incluyen adivinación de contraseñas, suplantación de identidad y ataques de registro de claves.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span> <span data-ttu-id="6ebc2-106">La implementación actual de Microsoft Edge se basa en la recomendación candidata de la especificación de autenticación de Web.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span> **<span data-ttu-id="6ebc2-107">En este tema se explica cómo probar Windows Hello y la autenticación FIDO2 con Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>**

<span data-ttu-id="6ebc2-108">Con la autenticación Web, el servidor envía un desafío de texto sin formato al explorador.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="6ebc2-109">Una vez que Microsoft Edge puede comprobar el usuario a través de Windows Hello o de un dispositivo de FIDO2 externo, el sistema firmará el desafío con una clave privada que previamente se aprovisionó para este usuario y enviaba la firma de vuelta al servidor.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="6ebc2-110">Si el servidor puede validar la firma con la clave pública que tiene para ese usuario y comprobar que el desafío es correcto, puede autenticar al usuario de forma segura.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="6ebc2-111">Con la [Criptografía asimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como esta, la clave pública no tiene sentido por sí misma y la clave privada nunca se comparte.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="6ebc2-112">Además, la clave privada nunca se puede mover de elementos seguros o sistemas modernos con hardware habilitado para TPM.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="6ebc2-113">Existen dos pasos básicos para usar la API de autenticación Web:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-113">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="6ebc2-114">1. registrar a un usuario con</span><span class="sxs-lookup"><span data-stu-id="6ebc2-114">1. Register your user with</span></span> `create`**

**<span data-ttu-id="6ebc2-115">2. autenticar al usuario con</span><span class="sxs-lookup"><span data-stu-id="6ebc2-115">2. Authenticate your user with</span></span> `get`**

<span data-ttu-id="6ebc2-116">La siguiente guía de desarrollo te guiará a través de este flujo con la [aplicación de ejemplo Webauthn](https://github.com/MicrosoftEdge/webauthnsample).</span><span class="sxs-lookup"><span data-stu-id="6ebc2-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>

## <span data-ttu-id="6ebc2-117">Registrar el usuario</span><span class="sxs-lookup"><span data-stu-id="6ebc2-117">Register your user</span></span>

<span data-ttu-id="6ebc2-118">Actuando como *proveedor de identidad*, primero deberá crear una credencial de autenticación Web para el usuario con el navegador. Credentials. **crear** método.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-118">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the navigator.credentials.**create** method.</span></span> <span data-ttu-id="6ebc2-119">Antes de registrar la credencial en el servidor, tendrá que confirmar la identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="6ebc2-120">Esto se puede hacer enviando al usuario una confirmación por correo electrónico o pidiéndole que use su método de inicio de sesión tradicional.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>


<span data-ttu-id="6ebc2-121">El `create` método toma los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-121">The `create` method takes the following parameters:</span></span>

 - **<span data-ttu-id="6ebc2-122">información de usuario de confianza</span><span class="sxs-lookup"><span data-stu-id="6ebc2-122">relying party information</span></span>**

```javascript
    rp: {
        name: "WebAuthn Sample App",
        icon: "https://example.com/rpIcon.png"
    },
```

 - **<span data-ttu-id="6ebc2-123">información de la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="6ebc2-123">user account information</span></span>**

```javascript
    user: {
        id: stringToArrayBuffer("some.user.id"),
        name: "bob.smith@contoso.com",
        displayName: "Bob Smith",
        icon: "https://example.com/userIcon.png"
    },
```

 - **<span data-ttu-id="6ebc2-124">parámetros criptográficos</span><span class="sxs-lookup"><span data-stu-id="6ebc2-124">crypto parameters</span></span>**

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

 - **<span data-ttu-id="6ebc2-125">parámetros de selección de autenticador</span><span class="sxs-lookup"><span data-stu-id="6ebc2-125">authenticator selection parameters</span></span>**

```javascript
    authenticatorSelection: {
        //Select authenticators that support username-less flows
        requireResidentKey: true,
        //Select authenticators that have a second factor (e.g. PIN, Bio)
        userVerification: "required",
        //Selects between bound or detachable authenticators
        authenticatorAttachment: "platform"
    },
```

- **<span data-ttu-id="6ebc2-126">otras opciones</span><span class="sxs-lookup"><span data-stu-id="6ebc2-126">other options</span></span>**

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

<span data-ttu-id="6ebc2-127">Puede usar [los parámetros de creación de credenciales](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) para configurar las credenciales que desea crear.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-127">You can use [credential creation parameters](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span> <span data-ttu-id="6ebc2-128">En particular, puede optar por crear una credencial de Windows Hello si establece la opción en `authenticatorAttachment` `platform` o una credencial de itinerancia en un dispositivo de FIDO2 externo estableciendo `authenticatorAttachment` en `cross-platform` .</span><span class="sxs-lookup"><span data-stu-id="6ebc2-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span> 

<span data-ttu-id="6ebc2-129">Cuando usas el `create` método, Microsoft Edge primero pide al usuario que verifique su presencia escaneando su cara o huella digital, especificando un PIN o realizando una acción en un dispositivo FIDO2 externo.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span> <span data-ttu-id="6ebc2-130">Una vez completado este paso, el autenticador generará un par de claves pública y privada y almacenará la clave privada.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-130">Once this step is completed the authenticator will generate a public/private key pair and store the private key.</span></span> <span data-ttu-id="6ebc2-131">Estas credenciales se crean por origen, por cuenta, y no se pueden extraer porque se almacenan de manera segura en el dispositivo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span> 

<span data-ttu-id="6ebc2-132">La promesa resultante devuelve un [objeto de atestación](https://w3c.github.io/webauthn/#sctn-attestation) que representa la nueva credencial.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn/#sctn-attestation) representing the new credential.</span></span> <span data-ttu-id="6ebc2-133">El objeto de atestación contiene la clave pública de la credencial.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-133">The attestation object contains the public key for the credential.</span></span> <span data-ttu-id="6ebc2-134">Enviará este objeto al servidor para validar autenticaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-134">You'll send this object to the server for validating future authentications.</span></span> <span data-ttu-id="6ebc2-135">Antes de devolverlo al servidor, necesitará codificar en Base64 los datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>

**<span data-ttu-id="6ebc2-136">Cliente</span><span class="sxs-lookup"><span data-stu-id="6ebc2-136">Client</span></span>**

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

<span data-ttu-id="6ebc2-137">El servidor debería entonces descodificar el objeto atestación, realizar pasos de verificación, extraer la clave pública de las credenciales y almacenarla para autenticaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span> <span data-ttu-id="6ebc2-138">Puede encontrar una lista detallada de los pasos en el [algoritmo de registro de credenciales](https://w3c.github.io/webauthn/#registering-a-new-credential) en la especificación de webauthn.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn/#registering-a-new-credential) in the WebAuthn specification.</span></span>

**<span data-ttu-id="6ebc2-139">Servidor</span><span class="sxs-lookup"><span data-stu-id="6ebc2-139">Server</span></span>**

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```

## <span data-ttu-id="6ebc2-140">Autenticar al usuario</span><span class="sxs-lookup"><span data-stu-id="6ebc2-140">Authenticate your user</span></span>

<span data-ttu-id="6ebc2-141">Una vez que se crea la credencial en el cliente, la próxima vez que el usuario intente iniciar sesión en el sitio, podrá ofrecer su credencial de autenticación Web en lugar de una contraseña con una llamada a Navigator. Credentials. **obtener**.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to navigator.credentials.**get**.</span></span>

<span data-ttu-id="6ebc2-142">El `get` método toma el *desafío* como su único parámetro obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-142">The `get` method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="6ebc2-143">El desafío es una secuencia opaca de bytes que el servidor enviará a un cliente para que inicie sesión con la clave privada del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="6ebc2-144">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-144">For example:</span></span>

**<span data-ttu-id="6ebc2-145">Servidor</span><span class="sxs-lookup"><span data-stu-id="6ebc2-145">Server</span></span>**

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```

<span data-ttu-id="6ebc2-146">Después de recuperar un desafío del servidor, deberá llamar a la API Get junto con [las opciones de solicitud de credenciales](https://w3c.github.io/webauthn/#credentialrequestoptions-extension).</span><span class="sxs-lookup"><span data-stu-id="6ebc2-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn/#credentialrequestoptions-extension).</span></span> <span data-ttu-id="6ebc2-147">Microsoft Edge mostrará un mensaje para comprobar la identidad del usuario que usa Windows Hello o un dispositivo FIDO2 externo.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span> <span data-ttu-id="6ebc2-148">Una vez que se haya verificado el usuario, el desafío se firmará en el dispositivo TPM o FIDO2 y la promesa devolverá un [objeto de aserción](https://w3c.github.io/webauthn/#authenticatorassertionresponse) que contiene la firma y otros metadatos que se enviarán al servidor.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn/#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>

**<span data-ttu-id="6ebc2-149">Cliente</span><span class="sxs-lookup"><span data-stu-id="6ebc2-149">Client</span></span>**

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

<span data-ttu-id="6ebc2-150">Una vez que reciba la aserción en el servidor, tendrá que validar la firma para autenticar al usuario.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="6ebc2-151">A continuación se muestra un ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-151">The following is some sample code.</span></span>  <span data-ttu-id="6ebc2-152">Puede encontrar una lista detallada de los pasos en el [algoritmo de verificación de aserción](https://w3c.github.io/webauthn/#verifying-assertion) en la especificación de webauthn.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn/#verifying-assertion) in the WebAuthn specification.</span></span>

**<span data-ttu-id="6ebc2-153">Servidor</span><span class="sxs-lookup"><span data-stu-id="6ebc2-153">Server</span></span>**

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

## <span data-ttu-id="6ebc2-154">Notas de implementación</span><span class="sxs-lookup"><span data-stu-id="6ebc2-154">Implementation notes</span></span>

### <span data-ttu-id="6ebc2-155">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="6ebc2-155">Supported platforms</span></span>
- <span data-ttu-id="6ebc2-156">La versión de recomendación de candidato de la API de autenticación Web se puede usar desde Microsoft Edge a partir de EdgeHTML 18 (Windows Insider Preview versión 17713 y superior).</span><span class="sxs-lookup"><span data-stu-id="6ebc2-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 (Windows Insider Preview version 17713 and up).</span></span>
- <span data-ttu-id="6ebc2-157">La [versión prefija](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) de la API de autenticación Web se ha quitado y ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) of the Web Authentication API has been removed and is no longer available.</span></span>
- <span data-ttu-id="6ebc2-158">La API de autenticación Web aún no está disponible para las aplicaciones para UWP y PWAs.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>
- <span data-ttu-id="6ebc2-159">Internet Explorer no admite la API de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-159">Internet Explorer does not support the Web Authentication API.</span></span> 

### <span data-ttu-id="6ebc2-160">Autenticadores compatibles</span><span class="sxs-lookup"><span data-stu-id="6ebc2-160">Supported authenticators</span></span>
<span data-ttu-id="6ebc2-161">Con la API de autenticación Web de Microsoft Edge, puedes autenticar a los usuarios con las siguientes tecnologías:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>
- <span data-ttu-id="6ebc2-162">**Windows Hello**, habilitación de la autenticación en el dispositivo sin contraseñas con rostro, huella dactilar o PIN</span><span class="sxs-lookup"><span data-stu-id="6ebc2-162">**Windows Hello**, enabling passwordless on-device authentication with  face, fingerprint, or PIN</span></span>
- <span data-ttu-id="6ebc2-163">**FIDO2**, habilitar la autenticación de itinerancia sin contraseñas con un dispositivo extraíble y una huella dactilar o un PIN</span><span class="sxs-lookup"><span data-stu-id="6ebc2-163">**FIDO2**, enabling passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>
- <span data-ttu-id="6ebc2-164">**U2F**, habilitando la autenticación de factor sólido para sitios web que no están listos para moverse a un modelo sin contraseñas</span><span class="sxs-lookup"><span data-stu-id="6ebc2-164">**U2F**, enabling strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>

### <span data-ttu-id="6ebc2-165">Consideraciones especiales para Windows Hello</span><span class="sxs-lookup"><span data-stu-id="6ebc2-165">Special considerations for Windows Hello</span></span> 
<span data-ttu-id="6ebc2-166">Algunas cosas que debe tener en cuenta al usar el autenticador de Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-166">A few things to note when using the Windows Hello authenticator:</span></span>
- <span data-ttu-id="6ebc2-167">Puedes detectar si Windows Hello está disponible en tu PC llamando a la `isUserVerifyingPlatformAuthenticatorAvailable` API.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span> <span data-ttu-id="6ebc2-168">Obtén más información sobre esta API [aquí](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable).</span><span class="sxs-lookup"><span data-stu-id="6ebc2-168">Learn more about this API [here](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>
- <span data-ttu-id="6ebc2-169">Al crear una credencial para Windows Hello, debe establecer `authenticatorAttachment` para `platform` la mejor experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
- <span data-ttu-id="6ebc2-170">Windows Hello solo admite RS256 (ALG-257) como algoritmo de clave pública.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-170">Windows Hello only supports RS256 (alg -257) as its public key algorithm.</span></span> <span data-ttu-id="6ebc2-171">Asegúrese de especificar este algoritmo al crear una credencial.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-171">Be sure to specify this algorithm when creating a credential.</span></span>
- <span data-ttu-id="6ebc2-172">Para recibir una [declaración de atestación de TPM](https://w3c.github.io/webauthn/#tpm-attestation), establece la atestación en "directo" al llamar a la `create` API.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn/#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span> <span data-ttu-id="6ebc2-173">La atestación de TPM es el mejor intento.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-173">TPM attestation is a best effort.</span></span> <span data-ttu-id="6ebc2-174">Solo los equipos con el TPM 2,0 devolverán una declaración de atestación de TPM, y el proceso de atestación podría producir un error por varias razones.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>
- <span data-ttu-id="6ebc2-175">Windows Hello emplea una variedad de formas para proteger las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-175">Windows Hello employs a variety of ways to protect user credentials.</span></span> <span data-ttu-id="6ebc2-176">Para comprobar qué método se ha usado para proteger una credencial, consume el campo [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) en el objeto atestación que se ha devuelto durante la creación de la credencial.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span> <span data-ttu-id="6ebc2-177">A continuación se muestra la lista de AAGUIDs que Windows Hello puede devolver:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span> 
  - <span data-ttu-id="6ebc2-178">Autenticadores devueltos por software</span><span class="sxs-lookup"><span data-stu-id="6ebc2-178">Software backed authenticators</span></span>
    - <span data-ttu-id="6ebc2-179">Autenticador de software de Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-179">Windows Hello software authenticator:</span></span> `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`
    - <span data-ttu-id="6ebc2-180">Autenticador de software Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-180">Windows Hello VBS software authenticator:</span></span> `6E96969E-A5CF-4AAD-9B56-305FE6C82795`
  - <span data-ttu-id="6ebc2-181">Autenticadores devueltos del módulo de plataforma segura (TPM)</span><span class="sxs-lookup"><span data-stu-id="6ebc2-181">Trusted Platform Module (TPM) backed authenticators</span></span>
    - <span data-ttu-id="6ebc2-182">Autenticador de hardware de Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-182">Windows Hello hardware authenticator:</span></span> `08987058-CADC-4B81-B6E1-30DE50DCBE96`
    - <span data-ttu-id="6ebc2-183">Autenticador de hardware Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="6ebc2-183">Windows Hello VBS hardware authenticator:</span></span> `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`


### <span data-ttu-id="6ebc2-184">Superficie de la API</span><span class="sxs-lookup"><span data-stu-id="6ebc2-184">API surface</span></span>
- <span data-ttu-id="6ebc2-185">Microsoft Edge tiene una implementación completa de la versión de recomendación candidata de la especificación de autenticación Web básica.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>
- <span data-ttu-id="6ebc2-186">La [extensión AppID](https://w3c.github.io/webauthn/#sctn-appid-extension) es compatible.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-186">The [AppID extension](https://w3c.github.io/webauthn/#sctn-appid-extension) is supported.</span></span> 
- <span data-ttu-id="6ebc2-187">No se admite ninguna otra extensión.</span><span class="sxs-lookup"><span data-stu-id="6ebc2-187">No other extensions are supported.</span></span>


## <span data-ttu-id="6ebc2-188">Demos</span><span class="sxs-lookup"><span data-stu-id="6ebc2-188">Demos</span></span>

[<span data-ttu-id="6ebc2-189">Ejemplo de código de cliente y servidor</span><span class="sxs-lookup"><span data-stu-id="6ebc2-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)

[<span data-ttu-id="6ebc2-190">Demostración de Windows Hello Test Drive</span><span class="sxs-lookup"><span data-stu-id="6ebc2-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net/)

## <span data-ttu-id="6ebc2-191">Estadístico</span><span class="sxs-lookup"><span data-stu-id="6ebc2-191">Specification</span></span>

[<span data-ttu-id="6ebc2-192">Autenticación Web: una API para obtener acceso a las credenciales de clave pública</span><span class="sxs-lookup"><span data-stu-id="6ebc2-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn/)
