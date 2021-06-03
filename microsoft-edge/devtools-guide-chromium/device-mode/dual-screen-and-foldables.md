---
description: Usa dispositivos virtuales en Microsoft Edge para mejorar tu sitio web para dispositivos de doble pantalla y plegables.
title: Emular dispositivos de pantalla doble y plegado en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, emulación, dispositivo, simulación, móvil, pantalla doble, plegado, Surface Duo, Samsung Galaxy Fold
ms.openlocfilehash: c3bd3296afa86d9d2c90c164bc3e9088bc043c3c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564346"
---
# <a name="emulate-dual-screen-and-foldable-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="67230-104">Emular dispositivos de pantalla doble y plegado en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="67230-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="67230-105">En Microsoft Edge versión 89 o posterior, puedes emular los siguientes dispositivos de doble pantalla y plegados.</span><span class="sxs-lookup"><span data-stu-id="67230-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="67230-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="67230-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="67230-107">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="67230-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="67230-108">Emula los dispositivos y alterna entre las siguientes posturas.</span><span class="sxs-lookup"><span data-stu-id="67230-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="67230-109">Postura de pantalla única o doblada</span><span class="sxs-lookup"><span data-stu-id="67230-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="67230-110">Postura de pantalla doble o desdoblada</span><span class="sxs-lookup"><span data-stu-id="67230-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="67230-111">Activa las API [experimentales](#turn-on-experimental-apis) de plataforma web y usa la característica de pantalla multimedia [CSS][DualScreenDocsCssMedia] y la [API getWindowSegments][DualScreenDocsJSAPI] de JavaScript para mejorar tu sitio web \(o aplicación\) para dispositivos de pantalla doble y plegables.</span><span class="sxs-lookup"><span data-stu-id="67230-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular Surface Duo en Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="67230-113">Emular Surface Duo en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67230-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <a name="turn-on-experimental-apis"></a><span data-ttu-id="67230-114">Activar API experimentales</span><span class="sxs-lookup"><span data-stu-id="67230-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="67230-115">Para usar la característica de pantalla de medios [CSS][DualScreenDocsCssMedia] y la [API getWindowSegments de JavaScript,][DualScreenDocsJSAPI]active la marca en `Experimental Web Platform features` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67230-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="67230-116">Complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="67230-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="67230-117">Vaya a `edge://flags`.</span><span class="sxs-lookup"><span data-stu-id="67230-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="67230-118">En el **cuadro de texto** Marcas de búsqueda, escriba , elija la marca características de plataforma web `Experimental Web Platform features` **experimental** y cambie **Deshabilitado** a **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="67230-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="67230-119">Reiniciar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67230-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activar la marca de características de la plataforma web experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="67230-121">Activar la marca **de características de la plataforma web** experimental</span><span class="sxs-lookup"><span data-stu-id="67230-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="67230-122">Si usas consultas multimedia [CSS][DualScreenDocsCssMedia] o la API de enumeración de segmentos de [JavaScript Windows][DualScreenDocsJSAPI] para mejorar tu sitio web o aplicación para [Surface Duo,][SurfaceDevicesDuo]también debes activar la marca de características de plataforma **web experimental** en la aplicación [Android Microsoft Edge][GooglePlayMicrosoftEdge] en tu dispositivo [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="67230-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="67230-123">Si la marca de características de [][MicrosoftEdge] la Plataforma web experimental está activada en Microsoft Edge de escritorio y desactivada en la aplicación [Android Microsoft Edge][GooglePlayMicrosoftEdge], el comportamiento de tu sitio **web** o aplicación en el emulador de Surface Duo en el Microsoft Edge de escritorio no coincide con la aplicación de Android [Microsoft Edge en][GooglePlayMicrosoftEdge] Surface [Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="67230-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="67230-124">Asegúrate de que las marcas coincidan en android y Microsoft Edge para usar correctamente el emulador de Surface Duo en el equipo de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="67230-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <a name="test-on-foldable-and-dual-screen-devices"></a><span data-ttu-id="67230-125">Probar en dispositivos de doble pantalla y plegados</span><span class="sxs-lookup"><span data-stu-id="67230-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="67230-126">Cuando emulas Surface [Duo][SurfaceDevicesDuo] en una posición de pantalla doble en Microsoft Edge, la costura \(el espacio entre las dos pantallas\) se dibuja sobre tu sitio web o aplicación.</span><span class="sxs-lookup"><span data-stu-id="67230-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="67230-127">La pantalla emulada coincide con la forma en que el sitio web \(o aplicación\) se representa en la [aplicación android][GooglePlayMicrosoftEdge] Microsoft Edge mientras se ejecuta en [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="67230-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="67230-128">Es posible que deba actualizar su sitio web \(o app\) para mostrarse mejor a lo largo de la costura.</span><span class="sxs-lookup"><span data-stu-id="67230-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="67230-129">Para obtener más información acerca de cómo adaptar el sitio web \(o aplicación\) a la costura, vaya a Cómo trabajar [con la costura][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="67230-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="67230-130">La [barra de herramientas del][DevtoolsDeviceModeIndexSimulateMobileViewport] dispositivo tiene características adicionales que te ayudarán a probar tu sitio web o aplicación en varias posturas y orientaciones.</span><span class="sxs-lookup"><span data-stu-id="67230-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="67230-131">Elija **Girar** \( ![ Girar ](../media/rotate-dark-icon.msft.png) \) para girar la ventanilla a orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="67230-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="67230-132">Combina la característica con **Span** \( Span \) para alternar entre posturas de pantalla única o doblada y de doble ![ pantalla o ](../media/span-dark-icon.msft.png) desdobladas.</span><span class="sxs-lookup"><span data-stu-id="67230-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="67230-133">Juntos, las características te permiten probar tu sitio web o aplicación en las cuatro posturas y orientaciones posibles.</span><span class="sxs-lookup"><span data-stu-id="67230-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas y orientaciones para dispositivos de pantalla doble y plegables" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="67230-135">Matriz de posturas y orientaciones para dispositivos de pantalla doble y plegables</span><span class="sxs-lookup"><span data-stu-id="67230-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="67230-136">El **icono Características de la plataforma web** experimental \( ![ ExperimentalApis \) muestra el estado de la marca de características de la ](../media/experimental-apis-dark-icon.msft.png) Plataforma **web** experimental.</span><span class="sxs-lookup"><span data-stu-id="67230-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="67230-137">Si la marca está activada, se resalta el icono.</span><span class="sxs-lookup"><span data-stu-id="67230-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="67230-138">Si la marca está desactivada, el icono no se resalta.</span><span class="sxs-lookup"><span data-stu-id="67230-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="67230-139">Para activar \(o desactivar\) la marca, elija el icono o vaya a `edge://flags` y cambie la marca.</span><span class="sxs-lookup"><span data-stu-id="67230-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="67230-140">A continuación se muestra una lista de problemas conocidos actuales.</span><span class="sxs-lookup"><span data-stu-id="67230-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="67230-141">Cuando usas un [cliente Escritorio remoto de Microsoft para][RemoteDesktopClientDocs] conectarte a un equipo remoto y emular Surface [Duo][SurfaceDevicesDuo] o Samsung [Galaxy Fold,][SamsungMobileGalaxyFold]el puntero puede agitarse o tartamudear.</span><span class="sxs-lookup"><span data-stu-id="67230-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="67230-142">Si se ejecuta con el problema, [envíe comentarios](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="67230-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="67230-143">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="67230-143">Additional Resources</span></span>  

<span data-ttu-id="67230-144">Estos son recursos adicionales que pueden ayudarle a mejorar su sitio web \(o aplicación\) para dispositivos de pantalla doble.</span><span class="sxs-lookup"><span data-stu-id="67230-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="67230-145">Para obtener más información sobre el desarrollo web en dispositivos de pantalla doble, vaya a [Experiencias web de pantalla dual.][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="67230-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="67230-146">Instalar el [emulador de Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="67230-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="67230-147">El emulador de Surface Duo es diferente del emulador de Microsoft Edge, ejecuta Android e se integra con [Android Studio][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="67230-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="67230-148">Para obtener más información, ve [a Obtener el SDK de Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="67230-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="67230-149">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="67230-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la unión: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla expandida para medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API de JavaScript de getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/global/galaxy/galaxy-fold "Galaxy Fold | Samsung"  
