---
description: Introducción a los emuladores de Surface Duo de depuración remota.
title: Introducción a los emuladores de Surface Duo de depuración remota
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, depuración remota, android, surface duo
ms.openlocfilehash: 61f903a5b929b7ee7b924938cf6ddc21a9783ca7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439334"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a><span data-ttu-id="0a764-104">Introducción a los emuladores de Surface Duo de depuración remota</span><span class="sxs-lookup"><span data-stu-id="0a764-104">Get started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="0a764-105">En este artículo, describes el proceso de depuración remota del contenido web en la aplicación [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en un emulador de [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] desde una instancia de escritorio de Microsoft [Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="0a764-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="0a764-106">Para obtener información sobre la depuración en un dispositivo Surface Duo, sigue nuestra guía para la depuración remota [de dispositivos Android.][DevtoolsRemoteDebuggingMain]</span><span class="sxs-lookup"><span data-stu-id="0a764-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="0a764-107">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="0a764-107">Before you Begin</span></span>

<span data-ttu-id="0a764-108">Instala el [SDK de Surface Duo][MicrosoftDownload100847] antes de ejecutar el emulador de Surface [Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="0a764-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="0a764-109">Para obtener más información, ve [a Obtener el SDK de Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="0a764-109">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="step-1-navigate-to-edgeinspect"></a><span data-ttu-id="0a764-110">Paso 1: Vaya a edge://inspect</span><span class="sxs-lookup"><span data-stu-id="0a764-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="0a764-111">Abra una instancia de escritorio de [Microsoft Edge][MicrosoftEdge]y vaya a `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="0a764-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="La edge://inspect de Microsoft Edge en el escritorio" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="0a764-113">La `edge://inspect` página de Microsoft Edge en el escritorio</span><span class="sxs-lookup"><span data-stu-id="0a764-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="0a764-114">Si la `edge://inspect` página no reconoce el emulador de Surface [Duo,][DualScreenAndroidUseEmulator]reinicia el emulador.</span><span class="sxs-lookup"><span data-stu-id="0a764-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <a name="step-2-launch-the-surface-duo-emulator"></a><span data-ttu-id="0a764-115">Paso 2: Iniciar el emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0a764-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="0a764-116">Inicia el [emulador de Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="0a764-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="0a764-117">Observe que el emulador muestra 2 pantallas diferentes que se ejecutan en el emulador.</span><span class="sxs-lookup"><span data-stu-id="0a764-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Emulador de Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="0a764-119">Emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0a764-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a><span data-ttu-id="0a764-120">Paso 3: Cargar el contenido web en Microsoft Edge en el emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0a764-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="0a764-121">En cualquier pantalla, desliza el dedo hacia arriba en la Bandeja de favoritos del emulador [de Surface Duo][DualScreenAndroidUseEmulator] para mostrar el cajón de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0a764-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="0a764-122">Elija **Edge** para iniciar la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="0a764-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="La aplicación Microsoft Edge en el emulador de Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="0a764-124">La aplicación Microsoft Edge en el emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0a764-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="0a764-125">Navegue hasta el sitio web o la aplicación que desea depurar en la [aplicación de Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="0a764-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a><span data-ttu-id="0a764-126">Paso 4: Depurar el contenido web desde el emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0a764-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="0a764-127">Vuelva a la instancia de escritorio de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="0a764-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="0a764-128">La `edge://inspect` página ahora muestra **SurfaceDuoEmulator** con una lista de las pestañas abiertas o [pwas][ProgressiveWebAppsIndex] que se ejecutan en el emulador [de Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="0a764-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La edge://inspect muestra una lista de las pestañas abiertas en la aplicación de Microsoft Edge que se ejecuta en el emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="0a764-130">La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación microsoft edge que se ejecuta en el emulador</span><span class="sxs-lookup"><span data-stu-id="0a764-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0a764-131">Si **SurfaceDuoEmulator** no se muestra en la página, intenta abrir o cerrar pestañas en la aplicación Microsoft Edge en `edge://inspect` el emulador de Surface [Duo][DualScreenAndroidUseEmulator]. [][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="0a764-131">If **SurfaceDuoEmulator** is not displayed on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="0a764-132">Para obtener pasos adicionales de solución de problemas, vaya a la sección [de solución de problemas para dispositivos Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span><span class="sxs-lookup"><span data-stu-id="0a764-132">For additional troubleshooting steps, navigate to [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="0a764-133">En la lista de pestañas abiertas que se ejecutan en el emulador, elija **Inspeccionar** en la pestaña que tiene el contenido web que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="0a764-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="0a764-134">Microsoft [Edge DevTools][DevtoolsIndex] se abrirá en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="0a764-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="0a764-135">Elige **Alternar difusión** de pantalla \( Alternar difusión por pantalla \) para ver el contenido web desde el emulador ![ de Surface ](../media/toggle-screencast-icon.msft.png) [Duo][DualScreenAndroidUseEmulator] en la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="0a764-135">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="0a764-136">Ahora puedes usar Microsoft Edge DevTools para depurar el contenido web en el emulador [de Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="0a764-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Uso de Microsoft Edge DevTools para depurar Bing en la aplicación Microsoft Edge en el emulador de Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="0a764-138">Uso de Microsoft Edge DevTools para depurar Bing en la aplicación Microsoft Edge en el emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0a764-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0a764-139">Si abarcas la [aplicación de Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en ambas pantallas del emulador, la difusión en pantalla reflejará el nuevo tamaño de la aplicación, pero no la bisagra.</span><span class="sxs-lookup"><span data-stu-id="0a764-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="0a764-140">Para comprender cómo afecta la bisagra al diseño del contenido web, usa el [emulador de Surface Duo][DualScreenAndroidUseEmulator] en lugar de la difusión por pantalla.</span><span class="sxs-lookup"><span data-stu-id="0a764-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="0a764-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0a764-141">Additional Resources</span></span>  

<span data-ttu-id="0a764-142">La web es una excelente plataforma para la nueva clase de dispositivos de doble pantalla y plegados, ya que puede escribir html, CSS y JavaScript una vez y tener un aspecto excelente en dispositivos de pantalla única, doble pantalla y plegados.</span><span class="sxs-lookup"><span data-stu-id="0a764-142">The web is a great platform for the new class of foldable and dual-screen devices because you may write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="0a764-143">Para obtener más información, vaya a los siguientes recursos adicionales para empezar a crear contenido web para estos nuevos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0a764-143">For more information, navigate to the following additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="0a764-144">Documentación para crear aplicaciones en dispositivos de pantalla doble</span><span class="sxs-lookup"><span data-stu-id="0a764-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="0a764-145">El explicador de la plataforma web de Microsoft Edge para nuevas API para crear experiencias web en dispositivos de doble pantalla y plegados</span><span class="sxs-lookup"><span data-stu-id="0a764-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="0a764-146">Grabación de la sesión del Día del desarrollador de Microsoft 365: cómo crear experiencias de pantalla doble para sitios web y aplicaciones web</span><span class="sxs-lookup"><span data-stu-id="0a764-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0a764-147">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0a764-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicaciones web progresivas en Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solución de problemas: DevTools no detecta el dispositivo Android: introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[DualScreenIndex]: /dual-screen/index "Crear aplicaciones para dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface DUo | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el SDK de Surface Duo | Microsoft Docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Presentación del nuevo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "El nuevo surface duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Descargar Surface Duo SDK Preview Release | Centro de descarga de Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: Explorador web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivos de plataforma web para experiencias ilustradas en dispositivos plegables: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Cómo crear experiencias de pantalla doble para el sitio web y las aplicaciones web | YouTube"  
