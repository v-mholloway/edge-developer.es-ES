---
description: Los fragmentos de código son pequeños scripts que puede crear y ejecutar en el panel orígenes de Microsoft Edge DevTools.  Puede acceder a ellos desde cualquier página y ejecutarlos.  Cuando se ejecuta un fragmento de código, se ejecuta desde el contexto de la página abierta en ese momento.
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124743"
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

# <span data-ttu-id="7b884-106">Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7b884-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7b884-107">Si tienes que ejecutar el mismo código de forma repetida en la [consola][DevtoolsConsoleIndex] , considera la posibilidad de guardar el código como un fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="7b884-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="7b884-108">Los fragmentos de código son scripts que se crean en el panel [fuentes][DevToolsSourcesPanel] .</span><span class="sxs-lookup"><span data-stu-id="7b884-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="7b884-109">Tienen acceso al contexto de JavaScript de la página y puede ejecutarlos en cualquier página.</span><span class="sxs-lookup"><span data-stu-id="7b884-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="7b884-110">Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="7b884-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="7b884-111">Firefox DevTools tiene una característica similar a la de los fragmentos de código denominado [Bloc][MDNScratchpad]dedo.</span><span class="sxs-lookup"><span data-stu-id="7b884-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="7b884-112">Por ejemplo, en la siguiente ilustración se muestra la Página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.</span><span class="sxs-lookup"><span data-stu-id="7b884-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="7b884-114">Aspecto de la página antes de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="7b884-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="7b884-115">El código fuente del fragmento de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="7b884-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="7b884-116">En la siguiente ilustración, la página aparece después de ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="7b884-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="7b884-117">El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el recorte y el contenido de la página cambian por completo.</span><span class="sxs-lookup"><span data-stu-id="7b884-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="7b884-119">Aspecto de la página después de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="7b884-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="7b884-120">Abrir el panel de fragmentos</span><span class="sxs-lookup"><span data-stu-id="7b884-120">Open the Snippets pane</span></span>  

<span data-ttu-id="7b884-121">El panel de **fragmentos de código** muestra los fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="7b884-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="7b884-122">Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="7b884-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="7b884-124">El panel de **fragmentos**</span><span class="sxs-lookup"><span data-stu-id="7b884-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="7b884-125">Abrir el panel de fragmentos de código con un mouse</span><span class="sxs-lookup"><span data-stu-id="7b884-125">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="7b884-126">Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="7b884-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="7b884-127">El panel de **páginas** suele abrirse de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b884-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="7b884-129">Panel **orígenes** con el panel de **páginas** abierto a la izquierda</span><span class="sxs-lookup"><span data-stu-id="7b884-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b884-130">Haga clic en la pestaña **fragmentos** para abrir el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="7b884-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="7b884-131">Es posible que tenga que elegir **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \) para acceder a la opción **fragmentos** .</span><span class="sxs-lookup"><span data-stu-id="7b884-131">You might need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="7b884-132">Abrir el panel de fragmentos de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="7b884-132">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="7b884-133">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7b884-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="7b884-134">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="7b884-134">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="7b884-135">Comience `Snippets` a escribir, elija **Mostrar fragmentos**y, a continuación, seleccione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="7b884-135">Start typing `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="7b884-137">El comando **Mostrar fragmentos**</span><span class="sxs-lookup"><span data-stu-id="7b884-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7b884-138">Crear fragmentos</span><span class="sxs-lookup"><span data-stu-id="7b884-138">Create Snippets</span></span>  

### <span data-ttu-id="7b884-139">Crear un fragmento de código a través del panel orígenes</span><span class="sxs-lookup"><span data-stu-id="7b884-139">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="7b884-140">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="7b884-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="7b884-141">Elija **nuevo fragmento de código**.</span><span class="sxs-lookup"><span data-stu-id="7b884-141">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="7b884-142">Escriba un nombre para el fragmento de código y, después, seleccione `Enter` Guardar.</span><span class="sxs-lookup"><span data-stu-id="7b884-142">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="7b884-144">Nombrar un fragmento de código</span><span class="sxs-lookup"><span data-stu-id="7b884-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="7b884-145">Crear un fragmento de código mediante el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="7b884-145">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="7b884-146">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7b884-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="7b884-147">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="7b884-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="7b884-148">Comience `Snippet` a escribir, elija **crear nuevo fragmento de código**y, a continuación, seleccione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="7b884-148">Start typing `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="7b884-150">Comando para crear un nuevo fragmento de código</span><span class="sxs-lookup"><span data-stu-id="7b884-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="7b884-151">Consulte cambiar [el nombre](#rename-snippets) de los fragmentos de código si desea asignar un nombre personalizado al nuevo fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="7b884-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="7b884-152">Editar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="7b884-152">Edit Snippets</span></span>  

1.  <span data-ttu-id="7b884-153">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="7b884-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="7b884-154">En el panel **fragmentos** de código, haga clic en el nombre del fragmento de código que desea editar para abrirlo en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="7b884-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="7b884-156">El **Editor de código**</span><span class="sxs-lookup"><span data-stu-id="7b884-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b884-157">Use el **Editor de código** para agregar JavaScript al fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="7b884-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="7b884-158">Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado.</span><span class="sxs-lookup"><span data-stu-id="7b884-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="7b884-159">Seleccione `Control` + `S` \ (Windows, Linux \) o `Command` + `S` \ (MacOS \) para guardar.</span><span class="sxs-lookup"><span data-stu-id="7b884-159">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="7b884-161">Un asterisco junto al nombre del fragmento de código, que indica código no guardado</span><span class="sxs-lookup"><span data-stu-id="7b884-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7b884-162">Ejecutar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="7b884-162">Run Snippets</span></span>  

### <span data-ttu-id="7b884-163">Ejecutar un recorte desde el panel fuentes</span><span class="sxs-lookup"><span data-stu-id="7b884-163">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="7b884-164">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="7b884-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="7b884-165">Haga clic en el nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="7b884-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="7b884-166">El fragmento de código se abre en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="7b884-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="7b884-167">Elija **Ejecutar fragmento** \ ( ![ Ejecutar miniprograma ][ImageRunSnippetIcon] \) o seleccione `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="7b884-167">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="7b884-168">Ejecutar un fragmento de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="7b884-168">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="7b884-169">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7b884-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="7b884-170">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="7b884-170">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="7b884-171">Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="7b884-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="7b884-173">Ejecución de un fragmento de código desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="7b884-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b884-174">Seleccione `Enter` para ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="7b884-174">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="7b884-175">Cambiar el nombre de los fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="7b884-175">Rename Snippets</span></span>  

1.  <span data-ttu-id="7b884-176">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="7b884-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="7b884-177">Haga clic con el botón derecho en el nombre del fragmento y seleccione **cambiar nombre**.</span><span class="sxs-lookup"><span data-stu-id="7b884-177">Right-click the Snippet name and choose **Rename**.</span></span>  
    
## <span data-ttu-id="7b884-178">Eliminar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="7b884-178">Delete Snippets</span></span>  

1.  <span data-ttu-id="7b884-179">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="7b884-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="7b884-180">Haga clic con el botón derecho en el nombre del fragmento y elija **quitar**.</span><span class="sxs-lookup"><span data-stu-id="7b884-180">Right-click the Snippet name and choose **Remove**.</span></span>  
    
## <span data-ttu-id="7b884-181">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7b884-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft docs"  
[DevToolsSourcesPanel]: ../sources.md "Información general del panel orígenes | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet, Wikipedia"  

> [!NOTE]
> <span data-ttu-id="7b884-186">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7b884-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7b884-187">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7b884-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7b884-189">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7b884-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
