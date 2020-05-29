---
title: Referencia de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601791"
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





# <span data-ttu-id="66fd3-103">Referencia de consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-103">Console Reference</span></span>   



<span data-ttu-id="66fd3-104">Esta página es una referencia de las características relacionadas con la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="66fd3-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="66fd3-105">Se da por supuesto que ya está familiarizado con el uso de la consola para ver mensajes registrados y ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66fd3-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="66fd3-106">Si no es así, vea empezar [a ejecutar JavaScript en la consola][DevToolsConsoleJavascript] y empezar [a registrar mensajes en la consola][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="66fd3-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="66fd3-107">Si busca la referencia de la API en funciones como `console.log()` vea la [referencia de API de consola][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="66fd3-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="66fd3-108">Para consultar la referencia en funciones como, consulte la referencia de la `monitorEvents()` API de [utilidades de consola][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="66fd3-108">For the reference on functions like `monitorEvents()` see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="66fd3-109">Abrir la consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-109">Open the Console</span></span>   

<span data-ttu-id="66fd3-110">Puede abrir la consola como un [Panel](#open-the-console-panel) o como una [pestaña en el cajón](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="66fd3-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="66fd3-111">Abrir el panel de consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-111">Open the Console panel</span></span>   

<span data-ttu-id="66fd3-112">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="66fd3-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

> ##### <span data-ttu-id="66fd3-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="66fd3-113">Figure 1</span></span>  
> <span data-ttu-id="66fd3-114">Panel de consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-114">The Console panel</span></span>  
> ![Panel de consola][ImageConsolePanel]  

<span data-ttu-id="66fd3-116">Para abrir el panel de consola desde el [menú de comandos][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **Panel** al lado.</span><span class="sxs-lookup"><span data-stu-id="66fd3-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

> ##### <span data-ttu-id="66fd3-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="66fd3-117">Figure 2</span></span>  
> <span data-ttu-id="66fd3-118">Comando para mostrar el panel de consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-118">The command for showing the Console panel</span></span>  
> ![Comando para mostrar el panel de consola][ImageCommandShowConsole]  

### <span data-ttu-id="66fd3-120">Abrir la pestaña consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="66fd3-120">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="66fd3-121">Pulse `Escape` o haga clic en **personalizar y controlar DevTools** `...` y, a continuación, seleccione **Mostrar cajón de consola**.</span><span class="sxs-lookup"><span data-stu-id="66fd3-121">Press `Escape` or click **Customize And Control DevTools** `...` and then select **Show console drawer**.</span></span>  

> ##### <span data-ttu-id="66fd3-122">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="66fd3-122">Figure 3</span></span>  
> <span data-ttu-id="66fd3-123">Mostrar cajón de consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-123">Show console drawer</span></span>  
> ![Mostrar cajón de consola][ImageShowConsoleDrawer]  

<span data-ttu-id="66fd3-125">El cajón aparece en la parte inferior de la ventana de DevTools, con la pestaña **consola** abierto.</span><span class="sxs-lookup"><span data-stu-id="66fd3-125">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

> ##### <span data-ttu-id="66fd3-126">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="66fd3-126">Figure 4</span></span>  
> <span data-ttu-id="66fd3-127">Ficha de consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="66fd3-127">The Console tab in the Drawer</span></span>  
> ![Ficha de consola en el cajón][ImageDrawerConsole]  

<span data-ttu-id="66fd3-129">Para abrir la pestaña consola desde el [menú comando][DevToolsCommandMenu], empiece a escribir `Console` y, a continuación, ejecute el comando **Mostrar consola** que tiene el distintivo del **alimentador** al lado.</span><span class="sxs-lookup"><span data-stu-id="66fd3-129">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

> ##### <span data-ttu-id="66fd3-130">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="66fd3-130">Figure 5</span></span>  
> <span data-ttu-id="66fd3-131">Comando para mostrar la ficha de consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="66fd3-131">The command for showing the Console tab in the Drawer</span></span>  
> ![Comando para mostrar la ficha de consola en el cajón][ImageShowDrawerCommand]  

### <span data-ttu-id="66fd3-133">Abrir configuración de consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-133">Open Console Settings</span></span>   

<span data-ttu-id="66fd3-134">Haga clic en configuración de consola de **configuración** ![ ][ImageSettingsButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="66fd3-134">Click **Console Settings** ![Console Settings][ImageSettingsButtonIcon].</span></span>  

> ##### <span data-ttu-id="66fd3-135">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="66fd3-135">Figure 6</span></span>  
> <span data-ttu-id="66fd3-136">Configuración de la consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-136">Console Settings</span></span>  
> ![Configuración de la consola][ImageConsoleSettings]  

<span data-ttu-id="66fd3-138">Los vínculos siguientes explican cada configuración:</span><span class="sxs-lookup"><span data-stu-id="66fd3-138">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="66fd3-139">Ocultar red</span><span class="sxs-lookup"><span data-stu-id="66fd3-139">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="66fd3-140">Conservar registro</span><span class="sxs-lookup"><span data-stu-id="66fd3-140">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="66fd3-141">Solo el contexto seleccionado</span><span class="sxs-lookup"><span data-stu-id="66fd3-141">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="66fd3-142">Grupo similar</span><span class="sxs-lookup"><span data-stu-id="66fd3-142">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="66fd3-143">Registro XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="66fd3-143">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="66fd3-144">Evaluación diligente</span><span class="sxs-lookup"><span data-stu-id="66fd3-144">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="66fd3-145">Autocompletar desde historial</span><span class="sxs-lookup"><span data-stu-id="66fd3-145">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  

### <span data-ttu-id="66fd3-146">Abrir la barra lateral de la consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-146">Open the Console Sidebar</span></span>   

<span data-ttu-id="66fd3-147">Haga clic en **Mostrar** la barra lateral de consola para mostrar la barra lateral ![ ][ImageShowConsoleSidebarIcon] , que es útil para filtrar.</span><span class="sxs-lookup"><span data-stu-id="66fd3-147">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon] to show the Sidebar, which is useful for filtering.</span></span>  

> ##### <span data-ttu-id="66fd3-148">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="66fd3-148">Figure 7</span></span>  
> <span data-ttu-id="66fd3-149">Barra lateral de la consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-149">Console Sidebar</span></span>  
> ![Barra lateral de la consola][ImageConsoleSidebar]  

## <span data-ttu-id="66fd3-151">Ver mensajes</span><span class="sxs-lookup"><span data-stu-id="66fd3-151">View messages</span></span>   

<span data-ttu-id="66fd3-152">Esta sección contiene características que cambian la presentación de los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-152">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="66fd3-153">Vea [Ver mensajes][DevToolsConsoleViewMessages] para obtener un tutorial práctico.</span><span class="sxs-lookup"><span data-stu-id="66fd3-153">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="66fd3-154">Deshabilitar la agrupación de mensajes</span><span class="sxs-lookup"><span data-stu-id="66fd3-154">Disable message grouping</span></span>   

<span data-ttu-id="66fd3-155">[Abra configuración de consola](#open-console-settings) y deshabilite **grupo similar** para deshabilitar el comportamiento predeterminado de agrupación de mensajes de la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-155">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="66fd3-156">Para obtener un ejemplo [, consulta log XHR y solicitudes fetch](#log-xhr-and-fetch-requests) .</span><span class="sxs-lookup"><span data-stu-id="66fd3-156">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="66fd3-157">Registrar solicitudes de XHR y fetch</span><span class="sxs-lookup"><span data-stu-id="66fd3-157">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="66fd3-158">[Abra configuración de consola](#open-console-settings) y habilite **log XMLHttpRequests** para registrar todas las `XMLHttpRequest` solicitudes de `Fetch` la consola a medida que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="66fd3-158">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

> ##### <span data-ttu-id="66fd3-159">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="66fd3-159">Figure 8</span></span>  
> <span data-ttu-id="66fd3-160">Registro `XMLHttpRequest` y `Fetch` solicitudes</span><span class="sxs-lookup"><span data-stu-id="66fd3-160">Logging `XMLHttpRequest` and `Fetch` requests</span></span>  
> ![Registro de solicitudes de XMLHttpRequest y fetch][ImageXhrGrouped]  

<span data-ttu-id="66fd3-162">El mensaje superior de la [ilustración 8](#figure-8) muestra el comportamiento de agrupación predeterminado de la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-162">The top message in [Figure 8](#figure-8) shows the default grouping behavior of the Console.</span></span>  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="66fd3-163">Conservar mensajes en la carga de la página</span><span class="sxs-lookup"><span data-stu-id="66fd3-163">Persist messages across page loads</span></span>   

<span data-ttu-id="66fd3-164">De forma predeterminada, la consola se desactiva cada vez que se carga una página nueva.</span><span class="sxs-lookup"><span data-stu-id="66fd3-164">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="66fd3-165">Para conservar los mensajes en la carga de la página, [abra configuración de consola](#open-console-settings) y active la casilla **conservar registro** .</span><span class="sxs-lookup"><span data-stu-id="66fd3-165">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="66fd3-166">Ocultar mensajes de red</span><span class="sxs-lookup"><span data-stu-id="66fd3-166">Hide network messages</span></span>   

<span data-ttu-id="66fd3-167">De forma predeterminada, el explorador registra los mensajes de red en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="66fd3-167">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="66fd3-168">Por ejemplo, el mensaje seleccionado en la [figura 9](#figure-9) representa un código de estado de `429` .</span><span class="sxs-lookup"><span data-stu-id="66fd3-168">For example, the selected message in [Figure 9](#figure-9) represents a status code of `429`.</span></span>  

> ##### <span data-ttu-id="66fd3-169">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="66fd3-169">Figure 9</span></span>  
> <span data-ttu-id="66fd3-170">Un mensaje de 429 en la consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-170">A 429 message in the Console</span></span>  
> <span data-ttu-id="66fd3-171">! [Un mensaje de 429 en la consola] [Image429Message]</span><span class="sxs-lookup"><span data-stu-id="66fd3-171">![A 429 message in the Console][Image429Message]</span></span>  

<span data-ttu-id="66fd3-172">Para ocultar mensajes de red:</span><span class="sxs-lookup"><span data-stu-id="66fd3-172">To hide network messages:</span></span>  

1.  <span data-ttu-id="66fd3-173">[Abra configuración de consola](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="66fd3-173">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="66fd3-174">Active la casilla **ocultar red** .</span><span class="sxs-lookup"><span data-stu-id="66fd3-174">Enable the **Hide Network** checkbox.</span></span>  

## <span data-ttu-id="66fd3-175">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="66fd3-175">Filter messages</span></span>   

<span data-ttu-id="66fd3-176">Existen muchas maneras de filtrar los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-176">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="66fd3-177">Filtrar los mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="66fd3-177">Filter out browser messages</span></span>   

<span data-ttu-id="66fd3-178">[Abra la barra lateral](#open-the-console-sidebar) de la consola y haga clic en **mensajes de usuario** para mostrar solo los mensajes que proceden del JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="66fd3-178">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

> ##### <span data-ttu-id="66fd3-179">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="66fd3-179">Figure 10</span></span>  
> <span data-ttu-id="66fd3-180">Ver mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="66fd3-180">Viewing user messages</span></span>  
> <span data-ttu-id="66fd3-181">! [Visualización de mensajes de usuario] [ImageUserMessages]</span><span class="sxs-lookup"><span data-stu-id="66fd3-181">![Viewing user messages][ImageUserMessages]</span></span>  

### <span data-ttu-id="66fd3-182">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="66fd3-182">Filter by log level</span></span>   

<span data-ttu-id="66fd3-183">DevTools asigna cada `console.*` método a nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="66fd3-183">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="66fd3-184">Hay 4 niveles: `Verbose` ,, `Info` `Warning` y `Error` .</span><span class="sxs-lookup"><span data-stu-id="66fd3-184">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="66fd3-185">Por ejemplo, `console.log()` se encuentra en el `Info` grupo, mientras que `console.error()` se encuentra en el `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="66fd3-185">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="66fd3-186">La [referencia][DevToolsConsoleApi] de la API de consola describe el nivel de gravedad de cada método aplicable.</span><span class="sxs-lookup"><span data-stu-id="66fd3-186">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="66fd3-187">Cada mensaje que el explorador registra en la consola también tiene un nivel de gravedad.</span><span class="sxs-lookup"><span data-stu-id="66fd3-187">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="66fd3-188">Puede ocultar cualquier nivel de mensajes que no le interese.</span><span class="sxs-lookup"><span data-stu-id="66fd3-188">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="66fd3-189">Por ejemplo, si solo le interesan `Error` los mensajes, puede ocultar los otros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="66fd3-189">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="66fd3-190">Haga clic en el menú desplegable **niveles de registro** para habilitar o deshabilitar `Verbose` , `Info` `Warning` o `Error` mensajes.</span><span class="sxs-lookup"><span data-stu-id="66fd3-190">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

> ##### <span data-ttu-id="66fd3-191">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="66fd3-191">Figure 11</span></span>  
> <span data-ttu-id="66fd3-192">Lista desplegable de **niveles de registro**</span><span class="sxs-lookup"><span data-stu-id="66fd3-192">The **Log Levels** dropdown</span></span>  
> <span data-ttu-id="66fd3-193">! [La lista desplegable de niveles de registro] [ImageLogLevels]</span><span class="sxs-lookup"><span data-stu-id="66fd3-193">![The Log Levels dropdown][ImageLogLevels]</span></span>  

<span data-ttu-id="66fd3-194">También puede filtrar por nivel de registro si [abre la barra lateral de la consola](#open-the-console-sidebar) y hace clic en **errores**, **advertencias**, **información**o **detallado**.</span><span class="sxs-lookup"><span data-stu-id="66fd3-194">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

> ##### <span data-ttu-id="66fd3-195">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="66fd3-195">Figure 12</span></span>  
> <span data-ttu-id="66fd3-196">Uso de la barra lateral para ver las advertencias</span><span class="sxs-lookup"><span data-stu-id="66fd3-196">Using the Sidebar to view warnings</span></span>  
> <span data-ttu-id="66fd3-197">! [Uso de la barra lateral para ver las advertencias] [ImageSidebarWarnings]</span><span class="sxs-lookup"><span data-stu-id="66fd3-197">![Using the Sidebar to view warnings][ImageSidebarWarnings]</span></span>  

### <span data-ttu-id="66fd3-198">Filtrar mensajes por dirección URL</span><span class="sxs-lookup"><span data-stu-id="66fd3-198">Filter messages by URL</span></span>   

<span data-ttu-id="66fd3-199">Escriba `url:` seguido de una dirección URL para ver solo los mensajes que proceden de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="66fd3-199">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="66fd3-200">Después de escribir `url:` DevTools, se muestran todas las direcciones URL relevantes.</span><span class="sxs-lookup"><span data-stu-id="66fd3-200">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="66fd3-201">Los dominios también funcionan.</span><span class="sxs-lookup"><span data-stu-id="66fd3-201">Domains also work.</span></span>  <span data-ttu-id="66fd3-202">Por ejemplo, si `https://example.com/a.js` y `https://example.com/b.js` están registrando mensajes, `url:https://example.com` le permite centrarse en los mensajes de estas dos secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="66fd3-202">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

> ##### <span data-ttu-id="66fd3-203">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="66fd3-203">Figure 13</span></span>  
> <span data-ttu-id="66fd3-204">Un filtro de URL</span><span class="sxs-lookup"><span data-stu-id="66fd3-204">A URL filter</span></span>  
> <span data-ttu-id="66fd3-205">! [Un filtro de URL] [ImageUrlFilter]</span><span class="sxs-lookup"><span data-stu-id="66fd3-205">![A URL filter][ImageUrlFilter]</span></span>  

<span data-ttu-id="66fd3-206">Escriba `-url:` para ocultar mensajes de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="66fd3-206">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="66fd3-207">Esto se conoce como un filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="66fd3-207">This is called a negative URL filter.</span></span>  

> ##### <span data-ttu-id="66fd3-208">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="66fd3-208">Figure 14</span></span>  
> <span data-ttu-id="66fd3-209">Filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la dirección URL</span><span class="sxs-lookup"><span data-stu-id="66fd3-209">A negative URL filter that hides all messages matching the URL</span></span> `https://b.wal.co`  
> <span data-ttu-id="66fd3-210">! [Un filtro de URL negativo que oculta todos los mensajes que coinciden con la URL https://b.wal.co ] [ImageNegativeUrlFilter1]</span><span class="sxs-lookup"><span data-stu-id="66fd3-210">![A negative URL filter that hides all messages matching the URL https://b.wal.co][ImageNegativeUrlFilter1]</span></span>  

<span data-ttu-id="66fd3-211">También puede mostrar los mensajes de una sola dirección URL [abriendo la barra lateral](#open-the-console-sidebar)de la consola, expandiendo la sección de **mensajes de usuario** y, a continuación, haciendo clic en la dirección URL de la secuencia de comandos que contiene los mensajes en los que desea concentrarse.</span><span class="sxs-lookup"><span data-stu-id="66fd3-211">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

> ##### <span data-ttu-id="66fd3-212">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="66fd3-212">Figure 15</span></span>  
> <span data-ttu-id="66fd3-213">Ver los mensajes procedentes de</span><span class="sxs-lookup"><span data-stu-id="66fd3-213">Viewing the messages that came from</span></span> `wp-ad.min.js`  
> <span data-ttu-id="66fd3-214">! [Viendo los mensajes que proceden de WP-ad. min. js] [ImageNegativeUrlFilter2]</span><span class="sxs-lookup"><span data-stu-id="66fd3-214">![Viewing the messages that came from wp-ad.min.js][ImageNegativeUrlFilter2]</span></span>  

### <span data-ttu-id="66fd3-215">Filtrar mensajes de distintos contextos</span><span class="sxs-lookup"><span data-stu-id="66fd3-215">Filter out messages from different contexts</span></span>   

<span data-ttu-id="66fd3-216">Supongamos que tiene un anuncio \ (ad \) en la página.</span><span class="sxs-lookup"><span data-stu-id="66fd3-216">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="66fd3-217">El anuncio está insertado en una `<iframe>` y está generando un gran número de mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-217">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="66fd3-218">Como AD se está ejecutando en un [contexto de JavaScript](#select-javascript-context)diferente, una forma de ocultar los mensajes es [abrir la configuración de consola](#open-console-settings) y habilitar la casilla de verificación de solo el **contexto seleccionado** .</span><span class="sxs-lookup"><span data-stu-id="66fd3-218">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="66fd3-219">Filtrar mensajes que no coincidan con un modelo de expresión regular</span><span class="sxs-lookup"><span data-stu-id="66fd3-219">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="66fd3-220">Escriba una expresión regular, como `/[gm][ta][mi]/` en el cuadro de texto **filtro** , para filtrar los mensajes que no coincidan con ese patrón.</span><span class="sxs-lookup"><span data-stu-id="66fd3-220">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="66fd3-221">DevTools comprueba si el patrón se encuentra en el texto del mensaje o en la secuencia de comandos que ha provocado el registro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="66fd3-221">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

> ##### <span data-ttu-id="66fd3-222">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="66fd3-222">Figure 16</span></span>  
> <span data-ttu-id="66fd3-223">Filtrar los mensajes que no coincidan</span><span class="sxs-lookup"><span data-stu-id="66fd3-223">Filtering out any messages that do not match</span></span> `/[gm][ta][mi]/`  
> <span data-ttu-id="66fd3-224">! [Filtrar los mensajes que no coincidan con la expresión regex] [ImageRegExFilter]</span><span class="sxs-lookup"><span data-stu-id="66fd3-224">![Filtering out any messages that do not match regex expression][ImageRegExFilter]</span></span>  

## <span data-ttu-id="66fd3-225">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="66fd3-225">Run JavaScript</span></span>   

<span data-ttu-id="66fd3-226">Esta sección contiene características relacionadas con la ejecución de JavaScript en la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-226">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="66fd3-227">Consulte [ejecutar JavaScript][DevToolsConsoleOverviewJavascript] para obtener un tutorial práctico.</span><span class="sxs-lookup"><span data-stu-id="66fd3-227">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="66fd3-228">Volver a ejecutar expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="66fd3-228">Re-run expressions from history</span></span>   

<span data-ttu-id="66fd3-229">Presione la `Up Arrow` tecla para recorrer el historial de expresiones de JavaScript que ejecutó anteriormente en la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-229">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="66fd3-230">Pulse `Enter` para volver a ejecutar la expresión.</span><span class="sxs-lookup"><span data-stu-id="66fd3-230">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="66fd3-231">Ver el valor de una expresión en tiempo real con expresiones en directo</span><span class="sxs-lookup"><span data-stu-id="66fd3-231">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="66fd3-232">Si se encuentra escribiendo la misma expresión de JavaScript en la consola varias veces, es posible que le resulte más fácil crear una **expresión en vivo**.</span><span class="sxs-lookup"><span data-stu-id="66fd3-232">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="66fd3-233">Con **expresiones en vivo** , escriba una expresión una vez y, a continuación, ancle en la parte superior de la consola.</span><span class="sxs-lookup"><span data-stu-id="66fd3-233">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="66fd3-234">El valor de la expresión se actualiza casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="66fd3-234">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="66fd3-235">Vea [inspeccionar valores de expresiones de JavaScript en tiempo real con expresiones en directo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="66fd3-235">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="66fd3-236">Deshabilitar evaluación diligente</span><span class="sxs-lookup"><span data-stu-id="66fd3-236">Disable Eager Evaluation</span></span>   

<span data-ttu-id="66fd3-237">Mientras escribe las expresiones de JavaScript en la consola, **evaluación diligente** muestra una vista previa del valor devuelto para esa expresión.</span><span class="sxs-lookup"><span data-stu-id="66fd3-237">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="66fd3-238">[Abra configuración de consola](#open-console-settings) y deshabilite la casilla **evaluación diligente** para desactivar las vistas previas de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="66fd3-238">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="66fd3-239">Deshabilitar Autocompletar desde historial</span><span class="sxs-lookup"><span data-stu-id="66fd3-239">Disable autocomplete from history</span></span>   

<span data-ttu-id="66fd3-240">A medida que escribe una expresión, la ventana emergente de autocompletar de la consola muestra expresiones que ejecutó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="66fd3-240">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="66fd3-241">Estas expresiones van precedidas del `>` carácter.</span><span class="sxs-lookup"><span data-stu-id="66fd3-241">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="66fd3-242">[Abra configuración de consola](#open-console-settings) y deshabilite la casilla **Autocompletar del historial** para dejar de mostrar las expresiones de su historial.</span><span class="sxs-lookup"><span data-stu-id="66fd3-242">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="66fd3-243">En la [figura 17](#figure-17), `document.querySelector('a')` y `document.querySelector('img')` son expresiones que se han evaluado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="66fd3-243">In [Figure 17](#figure-17), `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

> ##### <span data-ttu-id="66fd3-244">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="66fd3-244">Figure 17</span></span>  
> <span data-ttu-id="66fd3-245">Elemento emergente de autocompletar que muestra expresiones del historial</span><span class="sxs-lookup"><span data-stu-id="66fd3-245">The autocomplete popup showing expressions from history</span></span>  
> <span data-ttu-id="66fd3-246">! [El elemento emergente de Autocompletar muestra expresiones del historial] [ImageHistoryAutocomplete]</span><span class="sxs-lookup"><span data-stu-id="66fd3-246">![The autocomplete popup showing expressions from history][ImageHistoryAutocomplete]</span></span>  

### <span data-ttu-id="66fd3-247">Seleccionar contexto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="66fd3-247">Select JavaScript context</span></span>   

<span data-ttu-id="66fd3-248">De forma predeterminada, la lista desplegable de **contexto de JavaScript** se establece en **Top**, que representa el [contexto de exploración][MDNBrowsingContext] del documento principal.</span><span class="sxs-lookup"><span data-stu-id="66fd3-248">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

> ##### <span data-ttu-id="66fd3-249">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="66fd3-249">Figure 18</span></span>  
> <span data-ttu-id="66fd3-250">Lista desplegable de **contexto de JavaScript**</span><span class="sxs-lookup"><span data-stu-id="66fd3-250">The **JavaScript Context** dropdown</span></span>  
> <span data-ttu-id="66fd3-251">! [La lista desplegable de contexto de JavaScript] [ImageJavascriptContext]</span><span class="sxs-lookup"><span data-stu-id="66fd3-251">![The JavaScript Context dropdown][ImageJavascriptContext]</span></span>  

<span data-ttu-id="66fd3-252">Supongamos que tiene un anuncio en la página insertado en una `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="66fd3-252">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="66fd3-253">Para poder ajustar el DOM del anuncio, deseas ejecutar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66fd3-253">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="66fd3-254">En primer lugar, debe seleccionar el contexto de exploración del anuncio en la lista desplegable de **contexto de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="66fd3-254">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

> ##### <span data-ttu-id="66fd3-255">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="66fd3-255">Figure 19</span></span>  
> <span data-ttu-id="66fd3-256">Selección de un contexto de JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="66fd3-256">Selecting a different JavaScript context</span></span>  
> <span data-ttu-id="66fd3-257">! [Seleccionando un contexto de JavaScript diferente] [ImageSelectContext]</span><span class="sxs-lookup"><span data-stu-id="66fd3-257">![Selecting a different JavaScript context][ImageSelectContext]</span></span>  

## <span data-ttu-id="66fd3-258">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="66fd3-258">Clear the Console</span></span>   

<span data-ttu-id="66fd3-259">Puede usar cualquiera de los siguientes flujos de trabajo para borrar la consola:</span><span class="sxs-lookup"><span data-stu-id="66fd3-259">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="66fd3-260">Haga clic en **Borrar** consola ![ Borrar consola ][ImageClearConsoleIcon] .</span><span class="sxs-lookup"><span data-stu-id="66fd3-260">Click **Clear Console** ![Clear Console][ImageClearConsoleIcon].</span></span>  
*   <span data-ttu-id="66fd3-261">Haga clic con el botón derecho en un mensaje y seleccione **Borrar consola**.</span><span class="sxs-lookup"><span data-stu-id="66fd3-261">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="66fd3-262">Escriba `clear()` la consola y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="66fd3-262">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="66fd3-263">Llama `console.clear()` desde el JavaScript de tu página web.</span><span class="sxs-lookup"><span data-stu-id="66fd3-263">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="66fd3-264">Pulsa `Control` + `L` mientras la consola está en el foco.</span><span class="sxs-lookup"><span data-stu-id="66fd3-264">Press `Control`+`L` while the Console is in focus.</span></span>  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Ilustración 1: panel de consola"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Ilustración 2: el comando para mostrar el panel de la consola"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Ilustración 3: mostrar el cajón de consola"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Ilustración 4: la pestaña de consola en el cajón"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Ilustración 5: el comando para mostrar la pestaña de consola en el cajón"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Ilustración 6: configuración de la consola"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Ilustración 7: barra lateral de la consola"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Ilustración 8: registro de solicitudes de XMLHttpRequest y fetch"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Show-Network.msft.png "Ilustración 9: un mensaje de 429 en la consola"  
[ImageUserMessages]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-Drawer-User-messages.msft.png "Ilustración 10: ver mensajes de usuario"  
[ImageLogLevels]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-LEVEL-default-levels.msft.png "ilustración 11: la lista desplegable de niveles de registro"  
[ImageSidebarWarnings]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-Warnings.msft.png "Ilustración 12: usar la barra lateral para ver las advertencias"  
[ImageUrlFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Text.msft.png "ilustración 13: un filtro de dirección URL"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-negative-Filter-Text.msft.png "Ilustración 14: un filtro de dirección URL negativo que oculta todos los mensajes que coinciden con la dirección URL https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Text-Specified.msft.png "Ilustración 15: ver los mensajes procedentes de WP-ad. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Regex.msft.png "Ilustración 16: filtrar los mensajes que no coincidan con la expresión regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Filter-Text-AutoFilter-History.msft.png "Ilustración 17: el elemento emergente de Autocompletar muestra las expresiones del historial"  
[ImageJavascriptContext]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-DOM-Level-Top.msft.png "ilustración 18: la lista desplegable de contexto de JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-DOM-Level-Multiple.msft.png "Ilustración 19: seleccionar un contexto de JavaScript diferente"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Ver mensajes registrados-Descripción general de la consola"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Ejecución de JavaScript-Introducción a la consola"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Introducción a la ejecución de JavaScript en la consola"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de API de utilidades de consola"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de exploración | MDN"  

> [!NOTE]
> <span data-ttu-id="66fd3-293">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="66fd3-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="66fd3-294">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="66fd3-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="66fd3-296">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="66fd3-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
