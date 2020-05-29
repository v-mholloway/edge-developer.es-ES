---
description: Familiarizarse con las herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
title: Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629507"
---
# <span data-ttu-id="7487c-104">Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="7487c-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

<span data-ttu-id="7487c-105">Los DevTools de Microsoft Edge \ (EdgeHTML \) están creados con [TypeScript][|::ref1::|Index], con tecnología de [código abierto][GithubMicrosoftChakracore], optimizado para los flujos de trabajo front-end modernos y ahora disponibles como una [aplicación independiente de Windows 10][MicrosoftStoreEdgeDevtoolsPreview] en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7487c-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="7487c-106">Para obtener más información sobre las características más recientes, consulte [DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="7487c-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="7487c-107">Herramientas básicas</span><span class="sxs-lookup"><span data-stu-id="7487c-107">Core tools</span></span>  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   <span data-ttu-id="7487c-109">Microsoft Edge (EdgeHTML) DevTools</span><span class="sxs-lookup"><span data-stu-id="7487c-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="7487c-110">La DevTools de Microsoft Edge \ (EdgeHTML \) incluye:</span><span class="sxs-lookup"><span data-stu-id="7487c-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="7487c-111">Un panel [elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML y CSS, inspeccionar propiedades de accesibilidad, ver detectores de eventos y establecer puntos de interrupción de mutación Dom</span><span class="sxs-lookup"><span data-stu-id="7487c-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="7487c-112">Una [consola][DevtoolsGuideEdgehtml|::ref3::|] para ver y filtrar los mensajes de registro, inspeccionar objetos de JavaScript y nodos DOM y ejecutar JavaScript en el contexto de la ventana o el marco seleccionado</span><span class="sxs-lookup"><span data-stu-id="7487c-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="7487c-113">Un [depurador][DevtoolsGuideEdgehtml|::ref4::|] para recorrer el código, establecer relojes y puntos de interrupción, editar en vivo el código e inspeccionar el almacenamiento web y las cachés de cookies</span><span class="sxs-lookup"><span data-stu-id="7487c-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="7487c-114">Panel de [red][DevtoolsGuideEdgehtml|::ref5::|] para supervisar e inspeccionar solicitudes y respuestas desde la red y la caché del explorador</span><span class="sxs-lookup"><span data-stu-id="7487c-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="7487c-115">Un panel de [rendimiento][DevtoolsGuideEdgehtml|::ref6::|] para perfilar el tiempo y los recursos del sistema que necesita su sitio</span><span class="sxs-lookup"><span data-stu-id="7487c-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="7487c-116">Panel [memoria][DevtoolsGuideEdgehtml|::ref7::|] para medir el uso de los recursos de memoria y Comparar instantáneas de montones en diferentes Estados de tiempo de ejecución de código</span><span class="sxs-lookup"><span data-stu-id="7487c-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="7487c-117">Panel de [almacenamiento][DevtoolsGuideEdgehtml|::ref8::|] para inspeccionar y administrar el almacenamiento Web, IndexedDB, cookies y datos de la caché</span><span class="sxs-lookup"><span data-stu-id="7487c-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="7487c-118">Un panel de [trabajo de servicios][DevtoolsGuideEdgehtmlServiceworkers] para la administración y la depuración de los trabajadores de servicios</span><span class="sxs-lookup"><span data-stu-id="7487c-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="7487c-119">Un panel de [emulación][DevtoolsGuideEdgehtml|::ref9::|] para probar su sitio con diferentes perfiles de explorador, resoluciones de pantalla y coordenadas de ubicación GPS</span><span class="sxs-lookup"><span data-stu-id="7487c-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="7487c-120">¡ Sigue enviando tus [comentarios y solicitudes de características](#feedback)!</span><span class="sxs-lookup"><span data-stu-id="7487c-120">Please keep sending your [feedback and feature requests](#feedback)!</span></span>  

> [!TIP]
> <span data-ttu-id="7487c-121">[Prueba en Microsoft Edge \ (EdgeHTML \) gratis desde cualquier explorador][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="7487c-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="7487c-122">El equipo de Microsoft Edge se asoció con [BrowserStack][BrowserstackEdgehtml] para ofrecer pruebas gratuitas en vivo y automatizadas en Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="7487c-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="7487c-123">Aplicación de la Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7487c-123">Microsoft Store app</span></span>  

<span data-ttu-id="7487c-124">Los **DevTools de Microsoft Edge \ (EdgeHTML \)** [ahora están disponibles][DevtoolsGuideEdgehtmlWhatsnew] como una [aplicación independiente de Windows 10 en Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], además de la experiencia de herramientas en el explorador \ ( `F12` \).</span><span class="sxs-lookup"><span data-stu-id="7487c-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="7487c-125">La versión de la tienda viene con un panel de **selección** para adjuntar a destinos de página locales y remotos y un diseño con fichas para facilitar el cambio entre instancias de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7487c-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="7487c-126">Depuración local</span><span class="sxs-lookup"><span data-stu-id="7487c-126">Local debugging</span></span>  

<span data-ttu-id="7487c-127">Para depurar una página de forma local, simplemente inicia la aplicación Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7487c-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="7487c-128">El panel **local** del selector muestra todos los procesos de contenido de EdgeHTML activos, incluidas las pestañas del explorador abierto, que ejecutan [PWAs][PwasEdgehtmlIndex] \ ( `WWAHost.exe` procesos \) y los controles de [WebView][HostingWebview] .</span><span class="sxs-lookup"><span data-stu-id="7487c-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="7487c-129">Seleccione el destino que desea adjuntar y abra una nueva pestaña de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="7487c-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Panel local de la aplicación DevTools":::
   <span data-ttu-id="7487c-131">Panel local de la aplicación DevTools</span><span class="sxs-lookup"><span data-stu-id="7487c-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="7487c-132">Depuración remota</span><span class="sxs-lookup"><span data-stu-id="7487c-132">Remote debugging</span></span>  

<span data-ttu-id="7487c-133">La aplicación Microsoft Edge DevTools presenta compatibilidad básica para la depuración de páginas en un equipo remoto a través de nuestro nuevo [Protocolo de DevTools][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="7487c-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="7487c-134">Con la última versión, se obtiene acceso remoto a la funcionalidad principal en el [depurador][DevtoolsGuideEdgehtml|::ref10::|]: [los elementos][DevtoolsGuideEdgehtml|::ref11::|] \ (para las operaciones de solo lectura \) y los paneles de [consola][DevtoolsGuideEdgehtml|::ref12::|] .</span><span class="sxs-lookup"><span data-stu-id="7487c-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="7487c-135">La depuración remota está limitada a Microsoft Edge \ (EdgeHTML \) ejecutando hosts de escritorio, con compatibilidad para otros hosts de EdgeHTML y dispositivos Windows 10 que se publiquen en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="7487c-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="7487c-136">Para comenzar, consulta la sección [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] de los documentos de [Protocolo de DevTools][DevtoolsProtocolEdgehtmlIndex] .</span><span class="sxs-lookup"><span data-stu-id="7487c-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Panel remoto de aplicaciones de DevTools":::
   <span data-ttu-id="7487c-138">Panel remoto de aplicaciones de DevTools</span><span class="sxs-lookup"><span data-stu-id="7487c-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="7487c-139">Métodos abreviados generales</span><span class="sxs-lookup"><span data-stu-id="7487c-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="7487c-140">Todos los métodos abreviados se han verificado en la versión más reciente de Windows.</span><span class="sxs-lookup"><span data-stu-id="7487c-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="7487c-141">Si no puede usar un acceso directo, actualice su copia de Windows.</span><span class="sxs-lookup"><span data-stu-id="7487c-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="7487c-142">Estos métodos abreviados controlan la ventana principal de DevTools y deben funcionar en todas las herramientas.</span><span class="sxs-lookup"><span data-stu-id="7487c-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="7487c-143">Acción</span><span class="sxs-lookup"><span data-stu-id="7487c-143">Action</span></span> | <span data-ttu-id="7487c-144">Método abreviado</span><span class="sxs-lookup"><span data-stu-id="7487c-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="7487c-145">Mostrar u ocultar DevTools \ (se abre en el panel de última vista \)</span><span class="sxs-lookup"><span data-stu-id="7487c-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="7487c-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="7487c-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="7487c-147">Activar o desactivar el acoplamiento \ (desacoplar/inferior/derecha \)</span><span class="sxs-lookup"><span data-stu-id="7487c-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="7487c-148">Abrir archivo</span><span class="sxs-lookup"><span data-stu-id="7487c-148">Open file</span></span> | `Ctrl`<span data-ttu-id="7487c-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="7487c-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="7487c-150">Mostrar código fuente HTML no modificable en el depurador</span><span class="sxs-lookup"><span data-stu-id="7487c-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="7487c-151">Mostrar u ocultar consola en la parte inferior de cualquier otra herramienta</span><span class="sxs-lookup"><span data-stu-id="7487c-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="7487c-152">Cambiar a elementos \ (explorador DOM \)</span><span class="sxs-lookup"><span data-stu-id="7487c-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="7487c-153">Cambiar a consola</span><span class="sxs-lookup"><span data-stu-id="7487c-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="7487c-154">Cambiar a depurador</span><span class="sxs-lookup"><span data-stu-id="7487c-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="7487c-155">Cambiar a red</span><span class="sxs-lookup"><span data-stu-id="7487c-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="7487c-156">Cambiar al rendimiento</span><span class="sxs-lookup"><span data-stu-id="7487c-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="7487c-157">Cambiar a memoria</span><span class="sxs-lookup"><span data-stu-id="7487c-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="7487c-158">Cambiar a la emulación</span><span class="sxs-lookup"><span data-stu-id="7487c-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="7487c-159">Documento de ayuda</span><span class="sxs-lookup"><span data-stu-id="7487c-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="7487c-160">Siguiente herramienta</span><span class="sxs-lookup"><span data-stu-id="7487c-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="7487c-161">Herramienta anterior</span><span class="sxs-lookup"><span data-stu-id="7487c-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="7487c-162">Herramienta anterior \ (desde historial \)</span><span class="sxs-lookup"><span data-stu-id="7487c-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="7487c-163">Siguiente herramienta \ (desde historial \)</span><span class="sxs-lookup"><span data-stu-id="7487c-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="7487c-164">Submarco siguiente</span><span class="sxs-lookup"><span data-stu-id="7487c-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="7487c-165">Submarco anterior</span><span class="sxs-lookup"><span data-stu-id="7487c-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="7487c-166">Coincidencia siguiente en el cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="7487c-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="7487c-167">Coincidencia anterior en el cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="7487c-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="7487c-168">Buscar en el cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="7487c-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="7487c-169">Dar el foco a la consola en la parte inferior</span><span class="sxs-lookup"><span data-stu-id="7487c-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="7487c-170">Iniciar DevTools a la consola</span><span class="sxs-lookup"><span data-stu-id="7487c-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="7487c-171">Actualizar la página</span><span class="sxs-lookup"><span data-stu-id="7487c-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="7487c-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="7487c-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="7487c-173">Si está depurando un punto de interrupción y se encuentra en pausa, la acción **actualizar la página** reanuda el tiempo de ejecución en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="7487c-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="7487c-174">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7487c-174">Feedback</span></span>  

<span data-ttu-id="7487c-175">Envíanos tus comentarios para ayudar a mejorar la DevTools de Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="7487c-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="7487c-176">Simplemente abre las herramientas \ ( `F12` \) y selecciona el botón [Enviar comentarios](#microsoft-edge-edgehtml-developer-tools) .</span><span class="sxs-lookup"><span data-stu-id="7487c-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="7487c-177">Conviértase en un [Windows Insider][WindowsInsiderProgram] para obtener una vista previa de las [características más recientes de la DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="7487c-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="7487c-178">Use la aplicación Hub de comentarios de Windows para publicar, votar, realizar un seguimiento y obtener soporte técnico para sugerencias y problemas generales de Windows.</span><span class="sxs-lookup"><span data-stu-id="7487c-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Sola"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulación"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Memoria"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Red"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Comportamiento"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Trabajadores de servicio"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Storage"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo Microsoft Edge (EdgeHTML) DevTools"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview-clientes de protocolo DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "Vista de WebView (EdgeHTML) para aplicaciones de Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicaciones web progresivas (EdgeHTML) en Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Vista previa de Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Prueba gratuita del explorador Microsoft Edge BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "Llena"  
