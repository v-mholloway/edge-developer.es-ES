---
title: Novedades de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fc5dcc10ba3a79bd3f073e0e3504e551d7e23d70
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688181"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="9194a-103">Novedades de DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="9194a-103">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <span data-ttu-id="9194a-104">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9194a-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="9194a-105">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9194a-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="9194a-106">Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.</span><span class="sxs-lookup"><span data-stu-id="9194a-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="9194a-107">Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="9194a-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="9194a-108">Usar el DevTools en el modo de contraste alto de Windows</span><span class="sxs-lookup"><span data-stu-id="9194a-108">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="9194a-109">Ahora, los DevTools de Microsoft Edge se muestran en el modo contraste alto cuando Windows está en modo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="9194a-109">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en el modo contraste alto" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="9194a-111">Microsoft Edge DevTools en el modo contraste alto</span><span class="sxs-lookup"><span data-stu-id="9194a-111">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-112">[Siga las instrucciones para activar el modo de contraste alto en Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="9194a-112">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="9194a-113">Para abrir el DevTools en Microsoft Edge, presione `F12` o `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="9194a-113">Open the DevTools in Microsoft Edge by pressing `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="9194a-114">El DevTools se muestra en el modo contraste alto.</span><span class="sxs-lookup"><span data-stu-id="9194a-114">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="9194a-115">En la actualidad, Microsoft Edge DevTools es compatible con el modo de alto contraste en Windows, pero no en macOS.</span><span class="sxs-lookup"><span data-stu-id="9194a-115">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span> 

<span data-ttu-id="9194a-116">[#1048378][CR1048378] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-116">Chromium issue [#1048378][CR1048378]</span></span>  

### <span data-ttu-id="9194a-117">Hacer coincidir los métodos abreviados de teclado en el código de DevTools a VS</span><span class="sxs-lookup"><span data-stu-id="9194a-117">Match keyboard shortcuts in the DevTools to VS Code</span></span>  

<span data-ttu-id="9194a-118">En su [opinión](#getting-in-touch-with-microsoft-edge-devtools-team) y el [rastreador de problemas públicos de cromo][CRIssuesList], el equipo de DevTools de Microsoft Edge aprendió que desea poder personalizar los métodos abreviados de teclado en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="9194a-118">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="9194a-119">En Microsoft Edge 84, ahora puede hacer coincidir los métodos abreviados de teclado del DevTools con el [código de vs][VSCode], que es solo una de las características en las que está trabajando el equipo para la personalización de los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="9194a-119">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [VS Code][VSCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a VS" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="9194a-121">Microsoft Edge DevTools en el modo contraste alto</span><span class="sxs-lookup"><span data-stu-id="9194a-121">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-122">Para probar el experimento, abre DevTools configuración pulsando `?` o seleccionando el icono del ![ icono ][ImageSettingsIcon] de configuración de DevTools en la esquina superior derecha de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="9194a-122">To try the experiment, open DevTools Settings by pressing `?` or selecting the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="9194a-123">Vaya a la sección **experimentos** y active la casilla **Habilitar la opción de configuración personalizada de métodos abreviados de teclado (se necesita volver a cargar)**.</span><span class="sxs-lookup"><span data-stu-id="9194a-123">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="9194a-124">Ahora vuelva a cargar el DevTools, abra la configuración de nuevo y vaya a la sección **accesos directos** .</span><span class="sxs-lookup"><span data-stu-id="9194a-124">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="9194a-125">Seleccione **DevTools (valor predeterminado)** en la lista desplegable **coincidir con métodos abreviados preestablecidos** y seleccione **código de Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="9194a-125">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="9194a-126">Los métodos abreviados de teclado de la DevTools ahora coinciden con los métodos abreviados para acciones equivalentes en VS Code.</span><span class="sxs-lookup"><span data-stu-id="9194a-126">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

<span data-ttu-id="9194a-127">Por ejemplo, el método abreviado de teclado para pausar o seguir ejecutando un script en [vs Code][VSCodeShortcuts] es `F5` .</span><span class="sxs-lookup"><span data-stu-id="9194a-127">For example, the keyboard shortcut for pausing or continuing running a script in [VS Code][VSCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="9194a-128">Con el valor preestablecido **DevTools (predeterminado)** , ese mismo método abreviado de DevTools es, `F8` pero con el prefijo de código de **Visual Studio** , ese método abreviado también está ahora `F5` .</span><span class="sxs-lookup"><span data-stu-id="9194a-128">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="9194a-129">La característica está actualmente disponible en Microsoft Edge 84 como experimento, por lo tanto, comparte tus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) con el equipo.</span><span class="sxs-lookup"><span data-stu-id="9194a-129">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="9194a-130">[#174309][CR174309] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-130">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="9194a-131">Emuladores de Surface de depuración remota Duo</span><span class="sxs-lookup"><span data-stu-id="9194a-131">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="9194a-132">Ahora puede depurar de forma remota el contenido web que se ejecuta en el [emulador Surface Duo][DualScreensAndroidEmulator] con toda la potencia de [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="9194a-132">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="9194a-133">Con el [emulador Surface Duo][DualScreensAndroidEmulator], puedes probar cómo se procesa tu contenido web en una nueva clase de plegable y dispositivos de doble pantalla.</span><span class="sxs-lookup"><span data-stu-id="9194a-133">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="9194a-134">El emulador ejecuta el sistema operativo Android y proporciona la [aplicación Microsoft Edge Android][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="9194a-134">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="9194a-135">Cargue el contenido web en la [aplicación Microsoft Edge][AndroidEdge] y depure con el [DevTools de Microsoft Edge][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="9194a-135">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="La aplicación Microsoft Edge que se ejecuta en el emulador Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="9194a-137">La aplicación Microsoft Edge en el emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="9194a-137">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-138">La `edge://inspect` Página de una instancia de escritorio de [Microsoft Edge][DesktopEdge] muestra la **SurfaceDuoEmulator** con una lista de las pestañas abiertas o de [PWAs][PwaIndex] que se ejecutan en el [emulador Surface Duo][DualScreensAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="9194a-138">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La página edge://inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="9194a-140">La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador</span><span class="sxs-lookup"><span data-stu-id="9194a-140">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="9194a-141">Al seleccionar **inspeccionar** para la ficha o PWA que desea depurar, se abre la [DevTools Microsoft Edge][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="9194a-141">Selecting **inspect** for the tab or PWA that you want to debug opens the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="9194a-142">[Sigue la guía paso a paso para depurar de forma remota el contenido web en el emulador Surface Duo][DevToolsRemoteDebugDuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="9194a-142">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <span data-ttu-id="9194a-143">Cambiar el tamaño del cajón de DevTools más fácilmente</span><span class="sxs-lookup"><span data-stu-id="9194a-143">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="9194a-144">En Microsoft Edge 83 o versiones anteriores, solo podía cambiar el tamaño del [cajón de DevTools][DevToolsDrawer] al colocar el puntero del ratón dentro de la barra de herramientas del cajón.</span><span class="sxs-lookup"><span data-stu-id="9194a-144">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the Drawer's toolbar.</span></span>  <span data-ttu-id="9194a-145">El cajón se comportó de forma diferente que otros controles de tamaño de los paneles de la DevTools, donde coloca el puntero sobre el borde del panel para cambiar su tamaño.</span><span class="sxs-lookup"><span data-stu-id="9194a-145">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover over the border of the pane to resize it.</span></span>  <span data-ttu-id="9194a-146">Seleccione la siguiente imagen para ver cómo ha funcionado el cambio de tamaño del cajón en la versión 83 o anterior de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9194a-146">Select the following image to see how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Cambiar el tamaño del cajón de DevTools en Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="9194a-148">Cambiar el tamaño del cajón de DevTools en Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="9194a-148">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="9194a-149">A partir de Microsoft Edge 84, ahora puede cambiar el tamaño de la bandeja de la caja al colocar el puntero sobre el borde del alimentador.</span><span class="sxs-lookup"><span data-stu-id="9194a-149">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="9194a-150">Este cambio alinea el comportamiento que cambia el tamaño del cajón de DevTools con la forma de cambiar el tamaño de otros paneles en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="9194a-150">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="9194a-151">Seleccione la siguiente imagen para ver cómo cambiar el tamaño en acción en Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="9194a-151">Select the following image to see resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Cambiar el tamaño del cajón de DevTools en Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="9194a-153">Cambiar el tamaño del cajón de DevTools en Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="9194a-153">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="9194a-154">[#1076112][CR1076112] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-154">Chromium issue [#1076112][CR1076112]</span></span>  

### <span data-ttu-id="9194a-155">Los botones de navegación en el screencast muestran el foco</span><span class="sxs-lookup"><span data-stu-id="9194a-155">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="9194a-156">Cuando se depura de forma remota un [dispositivo Android][DevToolsRemoteDebugAndroid], un [dispositivo Windows 10][DevToolsRemoteDebugWindows]o un [emulador Surface Duo][DevToolsRemoteDebugDuoEmulator], puede alternar el icono de la ![ demostración de alternancia ][ImageScreencastingIcon] en la esquina superior izquierda de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="9194a-156">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="9194a-157">Con el screencasts habilitado, podrás navegar por la pestaña de Microsoft Edge en el dispositivo remoto desde la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9194a-157">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="9194a-158">En Microsoft Edge 84, estos botones de navegación ahora también son accesibles desde el teclado.</span><span class="sxs-lookup"><span data-stu-id="9194a-158">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Al presionar Mayús + Tab en la barra de URL con el screencast se muestra el foco en el botón actualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="9194a-160">Al pulsar en `Shift` + `Tab` la barra de URL con el screencast se muestra el foco en el botón **Actualizar**</span><span class="sxs-lookup"><span data-stu-id="9194a-160">Pressing `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="9194a-161">[#1081486][CR1081486] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-161">Chromium issue [#1081486][CR1081486]</span></span>  

### <span data-ttu-id="9194a-162">El panel de detalles del panel de red está ahora accesible</span><span class="sxs-lookup"><span data-stu-id="9194a-162">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="9194a-163">En Microsoft Edge 84, el [Panel de detalles][DevToolsNetworkDetails] del panel **red** toma el foco cuando lo abre para un recurso en el [registro de red][DevToolsNetworkLog].</span><span class="sxs-lookup"><span data-stu-id="9194a-163">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** panel now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="9194a-164">Este cambio permite a los lectores de pantalla leer e interactuar con el contenido del panel de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="9194a-164">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="El panel de detalles del panel red toma el foco cuando se abre" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="9194a-166">El panel de **detalles** del panel **red** toma el foco cuando se abre</span><span class="sxs-lookup"><span data-stu-id="9194a-166">The **Details** pane in the **Network** panel takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="9194a-167">[#963183][CR963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-167">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="9194a-168">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-168">Announcements from the Chromium project</span></span>  

<span data-ttu-id="9194a-169">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 84 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="9194a-169">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="9194a-170">Solucionar problemas del sitio con la nueva herramienta problemas en el cajón de DevTools</span><span class="sxs-lookup"><span data-stu-id="9194a-170">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="9194a-171">La nueva herramienta **problemas** del cajón de DevTools se creó para ayudar a reducir la fatiga de las notificaciones y el desorden de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="9194a-171">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="9194a-172">En la actualidad, la **consola** es el lugar más central para que los desarrolladores de sitios web, bibliotecas, marcos y Microsoft Edge registren mensajes, advertencias y errores.</span><span class="sxs-lookup"><span data-stu-id="9194a-172">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="9194a-173">La herramienta **problemas** agrega advertencias al explorador de una forma estructurada, agregada y con procedimientos, vínculos a recursos afectados en Microsoft Edge DevTools, y proporciona instrucciones sobre cómo corregir los problemas.</span><span class="sxs-lookup"><span data-stu-id="9194a-173">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="9194a-174">Con el tiempo, debería ver cada vez más advertencias en Microsoft Edge en la herramienta **problemas** en lugar de en la **consola**, lo que ayuda a reducir el desorden en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="9194a-174">Over time, you should see more and more warnings in Microsoft Edge surfacing in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="9194a-175">Para empezar, vea [Buscar y corregir problemas con la herramienta problemas de Microsoft Edge DevTools][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="9194a-175">To get started, see [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="La herramienta problemas del cajón de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="9194a-177">La herramienta **problemas** del cajón de DevTools</span><span class="sxs-lookup"><span data-stu-id="9194a-177">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-178">[#1068116][CR1068116] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-178">Chromium issue [#1068116][CR1068116]</span></span>  

### <span data-ttu-id="9194a-179">Ver información de accesibilidad en la información sobre herramientas del modo inspeccionar</span><span class="sxs-lookup"><span data-stu-id="9194a-179">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="9194a-180">La información sobre herramientas del **modo de inspección** ahora indica si el elemento tiene un [nombre y una función][WebhintHintsAxeNameRoleValue] accesibles y tiene el [teclado enfocado][WebhintHintsAxeKeyboard].</span><span class="sxs-lookup"><span data-stu-id="9194a-180">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Información sobre herramientas de modo inspeccionar con información de accesibilidad" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="9194a-182">Información sobre herramientas de **modo inspeccionar** con información de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="9194a-182">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-183">[#1040025][CR1040025] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-183">Chromium issue [#1040025][CR1040025]</span></span>  

### <span data-ttu-id="9194a-184">Actualizaciones del panel de rendimiento</span><span class="sxs-lookup"><span data-stu-id="9194a-184">Performance panel updates</span></span>  

#### <span data-ttu-id="9194a-185">Ver la información de tiempo de bloqueo total en el pie de página</span><span class="sxs-lookup"><span data-stu-id="9194a-185">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="9194a-186">Después de grabar el rendimiento de la carga, el panel **rendimiento** ahora muestra la información de tiempo de bloqueo total \ (TBT \) en el pie de página.</span><span class="sxs-lookup"><span data-stu-id="9194a-186">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="9194a-187">TBT es una métrica de rendimiento de carga que ayuda a cuantificar cuánto tarda una página en ser utilizable.</span><span class="sxs-lookup"><span data-stu-id="9194a-187">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="9194a-188">Esencialmente mide cuánto tiempo una página parece ser utilizable \ (porque el contenido se representa en la pantalla \); pero no es realmente utilizable, porque JavaScript está bloqueando el subproceso principal y, por consiguiente, la página no responde a la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="9194a-188">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="9194a-189">TBT es la métrica principal para aproximar el primer retraso de entrada.</span><span class="sxs-lookup"><span data-stu-id="9194a-189">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="9194a-190">Para obtener información sobre el tiempo de bloqueo total, no **Refresh Page** use el ![ flujo de trabajo actualizar icono de la página actualizar página ][ImageRefreshPageIcon] para grabar el rendimiento de carga de la página.</span><span class="sxs-lookup"><span data-stu-id="9194a-190">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="9194a-191">En su lugar, **Record** seleccione ![ el icono grabar Registro ][ImageRecordIcon] , vuelva a cargar manualmente la página, espere a que se cargue la página y, a continuación, detenga la grabación.</span><span class="sxs-lookup"><span data-stu-id="9194a-191">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="9194a-192">Si ves `Total Blocking Time: Unavailable` , Microsoft Edge DevTools no obtiene la información necesaria de los datos internos de generación de perfiles en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9194a-192">If you see `Total Blocking Time: Unavailable`, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Información sobre el tiempo de bloqueo total en el pie de página de una grabación del panel rendimiento" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="9194a-194">Información sobre el tiempo de bloqueo total en el pie de página de una grabación del panel **rendimiento**</span><span class="sxs-lookup"><span data-stu-id="9194a-194">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-195">[#1054381][CR1054381] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-195">Chromium issue [#1054381][CR1054381]</span></span>  

#### <span data-ttu-id="9194a-196">Diseño de eventos de desplazamiento en la nueva sección de la experiencia</span><span class="sxs-lookup"><span data-stu-id="9194a-196">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="9194a-197">La nueva sección de **experiencia** del panel **rendimiento** le ayuda a detectar los cambios de diseño.</span><span class="sxs-lookup"><span data-stu-id="9194a-197">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="9194a-198">La función de distribución acumulativa \ (CLS \) es una métrica que ayuda a cuantificar la inestabilidad visual no deseada.</span><span class="sxs-lookup"><span data-stu-id="9194a-198">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="9194a-199">Seleccione el evento de **desplazamiento de diseño** para ver los detalles de los cambios de diseño en el panel **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="9194a-199">Select the **Layout Shift** event to see the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="9194a-200">Mantenga el mouse sobre los campos **movido desde** y **movido a** para visualizar dónde se produjo el desplazamiento de diseño.</span><span class="sxs-lookup"><span data-stu-id="9194a-200">Hover over the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Detalles de un desplazamiento de diseño" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="9194a-202">Detalles de un desplazamiento de diseño</span><span class="sxs-lookup"><span data-stu-id="9194a-202">The details of a layout shift</span></span>  
:::image-end:::  

### <span data-ttu-id="9194a-203">Terminología de promesas más exacta en la consola</span><span class="sxs-lookup"><span data-stu-id="9194a-203">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="9194a-204">Al iniciar sesión `Promise` , el valor proporcionado en la **consola** incorrectamente `PromiseStatus` establecido en `resolved` .</span><span class="sxs-lookup"><span data-stu-id="9194a-204">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Un ejemplo de la consola con la terminología anterior resuelta" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="9194a-206">Ejemplo de la **consola** con la terminología antigua `resolved`</span><span class="sxs-lookup"><span data-stu-id="9194a-206">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-207">La **consola** ahora usa el término `fulfilled` , que se alinea con la `Promise` especificación.</span><span class="sxs-lookup"><span data-stu-id="9194a-207">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="9194a-208">Para obtener más información sobre la `Promise` especificación, consulte [Estados y Fates en github](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="9194a-208">For more information about the `Promise` specification, see [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Un ejemplo de la consola con la nueva terminología completada" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="9194a-210">Un ejemplo de la **consola** con la nueva `fulfilled` terminología</span><span class="sxs-lookup"><span data-stu-id="9194a-210">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-211">V8 [#6751][CRV86751] de problemas</span><span class="sxs-lookup"><span data-stu-id="9194a-211">V8 issue [#6751][CRV86751]</span></span>  

### <span data-ttu-id="9194a-212">Actualizaciones del panel estilos</span><span class="sxs-lookup"><span data-stu-id="9194a-212">Styles pane updates</span></span>  

#### <span data-ttu-id="9194a-213">Compatibilidad con la palabra clave Revert</span><span class="sxs-lookup"><span data-stu-id="9194a-213">Support for the revert keyword</span></span>  

<span data-ttu-id="9194a-214">La interfaz de usuario de autocompletar del panel **estilos** ahora detecta la palabra clave [Revert][MDNRevert] CSS, que revierte el valor de una propiedad en cascada al valor anterior que se aplica al estilo del elemento.</span><span class="sxs-lookup"><span data-stu-id="9194a-214">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Establecer el valor de una propiedad para revertir" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="9194a-216">Establecer el valor de una propiedad para revertir</span><span class="sxs-lookup"><span data-stu-id="9194a-216">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-217">[#1075437][CR1075437] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-217">Chromium issue [#1075437][CR1075437]</span></span>  

#### <span data-ttu-id="9194a-218">Vistas previas de imágenes</span><span class="sxs-lookup"><span data-stu-id="9194a-218">Image previews</span></span>  

<span data-ttu-id="9194a-219">Mantenga el mouse sobre un `background-image` valor en el panel **estilos** para obtener una vista previa de la imagen en una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="9194a-219">Hover over a `background-image` value in the **Styles** pane to see a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Mantener el puntero sobre un valor de imagen de fondo" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="9194a-221">Mantener el puntero sobre un `background-image` valor</span><span class="sxs-lookup"><span data-stu-id="9194a-221">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-222">[#1040019][CR1040019] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-222">Chromium issue [#1040019][CR1040019]</span></span>  

#### <span data-ttu-id="9194a-223">El selector de colores ahora usa una notación de color funcional separada por espacios</span><span class="sxs-lookup"><span data-stu-id="9194a-223">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="9194a-224">El [módulo de color CSS nivel 4][CSSWGDraftsColor4Changes3] especifica que las funciones de color, como `rgb()` , deben admitir argumentos separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="9194a-224">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="9194a-225">Por ejemplo, `rgb(0, 0, 0)` equivale a `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="9194a-225">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="9194a-226">Al elegir colores con el [selector de colores][DevtoolsCssReferenceColorPicker] o alternar entre representaciones de color en el panel **estilos** , si mantiene presionado `Shift` el `background-color` valor, debería ver la sintaxis de los argumentos separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="9194a-226">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, you should see the space-separated argument syntax.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Usar argumentos separados por espacios en el panel estilos" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="9194a-228">Usar argumentos separados por espacios en el panel **estilos**</span><span class="sxs-lookup"><span data-stu-id="9194a-228">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="9194a-229">También debe ver la sintaxis en el panel **calculado** y en la información sobre herramientas del **modo inspeccionar** .</span><span class="sxs-lookup"><span data-stu-id="9194a-229">You should also see the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="9194a-230">Microsoft Edge DevTools usa la nueva sintaxis porque las próximas características CSS, como [color ()][CSSWGDraftsColor4Property] , no admiten la sintaxis de argumentos separados por comas obsoletas.</span><span class="sxs-lookup"><span data-stu-id="9194a-230">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="9194a-231">La sintaxis de argumentos separados por espacios es compatible con la mayoría de los exploradores durante un rato.</span><span class="sxs-lookup"><span data-stu-id="9194a-231">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="9194a-232">Para obtener más información, vea [¿puedo usar las notas de colores funcionales separadas por espacios?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="9194a-232">For more information, see [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="9194a-233">[#1072952][CR1072952] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="9194a-233">Chromium issue [#1072952][CR1072952]</span></span>  

### <span data-ttu-id="9194a-234">Desuso del panel de propiedades en el panel elementos</span><span class="sxs-lookup"><span data-stu-id="9194a-234">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="9194a-235">El panel de **propiedades** del panel **elementos** está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="9194a-235">The **Properties** pane in the **Elements** panel is deprecated.</span></span>  <span data-ttu-id="9194a-236">`console.dir($0)`En su lugar, se ejecuta en la **consola** .</span><span class="sxs-lookup"><span data-stu-id="9194a-236">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="El panel Propiedades obsoletas" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="9194a-238">El panel **propiedades** obsoletas</span><span class="sxs-lookup"><span data-stu-id="9194a-238">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <span data-ttu-id="9194a-239">Referencias</span><span class="sxs-lookup"><span data-stu-id="9194a-239">References</span></span>  

*   [<span data-ttu-id="9194a-240">Console. dir ()</span><span class="sxs-lookup"><span data-stu-id="9194a-240">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="9194a-241">$0</span><span class="sxs-lookup"><span data-stu-id="9194a-241">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <span data-ttu-id="9194a-242">Compatibilidad con los métodos abreviados de aplicaciones en el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="9194a-242">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="9194a-243">Los accesos directos a aplicaciones ayudan a los usuarios a iniciar rápidamente las tareas comunes o recomendadas dentro de una aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="9194a-243">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="9194a-244">El menú de métodos abreviados de la aplicación solo se muestra para las [aplicaciones web progresivas][PwaIndex] que se instalan en el dispositivo móvil o de escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="9194a-244">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Accesos directos a aplicaciones en el panel manifiesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="9194a-246">Accesos directos a aplicaciones en el panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="9194a-246">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="9194a-247">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="9194a-247">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="9194a-248">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9194a-248">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="9194a-249">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9194a-249">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="9194a-250">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9194a-250">Getting in touch with Microsoft Edge Devtools team</span></span>  

  

<span data-ttu-id="9194a-251">Para comentar las nuevas características y cambios de la publicación, o cualquier otro tema relacionado con DevTools:</span><span class="sxs-lookup"><span data-stu-id="9194a-251">To discuss the new features and changes in the post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="9194a-252">Envíe sus comentarios con el icono de **comentarios** en el DevTools</span><span class="sxs-lookup"><span data-stu-id="9194a-252">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="9194a-253">Tweet a [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="9194a-253">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="9194a-254">Enviar una sugerencia a [la web][TheWebWeWant] que queremos</span><span class="sxs-lookup"><span data-stu-id="9194a-254">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="9194a-255">Archivar errores en esta página en el repositorio [Edge-desarrollador][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="9194a-255">File bugs on this page in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="El icono de comentarios en el DevTools de Microsoft Edge" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  <span data-ttu-id="9194a-257">El icono de **comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9194a-257">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icono configuración de DevTools"
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "Botón de alternancia de DevTools"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Icono de página de actualización del panel de rendimiento de DevTools"
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Icono de registro del panel de rendimiento de DevTools"

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Usar el emulador Surface Duo | Microsoft docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "DIR-consola de referencia de API | Microsoft docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto de JavaScript: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar los colores con el selector de colores-referencia de CSS | Microsoft docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón: personalizar información general | Microsoft docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la ficha problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introducción a la depuración remota dispositivos Android | Microsoft docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Introducción a los emuladores de superficies de depuración remota Duo | Microsoft docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota dispositivos con Windows 10 | Microsoft docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Revise los detalles del recurso | Microsoft docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red | Microsoft docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicación Microsoft Edge Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notas de colores funcionales separadas por espacios: MDN | ¿Puedo usar"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de cromo"  
[CR1040019]: https://crbug.com/1040019 "DevTools: obtener fácilmente una vista previa de imágenes e imágenes de fondo en el panel estilos | Errores de cromo"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Mostrar información de a11y básica en el elemento popover | Errores de cromo"  
[CR1048378]: https://crbug.com/1048378 "Compatibilidad con la interfaz de usuario de DevTools para el modo de contraste alto | Errores de cromo"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Errores de cromo"  
[CR1068116]: https://crbug.com/1068116 "Panel de problemas de envío | Errores de cromo"  
[CR1072952]: https://crbug.com/1072952 "DevTools: el selector de colores debe producir sintaxis de color CSS moderna | Errores de cromo"  
[CR1075437]: https://crbug.com/1075437 "DevTools: agregar compatibilidad con la palabra clave ' Revert ' de CSS | Errores de cromo"  
[CR1076112]: https://crbug.com/1076112 "Personalización de DevTools: el tamaño del cajón"  
[CR1081486]: https://crbug.com/1081486 "El foco del teclado no está visible para los botones de navegación en el modo de screencast | Errores de cromo"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus debe ser ' cumplida ', no ' resuelto ' | Errores de la V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Cambios de colores 3-módulo de color CSS nivel 4 | Borradores del editor del grupo de trabajo CSS W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. color de primer plano: el ' color ': módulo de color CSS nivel 4 | Borradores del editor del grupo de trabajo CSS W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Presentamos el nuevo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados y Fates-Domenic/promesas: desenvolver | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "revertir | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidad de explorador | MDN"  

[VSCode]: https://code.visualstudio.com/ "Código de Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Métodos abreviados de teclado de código de Visual Studio para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: teclado | Sugerencia"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: valor del rol de nombre | Sugerencia"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activar o desactivar el modo de alto contraste en Windows | Soporte técnico de Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="9194a-306">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9194a-306">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9194a-307">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/05/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="9194a-307">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9194a-309">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9194a-309">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
