---
description: Los fragmentos de código son pequeños scripts que puede crear y ejecutar en la herramienta Orígenes de Microsoft Edge DevTools.  Puede acceder y ejecutar recursos desde cualquier página web.  Cuando se ejecuta un fragmento de código, se ejecuta desde el contexto de la página web abierta actualmente.
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439426"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="56fc1-106">Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="56fc1-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="56fc1-107">Si ejecuta el mismo código en la [consola][DevtoolsConsoleIndex] repetidamente, considere la posibilidad de guardar el código como fragmento de código en su lugar.</span><span class="sxs-lookup"><span data-stu-id="56fc1-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="56fc1-108">Los fragmentos de código son scripts que se pueden crear en la [herramienta][DevToolsSourcesTool] Orígenes.</span><span class="sxs-lookup"><span data-stu-id="56fc1-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="56fc1-109">Los fragmentos de código tienen acceso al contexto de JavaScript de la página web y puede ejecutar fragmentos de código en cualquier página web.</span><span class="sxs-lookup"><span data-stu-id="56fc1-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="56fc1-110">La configuración de seguridad de la mayoría de las páginas web bloquea la carga de otros scripts en fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="56fc1-111">Por este motivo, debe incluir todo el código en un archivo.</span><span class="sxs-lookup"><span data-stu-id="56fc1-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="56fc1-112">Los fragmentos de código son una alternativa a [los bookmarklets][WikiBookmarklet] con la diferencia de que los fragmentos de código solo se ejecutan en DevTools y no se limitan a la longitud permitida de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="56fc1-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="56fc1-113">El uso de fragmentos de código es una excelente manera de cambiar algunas cosas en una página web de terceros.</span><span class="sxs-lookup"><span data-stu-id="56fc1-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="56fc1-114">Los cambios de código en fragmentos de código se agregan a la página web actual y se ejecutan en el mismo contexto.</span><span class="sxs-lookup"><span data-stu-id="56fc1-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="56fc1-115">Para obtener más información sobre cómo cambiar el código existente de una página web, vaya a [Invalidaciones][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="56fc1-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="56fc1-116">Por ejemplo, en la siguiente figura se muestra la página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.</span><span class="sxs-lookup"><span data-stu-id="56fc1-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="56fc1-118">La página web antes de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="56fc1-119">El código fuente de fragmento de código de la página web antes de ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="56fc1-120">En la siguiente figura, la página web aparece después de ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="56fc1-121">El **cajón de** consola aparece para mostrar el mensaje de que el fragmento de `Hello, Snippets!` código registra y el contenido de la página web cambia por completo.</span><span class="sxs-lookup"><span data-stu-id="56fc1-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="La página web después de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="56fc1-123">La página web después de ejecutar el fragmento de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-pane"></a><span data-ttu-id="56fc1-124">Abrir el panel Fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-124">Open the Snippets pane</span></span>  

<span data-ttu-id="56fc1-125">El **panel Fragmentos de** código enumera los fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="56fc1-126">Cuando desee editar un fragmento de código, debe abrirlo desde el panel **Fragmentos de** código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Panel Fragmentos de código" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="56fc1-128">Panel **Fragmentos de** código</span><span class="sxs-lookup"><span data-stu-id="56fc1-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a><span data-ttu-id="56fc1-129">Abra el panel Fragmentos de código con un mouse</span><span class="sxs-lookup"><span data-stu-id="56fc1-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="56fc1-130">Elija la **pestaña Orígenes** para abrir la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="56fc1-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="56fc1-131">El **panel Página** normalmente se abre de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="56fc1-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="La herramienta Orígenes con el panel Página abierto a la izquierda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="56fc1-133">La **herramienta Orígenes** con el panel **Página** abierto a la izquierda</span><span class="sxs-lookup"><span data-stu-id="56fc1-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56fc1-134">Elija la **pestaña Fragmentos de** código para abrir el **panel Fragmentos de** código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="56fc1-135">Es posible que deba elegir **Más pestañas** \( ![ Más pestañas \) para tener acceso a la opción ](../media/more-tabs-icon.msft.png) **Fragmentos de** código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-135">You may need to choose **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) to access the **Snippets** option.</span></span>  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a><span data-ttu-id="56fc1-136">Abra el panel Fragmentos de código con el menú Comando</span><span class="sxs-lookup"><span data-stu-id="56fc1-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="56fc1-137">Centra el cursor en alguna parte de DevTools.</span><span class="sxs-lookup"><span data-stu-id="56fc1-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="56fc1-138">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el menú comando.</span><span class="sxs-lookup"><span data-stu-id="56fc1-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="56fc1-139">Escriba `Snippets` , elija Mostrar **fragmentos de código**y, a continuación, seleccione para ejecutar el `Enter` comando.</span><span class="sxs-lookup"><span data-stu-id="56fc1-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="El comando Mostrar fragmentos de código" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="56fc1-141">El **comando Mostrar fragmentos de código**</span><span class="sxs-lookup"><span data-stu-id="56fc1-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="56fc1-142">Crear fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-142">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-panel"></a><span data-ttu-id="56fc1-143">Crear un fragmento de código a través del panel Orígenes</span><span class="sxs-lookup"><span data-stu-id="56fc1-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="56fc1-144">[Abra el **panel Fragmentos de** código](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="56fc1-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="56fc1-145">Elija **Nuevo fragmento de código**.</span><span class="sxs-lookup"><span data-stu-id="56fc1-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="56fc1-146">Escriba un nombre para el fragmento de código y, a continuación, `Enter` seleccione para guardar.</span><span class="sxs-lookup"><span data-stu-id="56fc1-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Asigne un nombre a un fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="56fc1-148">Asigne un nombre a un fragmento de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="56fc1-149">Crear un fragmento de código a través del menú de comandos</span><span class="sxs-lookup"><span data-stu-id="56fc1-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="56fc1-150">Centra el cursor en alguna parte de DevTools.</span><span class="sxs-lookup"><span data-stu-id="56fc1-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="56fc1-151">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el menú comando.</span><span class="sxs-lookup"><span data-stu-id="56fc1-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="56fc1-152">Escriba `Snippet` , elija Crear nuevo fragmento **de**código y, a continuación, `Enter` seleccione para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="56fc1-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="El comando para crear un nuevo fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="56fc1-154">El comando para crear un nuevo fragmento de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="56fc1-155">Para cambiar el nombre del nuevo fragmento de código con un nombre personalizado, vaya a [Cambiar el nombre de fragmentos de código](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="56fc1-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="56fc1-156">Editar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="56fc1-157">[Abra el **panel Fragmentos de** código](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="56fc1-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="56fc1-158">En el **panel Fragmentos** de código, elija el nombre del fragmento de código que desea editar.</span><span class="sxs-lookup"><span data-stu-id="56fc1-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="56fc1-159">Se abre en el **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="56fc1-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="56fc1-161">Editor **de código**</span><span class="sxs-lookup"><span data-stu-id="56fc1-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56fc1-162">Use el **Editor de código** para agregar JavaScript al fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="56fc1-163">Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado.</span><span class="sxs-lookup"><span data-stu-id="56fc1-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="56fc1-164">Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar.</span><span class="sxs-lookup"><span data-stu-id="56fc1-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un asterisco junto al nombre del fragmento de código indica código no guardado" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="56fc1-166">Un asterisco junto al nombre del fragmento de código indica código no guardado</span><span class="sxs-lookup"><span data-stu-id="56fc1-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="56fc1-167">Ejecutar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-167">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-panel"></a><span data-ttu-id="56fc1-168">Ejecutar un fragmento de código desde el panel Orígenes</span><span class="sxs-lookup"><span data-stu-id="56fc1-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="56fc1-169">[Abra el **panel Fragmentos de** código](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="56fc1-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="56fc1-170">Elija el nombre del fragmento de código que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="56fc1-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="56fc1-171">El fragmento de código se abre en **el Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="56fc1-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="56fc1-172">Elija **Ejecutar fragmento de** código \( Ejecutar fragmento de código ![ ](../media/run-snippet-icon.msft.png) \) o seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="56fc1-172">Choose **Run Snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="56fc1-173">Ejecutar un fragmento de código con el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="56fc1-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="56fc1-174">Centra el cursor en alguna parte de DevTools.</span><span class="sxs-lookup"><span data-stu-id="56fc1-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="56fc1-175">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el menú comando.</span><span class="sxs-lookup"><span data-stu-id="56fc1-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="56fc1-176">Elimine el `>` carácter y escriba el carácter seguido del nombre del fragmento de código que desea `!` ejecutar.</span><span class="sxs-lookup"><span data-stu-id="56fc1-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ejecución de un fragmento de código desde el menú de comandos" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="56fc1-178">Ejecución de un fragmento de código desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="56fc1-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56fc1-179">Seleccione `Enter` para ejecutar el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="56fc1-179">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="56fc1-180">Cambiar el nombre de fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="56fc1-181">[Abra el **panel Fragmentos de** código](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="56fc1-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="56fc1-182">Mantenga el mouse en el nombre del fragmento de código, abra el menú contextual \(haga clic con el botón secundario\) y elija **Cambiar nombre**.</span><span class="sxs-lookup"><span data-stu-id="56fc1-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="56fc1-183">Eliminar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="56fc1-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="56fc1-184">[Abra el **panel Fragmentos de** código](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="56fc1-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="56fc1-185">Mantenga el mouse sobre el nombre del fragmento de código, abra el menú contextual \(haga clic con el botón secundario en\) y elija **Quitar**.</span><span class="sxs-lookup"><span data-stu-id="56fc1-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="56fc1-186">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="56fc1-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Información general de la consola | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Invalida | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> <span data-ttu-id="56fc1-192">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56fc1-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="56fc1-193">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="56fc1-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="56fc1-195">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56fc1-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
