---
title: Referencia de API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: efa03e02813d718514f73445bc0dceb3a1a83f39
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708903"
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

# <span data-ttu-id="71f04-103">Referencia de API de utilidades de consola</span><span class="sxs-lookup"><span data-stu-id="71f04-103">Console Utilities API Reference</span></span>  

<span data-ttu-id="71f04-104">La API de utilidades de consola contiene una colección de comandos útiles para realizar tareas comunes: seleccionar e inspeccionar elementos de DOM, Mostrar datos en formato legible, detener e iniciar el generador de perfiles y supervisar eventos de DOM.</span><span class="sxs-lookup"><span data-stu-id="71f04-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="71f04-105">Los siguientes comandos solo funcionan en la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="71f04-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="71f04-106">Los comandos no funcionan si se ejecutan desde las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="71f04-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="71f04-107">¿Busca `console.log()` , `console.error()` y el resto de los `console.*` métodos?</span><span class="sxs-lookup"><span data-stu-id="71f04-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="71f04-108">Consulte [referencia][DevToolsConsoleApi]de la API de consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="71f04-109">Expresión evaluada recientemente</span><span class="sxs-lookup"><span data-stu-id="71f04-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="71f04-110">Devuelve el valor de la expresión evaluada más reciente.</span><span class="sxs-lookup"><span data-stu-id="71f04-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="71f04-111">En la siguiente ilustración, se evalúa una expresión simple \ ( `2 + 2` \).</span><span class="sxs-lookup"><span data-stu-id="71f04-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="71f04-112">`$_`A continuación, se evalúa la propiedad, que contiene el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="71f04-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ es la expresión evaluada más recientemente" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="71f04-114">Ilustración 1: `$_` es la expresión evaluada más reciente</span><span class="sxs-lookup"><span data-stu-id="71f04-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-115">En la siguiente ilustración, la expresión evaluada inicialmente contiene una matriz de nombres.</span><span class="sxs-lookup"><span data-stu-id="71f04-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="71f04-116">Si se evalúa `$_.length` para encontrar la longitud de la matriz, el valor almacenado en `$_` los cambios se convertirá en la última expresión evaluada, `4` .</span><span class="sxs-lookup"><span data-stu-id="71f04-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ cambios cuando se evalúan nuevos comandos" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="71f04-118">Ilustración 2: `$_` cambios cuando se evalúan nuevos comandos</span><span class="sxs-lookup"><span data-stu-id="71f04-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <span data-ttu-id="71f04-119">Elemento o objeto JavaScript recientemente seleccionados</span><span class="sxs-lookup"><span data-stu-id="71f04-119">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="71f04-120">Devuelve el último elemento o objeto JavaScript seleccionado.</span><span class="sxs-lookup"><span data-stu-id="71f04-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="71f04-121">Devuelve la segunda versión seleccionada recientemente, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="71f04-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="71f04-122">Los `$0` comandos,,, `$1` `$2` `$3` y `$4` funcionan como referencia histórica a los últimos cinco elementos DOM inspeccionados en el panel **elementos** o los últimos cinco objetos del montón de JavaScript seleccionados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="71f04-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

<span data-ttu-id="71f04-123">En la siguiente ilustración, `img` se selecciona un elemento en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="71f04-123">In the following figure, an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="71f04-124">En el cajón de **consola** , se ha `$0` evaluado y muestra el mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="71f04-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="El $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="71f04-126">Ilustración 3: el</span><span class="sxs-lookup"><span data-stu-id="71f04-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="71f04-127">En la siguiente ilustración, la imagen muestra un elemento diferente seleccionado en la misma página.</span><span class="sxs-lookup"><span data-stu-id="71f04-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="71f04-128">`$0`Ahora hace referencia al elemento que acaba de seleccionarse, mientras `$1` devuelve la selección.</span><span class="sxs-lookup"><span data-stu-id="71f04-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="El $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="71f04-130">Ilustración 4: el</span><span class="sxs-lookup"><span data-stu-id="71f04-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <span data-ttu-id="71f04-131">Selector de consultas</span><span class="sxs-lookup"><span data-stu-id="71f04-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="71f04-132">Devuelve la referencia al primer elemento DOM con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="71f04-133">Este método es un alias para el método [Document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="71f04-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="71f04-134">En la siguiente ilustración, se devuelve una referencia al primer `<img>` elemento en el documento.</span><span class="sxs-lookup"><span data-stu-id="71f04-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ (' IMG ')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="71f04-136">Ilustración 5: el</span><span class="sxs-lookup"><span data-stu-id="71f04-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="71f04-137">Mantenga el puntero sobre el resultado devuelto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **Mostrar en el panel de elementos** para encontrarlo en el Dom o **Desplácese hasta la vista** para mostrarlo en la página.</span><span class="sxs-lookup"><span data-stu-id="71f04-137">Hover on the returned result, open the contextual menu \(right-click\), and select **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="71f04-138">En la siguiente ilustración, se devuelve una referencia al elemento que está seleccionado y se muestra la propiedad src.</span><span class="sxs-lookup"><span data-stu-id="71f04-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="El $ (' IMG '). src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="71f04-140">Ilustración 6: el</span><span class="sxs-lookup"><span data-stu-id="71f04-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="71f04-141">Este método también admite un segundo parámetro, startNode, que especifica un "elemento" o un nodo desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="71f04-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="71f04-142">El valor predeterminado del parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="71f04-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="71f04-143">En la siguiente ilustración, el primer `img` elemento se encuentra después de `title--image` y muestra que `src` se devuelve correctamente.</span><span class="sxs-lookup"><span data-stu-id="71f04-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ (' IMG ', Document. querySelector (' title--Image ')). src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="71f04-145">Ilustración 7: el</span><span class="sxs-lookup"><span data-stu-id="71f04-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71f04-146">Si está usando una biblioteca, como jQuery, que usa `$` , la funcionalidad se sobrescribe y se `$` corresponde con la implementación de esa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="71f04-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="71f04-147">Selector de consulta todo</span><span class="sxs-lookup"><span data-stu-id="71f04-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="71f04-148">Devuelve una matriz de elementos que coincide con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="71f04-149">Este método es equivalente a llamar al método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="71f04-149">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="71f04-150">En el siguiente ejemplo de código y Ilustración, use `$$()` para crear una matriz de todos los `<img>` elementos en el documento actual y mostrar el valor de la `src` propiedad para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="71f04-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Uso de $ $ () para seleccionar todas las imágenes del documento y mostrar las fuentes" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="71f04-152">Ilustración 8: usar `$$()` para seleccionar todas las imágenes del documento y mostrar las fuentes</span><span class="sxs-lookup"><span data-stu-id="71f04-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-153">Este método también admite un segundo parámetro, startNode, que especifica un nodo o elemento desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="71f04-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="71f04-154">El valor predeterminado del parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="71f04-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="71f04-155">En el siguiente ejemplo de código y figura, una versión modificada de la muestra de código anterior y la ilustración usa `$$()` para crear una matriz de todos los `<img>` elementos que aparecen en el documento actual después del nodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="71f04-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usar $ $ () para seleccionar todas las imágenes que aparecen después del elemento <div> especificado en el documento y mostrar los orígenes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="71f04-157">Ilustración 9: usar `$$()` para seleccionar todas las imágenes que aparecen después del `<div>` elemento especificado en el documento y mostrar los orígenes</span><span class="sxs-lookup"><span data-stu-id="71f04-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71f04-158">Pulse `Shift` + `Enter` en la consola para iniciar una nueva línea sin ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="71f04-158">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="71f04-159">Instrucción</span><span class="sxs-lookup"><span data-stu-id="71f04-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="71f04-160">Devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="71f04-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="71f04-161">En el siguiente ejemplo de código y figura, `<p>` se devuelven todos los elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="71f04-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usar un selector XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="71f04-163">Ilustración 10: uso de un selector XPath</span><span class="sxs-lookup"><span data-stu-id="71f04-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-164">En el siguiente ejemplo de código y figura, `<p>` se devuelven todos los elementos que contienen `<a>` elementos.</span><span class="sxs-lookup"><span data-stu-id="71f04-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usar un selector de XPath más complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="71f04-166">Ilustración 11: usar un selector de XPath más complicado</span><span class="sxs-lookup"><span data-stu-id="71f04-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-167">Es similar a los otros comandos del selector, `$x(path)` tiene un segundo parámetro opcional, `startNode` que especifica un elemento o nodo desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="71f04-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usar un selector XPath con startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="71f04-169">Ilustración 12: uso de un selector XPath con</span><span class="sxs-lookup"><span data-stu-id="71f04-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <span data-ttu-id="71f04-170">Libere</span><span class="sxs-lookup"><span data-stu-id="71f04-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="71f04-171">Borra la consola del historial.</span><span class="sxs-lookup"><span data-stu-id="71f04-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="71f04-172">copy</span><span class="sxs-lookup"><span data-stu-id="71f04-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="71f04-173">El `copy(object)` método copia una representación de cadena del objeto especificado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="71f04-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="71f04-174">depurar</span><span class="sxs-lookup"><span data-stu-id="71f04-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="71f04-175">El [#1050237 de problemas de cromo][MonorailIssue1050237] está realizando un seguimiento de un error con la `debug()` función.</span><span class="sxs-lookup"><span data-stu-id="71f04-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="71f04-176">Si encuentra el problema, pruebe a [usar puntos de interrupción][DevtoolsJavascriptBreakpoints] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="71f04-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="71f04-177">Cuando se solicita el método especificado, se invoca el depurador y se interrumpe dentro del método en el panel de **fuentes** , lo que permite recorrer el código y depurarlo.</span><span class="sxs-lookup"><span data-stu-id="71f04-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Interrumpir dentro de un método con debug ()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="71f04-179">Ilustración 13: interrumpir un método con</span><span class="sxs-lookup"><span data-stu-id="71f04-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="71f04-180">Use `undebug(method)` este modo para detener la ruptura en el método o use la interfaz de usuario para deshabilitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="71f04-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="71f04-181">Para obtener más información sobre puntos de interrupción, vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="71f04-181">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="71f04-182">dir</span><span class="sxs-lookup"><span data-stu-id="71f04-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="71f04-183">Muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="71f04-184">Este método es un alias para el método [Console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="71f04-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="71f04-185">Evalúe `document.head` en la consola para mostrar el código HTML entre `<head>` las `</head>` etiquetas y.</span><span class="sxs-lookup"><span data-stu-id="71f04-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="71f04-186">En el siguiente ejemplo de código y figura, se muestra una lista de estilo de objeto después `console.dir()` de usar en la consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registro de documento. Head con el método DIR ()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="71f04-188">Ilustración 14: registrar `document.head` con el `dir()` método</span><span class="sxs-lookup"><span data-stu-id="71f04-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-189">Para obtener más información, consulte la [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrada en la API de consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-189">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="71f04-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="71f04-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="71f04-191">Imprime una representación XML del objeto especificado, como se muestra en la pestaña **elementos** .  Este método es equivalente al método [Console. dirxml ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="71f04-191">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="71f04-192">controlados</span><span class="sxs-lookup"><span data-stu-id="71f04-192">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="71f04-193">Abre y selecciona el elemento u objeto especificado en el panel correspondiente: el panel **elementos** de los elementos DOM o el panel **memoria** para los objetos del montón JavaScript.</span><span class="sxs-lookup"><span data-stu-id="71f04-193">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="71f04-194">En el siguiente ejemplo de código y figura, el `document.body` se abre en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="71f04-194">In the following code sample and figure, the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspeccionar un elemento con inspeccionar ()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="71f04-196">Ilustración 15: inspeccionar un elemento con</span><span class="sxs-lookup"><span data-stu-id="71f04-196">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="71f04-197">Cuando pase un método para inspeccionar, el método abrirá el documento en el panel **orígenes** para que lo inspeccione.</span><span class="sxs-lookup"><span data-stu-id="71f04-197">When passing a method to inspect, the method opens the document in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="71f04-198">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="71f04-198">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="71f04-199">Devuelve los agentes de escucha de eventos registrados en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-199">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="71f04-200">El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \ (como `click` o `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="71f04-200">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="71f04-201">Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="71f04-201">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="71f04-202">En la siguiente ilustración de ejemplo de código, se enumeran todos los agentes de escucha de eventos registrados en el objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="71f04-202">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Resultado de usar getEventListeners (Document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="71f04-204">Ilustración 16: el resultado de usar</span><span class="sxs-lookup"><span data-stu-id="71f04-204">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="71f04-205">Si hay más de un agente de escucha registrado en el objeto especificado, la matriz contendrá un miembro para cada agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="71f04-205">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="71f04-206">En la siguiente ilustración, hay dos escuchas de eventos registradas en el elemento de documento para el `click` evento.</span><span class="sxs-lookup"><span data-stu-id="71f04-206">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Varios agentes de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="71f04-208">Ilustración 17: varios agentes de escucha</span><span class="sxs-lookup"><span data-stu-id="71f04-208">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-209">Puede expandir aún más cada uno de los siguientes objetos para explorar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="71f04-209">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vista expandida del objeto Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="71f04-211">Ilustración 18: vista ampliada del objeto Listener</span><span class="sxs-lookup"><span data-stu-id="71f04-211">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <span data-ttu-id="71f04-212">teclas</span><span class="sxs-lookup"><span data-stu-id="71f04-212">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="71f04-213">Devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-213">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="71f04-214">Para obtener los valores asociados de las mismas propiedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="71f04-214">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="71f04-215">Por ejemplo, supongamos que su aplicación ha definido el siguiente objeto.</span><span class="sxs-lookup"><span data-stu-id="71f04-215">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="71f04-216">En los siguientes ejemplos de código y la figura, el resultado se ha dado por sentado que `player1` se definió en el espacio de nombres global \ (para simplificar \) antes de escribir `keys(player1)` y `values(player1)` en la consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-216">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Los comandos Keys () y Values ()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="71f04-218">Ilustración 19: `keys()` comandos y `values()`</span><span class="sxs-lookup"><span data-stu-id="71f04-218">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <span data-ttu-id="71f04-219">monitor</span><span class="sxs-lookup"><span data-stu-id="71f04-219">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="71f04-220">Registra un mensaje en la consola que indica el nombre del método junto con los argumentos que se pasan al método cuando se llamó.</span><span class="sxs-lookup"><span data-stu-id="71f04-220">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="El método monitor ()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="71f04-222">Ilustración 20: el `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="71f04-222">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-223">Usar `unmonitor(method)` para cesar la supervisión.</span><span class="sxs-lookup"><span data-stu-id="71f04-223">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="71f04-224">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="71f04-224">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="71f04-225">Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-225">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="71f04-226">Puede especificar un solo evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="71f04-226">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="71f04-227">Consulta la siguiente muestra de código y la figura.</span><span class="sxs-lookup"><span data-stu-id="71f04-227">See the following code sample and figure.</span></span>  

<span data-ttu-id="71f04-228">El siguiente monitor supervisa todos los eventos de cambiar tamaño en el objeto Window.</span><span class="sxs-lookup"><span data-stu-id="71f04-228">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Supervisión de eventos de la ventana de supervisión" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="71f04-230">Ilustración 21: supervisión de los eventos de la ventana de supervisión</span><span class="sxs-lookup"><span data-stu-id="71f04-230">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="71f04-231">En el procedimiento siguiente se define una matriz para supervisar ambos `resize` `scroll` eventos y eventos en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="71f04-231">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="71f04-232">También puede especificar uno de los tipos de eventos disponibles, cadenas que se asignan a conjuntos de eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="71f04-232">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="71f04-233">En la tabla siguiente se muestran los tipos de eventos disponibles y las asignaciones de eventos asociadas.</span><span class="sxs-lookup"><span data-stu-id="71f04-233">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="71f04-234">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="71f04-234">Event type</span></span> | <span data-ttu-id="71f04-235">Eventos asignados correspondientes</span><span class="sxs-lookup"><span data-stu-id="71f04-235">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="71f04-236">"click", "DblClick", "MouseDown", "MouseMove", "mouseout", "mouseover", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="71f04-236">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="71f04-237">"KeyDown", "KeyPress", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="71f04-237">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="71f04-238">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="71f04-238">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="71f04-239">"desenfocar", "cambiar", "foco", "restablecer", "cambiar tamaño", "desplazar", "seleccionar", "enviar", "hacer zoom"</span><span class="sxs-lookup"><span data-stu-id="71f04-239">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="71f04-240">En el siguiente ejemplo de código, el `key` tipo de evento correspondiente a `key` los eventos de un campo de texto de entrada está actualmente seleccionado en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="71f04-240">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="71f04-241">En la siguiente ilustración, se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.</span><span class="sxs-lookup"><span data-stu-id="71f04-241">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Supervisión de eventos clave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="71f04-243">Ilustración 22: supervisión de eventos clave</span><span class="sxs-lookup"><span data-stu-id="71f04-243">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <span data-ttu-id="71f04-244">profile</span><span class="sxs-lookup"><span data-stu-id="71f04-244">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="71f04-245">Inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.</span><span class="sxs-lookup"><span data-stu-id="71f04-245">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="71f04-246">El método [profileEnd ()](#profileend) completa el perfil y muestra los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="71f04-246">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="71f04-247">Ejecute el `profile()` método para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="71f04-247">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="71f04-248">Ejecuta el método [profileEnd ()](#profileend) para detener la generación de perfiles y mostrar los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="71f04-248">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="71f04-249">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="71f04-249">Profiles may also be nested.</span></span>  <span data-ttu-id="71f04-250">En los siguientes ejemplos de código y figura el resultado es el mismo, independientemente del orden.</span><span class="sxs-lookup"><span data-stu-id="71f04-250">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="71f04-251">Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.</span><span class="sxs-lookup"><span data-stu-id="71f04-251">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="71f04-252">profileEnd</span><span class="sxs-lookup"><span data-stu-id="71f04-252">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="71f04-253">Completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="71f04-253">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="71f04-254">Debes estar ejecutando el método [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="71f04-254">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="71f04-255">Ejecuta el método [Profile ()](#profile) para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="71f04-255">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="71f04-256">Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="71f04-256">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="71f04-257">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="71f04-257">Profiles may also be nested.</span></span>  <span data-ttu-id="71f04-258">En el siguiente ejemplo de código y figura el resultado es el mismo, independientemente del orden.</span><span class="sxs-lookup"><span data-stu-id="71f04-258">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="71f04-259">El resultado aparece como una instantánea de montones en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="71f04-259">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfiles agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="71f04-261">Ilustración 23: perfiles agrupados</span><span class="sxs-lookup"><span data-stu-id="71f04-261">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71f04-262">Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.</span><span class="sxs-lookup"><span data-stu-id="71f04-262">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="71f04-263">queryObjects</span><span class="sxs-lookup"><span data-stu-id="71f04-263">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="71f04-264">Devuelve una matriz de objetos creados con el constructor especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-264">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="71f04-265">El ámbito de `queryObjects()` es el contexto en tiempo de ejecución actualmente seleccionado en la consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-265">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="71f04-266">Devuelve All `Promises` .</span><span class="sxs-lookup"><span data-stu-id="71f04-266">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="71f04-267">Devuelve todos los elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="71f04-267">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="71f04-268">Devuelve todos los objetos de los que se crearon instancias mediante `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="71f04-268">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <span data-ttu-id="71f04-269">Table</span><span class="sxs-lookup"><span data-stu-id="71f04-269">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="71f04-270">Registra datos de objeto con formato de tabla basado en el objeto de datos en con encabezados de columna opcionales.</span><span class="sxs-lookup"><span data-stu-id="71f04-270">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="71f04-271">En el siguiente ejemplo de código y figura, se muestra una lista de nombres que usan una tabla de la consola.</span><span class="sxs-lookup"><span data-stu-id="71f04-271">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="El resultado del método Table ()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="71f04-273">Ilustración 24: el resultado del `table()` método</span><span class="sxs-lookup"><span data-stu-id="71f04-273">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <span data-ttu-id="71f04-274">despurar</span><span class="sxs-lookup"><span data-stu-id="71f04-274">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="71f04-275">Detiene la depuración del método especificado para que cuando se llame al método se deje de llamar al depurador.</span><span class="sxs-lookup"><span data-stu-id="71f04-275">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="71f04-276">dessupervisar</span><span class="sxs-lookup"><span data-stu-id="71f04-276">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="71f04-277">Detiene la supervisión del método especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-277">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="71f04-278">Este método se usa en conjunto con el método [monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="71f04-278">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="71f04-279">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="71f04-279">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="71f04-280">Detiene la supervisión de eventos para el objeto y los eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="71f04-280">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="71f04-281">Por ejemplo, a continuación se detiene toda la supervisión de eventos en el objeto Window.</span><span class="sxs-lookup"><span data-stu-id="71f04-281">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="71f04-282">También puede dejar de supervisar selectivamente los eventos específicos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="71f04-282">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="71f04-283">Por ejemplo, el siguiente código comienza a supervisar todos los `mouse` eventos del elemento seleccionado actualmente y, a continuación, detiene `mousemove` la supervisión de eventos \ (quizás para reducir el ruido en el resultado de la consola \).</span><span class="sxs-lookup"><span data-stu-id="71f04-283">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="71f04-284">los</span><span class="sxs-lookup"><span data-stu-id="71f04-284">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="71f04-285">Devuelve una matriz que contiene todos los valores de todas las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="71f04-285">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

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
> <span data-ttu-id="71f04-295">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71f04-295">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="71f04-296">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="71f04-296">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="71f04-298">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71f04-298">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
