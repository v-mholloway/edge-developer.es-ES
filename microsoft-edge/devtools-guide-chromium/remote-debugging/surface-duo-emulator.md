---
description: Introducción a los emuladores de superficies de depuración remota Duo.
title: Introducción a los emuladores de superficies de depuración remota Duo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, depuración remota, Android, Surface Duo
ms.openlocfilehash: f44c85c468de3bdd7727695e3f33269584966231
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230659"
---
# <span data-ttu-id="32281-104">Introducción a los emuladores de superficies de depuración remota Duo</span><span class="sxs-lookup"><span data-stu-id="32281-104">Get Started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="32281-105">En este artículo, encontrarás el proceso de depuración remota de contenido web en la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en un emulador [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] desde una instancia de escritorio de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="32281-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="32281-106">Para obtener información sobre la depuración en un dispositivo Surface Duo, siga nuestra guía para la [depuración remota de dispositivos Android][DevtoolsRemoteDebuggingMain].</span><span class="sxs-lookup"><span data-stu-id="32281-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <span data-ttu-id="32281-107">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="32281-107">Before you Begin</span></span>

<span data-ttu-id="32281-108">Instala el [SDK Surface Duo][MicrosoftDownload100847] antes de ejecutar el [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="32281-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="32281-109">Para obtener más información, vea [obtener el SDK de Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="32281-109">For more information, see [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="32281-110">Paso 1: vaya a edge://inspect</span><span class="sxs-lookup"><span data-stu-id="32281-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="32281-111">Abra una instancia de escritorio de [Microsoft Edge][MicrosoftEdge]y vaya a `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="32281-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="La página edge://inspect en Microsoft Edge en el escritorio" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="32281-113">La `edge://inspect` página en Microsoft Edge en el escritorio</span><span class="sxs-lookup"><span data-stu-id="32281-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="32281-114">Si la `edge://inspect` Página no reconoce el [emulador Surface Duo][DualScreenAndroidUseEmulator], reinicie el emulador.</span><span class="sxs-lookup"><span data-stu-id="32281-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <span data-ttu-id="32281-115">Paso 2: iniciar el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="32281-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="32281-116">Inicia el [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="32281-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="32281-117">Observe que el emulador muestra dos pantallas diferentes ejecutándose en el emulador.</span><span class="sxs-lookup"><span data-stu-id="32281-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="32281-119">Emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="32281-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <span data-ttu-id="32281-120">Paso 3: cargar el contenido web en Microsoft Edge en el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="32281-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="32281-121">En cualquiera de las dos pantallas, deslice el dedo hacia arriba en la bandeja favoritos del [emulador Surface Duo][DualScreenAndroidUseEmulator] para mostrar el cajón de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="32281-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="32281-122">Elija **borde** para iniciar la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="32281-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="La aplicación Microsoft Edge en el emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="32281-124">La aplicación Microsoft Edge en el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="32281-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="32281-125">Navegue hasta el sitio web o la aplicación que quiera depurar en la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="32281-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <span data-ttu-id="32281-126">Paso 4: Depure su contenido web desde el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="32281-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="32281-127">Vuelva a la instancia de escritorio de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="32281-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="32281-128">La `edge://inspect` página ahora muestra la **SurfaceDuoEmulator** con una lista de las pestañas abiertas o de [PWAs][ProgressiveWebAppsIndex] que se ejecutan en el [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="32281-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La página edge://inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="32281-130">La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador</span><span class="sxs-lookup"><span data-stu-id="32281-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="32281-131">Si no ve **SurfaceDuoEmulator** en la `edge://inspect` página, intente abrir o cerrar las pestañas en la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en el [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="32281-131">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="32281-132">Para obtener instrucciones adicionales para la solución de problemas, consulte la [sección solución de problemas para dispositivos Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span><span class="sxs-lookup"><span data-stu-id="32281-132">For additional troubleshooting steps, see the [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="32281-133">En la lista de las pestañas abiertas que se ejecutan en el emulador, elija **inspeccionar** en la pestaña que tiene el contenido web que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="32281-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="32281-134">El [DevTools de Microsoft Edge][DevtoolsIndex] se abrirá en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="32281-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="32281-135">Elija **alternar screencast** \ ( ![ alternar screencast ][ImageToggleScreencastIcon] \) para ver el contenido web desde el [emulador Surface Duo][DualScreenAndroidUseEmulator] en la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="32281-135">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="32281-136">Ahora puede usar el DevTools de Microsoft Edge para depurar su contenido web en el [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="32281-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="32281-138">Usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="32281-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="32281-139">Si abarca la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en las dos pantallas del emulador, el screencast reflejará el nuevo tamaño de la aplicación, pero no la articulación.</span><span class="sxs-lookup"><span data-stu-id="32281-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="32281-140">Para comprender cómo la bisagra afecta al diseño de su contenido Web, use el [emulador Surface Duo][DualScreenAndroidUseEmulator] en lugar del screencast.</span><span class="sxs-lookup"><span data-stu-id="32281-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <span data-ttu-id="32281-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="32281-141">Additional Resources</span></span>  

<span data-ttu-id="32281-142">La web es una excelente plataforma para la nueva clase de plegable y dispositivos de pantalla dual porque puedes escribir una vez HTML, CSS y JavaScript y hacer que tenga un aspecto excelente en los dispositivos de pantalla única, dual y plegable.</span><span class="sxs-lookup"><span data-stu-id="32281-142">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="32281-143">Para obtener más información, vea estos recursos adicionales para empezar a crear contenido web para estos dispositivos nuevos.</span><span class="sxs-lookup"><span data-stu-id="32281-143">For more information, see these additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="32281-144">Documentación para crear aplicaciones en dispositivos de doble pantalla</span><span class="sxs-lookup"><span data-stu-id="32281-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="32281-145">El explicación de la plataforma web Microsoft Edge para nuevas API para crear experiencias Web en dispositivos de plegable y de doble pantalla</span><span class="sxs-lookup"><span data-stu-id="32281-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="32281-146">Grabación de la sesión del día del desarrollador de 365 de Microsoft: Cómo crear experiencias en dos pantallas para sitios web y aplicaciones Web</span><span class="sxs-lookup"><span data-stu-id="32281-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicaciones web progresivas en Windows | Microsoft docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solución de problemas: DevTools no detecta el dispositivo Android: Introducción a la depuración remota dispositivos Android | Microsoft docs"  

[DualScreenIndex]: /dual-screen/index "Crear aplicaciones para dispositivos de doble pantalla | Microsoft docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usar el emulador Surface DUo | Microsoft docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el SDK Surface Duo | Microsoft docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Presentamos el nuevo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "La nueva superficie | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Descargar Surface Duo SDK Preview versión | Centro de descarga de Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: explorador Web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma web para experiencias habilitadas en dispositivos plegable: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Cómo crear experiencias en dos pantallas para el sitio web y aplicaciones Web | YouTube"  
