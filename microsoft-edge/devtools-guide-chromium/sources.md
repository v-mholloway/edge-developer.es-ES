---
title: Información general del panel orígenes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601911"
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
   limitations under the License. -->






# <span data-ttu-id="4ec43-103">Información general del panel orígenes</span><span class="sxs-lookup"><span data-stu-id="4ec43-103">Sources Panel Overview</span></span> 



<span data-ttu-id="4ec43-104">Use el panel de **orígenes** de Microsoft Edge DevTools para:</span><span class="sxs-lookup"><span data-stu-id="4ec43-104">Use the Microsoft Edge DevTools **Sources** panel to:</span></span>

*   <span data-ttu-id="4ec43-105">[Ver archivos](#view-files).</span><span class="sxs-lookup"><span data-stu-id="4ec43-105">[View files](#view-files).</span></span>  
*   <span data-ttu-id="4ec43-106">[Edite CSS y JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="4ec43-106">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="4ec43-107">[Cree y guarde **fragmentos** de código de JavaScript](#create-save-and-run-snippets), que puede ejecutar en cualquier página.</span><span class="sxs-lookup"><span data-stu-id="4ec43-107">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="4ec43-108">Los **fragmentos de código** son similares a bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="4ec43-108">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="4ec43-109">[Depure JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="4ec43-109">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="4ec43-110">[Configure un área de trabajo](#set-up-a-workspace)para que los cambios que realice en DevTools se guarden en el código de su sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ec43-110">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  

## <span data-ttu-id="4ec43-111">Ver archivos</span><span class="sxs-lookup"><span data-stu-id="4ec43-111">View files</span></span> 

<span data-ttu-id="4ec43-112">Use el panel de **páginas** para ver todos los recursos que la página ha cargado.</span><span class="sxs-lookup"><span data-stu-id="4ec43-112">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

> ##### <span data-ttu-id="4ec43-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="4ec43-113">Figure 1</span></span>  
> <span data-ttu-id="4ec43-114">El panel de **páginas**</span><span class="sxs-lookup"><span data-stu-id="4ec43-114">The **Page** pane</span></span>  
> ![Ilustración 1: el panel de páginas][ImageSourcesPagePane]  

<span data-ttu-id="4ec43-116">Organización del panel de **páginas** :</span><span class="sxs-lookup"><span data-stu-id="4ec43-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="4ec43-117">El nivel superior, como en la `top` [**figura 1**](#figure-1), representa un [marco HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="4ec43-117">The top-level, such as `top` in [**Figure 1**](#figure-1), represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="4ec43-118">Buscar `top` en cada página que visite.</span><span class="sxs-lookup"><span data-stu-id="4ec43-118">Find `top` on every page that you visit.</span></span> `top` <span data-ttu-id="4ec43-119">representa el marco del documento principal.</span><span class="sxs-lookup"><span data-stu-id="4ec43-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="4ec43-120">El segundo nivel, como en la `docs.microsoft.com` [**figura 1**](#figure-1), representa un [origen][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="4ec43-120">The second-level, such as `docs.microsoft.com` in [**Figure 1**](#figure-1), represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="4ec43-121">El tercer nivel, el cuarto nivel, etc., representan los directorios y recursos que se cargaron desde ese origen.</span><span class="sxs-lookup"><span data-stu-id="4ec43-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="4ec43-122">Por ejemplo, en la [**figura 1**](#figure-1) , la ruta de acceso completa al recurso `devtools-guide-chromium` es</span><span class="sxs-lookup"><span data-stu-id="4ec43-122">For example, in [**Figure 1**](#figure-1) the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

<span data-ttu-id="4ec43-123">Haga clic en un archivo en el panel de **páginas** para ver el contenido en el panel del **Editor** .</span><span class="sxs-lookup"><span data-stu-id="4ec43-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="4ec43-124">Puede ver cualquier tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="4ec43-124">You may view any type of file.</span></span> <span data-ttu-id="4ec43-125">Para las imágenes, verá una vista previa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4ec43-125">For images, you see a preview of the image.</span></span>  

> ##### <span data-ttu-id="4ec43-126">Figura 2</span><span class="sxs-lookup"><span data-stu-id="4ec43-126">Figure 2</span></span>  
> <span data-ttu-id="4ec43-127">Ver el contenido de `a4d10f71.index-docs.js` en el panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="4ec43-127">Viewing the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
> ![Figura 2.][ImageSourcesEditorPane]  

## <span data-ttu-id="4ec43-130">Editar CSS y JavaScript</span><span class="sxs-lookup"><span data-stu-id="4ec43-130">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="4ec43-131">Use el panel **Editor** para editar CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ec43-131">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="4ec43-132">DevTools actualiza la página para ejecutar el nuevo código.</span><span class="sxs-lookup"><span data-stu-id="4ec43-132">DevTools updates the page to run your new code.</span></span> <span data-ttu-id="4ec43-133">Por ejemplo, Si edita un archivo CSS agregando la regla de estilo a continuación:</span><span class="sxs-lookup"><span data-stu-id="4ec43-133">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="4ec43-134">Verá que el cambio se aplicará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4ec43-134">You should see that change take effect immediately.</span></span>

> ##### <span data-ttu-id="4ec43-135">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="4ec43-135">Figure 3</span></span>  
> <span data-ttu-id="4ec43-136">Editar CSS en el panel **Editor** para cambiar el color del texto del subtítulo a rojo</span><span class="sxs-lookup"><span data-stu-id="4ec43-136">Editing CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
> ![Figura 3.][ImageEditCSS]  

<span data-ttu-id="4ec43-139">Los cambios de CSS se aplican inmediatamente, no es necesario guardar.</span><span class="sxs-lookup"><span data-stu-id="4ec43-139">CSS changes take effect immediately, no save needed.</span></span> <span data-ttu-id="4ec43-140">Para que los cambios de JavaScript surtan efecto, pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="4ec43-140">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span> <span data-ttu-id="4ec43-141">DevTools no vuelve a ejecutar un script, por lo que los únicos cambios de JavaScript que se aplican son los que realiza dentro de las funciones.</span><span class="sxs-lookup"><span data-stu-id="4ec43-141">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="4ec43-142">Por ejemplo, en la [**figura 4**](#figure-4) , observe cómo `console.log('A')` no se ejecuta, pero `console.log('B')` sí.</span><span class="sxs-lookup"><span data-stu-id="4ec43-142">For example, in [**Figure 4**](#figure-4) note how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span> <span data-ttu-id="4ec43-143">Si DevTools vuelto a ejecutar la secuencia de comandos completa después de realizar el cambio, el texto `A` se habría registrado en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="4ec43-143">If DevTools re-ran the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

> ##### <span data-ttu-id="4ec43-144">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="4ec43-144">Figure 4</span></span>  
> <span data-ttu-id="4ec43-145">Edición de JavaScript en el panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="4ec43-145">Editing JavaScript in the **Editor** pane</span></span>  
> ![Figura 4.][ImageEditJS]  

<span data-ttu-id="4ec43-148">DevTools borra los cambios de CSS y JavaScript al volver a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="4ec43-148">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span> <span data-ttu-id="4ec43-149">Vea [configurar un área de trabajo](#set-up-a-workspace) para obtener información sobre cómo guardar los cambios en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ec43-149">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="4ec43-150">Crear, guardar y ejecutar fragmentos de código</span><span class="sxs-lookup"><span data-stu-id="4ec43-150">Create, save, and run Snippets</span></span> 

<span data-ttu-id="4ec43-151">Los fragmentos de código son scripts que se pueden ejecutar en cualquier página.</span><span class="sxs-lookup"><span data-stu-id="4ec43-151">Snippets are scripts which you may run on any page.</span></span> <span data-ttu-id="4ec43-152">Suponga que escribe repetidamente el siguiente código en la **consola**, para insertar la biblioteca de jQuery en una página, de modo que pueda ejecutar comandos de jQuery desde la **consola**:</span><span class="sxs-lookup"><span data-stu-id="4ec43-152">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="4ec43-153">En su lugar, puede guardar este código en un **fragmento** de código y ejecutarlo con un par de clics de botón, cada vez que lo necesite.</span><span class="sxs-lookup"><span data-stu-id="4ec43-153">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="4ec43-154">DevTools guarda el **fragmento de código** en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ec43-154">DevTools saves the **Snippet** to your file system.</span></span>  

> ##### <span data-ttu-id="4ec43-155">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="4ec43-155">Figure 5</span></span>  
> <span data-ttu-id="4ec43-156">Un **fragmento de código** que inserta la biblioteca jQuery en una página</span><span class="sxs-lookup"><span data-stu-id="4ec43-156">A **Snippet** that inserts the jQuery library into a page</span></span>  
> ![Figura 5.][ImageSnippet]  

<span data-ttu-id="4ec43-159">Para ejecutar un **fragmento de código**:</span><span class="sxs-lookup"><span data-stu-id="4ec43-159">To run a **Snippet**:</span></span>

*   <span data-ttu-id="4ec43-160">Abra el archivo a través del panel **fragmentos de código** y haga clic en **Ejecutar** ![ el botón ejecutar ][ImageRunIcon] .</span><span class="sxs-lookup"><span data-stu-id="4ec43-160">Open the file via the **Snippets** pane, and click **Run** ![The Run button][ImageRunIcon].</span></span>  
*   <span data-ttu-id="4ec43-161">Abra el **[menú de comandos][DevtoolsGuideChromiumCommandMenuIndex]**, elimine el `>` carácter, escriba `!` , escriba el nombre del **fragmento**y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4ec43-161">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  

<span data-ttu-id="4ec43-162">Vea [Ejecutar fragmentos de código desde cualquier página][DevtoolsGuideChromiumJavascriptSnippets] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4ec43-162">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>


## <span data-ttu-id="4ec43-163">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="4ec43-163">Debug JavaScript</span></span> 

<span data-ttu-id="4ec43-164">En lugar de usar `console.log()` para inferir Dónde está el error de JavaScript, considere la posibilidad de usar las herramientas de depuración de Microsoft Edge DevTools en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4ec43-164">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span> <span data-ttu-id="4ec43-165">La idea general es establecer un punto de interrupción, que es un lugar de detención intencionado en el código, y, a continuación, pasar por el tiempo de ejecución del código, de línea en línea.</span><span class="sxs-lookup"><span data-stu-id="4ec43-165">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span> <span data-ttu-id="4ec43-166">Mientras recorres el código, puedes ver y cambiar los valores de todas las propiedades y variables definidas actualmente, ejecutar JavaScript en la **consola**y mucho más.</span><span class="sxs-lookup"><span data-stu-id="4ec43-166">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="4ec43-167">Consulte Introducción a la [depuración de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para conocer los conceptos básicos de la depuración en DevTools.</span><span class="sxs-lookup"><span data-stu-id="4ec43-167">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

> ##### <span data-ttu-id="4ec43-168">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="4ec43-168">Figure 6</span></span>  
> <span data-ttu-id="4ec43-169">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="4ec43-169">Debugging JavaScript</span></span>  
> ![Figura 6.][ImageDebugging]  

## <span data-ttu-id="4ec43-172">Configurar un área de trabajo</span><span class="sxs-lookup"><span data-stu-id="4ec43-172">Set up a Workspace</span></span> 

<span data-ttu-id="4ec43-173">De forma predeterminada, al editar un archivo en el panel **orígenes** , esos cambios se pierden al volver a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="4ec43-173">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="4ec43-174">Las **áreas de trabajo** le permiten guardar los cambios que realice en DevTools en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ec43-174">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="4ec43-175">Esencialmente, esto te permite usar DevTools como tu editor de código.</span><span class="sxs-lookup"><span data-stu-id="4ec43-175">Essentially, this lets you use DevTools as your code editor.</span></span>

<span data-ttu-id="4ec43-176">Consulte [editar archivos con áreas de trabajo][DevtoolsGuideChromiumWorkspacesIndex] para comenzar.</span><span class="sxs-lookup"><span data-stu-id="4ec43-176">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Ilustración 1: el panel de páginas"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Ilustración 2: visualización del contenido de a4d10f71. index-docs. js en el panel Editor"  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Ilustración 3: edición de CSS en el panel Editor para cambiar el color del texto del subtítulo a rojo"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Ilustración 4: edición de JavaScript en el panel Editor"  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Ilustración 5: un miniprograma que inserta la biblioteca jQuery en una página"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Ilustración 6: depurar JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Editar archivos con áreas de trabajo"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origen-estándar HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Marcos | RELATIVA"  

> [!NOTE]
> <span data-ttu-id="4ec43-189">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ec43-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4ec43-190">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/sources) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4ec43-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4ec43-192">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ec43-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
