---
description: Una referencia de comandos de comodidad disponibles en la consola de Microsoft Edge DevTools.
title: Referencia de la API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398829"
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

# <a name="console-utilities-api-reference"></a><span data-ttu-id="49576-104">Referencia de la API de utilidades de consola</span><span class="sxs-lookup"><span data-stu-id="49576-104">Console Utilities API reference</span></span>  

<span data-ttu-id="49576-105">La API de utilidades de consola contiene una colección de comandos de comodidad para realizar tareas comunes: seleccionar e inspeccionar elementos DOM, mostrar datos en formato legible, detener e iniciar el perfilador y supervisar eventos DOM.</span><span class="sxs-lookup"><span data-stu-id="49576-105">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="49576-106">Los siguientes comandos solo funcionan en la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="49576-106">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="49576-107">Los comandos no funcionan si se ejecutan desde los scripts.</span><span class="sxs-lookup"><span data-stu-id="49576-107">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="49576-108">Para los `console.log()` métodos and `console.error()` del resto de los `console.*` métodos, vaya a [Console API Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="49576-108">For the `console.log()` and `console.error()` methods the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="49576-109">Expresión recientemente evaluada</span><span class="sxs-lookup"><span data-stu-id="49576-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="49576-110">Devuelve el valor de la expresión evaluada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="49576-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="49576-111">En la siguiente figura, se evalúa una expresión sencilla \( `2 + 2` \).</span><span class="sxs-lookup"><span data-stu-id="49576-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="49576-112">A `$_` continuación, se evalúa la propiedad, que contiene el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="49576-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ es la expresión evaluada más recientemente" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="49576-114">Figura 1:  `$_` es la expresión evaluada más recientemente</span><span class="sxs-lookup"><span data-stu-id="49576-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="49576-115">En la siguiente figura, la expresión evaluada contiene inicialmente una matriz de nombres.</span><span class="sxs-lookup"><span data-stu-id="49576-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="49576-116">Al evaluar para encontrar la longitud de la matriz, el valor almacenado en los cambios para convertirse en `$_.length` `$_` la última expresión evaluada, `4` .</span><span class="sxs-lookup"><span data-stu-id="49576-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ cambia cuando se evalúan nuevos comandos" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="49576-118">Figura 2:  `$_` cambios cuando se evalúan nuevos comandos</span><span class="sxs-lookup"><span data-stu-id="49576-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="49576-119">Elemento elegido recientemente o objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="49576-119">Recently Chosen Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="49576-120">Devuelve el elemento seleccionado más recientemente o el objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49576-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="49576-121">devuelve el segundo seleccionado más recientemente, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="49576-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="49576-122">Los comandos , , y funcionan como una referencia histórica a los últimos cinco elementos DOM inspeccionados dentro de la herramienta Elementos o los últimos cinco objetos de `$0` `$1` montón de `$2` `$3` `$4` JavaScript seleccionados   en la herramienta Memoria.</span><span class="sxs-lookup"><span data-stu-id="49576-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects selected in the **Memory** tool.</span></span>  

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

<span data-ttu-id="49576-123">En la siguiente figura, se `img` selecciona un elemento en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-123">In the following figure, an `img` element is selected in the **Elements** tool.</span></span>  <span data-ttu-id="49576-124">En el **cajón** de consola, `$0` se ha evaluado y muestra el mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="49576-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Los $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="49576-126">Figura 3: La</span><span class="sxs-lookup"><span data-stu-id="49576-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="49576-127">En la siguiente figura, la imagen muestra un elemento diferente seleccionado en la misma página.</span><span class="sxs-lookup"><span data-stu-id="49576-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="49576-128">Ahora `$0` hace referencia al elemento recién seleccionado, mientras que devuelve el seleccionado `$1` anteriormente.</span><span class="sxs-lookup"><span data-stu-id="49576-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="El $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="49576-130">Figura 4: La</span><span class="sxs-lookup"><span data-stu-id="49576-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <a name="query-selector"></a><span data-ttu-id="49576-131">Selector de consultas</span><span class="sxs-lookup"><span data-stu-id="49576-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="49576-132">Devuelve la referencia al primer elemento DOM con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="49576-133">Este método es un alias para el [método document.querySelector().][MDNDocumentQuerySelector]</span><span class="sxs-lookup"><span data-stu-id="49576-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="49576-134">En la figura siguiente, se devuelve una referencia al primer `<img>` elemento del documento.</span><span class="sxs-lookup"><span data-stu-id="49576-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="El $('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="49576-136">Figura 5: La</span><span class="sxs-lookup"><span data-stu-id="49576-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="49576-137">Mantenga el mouse sobre el resultado devuelto, abra el menú contextual \(hacer clic con  el botón secundario\) y elija Mostrar en el **Panel** de elementos para encontrarlo en el DOM o Desplazarse hasta Ver para mostrarlo en la página.</span><span class="sxs-lookup"><span data-stu-id="49576-137">Hover on the returned result, open the contextual menu \(right-click\), and choose **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="49576-138">En la siguiente figura, se devuelve una referencia al elemento seleccionado actualmente y se muestra la propiedad src.</span><span class="sxs-lookup"><span data-stu-id="49576-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="El $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="49576-140">Figura 6: La</span><span class="sxs-lookup"><span data-stu-id="49576-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="49576-141">Este método también admite un segundo parámetro, startNode, que especifica un "elemento" o Node desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="49576-142">El valor predeterminado del parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="49576-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="49576-143">En la siguiente figura, se encuentra el primer elemento después de que se devuelve el elemento `img` `title--image` y muestra el `src` correcto.</span><span class="sxs-lookup"><span data-stu-id="49576-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="El $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="49576-145">Figura 7: La</span><span class="sxs-lookup"><span data-stu-id="49576-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="49576-146">Si usa una biblioteca como jQuery que usa , la funcionalidad se sobrescribe y corresponde a la implementación `$` `$` de esa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="49576-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <a name="query-selector-all"></a><span data-ttu-id="49576-147">Selector de consultas todo</span><span class="sxs-lookup"><span data-stu-id="49576-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="49576-148">Devuelve una matriz de elementos que coinciden con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="49576-149">Este método equivale a ejecutar el [método document.querySelectorAll().][MDNDocumentQuerySelectorAll]</span><span class="sxs-lookup"><span data-stu-id="49576-149">This method is equivalent to running the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="49576-150">En el siguiente ejemplo de código y figura, se usa para crear una matriz de todos los elementos del documento actual y mostrar el valor de la propiedad `$$()` `<img>` para cada `src` elemento.</span><span class="sxs-lookup"><span data-stu-id="49576-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Uso de $$() para seleccionar todas las imágenes del documento y mostrar los orígenes" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="49576-152">Figura 8: Usar `$$()` para seleccionar todas las imágenes del documento y mostrar los orígenes</span><span class="sxs-lookup"><span data-stu-id="49576-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="49576-153">Este método también admite un segundo parámetro, startNode, que especifica un elemento o Node desde el que buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="49576-154">El valor predeterminado del parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="49576-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="49576-155">En la siguiente ilustración y ejemplo de código, se usa una versión modificada del ejemplo de código y la figura anteriores para crear una matriz de todos los elementos que aparecen en el documento actual después del `$$()` `<img>` nodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="49576-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Uso de $$() para seleccionar todas las imágenes que aparecen después del elemento div <div> especificado en el documento y mostrar los orígenes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="49576-157">Figura 9: Usar para seleccionar todas las imágenes que aparecen después del elemento especificado en el documento y `$$()` `<div>` mostrar los orígenes</span><span class="sxs-lookup"><span data-stu-id="49576-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="49576-158">Seleccione `Shift` + `Enter` en la consola para iniciar una nueva línea sin ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="49576-158">Select `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <a name="xpath"></a><span data-ttu-id="49576-159">XPath</span><span class="sxs-lookup"><span data-stu-id="49576-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="49576-160">Devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="49576-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="49576-161">En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="49576-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Uso de un selector XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="49576-163">Figura 10: Uso de un selector XPath</span><span class="sxs-lookup"><span data-stu-id="49576-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="49576-164">En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos que contienen `<a>` elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Uso de un selector XPath más complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="49576-166">Figura 11: Uso de un selector XPath más complicado</span><span class="sxs-lookup"><span data-stu-id="49576-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="49576-167">Al igual que los demás comandos de selector, tiene un segundo parámetro opcional, , que especifica un elemento o Node desde el que buscar `$x(path)` `startNode` elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Uso de un selector XPath con startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="49576-169">Figura 12: Uso de un selector XPath con</span><span class="sxs-lookup"><span data-stu-id="49576-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <a name="clear"></a><span data-ttu-id="49576-170">clear</span><span class="sxs-lookup"><span data-stu-id="49576-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="49576-171">Borra la consola del historial.</span><span class="sxs-lookup"><span data-stu-id="49576-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="49576-172">copy</span><span class="sxs-lookup"><span data-stu-id="49576-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="49576-173">El `copy(object)` método copia una representación de cadena del objeto especificado en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="49576-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <a name="debug"></a><span data-ttu-id="49576-174">depurar</span><span class="sxs-lookup"><span data-stu-id="49576-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="49576-175">El [problema chromium #1050237][MonorailIssue1050237] está rastreando un error con la `debug()` función.</span><span class="sxs-lookup"><span data-stu-id="49576-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="49576-176">Si encuentra el problema, intente [usar puntos de interrupción en][DevtoolsJavascriptBreakpoints] su lugar.</span><span class="sxs-lookup"><span data-stu-id="49576-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="49576-177">Cuando se solicita el método especificado, se invoca al depurador y se interrumpe dentro del método en la herramienta **Orígenes,** lo que le permite pasar por el código y depurarlo.</span><span class="sxs-lookup"><span data-stu-id="49576-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** tool allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Irrumpir dentro de un método con debug()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="49576-179">Figura 13: Dividir dentro de un método con</span><span class="sxs-lookup"><span data-stu-id="49576-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="49576-180">Se `undebug(method)` usa para detener la interrupción del método o usar la interfaz de usuario para deshabilitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="49576-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="49576-181">Para obtener más información sobre los puntos de interrupción, vaya [a Pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="49576-181">For more information on breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="dir"></a><span data-ttu-id="49576-182">dir</span><span class="sxs-lookup"><span data-stu-id="49576-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="49576-183">Muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="49576-184">Este método es un alias para el [método console.dir().][MDNConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="49576-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="49576-185">Evalúe `document.head` en la consola para mostrar el HTML entre las `<head>` `</head>` etiquetas y.</span><span class="sxs-lookup"><span data-stu-id="49576-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="49576-186">En el siguiente ejemplo de código y figura, se muestra una descripción de estilo de objeto después de usar `console.dir()` en la consola.</span><span class="sxs-lookup"><span data-stu-id="49576-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registro de document.head con el método dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="49576-188">Figura 14: Registro `document.head` con `dir()` método</span><span class="sxs-lookup"><span data-stu-id="49576-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="49576-189">Para obtener más información, vaya a [`console.dir()`][DevToolsConsoleApiConsoleDirObject] la entrada en la API de consola.</span><span class="sxs-lookup"><span data-stu-id="49576-189">For more information, navigate to [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <a name="dirxml"></a><span data-ttu-id="49576-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="49576-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="49576-191">Imprime una representación XML del objeto especificado, tal como se muestra en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-191">Prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="49576-192">Este método es equivalente al [método console.dirxml().][MDNConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="49576-192">This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <a name="inspect"></a><span data-ttu-id="49576-193">inspeccionar</span><span class="sxs-lookup"><span data-stu-id="49576-193">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="49576-194">Abre y selecciona el elemento u objeto especificado en el panel correspondiente:  la herramienta **Elementos** para elementos DOM o la herramienta Memoria para objetos de montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49576-194">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

<span data-ttu-id="49576-195">En el siguiente ejemplo de código y figura, se `document.body` abre en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-195">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspeccionar un elemento con inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="49576-197">Figura 15: Inspeccionar un elemento con</span><span class="sxs-lookup"><span data-stu-id="49576-197">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="49576-198">Al pasar un método para inspeccionar, el método abre el documento en la **herramienta Orígenes** para que lo examine.</span><span class="sxs-lookup"><span data-stu-id="49576-198">When passing a method to inspect, the method opens the document in the **Sources** tool for you to inspect.</span></span>  

## <a name="geteventlisteners"></a><span data-ttu-id="49576-199">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="49576-199">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="49576-200">Devuelve los agentes de escucha de eventos registrados en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-200">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="49576-201">El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \(como `click` o `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="49576-201">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="49576-202">Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="49576-202">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="49576-203">En la siguiente figura de ejemplo de código, se enumeran todos los agentes de escucha de eventos registrados en el objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="49576-203">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Resultado del uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="49576-205">Figura 16: El resultado del uso</span><span class="sxs-lookup"><span data-stu-id="49576-205">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="49576-206">Si se registra más de un agente de escucha en el objeto especificado, la matriz contiene un miembro para cada escucha.</span><span class="sxs-lookup"><span data-stu-id="49576-206">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="49576-207">En la siguiente figura, hay dos agentes de escucha de eventos registrados en el elemento de documento para el `click` evento.</span><span class="sxs-lookup"><span data-stu-id="49576-207">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Varios agentes de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="49576-209">Figura 17: Varios agentes de escucha</span><span class="sxs-lookup"><span data-stu-id="49576-209">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="49576-210">Puede expandir cada uno de los siguientes objetos para explorar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="49576-210">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vista expandida del objeto de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="49576-212">Figura 18: Vista expandida del objeto de escucha</span><span class="sxs-lookup"><span data-stu-id="49576-212">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <a name="keys"></a><span data-ttu-id="49576-213">teclas</span><span class="sxs-lookup"><span data-stu-id="49576-213">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="49576-214">Devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-214">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="49576-215">Para obtener los valores asociados de las mismas propiedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="49576-215">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="49576-216">Por ejemplo, supongamos que la aplicación definió el siguiente objeto.</span><span class="sxs-lookup"><span data-stu-id="49576-216">For example, suppose your application defined the following object.</span></span>  

```console
var player1 =   
```  

<span data-ttu-id="49576-217">En los siguientes ejemplos de código y figura, se supone que el resultado se definió en el espacio de nombres global \(por simplicidad\) antes de escribir y `player1` `keys(player1)` en la `values(player1)` consola.</span><span class="sxs-lookup"><span data-stu-id="49576-217">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Los comandos keys() y values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="49576-219">Figura 19: Los `keys()` comandos y `values()`</span><span class="sxs-lookup"><span data-stu-id="49576-219">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <a name="monitor"></a><span data-ttu-id="49576-220">monitor</span><span class="sxs-lookup"><span data-stu-id="49576-220">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="49576-221">Registra un mensaje en la consola que indica el nombre del método junto con los argumentos que se pasan al método cuando se llamó.</span><span class="sxs-lookup"><span data-stu-id="49576-221">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="El método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="49576-223">Figura 20: El `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="49576-223">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="49576-224">Se `unmonitor(method)` usa para dejar de supervisar.</span><span class="sxs-lookup"><span data-stu-id="49576-224">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <a name="monitorevents"></a><span data-ttu-id="49576-225">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="49576-225">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="49576-226">Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="49576-226">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="49576-227">Puede especificar un único evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="49576-227">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="49576-228">Revise el siguiente ejemplo de código y figura.</span><span class="sxs-lookup"><span data-stu-id="49576-228">Review the following code sample and figure.</span></span>  

<span data-ttu-id="49576-229">A continuación se supervisan todos los eventos de cambio de tamaño del objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="49576-229">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Eventos de cambio de tamaño de ventana de supervisión" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="49576-231">Figura 21: Eventos de cambio de tamaño de ventana de supervisión</span><span class="sxs-lookup"><span data-stu-id="49576-231">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="49576-232">A continuación se define una matriz para supervisar tanto `resize` los eventos como los del objeto `scroll` window.</span><span class="sxs-lookup"><span data-stu-id="49576-232">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="49576-233">También puede especificar uno de los tipos de eventos disponibles, cadenas que se asignan a conjuntos predefinidos de eventos.</span><span class="sxs-lookup"><span data-stu-id="49576-233">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="49576-234">En la tabla siguiente se muestran los tipos de eventos disponibles y las asignaciones de eventos asociadas.</span><span class="sxs-lookup"><span data-stu-id="49576-234">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="49576-235">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="49576-235">Event type</span></span> | <span data-ttu-id="49576-236">Eventos asignados correspondientes</span><span class="sxs-lookup"><span data-stu-id="49576-236">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="49576-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="49576-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="49576-238">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="49576-238">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="49576-239">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="49576-239">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="49576-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="49576-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="49576-241">En el siguiente ejemplo de código, el tipo de evento correspondiente a los eventos de un campo de texto de entrada se selecciona actualmente `key` `key` en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="49576-241">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="49576-242">En la siguiente figura se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.</span><span class="sxs-lookup"><span data-stu-id="49576-242">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Supervisión de eventos clave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="49576-244">Figura 22: Eventos clave de supervisión</span><span class="sxs-lookup"><span data-stu-id="49576-244">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <a name="profile"></a><span data-ttu-id="49576-245">profile</span><span class="sxs-lookup"><span data-stu-id="49576-245">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="49576-246">Inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.</span><span class="sxs-lookup"><span data-stu-id="49576-246">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="49576-247">El [método profileEnd()](#profileend) completa el perfil y muestra los resultados en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="49576-247">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="49576-248">Ejecute el `profile()` método para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="49576-248">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="49576-249">Ejecute el [método profileEnd()](#profileend) para detener la generación de perfiles y mostrar los resultados en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="49576-249">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="49576-250">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="49576-250">Profiles may also be nested.</span></span>  <span data-ttu-id="49576-251">En los siguientes ejemplos de código y figura, el resultado es el mismo independientemente del orden.</span><span class="sxs-lookup"><span data-stu-id="49576-251">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="49576-252">Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.</span><span class="sxs-lookup"><span data-stu-id="49576-252">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="profileend"></a><span data-ttu-id="49576-253">profileEnd</span><span class="sxs-lookup"><span data-stu-id="49576-253">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="49576-254">Completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="49576-254">Completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="49576-255">Debe ejecutar el método [profile().](#profile)</span><span class="sxs-lookup"><span data-stu-id="49576-255">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="49576-256">Ejecute el [método profile()](#profile) para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="49576-256">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="49576-257">Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en la herramienta **Memoria.**</span><span class="sxs-lookup"><span data-stu-id="49576-257">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="49576-258">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="49576-258">Profiles may also be nested.</span></span>  <span data-ttu-id="49576-259">En el siguiente ejemplo de código y figura, el resultado es el mismo independientemente del orden.</span><span class="sxs-lookup"><span data-stu-id="49576-259">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="49576-260">El resultado aparece como una instantánea de montón en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="49576-260">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfiles agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="49576-262">Figura 23: Perfiles agrupados</span><span class="sxs-lookup"><span data-stu-id="49576-262">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="49576-263">Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.</span><span class="sxs-lookup"><span data-stu-id="49576-263">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="queryobjects"></a><span data-ttu-id="49576-264">queryObjects</span><span class="sxs-lookup"><span data-stu-id="49576-264">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="49576-265">Devuelve una matriz de objetos creados con el constructor especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-265">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="49576-266">El ámbito de `queryObjects()` es el contexto de tiempo de ejecución seleccionado actualmente en la consola.</span><span class="sxs-lookup"><span data-stu-id="49576-266">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="49576-267">Devuelve todo `Promises` .</span><span class="sxs-lookup"><span data-stu-id="49576-267">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="49576-268">Devuelve todos los elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="49576-268">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="49576-269">Devuelve todos los objetos que se crearon instancias mediante `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="49576-269">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="49576-270">tabla</span><span class="sxs-lookup"><span data-stu-id="49576-270">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="49576-271">Registra los datos del objeto con formato de tabla en función del objeto de datos con encabezados de columna opcionales.</span><span class="sxs-lookup"><span data-stu-id="49576-271">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="49576-272">En el siguiente ejemplo de código y figura, se muestra una lista de nombres que usan una tabla en la consola.</span><span class="sxs-lookup"><span data-stu-id="49576-272">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="El resultado del método table()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="49576-274">Figura 24: El resultado del `table()` método</span><span class="sxs-lookup"><span data-stu-id="49576-274">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <a name="undebug"></a><span data-ttu-id="49576-275">undebug</span><span class="sxs-lookup"><span data-stu-id="49576-275">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="49576-276">Detiene la depuración del método especificado de modo que, cuando se llama al método, ya no se invoca al depurador.</span><span class="sxs-lookup"><span data-stu-id="49576-276">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <a name="unmonitor"></a><span data-ttu-id="49576-277">unmonitor</span><span class="sxs-lookup"><span data-stu-id="49576-277">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="49576-278">Detiene la supervisión del método especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-278">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="49576-279">Este método se usa en función del [método monitor().](#monitor)</span><span class="sxs-lookup"><span data-stu-id="49576-279">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a><span data-ttu-id="49576-280">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="49576-280">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="49576-281">Detiene la supervisión de eventos para el objeto y los eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="49576-281">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="49576-282">Por ejemplo, lo siguiente detiene toda la supervisión de eventos en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="49576-282">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="49576-283">También puede detener selectivamente la supervisión de eventos específicos en un objeto.</span><span class="sxs-lookup"><span data-stu-id="49576-283">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="49576-284">Por ejemplo, el siguiente código inicia la supervisión de todos los eventos del elemento seleccionado actualmente y, a continuación, detiene la supervisión de eventos \(quizás para reducir el ruido en la salida de la `mouse` `mousemove` consola\).</span><span class="sxs-lookup"><span data-stu-id="49576-284">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a><span data-ttu-id="49576-285">valores</span><span class="sxs-lookup"><span data-stu-id="49576-285">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="49576-286">Devuelve una matriz que contiene los valores de todas las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="49576-286">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="49576-287">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49576-287">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de api de consola"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir: referencia de api de consola"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar el tiempo de ejecución de JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: debug(function) no funciona | Monorraíl"  

> [!NOTE]
> <span data-ttu-id="49576-297">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49576-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49576-298">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="49576-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="49576-300">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49576-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
