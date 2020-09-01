---
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3a5ae986e3080a0b6a8b1bf34b0e0efc44c90303
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982046"
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





# <span data-ttu-id="4d5ac-103">Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4d5ac-103">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="4d5ac-104">Si tienes que ejecutar el mismo código de forma repetida en la [consola][DevtoolsConsoleIndex] , considera la posibilidad de guardar el código como un fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="4d5ac-105">Los fragmentos de código son scripts que se crean en el panel [fuentes][DevToolsSourcesPanel] .</span><span class="sxs-lookup"><span data-stu-id="4d5ac-105">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="4d5ac-106">Tienen acceso al contexto de JavaScript de la página y puede ejecutarlos en cualquier página.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="4d5ac-107">Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="4d5ac-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="4d5ac-108">Firefox DevTools tiene una característica similar a la de los fragmentos de código denominado [Bloc][MDNScratchpad]dedo.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="4d5ac-109">Por ejemplo, en la siguiente ilustración se muestra la Página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-109">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="4d5ac-111">Aspecto de la página antes de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-111">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="4d5ac-112">El código fuente del fragmento de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-112">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="4d5ac-113">En la siguiente ilustración, la página aparece después de ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-113">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="4d5ac-114">El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el recorte y el contenido de la página cambian por completo.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-114">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aspecto de la página después de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="4d5ac-116">Aspecto de la página después de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-116">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="4d5ac-117">Abrir el panel de fragmentos</span><span class="sxs-lookup"><span data-stu-id="4d5ac-117">Open the Snippets pane</span></span>   

<span data-ttu-id="4d5ac-118">El panel de **fragmentos de código** muestra los fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-118">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="4d5ac-119">Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="4d5ac-119">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="El panel de fragmentos" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="4d5ac-121">El panel de **fragmentos**</span><span class="sxs-lookup"><span data-stu-id="4d5ac-121">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="4d5ac-122">Abrir el panel de fragmentos de código con un mouse</span><span class="sxs-lookup"><span data-stu-id="4d5ac-122">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="4d5ac-123">Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="4d5ac-123">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="4d5ac-124">El panel de **páginas** suele abrirse de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-124">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Panel orígenes con el panel de páginas abierto a la izquierda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="4d5ac-126">Panel **orígenes** con el panel de **páginas** abierto a la izquierda</span><span class="sxs-lookup"><span data-stu-id="4d5ac-126">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4d5ac-127">Haga clic en la pestaña **fragmentos** para abrir el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="4d5ac-127">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="4d5ac-128">Es posible que tenga que hacer clic en **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \) para acceder a la opción **fragmentos** .</span><span class="sxs-lookup"><span data-stu-id="4d5ac-128">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="4d5ac-129">Abrir el panel de fragmentos de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="4d5ac-129">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="4d5ac-130">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-130">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="4d5ac-131">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-131">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4d5ac-132">Comience `Snippets` a escribir, seleccione **Mostrar fragmentos**y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-132">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="El comando Mostrar fragmentos" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="4d5ac-134">El comando **Mostrar fragmentos**</span><span class="sxs-lookup"><span data-stu-id="4d5ac-134">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4d5ac-135">Crear fragmentos</span><span class="sxs-lookup"><span data-stu-id="4d5ac-135">Create Snippets</span></span>   

### <span data-ttu-id="4d5ac-136">Crear un fragmento de código a través del panel orígenes</span><span class="sxs-lookup"><span data-stu-id="4d5ac-136">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="4d5ac-137">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-137">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4d5ac-138">Haga clic en **nuevo fragmento de código**.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-138">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="4d5ac-139">Escriba un nombre para el fragmento de código y, a continuación, presione `Enter` para guardar.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-139">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nombrar un fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="4d5ac-141">Nombrar un fragmento de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-141">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4d5ac-142">Crear un fragmento de código mediante el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="4d5ac-142">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="4d5ac-143">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-143">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="4d5ac-144">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-144">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4d5ac-145">Comience `Snippet` a escribir, seleccione **crear nuevo fragmento**y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-145">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Comando para crear un nuevo fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="4d5ac-147">Comando para crear un nuevo fragmento de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-147">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4d5ac-148">Consulte cambiar [el nombre](#rename-snippets) de los fragmentos de código si desea asignar un nombre personalizado al nuevo fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-148">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="4d5ac-149">Editar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-149">Edit Snippets</span></span>   

1.  <span data-ttu-id="4d5ac-150">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-150">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4d5ac-151">En el panel **fragmentos** de código, haga clic en el nombre del fragmento de código que desea editar para abrirlo en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-151">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="El editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="4d5ac-153">El **Editor de código**</span><span class="sxs-lookup"><span data-stu-id="4d5ac-153">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4d5ac-154">Use el **Editor de código** para agregar JavaScript al fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-154">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="4d5ac-155">Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-155">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="4d5ac-156">Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-156">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un asterisco junto al nombre del fragmento de código, que indica código no guardado" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="4d5ac-158">Un asterisco junto al nombre del fragmento de código, que indica código no guardado</span><span class="sxs-lookup"><span data-stu-id="4d5ac-158">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4d5ac-159">Ejecutar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-159">Run Snippets</span></span>   

### <span data-ttu-id="4d5ac-160">Ejecutar un recorte desde el panel fuentes</span><span class="sxs-lookup"><span data-stu-id="4d5ac-160">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="4d5ac-161">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-161">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4d5ac-162">Haga clic en el nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-162">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="4d5ac-163">El fragmento de código se abre en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-163">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="4d5ac-164">Haga clic en **Ejecutar fragmento** \ ( ![ Ejecutar fragmento ][ImageRunSnippetIcon] \) o `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-164">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="4d5ac-165">Ejecutar un fragmento de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="4d5ac-165">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="4d5ac-166">Centre el cursor en algún lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-166">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="4d5ac-167">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-167">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4d5ac-168">Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-168">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ejecución de un fragmento de código desde el menú de comandos" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="4d5ac-170">Ejecución de un fragmento de código desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="4d5ac-170">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4d5ac-171">Pulse `Enter` para ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-171">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="4d5ac-172">Cambiar el nombre de los fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-172">Rename Snippets</span></span>   

1.  <span data-ttu-id="4d5ac-173">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-173">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4d5ac-174">Haga clic con el botón derecho en el nombre del fragmento y seleccione cambiar **nombre**.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-174">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="4d5ac-175">Eliminar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="4d5ac-175">Delete Snippets</span></span>   

1.  <span data-ttu-id="4d5ac-176">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4d5ac-177">Haga clic con el botón derecho en el nombre del fragmento y seleccione **quitar**.</span><span class="sxs-lookup"><span data-stu-id="4d5ac-177">Right-click the Snippet name and select **Remove**.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft docs"  
[DevToolsSourcesPanel]: ../sources.md "Información general del panel orígenes | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet, Wikipedia"  

> [!NOTE]
> <span data-ttu-id="4d5ac-182">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4d5ac-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4d5ac-183">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4d5ac-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4d5ac-185">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4d5ac-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
