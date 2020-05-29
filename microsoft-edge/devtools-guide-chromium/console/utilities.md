---
title: Referencia de API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601799"
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





# <span data-ttu-id="c5531-103">Referencia de API de utilidades de consola</span><span class="sxs-lookup"><span data-stu-id="c5531-103">Console Utilities API Reference</span></span>   



<span data-ttu-id="c5531-104">La API de utilidades de consola contiene una colección de comandos útiles para realizar tareas comunes: seleccionar e inspeccionar elementos de DOM, Mostrar datos en formato legible, detener e iniciar el generador de perfiles y supervisar eventos de DOM.</span><span class="sxs-lookup"><span data-stu-id="c5531-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="c5531-105">Los siguientes comandos solo funcionan en la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c5531-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="c5531-106">Los comandos no funcionan si se ejecutan desde las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="c5531-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="c5531-107">¿Busca `console.log()` , `console.error()` y el resto de los `console.*` métodos?</span><span class="sxs-lookup"><span data-stu-id="c5531-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="c5531-108">Consulte [referencia][DevToolsConsoleApi]de la API de consola.</span><span class="sxs-lookup"><span data-stu-id="c5531-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="c5531-109">Expresión evaluada recientemente</span><span class="sxs-lookup"><span data-stu-id="c5531-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="c5531-110">Devuelve el valor de la expresión evaluada más reciente.</span><span class="sxs-lookup"><span data-stu-id="c5531-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="c5531-111">En la [Ilustración 1](#figure-1), se evalúa una expresión simple \ ( `2 + 2` \).</span><span class="sxs-lookup"><span data-stu-id="c5531-111">In [Figure 1](#figure-1), a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="c5531-112">`$_`A continuación, se evalúa la propiedad, que contiene el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="c5531-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

> ##### <span data-ttu-id="c5531-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="c5531-113">Figure 1</span></span>  
> `$_` <span data-ttu-id="c5531-114">es la expresión evaluada más reciente</span><span class="sxs-lookup"><span data-stu-id="c5531-114">is the most recently evaluated expression</span></span>  
> ![$ _ es la expresión evaluada más recientemente][ImageRecentExpression]  

<span data-ttu-id="c5531-116">En la [ilustración 2](#figure-2), la expresión evaluada inicialmente contiene una matriz de nombres.</span><span class="sxs-lookup"><span data-stu-id="c5531-116">In [Figure 2](#figure-2), the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="c5531-117">Si se evalúa `$_.length` para encontrar la longitud de la matriz, el valor almacenado en `$_` los cambios se convertirá en la última expresión evaluada, `4` .</span><span class="sxs-lookup"><span data-stu-id="c5531-117">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

> ##### <span data-ttu-id="c5531-118">Figura 2</span><span class="sxs-lookup"><span data-stu-id="c5531-118">Figure 2</span></span>  
> `$_` <span data-ttu-id="c5531-119">cambios cuando se evalúan nuevos comandos</span><span class="sxs-lookup"><span data-stu-id="c5531-119">changes when new commands are evaluated</span></span>  
> ![$ _ cambios cuando se evalúan nuevos comandos][ImageChangedRecentExpression]  

## <span data-ttu-id="c5531-121">Elemento o objeto JavaScript recientemente seleccionados</span><span class="sxs-lookup"><span data-stu-id="c5531-121">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="c5531-122">Devuelve el último elemento o objeto JavaScript seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c5531-122">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="c5531-123">Devuelve la segunda versión seleccionada recientemente, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="c5531-123">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="c5531-124">Los `$0` comandos,,, `$1` `$2` `$3` y `$4` funcionan como referencia histórica a los últimos cinco elementos DOM inspeccionados en el panel **elementos** o los últimos cinco objetos del montón de JavaScript seleccionados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="c5531-124">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

<span data-ttu-id="c5531-125">En la [figura 3](#figure-3), `img` se selecciona un elemento en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="c5531-125">In [Figure 3](#figure-3), an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="c5531-126">En el cajón de **consola** , se ha `$0` evaluado y muestra el mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="c5531-126">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

> ##### <span data-ttu-id="c5531-127">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="c5531-127">Figure 3</span></span>  
> <span data-ttu-id="c5531-128">El</span><span class="sxs-lookup"><span data-stu-id="c5531-128">The</span></span> `$0`  
> ![El $0][ImageElement0]  

<span data-ttu-id="c5531-130">En la [figura 4](#figure-4), la imagen muestra un elemento diferente seleccionado en la misma página.</span><span class="sxs-lookup"><span data-stu-id="c5531-130">In [Figure 4](#figure-4), the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="c5531-131">`$0`Ahora hace referencia al elemento que acaba de seleccionarse, mientras `$1` devuelve la selección.</span><span class="sxs-lookup"><span data-stu-id="c5531-131">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

> ##### <span data-ttu-id="c5531-132">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="c5531-132">Figure 4</span></span>  
> <span data-ttu-id="c5531-133">El</span><span class="sxs-lookup"><span data-stu-id="c5531-133">The</span></span> `$1`  
> ![El $1][ImageElement1]  

## <span data-ttu-id="c5531-135">Selector de consultas</span><span class="sxs-lookup"><span data-stu-id="c5531-135">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="c5531-136">Devuelve la referencia al primer elemento DOM con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-136">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="c5531-137">Este método es un alias para el método [Document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="c5531-137">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="c5531-138">En la [figura 5](#figure-5), se devuelve una referencia al primer `<img>` elemento en el documento.</span><span class="sxs-lookup"><span data-stu-id="c5531-138">In [Figure 5](#figure-5), a reference to the first `<img>` element in the document is returned.</span></span>  

> ##### <span data-ttu-id="c5531-139">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="c5531-139">Figure 5</span></span>  
> <span data-ttu-id="c5531-140">El</span><span class="sxs-lookup"><span data-stu-id="c5531-140">The</span></span> `$('img')`  
> ![$ (' IMG ')][ImageElementImg]  

<span data-ttu-id="c5531-142">Haga clic con el botón derecho en el resultado devuelto y seleccione **Mostrar en el panel de elementos** para encontrarlo en el Dom, o **Desplácese hasta la vista** para mostrarlo en la página.</span><span class="sxs-lookup"><span data-stu-id="c5531-142">Right-click on the returned result and select **Reveal in Elements Panel** to find it in the DOM, or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="c5531-143">En la [figura 6](#figure-6), se devuelve una referencia al elemento seleccionado actualmente y se muestra la propiedad src.</span><span class="sxs-lookup"><span data-stu-id="c5531-143">In [Figure 6](#figure-6), a reference to the currently selected element is returned and the src property is displayed.</span></span>  

> ##### <span data-ttu-id="c5531-144">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="c5531-144">Figure 6</span></span>  
> <span data-ttu-id="c5531-145">El</span><span class="sxs-lookup"><span data-stu-id="c5531-145">The</span></span> `$('img').src`  
> ![El $ (' IMG '). src][ImageElementImgSource]  

<span data-ttu-id="c5531-147">Este método también admite un segundo parámetro, startNode, que especifica un "elemento" o un nodo desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="c5531-147">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="c5531-148">El valor predeterminado de este parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="c5531-148">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="c5531-149">En la [figura 7](#figure-7), el primer `img` elemento se encuentra después de `title--image` y muestra que `src` se devuelve correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5531-149">In [Figure 7](#figure-7), the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

> ##### <span data-ttu-id="c5531-150">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="c5531-150">Figure 7</span></span>  
> <span data-ttu-id="c5531-151">$ (' IMG ', Document. querySelector (' title--Image ')). src</span><span class="sxs-lookup"><span data-stu-id="c5531-151">The $('img', document.querySelector('title--image')).src</span></span>  
> ![$ (' IMG ', Document. querySelector (' title--Image ')). src][ImageElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="c5531-153">Si está usando una biblioteca, como jQuery, que usa `$` , esta funcionalidad se sobrescribe y se `$` corresponde con la implementación de esa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c5531-153">If you are using a library such as jQuery that uses `$`, this functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="c5531-154">Selector de consulta todo</span><span class="sxs-lookup"><span data-stu-id="c5531-154">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="c5531-155">Devuelve una matriz de elementos que coincide con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-155">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="c5531-156">Este método es equivalente a llamar al método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="c5531-156">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="c5531-157">En la [ilustración 8](#figure-8), `$$()` se usa para crear una matriz de todos los `<img>` elementos en el documento actual y mostrar el valor de la `src` propiedad para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="c5531-157">In [Figure 8](#figure-8), use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="c5531-158">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="c5531-158">Figure 8</span></span>  
> <span data-ttu-id="c5531-159">Usar `$$()` para seleccionar todas las imágenes del documento y mostrar las fuentes</span><span class="sxs-lookup"><span data-stu-id="c5531-159">Using `$$()` to select all images in the document and display the sources</span></span>  
> ![Uso de $ $ () para seleccionar todas las imágenes del documento y mostrar las fuentes][ImageArrayElementImgSource]  

<span data-ttu-id="c5531-161">Este método también admite un segundo parámetro, startNode, que especifica un nodo o elemento desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="c5531-161">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="c5531-162">El valor predeterminado de este parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="c5531-162">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="c5531-163">En la [figura 9](#figure-9), una versión modificada de la [figura 8](#figure-8) usa `$$()` para crear una matriz de todos los `<img>` elementos que aparecen en el documento actual después del nodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c5531-163">In [Figure 9](#figure-9), a modified version of [Figure 8](#figure-8) uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="c5531-164">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="c5531-164">Figure 9</span></span>  
> <span data-ttu-id="c5531-165">Usar `$$()` para seleccionar todas las imágenes que aparecen después del `<div>` elemento especificado en el documento y mostrar los orígenes</span><span class="sxs-lookup"><span data-stu-id="c5531-165">Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
> ![Usar $ $ () para seleccionar todas las imágenes que aparecen después del elemento <div> especificado en el documento y mostrar los orígenes][ImageArrayElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="c5531-167">Pulse `Shift` + `Enter` en la consola para iniciar una nueva línea sin ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="c5531-167">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="c5531-168">Instrucción</span><span class="sxs-lookup"><span data-stu-id="c5531-168">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="c5531-169">Devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="c5531-169">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="c5531-170">En la [figura 10](#figure-10), `<p>` se devuelven todos los elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="c5531-170">In [Figure 10](#figure-10), all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

> ##### <span data-ttu-id="c5531-171">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="c5531-171">Figure 10</span></span>  
> <span data-ttu-id="c5531-172">Usar un selector XPath</span><span class="sxs-lookup"><span data-stu-id="c5531-172">Using an XPath selector</span></span>  
> ![Usar un selector XPath][ImageArrayXpath]  

<span data-ttu-id="c5531-174">En la [ilustración 11](#figure-11), `<p>` `<a>` se devuelven todos los elementos que contienen elementos.</span><span class="sxs-lookup"><span data-stu-id="c5531-174">In [Figure 11](#figure-11), all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

> ##### <span data-ttu-id="c5531-175">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="c5531-175">Figure 11</span></span>  
> <span data-ttu-id="c5531-176">Usar un selector de XPath más complicado</span><span class="sxs-lookup"><span data-stu-id="c5531-176">Using a more complicated XPath selector</span></span>  
> ![Usar un selector de XPath más complicado][ImageArrayXpathChild]  

<span data-ttu-id="c5531-178">Es similar a los otros comandos del selector, `$x(path)` tiene un segundo parámetro opcional, `startNode` que especifica un elemento o nodo desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="c5531-178">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

> ##### <span data-ttu-id="c5531-179">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="c5531-179">Figure 12</span></span>  
> <span data-ttu-id="c5531-180">Usar un selector XPath con</span><span class="sxs-lookup"><span data-stu-id="c5531-180">Using an XPath selector with</span></span> `startNode`  
> ![Usar un selector XPath con startNode][ImageArrayXpathNode]  

## <span data-ttu-id="c5531-182">Libere</span><span class="sxs-lookup"><span data-stu-id="c5531-182">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="c5531-183">Borra la consola del historial.</span><span class="sxs-lookup"><span data-stu-id="c5531-183">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="c5531-184">copy</span><span class="sxs-lookup"><span data-stu-id="c5531-184">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="c5531-185">El `copy(object)` método copia una representación de cadena del objeto especificado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c5531-185">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="c5531-186">depurar</span><span class="sxs-lookup"><span data-stu-id="c5531-186">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="c5531-187">El [#1050237 de problemas de cromo][MonorailIssue1050237] está realizando un seguimiento de un error con la `debug()` función.</span><span class="sxs-lookup"><span data-stu-id="c5531-187">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="c5531-188">Si se produce este problema, pruebe a [usar puntos de interrupción][DevtoolsJavascriptBreakpoints] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c5531-188">If you encounter this issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="c5531-189">Cuando se solicita el método especificado, se invoca el depurador y se interrumpe dentro del método en el panel de **fuentes** , lo que permite recorrer el código y depurarlo.</span><span class="sxs-lookup"><span data-stu-id="c5531-189">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

> ##### <span data-ttu-id="c5531-190">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="c5531-190">Figure 13</span></span>  
> <span data-ttu-id="c5531-191">Interrumpir un método con</span><span class="sxs-lookup"><span data-stu-id="c5531-191">Breaking inside a method with</span></span> `debug()`  
> ![Interrumpir dentro de un método con debug ()][ImageDebugMethod]  

<span data-ttu-id="c5531-193">Use `undebug(method)` este modo para detener la ruptura en el método o use la interfaz de usuario para deshabilitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c5531-193">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="c5531-194">Para obtener más información sobre puntos de interrupción, vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="c5531-194">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="c5531-195">dir</span><span class="sxs-lookup"><span data-stu-id="c5531-195">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="c5531-196">Muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-196">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="c5531-197">Este método es un alias para el método [Console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="c5531-197">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="c5531-198">Evalúe `document.head` en la consola para mostrar el código HTML entre `<head>` las `</head>` etiquetas y.</span><span class="sxs-lookup"><span data-stu-id="c5531-198">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="c5531-199">En la [figura 14](#figure-14), se muestra una lista de estilo de objeto después `console.dir()` de usar en la consola.</span><span class="sxs-lookup"><span data-stu-id="c5531-199">In [Figure 14](#figure-14), an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

> ##### <span data-ttu-id="c5531-200">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="c5531-200">Figure 14</span></span>  
> <span data-ttu-id="c5531-201">Registrar `document.head` con el `dir()` método</span><span class="sxs-lookup"><span data-stu-id="c5531-201">Logging `document.head` with `dir()` method</span></span>  
> ![Registro de documento. Head con el método DIR ()][ImageLogObject]  

<span data-ttu-id="c5531-203">Para obtener más información, consulte la [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrada en la API de consola.</span><span class="sxs-lookup"><span data-stu-id="c5531-203">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="c5531-204">dirxml</span><span class="sxs-lookup"><span data-stu-id="c5531-204">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="c5531-205">Imprime una representación XML del objeto especificado, como se muestra en la pestaña **elementos** .  Este método es equivalente al método [Console. dirxml ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="c5531-205">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="c5531-206">controlados</span><span class="sxs-lookup"><span data-stu-id="c5531-206">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="c5531-207">Abre y selecciona el elemento u objeto especificado en el panel correspondiente: el panel **elementos** de los elementos DOM o el panel **memoria** para los objetos del montón JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c5531-207">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="c5531-208">En la [figura 15](#figure-15), `document.body` se abre el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="c5531-208">In [Figure 15](#figure-15), the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

> ##### <span data-ttu-id="c5531-209">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="c5531-209">Figure 15</span></span>  
> <span data-ttu-id="c5531-210">Inspeccionar un elemento con</span><span class="sxs-lookup"><span data-stu-id="c5531-210">Inspecting an element with</span></span> `inspect()`  
> ![Inspeccionar un elemento con inspeccionar ()][ImageInspectElement]  

<span data-ttu-id="c5531-212">Al pasar un método para inspeccionar, el método abre el documento en el panel **orígenes** para que usted lo examine.</span><span class="sxs-lookup"><span data-stu-id="c5531-212">When passing a method to inspect, the method opens the document up in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="c5531-213">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="c5531-213">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="c5531-214">Devuelve los agentes de escucha de eventos registrados en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-214">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="c5531-215">El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \ (como `click` o `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="c5531-215">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="c5531-216">Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="c5531-216">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="c5531-217">En la [figura 16](#figure-16), se muestran todas las escuchas de eventos registradas en el objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="c5531-217">In [Figure 16](#figure-16), all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

> ##### <span data-ttu-id="c5531-218">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="c5531-218">Figure 16</span></span>  
> <span data-ttu-id="c5531-219">Resultado de usar</span><span class="sxs-lookup"><span data-stu-id="c5531-219">Output of using</span></span> `getEventListeners(document)`  
> ![Resultado de usar getEventListeners (Document)][ImageGetListeners]  

<span data-ttu-id="c5531-221">Si hay más de un agente de escucha registrado en el objeto especificado, la matriz contendrá un miembro para cada agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="c5531-221">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="c5531-222">En la [figura 16](#figure-16), hay dos escuchas de eventos registradas en el elemento de documento para el `click` evento.</span><span class="sxs-lookup"><span data-stu-id="c5531-222">In [Figure 16](#figure-16), there are two event listeners registered on the document element for the `click` event.</span></span>  

> ##### <span data-ttu-id="c5531-223">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="c5531-223">Figure 17</span></span>  
> <span data-ttu-id="c5531-224">Varios agentes de escucha</span><span class="sxs-lookup"><span data-stu-id="c5531-224">Multiple listeners</span></span>  
> ![Varios agentes de escucha][ImageMultipleListeners]  

<span data-ttu-id="c5531-226">Puede expandir aún más cada uno de los siguientes objetos para explorar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="c5531-226">You may further expand each of the following objects to explore the properties.</span></span>  

> ##### <span data-ttu-id="c5531-227">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="c5531-227">Figure 18</span></span>  
> <span data-ttu-id="c5531-228">Vista expandida del objeto Listener</span><span class="sxs-lookup"><span data-stu-id="c5531-228">Expanded view of listener object</span></span>  
> ![Vista expandida del objeto Listener][ImageListenersExpanded]  

## <span data-ttu-id="c5531-230">teclas</span><span class="sxs-lookup"><span data-stu-id="c5531-230">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="c5531-231">Devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-231">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="c5531-232">Para obtener los valores asociados de las mismas propiedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="c5531-232">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="c5531-233">Por ejemplo, supongamos que su aplicación ha definido el siguiente objeto.</span><span class="sxs-lookup"><span data-stu-id="c5531-233">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="c5531-234">En la [figura 19](#figure-19), el resultado `player1` es el que se definió en el espacio de nombres global \ (para simplificar \) antes de escribir `keys(player1)` y `values(player1)` en la consola.</span><span class="sxs-lookup"><span data-stu-id="c5531-234">In [Figure 19](#figure-19), the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### <span data-ttu-id="c5531-235">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="c5531-235">Figure 19</span></span>  
> <span data-ttu-id="c5531-236">Los `keys()` `values()` comandos y</span><span class="sxs-lookup"><span data-stu-id="c5531-236">The `keys()` and `values()` commands</span></span>  
> ![Los comandos Keys () y Values ()][ImageConsoleKeysValues]  

## <span data-ttu-id="c5531-238">monitor</span><span class="sxs-lookup"><span data-stu-id="c5531-238">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="c5531-239">Registra un mensaje en la consola que indica el nombre del método junto con los argumentos que se pasan al método cuando se llamó.</span><span class="sxs-lookup"><span data-stu-id="c5531-239">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### <span data-ttu-id="c5531-240">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="c5531-240">Figure 20</span></span>  
> <span data-ttu-id="c5531-241">El `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="c5531-241">The `monitor()` method</span></span>  
> ![El método monitor ()][ImageConsoleMonitorSum]  

<span data-ttu-id="c5531-243">Usar `unmonitor(method)` para cesar la supervisión.</span><span class="sxs-lookup"><span data-stu-id="c5531-243">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="c5531-244">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="c5531-244">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="c5531-245">Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="c5531-245">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="c5531-246">Puede especificar un solo evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="c5531-246">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="c5531-247">Consulte la [figura 21](#figure-21).</span><span class="sxs-lookup"><span data-stu-id="c5531-247">See [Figure 21](#figure-21).</span></span>  

<span data-ttu-id="c5531-248">El siguiente monitor supervisa todos los eventos de cambiar tamaño en el objeto Window.</span><span class="sxs-lookup"><span data-stu-id="c5531-248">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

> ##### <span data-ttu-id="c5531-249">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="c5531-249">Figure 21</span></span>  
> <span data-ttu-id="c5531-250">Supervisión de eventos de la ventana de supervisión</span><span class="sxs-lookup"><span data-stu-id="c5531-250">Monitoring window resize events</span></span>  
> ![Supervisión de eventos de la ventana de supervisión][ImageMonitorResize]  

<span data-ttu-id="c5531-252">En el procedimiento siguiente se define una matriz para supervisar ambos `resize` `scroll` eventos y eventos en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="c5531-252">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="c5531-253">También puede especificar uno de los tipos de eventos disponibles, cadenas que se asignan a conjuntos de eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="c5531-253">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="c5531-254">En la tabla siguiente se muestran los tipos de eventos disponibles y las asignaciones de eventos asociadas.</span><span class="sxs-lookup"><span data-stu-id="c5531-254">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="c5531-255">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="c5531-255">Event type</span></span> | <span data-ttu-id="c5531-256">Eventos asignados correspondientes</span><span class="sxs-lookup"><span data-stu-id="c5531-256">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="c5531-257">"click", "DblClick", "MouseDown", "MouseMove", "mouseout", "mouseover", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="c5531-257">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="c5531-258">"KeyDown", "KeyPress", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="c5531-258">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="c5531-259">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="c5531-259">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="c5531-260">"desenfocar", "cambiar", "foco", "restablecer", "cambiar tamaño", "desplazar", "seleccionar", "enviar", "hacer zoom"</span><span class="sxs-lookup"><span data-stu-id="c5531-260">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="c5531-261">En la [figura 22](#figure-22), el `key` tipo de evento que corresponde a `key` los eventos en un campo de texto de entrada está actualmente seleccionado en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="c5531-261">In [Figure 22](#figure-22), the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="c5531-262">En la [figura 22](#figure-22) , se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.</span><span class="sxs-lookup"><span data-stu-id="c5531-262">In [Figure 22](#figure-22) the sample output after typing a character in the text field is displayed.</span></span>  

> ##### <span data-ttu-id="c5531-263">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="c5531-263">Figure 22</span></span>  
> <span data-ttu-id="c5531-264">Supervisión de eventos clave</span><span class="sxs-lookup"><span data-stu-id="c5531-264">Monitoring key events</span></span>  
> ![Supervisión de eventos clave][ImageMonitorKey]  

## <span data-ttu-id="c5531-266">profile</span><span class="sxs-lookup"><span data-stu-id="c5531-266">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="c5531-267">Inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.</span><span class="sxs-lookup"><span data-stu-id="c5531-267">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="c5531-268">El método [profileEnd ()](#profileend) completa el perfil y muestra los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="c5531-268">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="c5531-269">Ejecute el `profile()` método para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="c5531-269">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="c5531-270">Ejecuta el método [profileEnd ()](#profileend) para detener la generación de perfiles y mostrar los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="c5531-270">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="c5531-271">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="c5531-271">Profiles may also be nested.</span></span>  <span data-ttu-id="c5531-272">En la [Figura 23](#figure-23) , el resultado es el mismo, independientemente del orden.</span><span class="sxs-lookup"><span data-stu-id="c5531-272">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="c5531-273">Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.</span><span class="sxs-lookup"><span data-stu-id="c5531-273">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="c5531-274">profileEnd</span><span class="sxs-lookup"><span data-stu-id="c5531-274">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="c5531-275">Completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="c5531-275">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="c5531-276">Debes estar ejecutando el método [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="c5531-276">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="c5531-277">Ejecuta el método [Profile ()](#profile) para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="c5531-277">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="c5531-278">Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="c5531-278">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="c5531-279">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="c5531-279">Profiles may also be nested.</span></span>  <span data-ttu-id="c5531-280">En la [Figura 23](#figure-23) , el resultado es el mismo, independientemente del orden.</span><span class="sxs-lookup"><span data-stu-id="c5531-280">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="c5531-281">El resultado aparece como una instantánea de montones en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="c5531-281">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="c5531-282">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="c5531-282">Figure 23</span></span>  
> <span data-ttu-id="c5531-283">Perfiles agrupados</span><span class="sxs-lookup"><span data-stu-id="c5531-283">Grouped profiles</span></span>  
> ![Perfiles agrupados][ImageGroupedProfiles]  

> [!NOTE]
> <span data-ttu-id="c5531-285">Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.</span><span class="sxs-lookup"><span data-stu-id="c5531-285">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="c5531-286">Table</span><span class="sxs-lookup"><span data-stu-id="c5531-286">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="c5531-287">Registra datos de objeto con formato de tabla basado en el objeto de datos en con encabezados de columna opcionales.</span><span class="sxs-lookup"><span data-stu-id="c5531-287">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="c5531-288">En la [figura 24](#figure-24), se muestra una lista de nombres que usan una tabla en la consola.</span><span class="sxs-lookup"><span data-stu-id="c5531-288">In [Figure 24](#figure-24), a list of names using a table in the console is displayed.</span></span>  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

> ##### <span data-ttu-id="c5531-289">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="c5531-289">Figure 24</span></span>  
> <span data-ttu-id="c5531-290">El `table()` método</span><span class="sxs-lookup"><span data-stu-id="c5531-290">The `table()` method</span></span>  
> ![El método Table ()][ImageConsoleTable]  

## <span data-ttu-id="c5531-292">despurar</span><span class="sxs-lookup"><span data-stu-id="c5531-292">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="c5531-293">Detiene la depuración del método especificado para que cuando se llame al método se deje de llamar al depurador.</span><span class="sxs-lookup"><span data-stu-id="c5531-293">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="c5531-294">dessupervisar</span><span class="sxs-lookup"><span data-stu-id="c5531-294">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="c5531-295">Detiene la supervisión del método especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-295">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="c5531-296">Se usa en conjunto con el método [monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="c5531-296">This is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="c5531-297">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="c5531-297">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="c5531-298">Detiene la supervisión de eventos para el objeto y los eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="c5531-298">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="c5531-299">Por ejemplo, a continuación se detiene toda la supervisión de eventos en el objeto Window.</span><span class="sxs-lookup"><span data-stu-id="c5531-299">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="c5531-300">También puede dejar de supervisar selectivamente los eventos específicos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="c5531-300">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="c5531-301">Por ejemplo, el siguiente código comienza a supervisar todos los `mouse` eventos del elemento seleccionado actualmente y, a continuación, detiene `mousemove` la supervisión de eventos \ (quizás para reducir el ruido en el resultado de la consola \).</span><span class="sxs-lookup"><span data-stu-id="c5531-301">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="c5531-302">los</span><span class="sxs-lookup"><span data-stu-id="c5531-302">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="c5531-303">Devuelve una matriz que contiene todos los valores de todas las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c5531-303">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Ilustración 1: $ _ es la expresión evaluada más recientemente"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Ilustración 2: $ _ cambios cuando se evalúan nuevos comandos"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Ilustración 3: $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Ilustración 4: $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Ilustración 5: $ (' IMG ')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Ilustración 6: el $ (' IMG '). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Ilustración 7: $ (' IMG ', Document. querySelector (' title--Image ')). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Ilustración 8: uso de $ $ () para seleccionar todas las imágenes del documento y mostrar las fuentes"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Ilustración 9: uso de $ $ () para seleccionar todas las imágenes que aparecen después de la <especificada div> en el documento y mostrar los orígenes"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Ilustración 10: uso de un selector XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Ilustración 11: usar un selector de XPath más complicado"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Ilustración 12: uso de un selector XPath con startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Ilustración 13: interrumpir un método con debug ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Ilustración 14: registro de Document. Body con el método DIR ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Ilustración 15: inspeccionar un elemento con inspeccionar ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Ilustración 16: resultado de usar getEventListeners (Document)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Ilustración 17: varios agentes de escucha"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Ilustración 18: vista ampliada del objeto Listener"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Ilustración 19: los comandos Keys () y Values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Ilustración 20: el método monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Ilustración 21: supervisión de los eventos de la ventana de supervisión"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Ilustración 22: supervisión de eventos clave"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Ilustración 23: perfiles agrupados"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Ilustración 24: el método Table ()"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "DIR-consola de referencia de API"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar el tiempo de ejecución de JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. dirxml () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: debug (función) no funciona | Monorail"  

> [!NOTE]
> <span data-ttu-id="c5531-337">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c5531-337">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c5531-338">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c5531-338">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c5531-340">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c5531-340">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
