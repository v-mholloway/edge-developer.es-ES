---
description: Una referencia completa sobre todas las características y comportamientos relacionados con la interfaz de usuario de consola en Microsoft Edge DevTools.
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d6fed1681e64f8f57c2e577017d623039a7b4152
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439370"
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

# <a name="console-reference"></a><span data-ttu-id="e603f-104">Referencia de consola</span><span class="sxs-lookup"><span data-stu-id="e603f-104">Console reference</span></span>  

<span data-ttu-id="e603f-105">Esta página es una referencia de las características relacionadas con la consola DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e603f-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="e603f-106">Se supone que ya está familiarizado con el uso de la consola para ver los mensajes registrados y ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e603f-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="e603f-107">Si no es así, vaya a Introducción a la ejecución [de JavaScript en][DevToolsConsoleJavascript] la consola y Empezar a registrar [mensajes en la consola][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="e603f-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="e603f-108">Si está buscando la referencia de API en funciones como `console.log()` , vaya a Referencia de api de [consola][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="e603f-108">If you are looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="e603f-109">Para obtener la referencia de funciones como `monitorEvents()` , vaya a Console Utilities API [Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="e603f-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="e603f-110">Abrir la consola</span><span class="sxs-lookup"><span data-stu-id="e603f-110">Open the Console</span></span>  

<span data-ttu-id="e603f-111">Puede abrir la consola **como** una herramienta [en el panel superior](#open-the-console-tool) o como una herramienta en el [cajón](#open-the-console-tool-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="e603f-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="e603f-112">Abrir la herramienta Consola</span><span class="sxs-lookup"><span data-stu-id="e603f-112">Open the Console tool</span></span>  

<span data-ttu-id="e603f-113">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e603f-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="La herramienta Consola" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="e603f-115">La **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="e603f-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="e603f-116">Para abrir la **herramienta Consola** desde [el][DevToolsCommandMenu]menú comando, empiece a escribir y, a continuación, ejecute el comando Mostrar consola que tiene el `Console` distintivo **Panel** junto a él. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e603f-116">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="El comando para mostrar el panel Consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="e603f-118">El comando para mostrar la **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="e603f-118">The command to show the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="e603f-119">Abrir la herramienta Consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="e603f-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="e603f-120">Seleccione `Escape` o elija Personalizar y controlar **DevTools** \( \) y, a continuación, `...` elija Mostrar **cajón de consola**.</span><span class="sxs-lookup"><span data-stu-id="e603f-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar el cajón de la consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="e603f-122">Mostrar el cajón de la consola</span><span class="sxs-lookup"><span data-stu-id="e603f-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="e603f-123">El cajón aparece en la parte inferior de la ventana DevTools, con la **herramienta Consola** abierta.</span><span class="sxs-lookup"><span data-stu-id="e603f-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="La herramienta Consola en el cajón" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="e603f-125">La **herramienta Consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="e603f-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="e603f-126">Para abrir la **herramienta Consola** desde [el][DevToolsCommandMenu]menú comando, empiece a escribir y, a continuación, ejecute el comando Mostrar consola que tiene el distintivo `Console` **De** cajón junto \*\*\*\* a él.</span><span class="sxs-lookup"><span data-stu-id="e603f-126">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="El comando para mostrar la herramienta **Consola** en el cajón" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="e603f-128">El comando para mostrar la **herramienta Consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="e603f-128">The command to show the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="e603f-129">Abrir configuración de consola</span><span class="sxs-lookup"><span data-stu-id="e603f-129">Open Console Settings</span></span>  

<span data-ttu-id="e603f-130">Elija **Configuración de consola** \( Icono configuración de consola ![ ](../media/settings-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="e603f-130">Choose **Console Settings** \(![Console Settings icon](../media/settings-button-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configuración de consola" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="e603f-132">Configuración de consola</span><span class="sxs-lookup"><span data-stu-id="e603f-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="e603f-133">Los vínculos siguientes explican cada configuración:</span><span class="sxs-lookup"><span data-stu-id="e603f-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="e603f-134">Ocultar red</span><span class="sxs-lookup"><span data-stu-id="e603f-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="e603f-135">Conservar registro</span><span class="sxs-lookup"><span data-stu-id="e603f-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="e603f-136">Solo contexto seleccionado</span><span class="sxs-lookup"><span data-stu-id="e603f-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="e603f-137">Group Similar</span><span class="sxs-lookup"><span data-stu-id="e603f-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="e603f-138">Log XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="e603f-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="e603f-139">Evaluación ansiosa</span><span class="sxs-lookup"><span data-stu-id="e603f-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="e603f-140">Autocompletar desde el historial</span><span class="sxs-lookup"><span data-stu-id="e603f-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="e603f-141">Abrir la barra lateral de la consola</span><span class="sxs-lookup"><span data-stu-id="e603f-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="e603f-142">Elija **Mostrar barra lateral de consola** \( Mostrar barra lateral de consola \) para mostrar la barra ![ ](../media/show-console-sidebar-icon.msft.png) lateral, que es útil para filtrar.</span><span class="sxs-lookup"><span data-stu-id="e603f-142">Choose **Show Console Sidebar** \(![Show Console Sidebar](../media/show-console-sidebar-icon.msft.png)\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral de consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="e603f-144">**Consola** Barra lateral</span><span class="sxs-lookup"><span data-stu-id="e603f-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="e603f-145">Ver mensajes</span><span class="sxs-lookup"><span data-stu-id="e603f-145">View messages</span></span>  

<span data-ttu-id="e603f-146">Esta sección contiene características que cambian la forma en que se presentan los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="e603f-147">Para obtener un tutorial práctica, vaya a [Ver mensajes][DevToolsConsoleViewMessages].</span><span class="sxs-lookup"><span data-stu-id="e603f-147">For a hands-on walkthrough, navigate to [View messages][DevToolsConsoleViewMessages].</span></span>  

### <a name="disable-message-grouping"></a><span data-ttu-id="e603f-148">Deshabilitar la agrupación de mensajes</span><span class="sxs-lookup"><span data-stu-id="e603f-148">Disable message grouping</span></span>  

<span data-ttu-id="e603f-149">[Abra Configuración de la](#open-console-settings) consola y deshabilite **Grupo de forma similar** para deshabilitar el comportamiento de agrupación de mensajes predeterminado de la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="e603f-150">Para obtener un ejemplo, vaya [a Registrar XHR y Obtener solicitudes](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="e603f-150">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="e603f-151">Registrar solicitudes XHR y Fetch</span><span class="sxs-lookup"><span data-stu-id="e603f-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="e603f-152">[Abra Configuración de la](#open-console-settings) consola y **habilite Log XMLHttpRequests** para registrar todas y solicitudes `XMLHttpRequest` en la consola a medida que se `Fetch` suceden.</span><span class="sxs-lookup"><span data-stu-id="e603f-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Registrar solicitudes XMLHttpRequest y Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="e603f-154">Registro `XMLHttpRequest` y `Fetch` solicitudes</span><span class="sxs-lookup"><span data-stu-id="e603f-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="e603f-155">El mensaje superior de la figura anterior muestra el comportamiento de agrupación predeterminado de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e603f-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="e603f-156">Conservar mensajes entre cargas de página</span><span class="sxs-lookup"><span data-stu-id="e603f-156">Persist messages across page loads</span></span>  

<span data-ttu-id="e603f-157">De forma predeterminada, la consola borra cada vez que se carga una página nueva.</span><span class="sxs-lookup"><span data-stu-id="e603f-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="e603f-158">Para conservar los mensajes en las cargas de página, [abra configuración de consola](#open-console-settings) y, a continuación, habilite la casilla **Conservar** registro.</span><span class="sxs-lookup"><span data-stu-id="e603f-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="e603f-159">Ocultar mensajes de red</span><span class="sxs-lookup"><span data-stu-id="e603f-159">Hide network messages</span></span>  

<span data-ttu-id="e603f-160">De forma predeterminada, el explorador registra los mensajes de red en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e603f-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="e603f-161">En la siguiente figura, el mensaje seleccionado representa un código de estado HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="e603f-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un mensaje 429 en la consola" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="e603f-163">Un `429` mensaje en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e603f-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="e603f-164">Para ocultar mensajes de red:</span><span class="sxs-lookup"><span data-stu-id="e603f-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="e603f-165">[Abra Configuración de la consola](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="e603f-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="e603f-166">Active la casilla **Ocultar red.**</span><span class="sxs-lookup"><span data-stu-id="e603f-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="e603f-167">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="e603f-167">Filter messages</span></span>  

<span data-ttu-id="e603f-168">Hay muchas maneras de filtrar los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-168">There are many ways to filter out messages in the Console.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="e603f-169">Filtrar mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="e603f-169">Filter out browser messages</span></span>  

<span data-ttu-id="e603f-170">[Abra la barra lateral de la](#open-the-console-sidebar) consola y elija Mensajes de **usuario** para mostrar solo los mensajes que provenían del JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="e603f-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Ver mensajes de usuario" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="e603f-172">Ver mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="e603f-172">View user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="e603f-173">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="e603f-173">Filter by log level</span></span>  

<span data-ttu-id="e603f-174">DevTools asigna a cada `console.*` método un nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="e603f-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="e603f-175">Hay 4 niveles: `Verbose` , `Info` , y `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="e603f-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="e603f-176">Por ejemplo, `console.log()` está en el `Info` grupo, mientras que está en el `console.error()` `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="e603f-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="e603f-177">La [referencia de la API de][DevToolsConsoleApi] consola describe el nivel de gravedad de cada método aplicable.</span><span class="sxs-lookup"><span data-stu-id="e603f-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="e603f-178">Cada mensaje que el explorador inicia sesión en la consola también tiene un nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="e603f-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="e603f-179">Puede ocultar cualquier nivel de mensajes que no le interesen.</span><span class="sxs-lookup"><span data-stu-id="e603f-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="e603f-180">Por ejemplo, si solo está interesado en los `Error` mensajes, puede ocultar los otros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="e603f-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="e603f-181">Elija el **desplegable Niveles de registro** para habilitar o deshabilitar , o `Verbose` `Info` `Warning` `Error` mensajes.</span><span class="sxs-lookup"><span data-stu-id="e603f-181">Choose the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Desplegable Niveles de registro" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="e603f-183">Desplegable **Niveles de** registro</span><span class="sxs-lookup"><span data-stu-id="e603f-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="e603f-184">También puede filtrar por [](#open-the-console-sidebar) nivel de registro abriendo la barra lateral de la consola y, a continuación, haciendo clic en **Errores,** **Advertencias,** **Información**o **Verbose**.</span><span class="sxs-lookup"><span data-stu-id="e603f-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and thenchoosing **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar la barra lateral para ver advertencias" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="e603f-186">Usar la barra lateral para ver advertencias</span><span class="sxs-lookup"><span data-stu-id="e603f-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="e603f-187">Filtrar mensajes por dirección URL</span><span class="sxs-lookup"><span data-stu-id="e603f-187">Filter messages by URL</span></span>  

<span data-ttu-id="e603f-188">Escriba `url:` seguido de una dirección URL para ver solo los mensajes que provenían de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e603f-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="e603f-189">Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.</span><span class="sxs-lookup"><span data-stu-id="e603f-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="e603f-190">Los dominios también funcionan.</span><span class="sxs-lookup"><span data-stu-id="e603f-190">Domains also work.</span></span>  <span data-ttu-id="e603f-191">Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, le permite `url:https://example.com` centrarse en los mensajes de estos 2 scripts.</span><span class="sxs-lookup"><span data-stu-id="e603f-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtro de dirección URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="e603f-193">Un filtro de dirección URL</span><span class="sxs-lookup"><span data-stu-id="e603f-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="e603f-194">Escriba `-url:` para ocultar mensajes de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e603f-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="e603f-195">Esto se denomina filtro de dirección URL negativa.</span><span class="sxs-lookup"><span data-stu-id="e603f-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la https://b.wal.co dirección URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="e603f-197">Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL</span><span class="sxs-lookup"><span data-stu-id="e603f-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="e603f-198">También puede mostrar mensajes de una sola dirección URL \*\*\*\* abriendo la barra lateral de [consola,](#open-the-console-sidebar)expandiendo la sección Mensajes de usuario y, a continuación, haciendo clic en la dirección URL del script que contiene los mensajes en los que desea centrarse.</span><span class="sxs-lookup"><span data-stu-id="e603f-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and thenchoosing the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Ver los mensajes procedentes de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="e603f-200">Ver los mensajes procedentes</span><span class="sxs-lookup"><span data-stu-id="e603f-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="e603f-201">Filtrar mensajes de distintos contextos</span><span class="sxs-lookup"><span data-stu-id="e603f-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="e603f-202">Suponga que tiene un anuncio \(ad\) en su página.</span><span class="sxs-lookup"><span data-stu-id="e603f-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="e603f-203">El anuncio está incrustado en un y está generando una gran cantidad `<iframe>` de mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="e603f-204">Dado que el anuncio se ejecuta en un contexto de [](#open-console-settings) [JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es abrir la configuración de consola y activar la casilla **Solo contexto** seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e603f-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and turn on the **Selected Context Only** checkbox.</span></span>  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a><span data-ttu-id="e603f-205">Filtrar mensajes que no coinciden con un patrón de expresión regular</span><span class="sxs-lookup"><span data-stu-id="e603f-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="e603f-206">Escriba una expresión regular como, por ejemplo, en el cuadro de texto Filtrar para filtrar los mensajes que no `/[gm][ta][mi]/` coincidan con ese patrón. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e603f-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="e603f-207">DevTools comprueba si el patrón se encuentra en el texto del mensaje o en el script que hizo que se registrara el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e603f-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar los mensajes que no coincidan con la expresión regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="e603f-209">Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión regex</span><span class="sxs-lookup"><span data-stu-id="e603f-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="e603f-210">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="e603f-210">Run JavaScript</span></span>  

<span data-ttu-id="e603f-211">Esta sección contiene características relacionadas con la ejecución de JavaScript en la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="e603f-212">Para obtener un tutorial práctica, vaya a [Ejecutar JavaScript][DevToolsConsoleOverviewJavascript].</span><span class="sxs-lookup"><span data-stu-id="e603f-212">For a hands-on walkthrough, navigate to [Run JavaScript][DevToolsConsoleOverviewJavascript].</span></span>  

### <a name="re-run-expressions-from-history"></a><span data-ttu-id="e603f-213">Volver a ejecutar expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="e603f-213">Re-run expressions from history</span></span>  

<span data-ttu-id="e603f-214">Seleccione la `Up Arrow` clave para recorrer el historial de expresiones de JavaScript que ejecutó anteriormente en la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-214">Select the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="e603f-215">Seleccione `Enter` para ejecutar esa expresión de nuevo.</span><span class="sxs-lookup"><span data-stu-id="e603f-215">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="e603f-216">Ver el valor de una expresión en tiempo real con live expressions</span><span class="sxs-lookup"><span data-stu-id="e603f-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="e603f-217">Si se encuentra escribiendo la misma expresión de JavaScript en la consola repetidamente, es posible que le resulte más fácil crear **una expresión live**.</span><span class="sxs-lookup"><span data-stu-id="e603f-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="e603f-218">Con **Live Expressions,** escribe una expresión una vez y, a continuación, anclarla a la parte superior de la consola.</span><span class="sxs-lookup"><span data-stu-id="e603f-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="e603f-219">El valor de la expresión se actualiza casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="e603f-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="e603f-220">Vaya a [Ver valores de expresión de JavaScript en Real-Time Con expresiones en directo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="e603f-220">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="disable-eager-evaluation"></a><span data-ttu-id="e603f-221">Deshabilitar la evaluación de Eager</span><span class="sxs-lookup"><span data-stu-id="e603f-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="e603f-222">Al escribir expresiones de JavaScript en la consola, La evaluación **ansiosa** muestra una vista previa del valor devuelto para esa expresión.</span><span class="sxs-lookup"><span data-stu-id="e603f-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="e603f-223">[Abra Configuración de la](#open-console-settings) consola y deshabilite la casilla **Evaluación** ansiosa para desactivar las vistas previas del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e603f-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <a name="disable-autocomplete-from-history"></a><span data-ttu-id="e603f-224">Deshabilitar la autocompletar del historial</span><span class="sxs-lookup"><span data-stu-id="e603f-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="e603f-225">Al escribir una expresión, la ventana emergente autocompletar de la consola muestra las expresiones que ejecutó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e603f-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="e603f-226">Estas expresiones se anteponen al `>` carácter.</span><span class="sxs-lookup"><span data-stu-id="e603f-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="e603f-227">[Abra Configuración de consola](#open-console-settings) y deshabilite la casilla **Autocompletar desde el historial** para dejar de mostrar expresiones de su historial.</span><span class="sxs-lookup"><span data-stu-id="e603f-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="e603f-228">En la siguiente figura, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se evaluaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e603f-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="El elemento emergente autocompletar muestra expresiones del historial" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="e603f-230">El elemento emergente autocompletar muestra expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="e603f-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <a name="select-javascript-context"></a><span data-ttu-id="e603f-231">Seleccionar contexto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="e603f-231">Select JavaScript context</span></span>  

<span data-ttu-id="e603f-232">De forma predeterminada, el desplegable Contexto de **JavaScript** se establece en **la parte**superior, que representa el contexto [de exploración][MDNBrowsingContext] del documento principal.</span><span class="sxs-lookup"><span data-stu-id="e603f-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Desplegable Contexto de JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="e603f-234">Desplegable **Contexto de JavaScript**</span><span class="sxs-lookup"><span data-stu-id="e603f-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="e603f-235">Supongamos que tienes un anuncio en tu página incrustado en un `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="e603f-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="e603f-236">Quieres ejecutar JavaScript para ajustar el DOM del anuncio.</span><span class="sxs-lookup"><span data-stu-id="e603f-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="e603f-237">Primero debes seleccionar el contexto de exploración del anuncio en el desplegable **Contexto de JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="e603f-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Elegir un contexto de JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="e603f-239">Elegir un contexto de JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="e603f-239">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="e603f-240">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="e603f-240">Clear the Console</span></span>  

<span data-ttu-id="e603f-241">Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:</span><span class="sxs-lookup"><span data-stu-id="e603f-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="e603f-242">Elija **Borrar consola** \( Borrar consola ![ ](../media/clear-console-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="e603f-242">Choose **Clear Console** \(![Clear Console](../media/clear-console-button-icon.msft.png)\).</span></span>  
*   <span data-ttu-id="e603f-243">Mantenga el mouse sobre un mensaje, abra el menú contextual \(righ-click\) y elija **Borrar consola**.</span><span class="sxs-lookup"><span data-stu-id="e603f-243">Hover on a message, open the contextual menu \(righ-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="e603f-244">Escriba `clear()` en la **Consola** y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e603f-244">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="e603f-245">Ejecute `console.clear()` desde JavaScript para la página web.</span><span class="sxs-lookup"><span data-stu-id="e603f-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="e603f-246">Seleccione `Control` + `L` mientras la **consola** está en foco.</span><span class="sxs-lookup"><span data-stu-id="e603f-246">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e603f-247">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e603f-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Visualización de mensajes registrados: información general de la consola | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ejecución de JavaScript: información general de la consola | Microsoft Docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft Docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Ver valores de expresión de JavaScript en tiempo real con Live Expressions | Microsoft Docs"  
[DevToolsConsoleLog]: ./log.md "Introducción al registro de mensajes en la consola | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> <span data-ttu-id="e603f-257">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e603f-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e603f-258">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e603f-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e603f-260">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e603f-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
