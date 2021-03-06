---
description: Usa DevTools en el modo de contraste alto de Windows, coincide con los métodos abreviados de teclado en DevTools para Visual Studio código y mucho más.
title: Novedades de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 701c328c1dc975a81129049fe2931139757205c3
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398577"
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

# <a name="whats-new-in-devtools-microsoft-edge-84"></a><span data-ttu-id="4cc06-104">Novedades de DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="4cc06-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4cc06-105">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4cc06-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="4cc06-106">Las siguientes secciones son una lista de anuncios que puede que falte del equipo de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="4cc06-107">Echa un vistazo a los anuncios para probar nuevas características en DevTools, microsoft Visual Studio code extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="4cc06-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="4cc06-108">Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] y [síganos en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="4cc06-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a><span data-ttu-id="4cc06-109">Usar DevTools en el modo de contraste alto de Windows</span><span class="sxs-lookup"><span data-stu-id="4cc06-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="4cc06-110">Las DevTools de Microsoft Edge ahora se muestran en modo de contraste alto cuando Windows está en modo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="4cc06-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en modo de contraste alto" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="4cc06-112">Microsoft Edge DevTools en modo de contraste alto</span><span class="sxs-lookup"><span data-stu-id="4cc06-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-113">[Siga las instrucciones para activar el modo de contraste alto en Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="4cc06-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="4cc06-114">Para abrir DevTools en Microsoft Edge, seleccione `F12` o `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="4cc06-114">To open the DevTools in Microsoft Edge, select `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="4cc06-115">Las DevTools se muestran en modo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="4cc06-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="4cc06-116">Microsoft Edge DevTools admite actualmente el modo de contraste alto en Windows, pero no en macOS.</span><span class="sxs-lookup"><span data-stu-id="4cc06-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span>  

<span data-ttu-id="4cc06-117">Problema de [chromium #1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="4cc06-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a><span data-ttu-id="4cc06-118">Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="4cc06-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="4cc06-119">De [sus](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios y del rastreador de problemas [públicos chromium,][CRIssuesList]el equipo de DevTools de Microsoft Edge aprendió que deseaba la posibilidad de personalizar los métodos abreviados de teclado en DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="4cc06-120">En Microsoft Edge 84, ahora puedes hacer coincidir los métodos abreviados de teclado en DevTools [para Visual Studio Code,][VisualStudioCode]que es solo una de las características en las que el equipo está trabajando para personalizar los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="4cc06-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VisualStudioCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="4cc06-122">Microsoft Edge DevTools en modo de contraste alto</span><span class="sxs-lookup"><span data-stu-id="4cc06-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-123">Para probar el experimento, abra Configuración de DevTools seleccionando o seleccionando el icono Configuración de DevTools en la esquina superior derecha de `?` ![ ][ImageSettingsIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-123">To try the experiment, open DevTools Settings by selecting `?` or choosing the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="4cc06-124">Vaya a la **sección Experimentos y** active la pestaña Habilitar la configuración de métodos abreviados de teclado **personalizados (requiere volver a cargar).**</span><span class="sxs-lookup"><span data-stu-id="4cc06-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="4cc06-125">Ahora vuelve a cargar DevTools, abre Configuración de nuevo y navega a la sección **Accesos directos.**</span><span class="sxs-lookup"><span data-stu-id="4cc06-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="4cc06-126">Elija **DevTools (Valor predeterminado)** en el menú desplegable Coincidencia **de accesos directos** de la lista desplegable preestablecido y **seleccione Visual Studio Código**.</span><span class="sxs-lookup"><span data-stu-id="4cc06-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="4cc06-127">Los métodos abreviados de teclado de DevTools ahora coinciden con los métodos abreviados para acciones equivalentes en Visual Studio código.</span><span class="sxs-lookup"><span data-stu-id="4cc06-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="4cc06-128">Por ejemplo, el método abreviado de teclado para pausar o continuar ejecutando un script [en Visual Studio Code][VisualStudioCodeShortcuts] es `F5` .</span><span class="sxs-lookup"><span data-stu-id="4cc06-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="4cc06-129">Con el valor **preestablecido DevTools (predeterminado),** ese mismo acceso directo en DevTools es, pero con el valor preestablecido Visual Studio `F8` **Code,** ese acceso directo ahora también es `F5` .</span><span class="sxs-lookup"><span data-stu-id="4cc06-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="4cc06-130">La característica está disponible actualmente en Microsoft Edge 84 como un experimento, así que comparta sus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) con el equipo.</span><span class="sxs-lookup"><span data-stu-id="4cc06-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="4cc06-131">Problema de [chromium #174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="4cc06-131">Chromium issue [#174309][CR174309]</span></span>  

### <a name="remote-debug-surface-duo-emulators"></a><span data-ttu-id="4cc06-132">Emuladores de Surface Duo de depuración remota</span><span class="sxs-lookup"><span data-stu-id="4cc06-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="4cc06-133">Ahora puedes depurar de forma remota el contenido web que se ejecuta en el emulador [de Surface Duo][DualScreensAndroidEmulator] con toda la potencia de Microsoft Edge [DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="4cc06-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="4cc06-134">Con el [emulador de Surface Duo,][DualScreensAndroidEmulator]puedes probar cómo se representa el contenido web en una nueva clase de dispositivos de pantalla doble y plegables.</span><span class="sxs-lookup"><span data-stu-id="4cc06-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="4cc06-135">El emulador ejecuta el sistema operativo Android y proporciona la [aplicación Android de Microsoft Edge.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="4cc06-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="4cc06-136">Cargue el contenido web en la [aplicación Microsoft Edge][AndroidEdge] y depurelo con Microsoft Edge [DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="4cc06-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="La aplicación de Microsoft Edge que se ejecuta en el emulador de Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="4cc06-138">La aplicación Microsoft Edge en el emulador de Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4cc06-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-139">La página de una instancia de escritorio de Microsoft Edge muestra `edge://inspect` **SurfaceDuoEmulator** [][DesktopEdge] con una lista de las pestañas abiertas o [pwas][PwaIndex] que se ejecutan en el emulador [de Surface Duo][DualScreensAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="4cc06-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La edge://inspect muestra una lista de las pestañas abiertas en la aplicación de Microsoft Edge que se ejecuta en el emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="4cc06-141">La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación microsoft edge que se ejecuta en el emulador</span><span class="sxs-lookup"><span data-stu-id="4cc06-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="4cc06-142">Elija **inspeccionar** la pestaña o PWA que desea depurar para abrir [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="4cc06-142">Choose **inspect** for the tab or PWA that you want to debug to open the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="4cc06-143">Sigue la guía paso a paso para depurar de forma remota el contenido [web en el emulador de Surface Duo.][DevToolsRemoteDebugDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="4cc06-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <a name="resize-the-devtools-drawer-more-easily"></a><span data-ttu-id="4cc06-144">Cambiar el tamaño del cajón de DevTools más fácilmente</span><span class="sxs-lookup"><span data-stu-id="4cc06-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="4cc06-145">En Microsoft Edge 83 o versiones anteriores, solo era posible cambiar el tamaño del cajón [de DevTools][DevToolsDrawer] activando el mouse dentro de la barra de herramientas del cajón.</span><span class="sxs-lookup"><span data-stu-id="4cc06-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the toolbar of the Drawer.</span></span>  <span data-ttu-id="4cc06-146">El drawer se comportó de forma diferente que los demás controles de cambio de tamaño de los paneles de DevTools donde se mantiene el mouse en el borde del panel para cambiar su tamaño.</span><span class="sxs-lookup"><span data-stu-id="4cc06-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane to resize it.</span></span>  <span data-ttu-id="4cc06-147">Elija la siguiente imagen para mostrar cómo funcionaba el tamaño del cajón en la versión 83 o anterior de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4cc06-147">Choose the following image to display how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Redimensionar el cajón de DevTools en Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="4cc06-149">Redimensionar el cajón de DevTools en Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="4cc06-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="4cc06-150">A partir de Microsoft Edge 84, ahora puedes cambiar el tamaño del cajón activando el mouse sobre el borde del cajón.</span><span class="sxs-lookup"><span data-stu-id="4cc06-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="4cc06-151">Este cambio alinea el comportamiento cambiando el tamaño del cajón de DevTools con la forma en que cambia el tamaño de otros paneles en DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="4cc06-152">Elija la siguiente imagen para mostrar el tamaño en acción en Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="4cc06-152">Choose the following image to display resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Redimensionar el cajón de DevTools en Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="4cc06-154">Redimensionar el cajón de DevTools en Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="4cc06-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="4cc06-155">Problema de [chromium #1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="4cc06-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <a name="screencasting-navigation-buttons-display-focus"></a><span data-ttu-id="4cc06-156">Foco de visualización de botones de navegación de difusión por pantalla</span><span class="sxs-lookup"><span data-stu-id="4cc06-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="4cc06-157">Al depurar de forma remota un dispositivo [Android,][DevToolsRemoteDebugAndroid]un dispositivo [Windows 10][DevToolsRemoteDebugWindows]o un emulador de [Surface Duo,][DevToolsRemoteDebugDuoEmulator]puedes alternar la difusión por pantalla con el icono Alternar difusión en pantalla en la esquina superior izquierda de ![ ][ImageScreencastingIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="4cc06-158">Con la difusión por pantalla habilitada, puedes navegar por la pestaña de Microsoft Edge en el dispositivo remoto desde la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="4cc06-159">En Microsoft Edge 84, estos botones de navegación ahora también son accesibles con el teclado.</span><span class="sxs-lookup"><span data-stu-id="4cc06-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Seleccionar Mayús+Tab en la barra url proyectada en pantalla muestra el foco en el botón Actualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="4cc06-161">Select `Shift` + `Tab` from the screencasted URL bar shows focus on the **Refresh** button</span><span class="sxs-lookup"><span data-stu-id="4cc06-161">Select `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="4cc06-162">Problema de [chromium #1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="4cc06-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <a name="network-panel-details-pane-is-now-accessible"></a><span data-ttu-id="4cc06-163">Panel de red Panel Detalles panel ahora es accesible</span><span class="sxs-lookup"><span data-stu-id="4cc06-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="4cc06-164">En Microsoft Edge 84, el \*\*\*\* panel Detalles de la herramienta Red ahora se centra cuando se abre para un recurso en el registro [de red][DevToolsNetworkLog]. [][DevToolsNetworkDetails]</span><span class="sxs-lookup"><span data-stu-id="4cc06-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** tool now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="4cc06-165">Este cambio permite a los lectores de pantalla leer e interactuar con el contenido del **panel** Detalles.</span><span class="sxs-lookup"><span data-stu-id="4cc06-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="El panel Detalles del panel Red se centra cuando se abre" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="4cc06-167">El **panel Detalles** de la herramienta **Red** se centra cuando se abre</span><span class="sxs-lookup"><span data-stu-id="4cc06-167">The **Details** pane in the **Network** tool takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="4cc06-168">Problema de [chromium #963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="4cc06-168">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="4cc06-169">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="4cc06-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="4cc06-170">En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 84 que se contribuyeron al proyecto chromium de código abierto.</span><span class="sxs-lookup"><span data-stu-id="4cc06-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="4cc06-171">Corregir problemas del sitio con la nueva herramienta Problemas en el cajón de DevTools</span><span class="sxs-lookup"><span data-stu-id="4cc06-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="4cc06-172">La nueva **herramienta Problemas** del cajón DevTools se creó para ayudar a reducir la fatiga y el desorden de notificaciones de la **consola.**</span><span class="sxs-lookup"><span data-stu-id="4cc06-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="4cc06-173">Actualmente, la **consola es** el lugar central para que desarrolladores de sitios web, bibliotecas, marcos y Microsoft Edge registren mensajes, advertencias y errores.</span><span class="sxs-lookup"><span data-stu-id="4cc06-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="4cc06-174">La **herramienta Problemas** agrega advertencias desde el explorador de una forma estructurada, agregada y que puede actuar, vínculos a recursos afectados dentro de Microsoft Edge DevTools y proporciona instrucciones sobre cómo solucionar los problemas.</span><span class="sxs-lookup"><span data-stu-id="4cc06-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="4cc06-175">Con el tiempo, cada vez hay más advertencias en Microsoft Edge en la herramienta Problemas en lugar de en la consola **,** lo que debería ayudar a reducir el desorden en la \*\*\*\* **consola**.</span><span class="sxs-lookup"><span data-stu-id="4cc06-175">Over time, more and more warnings are surfaced in Microsoft Edge in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="4cc06-176">Para empezar, vaya a [Buscar y corregir problemas con la herramienta Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="4cc06-176">To get started, navigate to [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="La herramienta Problemas en el cajón de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="4cc06-178">La **herramienta Problemas** en el cajón de DevTools</span><span class="sxs-lookup"><span data-stu-id="4cc06-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-179">Problema de [chromium #1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="4cc06-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a><span data-ttu-id="4cc06-180">Ver información de accesibilidad en la información sobre herramientas del modo de inspección</span><span class="sxs-lookup"><span data-stu-id="4cc06-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="4cc06-181">La **información sobre** herramientas del modo de inspección ahora indica si el elemento tiene un nombre y un [rol][WebhintHintsAxeNameRoleValue] accesibles y si se puede centrar en [el teclado.][WebhintHintsAxeKeyboard]</span><span class="sxs-lookup"><span data-stu-id="4cc06-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Información sobre herramientas del modo de inspección con información de accesibilidad" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="4cc06-183">Información **sobre herramientas del modo de** inspección con información de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4cc06-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-184">Problema de [chromium #1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="4cc06-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="4cc06-185">Actualizaciones del panel de rendimiento</span><span class="sxs-lookup"><span data-stu-id="4cc06-185">Performance panel updates</span></span>  

#### <a name="view-total-blocking-time-information-in-the-footer"></a><span data-ttu-id="4cc06-186">Ver información de tiempo de bloqueo total en el pie de página</span><span class="sxs-lookup"><span data-stu-id="4cc06-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="4cc06-187">Después de grabar el rendimiento de carga, **el** panel Rendimiento muestra ahora información del tiempo de bloqueo total \(TBT\) en el pie de página.</span><span class="sxs-lookup"><span data-stu-id="4cc06-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="4cc06-188">TBT es una métrica de rendimiento de carga que ayuda a cuantificar el tiempo que tarda una página en usarse.</span><span class="sxs-lookup"><span data-stu-id="4cc06-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="4cc06-189">Básicamente mide cuánto tiempo parece que una página puede usarse \(porque el contenido se representa en la pantalla\); pero en realidad no se puede usar, porque JavaScript bloquea el subproceso principal y, por lo tanto, la página no responde a la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="4cc06-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="4cc06-190">TBT es la métrica principal para aproximar el retraso de primera entrada.</span><span class="sxs-lookup"><span data-stu-id="4cc06-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="4cc06-191">Para obtener información sobre el tiempo \*\*\*\* total de bloqueo, no use el flujo de trabajo del icono Actualizar página ![ Actualizar página para registrar el rendimiento de carga de ][ImageRefreshPageIcon] página.</span><span class="sxs-lookup"><span data-stu-id="4cc06-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="4cc06-192">En su lugar, **seleccione Grabar** icono de registro, vuelva a cargar manualmente la página, espere a que se cargue la página y, a ![ continuación, detenga la ][ImageRecordIcon] grabación.</span><span class="sxs-lookup"><span data-stu-id="4cc06-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="4cc06-193">Si se muestra, Microsoft Edge DevTools no ha obtiene la información necesaria de los datos de generación de perfiles `Total Blocking Time: Unavailable` internos en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4cc06-193">If `Total Blocking Time: Unavailable` is displayed, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Información de tiempo de bloqueo total en el pie de página de una grabación del panel Rendimiento" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="4cc06-195">Información de tiempo de bloqueo total en el pie de página de una **grabación del** panel Rendimiento</span><span class="sxs-lookup"><span data-stu-id="4cc06-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-196">Problema de [chromium #1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="4cc06-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <a name="layout-shift-events-in-the-new-experience-section"></a><span data-ttu-id="4cc06-197">Eventos Shift de diseño en la nueva sección Experiencia</span><span class="sxs-lookup"><span data-stu-id="4cc06-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="4cc06-198">La nueva **sección Experiencia** del panel **Rendimiento** le ayuda a detectar los turnos de diseño.</span><span class="sxs-lookup"><span data-stu-id="4cc06-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="4cc06-199">Cumulative Layout Shift \(CLS\) es una métrica que ayuda a cuantificar la inestabilidad visual no deseada.</span><span class="sxs-lookup"><span data-stu-id="4cc06-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="4cc06-200">Elija el **evento Layout Shift** para mostrar los detalles del turno de diseño en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="4cc06-200">Choose the **Layout Shift** event to display the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="4cc06-201">Mantenga el mouse en **los campos Movido de** y Movido **a** para visualizar dónde se produjo el cambio de diseño.</span><span class="sxs-lookup"><span data-stu-id="4cc06-201">Hover on the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Los detalles de un turno de diseño" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="4cc06-203">Los detalles de un turno de diseño</span><span class="sxs-lookup"><span data-stu-id="4cc06-203">The details of a layout shift</span></span>  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a><span data-ttu-id="4cc06-204">Terminología de promesas más precisa en la consola</span><span class="sxs-lookup"><span data-stu-id="4cc06-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="4cc06-205">Al registrar un `Promise` , el valor **proporcionado** incorrectamente por la consola se establece `PromiseStatus` en `resolved` .</span><span class="sxs-lookup"><span data-stu-id="4cc06-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Un ejemplo de la consola mediante la terminología antigua resuelta" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="4cc06-207">Un ejemplo de la **consola con** la `resolved` terminología antigua</span><span class="sxs-lookup"><span data-stu-id="4cc06-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-208">La **consola** ahora usa el término `fulfilled` , que se alinea con la `Promise` especificación.</span><span class="sxs-lookup"><span data-stu-id="4cc06-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="4cc06-209">Para obtener más información acerca de `Promise` la especificación, vaya a [Estados y destinos en GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="4cc06-209">For more information about the `Promise` specification, navigate to [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Un ejemplo de la consola mediante la nueva terminología cumplida" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="4cc06-211">Un ejemplo de la **consola mediante** la `fulfilled` nueva terminología</span><span class="sxs-lookup"><span data-stu-id="4cc06-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-212">Problema V8 [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="4cc06-212">V8 issue [#6751][CRV86751]</span></span>  

### <a name="styles-pane-updates"></a><span data-ttu-id="4cc06-213">Actualizaciones del panel Estilos</span><span class="sxs-lookup"><span data-stu-id="4cc06-213">Styles pane updates</span></span>  

#### <a name="support-for-the-revert-keyword"></a><span data-ttu-id="4cc06-214">Compatibilidad con la palabra clave revert</span><span class="sxs-lookup"><span data-stu-id="4cc06-214">Support for the revert keyword</span></span>  

<span data-ttu-id="4cc06-215">La interfaz de usuario de autocompletar del panel **Estilos** ahora detecta la palabra clave [CSS][MDNRevert] revert, que revierte el valor en cascada de una propiedad al valor anterior aplicado al estilo del elemento.</span><span class="sxs-lookup"><span data-stu-id="4cc06-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Establecer el valor de una propiedad para revertir" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="4cc06-217">Establecer el valor de una propiedad para revertir</span><span class="sxs-lookup"><span data-stu-id="4cc06-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-218">Problema de [chromium #1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="4cc06-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <a name="image-previews"></a><span data-ttu-id="4cc06-219">Vistas previas de imágenes</span><span class="sxs-lookup"><span data-stu-id="4cc06-219">Image previews</span></span>  

<span data-ttu-id="4cc06-220">Mantenga el mouse sobre un valor en el panel Estilos para mostrar una `background-image` vista previa de la imagen en una información sobre herramientas. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4cc06-220">Hover on a `background-image` value in the **Styles** pane to display a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Mantener el mouse sobre un valor de imagen de fondo" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="4cc06-222">Pasar el puntero sobre un `background-image` valor</span><span class="sxs-lookup"><span data-stu-id="4cc06-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-223">Problema de [chromium #1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="4cc06-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a><span data-ttu-id="4cc06-224">El Selector de colores ahora usa la notación de color funcional separada por espacios</span><span class="sxs-lookup"><span data-stu-id="4cc06-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="4cc06-225">[Css Color Module Level 4][CSSWGDraftsColor4Changes3] especifica que las funciones de color, como `rgb()` , deben admitir argumentos separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="4cc06-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="4cc06-226">Por ejemplo, `rgb(0, 0, 0)` equivale a `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="4cc06-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="4cc06-227">Al elegir colores [][DevtoolsCssReferenceColorPicker] con el Selector de colores o \*\*\*\* alternar entre representaciones de color en el panel Estilos manteniendo y seleccionando el valor, se muestra la sintaxis del argumento separado `Shift` por `background-color` espacios.</span><span class="sxs-lookup"><span data-stu-id="4cc06-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, the space-separated argument syntax is displayed.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Uso de argumentos separados por espacios en el panel Estilos" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="4cc06-229">Uso de argumentos separados por espacios en el **panel Estilos**</span><span class="sxs-lookup"><span data-stu-id="4cc06-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="4cc06-230">También debe mostrar la sintaxis en el **panel Calculado** y la información sobre herramientas del **modo de** inspección.</span><span class="sxs-lookup"><span data-stu-id="4cc06-230">You should also display the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="4cc06-231">Microsoft Edge DevTools usa la nueva sintaxis porque las próximas características CSS como [color()][CSSWGDraftsColor4Property] no admiten la sintaxis de argumentos separados por comas en desuso.</span><span class="sxs-lookup"><span data-stu-id="4cc06-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="4cc06-232">La sintaxis de argumentos separados por espacios se ha admitido en la mayoría de los exploradores durante un tiempo.</span><span class="sxs-lookup"><span data-stu-id="4cc06-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="4cc06-233">Para obtener más información, vaya [a ¿Puedo usar: notaciones de color funcionales separadas por espacios?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="4cc06-233">For more information, navigate to [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="4cc06-234">Problema de [chromium #1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="4cc06-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a><span data-ttu-id="4cc06-235">Desuso del panel Propiedades en el panel Elementos</span><span class="sxs-lookup"><span data-stu-id="4cc06-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="4cc06-236">El **panel Propiedades** de la herramienta **Elementos** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="4cc06-236">The **Properties** pane in the **Elements** tool is deprecated.</span></span>  <span data-ttu-id="4cc06-237">En `console.dir($0)` su lugar, ejecute **en la** consola.</span><span class="sxs-lookup"><span data-stu-id="4cc06-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="El panel Propiedades en desuso" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="4cc06-239">El panel Propiedades **en desuso**</span><span class="sxs-lookup"><span data-stu-id="4cc06-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <a name="references"></a><span data-ttu-id="4cc06-240">Referencias</span><span class="sxs-lookup"><span data-stu-id="4cc06-240">References</span></span>  

*   [<span data-ttu-id="4cc06-241">console.dir()</span><span class="sxs-lookup"><span data-stu-id="4cc06-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="4cc06-242">$0</span><span class="sxs-lookup"><span data-stu-id="4cc06-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a><span data-ttu-id="4cc06-243">Compatibilidad con accesos directos de aplicaciones en el panel Manifiesto</span><span class="sxs-lookup"><span data-stu-id="4cc06-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="4cc06-244">Los accesos directos de la aplicación ayudan a los usuarios a iniciar rápidamente tareas comunes o recomendadas dentro de una aplicación web.</span><span class="sxs-lookup"><span data-stu-id="4cc06-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="4cc06-245">El menú de accesos directos de la aplicación solo se muestra para [las aplicaciones web][PwaIndex] progresivas que están instaladas en el dispositivo móvil o de escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="4cc06-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Accesos directos de la aplicación en el panel Manifiesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="4cc06-247">Accesos directos de la aplicación en el **panel** Manifiesto</span><span class="sxs-lookup"><span data-stu-id="4cc06-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="4cc06-248">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4cc06-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4cc06-249">Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4cc06-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4cc06-250">Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4cc06-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="4cc06-251">Getting in touch with Microsoft Edge Devtools team</span><span class="sxs-lookup"><span data-stu-id="4cc06-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir: referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto JavaScript: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar colores con el Selector de colores: referencia CSS | Microsoft Docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer: personalizar información general | Microsoft Docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y corregir problemas con la pestaña Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Introducción a los emuladores de Surface Duo de depuración remota | Microsoft Docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota de dispositivos Windows 10 | Microsoft Docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspeccione los detalles del recurso | Microsoft Docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red | Microsoft Docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft Docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicación Android de Microsoft Edge"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notaciones de color funcionales separadas por espacios: MDN | ¿Puedo usar?"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar los métodos abreviados de teclado o los enlaces de teclas | Errores de Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: vista previa de imágenes e imágenes de fondo fácilmente en el panel Estilos | Errores de Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: muestra información básica de a11y en elementos emergentes | Errores de Chromium"  
[CR1048378]: https://crbug.com/1048378 "Compatibilidad con la interfaz de usuario de DevTools para el modo de contraste alto | Errores de Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Errores de Chromium"  
[CR1068116]: https://crbug.com/1068116 "Enviar problemas de panel | Errores de Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: el selector de colores debe producir una sintaxis de color CSS moderna | Errores de Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: agregue compatibilidad con la palabra clave y el valor css 'revert' | Errores de Chromium"  
[CR1076112]: https://crbug.com/1076112 "Personalización de Devtools: cambiador de tamaño de cajón"  
[CR1081486]: https://crbug.com/1081486 "El foco del teclado no está visible para los botones de navegación en modo de difusión | Errores de Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus debe ser "cumplido", no "resuelto" | Errores de V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Cambios de Colors 3 - CSS Color Module Level 4 | Borradores del editor de grupo de trabajo CSS de W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Color de primer plano: el 'color' - Módulo de color CSS Nivel 4 | Borradores del editor de grupo de trabajo CSS de W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Presentación del nuevo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados y destinos: domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "revertir | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidad del explorador | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio código"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio métodos abreviados de teclado de código para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: Teclado | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activar o desactivar el modo de contraste alto en Windows | Compatibilidad con Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de vista previa de Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="4cc06-296">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4cc06-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4cc06-297">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/05/devtools/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4cc06-297">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4cc06-299">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4cc06-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
