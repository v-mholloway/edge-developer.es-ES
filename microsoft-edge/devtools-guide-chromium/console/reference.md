---
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 51a85c3dad121dcb42633390de9b4e817074546e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982522"
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





# <span data-ttu-id="d6521-103">Referencia de consola</span><span class="sxs-lookup"><span data-stu-id="d6521-103">Console Reference</span></span>   



<span data-ttu-id="d6521-104">Esta página es una referencia de las características relacionadas con la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6521-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="d6521-105">Se da por supuesto que ya está familiarizado con el uso de la consola para ver mensajes registrados y ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d6521-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="d6521-106">Si no es así, vea empezar [a ejecutar JavaScript en la consola][DevToolsConsoleJavascript] y empezar [a registrar mensajes en la consola][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="d6521-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="d6521-107">Si busca la referencia de la API en funciones como `console.log()` vea la [referencia de API de consola][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="d6521-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="d6521-108">Para obtener la referencia en funciones como `monitorEvents()` , consulte referencia de la [API de utilidades de consola][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="d6521-108">For the reference on functions like `monitorEvents()`, see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="d6521-109">Abrir la consola</span><span class="sxs-lookup"><span data-stu-id="d6521-109">Open the Console</span></span>   

<span data-ttu-id="d6521-110">Puede abrir la consola como un [Panel](#open-the-console-panel) o como una [pestaña en el cajón](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="d6521-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="d6521-111">Abrir el panel de consola</span><span class="sxs-lookup"><span data-stu-id="d6521-111">Open the Console panel</span></span>   

<span data-ttu-id="d6521-112">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="d6521-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Panel de consola" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="d6521-114">Panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="d6521-114">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="d6521-115">Para abrir el panel de consola desde el [menú de comandos][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **Panel** al lado.</span><span class="sxs-lookup"><span data-stu-id="d6521-115">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Comando para mostrar el panel de consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="d6521-117">Comando para mostrar el panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="d6521-117">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="d6521-118">Abrir la pestaña consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="d6521-118">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="d6521-119">Pulse `Escape` o haga clic en **personalizar y controlar DevTools** \ ( `...` \) y, a continuación, seleccione **Mostrar cajón de consola**.</span><span class="sxs-lookup"><span data-stu-id="d6521-119">Press `Escape` or click **Customize And Control DevTools** \(`...`\) and then select **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar cajón de consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="d6521-121">Mostrar cajón de consola</span><span class="sxs-lookup"><span data-stu-id="d6521-121">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="d6521-122">El cajón aparece en la parte inferior de la ventana de DevTools, con la pestaña **consola** abierto.</span><span class="sxs-lookup"><span data-stu-id="d6521-122">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Ficha de consola en el cajón" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="d6521-124">Ficha de **consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="d6521-124">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="d6521-125">Para abrir la pestaña consola desde el [menú comando][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **alimentador** al lado.</span><span class="sxs-lookup"><span data-stu-id="d6521-125">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Comando para mostrar la ficha de consola en el cajón" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="d6521-127">Comando para mostrar la ficha de **consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="d6521-127">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="d6521-128">Abrir configuración de consola</span><span class="sxs-lookup"><span data-stu-id="d6521-128">Open Console Settings</span></span>   

<span data-ttu-id="d6521-129">Haga clic en **configuración de consola** \ ( ![ configuración de consola ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d6521-129">Click **Console Settings** \(![Console Settings][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configuración de la consola" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="d6521-131">Configuración de la consola</span><span class="sxs-lookup"><span data-stu-id="d6521-131">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="d6521-132">Los vínculos siguientes explican cada configuración:</span><span class="sxs-lookup"><span data-stu-id="d6521-132">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="d6521-133">Ocultar red</span><span class="sxs-lookup"><span data-stu-id="d6521-133">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="d6521-134">Conservar registro</span><span class="sxs-lookup"><span data-stu-id="d6521-134">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="d6521-135">Solo el contexto seleccionado</span><span class="sxs-lookup"><span data-stu-id="d6521-135">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="d6521-136">Grupo similar</span><span class="sxs-lookup"><span data-stu-id="d6521-136">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="d6521-137">Registro XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="d6521-137">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="d6521-138">Evaluación diligente</span><span class="sxs-lookup"><span data-stu-id="d6521-138">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="d6521-139">Autocompletar desde historial</span><span class="sxs-lookup"><span data-stu-id="d6521-139">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="d6521-140">Abrir la barra lateral de la consola</span><span class="sxs-lookup"><span data-stu-id="d6521-140">Open the Console Sidebar</span></span>   

<span data-ttu-id="d6521-141">Haga clic en **Mostrar la barra** lateral de consola \ ( ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] de consola \) para mostrar la barra lateral, que es útil para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d6521-141">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral de la consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="d6521-143">**Consola** Laterales</span><span class="sxs-lookup"><span data-stu-id="d6521-143">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="d6521-144">Ver mensajes</span><span class="sxs-lookup"><span data-stu-id="d6521-144">View messages</span></span>   

<span data-ttu-id="d6521-145">Esta sección contiene características que cambian la presentación de los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-145">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="d6521-146">Vea [Ver mensajes][DevToolsConsoleViewMessages] para obtener un tutorial práctico.</span><span class="sxs-lookup"><span data-stu-id="d6521-146">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="d6521-147">Deshabilitar la agrupación de mensajes</span><span class="sxs-lookup"><span data-stu-id="d6521-147">Disable message grouping</span></span>   

<span data-ttu-id="d6521-148">[Abra configuración de consola](#open-console-settings) y deshabilite **grupo similar** para deshabilitar el comportamiento predeterminado de agrupación de mensajes de la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-148">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="d6521-149">Para obtener un ejemplo [, consulta log XHR y solicitudes fetch](#log-xhr-and-fetch-requests) .</span><span class="sxs-lookup"><span data-stu-id="d6521-149">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="d6521-150">Registrar solicitudes de XHR y fetch</span><span class="sxs-lookup"><span data-stu-id="d6521-150">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="d6521-151">[Abra configuración de consola](#open-console-settings) y habilite **log XMLHttpRequests** para registrar todas las `XMLHttpRequest` solicitudes de `Fetch` la consola a medida que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="d6521-151">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Registrar solicitudes de recuperación y recuperación" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="d6521-153">Registro `XMLHttpRequest` y `Fetch` solicitudes</span><span class="sxs-lookup"><span data-stu-id="d6521-153">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="d6521-154">En el mensaje superior de la figura anterior se muestra el comportamiento de agrupación predeterminado de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="d6521-154">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="d6521-155">Conservar mensajes en la carga de la página</span><span class="sxs-lookup"><span data-stu-id="d6521-155">Persist messages across page loads</span></span>   

<span data-ttu-id="d6521-156">De forma predeterminada, la consola se desactiva cada vez que se carga una página nueva.</span><span class="sxs-lookup"><span data-stu-id="d6521-156">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="d6521-157">Para conservar los mensajes en la carga de la página, [abra configuración de consola](#open-console-settings) y active la casilla **conservar registro** .</span><span class="sxs-lookup"><span data-stu-id="d6521-157">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="d6521-158">Ocultar mensajes de red</span><span class="sxs-lookup"><span data-stu-id="d6521-158">Hide network messages</span></span>   

<span data-ttu-id="d6521-159">De forma predeterminada, el explorador registra los mensajes de red en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="d6521-159">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="d6521-160">En la siguiente ilustración, el mensaje seleccionado representa un código de Estado HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="d6521-160">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un mensaje de 429 en la consola" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="d6521-162">Un `429` mensaje en la **consola**</span><span class="sxs-lookup"><span data-stu-id="d6521-162">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="d6521-163">Para ocultar mensajes de red:</span><span class="sxs-lookup"><span data-stu-id="d6521-163">To hide network messages:</span></span>  

1.  <span data-ttu-id="d6521-164">[Abra configuración de consola](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="d6521-164">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="d6521-165">Active la casilla **ocultar red** .</span><span class="sxs-lookup"><span data-stu-id="d6521-165">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="d6521-166">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="d6521-166">Filter messages</span></span>   

<span data-ttu-id="d6521-167">Existen muchas maneras de filtrar los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-167">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="d6521-168">Filtrar los mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="d6521-168">Filter out browser messages</span></span>   

<span data-ttu-id="d6521-169">[Abra la barra lateral](#open-the-console-sidebar) de la consola y haga clic en **mensajes de usuario** para mostrar solo los mensajes que proceden del JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="d6521-169">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Ver mensajes de usuario" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="d6521-171">Ver mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="d6521-171">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="d6521-172">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="d6521-172">Filter by log level</span></span>   

<span data-ttu-id="d6521-173">DevTools asigna cada `console.*` método a nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="d6521-173">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="d6521-174">Hay 4 niveles: `Verbose` ,, `Info` `Warning` y `Error` .</span><span class="sxs-lookup"><span data-stu-id="d6521-174">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="d6521-175">Por ejemplo, `console.log()` se encuentra en el `Info` grupo, mientras que `console.error()` se encuentra en el `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="d6521-175">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="d6521-176">La [referencia][DevToolsConsoleApi] de la API de consola describe el nivel de gravedad de cada método aplicable.</span><span class="sxs-lookup"><span data-stu-id="d6521-176">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="d6521-177">Cada mensaje que el explorador registra en la consola también tiene un nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="d6521-177">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="d6521-178">Puede ocultar cualquier nivel de mensajes que no le interese.</span><span class="sxs-lookup"><span data-stu-id="d6521-178">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="d6521-179">Por ejemplo, si solo le interesan `Error` los mensajes, puede ocultar los otros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="d6521-179">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="d6521-180">Haga clic en el menú desplegable **niveles de registro** para habilitar o deshabilitar `Verbose` , `Info` `Warning` o `Error` mensajes.</span><span class="sxs-lookup"><span data-stu-id="d6521-180">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Lista desplegable de niveles de registro" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="d6521-182">Lista desplegable de **niveles de registro**</span><span class="sxs-lookup"><span data-stu-id="d6521-182">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="d6521-183">También puede filtrar por nivel de registro si [abre la barra lateral de la consola](#open-the-console-sidebar) y hace clic en **errores**, **advertencias**, **información**o **detallado**.</span><span class="sxs-lookup"><span data-stu-id="d6521-183">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar la barra lateral para ver las advertencias" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="d6521-185">Usar la barra lateral para ver las advertencias</span><span class="sxs-lookup"><span data-stu-id="d6521-185">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="d6521-186">Filtrar mensajes por dirección URL</span><span class="sxs-lookup"><span data-stu-id="d6521-186">Filter messages by URL</span></span>   

<span data-ttu-id="d6521-187">Escriba `url:` seguido de una dirección URL para ver solo los mensajes que proceden de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d6521-187">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="d6521-188">Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.</span><span class="sxs-lookup"><span data-stu-id="d6521-188">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="d6521-189">Los dominios también funcionan.</span><span class="sxs-lookup"><span data-stu-id="d6521-189">Domains also work.</span></span>  <span data-ttu-id="d6521-190">Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, `url:https://example.com` le permite centrarse en los mensajes de estas dos secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="d6521-190">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtro de URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="d6521-192">Un filtro de URL</span><span class="sxs-lookup"><span data-stu-id="d6521-192">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="d6521-193">Escriba `-url:` para ocultar mensajes de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d6521-193">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="d6521-194">Esto se conoce como un filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="d6521-194">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la https://b.wal.co dirección URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="d6521-196">Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL</span><span class="sxs-lookup"><span data-stu-id="d6521-196">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="d6521-197">También puede mostrar los mensajes de una sola dirección URL [abriendo la barra lateral](#open-the-console-sidebar)de la consola, expandiendo la sección de **mensajes de usuario** y, a continuación, haciendo clic en la dirección URL de la secuencia de comandos que contiene los mensajes en los que desea concentrarse.</span><span class="sxs-lookup"><span data-stu-id="d6521-197">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Ver los mensajes que proceden de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="d6521-199">Ver los mensajes procedentes de</span><span class="sxs-lookup"><span data-stu-id="d6521-199">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="d6521-200">Filtrar mensajes de distintos contextos</span><span class="sxs-lookup"><span data-stu-id="d6521-200">Filter out messages from different contexts</span></span>   

<span data-ttu-id="d6521-201">Supongamos que tiene un anuncio \ (ad \) en la página.</span><span class="sxs-lookup"><span data-stu-id="d6521-201">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="d6521-202">El anuncio está insertado en una `<iframe>` y está generando un gran número de mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-202">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="d6521-203">Como AD se está ejecutando en un [contexto de JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es [abrir la configuración de consola](#open-console-settings) y habilitar la casilla de verificación de solo el **contexto seleccionado** .</span><span class="sxs-lookup"><span data-stu-id="d6521-203">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="d6521-204">Filtrar mensajes que no coincidan con un modelo de expresión regular</span><span class="sxs-lookup"><span data-stu-id="d6521-204">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="d6521-205">Escriba una expresión regular, como `/[gm][ta][mi]/` en el cuadro de texto **filtro** , para filtrar los mensajes que no coincidan con ese patrón.</span><span class="sxs-lookup"><span data-stu-id="d6521-205">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="d6521-206">DevTools comprueba si el patrón se encuentra en el texto del mensaje o en la secuencia de comandos que ha provocado el registro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d6521-206">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar los mensajes que no coincidan con la expresión Regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="d6521-208">Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión Regex</span><span class="sxs-lookup"><span data-stu-id="d6521-208">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="d6521-209">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6521-209">Run JavaScript</span></span>   

<span data-ttu-id="d6521-210">Esta sección contiene características relacionadas con la ejecución de JavaScript en la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-210">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="d6521-211">Consulte [ejecutar JavaScript][DevToolsConsoleOverviewJavascript] para obtener un tutorial práctico.</span><span class="sxs-lookup"><span data-stu-id="d6521-211">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="d6521-212">Volver a ejecutar expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="d6521-212">Re-run expressions from history</span></span>   

<span data-ttu-id="d6521-213">Presione la `Up Arrow` tecla para recorrer el historial de expresiones de JavaScript que ejecutó anteriormente en la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-213">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="d6521-214">Pulse `Enter` para volver a ejecutar la expresión.</span><span class="sxs-lookup"><span data-stu-id="d6521-214">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="d6521-215">Ver el valor de una expresión en tiempo real con expresiones en directo</span><span class="sxs-lookup"><span data-stu-id="d6521-215">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="d6521-216">Si se encuentra escribiendo la misma expresión de JavaScript en la consola varias veces, es posible que le resulte más fácil crear una **expresión en vivo**.</span><span class="sxs-lookup"><span data-stu-id="d6521-216">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="d6521-217">Con **expresiones en vivo** , escriba una expresión una vez y, a continuación, ancle en la parte superior de la consola.</span><span class="sxs-lookup"><span data-stu-id="d6521-217">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="d6521-218">El valor de la expresión se actualiza casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="d6521-218">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="d6521-219">Vea [inspeccionar valores de expresiones de JavaScript en tiempo real con expresiones en directo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="d6521-219">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="d6521-220">Deshabilitar evaluación diligente</span><span class="sxs-lookup"><span data-stu-id="d6521-220">Disable Eager Evaluation</span></span>   

<span data-ttu-id="d6521-221">Mientras escribe las expresiones de JavaScript en la consola, **evaluación diligente** muestra una vista previa del valor devuelto para esa expresión.</span><span class="sxs-lookup"><span data-stu-id="d6521-221">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="d6521-222">[Abra configuración de consola](#open-console-settings) y deshabilite la casilla **evaluación diligente** para desactivar las vistas previas de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d6521-222">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="d6521-223">Deshabilitar Autocompletar desde historial</span><span class="sxs-lookup"><span data-stu-id="d6521-223">Disable autocomplete from history</span></span>   

<span data-ttu-id="d6521-224">A medida que escribe una expresión, la ventana emergente de autocompletar de la consola muestra expresiones que ejecutó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d6521-224">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="d6521-225">Estas expresiones van precedidas del `>` carácter.</span><span class="sxs-lookup"><span data-stu-id="d6521-225">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="d6521-226">[Abra configuración de consola](#open-console-settings) y deshabilite la casilla **Autocompletar del historial** para dejar de mostrar las expresiones de su historial.</span><span class="sxs-lookup"><span data-stu-id="d6521-226">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="d6521-227">En la siguiente ilustración, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se han evaluado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d6521-227">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="El mensaje emergente de Autocompletar muestra expresiones del historial" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="d6521-229">El mensaje emergente de Autocompletar muestra expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="d6521-229">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="d6521-230">Seleccionar contexto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6521-230">Select JavaScript context</span></span>   

<span data-ttu-id="d6521-231">De forma predeterminada, la lista desplegable de **contexto de JavaScript** se establece en **Top**, que representa el [contexto de exploración][MDNBrowsingContext] del documento principal.</span><span class="sxs-lookup"><span data-stu-id="d6521-231">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Lista desplegable de contexto de JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="d6521-233">Lista desplegable de **contexto de JavaScript**</span><span class="sxs-lookup"><span data-stu-id="d6521-233">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="d6521-234">Supongamos que tiene un anuncio en la página insertado en una `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="d6521-234">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="d6521-235">Para poder ajustar el DOM del anuncio, deseas ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d6521-235">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="d6521-236">En primer lugar, debe seleccionar el contexto de exploración del anuncio en la lista desplegable de **contexto de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="d6521-236">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Seleccionar un contexto de JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="d6521-238">Seleccionar un contexto de JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="d6521-238">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="d6521-239">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="d6521-239">Clear the Console</span></span>   

<span data-ttu-id="d6521-240">Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:</span><span class="sxs-lookup"><span data-stu-id="d6521-240">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="d6521-241">Haga clic en **Borrar consola** \ ( ![ Borrar consola ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d6521-241">Click **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="d6521-242">Haga clic con el botón derecho en un mensaje y seleccione **Borrar consola**.</span><span class="sxs-lookup"><span data-stu-id="d6521-242">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="d6521-243">Escriba `clear()` la consola y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d6521-243">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="d6521-244">Llama `console.clear()` desde el JavaScript de tu página web.</span><span class="sxs-lookup"><span data-stu-id="d6521-244">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="d6521-245">Pulsa `Control` + `L` mientras la consola está en el foco.</span><span class="sxs-lookup"><span data-stu-id="d6521-245">Press `Control`+`L` while the Console is in focus.</span></span>  
    
<!--
 

  
-->  

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
> <span data-ttu-id="d6521-255">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6521-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d6521-256">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d6521-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d6521-258">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6521-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
