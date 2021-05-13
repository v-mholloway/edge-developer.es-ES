---
description: Emular Autenticadores y Depurar WebAuthn en Microsoft Edge DevTools.
title: Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d5eeedfaa98e56bbba81634685a223844803a1ad
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564038"
---
# <a name="emulate-authenticators-and-debug-webauthn-in-microsoft-edge-devtools"></a><span data-ttu-id="211a9-104">Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="211a9-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="211a9-105">En lugar de depurar la autenticación web en tu sitio web o aplicación con autenticadores físicos, usa la herramienta **WebAuthn** en Microsoft Edge DevTools para crear e interactuar con autenticadores virtuales basados en software.</span><span class="sxs-lookup"><span data-stu-id="211a9-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="211a9-106">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="211a9-106">Before you begin</span></span>  

<span data-ttu-id="211a9-107">Un excelente lugar para empezar a usar la autenticación web es la especificación [de la API de autenticación web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="211a9-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <a name="set-up-the-webauthn-tool"></a><span data-ttu-id="211a9-108">Configurar la herramienta WebAuthn</span><span class="sxs-lookup"><span data-stu-id="211a9-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="211a9-109">Navegue a una página web que use WebAuthn, como el siguiente sitio web de demostración.</span><span class="sxs-lookup"><span data-stu-id="211a9-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="211a9-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="211a9-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="211a9-111">Inicie sesión en el sitio web.</span><span class="sxs-lookup"><span data-stu-id="211a9-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="211a9-112">[Abra DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="211a9-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="211a9-113">Para abrir la **herramienta WebAuthn,** elija el icono Personalizar y **controlar DevTools** \( \) > `...` Más **herramientas**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="211a9-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Herramienta WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="211a9-115">**Herramienta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="211a9-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="211a9-116">En la **herramienta WebAuthn,** active la casilla Habilitar **entorno de autenticación virtual.**</span><span class="sxs-lookup"><span data-stu-id="211a9-116">In the **WebAuthn** tool, turn on **Enable virtual authenticator environment** checkbox.</span></span>  
1.  <span data-ttu-id="211a9-117">Una vez habilitada, se muestra una nueva sección denominada **Nuevo autenticador.**</span><span class="sxs-lookup"><span data-stu-id="211a9-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Habilitar el entorno de autenticación virtual" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="211a9-119">Habilitar el entorno de autenticación virtual</span><span class="sxs-lookup"><span data-stu-id="211a9-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="211a9-120">En la **sección Nuevo autenticador,** configure las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="211a9-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="211a9-121">Opción</span><span class="sxs-lookup"><span data-stu-id="211a9-121">Option</span></span> | <span data-ttu-id="211a9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="211a9-122">Value</span></span> | <span data-ttu-id="211a9-123">Detalles</span><span class="sxs-lookup"><span data-stu-id="211a9-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="211a9-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] o [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="211a9-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="211a9-125">El protocolo que usa el autenticador virtual para codificar y decodificar</span><span class="sxs-lookup"><span data-stu-id="211a9-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="211a9-126">, `nfc` , `ble` o</span><span class="sxs-lookup"><span data-stu-id="211a9-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="211a9-127">El autenticador virtual simula el transporte seleccionado para comunicarse con los clientes con el fin de obtener una aserción para una credencial específica.</span><span class="sxs-lookup"><span data-stu-id="211a9-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="211a9-128">Para obtener más información, vaya [a Authenticator enumeración de transporte][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="211a9-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="211a9-129">Activar \(o desactivar\) con la casilla</span><span class="sxs-lookup"><span data-stu-id="211a9-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="211a9-130">Activar si la aplicación web se basa en claves residentes \(también conocidas como credenciales detectables del lado cliente\).</span><span class="sxs-lookup"><span data-stu-id="211a9-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="211a9-131">Para obtener más información, vaya a [Enumeración de requisitos de clave residente][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="211a9-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="211a9-132">Activar \(o desactivar\) con la casilla</span><span class="sxs-lookup"><span data-stu-id="211a9-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="211a9-133">Activar si la aplicación web se basa en la autorización local mediante modalidades de gestos como el código táctil más pin, la entrada de contraseña o el reconocimiento biométrico.</span><span class="sxs-lookup"><span data-stu-id="211a9-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="211a9-134">Para obtener más información, vaya a [Verificación de usuarios][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="211a9-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="211a9-135">Elija el **botón** Agregar.</span><span class="sxs-lookup"><span data-stu-id="211a9-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="211a9-136">Se muestra una nueva sección del autenticador recién creado.</span><span class="sxs-lookup"><span data-stu-id="211a9-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="211a9-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="211a9-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="211a9-139">La **Authenticator** incluye una **tabla Credenciales.**</span><span class="sxs-lookup"><span data-stu-id="211a9-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="211a9-140">La tabla está vacía hasta que se registra una credencial en el autenticador.</span><span class="sxs-lookup"><span data-stu-id="211a9-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Sin credenciales" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="211a9-142">Sin credenciales</span><span class="sxs-lookup"><span data-stu-id="211a9-142">No credentials</span></span>  
:::image-end:::  

## <a name="register-a-new-credential"></a><span data-ttu-id="211a9-143">Registrar una nueva credencial</span><span class="sxs-lookup"><span data-stu-id="211a9-143">Register a new credential</span></span>  

<span data-ttu-id="211a9-144">Para registrar una nueva credencial, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="211a9-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="211a9-145">Para obtener más información acerca de lo que está haciendo la [API de][GithubW3cWebauthn] autenticación web al registrar una nueva credencial, vaya a Crear una [nueva credencial][GithubW3cWebauthnSctnCreatecredential].</span><span class="sxs-lookup"><span data-stu-id="211a9-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="211a9-146">En el sitio web de demostración, elija **Registrar nueva credencial**.</span><span class="sxs-lookup"><span data-stu-id="211a9-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="211a9-147">Ahora se agrega una nueva credencial a la **tabla Credenciales** de la herramienta WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="211a9-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Ver credenciales" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="211a9-149">Ver credenciales</span><span class="sxs-lookup"><span data-stu-id="211a9-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="211a9-150">En el sitio web de demostración, elija el **botón Autenticar.**</span><span class="sxs-lookup"><span data-stu-id="211a9-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="211a9-151">Compruebe que el [número de signos][GithubW3cWebauthnSctnSignCounter] de la credencial de la tabla **Credenciales** aumentó en 1, lo que marca una operación [authenticatorGetAssertion correcta.][GithubW3cWebauthnAuthenticatorgetassertion]</span><span class="sxs-lookup"><span data-stu-id="211a9-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <a name="export-and-remove-credentials"></a><span data-ttu-id="211a9-152">Exportar y quitar credenciales</span><span class="sxs-lookup"><span data-stu-id="211a9-152">Export and remove credentials</span></span>  

<span data-ttu-id="211a9-153">Para exportar o quitar una credencial, elija el **botón Exportar** **o** Quitar.</span><span class="sxs-lookup"><span data-stu-id="211a9-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportar o quitar una credencial" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="211a9-155">Exportar o quitar una credencial</span><span class="sxs-lookup"><span data-stu-id="211a9-155">Export or remove a credential</span></span>  
:::image-end:::  

## <a name="rename-an-authenticator"></a><span data-ttu-id="211a9-156">Cambiar el nombre de un autenticador</span><span class="sxs-lookup"><span data-stu-id="211a9-156">Rename an authenticator</span></span>  

<span data-ttu-id="211a9-157">Para cambiar el nombre de un autenticador, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="211a9-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="211a9-158">Junto al nombre del autenticador, elija el **botón** Editar.</span><span class="sxs-lookup"><span data-stu-id="211a9-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="211a9-159">Edite el nombre y, a continuación, **elija Entrar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="211a9-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Cambiar el nombre de un autenticador" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="211a9-161">Cambiar el nombre de un autenticador</span><span class="sxs-lookup"><span data-stu-id="211a9-161">Rename an authenticator</span></span>  
:::image-end:::  

## <a name="set-the-active-authenticator"></a><span data-ttu-id="211a9-162">Establecer el autenticador activo</span><span class="sxs-lookup"><span data-stu-id="211a9-162">Set the active authenticator</span></span>  

<span data-ttu-id="211a9-163">Un autenticador recién creado se activa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="211a9-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="211a9-164">Para usar otro autenticador virtual, elija el **botón de** radio Activo junto al autenticador.</span><span class="sxs-lookup"><span data-stu-id="211a9-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="211a9-165">DevTools solo admite un autenticador virtual activo en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="211a9-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="211a9-166">Si quita el autenticador activo, otro autenticador no se activará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="211a9-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Establecer autenticador activo" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="211a9-168">Establecer autenticador activo</span><span class="sxs-lookup"><span data-stu-id="211a9-168">Set active authenticator</span></span>  
:::image-end:::  

## <a name="remove-a-virtual-authenticator"></a><span data-ttu-id="211a9-169">Quitar un autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="211a9-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="211a9-170">Para quitar un autenticador virtual, junto al autenticador, elija el **botón** Quitar.</span><span class="sxs-lookup"><span data-stu-id="211a9-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Quitar autenticador" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="211a9-172">Quitar autenticador</span><span class="sxs-lookup"><span data-stu-id="211a9-172">Remove authenticator</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="211a9-173">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="211a9-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demostración de webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocolo de Authenticator (CTAP) | alianza de fido"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Información general sobre el factor universal 2nd (U2F) | alianza de fido"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "La operación authenticatorGetAssertion: autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Enumeración de transporte (enumeración AuthenticatorTransport): autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeración de requisitos de clave residente (enumeración ResidentKeyRequirement): autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Comprobación del usuario: autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential's [[Create]](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Consideraciones del contador de firmas: autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="211a9-185">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="211a9-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="211a9-186">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="211a9-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="211a9-188">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="211a9-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
