---
description: Características agregadas a Microsoft Edge DevTools en Windows 10 Fall Creators Update (EdgeHTML 16)
title: DevTools en EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, edgehtml 16
ms.custom: seodec18
ms.openlocfilehash: 78ede81e022cc8f0f623ecd33fd2303314ec9cb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573773"
---
# <span data-ttu-id="6211a-104">DevTools en Windows 10 Fall Creators Update (EdgeHTML 16)</span><span class="sxs-lookup"><span data-stu-id="6211a-104">DevTools in the Windows 10 Fall Creators Update (EdgeHTML 16)</span></span>

<span data-ttu-id="6211a-105">Con esta versión comenzamos un esfuerzo importante de refactorización de DevTools para mejorar la solidez y el rendimiento, además de agregar un conjunto de nuevas características que puede comenzar a usar hoy.</span><span class="sxs-lookup"><span data-stu-id="6211a-105">With this release we started a major DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today!</span></span> 

<span data-ttu-id="6211a-106">Estas son las características de Microsoft Edge DevTools que se incluían en [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span><span class="sxs-lookup"><span data-stu-id="6211a-106">Here are the Microsoft Edge DevTools features that shipped with the [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span></span>

## <span data-ttu-id="6211a-107">Escuchas de eventos antecesores</span><span class="sxs-lookup"><span data-stu-id="6211a-107">Ancestor event listeners</span></span> 

<span data-ttu-id="6211a-108">El panel **eventos** ahora agrega la opción de ver las escuchas de eventos registradas en cualquier antecesor del elemento seleccionado actualmente (en el panel **elementos** ), además de las del propio elemento.</span><span class="sxs-lookup"><span data-stu-id="6211a-108">The **Events** pane now adds the option to view event listeners registered on any ancestor of the currently selected element (in the **Elements** panel), in addition to those on the element itself.</span></span> <span data-ttu-id="6211a-109">Además, ahora puede agrupar la escucha de eventos en un *evento* o *elemento*.</span><span class="sxs-lookup"><span data-stu-id="6211a-109">Additionally, you can now group the event listener display by either *Event* or *Element*.</span></span> 

![Panel inspección de detector de eventos](../media/elements_ancestor_events.png)

## <span data-ttu-id="6211a-111">Puntos de interrupción de mutación DOM</span><span class="sxs-lookup"><span data-stu-id="6211a-111">DOM mutation breakpoints</span></span>

<span data-ttu-id="6211a-112">Ahora puede establecer puntos de interrupción de mutación de DOM para que se interrumpan en el depurador cada vez que cambie un nodo de elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="6211a-112">You can now set DOM mutation breakpoints to break into the Debugger whenever a selected element node changes.</span></span> <span data-ttu-id="6211a-113">Desde el panel **elementos** , RT: haga clic en cualquier elemento de la vista de árbol DOM y seleccione una o varias de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="6211a-113">From the **Elements** panel, rt-click on any element in the DOM tree view and select one or more of the following:</span></span>

 - <span data-ttu-id="6211a-114">Interrupción en el nodo quitada</span><span class="sxs-lookup"><span data-stu-id="6211a-114">Break on Node removed</span></span>
 - <span data-ttu-id="6211a-115">Interrupción en subárbol modificada</span><span class="sxs-lookup"><span data-stu-id="6211a-115">Break on Subtree modified</span></span>
 - <span data-ttu-id="6211a-116">Interrupción en el atributo modificado</span><span class="sxs-lookup"><span data-stu-id="6211a-116">Break on Attribute modified</span></span>

<span data-ttu-id="6211a-117">Puede administrar los puntos de interrupción de mutación desde el panel de **puntos de interrupción Dom** en los paneles **elementos** o **depuración** .</span><span class="sxs-lookup"><span data-stu-id="6211a-117">You can manage your mutation breakpoints from the **DOM breakpoints** pane in the **Elements** or **Debugger** panels.</span></span>

![Panel de puntos de interrupción DOM](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="6211a-119">Compatibilidad con reglas en CSS</span><span class="sxs-lookup"><span data-stu-id="6211a-119">CSS at-rule support</span></span>

<span data-ttu-id="6211a-120">Las reglas de CSS "en" (@) ahora se representan entre otras declaraciones de regla CSS en el panel **estilos** , incluidas `@keyframes` las reglas de animación (actualmente limitadas a solo lectura), `@supports` consultas de características y `@media` consultas.</span><span class="sxs-lookup"><span data-stu-id="6211a-120">CSS "at" (@) rules are now represented among other CSS rule declarations on the **Styles** pane, including animation `@keyframes` rules (currently limited to read-only), `@supports` feature queries, and `@media` queries.</span></span>

![Inspección de CSS en las reglas del panel estilo de DevTools](../media/elements_at_rules.png)

## <span data-ttu-id="6211a-122">Panel fuentes CSS</span><span class="sxs-lookup"><span data-stu-id="6211a-122">CSS fonts pane</span></span>

<span data-ttu-id="6211a-123">`@font-face`Las reglas CSS ahora tienen su propio panel **fuentes** dedicadas en el que se muestra dónde se carga la fuente (*local* o de *red*) y el número de caracteres que la usan.</span><span class="sxs-lookup"><span data-stu-id="6211a-123">CSS `@font-face` rules now have their own dedicated **Fonts** pane that displays where the font is loaded from (*Local* or *Network*) and how many characters are using it.</span></span> <span data-ttu-id="6211a-124">Si se carga una fuente desde la red, DevTools mostrará la regla que la importó junto con su alias y tipo de fuente.</span><span class="sxs-lookup"><span data-stu-id="6211a-124">If a font is loaded from the network,  DevTools will display the rule that imported it along with its alias and font type.</span></span>

![Información de fuente CSS](../media/elements_fonts.png)

## <span data-ttu-id="6211a-126">Compatibilidad con los seudoelementos CSS</span><span class="sxs-lookup"><span data-stu-id="6211a-126">CSS pseudo-element support</span></span>

<span data-ttu-id="6211a-127">Ahora, el panel **estilos** agrupa los seudoelementos bajo sus propios títulos y ya no muestra su contenido como tachado.</span><span class="sxs-lookup"><span data-stu-id="6211a-127">The **Styles** pane now groups pseudo-elements under their own headings and no longer displays their content as crossed out.</span></span>

**<span data-ttu-id="6211a-128">Antes:</span><span class="sxs-lookup"><span data-stu-id="6211a-128">Before:</span></span>**
<br>
![El contenido generado estaba tachado anteriormente](../media/gc_before.png)

**<span data-ttu-id="6211a-130">Después:</span><span class="sxs-lookup"><span data-stu-id="6211a-130">After:</span></span>**
<br>
![El contenido generado ya no se muestra con tachado.](../media/gc_after.png)

## <span data-ttu-id="6211a-132">Mejoras en la consola</span><span class="sxs-lookup"><span data-stu-id="6211a-132">Console improvements</span></span>

<span data-ttu-id="6211a-133">El panel de **consola** ha reversión de la experiencia del usuario para mejorar la facilidad de uso y ofrece una experiencia de IntelliSense más rápida y eficaz.</span><span class="sxs-lookup"><span data-stu-id="6211a-133">The **Console** panel got a UX overhaul for improved usability and a faster, richer Intellisense experience.</span></span>

<span data-ttu-id="6211a-134">**Antes:** 
![ Consola anterior</span><span class="sxs-lookup"><span data-stu-id="6211a-134">**Before:**
![Previous console</span></span>](../media/console_old.png)

<span data-ttu-id="6211a-135">**Después de:** 
![ Nueva consola</span><span class="sxs-lookup"><span data-stu-id="6211a-135">**After:**
![New console</span></span>](../media/console_new.png)

<span data-ttu-id="6211a-136">También agregamos estas mejoras:</span><span class="sxs-lookup"><span data-stu-id="6211a-136">We also added these improvements:</span></span>

 -  <span data-ttu-id="6211a-137">`Shift + Enter`Se usa para agregar una línea adicional a un comando antes de ejecutarla `Enter` .</span><span class="sxs-lookup"><span data-stu-id="6211a-137">Use `Shift + Enter` to add an additional line to a command before executing it with `Enter`.</span></span> <span data-ttu-id="6211a-138">(Anteriormente había un cambio en el botón de alternancia de *modo multilínea o de línea única* ).</span><span class="sxs-lookup"><span data-stu-id="6211a-138">(Formerly there was a *Switch to multiline/single-line mode* toggle button.)</span></span>

 - <span data-ttu-id="6211a-139">Se admiten las siguientes API nuevas:</span><span class="sxs-lookup"><span data-stu-id="6211a-139">The following new APIs are supported:</span></span>
    - <span data-ttu-id="6211a-140">método [**Console. Table (***Object***)**](../console/console-api.md#organizing-log-output)</span><span class="sxs-lookup"><span data-stu-id="6211a-140">[**console.table(***object***)**](../console/console-api.md#organizing-log-output) method</span></span>
    - <span data-ttu-id="6211a-141">[**getEventListeners (***objeto***)**](../console/command-line.md#event-listeners) comando</span><span class="sxs-lookup"><span data-stu-id="6211a-141">[**getEventListeners(***object***)**](../console/command-line.md#event-listeners) command</span></span>
    - <span data-ttu-id="6211a-142">comando [**Keys (***objeto***)**](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="6211a-142">[**keys(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="6211a-143">comando [**valores (***objeto***)**](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="6211a-143">[**values(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="6211a-144">Selector de [**$x (***expresión XPath***)**](../console/command-line.md#dom-selectors)</span><span class="sxs-lookup"><span data-stu-id="6211a-144">[**$x(***xpath expression***)**](../console/command-line.md#dom-selectors) selector</span></span>

 - <span data-ttu-id="6211a-145">El parámetro de formato [**% c ()**](../console/console-api.md#logging-custom-messages) ahora es compatible</span><span class="sxs-lookup"><span data-stu-id="6211a-145">The [**%c()**](../console/console-api.md#logging-custom-messages) formatting parameter is now supported</span></span>

## <span data-ttu-id="6211a-146">Mejoras en la depuración</span><span class="sxs-lookup"><span data-stu-id="6211a-146">Debugging improvements</span></span>

<span data-ttu-id="6211a-147">Además de un conjunto de características nuevas para depurar los [trabajos de servicio y la caché de PWA](#progressive-web-app-debugging), el depurador agregó estas características:</span><span class="sxs-lookup"><span data-stu-id="6211a-147">In addition to a suite of new features for debugging your [PWA service workers and cache](#progressive-web-app-debugging), the Debugger added these features:</span></span>

### <span data-ttu-id="6211a-148">Depuración consolidada para recursos compartidos</span><span class="sxs-lookup"><span data-stu-id="6211a-148">Consolidated debugging for shared resources</span></span>

<span data-ttu-id="6211a-149">Incluso cuando se hace referencia varias veces a un recurso, como un archivo cargado desde CDN, en todo el código, DevTools le proporcionará una única instancia de depuración para ese archivo, donde podrá establecer puntos de interrupción comunes, que se alcanzarán sin importar dónde se hace referencia al archivo.</span><span class="sxs-lookup"><span data-stu-id="6211a-149">Even when a resource, such as a file loaded from CDN, is referenced multiple times throughout your code,  DevTools will now provide a single debugging instance for that file where you can then set common breakpoints which will be hit regardless of where that file is referenced.</span></span> <span data-ttu-id="6211a-150">(Anteriormente se consideró que cada referencia de script se asignaba a un conjunto separado de puntos de interrupción).</span><span class="sxs-lookup"><span data-stu-id="6211a-150">(Previously each script reference was considered a unique resource would map to a separate set of breakpoints.)</span></span>

### <span data-ttu-id="6211a-151">Editar en vivo de JavaScript con *la edición activada-inactiva*</span><span class="sxs-lookup"><span data-stu-id="6211a-151">Live edit JavaScript with *Edit-on-idle*</span></span>

<span data-ttu-id="6211a-152">Ahora puede editar su JavaScript en vivo durante una sesión de depuración.</span><span class="sxs-lookup"><span data-stu-id="6211a-152">You can now edit your JavaScript live during a debugging session.</span></span> <span data-ttu-id="6211a-153">Esta característica estaba disponible experimentalmente (detrás de una marca) en la versión [anterior](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) y ahora es una característica permanente.</span><span class="sxs-lookup"><span data-stu-id="6211a-153">This feature was experimentally available (behind a flag) in the [previous](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) release and now its a permanent feature.</span></span> <span data-ttu-id="6211a-154">Simplemente seleccione cualquier archivo de script en el panel **depuración** , edite, haga clic en **Guardar** (o `Ctrl+S` ) para probar los cambios la próxima vez que se ejecute esa sección de código.</span><span class="sxs-lookup"><span data-stu-id="6211a-154">Simply select any script file from the **Debugger** panel, edit, then click **Save** (or `Ctrl+S`) to test your changes next time that section of code runs.</span></span> 

![El depurador le permite modificar el script en vivo y comparar los cambios](../media/debugger_edit_buttons.png) 

<span data-ttu-id="6211a-156">Haga clic en el botón **comparar documento con el original** para ver las diferencias de los cambios que ha realizado.</span><span class="sxs-lookup"><span data-stu-id="6211a-156">Click the **Compare document to original** button to view the diff of what you changed.</span></span>

![Vista de diferencias del código editado en el depurador](../media/debugger_edit_code.png) 

<span data-ttu-id="6211a-158">Ten en cuenta las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="6211a-158">Please be aware of the following constraints:</span></span>

- <span data-ttu-id="6211a-159">La edición de script solo funciona en archivos *. js* externos (y no incrustados `<script>` en *. html*)</span><span class="sxs-lookup"><span data-stu-id="6211a-159">Script editing only works in external *.js* files (and not embedded `<script>` within *.html*)</span></span>
- <span data-ttu-id="6211a-160">Las modificaciones se guardan en memoria y se vacían al volver a cargar el documento, por lo que no podrá ejecutar modificaciones dentro de un `DOMContentLoaded` controlador, por ejemplo</span><span class="sxs-lookup"><span data-stu-id="6211a-160">Edits are saved in memory and flushed when the document is reloaded, thus you won’t be able to run edits inside a `DOMContentLoaded` handler, for example</span></span>
- <span data-ttu-id="6211a-161">Por el momento, no hay ninguna forma (como una opción **Guardar como** ) para guardar las modificaciones en el disco desde DevTools</span><span class="sxs-lookup"><span data-stu-id="6211a-161">Currently there’s no way (such as a **Save As** option) to save your edits to disk from  DevTools</span></span>

## <span data-ttu-id="6211a-162">Abreviados</span><span class="sxs-lookup"><span data-stu-id="6211a-162">Shortcuts</span></span>

<span data-ttu-id="6211a-163">Ahora puedes iniciar DevTools en el panel de la última `Ctrl+Shift+I` versión () o directamente en la consola ( `Ctrl+Shift+J` ) como lo harías en otros navegadores principales.</span><span class="sxs-lookup"><span data-stu-id="6211a-163">You can now launch DevTools to the last viewed panel (`Ctrl+Shift+I`) or directly to the Console (`Ctrl+Shift+J`) just like you would on other major browsers.</span></span>

## <span data-ttu-id="6211a-164">Depuración de aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="6211a-164">Progressive Web App debugging</span></span>

<span data-ttu-id="6211a-165">Pruebe el soporte experimental para las aplicaciones web progresivas (PWAs) en Microsoft Edge y DevTools seleccionando la opción **Habilitar trabajos de servicio** de `about:flags` (y reiniciando Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="6211a-165">Test out the experimental support for Progressive Web Apps (PWAs) in Microsoft Edge and  DevTools by selecting the **Enable service workers** option from `about:flags` (and restarting Microsoft Edge).</span></span> <span data-ttu-id="6211a-166">Si un sitio hace uso de **trabajadores del servicio** o de la API de **caché** , rellenará las entradas en el panel de **depuración** para cada origen, de forma similar a cómo funciona el almacenamiento web y la inspección de cookies.</span><span class="sxs-lookup"><span data-stu-id="6211a-166">If a site makes use of **Service Workers** and/or the **Cache** API,  will populate entries in the **Debugger** panel for each origin, similar to how web storage and cookie inspection work.</span></span>

<span data-ttu-id="6211a-167">Al hacer clic en una entrada de trabajador de servicio específica, se abrirá la **visión general**de los trabajadores del servicio, donde puede administrar el registro de trabajadores del servicio para el ámbito determinado y exigir una notificación de inserción de prueba.</span><span class="sxs-lookup"><span data-stu-id="6211a-167">Clicking on a specific service worker entry will open up the **Service Worker Overview**, where you can manage the service worker registration for the given scope and force a test push notification.</span></span> <span data-ttu-id="6211a-168">También puede **detener** / el**Inicio** de trabajos de servicio individuales e **inspeccionarlos** desde una ventana de depurador independiente:</span><span class="sxs-lookup"><span data-stu-id="6211a-168">You can also **Stop**/**Start** individual service workers and **Inspect** them from a separate debugger window:</span></span>

![Panel de información general del trabajo del servicio](../media/debugger_sw_overview.png)

<span data-ttu-id="6211a-170">Tenga en cuenta lo siguiente sobre la depuración de los trabajos de servicios:</span><span class="sxs-lookup"><span data-stu-id="6211a-170">Please note the following about service worker debugging:</span></span>

 - <span data-ttu-id="6211a-171">La depuración de un trabajador de servicio iniciará una nueva instancia de la DevTools independiente de las herramientas de la página porque los trabajos de servicio se pueden compartir entre varias pestañas.</span><span class="sxs-lookup"><span data-stu-id="6211a-171">Debugging a service worker will launch a new instance of the DevTools separate from the page's tools because service workers can be shared across multiple tabs.</span></span> 
 - <span data-ttu-id="6211a-172">Los [elementos](../elements.md) y los paneles de [emulación](../emulation.md) no están presentes en el depurador de trabajo de servicios, dado que los trabajadores del servicio se ejecutan en segundo plano y no controlan directamente el front-end de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6211a-172">The [Elements](../elements.md) and [Emulation](../emulation.md) panels are absent from the service worker debugger, given that service workers run in the background and do not directly control the front-end of your app.</span></span>
 - <span data-ttu-id="6211a-173">En este momento, el tráfico de red de un trabajador de servicio solo se notifica desde la instancia de depuración de DevTools para ese trabajo, y no desde la instancia central de la página.</span><span class="sxs-lookup"><span data-stu-id="6211a-173">Currently network traffic for a service worker is only reported from the DevTools debugging instance for that worker, and not from the central instance for the page itself.</span></span>

<span data-ttu-id="6211a-174">Al hacer clic en una entrada de caché específica, se abrirá el administrador de **caché** , donde puede inspeccionar y, opcionalmente, eliminar entradas de caché (pares clave/valor de*solicitud* y *respuesta* ).</span><span class="sxs-lookup"><span data-stu-id="6211a-174">Clicking on a specific cache entry will open up the **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs).</span></span>