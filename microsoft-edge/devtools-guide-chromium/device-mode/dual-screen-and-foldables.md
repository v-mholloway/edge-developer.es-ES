---
description: Usa dispositivos virtuales en Microsoft Edge para mejorar tu sitio web para dispositivos de doble pantalla y plegados.
title: Emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, emulación, dispositivo, simulación, móvil, pantalla doble, plegado, Surface Duo, Retenido de Samsung
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313368"
---
# <span data-ttu-id="8f360-104">Emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f360-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="8f360-105">En Microsoft Edge versión 89 o posterior, puedes emular los siguientes dispositivos de doble pantalla y plegados.</span><span class="sxs-lookup"><span data-stu-id="8f360-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="8f360-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="8f360-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="8f360-107">Redoblón Desdeso</span><span class="sxs-lookup"><span data-stu-id="8f360-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="8f360-108">Emula los dispositivos y alterna entre las siguientes posturas.</span><span class="sxs-lookup"><span data-stu-id="8f360-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="8f360-109">Posición de una sola pantalla o plegado</span><span class="sxs-lookup"><span data-stu-id="8f360-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="8f360-110">Posición de pantalla doble o desdoblada</span><span class="sxs-lookup"><span data-stu-id="8f360-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="8f360-111">Activa las API [experimentales](#turn-on-experimental-apis) de la plataforma web y usa la característica de pantalla multimedia [CSS][DualScreenDocsCssMedia] y la [API getWindowSegments][DualScreenDocsJSAPI] de JavaScript para mejorar tu sitio web \(o app\) para dispositivos de doble pantalla y plegados.</span><span class="sxs-lookup"><span data-stu-id="8f360-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular Surface Duo en Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="8f360-113">Emular Surface Duo en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8f360-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <span data-ttu-id="8f360-114">Activar las API experimentales</span><span class="sxs-lookup"><span data-stu-id="8f360-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="8f360-115">Para usar la característica [de pantalla][DualScreenDocsCssMedia] multimedia CSS y la [API getWindowSegments de JavaScript,][DualScreenDocsJSAPI]activa la marca en Microsoft `Experimental Web Platform features` Edge.</span><span class="sxs-lookup"><span data-stu-id="8f360-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="8f360-116">Complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f360-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="8f360-117">Vaya a `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="8f360-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="8f360-118">En el **cuadro de texto Marcas de** búsqueda, escriba , elija la marca de características de la plataforma web `Experimental Web Platform features` **experimental** y cambie **Deshabilitado** a **Habilitado.**</span><span class="sxs-lookup"><span data-stu-id="8f360-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="8f360-119">Reiniciar MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="8f360-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activar la marca de características de la plataforma web experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="8f360-121">Activar la marca **de características de la plataforma web** experimental</span><span class="sxs-lookup"><span data-stu-id="8f360-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8f360-122">Si usas consultas multimedia [CSS][DualScreenDocsCssMedia] o la API de enumeración de segmentos de Windows de [JavaScript][DualScreenDocsJSAPI] para mejorar tu sitio web o aplicación para [Surface Duo,][SurfaceDevicesDuo]también debes activar la marca de características de la plataforma **web experimental** en la aplicación De Microsoft Edge para [Android][GooglePlayMicrosoftEdge] en el dispositivo [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="8f360-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="8f360-123">Si la marca de características de la plataforma **web experimental** está activada en el escritorio de [Microsoft Edge][MicrosoftEdge] y desactivada en la aplicación De Microsoft Edge para [Android,][GooglePlayMicrosoftEdge]el comportamiento de tu sitio web o aplicación en el emulador de Surface Duo en el escritorio de Microsoft Edge no coincide con la aplicación [De Microsoft Edge][GooglePlayMicrosoftEdge] para Android en [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="8f360-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="8f360-124">Asegúrate de que las marcas coincidan en Microsoft Edge de escritorio y Android para usar correctamente el emulador de Surface Duo en el escritorio [de Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="8f360-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <span data-ttu-id="8f360-125">Prueba en dispositivos de doble pantalla y plegados</span><span class="sxs-lookup"><span data-stu-id="8f360-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="8f360-126">Cuando emulas [Surface Duo][SurfaceDevicesDuo] en una posición de pantalla doble en Microsoft Edge, la forma \(el espacio entre las dos pantallas\) se dibuja a través de tu sitio web o aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f360-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="8f360-127">La pantalla emulada coincide con la forma en que tu sitio web \(o app\) se representa en la aplicación [Microsoft Edge para Android][GooglePlayMicrosoftEdge] mientras se ejecuta en Surface [Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="8f360-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="8f360-128">Es posible que tenga que actualizar su sitio web \(o app\) para que se muestre mejor a lo largo de la seam.</span><span class="sxs-lookup"><span data-stu-id="8f360-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="8f360-129">Para obtener más información acerca de la adaptación de tu sitio web \(o app\) a la seam, ve a Cómo trabajar [con la seam][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="8f360-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="8f360-130">La [barra de herramientas del][DevtoolsDeviceModeIndexSimulateMobileViewport] dispositivo tiene características adicionales que te ayudarán a probar tu sitio web o aplicación en varias posturas y orientaciones.</span><span class="sxs-lookup"><span data-stu-id="8f360-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="8f360-131">Elige **Girar** \( Girar \) para girar la ventanilla ![ a orientación ](../media/rotate-dark-icon.msft.png) horizontal.</span><span class="sxs-lookup"><span data-stu-id="8f360-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="8f360-132">Combina la característica con **Span** \( Span \) para alternar entre una sola pantalla o con una pantalla doble o ![ ](../media/span-dark-icon.msft.png) posturas desenvolvadas.</span><span class="sxs-lookup"><span data-stu-id="8f360-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="8f360-133">Juntas, las características te permiten probar tu sitio web o aplicación en las cuatro posibles posturas y orientaciones.</span><span class="sxs-lookup"><span data-stu-id="8f360-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegados" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="8f360-135">Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegados</span><span class="sxs-lookup"><span data-stu-id="8f360-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="8f360-136">El **icono características de la plataforma** web experimental \( ExperimentalApis \) muestra el estado de la marca de características de ![ la plataforma web ](../media/experimental-apis-dark-icon.msft.png) **experimental.**</span><span class="sxs-lookup"><span data-stu-id="8f360-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="8f360-137">Si la marca está activada, se resalta el icono.</span><span class="sxs-lookup"><span data-stu-id="8f360-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="8f360-138">Si la marca está desactivada, el icono no se resalta.</span><span class="sxs-lookup"><span data-stu-id="8f360-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="8f360-139">Para activar \(o desactivar\) la marca, elige el icono o navega a `edge://flags` y alterna la marca.</span><span class="sxs-lookup"><span data-stu-id="8f360-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="8f360-140">A continuación se muestra una lista de problemas conocidos actuales.</span><span class="sxs-lookup"><span data-stu-id="8f360-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="8f360-141">Cuando usas un cliente de Escritorio remoto de [Microsoft][RemoteDesktopClientDocs] para conectarte a un equipo remoto y emular [Surface Duo][SurfaceDevicesDuo] o El plegado [Desconsudada de Samsung ,][SamsungMobileGalaxyFold]el puntero puede estremezárselo o estremezz.</span><span class="sxs-lookup"><span data-stu-id="8f360-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="8f360-142">Si tiene problemas con el problema, [envíe comentarios.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8f360-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <span data-ttu-id="8f360-143">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8f360-143">Additional Resources</span></span>  

<span data-ttu-id="8f360-144">Estos son recursos adicionales que pueden ayudarte a mejorar tu sitio web \(o app\) para dispositivos de pantalla doble.</span><span class="sxs-lookup"><span data-stu-id="8f360-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="8f360-145">Para obtener más información sobre el desarrollo web en dispositivos de pantalla doble, vaya a [experiencias web de doble pantalla.][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="8f360-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="8f360-146">Instala el [emulador de Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="8f360-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="8f360-147">El emulador de Surface Duo es diferente del emulador de Microsoft Edge, ejecuta Android y se integra con [Android Studio.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="8f360-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="8f360-148">Para obtener más información, ve [a Obtener el SDK de Surface Duo.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="8f360-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="8f360-149">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f360-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la seam: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla multimedia CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
