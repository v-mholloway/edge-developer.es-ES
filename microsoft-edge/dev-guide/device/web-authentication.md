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
# <span data-ttu-id="b8efa-104">Autenticación Web y Windows Hello</span><span class="sxs-lookup"><span data-stu-id="b8efa-104">Web authentication and Windows Hello</span></span>

<span data-ttu-id="b8efa-105">La API de autenticación Web (anteriormente *FIDO 2,0* ) en Microsoft Edge permite a las aplicaciones web usar [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometría para la autenticación de usuarios, de modo que usted y sus usuarios puedan evitar todos los problemas y riesgos de la administración de contraseñas, entre los que se incluyen averiguaciones de contraseñas, suplantación de identidad y ataques de keylogging.</span><span class="sxs-lookup"><span data-stu-id="b8efa-105">The Web Authentication (formerly *FIDO 2.0* ) API in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometrics for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and keylogging attacks.</span></span> <span data-ttu-id="b8efa-106">La implementación actual de Microsoft Edge (*MS-* Fixed) se basa en un borrador anterior de la especificación de autenticación Web y es probable que cambie en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b8efa-106">The current Microsoft Edge (*ms-* prefixed) implementation is based on an earlier draft of the Web Authentication specification and is likely to change in the future.</span></span> **<span data-ttu-id="b8efa-107">En este tema se explica cómo probar la autenticación de Windows Hello con Microsoft Edge, así como el código de las actualizaciones del explorador.</span><span class="sxs-lookup"><span data-stu-id="b8efa-107">This topic will show you how to try out Windows Hello authentication with Microsoft Edge while also future-proofing your code against browser updates.</span></span>**

<span data-ttu-id="b8efa-108">La API de autenticación Web es un estándar emergente establecido por la [Alianza de Fido](https://fidoalliance.org/) con el objetivo de ofrecer una manera interoperable de realizar la autenticación Web con Windows Hello y otros dispositivos biométricos en exploradores.</span><span class="sxs-lookup"><span data-stu-id="b8efa-108">The Web Authentication API is an emerging standard put forth by the [FIDO Alliance](https://fidoalliance.org/) with the aim of providing an interoperable way of doing web authentication using Windows Hello and other biometric devices across browsers.</span></span> <span data-ttu-id="b8efa-109">La especificación de autenticación Web define dos escenarios de autenticación: menos de contraseña y dos factores.</span><span class="sxs-lookup"><span data-stu-id="b8efa-109">The Web Authentication specification defines two authentication scenarios: password-less and two factor.</span></span> <span data-ttu-id="b8efa-110">En el caso de que no haya contraseña, el usuario no tiene que iniciar sesión en la página web con un nombre de usuario o una contraseña, ya que puede iniciar sesión únicamente con Windows Hello.</span><span class="sxs-lookup"><span data-stu-id="b8efa-110">In the password-less case, the user does not need to log into the web page using a user name or password – they can login solely using Windows Hello.</span></span> <span data-ttu-id="b8efa-111">En el caso de dos factores, el usuario inicia sesión normalmente con un nombre de usuario y una contraseña, pero Windows Hello se usa como una comprobación de segundo factor para que la autenticación general sea más segura.</span><span class="sxs-lookup"><span data-stu-id="b8efa-111">In the two factor case, the user logs in normally using a username and password, but Windows Hello is used as a second factor check to make the overall authentication stronger.</span></span>

<span data-ttu-id="b8efa-112">Con la autenticación Web combinada con Windows Hello, el servidor envía un desafío de texto sin formato al explorador.</span><span class="sxs-lookup"><span data-stu-id="b8efa-112">Using Web Authentication combined with Windows Hello, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="b8efa-113">Una vez que Microsoft Edge puede comprobar el usuario a través de Windows Hello, el sistema firmará el desafío con una clave privada que previamente se aprovisionó para este usuario y enviaba la firma de vuelta al servidor.</span><span class="sxs-lookup"><span data-stu-id="b8efa-113">Once Microsoft Edge is able to verify the user through Windows Hello, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="b8efa-114">Si el servidor puede validar la firma con la clave pública que tiene para ese usuario y comprobar que el desafío es correcto, puede autenticar al usuario de forma segura.</span><span class="sxs-lookup"><span data-stu-id="b8efa-114">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="b8efa-115">Con la [Criptografía asimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como esta, la clave pública no tiene sentido por sí misma y la clave privada nunca se comparte.</span><span class="sxs-lookup"><span data-stu-id="b8efa-115">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="b8efa-116">Además, la clave privada nunca se puede mover desde sistemas modernos con hardware habilitado para TPM.</span><span class="sxs-lookup"><span data-stu-id="b8efa-116">Furthermore, the private key can never be moved from modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="b8efa-117">Existen dos pasos básicos para usar la API de autenticación Web:</span><span class="sxs-lookup"><span data-stu-id="b8efa-117">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="b8efa-118">1. registrar a un usuario con</span><span class="sxs-lookup"><span data-stu-id="b8efa-118">1. Register your user with</span></span> `makeCredential`**

**<span data-ttu-id="b8efa-119">2. autenticar al usuario con</span><span class="sxs-lookup"><span data-stu-id="b8efa-119">2. Authenticate your user with</span></span> `getAssertion`**

<span data-ttu-id="b8efa-120">El siguiente paso le guiará a través de este flujo mediante el [rellenador recomendado de webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span><span class="sxs-lookup"><span data-stu-id="b8efa-120">The following will walk you through this flow using the recommended [Webauthn.js polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span></span> <span data-ttu-id="b8efa-121">El [código completo](https://github.com/adrianba/fido-snippets/) está disponible para este servidor y demostración de cliente.</span><span class="sxs-lookup"><span data-stu-id="b8efa-121">The [complete code](https://github.com/adrianba/fido-snippets/) is available for this server and client side demo.</span></span> <span data-ttu-id="b8efa-122">Las versiones del lado del servidor de [C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [php](https://github.com/adrianba/fido-snippets/tree/master/php)y [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b8efa-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php), and [Node.JS](https://github.com/adrianba/fido-snippets/tree/master/nodejs) server side versions are available.</span></span>

## <span data-ttu-id="b8efa-123">Registrar el usuario</span><span class="sxs-lookup"><span data-stu-id="b8efa-123">Register your user</span></span>

<span data-ttu-id="b8efa-124">Actuando como *proveedor de identidad*, primero deberá crear una credencial de autenticación Web para su usuario con la ventana. webauthn. método **makeCredential** .</span><span class="sxs-lookup"><span data-stu-id="b8efa-124">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the window.webauthn.**makeCredential** method.</span></span> <span data-ttu-id="b8efa-125">Antes de registrar la credencial en el servidor, tendrá que confirmar la identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="b8efa-125">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="b8efa-126">Esto se puede hacer enviando al usuario una confirmación por correo electrónico o pidiéndole que use su método de inicio de sesión tradicional.</span><span class="sxs-lookup"><span data-stu-id="b8efa-126">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>

<span data-ttu-id="b8efa-127">El método makeCredential toma los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="b8efa-127">The makeCredential method takes the following parameters:</span></span>
 - **<span data-ttu-id="b8efa-128">información de la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="b8efa-128">user account information</span></span>**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **<span data-ttu-id="b8efa-129">parámetros criptográficos</span><span class="sxs-lookup"><span data-stu-id="b8efa-129">crypto parameters</span></span>**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

<span data-ttu-id="b8efa-130">La promesa resultante devuelve un objeto que representa la credencial que se enviará de vuelta al servidor para validar autenticaciones futuras:</span><span class="sxs-lookup"><span data-stu-id="b8efa-130">The resulting promise returns an object representing the credential that you then send back to the server for validating future authentications:</span></span>

**<span data-ttu-id="b8efa-131">Cliente</span><span class="sxs-lookup"><span data-stu-id="b8efa-131">Client</span></span>**

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

<span data-ttu-id="b8efa-132">Cuando use el método makeCredential, Microsoft Edge primero pedirá a Windows Hello que use la imagen del rostro o de huella dactilar para comprobar que el usuario es el mismo usuario que ha iniciado sesión en la cuenta de Windows.</span><span class="sxs-lookup"><span data-stu-id="b8efa-132">When you use the makeCredential method, Microsoft Edge will first ask Windows Hello to use face or fingerprint identification to verify that the user is the same user as the one logged into the Windows account.</span></span> <span data-ttu-id="b8efa-133">Una vez completado este paso, Microsoft Passport generará un par de claves pública y privada y almacenará la clave privada en el módulo de plataforma segura (TPM), el hardware de procesador criptográfico dedicado usado para almacenar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="b8efa-133">Once this step is completed, Microsoft Passport will generate a public/private key pair and store the private key in the Trusted Platform Module (TPM), the dedicated crypto processor hardware used to store credentials.</span></span> <span data-ttu-id="b8efa-134">Si el usuario no tiene un dispositivo habilitado para TPM, estas claves se almacenarán en el software.</span><span class="sxs-lookup"><span data-stu-id="b8efa-134">If the user doesn’t have a TPM enabled device, these keys will be stored in software.</span></span> <span data-ttu-id="b8efa-135">Estas credenciales se crean por origen, por cuenta de Windows, y no se pueden mover porque están ligadas al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8efa-135">These credentials are created per origin, per Windows account, and will not be roamed because they are tied to the device.</span></span> <span data-ttu-id="b8efa-136">Esto significa que tendrás que asegurarte de que el usuario se registre para usar Windows Hello para cada dispositivo que usen.</span><span class="sxs-lookup"><span data-stu-id="b8efa-136">This means that you’ll need to make sure the user registers to use Windows Hello for every device they use.</span></span>

## <span data-ttu-id="b8efa-137">Autenticar al usuario</span><span class="sxs-lookup"><span data-stu-id="b8efa-137">Authenticate your user</span></span>

<span data-ttu-id="b8efa-138">Una vez que se crea la credencial en el cliente, la próxima vez que el usuario intente iniciar sesión en el sitio, podrá ofrecer su firma con Windows Hello en lugar de una contraseña con una llamada a Window. webauthn. **getAssertion**.</span><span class="sxs-lookup"><span data-stu-id="b8efa-138">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using Windows Hello instead of a password with a call to window.webauthn.**getAssertion**.</span></span>

<span data-ttu-id="b8efa-139">El método getAssertion toma el *desafío* como su único parámetro obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8efa-139">The getAssertion method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="b8efa-140">El desafío es la cantidad generada al azar que el servidor enviará a un cliente para que inicie sesión con la clave privada del usuario.</span><span class="sxs-lookup"><span data-stu-id="b8efa-140">The challenge is the randomly generated quantity that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="b8efa-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b8efa-141">For example:</span></span>

**<span data-ttu-id="b8efa-142">Servidor</span><span class="sxs-lookup"><span data-stu-id="b8efa-142">Server</span></span>**

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

<span data-ttu-id="b8efa-143">Una vez que se realice la llamada getAssertion, Microsoft Edge mostrará el mensaje de Windows Hello, que verificará la identidad del usuario mediante biometría.</span><span class="sxs-lookup"><span data-stu-id="b8efa-143">Once the getAssertion call is made, Microsoft Edge will show the Windows Hello prompt, which will verify the identity of the user using biometrics.</span></span> <span data-ttu-id="b8efa-144">Una vez que se haya verificado el usuario, el desafío se firmará en el TPM y la promesa devolverá un objeto de aserción que contiene la firma y otros metadatos que se enviarán al servidor:</span><span class="sxs-lookup"><span data-stu-id="b8efa-144">After the user is verified, the challenge will be signed within the TPM and the promise will return with an assertion object that contains the signature and other metadata for you to send to the server:</span></span>

**<span data-ttu-id="b8efa-145">Cliente</span><span class="sxs-lookup"><span data-stu-id="b8efa-145">Client</span></span>**

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

<span data-ttu-id="b8efa-146">Una vez que reciba la aserción en el servidor, tendrá que validar la firma para autenticar al usuario.</span><span class="sxs-lookup"><span data-stu-id="b8efa-146">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="b8efa-147">Por ejemplo (en node. JS):</span><span class="sxs-lookup"><span data-stu-id="b8efa-147">For example (in Node.JS):</span></span>

**<span data-ttu-id="b8efa-148">Servidor</span><span class="sxs-lookup"><span data-stu-id="b8efa-148">Server</span></span>**

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

## <span data-ttu-id="b8efa-149">Diferencias entre Microsoft Edge y las especificaciones</span><span class="sxs-lookup"><span data-stu-id="b8efa-149">Differences between Microsoft Edge and the spec</span></span>

> [!NOTE]
> <span data-ttu-id="b8efa-150">Al probar la API de autenticación Web con Windows Hello en Microsoft Edge, te recomendamos que uses el rellenador webauthn. js, como se muestra anteriormente, para evitar tener que contar las discrepancias que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="b8efa-150">When trying out the Web Authentication API with Windows Hello in Microsoft Edge, we recommend using the Webauthn.js polyfill as shown above to avoid having to account for the discrepancies listed here.</span></span> <span data-ttu-id="b8efa-151">Actualizaremos este polyfill por cada versión publicada importante de la especificación.</span><span class="sxs-lookup"><span data-stu-id="b8efa-151">We'll update this polyfill for every major published version of the specification.</span></span>


<span data-ttu-id="b8efa-152">La implementación actual de Microsoft Edge se basa en un borrador anterior de la especificación de autenticación Web y es probable que cambie en compilaciones futuras y que la especificación evolucione.</span><span class="sxs-lookup"><span data-stu-id="b8efa-152">The current Microsoft Edge implementation is based on an earlier draft of the Web Authentication specification and is likely to change in future builds and as the spec evolves.</span></span> <span data-ttu-id="b8efa-153">Las diferencias actuales son:</span><span class="sxs-lookup"><span data-stu-id="b8efa-153">The current differences include:</span></span>

- <span data-ttu-id="b8efa-154">Las API de Microsoft Edge son MS-prefijado.</span><span class="sxs-lookup"><span data-stu-id="b8efa-154">Microsoft Edge APIs are MS- prefixed.</span></span>
- <span data-ttu-id="b8efa-155">Microsoft Edge aún no admite credenciales externas como SerialKeys o dispositivos Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b8efa-155">Microsoft Edge does not yet support external credentials like USB keys or Bluetooth devices.</span></span> <span data-ttu-id="b8efa-156">La API actual está limitada a las credenciales incrustadas almacenadas en el TPM.</span><span class="sxs-lookup"><span data-stu-id="b8efa-156">The current API is limited to embedded credentials stored in the TPM.</span></span>
- <span data-ttu-id="b8efa-157">La cuenta de usuario de Windows actualmente conectada debe estar configurada para admitir al menos un PIN y, preferiblemente, una cara o una biometría de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="b8efa-157">The currently logged in Windows user account must be configured to support at least a PIN, and preferably face or fingerprint biometrics.</span></span> <span data-ttu-id="b8efa-158">Esto garantiza que Windows pueda autenticar el acceso al TPM.</span><span class="sxs-lookup"><span data-stu-id="b8efa-158">This is to ensure that Windows can authenticate the access to the TPM.</span></span>
- <span data-ttu-id="b8efa-159">La implementación de Microsoft Edge aún no admite la experiencia del selector de cuentas.</span><span class="sxs-lookup"><span data-stu-id="b8efa-159">The Microsoft Edge implementation does not yet support the account picker experience.</span></span>
- <span data-ttu-id="b8efa-160">En este momento se requiere un segundo parámetro de *filtros* que especifique el identificador de credencial para las llamadas a msCredentials. [getAssertion](https://msdn.microsoft.com/library/mt697640).</span><span class="sxs-lookup"><span data-stu-id="b8efa-160">A second *filters* parameter specifying the credential id is currently required for calls to msCredentials.[getAssertion](https://msdn.microsoft.com/library/mt697640).</span></span> <span data-ttu-id="b8efa-161">Como tal, tendrá que almacenar la información del identificador de credenciales en almacenamiento local en el cliente, ya sea en indexDB o localStorage al crear las credenciales.</span><span class="sxs-lookup"><span data-stu-id="b8efa-161">As such, you’ll need to store your credential ID information in local storage on the client, either in indexDB or localStorage when making your credential.</span></span> <span data-ttu-id="b8efa-162">Si un usuario elimina el historial de navegación, incluido el almacenamiento local, tendrá que volver a registrarse para usar Windows Hello la próxima vez que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="b8efa-162">If a user deletes their browsing history, including local storage, they will need to re-register to use Windows Hello the next time they log in.</span></span>
- <span data-ttu-id="b8efa-163">Microsoft Edge no admite todas las opciones del borrador de especificación de autenticación de Web actual, como extensiones o tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="b8efa-163">Microsoft Edge does not support all of the options in the current Web Authentication specification draft, such as extensions or timeouts.</span></span>

<span data-ttu-id="b8efa-164">En este último punto, se destacan las diferencias específicas de Microsoft Edge en las siguientes definiciones de especificación de autenticación Web:</span><span class="sxs-lookup"><span data-stu-id="b8efa-164">On that last point, the specific Microsoft Edge differences are noted in the following Web Authentication spec definitions:</span></span>

### <span data-ttu-id="b8efa-165">Especificación W3C</span><span class="sxs-lookup"><span data-stu-id="b8efa-165">W3C spec</span></span>

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



## <span data-ttu-id="b8efa-166">Referencia de API</span><span class="sxs-lookup"><span data-stu-id="b8efa-166">API Reference</span></span>

[<span data-ttu-id="b8efa-167">MSCredentials</span><span class="sxs-lookup"><span data-stu-id="b8efa-167">MSCredentials</span></span>](https://msdn.microsoft.com/library/mt697639)

[<span data-ttu-id="b8efa-168">makeCredential</span><span class="sxs-lookup"><span data-stu-id="b8efa-168">makeCredential</span></span>](https://msdn.microsoft.com/library/mt697641)

[<span data-ttu-id="b8efa-169">getAssertion</span><span class="sxs-lookup"><span data-stu-id="b8efa-169">getAssertion</span></span>](https://msdn.microsoft.com/library/mt697640)

## <span data-ttu-id="b8efa-170">Demos</span><span class="sxs-lookup"><span data-stu-id="b8efa-170">Demos</span></span>

[<span data-ttu-id="b8efa-171">Ejemplos de código de cliente y servidor</span><span class="sxs-lookup"><span data-stu-id="b8efa-171">Client and server code samples</span></span>](https://github.com/adrianba/fido-snippets/)

[<span data-ttu-id="b8efa-172">Polyfill de webauthn. js</span><span class="sxs-lookup"><span data-stu-id="b8efa-172">Webauthn.js polyfill</span></span>](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[<span data-ttu-id="b8efa-173">Demostración de Windows Hello Test Drive</span><span class="sxs-lookup"><span data-stu-id="b8efa-173">Windows Hello Test Drive demo</span></span>](https://testdrive-fido.azurewebsites.net/)

## <span data-ttu-id="b8efa-174">Estadístico</span><span class="sxs-lookup"><span data-stu-id="b8efa-174">Specification</span></span>

[<span data-ttu-id="b8efa-175">Autenticación Web: una API Web para acceder a las credenciales con ámbito 1</span><span class="sxs-lookup"><span data-stu-id="b8efa-175">Web Authentication: A Web API for accessing scoped credentials 1</span></span>](http://w3c.github.io/webauthn/)  
