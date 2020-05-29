---
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581820"
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





# <span data-ttu-id="23a3b-103">Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="23a3b-103">Run Snippets Of JavaScript On Any Page With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="23a3b-104">Si tienes que ejecutar el mismo código de forma repetida en la [consola][DevtoolsConsoleIndex] , considera la posibilidad de guardar el código como un fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="23a3b-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="23a3b-105">Los fragmentos de código son scripts que se crean en el [panel **fuentes** ][DevToolsSourcesPanel].</span><span class="sxs-lookup"><span data-stu-id="23a3b-105">Snippets are scripts that you author in the [**Sources** panel][DevToolsSourcesPanel].</span></span>  <span data-ttu-id="23a3b-106">Tienen acceso al contexto de JavaScript de la página y puede ejecutarlos en cualquier página.</span><span class="sxs-lookup"><span data-stu-id="23a3b-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="23a3b-107">Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="23a3b-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="23a3b-108">Firefox DevTools tiene una característica similar a la de los fragmentos de código denominado [Bloc][MDNScratchpad]dedo.</span><span class="sxs-lookup"><span data-stu-id="23a3b-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="23a3b-109">Por ejemplo, la [**figura 1**](#figure-1) muestra la página de inicio de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.</span><span class="sxs-lookup"><span data-stu-id="23a3b-109">For example, [**Figure 1**](#figure-1) shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

> ##### <span data-ttu-id="23a3b-110">Figura 1</span><span class="sxs-lookup"><span data-stu-id="23a3b-110">Figure 1</span></span>  
> <span data-ttu-id="23a3b-111">Aspecto de la página antes de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-111">How the page looks before running the Snippet</span></span>  
> ![Aspecto de la página antes de ejecutar el fragmento de código][ImageSnippetSplitScreen]  

<span data-ttu-id="23a3b-113">El código fuente del fragmento de código de la [**Ilustración 1**](#figure-1):</span><span class="sxs-lookup"><span data-stu-id="23a3b-113">The Snippet source code from [**Figure 1**](#figure-1):</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="23a3b-114">La [**ilustración 2**](#figure-2) muestra el aspecto que tendrá la página después de ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="23a3b-114">[**Figure 2**](#figure-2) shows how the page looks after running the Snippet.</span></span>  <span data-ttu-id="23a3b-115">El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el recorte y el contenido de la página cambian por completo.</span><span class="sxs-lookup"><span data-stu-id="23a3b-115">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

> ##### <span data-ttu-id="23a3b-116">Figura 2</span><span class="sxs-lookup"><span data-stu-id="23a3b-116">Figure 2</span></span>  
> <span data-ttu-id="23a3b-117">Aspecto de la página después de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-117">How the page looks after running the Snippet</span></span>  
> ![Aspecto de la página después de ejecutar el fragmento de código][ImageSnippetSplitScreenAfter]  

## <span data-ttu-id="23a3b-119">Abrir el panel de fragmentos</span><span class="sxs-lookup"><span data-stu-id="23a3b-119">Open the Snippets pane</span></span>   

<span data-ttu-id="23a3b-120">El panel de **fragmentos de código** muestra los fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="23a3b-120">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="23a3b-121">Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="23a3b-121">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

> ##### <span data-ttu-id="23a3b-122">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="23a3b-122">Figure 3</span></span>  
> <span data-ttu-id="23a3b-123">El panel de **fragmentos**</span><span class="sxs-lookup"><span data-stu-id="23a3b-123">The **Snippets** pane</span></span>  
> ![El panel de fragmentos][ImageSnippetsPane]  

### <span data-ttu-id="23a3b-125">Abrir el panel de fragmentos de código con un mouse</span><span class="sxs-lookup"><span data-stu-id="23a3b-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="23a3b-126">Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="23a3b-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="23a3b-127">El panel de **páginas** suele abrirse de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="23a3b-127">The **Page** pane usually opens by default.</span></span>  

    > ##### <span data-ttu-id="23a3b-128">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="23a3b-128">Figure 4</span></span>  
    > <span data-ttu-id="23a3b-129">Panel **orígenes** con el panel de **páginas** abierto a la izquierda</span><span class="sxs-lookup"><span data-stu-id="23a3b-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    > ![Panel orígenes con el panel de páginas abierto a la izquierda][ImageSourcesPageEmpty]  

1.  <span data-ttu-id="23a3b-131">Haga clic en la pestaña **fragmentos** para abrir el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="23a3b-131">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="23a3b-132">Es posible que tenga que hacer clic en **más pestañas** ![ más pestañas ][ImageMoreTabsIcon] para acceder a la opción **fragmentos** .</span><span class="sxs-lookup"><span data-stu-id="23a3b-132">You might need to click **More Tabs** ![More Tabs][ImageMoreTabsIcon] in order to access the **Snippets** option.</span></span>  

### <span data-ttu-id="23a3b-133">Abrir el panel de fragmentos de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="23a3b-133">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="23a3b-134">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="23a3b-134">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="23a3b-135">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="23a3b-135">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="23a3b-136">Comience `Snippets` a escribir, seleccione **Mostrar fragmentos**y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="23a3b-136">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="23a3b-137">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="23a3b-137">Figure 5</span></span>  
    > <span data-ttu-id="23a3b-138">El comando **Mostrar fragmentos**</span><span class="sxs-lookup"><span data-stu-id="23a3b-138">The **Show Snippets** command</span></span>  
    > ![El comando Mostrar fragmentos][ImageShowSnippetsSearch]  

## <span data-ttu-id="23a3b-140">Crear fragmentos</span><span class="sxs-lookup"><span data-stu-id="23a3b-140">Create Snippets</span></span>   

### <span data-ttu-id="23a3b-141">Crear un fragmento de código a través del panel orígenes</span><span class="sxs-lookup"><span data-stu-id="23a3b-141">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="23a3b-142">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="23a3b-142">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="23a3b-143">Haga clic en **nuevo fragmento de código**.</span><span class="sxs-lookup"><span data-stu-id="23a3b-143">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="23a3b-144">Escriba un nombre para el fragmento de código y, a continuación, presione `Enter` para guardar.</span><span class="sxs-lookup"><span data-stu-id="23a3b-144">Enter a name for your Snippet then press `Enter` to save.</span></span>  

    > ##### <span data-ttu-id="23a3b-145">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="23a3b-145">Figure 6</span></span>  
    > <span data-ttu-id="23a3b-146">Asignar un nombre a un fragmento</span><span class="sxs-lookup"><span data-stu-id="23a3b-146">Naming a Snippet</span></span>  
    > ![Asignar un nombre a un fragmento][ImageSnippetName]  

### <span data-ttu-id="23a3b-148">Crear un fragmento de código mediante el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="23a3b-148">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="23a3b-149">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="23a3b-149">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="23a3b-150">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="23a3b-150">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="23a3b-151">Comience `Snippet` a escribir, seleccione **crear nuevo fragmento**y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="23a3b-151">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="23a3b-152">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="23a3b-152">Figure 7</span></span>  
    > <span data-ttu-id="23a3b-153">Comando para crear un nuevo fragmento de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-153">The command for creating a new Snippet</span></span>  
    > ![Comando para crear un nuevo fragmento de código][ImageCreateSnippetSearch]  

<span data-ttu-id="23a3b-155">Consulte cambiar [el nombre](#rename-snippets) de los fragmentos de código si desea asignar un nombre personalizado al nuevo fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="23a3b-155">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="23a3b-156">Editar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-156">Edit Snippets</span></span>   

1.  <span data-ttu-id="23a3b-157">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="23a3b-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="23a3b-158">En el panel **fragmentos** de código, haga clic en el nombre del fragmento de código que desea editar para abrirlo en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="23a3b-158">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  

    > ##### <span data-ttu-id="23a3b-159">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="23a3b-159">Figure 8</span></span>  
    > <span data-ttu-id="23a3b-160">El editor de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-160">The Code Editor</span></span>  
    > ![El editor de código][ImageSnippetEditor]  

1.  <span data-ttu-id="23a3b-162">Use el **Editor de código** para agregar JavaScript al fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="23a3b-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="23a3b-163">Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado.</span><span class="sxs-lookup"><span data-stu-id="23a3b-163">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="23a3b-164">Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.</span><span class="sxs-lookup"><span data-stu-id="23a3b-164">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  

    > ##### <span data-ttu-id="23a3b-165">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="23a3b-165">Figure 9</span></span>  
    > <span data-ttu-id="23a3b-166">Un asterisco junto al nombre del fragmento de código, que indica código no guardado</span><span class="sxs-lookup"><span data-stu-id="23a3b-166">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    > ![Un asterisco junto al nombre del fragmento de código, que indica código no guardado][ImageUnsavedSnippet]  

## <span data-ttu-id="23a3b-168">Ejecutar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-168">Run Snippets</span></span>   

### <span data-ttu-id="23a3b-169">Ejecutar un recorte desde el panel fuentes</span><span class="sxs-lookup"><span data-stu-id="23a3b-169">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="23a3b-170">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="23a3b-170">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="23a3b-171">Haga clic en el nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="23a3b-171">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="23a3b-172">El fragmento de código se abre en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="23a3b-172">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="23a3b-173">Haga clic en **Ejecutar** ![ fragmento ][ImageRunSnippetIcon] de código de ejecución o pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="23a3b-173">Click **Run Snippet** ![Run Snippet][ImageRunSnippetIcon], or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  

### <span data-ttu-id="23a3b-174">Ejecutar un fragmento de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="23a3b-174">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="23a3b-175">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="23a3b-175">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="23a3b-176">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="23a3b-176">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="23a3b-177">Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="23a3b-177">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  

    > ##### <span data-ttu-id="23a3b-178">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="23a3b-178">Figure 10</span></span>  
    > <span data-ttu-id="23a3b-179">Ejecución de un fragmento de código desde el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="23a3b-179">Running a Snippet from the Command Menu</span></span>  
    > ![Ejecución de un fragmento de código desde el menú de comandos][ImageRunSnippetCommand]  

1.  <span data-ttu-id="23a3b-181">Pulse `Enter` para ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="23a3b-181">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="23a3b-182">Cambiar el nombre de los fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-182">Rename Snippets</span></span>   

1.  <span data-ttu-id="23a3b-183">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="23a3b-183">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="23a3b-184">Haga clic con el botón derecho en el nombre del fragmento y seleccione cambiar **nombre**.</span><span class="sxs-lookup"><span data-stu-id="23a3b-184">Right-click the Snippet name and select **Rename**.</span></span>  

## <span data-ttu-id="23a3b-185">Eliminar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="23a3b-185">Delete Snippets</span></span>   

1.  <span data-ttu-id="23a3b-186">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="23a3b-186">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="23a3b-187">Haga clic con el botón derecho en el nombre del fragmento y seleccione **quitar**.</span><span class="sxs-lookup"><span data-stu-id="23a3b-187">Right-click the Snippet name and select **Remove**.</span></span>  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Ilustración 1: aspecto de la página antes de ejecutar el fragmento de código"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Ilustración 2: el aspecto de la página después de ejecutar el fragmento de código"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Ilustración 3: el panel de fragmentos de código"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Ilustración 4: el panel orígenes con el panel de páginas abierto a la izquierda"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Ilustración 5: el comando Mostrar fragmentos"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Ilustración 6: asignar un nombre a un fragmento de código"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Ilustración 7: el comando para crear un nuevo fragmento de código"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Ilustración 8: el editor de código"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Ilustración 9: un asterisco junto al nombre del fragmento de código, que indica que el código no se ha guardado"  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Ilustración 10: ejecutar un recorte desde el menú de comandos"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola"  
[DevToolsSourcesPanel]: ../sources.md "Información general del panel orígenes"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet, Wikipedia"  

> [!NOTE]
> <span data-ttu-id="23a3b-202">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="23a3b-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="23a3b-203">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="23a3b-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="23a3b-205">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="23a3b-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
