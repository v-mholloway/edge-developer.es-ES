---
description: Una referencia completa sobre todas las características y el comportamiento relacionados con la interfaz de usuario de la consola en Microsoft Edge DevTools.
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125261"
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

# <span data-ttu-id="eef9b-104">Referencia de consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-104">Console Reference</span></span>  

<span data-ttu-id="eef9b-105">Esta página es una referencia de las características relacionadas con la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="eef9b-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="eef9b-106">Se da por supuesto que ya está familiarizado con el uso de la consola para ver mensajes registrados y ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eef9b-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="eef9b-107">Si no es así, navegue para empezar [con la ejecución de JavaScript en la consola][DevToolsConsoleJavascript] y empiece a usar [los mensajes de registro en la consola][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="eef9b-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="eef9b-108">Si busca la referencia de la API en funciones como `console.log()` vea la [referencia de API de consola][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="eef9b-108">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="eef9b-109">Para consultar la referencia de funciones como `monitorEvents()` , vaya a referencia de la [API de utilidades de consola][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="eef9b-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="eef9b-110">Abrir la consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-110">Open the Console</span></span>  

<span data-ttu-id="eef9b-111">Puede abrir la consola como un [Panel](#open-the-console-panel) o como una [pestaña en el cajón](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="eef9b-111">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="eef9b-112">Abrir el panel de consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-112">Open the Console panel</span></span>  

<span data-ttu-id="eef9b-113">Seleccione `Control` + `Shift` + `J` \ (Windows, Linux \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="eef9b-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Panel de consola" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="eef9b-115">Panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="eef9b-115">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="eef9b-116">Para abrir el panel de consola desde el [menú de comandos][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **Panel** al lado.</span><span class="sxs-lookup"><span data-stu-id="eef9b-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Panel de consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="eef9b-118">Comando para mostrar el panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="eef9b-118">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="eef9b-119">Abrir la pestaña consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="eef9b-119">Open the Console tab in the Drawer</span></span>  

<span data-ttu-id="eef9b-120">Seleccione `Escape` o elija **personalizar y control DevTools** \ ( `...` \) y, a continuación, elija **Mostrar el cajón de consola**.</span><span class="sxs-lookup"><span data-stu-id="eef9b-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Panel de consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="eef9b-122">Mostrar cajón de consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="eef9b-123">El cajón aparece en la parte inferior de la ventana de DevTools, con la pestaña **consola** abierto.</span><span class="sxs-lookup"><span data-stu-id="eef9b-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Panel de consola" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="eef9b-125">Ficha de **consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="eef9b-125">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="eef9b-126">Para abrir la pestaña consola desde el [menú comando][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **alimentador** al lado.</span><span class="sxs-lookup"><span data-stu-id="eef9b-126">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Panel de consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="eef9b-128">Comando para mostrar la ficha de **consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="eef9b-128">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="eef9b-129">Abrir configuración de consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-129">Open Console Settings</span></span>  

<span data-ttu-id="eef9b-130">Elija **configuración de consola** \ ( ![ icono configuración de consola ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="eef9b-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Panel de consola" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="eef9b-132">Configuración de la consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="eef9b-133">Los vínculos siguientes explican cada configuración:</span><span class="sxs-lookup"><span data-stu-id="eef9b-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="eef9b-134">Ocultar red</span><span class="sxs-lookup"><span data-stu-id="eef9b-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="eef9b-135">Conservar registro</span><span class="sxs-lookup"><span data-stu-id="eef9b-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="eef9b-136">Solo el contexto seleccionado</span><span class="sxs-lookup"><span data-stu-id="eef9b-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="eef9b-137">Grupo similar</span><span class="sxs-lookup"><span data-stu-id="eef9b-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="eef9b-138">Registro XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="eef9b-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="eef9b-139">Evaluación diligente</span><span class="sxs-lookup"><span data-stu-id="eef9b-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="eef9b-140">Autocompletar desde historial</span><span class="sxs-lookup"><span data-stu-id="eef9b-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="eef9b-141">Abrir la barra lateral de la consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="eef9b-142">Elija **Mostrar la barra** lateral de consola \ ( ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] de consola \) para mostrar la barra lateral, que es útil para filtrar.</span><span class="sxs-lookup"><span data-stu-id="eef9b-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Panel de consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="eef9b-144">**Consola** Laterales</span><span class="sxs-lookup"><span data-stu-id="eef9b-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="eef9b-145">Ver mensajes</span><span class="sxs-lookup"><span data-stu-id="eef9b-145">View messages</span></span>  

<span data-ttu-id="eef9b-146">Esta sección contiene características que cambian la presentación de los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="eef9b-147">Vea [Ver mensajes][DevToolsConsoleViewMessages] para obtener un tutorial práctico.</span><span class="sxs-lookup"><span data-stu-id="eef9b-147">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="eef9b-148">Deshabilitar la agrupación de mensajes</span><span class="sxs-lookup"><span data-stu-id="eef9b-148">Disable message grouping</span></span>  

<span data-ttu-id="eef9b-149">[Abra configuración de consola](#open-console-settings) y deshabilite **grupo similar** para deshabilitar el comportamiento predeterminado de agrupación de mensajes de la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="eef9b-150">Para obtener un ejemplo [, consulta log XHR y solicitudes fetch](#log-xhr-and-fetch-requests) .</span><span class="sxs-lookup"><span data-stu-id="eef9b-150">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="eef9b-151">Registrar solicitudes de XHR y fetch</span><span class="sxs-lookup"><span data-stu-id="eef9b-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="eef9b-152">[Abra configuración de consola](#open-console-settings) y habilite **log XMLHttpRequests** para registrar todas las `XMLHttpRequest` solicitudes de `Fetch` la consola a medida que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="eef9b-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Panel de consola" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="eef9b-154">Registro `XMLHttpRequest` y `Fetch` solicitudes</span><span class="sxs-lookup"><span data-stu-id="eef9b-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="eef9b-155">En el mensaje superior de la figura anterior se muestra el comportamiento de agrupación predeterminado de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="eef9b-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Panel de consola" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="eef9b-156">Conservar mensajes en la carga de la página</span><span class="sxs-lookup"><span data-stu-id="eef9b-156">Persist messages across page loads</span></span>  

<span data-ttu-id="eef9b-157">De forma predeterminada, la consola se desactiva cada vez que se carga una página nueva.</span><span class="sxs-lookup"><span data-stu-id="eef9b-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="eef9b-158">Para conservar los mensajes en la carga de la página, [abra configuración de consola](#open-console-settings) y active la casilla **conservar registro** .</span><span class="sxs-lookup"><span data-stu-id="eef9b-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="eef9b-159">Ocultar mensajes de red</span><span class="sxs-lookup"><span data-stu-id="eef9b-159">Hide network messages</span></span>  

<span data-ttu-id="eef9b-160">De forma predeterminada, el explorador registra los mensajes de red en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="eef9b-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="eef9b-161">En la siguiente ilustración, el mensaje seleccionado representa un código de Estado HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="eef9b-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Panel de consola" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="eef9b-163">Un `429` mensaje en la **consola**</span><span class="sxs-lookup"><span data-stu-id="eef9b-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="eef9b-164">Para ocultar mensajes de red:</span><span class="sxs-lookup"><span data-stu-id="eef9b-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="eef9b-165">[Abra configuración de consola](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="eef9b-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="eef9b-166">Active la casilla **ocultar red** .</span><span class="sxs-lookup"><span data-stu-id="eef9b-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="eef9b-167">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="eef9b-167">Filter messages</span></span>  

<span data-ttu-id="eef9b-168">Existen muchas maneras de filtrar los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-168">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="eef9b-169">Filtrar los mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="eef9b-169">Filter out browser messages</span></span>  

<span data-ttu-id="eef9b-170">[Abra la barra lateral](#open-the-console-sidebar) de la consola y elija **mensajes de usuario** para mostrar solo los mensajes que proceden del JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="eef9b-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Panel de consola" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="eef9b-172">Ver mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="eef9b-172">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="eef9b-173">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="eef9b-173">Filter by log level</span></span>  

<span data-ttu-id="eef9b-174">DevTools asigna cada `console.*` método a nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="eef9b-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="eef9b-175">Hay 4 niveles: `Verbose` ,, `Info` `Warning` y `Error` .</span><span class="sxs-lookup"><span data-stu-id="eef9b-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="eef9b-176">Por ejemplo, `console.log()` se encuentra en el `Info` grupo, mientras que `console.error()` se encuentra en el `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="eef9b-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="eef9b-177">La [referencia][DevToolsConsoleApi] de la API de consola describe el nivel de gravedad de cada método aplicable.</span><span class="sxs-lookup"><span data-stu-id="eef9b-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="eef9b-178">Cada mensaje que el explorador registra en la consola también tiene un nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="eef9b-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="eef9b-179">Puede ocultar cualquier nivel de mensajes que no le interese.</span><span class="sxs-lookup"><span data-stu-id="eef9b-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="eef9b-180">Por ejemplo, si solo le interesan `Error` los mensajes, puede ocultar los otros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="eef9b-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="eef9b-181">Haga clic en el menú desplegable **niveles de registro** para habilitar o deshabilitar `Verbose` , `Info` `Warning` o `Error` mensajes.</span><span class="sxs-lookup"><span data-stu-id="eef9b-181">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Panel de consola" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="eef9b-183">Lista desplegable de **niveles de registro**</span><span class="sxs-lookup"><span data-stu-id="eef9b-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="eef9b-184">También puede filtrar por nivel de registro si [abre la barra lateral de la consola](#open-the-console-sidebar) y hace clic en **errores**, **advertencias**, **información**o **detallado**.</span><span class="sxs-lookup"><span data-stu-id="eef9b-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Panel de consola" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="eef9b-186">Usar la barra lateral para ver las advertencias</span><span class="sxs-lookup"><span data-stu-id="eef9b-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="eef9b-187">Filtrar mensajes por dirección URL</span><span class="sxs-lookup"><span data-stu-id="eef9b-187">Filter messages by URL</span></span>  

<span data-ttu-id="eef9b-188">Escriba `url:` seguido de una dirección URL para ver solo los mensajes que proceden de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="eef9b-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="eef9b-189">Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.</span><span class="sxs-lookup"><span data-stu-id="eef9b-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="eef9b-190">Los dominios también funcionan.</span><span class="sxs-lookup"><span data-stu-id="eef9b-190">Domains also work.</span></span>  <span data-ttu-id="eef9b-191">Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, `url:https://example.com` le permite centrarse en los mensajes de estas dos secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="eef9b-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Panel de consola" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="eef9b-193">Un filtro de URL</span><span class="sxs-lookup"><span data-stu-id="eef9b-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="eef9b-194">Escriba `-url:` para ocultar mensajes de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="eef9b-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="eef9b-195">Esto se conoce como un filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="eef9b-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Panel de consola" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="eef9b-197">Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL</span><span class="sxs-lookup"><span data-stu-id="eef9b-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="eef9b-198">También puede mostrar los mensajes de una sola dirección URL [abriendo la barra lateral](#open-the-console-sidebar)de la consola, expandiendo la sección de **mensajes de usuario** y, a continuación, haciendo clic en la dirección URL de la secuencia de comandos que contiene los mensajes en los que desea concentrarse.</span><span class="sxs-lookup"><span data-stu-id="eef9b-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Panel de consola" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="eef9b-200">Ver los mensajes procedentes de</span><span class="sxs-lookup"><span data-stu-id="eef9b-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="eef9b-201">Filtrar mensajes de distintos contextos</span><span class="sxs-lookup"><span data-stu-id="eef9b-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="eef9b-202">Supongamos que tiene un anuncio \ (ad \) en la página.</span><span class="sxs-lookup"><span data-stu-id="eef9b-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="eef9b-203">El anuncio está insertado en una `<iframe>` y está generando un gran número de mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="eef9b-204">Como AD se está ejecutando en un [contexto de JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es [abrir la configuración de consola](#open-console-settings) y habilitar la casilla de verificación de solo el **contexto seleccionado** .</span><span class="sxs-lookup"><span data-stu-id="eef9b-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="eef9b-205">Filtrar mensajes que no coincidan con un modelo de expresión regular</span><span class="sxs-lookup"><span data-stu-id="eef9b-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="eef9b-206">Escriba una expresión regular, como `/[gm][ta][mi]/` en el cuadro de texto **filtro** , para filtrar los mensajes que no coincidan con ese patrón.</span><span class="sxs-lookup"><span data-stu-id="eef9b-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="eef9b-207">DevTools comprueba si el patrón se encuentra en el texto del mensaje o en la secuencia de comandos que ha provocado el registro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="eef9b-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Panel de consola" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="eef9b-209">Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión Regex</span><span class="sxs-lookup"><span data-stu-id="eef9b-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="eef9b-210">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="eef9b-210">Run JavaScript</span></span>  

<span data-ttu-id="eef9b-211">Esta sección contiene características relacionadas con la ejecución de JavaScript en la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="eef9b-212">Consulte [ejecutar JavaScript][DevToolsConsoleOverviewJavascript] para obtener un tutorial práctico.</span><span class="sxs-lookup"><span data-stu-id="eef9b-212">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="eef9b-213">Volver a ejecutar expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="eef9b-213">Re-run expressions from history</span></span>  

<span data-ttu-id="eef9b-214">Presione la `Up Arrow` tecla para recorrer el historial de expresiones de JavaScript que ejecutó anteriormente en la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-214">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="eef9b-215">Seleccione `Enter` para volver a ejecutar la expresión.</span><span class="sxs-lookup"><span data-stu-id="eef9b-215">Select `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="eef9b-216">Ver el valor de una expresión en tiempo real con expresiones en directo</span><span class="sxs-lookup"><span data-stu-id="eef9b-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="eef9b-217">Si se encuentra escribiendo la misma expresión de JavaScript en la consola varias veces, es posible que le resulte más fácil crear una **expresión en vivo**.</span><span class="sxs-lookup"><span data-stu-id="eef9b-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="eef9b-218">Con **expresiones en vivo** , escriba una expresión una vez y, a continuación, ancle en la parte superior de la consola.</span><span class="sxs-lookup"><span data-stu-id="eef9b-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="eef9b-219">El valor de la expresión se actualiza casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="eef9b-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="eef9b-220">Vea [inspeccionar valores de expresiones de JavaScript en Real-Time con expresiones en directo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="eef9b-220">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="eef9b-221">Deshabilitar evaluación diligente</span><span class="sxs-lookup"><span data-stu-id="eef9b-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="eef9b-222">Mientras escribe las expresiones de JavaScript en la consola, **evaluación diligente** muestra una vista previa del valor devuelto para esa expresión.</span><span class="sxs-lookup"><span data-stu-id="eef9b-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="eef9b-223">[Abra configuración de consola](#open-console-settings) y deshabilite la casilla **evaluación diligente** para desactivar las vistas previas de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="eef9b-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="eef9b-224">Deshabilitar Autocompletar desde historial</span><span class="sxs-lookup"><span data-stu-id="eef9b-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="eef9b-225">A medida que escribe una expresión, la ventana emergente de autocompletar de la consola muestra expresiones que ejecutó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="eef9b-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="eef9b-226">Estas expresiones van precedidas del `>` carácter.</span><span class="sxs-lookup"><span data-stu-id="eef9b-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="eef9b-227">[Abra configuración de consola](#open-console-settings) y deshabilite la casilla **Autocompletar del historial** para dejar de mostrar las expresiones de su historial.</span><span class="sxs-lookup"><span data-stu-id="eef9b-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="eef9b-228">En la siguiente ilustración, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se han evaluado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="eef9b-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Panel de consola" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="eef9b-230">El mensaje emergente de Autocompletar muestra expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="eef9b-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="eef9b-231">Seleccionar contexto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="eef9b-231">Select JavaScript context</span></span>  

<span data-ttu-id="eef9b-232">De forma predeterminada, la lista desplegable de **contexto de JavaScript** se establece en **Top**, que representa el [contexto de exploración][MDNBrowsingContext] del documento principal.</span><span class="sxs-lookup"><span data-stu-id="eef9b-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Panel de consola" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="eef9b-234">Lista desplegable de **contexto de JavaScript**</span><span class="sxs-lookup"><span data-stu-id="eef9b-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="eef9b-235">Supongamos que tiene un anuncio en la página insertado en una `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="eef9b-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="eef9b-236">Para poder ajustar el DOM del anuncio, deseas ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eef9b-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="eef9b-237">En primer lugar, debe seleccionar el contexto de exploración del anuncio en la lista desplegable de **contexto de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="eef9b-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Panel de consola" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="eef9b-239">Seleccionar un contexto de JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="eef9b-239">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="eef9b-240">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="eef9b-240">Clear the Console</span></span>  

<span data-ttu-id="eef9b-241">Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:</span><span class="sxs-lookup"><span data-stu-id="eef9b-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="eef9b-242">Elija **Borrar consola** \ ( ![ Borrar consola ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="eef9b-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="eef9b-243">Haga clic con el botón derecho en un mensaje y, a continuación, seleccione **Borrar consola**.</span><span class="sxs-lookup"><span data-stu-id="eef9b-243">Right-click a message and then choose **Clear Console**.</span></span>  
*   <span data-ttu-id="eef9b-244">Escriba `clear()` en la consola y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="eef9b-244">Enter `clear()` in the Console and then select `Enter`.</span></span>  
*   <span data-ttu-id="eef9b-245">Ejecutar `console.clear()` desde el JavaScript de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="eef9b-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="eef9b-246">Seleccione `Control` + `L` mientras la consola está en el foco.</span><span class="sxs-lookup"><span data-stu-id="eef9b-246">Select `Control`+`L` while the Console is in focus.</span></span>  
    
## <span data-ttu-id="eef9b-247">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eef9b-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Ver mensajes registrados-Descripción general de la consola | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de la API de consola | Microsoft docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ejecución de JavaScript-Descripción general de la consola | Microsoft docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo | Microsoft docs"  
[DevToolsConsoleLog]: ./log.md "Introducción a la creación de mensajes de registro en la consola | Microsoft docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referencia de API de utilidades de consola | Microsoft docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> <span data-ttu-id="eef9b-257">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eef9b-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="eef9b-258">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="eef9b-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="eef9b-260">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eef9b-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
