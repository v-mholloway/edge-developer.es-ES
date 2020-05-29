---
title: Introducción a los emuladores de superficies de depuración remota Duo
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, depuración remota, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621505"
---
# <span data-ttu-id="829d2-103">Introducción a los emuladores de superficies de depuración remota Duo</span><span class="sxs-lookup"><span data-stu-id="829d2-103">Get Started with Remote Debugging Surface Duo emulators</span></span>

<span data-ttu-id="829d2-104">En este artículo, encontrarás el proceso de depuración remota de contenido web en la [aplicación Microsoft Edge][AndroidEdge] en un emulador [Surface Duo][SurfaceDuo] desde una instancia de escritorio de [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="829d2-104">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][AndroidEdge] on a [Surface Duo][SurfaceDuo] emulator from a desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="829d2-105">Para obtener información sobre la depuración en un dispositivo Surface Duo, siga nuestra guía para la [depuración remota de dispositivos Android][RemoteDebuggingAndroid].</span><span class="sxs-lookup"><span data-stu-id="829d2-105">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][RemoteDebuggingAndroid].</span></span>

## <span data-ttu-id="829d2-106">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="829d2-106">Before you Begin</span></span>

<span data-ttu-id="829d2-107">Instala el [SDK Surface Duo][DuoSdk] antes de ejecutar el [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="829d2-107">Install the [Surface Duo SDK][DuoSdk] before running the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="829d2-108">Para obtener más información, vea [obtener el SDK de Surface Duo][DuoSdkdocs].</span><span class="sxs-lookup"><span data-stu-id="829d2-108">For more information, see [Get the Surface Duo SDK][DuoSdkdocs].</span></span>

## <span data-ttu-id="829d2-109">Paso 1: vaya a edge://inspect</span><span class="sxs-lookup"><span data-stu-id="829d2-109">Step 1: Navigate to edge://inspect</span></span>

<span data-ttu-id="829d2-110">Abra una instancia de escritorio de [Microsoft Edge][DesktopEdge]y vaya a `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="829d2-110">Open a desktop instance of [Microsoft Edge][DesktopEdge], and navigate to `edge://inspect`.</span></span>

> ##### <span data-ttu-id="829d2-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="829d2-111">Figure 1</span></span>  
> <span data-ttu-id="829d2-112">La `edge://inspect` Página de Microsoft Edge en el escritorio ![ la página Edge://Inspect de Microsoft Edge en el escritorio][ImageEdgeInspect]</span><span class="sxs-lookup"><span data-stu-id="829d2-112">The `edge://inspect` page in Microsoft Edge on the desktop ![The edge://inspect page in Microsoft Edge on the desktop][ImageEdgeInspect]</span></span>

> [!NOTE]
> <span data-ttu-id="829d2-113">Si la `edge://inspect` Página no reconoce el [emulador Surface Duo][DuoEmulator], reinicie el emulador.</span><span class="sxs-lookup"><span data-stu-id="829d2-113">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DuoEmulator], restart the emulator.</span></span>

## <span data-ttu-id="829d2-114">Paso 2: iniciar el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="829d2-114">Step 2: Launch the Surface Duo emulator</span></span>

<span data-ttu-id="829d2-115">Inicia el [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="829d2-115">Launch the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="829d2-116">Observe que el emulador muestra dos pantallas diferentes ejecutándose en el emulador.</span><span class="sxs-lookup"><span data-stu-id="829d2-116">Notice that the emulator displays 2 different screens running on the emulator.</span></span>

> ##### <span data-ttu-id="829d2-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="829d2-117">Figure 2</span></span>
> <span data-ttu-id="829d2-118">Emulador Surface Duo, ![ el emulador Surface Duo][ImageDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="829d2-118">The Surface Duo emulator ![The Surface Duo emulator][ImageDuoEmulator]</span></span>  

## <span data-ttu-id="829d2-119">Paso 3: cargar el contenido web en Microsoft Edge en el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="829d2-119">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>

<span data-ttu-id="829d2-120">En cualquiera de las dos pantallas, deslice el dedo hacia arriba en la bandeja favoritos del [emulador Surface Duo][DuoEmulator] para mostrar el cajón de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="829d2-120">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DuoEmulator] to display the Apps Drawer.</span></span> <span data-ttu-id="829d2-121">Elija **borde** para iniciar la [aplicación Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="829d2-121">Choose **Edge** to launch the [Microsoft Edge app][AndroidEdge].</span></span>

> ##### <span data-ttu-id="829d2-122">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="829d2-122">Figure 3</span></span>
> <span data-ttu-id="829d2-123">La aplicación Microsoft Edge en el emulador Surface Duo, ![ la aplicación Microsoft Edge en el emulador Surface Duo][ImageDuoEmulatorEdge]</span><span class="sxs-lookup"><span data-stu-id="829d2-123">The Microsoft Edge app on the Surface Duo emulator ![The Microsoft Edge app on the Surface Duo emulator][ImageDuoEmulatorEdge]</span></span>  

<span data-ttu-id="829d2-124">Navegue hasta el sitio web o la aplicación que quiera depurar en la [aplicación Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="829d2-124">Navigate to the website or app that you want to debug in the [Microsoft Edge app][AndroidEdge].</span></span>

## <span data-ttu-id="829d2-125">Paso 4: Depure su contenido web desde el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="829d2-125">Step 4: Debug your web content from the Surface Duo emulator</span></span> 

<span data-ttu-id="829d2-126">Vuelva a la instancia de escritorio de [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="829d2-126">Switch back to the desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="829d2-127">La `edge://inspect` página ahora muestra la **SurfaceDuoEmulator** con una lista de las pestañas abiertas o de [PWAs][PwaDocs] que se ejecutan en el [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="829d2-127">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaDocs] that are running on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="829d2-128">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="829d2-128">Figure 4</span></span>
> <span data-ttu-id="829d2-129">La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador ![ la página Edge://Inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador][ImageEdgeInspectTargets]</span><span class="sxs-lookup"><span data-stu-id="829d2-129">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator ![The edge://inspect page displays a list of the open tabs in the Microsoft Edge app running on the emulator][ImageEdgeInspectTargets]</span></span>  

> [!NOTE]
> <span data-ttu-id="829d2-130">Si no ve **SurfaceDuoEmulator** en la `edge://inspect` página, intente abrir o cerrar las pestañas en la [aplicación Microsoft Edge][AndroidEdge] en el [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="829d2-130">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][AndroidEdge] on the [Surface Duo Emulator][DuoEmulator].</span></span> <span data-ttu-id="829d2-131">Para obtener instrucciones adicionales para la solución de problemas, consulte la [sección solución de problemas para dispositivos Android][TroubleshootingAndroid].</span><span class="sxs-lookup"><span data-stu-id="829d2-131">For additional troubleshooting steps, see the [troubleshooting section for Android devices][TroubleshootingAndroid].</span></span>

<span data-ttu-id="829d2-132">En la lista de las pestañas abiertas que se ejecutan en el emulador, elija **inspeccionar** en la pestaña que tiene el contenido web que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="829d2-132">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span> <span data-ttu-id="829d2-133">El [DevTools de Microsoft Edge][DevToolsDocs] se abrirá en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="829d2-133">The [Microsoft Edge DevTools][DevToolsDocs] will open in a new window.</span></span> <span data-ttu-id="829d2-134">Elija **activar o desactivar** screencast de la demostración ![ ][ImageToggleScreencastIcon] para ver el contenido web desde el [emulador Surface Duo][DuoEmulator] en la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="829d2-134">Choose **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the web content from your [Surface Duo emulator][DuoEmulator] in the DevTools window.</span></span> <span data-ttu-id="829d2-135">Ahora puede usar el DevTools de Microsoft Edge para depurar su contenido web en el [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="829d2-135">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="829d2-136">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="829d2-136">Figure 5</span></span>
> <span data-ttu-id="829d2-137">Usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo con el emulador de ![ Microsoft Edge DevTools para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo][ImageDevTools]</span><span class="sxs-lookup"><span data-stu-id="829d2-137">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator ![Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator][ImageDevTools]</span></span>  

> [!NOTE]
> <span data-ttu-id="829d2-138">Si abarca la [aplicación Microsoft Edge][AndroidEdge] en las dos pantallas del emulador, el screencast reflejará el nuevo tamaño de la aplicación, pero no la articulación.</span><span class="sxs-lookup"><span data-stu-id="829d2-138">If you span the [Microsoft Edge app][AndroidEdge] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span> <span data-ttu-id="829d2-139">Para comprender cómo la bisagra afecta al diseño de su contenido Web, use el [emulador Surface Duo][DuoEmulator] en lugar del screencast.</span><span class="sxs-lookup"><span data-stu-id="829d2-139">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DuoEmulator] instead of the screencast.</span></span>

## <span data-ttu-id="829d2-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="829d2-140">Additional Resources</span></span>

<span data-ttu-id="829d2-141">La web es una excelente plataforma para la nueva clase de plegable y dispositivos de pantalla dual porque puedes escribir una vez HTML, CSS y JavaScript y hacer que tenga un aspecto excelente en los dispositivos de pantalla única, dual y plegable.</span><span class="sxs-lookup"><span data-stu-id="829d2-141">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span> <span data-ttu-id="829d2-142">Para obtener más información, vea estos recursos adicionales para empezar a crear contenido web para estos dispositivos nuevos.</span><span class="sxs-lookup"><span data-stu-id="829d2-142">For more information, see these additional resources to get started building web content for these new devices.</span></span>

- [<span data-ttu-id="829d2-143">Documentación para crear aplicaciones en dispositivos de doble pantalla</span><span class="sxs-lookup"><span data-stu-id="829d2-143">Documentation for creating apps on dual-screen devices</span></span>][DualScreenDocs]
- [<span data-ttu-id="829d2-144">El explicación de la plataforma web Microsoft Edge para nuevas API para crear experiencias Web en dispositivos de plegable y de doble pantalla</span><span class="sxs-lookup"><span data-stu-id="829d2-144">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][WebPlatformExplainer]
- [<span data-ttu-id="829d2-145">Grabación de la sesión del día del desarrollador de 365 de Microsoft: Cómo crear experiencias en dos pantallas para sitios web y aplicaciones Web</span><span class="sxs-lookup"><span data-stu-id="829d2-145">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Ilustración 1: la página edge://inspect en Microsoft Edge en el escritorio"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Ilustración 2: el emulador Surface Duo"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Ilustración 3: la aplicación Microsoft Edge en el emulador Surface Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Ilustración 4: la página edge://inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador"
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Ilustración 5: usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introducción a la depuración remota dispositivos Android"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Solución de problemas: DevTools no detecta el dispositivo Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicación Microsoft Edge Android"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Presentamos Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Presentamos el nuevo Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Usar el emulador Surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Versión preliminar del SDK de Surface Duo"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Obtener el SDK Surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Crear aplicaciones para dispositivos de doble pantalla"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma web para experiencias habilitadas en dispositivos plegable"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Cómo crear experiencias en pantalla dual para el sitio web y las aplicaciones Web"
