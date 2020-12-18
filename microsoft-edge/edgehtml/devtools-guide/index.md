---
description: Conozca las herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
title: Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236137"
---
# <span data-ttu-id="c97ba-104">Herramientas para desarrolladores de Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="c97ba-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

<span data-ttu-id="c97ba-105">Microsoft Edge \(EdgeHTML\) DevTools está creado con [TypeScript][|::ref1::|Index], con tecnología de [Open Source][GithubMicrosoftChakracore], optimizada para los flujos de trabajo front-end modernos y ahora disponible como una [aplicación independiente de Windows 10][MicrosoftStoreEdgeDevtoolsPreview] en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="c97ba-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="c97ba-106">Para más información sobre las características más recientes, consulte [DevTools en la última actualización de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="c97ba-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="c97ba-107">Herramientas básicas</span><span class="sxs-lookup"><span data-stu-id="c97ba-107">Core tools</span></span>  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   <span data-ttu-id="c97ba-109">Microsoft Edge (EdgeHTML) DevTools</span><span class="sxs-lookup"><span data-stu-id="c97ba-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="c97ba-110">Microsoft Edge \(EdgeHTML\) DevTools incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c97ba-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="c97ba-111">Un [panel de elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML y CSS, inspeccionar propiedades de accesibilidad, visualizar escuchas de eventos y definir puntos de interrupción de mutación de DOM</span><span class="sxs-lookup"><span data-stu-id="c97ba-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="c97ba-112">Una [consola][DevtoolsGuideEdgehtml|::ref3::|] para ver y filtrar los mensajes de registro, inspeccionar objetos de JavaScript y nodos de DOM y ejecutar JavaScript en el contexto de la ventana o marco seleccionados</span><span class="sxs-lookup"><span data-stu-id="c97ba-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="c97ba-113">Un [depurador][DevtoolsGuideEdgehtml|::ref4::|] para revisar código, establecer inspecciones y puntos de interrupción, editar en vivo su código y revisar el almacenamiento web y las cachés de cookies</span><span class="sxs-lookup"><span data-stu-id="c97ba-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="c97ba-114">Un panel de [red][DevtoolsGuideEdgehtml|::ref5::|] para supervisar e inspeccionar las solicitudes y respuestas de la red y de la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="c97ba-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="c97ba-115">Un panel de [rendimiento][DevtoolsGuideEdgehtml|::ref6::|] para generar perfiles de tiempo y de los recursos del sistema necesarios para su sitio</span><span class="sxs-lookup"><span data-stu-id="c97ba-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="c97ba-116">Un panel de [memoria][DevtoolsGuideEdgehtml|::ref7::|] para medir su uso de los recursos de memoria y comparar instantáneas de pila en diferentes estados del tiempo de ejecución de código.</span><span class="sxs-lookup"><span data-stu-id="c97ba-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="c97ba-117">Un panel de [almacenamiento][DevtoolsGuideEdgehtml|::ref8::|] para inspeccionar y administrar su almacenamiento web, IndexedDB, cookies y datos de caché</span><span class="sxs-lookup"><span data-stu-id="c97ba-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="c97ba-118">Un panel de [trabajos de servicio][DevtoolsGuideEdgehtmlServiceworkers] para administrar y depurar sus trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="c97ba-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="c97ba-119">Un panel de [emulación][DevtoolsGuideEdgehtml|::ref9::|] para probar su sitio con diferentes perfiles de explorador, resoluciones de pantalla y coordenadas de ubicación GPS</span><span class="sxs-lookup"><span data-stu-id="c97ba-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="c97ba-120">No dude en seguir enviando su [opinión y comentarios y en solicitar características](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="c97ba-120">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>  

> [!TIP]
> <span data-ttu-id="c97ba-121">[Puede probarlo en Microsoft Edge \(EdgeHTML\) desde cualquier explorador de manera gratuita][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="c97ba-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="c97ba-122">El equipo de Microsoft Edge se asoció con [BrowserStack][BrowserstackEdgehtml] para ofrecer pruebas gratuitas en tiempo real y automatizadas en Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="c97ba-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="c97ba-123">Aplicación de la Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="c97ba-123">Microsoft Store app</span></span>  

<span data-ttu-id="c97ba-124">**Microsoft Edge \(EdgeHTML\) DevTools** se encuentra [disponible][DevtoolsGuideEdgehtmlWhatsnew] como una [aplicación independiente de Windows 10 de Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview] y se añade a la experiencia de herramientas en el explorador \(`F12`\).</span><span class="sxs-lookup"><span data-stu-id="c97ba-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="c97ba-125">Con la versión de la tienda incluye un panel **selector** que permite adjuntar a destinos de página remotos y locales abiertos, así como un diseño con fichas para facilitar el cambio entre instancias de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c97ba-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="c97ba-126">Depuración local</span><span class="sxs-lookup"><span data-stu-id="c97ba-126">Local debugging</span></span>  

<span data-ttu-id="c97ba-127">Para depurar una página a nivel local, inicie la aplicación Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c97ba-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="c97ba-128">El panel **local** del selector muestra todos los procesos de contenido de EdgeHTML activos, incluidas las pestañas abiertas del explorador Edge, PWA en ejecución \( procesos\) y los controles de [WebView][HostingWebview].</span><span class="sxs-lookup"><span data-stu-id="c97ba-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="c97ba-129">Seleccione el destino que desee adjuntar y abra una instancia de nueva pestaña de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c97ba-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source=".//media/chooser_local.png" alt-text="Panel local de la aplicación DevTools":::
   <span data-ttu-id="c97ba-131">Panel local de la aplicación DevTools</span><span class="sxs-lookup"><span data-stu-id="c97ba-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="c97ba-132">Depuración remota</span><span class="sxs-lookup"><span data-stu-id="c97ba-132">Remote debugging</span></span>  

<span data-ttu-id="c97ba-133">La aplicación Microsoft Edge DevTools introduce la compatibilidad básica para la depuración de páginas en un equipo remoto mediante nuestro [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex] publicado recientemente.</span><span class="sxs-lookup"><span data-stu-id="c97ba-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="c97ba-134">Con la versión más reciente, se obtiene acceso remoto a la funcionalidad principal del depurador, elementos \ (para operaciones de solo lectura\) y paneles de [consola][DevtoolsGuideEdgehtml|::ref12::|].</span><span class="sxs-lookup"><span data-stu-id="c97ba-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="c97ba-135">La depuración remota está limitada a hosts de escritorio en ejecución de Microsoft Edge \ (EdgeHTML\) y es compatible con otros hosts EdgeHTML y dispositivos Windows 10 que disponibles en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="c97ba-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="c97ba-136">Para empezar, consulte la sección Microsoft Edge DevTools de los documentos del [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="c97ba-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./media/chooser_remote.png" alt-text="Panel remoto de la aplicación DevTools":::
   <span data-ttu-id="c97ba-138">Panel remoto de la aplicación DevTools</span><span class="sxs-lookup"><span data-stu-id="c97ba-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="c97ba-139">Accesos directos generales</span><span class="sxs-lookup"><span data-stu-id="c97ba-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c97ba-140">Todos los accesos directos han sido comprobados en la versión más reciente de Windows.</span><span class="sxs-lookup"><span data-stu-id="c97ba-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="c97ba-141">Si no puede usar un acceso directo, debe actualizar su copia de Windows.</span><span class="sxs-lookup"><span data-stu-id="c97ba-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="c97ba-142">Estos accesos directos controlan la ventana principal de DevTools y deberían funcionar en todas las herramientas.</span><span class="sxs-lookup"><span data-stu-id="c97ba-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="c97ba-143">Acción</span><span class="sxs-lookup"><span data-stu-id="c97ba-143">Action</span></span> | <span data-ttu-id="c97ba-144">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="c97ba-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c97ba-145">Mostrar u ocultar DevTools \(se abre en el último panel visualizado\)</span><span class="sxs-lookup"><span data-stu-id="c97ba-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="c97ba-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="c97ba-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="c97ba-147">Activar o desactivar el acoplamiento \(desacoplar/inferior/derecho\)</span><span class="sxs-lookup"><span data-stu-id="c97ba-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="c97ba-148">Abrir archivo</span><span class="sxs-lookup"><span data-stu-id="c97ba-148">Open file</span></span> | `Ctrl`<span data-ttu-id="c97ba-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="c97ba-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="c97ba-150">Mostrar en el depurador el código fuente HTML no modificable</span><span class="sxs-lookup"><span data-stu-id="c97ba-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="c97ba-151">Mostrar u ocultar consola en la parte inferior de cualquier otra herramienta</span><span class="sxs-lookup"><span data-stu-id="c97ba-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="c97ba-152">Cambiar a elementos \(explorador DOM\)</span><span class="sxs-lookup"><span data-stu-id="c97ba-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="c97ba-153">Cambiar a consola</span><span class="sxs-lookup"><span data-stu-id="c97ba-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="c97ba-154">Cambiar a depurador</span><span class="sxs-lookup"><span data-stu-id="c97ba-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="c97ba-155">Cambiar a red</span><span class="sxs-lookup"><span data-stu-id="c97ba-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="c97ba-156">Cambiar a rendimiento</span><span class="sxs-lookup"><span data-stu-id="c97ba-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="c97ba-157">Cambiar a memoria</span><span class="sxs-lookup"><span data-stu-id="c97ba-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="c97ba-158">Cambiar a emulación</span><span class="sxs-lookup"><span data-stu-id="c97ba-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="c97ba-159">Documento de ayuda</span><span class="sxs-lookup"><span data-stu-id="c97ba-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="c97ba-160">Siguiente herramienta</span><span class="sxs-lookup"><span data-stu-id="c97ba-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="c97ba-161">Herramienta anterior</span><span class="sxs-lookup"><span data-stu-id="c97ba-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="c97ba-162">Herramienta anterior \(desde historial\)</span><span class="sxs-lookup"><span data-stu-id="c97ba-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="c97ba-163">Siguiente herramienta \(desde historial\)</span><span class="sxs-lookup"><span data-stu-id="c97ba-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="c97ba-164">Submarco siguiente</span><span class="sxs-lookup"><span data-stu-id="c97ba-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="c97ba-165">Submarco anterior</span><span class="sxs-lookup"><span data-stu-id="c97ba-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="c97ba-166">Siguiente coincidencia en el cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="c97ba-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="c97ba-167">Coincidencia anterior en el cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="c97ba-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="c97ba-168">Buscar en el cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="c97ba-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="c97ba-169">Establecer el foco en la consola en la parte inferior</span><span class="sxs-lookup"><span data-stu-id="c97ba-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="c97ba-170">Iniciar DevTools en la consola</span><span class="sxs-lookup"><span data-stu-id="c97ba-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="c97ba-171">Actualizar la página.</span><span class="sxs-lookup"><span data-stu-id="c97ba-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="c97ba-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="c97ba-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="c97ba-173">Si pausa la depuración en un punto de ruptura, la acción **Actualizar página** reanuda en primer lugar el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c97ba-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="c97ba-174">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c97ba-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="c97ba-175">Envíenos sus comentarios para ayudar a mejorar Microsoft Edge \(EdgeHTML\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="c97ba-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="c97ba-176">Para ello, solo tiene que abrir las herramientas \(`F12`\) y seleccionar el botón [Enviar comentarios](#microsoft-edge-edgehtml-developer-tools).</span><span class="sxs-lookup"><span data-stu-id="c97ba-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="c97ba-177">Únase a[Windows Insider][WindowsInsiderProgram] para obtener una vista previa de las [últimas características de DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="c97ba-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="c97ba-178">Puede utilizar la aplicación del Centro de opiniones sobre Windows para publicar y votar sugerencias y problemas generales de Windows, realizar seguimientos de los mismos y obtener soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="c97ba-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Consola"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulación"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Memoria"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Red"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Rendimiento"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Trabajos de servicio"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Almacenamiento"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools en la última actualización de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo de Microsoft Edge (EdgeHTML) DevTools"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Vista previa de Microsoft Edge DevTools - Clientes de protocolo de DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicaciones de Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicaciones web progresivas (EdgeHTML) en Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Vista previa de Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Pruebas gratuitas de explorador de Microsoft Edge | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
