---
description: Los fragmentos de código son pequeños scripts que puede crear y ejecutar en la herramienta de orígenes de Microsoft Edge DevTools.  Puede obtener acceso a los recursos de cualquier página web y ejecutarlos.  Al ejecutar un fragmento de código, se ejecuta desde el contexto de la página web abierta actualmente.
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3542243f7fa886865ced47d47991cd9b11001e2e
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145123"
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

# <span data-ttu-id="5504c-106">Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5504c-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="5504c-107">Si ejecutas el mismo código de la [consola][DevtoolsConsoleIndex] varias veces, te recomendamos que guardes el código como un fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="5504c-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="5504c-108">Los fragmentos de código son scripts que se crean en la herramienta [orígenes][DevToolsSourcesTool] .</span><span class="sxs-lookup"><span data-stu-id="5504c-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="5504c-109">Los fragmentos de código tienen acceso al contexto de JavaScript de la página web y puede ejecutar fragmentos de código en cualquier página web.</span><span class="sxs-lookup"><span data-stu-id="5504c-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="5504c-110">La configuración de seguridad de la mayoría de las páginas web impide que se carguen otros scripts en los fragmentos.</span><span class="sxs-lookup"><span data-stu-id="5504c-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="5504c-111">Por ese motivo, debes incluir todo tu código en un archivo.</span><span class="sxs-lookup"><span data-stu-id="5504c-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="5504c-112">Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet] con la diferencia de que los fragmentos de código solo se ejecutan en DevTools y no se limitan a la longitud permitida de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="5504c-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="5504c-113">El uso de recortes es una excelente manera de cambiar algunas cosas en una página web de terceros.</span><span class="sxs-lookup"><span data-stu-id="5504c-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="5504c-114">Los cambios de código en los fragmentos se agregan a la página web actual y se ejecutan en el mismo contexto.</span><span class="sxs-lookup"><span data-stu-id="5504c-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="5504c-115">Para obtener más información sobre cómo cambiar el código existente de una página web, vaya a [invalidaciones][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="5504c-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5504c-116">Por ejemplo, en la siguiente ilustración se muestra la Página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.</span><span class="sxs-lookup"><span data-stu-id="5504c-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="5504c-118">La Página Web antes de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="5504c-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5504c-119">El código fuente del fragmento de código de la Página Web antes de ejecutar el fragmento.</span><span class="sxs-lookup"><span data-stu-id="5504c-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5504c-120">En la siguiente ilustración, la página web aparece después de ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="5504c-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="5504c-121">El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el fragmento de código registra y el contenido de la página web cambia por completo.</span><span class="sxs-lookup"><span data-stu-id="5504c-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="La página web después de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="5504c-123">La página web después de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="5504c-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="5504c-124">Abrir el panel de fragmentos</span><span class="sxs-lookup"><span data-stu-id="5504c-124">Open the Snippets pane</span></span>  

<span data-ttu-id="5504c-125">El panel de **fragmentos de código** muestra los fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="5504c-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="5504c-126">Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="5504c-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="El panel de fragmentos" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="5504c-128">El panel de **fragmentos**</span><span class="sxs-lookup"><span data-stu-id="5504c-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="5504c-129">Abrir el panel de fragmentos de código con un mouse</span><span class="sxs-lookup"><span data-stu-id="5504c-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="5504c-130">Elija la pestaña **orígenes** para abrir la herramienta **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="5504c-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="5504c-131">El panel de **páginas** suele abrirse de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5504c-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="La herramienta orígenes con el panel de páginas abierto a la izquierda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="5504c-133">La herramienta **orígenes** con el panel de **páginas** abierto a la izquierda</span><span class="sxs-lookup"><span data-stu-id="5504c-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5504c-134">Elija la pestaña **fragmentos** para abrir el panel **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="5504c-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="5504c-135">Es posible que tenga que elegir **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \) para acceder a la opción **fragmentos de código** .</span><span class="sxs-lookup"><span data-stu-id="5504c-135">You may need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="5504c-136">Abrir el panel de fragmentos de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="5504c-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="5504c-137">Centre el cursor en algún lugar de DevTools.</span><span class="sxs-lookup"><span data-stu-id="5504c-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="5504c-138">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="5504c-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5504c-139">Escriba `Snippets` , elija **Mostrar fragmentos**y, a continuación, seleccione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="5504c-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="El comando Mostrar fragmentos" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="5504c-141">El comando **Mostrar fragmentos**</span><span class="sxs-lookup"><span data-stu-id="5504c-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5504c-142">Crear fragmentos</span><span class="sxs-lookup"><span data-stu-id="5504c-142">Create Snippets</span></span>  

### <span data-ttu-id="5504c-143">Crear un fragmento de código a través del panel orígenes</span><span class="sxs-lookup"><span data-stu-id="5504c-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="5504c-144">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5504c-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5504c-145">Elija **nuevo fragmento de código**.</span><span class="sxs-lookup"><span data-stu-id="5504c-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="5504c-146">Escriba un nombre para el fragmento de código y, después, seleccione `Enter` Guardar.</span><span class="sxs-lookup"><span data-stu-id="5504c-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nombrar un fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="5504c-148">Nombrar un fragmento de código</span><span class="sxs-lookup"><span data-stu-id="5504c-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="5504c-149">Crear un fragmento de código mediante el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="5504c-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="5504c-150">Centre el cursor en algún lugar de DevTools.</span><span class="sxs-lookup"><span data-stu-id="5504c-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="5504c-151">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="5504c-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5504c-152">Escriba `Snippet` , elija **crear nuevo fragmento de código**y, a continuación, seleccione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="5504c-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Comando para crear un nuevo fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="5504c-154">Comando para crear un nuevo fragmento de código</span><span class="sxs-lookup"><span data-stu-id="5504c-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="5504c-155">Para cambiar el nombre de un nuevo fragmento con un nombre personalizado, navegue hasta [cambiar el nombre](#rename-snippets)de los fragmentos.</span><span class="sxs-lookup"><span data-stu-id="5504c-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <span data-ttu-id="5504c-156">Editar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="5504c-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="5504c-157">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5504c-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5504c-158">En el panel **fragmentos** , elija el nombre del fragmento de código que desea editar.</span><span class="sxs-lookup"><span data-stu-id="5504c-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="5504c-159">Se abre en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="5504c-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="El editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="5504c-161">El **Editor de código**</span><span class="sxs-lookup"><span data-stu-id="5504c-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5504c-162">Use el **Editor de código** para agregar JavaScript al fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="5504c-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="5504c-163">Cuando aparece un asterisco junto al nombre del fragmento, significa que tiene código no guardado.</span><span class="sxs-lookup"><span data-stu-id="5504c-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="5504c-164">Seleccione `Control` + `S` \ (Windows, Linux \) o `Command` + `S` \ (MacOS \) para guardar.</span><span class="sxs-lookup"><span data-stu-id="5504c-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un asterisco junto al nombre del fragmento de código indica que el código no se ha guardado" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="5504c-166">Un asterisco junto al nombre del fragmento de código indica que el código no se ha guardado</span><span class="sxs-lookup"><span data-stu-id="5504c-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5504c-167">Ejecutar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="5504c-167">Run Snippets</span></span>  

### <span data-ttu-id="5504c-168">Ejecutar un recorte desde el panel fuentes</span><span class="sxs-lookup"><span data-stu-id="5504c-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="5504c-169">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5504c-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5504c-170">Elija el nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="5504c-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="5504c-171">El fragmento de código se abre en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="5504c-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="5504c-172">Elija **Ejecutar fragmento** \ ( ![ Ejecutar miniprograma ][ImageRunSnippetIcon] \) o seleccione `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="5504c-172">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="5504c-173">Ejecutar un fragmento de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="5504c-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="5504c-174">Centre el cursor en algún lugar de DevTools.</span><span class="sxs-lookup"><span data-stu-id="5504c-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="5504c-175">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="5504c-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5504c-176">Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="5504c-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ejecución de un fragmento de código desde el menú de comandos" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="5504c-178">Ejecución de un fragmento de código desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="5504c-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5504c-179">Seleccione `Enter` para ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="5504c-179">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="5504c-180">Cambiar el nombre de los fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="5504c-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="5504c-181">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5504c-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5504c-182">Desplace el puntero sobre el nombre del fragmento de código, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **cambiar nombre**.</span><span class="sxs-lookup"><span data-stu-id="5504c-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <span data-ttu-id="5504c-183">Eliminar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="5504c-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="5504c-184">[Abra el panel **fragmentos de código** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5504c-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5504c-185">Desplace el puntero sobre el nombre del fragmento de código, abra el menú contextual \ (haga clic con el botón derecho \) y elija **quitar**.</span><span class="sxs-lookup"><span data-stu-id="5504c-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <span data-ttu-id="5504c-186">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5504c-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft docs"  
[DevToolsSourcesTool]: ../sources.md "Información general de la herramienta orígenes | Microsoft docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Invalidaciones | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> <span data-ttu-id="5504c-192">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5504c-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5504c-193">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5504c-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5504c-195">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5504c-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
