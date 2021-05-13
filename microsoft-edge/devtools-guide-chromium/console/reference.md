---
description: Una referencia completa para cada característica y comportamiento de la interfaz de usuario de consola en Microsoft Edge DevTools.
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f14663ca1883c0a81184f9a4fa67ddcbd3f08a24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564528"
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
# <a name="console-reference"></a><span data-ttu-id="52a40-104">Referencia de consola</span><span class="sxs-lookup"><span data-stu-id="52a40-104">Console reference</span></span>  

<span data-ttu-id="52a40-105">Este artículo es una referencia de las características relacionadas con la Microsoft Edge DevTools Console.</span><span class="sxs-lookup"><span data-stu-id="52a40-105">This article is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="52a40-106">Se supone que ya está familiarizado con el uso de la consola para ver los mensajes registrados y ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="52a40-106">It assumes you're already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="52a40-107">Si no es así, vaya a Introducción a la ejecución de [JavaScript en][DevtoolsConsoleConsoleJavascript] la consola y Empezar a registrar [mensajes en la consola][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="52a40-107">If not, navigate to [Get started with running JavaScript in the Console][DevtoolsConsoleConsoleJavascript] and [Get started with logging messages in the Console][DevtoolsConsoleConsoleLog].</span></span>  

<span data-ttu-id="52a40-108">Si está buscando la referencia de api en funciones como , vaya a `console.log()` Referencia de api de [consola][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="52a40-108">If you're looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="52a40-109">Para obtener la referencia de funciones como `monitorEvents()` , vaya a Console Utilities API [Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="52a40-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="52a40-110">Abrir la consola</span><span class="sxs-lookup"><span data-stu-id="52a40-110">Open the Console</span></span>  

<span data-ttu-id="52a40-111">Puede abrir la consola **como** una herramienta [en el panel superior](#open-the-console-tool) o como una herramienta en el [cajón](#open-the-console-tool-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="52a40-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="52a40-112">Abrir la herramienta Consola</span><span class="sxs-lookup"><span data-stu-id="52a40-112">Open the Console tool</span></span>  

<span data-ttu-id="52a40-113">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="52a40-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="La herramienta Consola" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="52a40-115">La **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="52a40-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-116">Para abrir la **herramienta Consola** desde [el][DevtoolsCommandMenuIndex]menú comando , escriba y, a continuación, ejecute el comando Mostrar consola que tiene el `Console` distintivo **Panel** junto a él. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="52a40-116">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Ejecute el comando para mostrar la herramienta Consola" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="52a40-118">Ejecute el comando para mostrar la **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="52a40-118">Run the command to display the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="52a40-119">Abrir la herramienta Consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="52a40-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="52a40-120">Seleccione `Esc` o elija Personalizar y controlar **DevTools** \( \) y, a continuación, `...` elija Mostrar **cajón de consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-120">Select `Esc` or choose **Customize and control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar el cajón de la consola" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="52a40-122">Mostrar el cajón de la consola</span><span class="sxs-lookup"><span data-stu-id="52a40-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="52a40-123">El cajón aparece en la parte inferior de la ventana DevTools, con la **herramienta Consola** abierta.</span><span class="sxs-lookup"><span data-stu-id="52a40-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="La herramienta Consola en el cajón" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="52a40-125">La **herramienta Consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="52a40-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-126">Para abrir la **herramienta Consola** desde el menú [comando][DevtoolsCommandMenuIndex], escriba y, a continuación, ejecute el comando Mostrar consola que tiene el distintivo `Console` **De** cajón junto a él. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="52a40-126">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Ejecute el comando para mostrar la herramienta **Consola** en el cajón" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="52a40-128">Ejecutar el comando para mostrar la **herramienta Consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="52a40-128">Run the command to display the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="52a40-129">Abra la consola Configuración</span><span class="sxs-lookup"><span data-stu-id="52a40-129">Open Console Settings</span></span>  

<span data-ttu-id="52a40-130">Elija el **botón Consola Configuración** \( Icono de Configuración ![ ](../media/settings-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="52a40-130">Choose the **Console Settings** \(![Console Settings icon](../media/settings-button-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Consola Configuración" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="52a40-132">Consola Configuración</span><span class="sxs-lookup"><span data-stu-id="52a40-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="52a40-133">Los vínculos siguientes explican cada configuración.</span><span class="sxs-lookup"><span data-stu-id="52a40-133">The following links explain each setting.</span></span>  

*   [<span data-ttu-id="52a40-134">Ocultar red</span><span class="sxs-lookup"><span data-stu-id="52a40-134">Hide network</span></span>](#hide-network-messages)  
*   [<span data-ttu-id="52a40-135">Conservar registro</span><span class="sxs-lookup"><span data-stu-id="52a40-135">Preserve log</span></span>](#persist-messages-across-page-loads)  
*   [<span data-ttu-id="52a40-136">Solo contexto seleccionado</span><span class="sxs-lookup"><span data-stu-id="52a40-136">Selected context only</span></span>](#filter-out-messages-from-different-contexts)  
*   [<span data-ttu-id="52a40-137">Grupo similar</span><span class="sxs-lookup"><span data-stu-id="52a40-137">Group similar</span></span>](#turn-off-message-grouping)  
*   [<span data-ttu-id="52a40-138">XML de registroHttpRequests</span><span class="sxs-lookup"><span data-stu-id="52a40-138">Log XMLHttpRequests</span></span>](#log-xhr-and-fetch-requests)  
*   [<span data-ttu-id="52a40-139">Evaluación ansiosa</span><span class="sxs-lookup"><span data-stu-id="52a40-139">Eager evaluation</span></span>](#turn-off-eager-evaluation)  
*   [<span data-ttu-id="52a40-140">Autocompletar del historial</span><span class="sxs-lookup"><span data-stu-id="52a40-140">Autocomplete from history</span></span>](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="52a40-141">Abrir la barra lateral de la consola</span><span class="sxs-lookup"><span data-stu-id="52a40-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="52a40-142">Para mostrar la **barra lateral,** elija **Mostrar barra lateral de la** consola \( Mostrar barra lateral de la consola ![ ](../media/show-console-sidebar-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="52a40-142">To display the **Sidebar**, choose **Show console sidebar** \(![Show console sidebar](../media/show-console-sidebar-icon.msft.png)\).</span></span>  <span data-ttu-id="52a40-143">La **barra** lateral le ayuda a filtrar.</span><span class="sxs-lookup"><span data-stu-id="52a40-143">The **Sidebar** is helps you filter.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral de consola" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **<span data-ttu-id="52a40-145">Barra lateral de consola</span><span class="sxs-lookup"><span data-stu-id="52a40-145">Console Sidebar</span></span>**  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="52a40-146">Ver mensajes</span><span class="sxs-lookup"><span data-stu-id="52a40-146">View messages</span></span>  

<span data-ttu-id="52a40-147">Esta sección contiene características que cambian la forma en que se presentan los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="52a40-147">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="52a40-148">Para obtener un tutorial práctica, vaya a [Ver mensajes][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].</span><span class="sxs-lookup"><span data-stu-id="52a40-148">For a hands-on walkthrough, navigate to [View messages][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].</span></span>  

### <a name="turn-off-message-grouping"></a><span data-ttu-id="52a40-149">Desactivar la agrupación de mensajes</span><span class="sxs-lookup"><span data-stu-id="52a40-149">Turn off message grouping</span></span>  

<span data-ttu-id="52a40-150">Para desactivar el comportamiento de agrupación de mensajes predeterminado de la **consola,** [abra consola Configuración](#open-console-settings) y elija la casilla junto a Grupo **similar**.</span><span class="sxs-lookup"><span data-stu-id="52a40-150">To turn off the default message grouping behavior of the **Console**, [open Console Settings](#open-console-settings) and choose the checkbox next to **Group similar**.</span></span>  <span data-ttu-id="52a40-151">Para obtener un ejemplo, vaya [a Registrar XHR y Obtener solicitudes](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="52a40-151">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="52a40-152">Registrar solicitudes XHR y Fetch</span><span class="sxs-lookup"><span data-stu-id="52a40-152">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="52a40-153">Para registrar todas las solicitudes y todas en la consola a medida que se produce cada una de ellas, abra console Configuración y seleccione la casilla situada junto a `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. \*\*\*\* [](#open-console-settings)</span><span class="sxs-lookup"><span data-stu-id="52a40-153">To log all `XMLHttpRequest` and `Fetch` requests to the **Console** as each happens, [open Console Settings](#open-console-settings) and choose the checkbox next to **Log XMLHttpRequests**.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Registrar solicitudes XMLHttpRequest y Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="52a40-155">Registro `XMLHttpRequest` y `Fetch` solicitudes</span><span class="sxs-lookup"><span data-stu-id="52a40-155">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-156">El mensaje superior de la figura anterior muestra el comportamiento de agrupación predeterminado de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-156">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="52a40-157">Conservar mensajes entre cargas de página</span><span class="sxs-lookup"><span data-stu-id="52a40-157">Persist messages across page loads</span></span>  

<span data-ttu-id="52a40-158">Al cargar una nueva página web, la acción predeterminada borra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-158">When you load a new webpage, the default action clears the **Console**.</span></span>  <span data-ttu-id="52a40-159">Para conservar los mensajes en las cargas de página, [abra Configuración](#open-console-settings) consola y seleccione la casilla situada junto a **Conservar registro**.</span><span class="sxs-lookup"><span data-stu-id="52a40-159">To persist messages across page loads, [open Console Settings](#open-console-settings) and choose the checkbox next to **Preserve Log**.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="52a40-160">Ocultar mensajes de red</span><span class="sxs-lookup"><span data-stu-id="52a40-160">Hide network messages</span></span>  

<span data-ttu-id="52a40-161">La acción predeterminada para Microsoft Edge es registra los mensajes de red en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-161">The default action for Microsoft Edge is to logs network messages to the **Console**.</span></span>  <span data-ttu-id="52a40-162">En la siguiente figura, el mensaje elegido representa un código de estado HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="52a40-162">In the following figure, the chosen message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un mensaje 429 en la consola" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="52a40-164">Un `429` mensaje en la **consola**</span><span class="sxs-lookup"><span data-stu-id="52a40-164">A `429` message in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-165">Para ocultar los mensajes de red, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="52a40-165">To hide network messages, complete the following actions.</span></span>  

1.  <span data-ttu-id="52a40-166">[Abra la consola Configuración](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="52a40-166">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="52a40-167">Seleccione la casilla situada junto a **Ocultar red**.</span><span class="sxs-lookup"><span data-stu-id="52a40-167">Choose the checkbox next to **Hide Network**.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="52a40-168">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="52a40-168">Filter messages</span></span>  

<span data-ttu-id="52a40-169">Existen muchas formas de filtrar los mensajes en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-169">Many ways exist to filter out messages in the **Console**.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="52a40-170">Filtrar mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="52a40-170">Filter out browser messages</span></span>  

<span data-ttu-id="52a40-171">[Abra la barra lateral de la](#open-the-console-sidebar) consola y elija # mensajes de **usuario** para mostrar solo los mensajes que provenían del JavaScript de la página web.</span><span class="sxs-lookup"><span data-stu-id="52a40-171">[Open the Console Sidebar](#open-the-console-sidebar) and choose **# user messages** to only display messages that came from the JavaScript of the webpage.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Mostrar mensajes de usuario" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="52a40-173">Mostrar mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="52a40-173">Display user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="52a40-174">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="52a40-174">Filter by log level</span></span>  

<span data-ttu-id="52a40-175">DevTools asigna a cada `console.*` método uno de los cuatro niveles de gravedad.</span><span class="sxs-lookup"><span data-stu-id="52a40-175">DevTools assigns each `console.*` method one of the four severity levels.</span></span>  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
<span data-ttu-id="52a40-176">Por ejemplo, `console.log()` está en el `Info` grupo, pero está en el `console.error()` `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="52a40-176">For example, `console.log()` is in the `Info` group, but `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="52a40-177">La [referencia de la API de][DevToolsConsoleApi] consola describe el nivel de gravedad de cada método aplicable.</span><span class="sxs-lookup"><span data-stu-id="52a40-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="52a40-178">Cada mensaje que el explorador inicia sesión en la consola también tiene un nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="52a40-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="52a40-179">Puede ocultar cualquier nivel de mensajes que no le interesen.</span><span class="sxs-lookup"><span data-stu-id="52a40-179">You may hide any level of messages that you're not interested in.</span></span>  <span data-ttu-id="52a40-180">Por ejemplo, si solo está interesado en los `Error` mensajes, puede ocultar los otros tres grupos.</span><span class="sxs-lookup"><span data-stu-id="52a40-180">For example, if you're only interested in `Error` messages, you may hide the other three groups.</span></span>  

<span data-ttu-id="52a40-181">Para filtrar los mensajes, elija el desplegable **Niveles de** registro y `Verbose` elija , , o `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="52a40-181">To filter the messages, choose the **Log Levels** dropdown and choose `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Desplegable Niveles de registro" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="52a40-183">Desplegable **Niveles de** registro</span><span class="sxs-lookup"><span data-stu-id="52a40-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-184">Para usar el nivel de registro para filtrar, [abra](#open-the-console-sidebar) la barra lateral de la consola y, a continuación, elija **Errores**, **Advertencias,** **Información**o **Detallado**.</span><span class="sxs-lookup"><span data-stu-id="52a40-184">To use the log level to filter, [open the Console Sidebar](#open-the-console-sidebar) and then choose **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar la barra lateral para ver advertencias" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="52a40-186">Usar la barra lateral para ver advertencias</span><span class="sxs-lookup"><span data-stu-id="52a40-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="52a40-187">Filtrar mensajes por dirección URL</span><span class="sxs-lookup"><span data-stu-id="52a40-187">Filter messages by URL</span></span>  

<span data-ttu-id="52a40-188">Escriba `url:` seguido de una dirección URL para ver solo los mensajes que provenían de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="52a40-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="52a40-189">Después de escribir `url:` , DevTools muestra todas las direcciones URL relevantes.</span><span class="sxs-lookup"><span data-stu-id="52a40-189">After you type `url:`, DevTools displays all relevant URLs.</span></span>  <span data-ttu-id="52a40-190">Los dominios también funcionan.</span><span class="sxs-lookup"><span data-stu-id="52a40-190">Domains also work.</span></span>  <span data-ttu-id="52a40-191">Por ejemplo, si y están registrando mensajes, le permite `https://example.com/a.js` `https://example.com/b.js` `url:https://example.com` centrarse en los mensajes de estos dos scripts.</span><span class="sxs-lookup"><span data-stu-id="52a40-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` allows you to focus on the messages from these two scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Un filtro de dirección URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="52a40-193">Un filtro de dirección URL</span><span class="sxs-lookup"><span data-stu-id="52a40-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-194">Para ocultar mensajes de una dirección URL, escriba `-url:` .</span><span class="sxs-lookup"><span data-stu-id="52a40-194">To hide messages from a URL, type `-url:`.</span></span>  <span data-ttu-id="52a40-195">Es un filtro de dirección URL negativo.</span><span class="sxs-lookup"><span data-stu-id="52a40-195">It's a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la https://b.wal.co dirección URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="52a40-197">Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la `https://b.wal.co` dirección URL</span><span class="sxs-lookup"><span data-stu-id="52a40-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="52a40-198">Para mostrar mensajes desde una única dirección URL, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="52a40-198">To display messages from a single URL, complete the following actions.</span></span>  

1.  <span data-ttu-id="52a40-199">[Abra la barra lateral de la consola](#open-the-console-sidebar).</span><span class="sxs-lookup"><span data-stu-id="52a40-199">[Open the Console Sidebar](#open-the-console-sidebar).</span></span>  
1.  <span data-ttu-id="52a40-200">Expanda la **sección # mensajes de** usuario.</span><span class="sxs-lookup"><span data-stu-id="52a40-200">Expand the **# user messages** section.</span></span>  
1.  <span data-ttu-id="52a40-201">Elija la dirección URL del script que contiene los mensajes en los que desea centrarse.</span><span class="sxs-lookup"><span data-stu-id="52a40-201">Choose the URL of the script that contains the messages on which you want to focus.</span></span>  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Mostrar los mensajes que provenían de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="52a40-203">Mostrar los mensajes procedentes de</span><span class="sxs-lookup"><span data-stu-id="52a40-203">Display the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="52a40-204">Filtrar mensajes de distintos contextos</span><span class="sxs-lookup"><span data-stu-id="52a40-204">Filter out messages from different contexts</span></span>  

<span data-ttu-id="52a40-205">Suponga que tiene un anuncio \(ad\) en su página web.</span><span class="sxs-lookup"><span data-stu-id="52a40-205">Suppose that you have an advertisement \(ad\) on your webpage.</span></span>  <span data-ttu-id="52a40-206">El anuncio está incrustado en un `<iframe>` y genera muchos mensajes en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-206">The ad is embedded in an `<iframe>` and generates many messages in your **Console**.</span></span>  <span data-ttu-id="52a40-207">Dado que el anuncio se ejecuta en un contexto [de JavaScript](#choose-javascript-context)diferente, una forma de ocultar los mensajes es abrir la consola [Configuración](#open-console-settings) y elegir la casilla junto a Solo **contexto seleccionado**.</span><span class="sxs-lookup"><span data-stu-id="52a40-207">Because the ad is running in a different [JavaScript context](#choose-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and choose the checkbox next to **Selected Context Only**.</span></span>  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a><span data-ttu-id="52a40-208">Filtrar mensajes que no coincidan con un patrón de expresión regular</span><span class="sxs-lookup"><span data-stu-id="52a40-208">Filter out messages that don't match a regular expression pattern</span></span>  

<span data-ttu-id="52a40-209">Escriba una expresión regular como, por ejemplo, en el cuadro de texto Filtrar para filtrar los mensajes que no `/[gm][ta][mi]/` coincidan con ese patrón. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="52a40-209">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** textbox to filter out any messages that don't match that pattern.</span></span>  <span data-ttu-id="52a40-210">DevTools comprueba si el patrón se encuentra en el texto del mensaje o en el script que hizo que se registrara el mensaje.</span><span class="sxs-lookup"><span data-stu-id="52a40-210">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar los mensajes que no coincidan con la expresión regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="52a40-212">Filtrar los mensajes que no coincidan con la `/[gm][ta][mi]/` expresión regex</span><span class="sxs-lookup"><span data-stu-id="52a40-212">Filter out any messages that don't match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="52a40-213">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="52a40-213">Run JavaScript</span></span>  

<span data-ttu-id="52a40-214">Esta sección contiene características relacionadas con la ejecución de JavaScript en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-214">This section contains features related to running JavaScript in the **Console**.</span></span>  <span data-ttu-id="52a40-215">Para obtener un tutorial práctica, vaya a [Ejecutar JavaScript][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="52a40-215">For a hands-on walkthrough, navigate to [Run JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  

### <a name="rerun-expressions-from-history"></a><span data-ttu-id="52a40-216">Volver a ejecutar expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="52a40-216">Rerun expressions from history</span></span>  

<span data-ttu-id="52a40-217">Seleccione `Up Arrow` esta opción para recorrer el historial de expresiones de JavaScript que se ejecutó anteriormente en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-217">Select `Up Arrow` to cycle through the history of JavaScript expressions that you ran earlier in the **Console**.</span></span>  <span data-ttu-id="52a40-218">Seleccione `Enter` para ejecutar esa expresión de nuevo.</span><span class="sxs-lookup"><span data-stu-id="52a40-218">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="52a40-219">Ver el valor de una expresión en tiempo real con Live Expressions</span><span class="sxs-lookup"><span data-stu-id="52a40-219">Watch the value of an expression in real time with Live Expressions</span></span>  

<span data-ttu-id="52a40-220">Si se encuentra escribiendo la misma expresión de JavaScript en la **consola** repetidamente, es posible que le resulte más fácil crear **una expresión live**.</span><span class="sxs-lookup"><span data-stu-id="52a40-220">If you find yourself typing the same JavaScript expression in the **Console** repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="52a40-221">Con **live expressions**, se escribe una expresión una vez y, a continuación, se ancla a la parte superior de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-221">With **Live Expressions**, you type an expression once and then pin it to the top of your **Console**.</span></span>  <span data-ttu-id="52a40-222">El valor de la expresión se actualiza casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="52a40-222">The value of the expression updates in near real time.</span></span>  <span data-ttu-id="52a40-223">Vaya a [Ver valores de expresión de JavaScript en Real-Time Con expresiones en directo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="52a40-223">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="turn-off-eager-evaluation"></a><span data-ttu-id="52a40-224">Desactivar evaluación ansiosa</span><span class="sxs-lookup"><span data-stu-id="52a40-224">Turn off Eager Evaluation</span></span>  

<span data-ttu-id="52a40-225">**Eager Evaluation** muestra una vista previa del valor devuelto al escribir expresiones de JavaScript en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-225">**Eager Evaluation** displays a preview of the return value as you type JavaScript expressions in the **Console**.</span></span>  <span data-ttu-id="52a40-226">Para desactivar las vistas previas de valor devuelto, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="52a40-226">To turn off the return value previews, complete the following actions.</span></span>  

1.  <span data-ttu-id="52a40-227">[Abra la consola Configuración](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="52a40-227">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="52a40-228">Quite la casilla situada junto a **Evaluación ansiosa**.</span><span class="sxs-lookup"><span data-stu-id="52a40-228">Remove the checkbox next to **Eager Evaluation**.</span></span>  
    
### <a name="turn-off-autocomplete-from-history"></a><span data-ttu-id="52a40-229">Desactivar autocompletar del historial</span><span class="sxs-lookup"><span data-stu-id="52a40-229">Turn off autocomplete from history</span></span>  

<span data-ttu-id="52a40-230">Al escribir una expresión, la ventana emergente autocompletar de la **consola** muestra las expresiones que ejecutó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52a40-230">As you type out an expression, the autocomplete popup window for the **Console** displays expressions that you ran earlier.</span></span>  <span data-ttu-id="52a40-231">Las expresiones están pre-pended con el `>` carácter.</span><span class="sxs-lookup"><span data-stu-id="52a40-231">The expressions are pre-pended with the `>` character.</span></span>  <span data-ttu-id="52a40-232">Para dejar de mostrar expresiones del historial, abra [la](#open-console-settings) Configuración consola y quite la casilla junto a **Autocompletar del historial.**</span><span class="sxs-lookup"><span data-stu-id="52a40-232">To stop displaying expressions from your history, [open Console Settings](#open-console-settings) and remove the checkbox next to **Autocomplete From History** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="52a40-233">En la siguiente figura, `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se evaluaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52a40-233">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="El menú emergente autocompletar muestra expresiones del historial" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="52a40-235">El menú emergente autocompletar muestra expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="52a40-235">The autocomplete popup menu displays expressions from history</span></span>  
:::image-end:::  

### <a name="choose-javascript-context"></a><span data-ttu-id="52a40-236">Elegir contexto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="52a40-236">Choose JavaScript context</span></span>  

<span data-ttu-id="52a40-237">La opción predeterminada para el desplegable **Contexto de JavaScript** es **la**parte superior, que representa el contexto [de exploración][MdnDocsGlossaryBrowsingContext] de la página web principal.</span><span class="sxs-lookup"><span data-stu-id="52a40-237">The default option for the **JavaScript Context** dropdown is **top**, which represents the [browsing context][MdnDocsGlossaryBrowsingContext] of the main webpage.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Desplegable Contexto de JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="52a40-239">Desplegable **Contexto de JavaScript**</span><span class="sxs-lookup"><span data-stu-id="52a40-239">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="52a40-240">Supongamos que tienes un anuncio en tu página web incrustado en un `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="52a40-240">Suppose you have an ad on your webpage embedded in an `<iframe>`.</span></span>  <span data-ttu-id="52a40-241">Quieres ejecutar JavaScript para ajustar el DOM del anuncio.</span><span class="sxs-lookup"><span data-stu-id="52a40-241">You want to run JavaScript to tweak the DOM of the ad.</span></span>  <span data-ttu-id="52a40-242">En primer lugar, elige el contexto de exploración del anuncio en el desplegable **Contexto de JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="52a40-242">First, choose the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Elegir un contexto de JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="52a40-244">Elegir un contexto de JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="52a40-244">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="52a40-245">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="52a40-245">Clear the Console</span></span>  

<span data-ttu-id="52a40-246">Para borrar la **consola,** complete cualquiera de los siguientes flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="52a40-246">To clear the **Console**, complete any of the following workflows.</span></span>  

*   <span data-ttu-id="52a40-247">Elija el **botón Borrar consola** \( Borrar consola ![ ](../media/clear-console-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="52a40-247">Choose the **Clear Console** \(![Clear Console](../media/clear-console-button-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="52a40-248">Mantenga el mouse sobre un mensaje, abra el menú contextual \(haga clic con el botón secundario\) y elija **Borrar consola**.</span><span class="sxs-lookup"><span data-stu-id="52a40-248">Hover on a message, open the contextual menu \(right-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="52a40-249">Escriba `clear()` en la **Consola** y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="52a40-249">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="52a40-250">Ejecute `console.clear()` desde JavaScript para la página web.</span><span class="sxs-lookup"><span data-stu-id="52a40-250">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="52a40-251">Seleccione `Control` + `L` mientras la **consola** está en foco.</span><span class="sxs-lookup"><span data-stu-id="52a40-251">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="52a40-252">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="52a40-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensajes en la herramienta consola | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Consola como entorno de JavaScript | Microsoft Docs"  
[DevtoolsConsoleIndex]: .index.md "Use la consola | Microsoft Docs"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Inspeccionar y filtrar información en la página web | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Supervisar los cambios en JavaScript mediante expresiones live | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecute comandos con el menú Microsoft Edge comando DevTools | Microsoft Docs"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> <span data-ttu-id="52a40-262">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52a40-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="52a40-263">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="52a40-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="52a40-265">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52a40-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
