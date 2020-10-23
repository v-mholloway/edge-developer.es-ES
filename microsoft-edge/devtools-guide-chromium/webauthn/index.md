---
description: Emular autenticadores y depurar webauthn en Microsoft Edge DevTools.
title: Emular autenticadores y depurar webauthn en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6727e9aeea1a51689a80570a2f1c9df880a8c9db
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134234"
---
# <span data-ttu-id="29158-104">Emular autenticadores y depurar webauthn en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="29158-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="29158-105">En lugar de depurar la autenticación Web en su sitio web o aplicación con autenticadores físicos, use la herramienta **Webauthn** en Microsoft Edge DevTools para crear e interactuar con autenticadores virtuales basados en software.</span><span class="sxs-lookup"><span data-stu-id="29158-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="29158-106">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="29158-106">Before you begin</span></span>  

<span data-ttu-id="29158-107">Un buen lugar para empezar a usar la autenticación Web es la [especificación de API de autenticación Web][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="29158-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="29158-108">Configurar la herramienta webauthn</span><span class="sxs-lookup"><span data-stu-id="29158-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="29158-109">Vaya a una página web que use webauthn, como el siguiente sitio web de demostración.</span><span class="sxs-lookup"><span data-stu-id="29158-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="29158-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="29158-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="29158-111">Inicie sesión en el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="29158-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="29158-112">[Abra DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="29158-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="29158-113">Para abrir la herramienta **webauthn** , elija el icono **personalizar y controlar DevTools** \ ( `...` \) > **más herramientas**  >  **webauthn**.</span><span class="sxs-lookup"><span data-stu-id="29158-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="29158-115">Herramienta **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="29158-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="29158-116">En la herramienta **Webauthn** , elija la casilla que se encuentra junto a **Habilitar el entorno de autenticador virtual**.</span><span class="sxs-lookup"><span data-stu-id="29158-116">In the **WebAuthn** tool, choose the checkbox next to **Enable virtual authenticator environment**.</span></span>  
1.  <span data-ttu-id="29158-117">Una vez que se haya habilitado, aparecerá una nueva sección llamada **nuevo autenticador** .</span><span class="sxs-lookup"><span data-stu-id="29158-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="29158-119">Habilitar el entorno de autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="29158-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="29158-120">En la sección **nuevo autenticador** , configure las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="29158-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="29158-121">Opción</span><span class="sxs-lookup"><span data-stu-id="29158-121">Option</span></span> | <span data-ttu-id="29158-122">Valor</span><span class="sxs-lookup"><span data-stu-id="29158-122">Value</span></span> | <span data-ttu-id="29158-123">Detalles</span><span class="sxs-lookup"><span data-stu-id="29158-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="29158-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] o [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="29158-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="29158-125">El protocolo que el autenticador virtual usa para codificar y descodificar</span><span class="sxs-lookup"><span data-stu-id="29158-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="29158-126">, `nfc` , `ble` o</span><span class="sxs-lookup"><span data-stu-id="29158-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="29158-127">El autenticador virtual simula el transporte seleccionado para comunicarse con los clientes a fin de obtener una aserción para una credencial específica.</span><span class="sxs-lookup"><span data-stu-id="29158-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="29158-128">Para obtener más información, vaya a la [enumeración de transporte de autenticador][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="29158-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="29158-129">Activar \ (o desactivar \) con la casilla</span><span class="sxs-lookup"><span data-stu-id="29158-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="29158-130">Active esta opción si su aplicación web depende de las claves residentes \ (también conocidas como credenciales detectables del cliente \).</span><span class="sxs-lookup"><span data-stu-id="29158-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="29158-131">Para obtener más información, vaya a la [enumeración de requisitos clave residente][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="29158-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="29158-132">Activar \ (o desactivar \) con la casilla</span><span class="sxs-lookup"><span data-stu-id="29158-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="29158-133">Active esta opción si su aplicación web se basa en la autorización local con modalidades de gestos como toque, código PIN, entrada de contraseña o reconocimiento biométrico.</span><span class="sxs-lookup"><span data-stu-id="29158-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="29158-134">Para obtener más información, vaya a verificación por el [usuario][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="29158-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="29158-135">Elija el botón **Agregar** .</span><span class="sxs-lookup"><span data-stu-id="29158-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="29158-136">Aparece una nueva sección del autenticador recién creado.</span><span class="sxs-lookup"><span data-stu-id="29158-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="29158-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="29158-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="29158-139">La sección **Authenticator** incluye una tabla de **credenciales** .</span><span class="sxs-lookup"><span data-stu-id="29158-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="29158-140">La tabla está vacía hasta que se registra una credencial para el autenticador.</span><span class="sxs-lookup"><span data-stu-id="29158-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="29158-142">No hay credenciales</span><span class="sxs-lookup"><span data-stu-id="29158-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="29158-143">Registrar una nueva credencial</span><span class="sxs-lookup"><span data-stu-id="29158-143">Register a new credential</span></span>  

<span data-ttu-id="29158-144">Siga los pasos que se indican a continuación para registrar una nueva credencial.</span><span class="sxs-lookup"><span data-stu-id="29158-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="29158-145">Para obtener más información sobre lo que hace la [API de autenticación Web][GithubW3cWebauthn] al registrar una credencial nueva, vaya a [crear una credencial nueva][GithubW3cWebauthnSctnCreatecredential].</span><span class="sxs-lookup"><span data-stu-id="29158-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="29158-146">En el sitio web de demostración, elija **registrar nueva credencial**.</span><span class="sxs-lookup"><span data-stu-id="29158-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="29158-147">Ahora se agrega una nueva credencial a la tabla de **credenciales** en la herramienta webauthn.</span><span class="sxs-lookup"><span data-stu-id="29158-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="29158-149">Ver credenciales</span><span class="sxs-lookup"><span data-stu-id="29158-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="29158-150">En el sitio web de demostración, elija el botón **autenticar** .</span><span class="sxs-lookup"><span data-stu-id="29158-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="29158-151">Compruebe que el [recuento de firma][GithubW3cWebauthnSctnSignCounter] de la credencial en la tabla de **credenciales** aumentó en 1, lo que marca una operación de [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] correcta.</span><span class="sxs-lookup"><span data-stu-id="29158-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="29158-152">Exportar y quitar credenciales</span><span class="sxs-lookup"><span data-stu-id="29158-152">Export and remove credentials</span></span>  

<span data-ttu-id="29158-153">Para exportar o quitar una credencial, seleccione el botón **exportar** o **quitar** .</span><span class="sxs-lookup"><span data-stu-id="29158-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="29158-155">Exportar o quitar una credencial</span><span class="sxs-lookup"><span data-stu-id="29158-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="29158-156">Cambiar el nombre de un autenticador</span><span class="sxs-lookup"><span data-stu-id="29158-156">Rename an authenticator</span></span>  

<span data-ttu-id="29158-157">Para cambiar el nombre de un autenticador, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="29158-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="29158-158">Junto al nombre de autenticador, seleccione el botón **Editar** .</span><span class="sxs-lookup"><span data-stu-id="29158-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="29158-159">Edite el nombre y, a continuación, elija **entrar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="29158-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="29158-161">Cambiar el nombre de un autenticador</span><span class="sxs-lookup"><span data-stu-id="29158-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="29158-162">Establecer el autenticador activo</span><span class="sxs-lookup"><span data-stu-id="29158-162">Set the active authenticator</span></span>  

<span data-ttu-id="29158-163">Un autenticador recién creado se activa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="29158-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="29158-164">Para usar otro autenticador virtual, seleccione el botón de radio **activo** junto al autenticador.</span><span class="sxs-lookup"><span data-stu-id="29158-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="29158-165">DevTools solo admite autenticadores virtuales activos en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="29158-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="29158-166">Si quita el autenticador activo, otro autenticador no se activará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="29158-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="29158-168">Establecer autenticador activo</span><span class="sxs-lookup"><span data-stu-id="29158-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="29158-169">Quitar un autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="29158-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="29158-170">Para quitar un autenticador virtual, junto al autenticador, seleccione el botón **quitar** .</span><span class="sxs-lookup"><span data-stu-id="29158-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="29158-172">Quitar autenticador</span><span class="sxs-lookup"><span data-stu-id="29158-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="29158-173">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="29158-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demostración de webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocolo de cliente a autenticador (CTAP) | Fido Alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "2º factor universal (U2F) Descripción general | Fido Alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "La operación authenticatorGetAssertion-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Enumeración de transporte de autenticadores (enumeración de AuthenticatorTransport)-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | RELATIVA"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeración de requisitos clave residentes (enumeración ResidentKeyRequirement)-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | RELATIVA"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Verificación de usuario: autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | RELATIVA"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Crear una nueva credencial-PublicKeyCredential [[Create]] (origen, opciones, sameOriginWithAncestors) método-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Consideraciones del contador de firmas: autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="29158-185">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="29158-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="29158-186">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="29158-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="29158-188">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="29158-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
