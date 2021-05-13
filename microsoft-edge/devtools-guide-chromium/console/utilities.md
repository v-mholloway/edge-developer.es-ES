---
description: Una referencia de comandos de comodidad disponibles en la Microsoft Edge DevTools Console.
title: Referencia de API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 436f2807c5fab1723ca6cc93fddc68d9ecf12db7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564535"
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
# <a name="console-utilities-api-reference"></a><span data-ttu-id="8f260-104">Referencia de API de utilidades de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-104">Console Utilities API reference</span></span>  

<span data-ttu-id="8f260-105">La API de utilidades de consola contiene una colección de comandos de comodidad para completar las siguientes tareas comunes.</span><span class="sxs-lookup"><span data-stu-id="8f260-105">The Console Utilities API contains a collection of convenience commands to complete the following common tasks.</span></span>  

*   <span data-ttu-id="8f260-106">Elegir e inspeccionar elementos DOM</span><span class="sxs-lookup"><span data-stu-id="8f260-106">Choose and inspect DOM elements</span></span>  
*   <span data-ttu-id="8f260-107">Mostrar datos en formato legible</span><span class="sxs-lookup"><span data-stu-id="8f260-107">Display data in readable format</span></span>  
*   <span data-ttu-id="8f260-108">Detener e iniciar el perfilador</span><span class="sxs-lookup"><span data-stu-id="8f260-108">Stop and start the profiler</span></span>  
*   <span data-ttu-id="8f260-109">Supervisar eventos DOM</span><span class="sxs-lookup"><span data-stu-id="8f260-109">Monitor DOM events</span></span>  
    
> [!WARNING]
> <span data-ttu-id="8f260-110">Los siguientes comandos solo funcionan en la Microsoft Edge DevTools **Console**.</span><span class="sxs-lookup"><span data-stu-id="8f260-110">The following commands only work in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="8f260-111">Los comandos no funcionan si se ejecutan desde los scripts.</span><span class="sxs-lookup"><span data-stu-id="8f260-111">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="8f260-112">Para obtener más información sobre los `console.log()` métodos and `console.error()` y el resto de los `console.*` métodos, vaya a [Console API Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="8f260-112">For more information about the `console.log()` and `console.error()` methods and the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="8f260-113">Expresión recientemente evaluada</span><span class="sxs-lookup"><span data-stu-id="8f260-113">Recently evaluated expression</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-114">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-114">Console syntax</span></span>  

```console
$_
```  

<span data-ttu-id="8f260-115">Este comando devuelve el valor de la expresión evaluada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="8f260-115">This command returns the value of the most recently evaluated expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-116">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-116">Console example</span></span>  

<span data-ttu-id="8f260-117">En la siguiente figura, se evalúa una expresión sencilla \( `2 + 2` \).</span><span class="sxs-lookup"><span data-stu-id="8f260-117">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="8f260-118">A `$_` continuación, se evalúa la propiedad, que contiene el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="8f260-118">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ es la expresión evaluada más recientemente" lightbox="../media/console-arithmatic.msft.png":::
   `$_` <span data-ttu-id="8f260-120">es la expresión evaluada más recientemente</span><span class="sxs-lookup"><span data-stu-id="8f260-120">is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-121">En la siguiente figura, la expresión evaluada contiene inicialmente una matriz de nombres.</span><span class="sxs-lookup"><span data-stu-id="8f260-121">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="8f260-122">Al evaluar para encontrar la longitud de la matriz, el valor almacenado en se convierte en `$_.length` la última expresión `$_` evaluada, `4` .</span><span class="sxs-lookup"><span data-stu-id="8f260-122">Evaluating `$_.length` to find the length of the array, the value stored in `$_` becomes the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ cambia cuando se evalúan nuevos comandos" lightbox="../media/console-array-length.msft.png":::
   `$_` <span data-ttu-id="8f260-124">cambios cuando se evalúan los nuevos comandos</span><span class="sxs-lookup"><span data-stu-id="8f260-124">changes when new commands are evaluated</span></span>  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="8f260-125">Elemento elegido recientemente o objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="8f260-125">Recently chosen element or JavaScript object</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-126">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-126">Console syntax</span></span>  

```console
$0
```  

<span data-ttu-id="8f260-127">Este comando devuelve el elemento elegido más recientemente o el objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8f260-127">This command returns the most recently chosen element or JavaScript object.</span></span>  `$1` <span data-ttu-id="8f260-128">devuelve el segundo elegido más recientemente, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="8f260-128">returns the second most recently chosen one, and so on.</span></span>  <span data-ttu-id="8f260-129">Los comandos , , y funcionan como una referencia histórica a los últimos cinco elementos DOM inspeccionados dentro de la herramienta Elementos o los últimos cinco objetos de montón de `$0` `$1` `$2` `$3` `$4` JavaScript elegidos \*\*\*\* \*\*\*\* en la herramienta Memoria.</span><span class="sxs-lookup"><span data-stu-id="8f260-129">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects chosen in the **Memory** tool.</span></span>  

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
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a><span data-ttu-id="8f260-130">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-130">Console example</span></span>  

<span data-ttu-id="8f260-131">En la siguiente figura, se `img` elige un elemento en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-131">In the following figure, an `img` element is chosen in the **Elements** tool.</span></span>  <span data-ttu-id="8f260-132">En el **cajón** de consola, `$0` se ha evaluado y muestra el mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="8f260-132">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Los $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="8f260-134">El</span><span class="sxs-lookup"><span data-stu-id="8f260-134">The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="8f260-135">En la siguiente figura, la imagen muestra un elemento diferente elegido en la misma página web.</span><span class="sxs-lookup"><span data-stu-id="8f260-135">In the following figure, the image displays a different element chosen in the same webpage.</span></span>  <span data-ttu-id="8f260-136">Ahora `$0` hace referencia al elemento recién elegido, mientras que devuelve el elegido `$1` anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8f260-136">The `$0` now refers to the newly chosen element, while `$1` returns the previously chosen one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="El $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="8f260-138">El</span><span class="sxs-lookup"><span data-stu-id="8f260-138">The</span></span> `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a><span data-ttu-id="8f260-139">Selector de consultas</span><span class="sxs-lookup"><span data-stu-id="8f260-139">Query selector</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-140">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-140">Console syntax</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="8f260-141">Este comando devuelve la referencia al primer elemento DOM con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-141">This command returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="8f260-142">Este método es un alias para el [método document.querySelector().][MdnDocsWebApiDocumentQueryselector]</span><span class="sxs-lookup"><span data-stu-id="8f260-142">This method is an alias for the [document.querySelector()][MdnDocsWebApiDocumentQueryselector] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-143">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-143">Console example</span></span>  

<span data-ttu-id="8f260-144">En la siguiente figura, se devuelve una referencia al primer `<img>` elemento de la página web.</span><span class="sxs-lookup"><span data-stu-id="8f260-144">In the following figure, a reference to the first `<img>` element in the webpage is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="El $('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="8f260-146">El</span><span class="sxs-lookup"><span data-stu-id="8f260-146">The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="8f260-147">Para buscar el primer elemento en el DOM o para buscarlo y mostrarlo en la página web, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8f260-147">To find the first element in the DOM or to find and display it on the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="8f260-148">Mantenga el mouse sobre el resultado devuelto.</span><span class="sxs-lookup"><span data-stu-id="8f260-148">Hover on the returned result.</span></span>  
1.  <span data-ttu-id="8f260-149">Abra el menú contextual \(haga clic con el botón derecho\).</span><span class="sxs-lookup"><span data-stu-id="8f260-149">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="8f260-150">Elija **Mostrar en el Panel de elementos**.</span><span class="sxs-lookup"><span data-stu-id="8f260-150">Choose **Reveal in Elements Panel**.</span></span>  

<span data-ttu-id="8f260-151">En la siguiente figura, se devuelve una referencia al elemento seleccionado actualmente y se `src` muestra la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f260-151">In the following figure, a reference to the currently chosen element is returned and the `src` property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="El $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="8f260-153">El</span><span class="sxs-lookup"><span data-stu-id="8f260-153">The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="8f260-154">Este método también admite un segundo parámetro, , que especifica un elemento o nodo desde el que `startNode` buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-154">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="8f260-155">El valor predeterminado del parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="8f260-155">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="8f260-156">En la siguiente figura, se devuelve el primer elemento después de que se encuentra el elemento y se devuelve la propiedad `img` `title--image` del `src` `img` elemento.</span><span class="sxs-lookup"><span data-stu-id="8f260-156">In the following figure, the first `img` element after the `title--image` element is found, and the `src` property of the `img` element is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="El $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="8f260-158">El</span><span class="sxs-lookup"><span data-stu-id="8f260-158">The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8f260-159">Si usa una biblioteca como jQuery que usa , la funcionalidad se sobrescribe y corresponde a la implementación `$` `$` de esa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8f260-159">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

---  

## <a name="query-selector-all"></a><span data-ttu-id="8f260-160">Selector de consultas todos</span><span class="sxs-lookup"><span data-stu-id="8f260-160">Query selector all</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-161">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-161">Console syntax</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="8f260-162">Este comando devuelve una matriz de elementos que coinciden con el selector CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-162">This command returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="8f260-163">Este método equivale a ejecutar el [método document.querySelectorAll().][MdnDocsWebApiDocumentQueryselectorall]</span><span class="sxs-lookup"><span data-stu-id="8f260-163">This method is equivalent to running the [document.querySelectorAll()][MdnDocsWebApiDocumentQueryselectorall] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-164">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-164">Console example</span></span>  

<span data-ttu-id="8f260-165">En el siguiente ejemplo de código y figura, se usa para crear una matriz de todos los elementos de la página web actual y mostrar el valor de la propiedad `$$()` `<img>` para cada `src` elemento.</span><span class="sxs-lookup"><span data-stu-id="8f260-165">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current webpage and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usar $$() para elegir todas las imágenes de la página web y mostrar los orígenes" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="8f260-167">Usar `$$()` para elegir todas las imágenes de la página web y mostrar los orígenes</span><span class="sxs-lookup"><span data-stu-id="8f260-167">Using `$$()` to choose all images in the webpage and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-168">Este método también admite un segundo parámetro, , que especifica un elemento o nodo desde el que `startNode` buscar elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-168">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="8f260-169">El valor predeterminado del parámetro es `document` .</span><span class="sxs-lookup"><span data-stu-id="8f260-169">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="8f260-170">En la siguiente ilustración y ejemplo de código, una versión modificada del ejemplo de código y la figura anteriores se usa para crear una matriz de todos los elementos que aparecen en la página web actual después del `$$()` `<img>` nodo elegido.</span><span class="sxs-lookup"><span data-stu-id="8f260-170">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current webpage after the chosen node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usar $$() para elegir todas las imágenes que aparecen después del elemento div <div> en la página web y mostrar los orígenes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="8f260-172">Usar para elegir todas las imágenes que aparecen después del elemento especificado en la página `$$()` web y mostrar los `<div>` orígenes</span><span class="sxs-lookup"><span data-stu-id="8f260-172">Using `$$()` to choose all images that appear after the specified `<div>` element in the webpage and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8f260-173">Seleccione `Shift` + `Enter` en la **Consola para** iniciar una nueva línea sin ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="8f260-173">Select `Shift`+`Enter` in the **Console** to start a new line without running the script.</span></span>  

---  

## <a name="xpath"></a><span data-ttu-id="8f260-174">XPath</span><span class="sxs-lookup"><span data-stu-id="8f260-174">XPath</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-175">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-175">Console syntax</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="8f260-176">Este comando devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="8f260-176">This command returns an array of DOM elements that match the specified XPath expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-177">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-177">Console example</span></span>  

<span data-ttu-id="8f260-178">En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos de la página web.</span><span class="sxs-lookup"><span data-stu-id="8f260-178">In the following code sample and figure, all of the `<p>` elements on the webpage are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Uso de un selector XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="8f260-180">Uso de un selector XPath</span><span class="sxs-lookup"><span data-stu-id="8f260-180">Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-181">En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos que contienen `<a>` elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-181">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Uso de un selector XPath más complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="8f260-183">Uso de un selector XPath más complicado</span><span class="sxs-lookup"><span data-stu-id="8f260-183">Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-184">Al igual que los demás comandos de selector, tiene un segundo parámetro opcional, , que especifica un elemento o nodo desde el que buscar `$x(path)` `startNode` elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-184">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Uso de un selector XPath con startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="8f260-186">Uso de un selector XPath con</span><span class="sxs-lookup"><span data-stu-id="8f260-186">Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="8f260-187">clear</span><span class="sxs-lookup"><span data-stu-id="8f260-187">clear</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-188">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-188">Console syntax</span></span>  

```console
clear()
```  

<span data-ttu-id="8f260-189">Este commnad borra la consola del historial.</span><span class="sxs-lookup"><span data-stu-id="8f260-189">This commnad clears the console of the history.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-190">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-190">Console example</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="8f260-191">copy</span><span class="sxs-lookup"><span data-stu-id="8f260-191">copy</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-192">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-192">Console syntax</span></span>  

```console
copy(object)
```  

<span data-ttu-id="8f260-193">Este método copia una representación de cadena del objeto especificado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8f260-193">This method copies a string representation of the specified object to the clipboard.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-194">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-194">Console example</span></span>  

```console
copy($0)
```  

---  

## <a name="debug"></a><span data-ttu-id="8f260-195">depurar</span><span class="sxs-lookup"><span data-stu-id="8f260-195">debug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-196">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-196">Console syntax</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="8f260-197">El [Chromium problema #1050237][CR1050237] está rastreando un error con la `debug()` función.</span><span class="sxs-lookup"><span data-stu-id="8f260-197">The [Chromium issue #1050237][CR1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="8f260-198">Si encuentra el problema, intente usar [puntos de interrupción en][DevtoolsJavascriptBreakpoints] su lugar.</span><span class="sxs-lookup"><span data-stu-id="8f260-198">If you encounter the issue, try using [breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="8f260-199">Cuando se solicita el método especificado, el depurador invoca y rompe dentro del método en la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="8f260-199">When you request the specified method, the debugger invokes and breaks inside the method on the **Sources** tool.</span></span>  <span data-ttu-id="8f260-200">Le permite realizar un paso a través y depurar el código.</span><span class="sxs-lookup"><span data-stu-id="8f260-200">It allows you to step through and debug the code.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-201">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-201">Console example</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Irrumpir dentro de un método con debug()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="8f260-203">Dividir dentro de un método con</span><span class="sxs-lookup"><span data-stu-id="8f260-203">Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="8f260-204">Se `undebug(method)` usa para detener la interrupción del método o usar la interfaz de usuario para desactivar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8f260-204">Use `undebug(method)` to stop breaking on the method, or use the UI to turn off all breakpoints.</span></span>  

<span data-ttu-id="8f260-205">Para obtener más información sobre los puntos de interrupción, vaya a Cómo pausar el código con puntos de interrupción [en Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="8f260-205">For more information on breakpoints, navigate to [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span></span>  

---  

## <a name="dir"></a><span data-ttu-id="8f260-206">dir</span><span class="sxs-lookup"><span data-stu-id="8f260-206">dir</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-207">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-207">Console syntax</span></span>  

```console
dir(object)
```  

<span data-ttu-id="8f260-208">Este comando muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-208">This command displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="8f260-209">Este método es un alias para el [método console.dir().][MdnDocsWebApiConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="8f260-209">This method is an alias for the [console.dir()][MdnDocsWebApiConsoleDir] method.</span></span>  

<span data-ttu-id="8f260-210">Evalúe `document.head` en la consola **para** mostrar el HTML entre las `<head>` `</head>` etiquetas y.</span><span class="sxs-lookup"><span data-stu-id="8f260-210">Evaluate `document.head` in the **Console** to display the HTML between the `<head>` and `</head>` tags.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-211">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-211">Console example</span></span>  

<span data-ttu-id="8f260-212">En el siguiente ejemplo de código y figura, se muestra una descripción de estilo de objeto después de usar `console.dir()` en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="8f260-212">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the **Console**.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registro de document.head con el método dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="8f260-214">Registro `document.head` con `dir()` método</span><span class="sxs-lookup"><span data-stu-id="8f260-214">Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-215">Para obtener más información, vaya a [console.dir()][DevToolsConsoleApiConsoleDirObject] en la API de consola.</span><span class="sxs-lookup"><span data-stu-id="8f260-215">For more information, navigate to [console.dir()][DevToolsConsoleApiConsoleDirObject] in the Console API.</span></span>  

---  

## <a name="dirxml"></a><span data-ttu-id="8f260-216">dirxml</span><span class="sxs-lookup"><span data-stu-id="8f260-216">dirxml</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-217">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-217">Console syntax</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="8f260-218">Este comando imprime una representación XML del objeto especificado, tal como se muestra en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-218">This command prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="8f260-219">Este método es equivalente al [método console.dirxml().][MdnDocsWebApiConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="8f260-219">This method is equivalent to the [console.dirxml()][MdnDocsWebApiConsoleDirxml] method.</span></span>  

---  

## <a name="inspect"></a><span data-ttu-id="8f260-220">inspeccionar</span><span class="sxs-lookup"><span data-stu-id="8f260-220">inspect</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-221">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-221">Console syntax</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="8f260-222">Este comando se abre y elige el elemento u objeto especificado en el \*\*\*\* panel correspondiente: la herramienta **Elementos** para elementos DOM o la herramienta Memoria para objetos de montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8f260-222">This command opens and chooses the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-223">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-223">Console example</span></span>  

<span data-ttu-id="8f260-224">En el siguiente ejemplo de código y figura, se `document.body` abre en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-224">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-225">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-225">Console example</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspeccionar un elemento con inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="8f260-227">Inspeccionar un elemento con</span><span class="sxs-lookup"><span data-stu-id="8f260-227">Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="8f260-228">Al pasar un método para inspeccionar, el método abre la página web en la **herramienta Orígenes** para que la examine.</span><span class="sxs-lookup"><span data-stu-id="8f260-228">When passing a method to inspect, the method opens the webpage in the **Sources** tool for you to inspect.</span></span>  

---  

## <a name="geteventlisteners"></a><span data-ttu-id="8f260-229">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="8f260-229">getEventListeners</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-230">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-230">Console syntax</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="8f260-231">Este comando devuelve los agentes de escucha de eventos registrados en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-231">This command returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="8f260-232">El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \(como `click` o `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="8f260-232">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="8f260-233">Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="8f260-233">The members of each array are objects that describe the listener registered for each type.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-234">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-234">Console example</span></span>  

<span data-ttu-id="8f260-235">En el siguiente fragmento de código y figura, se enumeran todos los agentes de escucha de eventos registrados `document` en el objeto.</span><span class="sxs-lookup"><span data-stu-id="8f260-235">In the following code snippet and figure, all of the event listeners registered on the `document` object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Resultado del uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="8f260-237">El resultado de usar</span><span class="sxs-lookup"><span data-stu-id="8f260-237">The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="8f260-238">Si se registra más de un agente de escucha en el objeto especificado, la matriz contiene un miembro para cada escucha.</span><span class="sxs-lookup"><span data-stu-id="8f260-238">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="8f260-239">En la siguiente figura, se registran dos agentes de escucha de eventos en el `document` elemento para el `click` evento.</span><span class="sxs-lookup"><span data-stu-id="8f260-239">In the following figure, two event listeners are registered on the `document` element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Varios agentes de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="8f260-241">Varios agentes de escucha</span><span class="sxs-lookup"><span data-stu-id="8f260-241">Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-242">Puede expandir cada uno de los siguientes objetos para explorar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="8f260-242">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vista expandida del objeto de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="8f260-244">Vista expandida del objeto de escucha</span><span class="sxs-lookup"><span data-stu-id="8f260-244">Expanded view of listener object</span></span>  
:::image-end:::  

---  

## <a name="keys"></a><span data-ttu-id="8f260-245">teclas</span><span class="sxs-lookup"><span data-stu-id="8f260-245">keys</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-246">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-246">Console syntax</span></span>  

```console
keys(object)
```  

<span data-ttu-id="8f260-247">Este comando devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-247">This command returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="8f260-248">Para obtener los valores asociados de las mismas propiedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="8f260-248">To get the associated values of the same properties, use `values()`.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-249">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-249">Console example</span></span>  

<span data-ttu-id="8f260-250">Por ejemplo, supongamos que la aplicación definió el siguiente objeto.</span><span class="sxs-lookup"><span data-stu-id="8f260-250">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = {"name": "Ted", "level": 42}
```  

<span data-ttu-id="8f260-251">En los siguientes ejemplos de código y figura, se supone que el resultado se definió en el espacio de nombres `player1` global \(por simplicidad\) antes de escribir y `keys(player1)` en la `values(player1)` consola.</span><span class="sxs-lookup"><span data-stu-id="8f260-251">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) before you type `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Los comandos keys() y values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="8f260-253">Los `keys()` comandos y `values()`</span><span class="sxs-lookup"><span data-stu-id="8f260-253">The `keys()` and `values()` commands</span></span>  
:::image-end:::  

---  

## <a name="monitor"></a><span data-ttu-id="8f260-254">monitor</span><span class="sxs-lookup"><span data-stu-id="8f260-254">monitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-255">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-255">Console syntax</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="8f260-256">Este comando registra un mensaje en la consola que indica el nombre del método junto con los argumentos pasados al método como parte de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f260-256">This command logs a message to the console that indicates the method name along with the arguments passed to the method as part of a request.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-257">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-257">Console example</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="El método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="8f260-259">El `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="8f260-259">The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-260">Se `unmonitor(method)` usa para finalizar la supervisión.</span><span class="sxs-lookup"><span data-stu-id="8f260-260">Use `unmonitor(method)` to end monitoring.</span></span>  

---  

## <a name="monitorevents"></a><span data-ttu-id="8f260-261">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="8f260-261">monitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-262">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-262">Console syntax</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="8f260-263">Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="8f260-263">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="8f260-264">Puede especificar un único evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="8f260-264">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-265">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-265">Console example</span></span>  

<span data-ttu-id="8f260-266">Revise el siguiente ejemplo de código y figura.</span><span class="sxs-lookup"><span data-stu-id="8f260-266">Review the following code sample and figure.</span></span>  

<span data-ttu-id="8f260-267">A continuación se supervisan todos los eventos de cambio de tamaño del objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="8f260-267">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Eventos de cambio de tamaño de ventana de supervisión" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="8f260-269">Eventos de cambio de tamaño de ventana de supervisión</span><span class="sxs-lookup"><span data-stu-id="8f260-269">Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="8f260-270">El siguiente fragmento de código define una matriz para supervisar los eventos `resize` y ambos en el objeto `scroll` window.</span><span class="sxs-lookup"><span data-stu-id="8f260-270">The following code snippet defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="8f260-271">También puede especificar uno de los tipos de eventos disponibles, cadenas que se asignan a conjuntos predefinidos de eventos.</span><span class="sxs-lookup"><span data-stu-id="8f260-271">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="8f260-272">En la tabla siguiente se muestran los tipos de eventos disponibles y las asignaciones de eventos asociadas.</span><span class="sxs-lookup"><span data-stu-id="8f260-272">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="8f260-273">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="8f260-273">Event type</span></span> | <span data-ttu-id="8f260-274">Eventos asignados correspondientes</span><span class="sxs-lookup"><span data-stu-id="8f260-274">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="8f260-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="8f260-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="8f260-276">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="8f260-276">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="8f260-277">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="8f260-277">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="8f260-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="8f260-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="8f260-279">En el siguiente ejemplo de código, el tipo de evento correspondiente a los eventos de un campo de texto de entrada se elige `key` actualmente en la `key` **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="8f260-279">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently chosen in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="8f260-280">En la siguiente figura, se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.</span><span class="sxs-lookup"><span data-stu-id="8f260-280">In the following figure, the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Supervisión de eventos clave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="8f260-282">Supervisión de eventos clave</span><span class="sxs-lookup"><span data-stu-id="8f260-282">Monitoring key events</span></span>  
:::image-end:::  

---  

## <a name="profile"></a><span data-ttu-id="8f260-283">profile</span><span class="sxs-lookup"><span data-stu-id="8f260-283">profile</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-284">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-284">Console syntax</span></span>  

```console
profile([name])
```  

<span data-ttu-id="8f260-285">Este comando inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.</span><span class="sxs-lookup"><span data-stu-id="8f260-285">This command starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="8f260-286">El [método profileEnd()](#profileend) completa el perfil y muestra los resultados en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="8f260-286">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="8f260-287">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-287">Console example</span></span>  

1.  <span data-ttu-id="8f260-288">Ejecute el `profile()` método para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="8f260-288">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="8f260-289">Ejecute el [método profileEnd()](#profileend) para detener la generación de perfiles y mostrar los resultados en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="8f260-289">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="8f260-290">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="8f260-290">Profiles may also be nested.</span></span>  <span data-ttu-id="8f260-291">En los siguientes ejemplos de código y figura, el resultado es el mismo sea cual sea el orden.</span><span class="sxs-lookup"><span data-stu-id="8f260-291">In the following code samples and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="8f260-292">Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.</span><span class="sxs-lookup"><span data-stu-id="8f260-292">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="profileend"></a><span data-ttu-id="8f260-293">profileEnd</span><span class="sxs-lookup"><span data-stu-id="8f260-293">profileEnd</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-294">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-294">Console syntax</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="8f260-295">Este comando completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="8f260-295">This command completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="8f260-296">Debe ejecutar el método [profile().](#profile)</span><span class="sxs-lookup"><span data-stu-id="8f260-296">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="8f260-297">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-297">Console example</span></span>  

1.  <span data-ttu-id="8f260-298">Ejecute el [método profile()](#profile) para iniciar la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="8f260-298">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="8f260-299">Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en la herramienta **Memoria.**</span><span class="sxs-lookup"><span data-stu-id="8f260-299">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="8f260-300">Los perfiles también pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="8f260-300">Profiles may also be nested.</span></span>  <span data-ttu-id="8f260-301">En el siguiente ejemplo de código y figura, el resultado es el mismo sea cual sea el orden.</span><span class="sxs-lookup"><span data-stu-id="8f260-301">In the following code sample and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="8f260-302">El resultado aparece como una instantánea de montón en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="8f260-302">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfiles agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="8f260-304">Perfiles agrupados</span><span class="sxs-lookup"><span data-stu-id="8f260-304">Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8f260-305">Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.</span><span class="sxs-lookup"><span data-stu-id="8f260-305">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="queryobjects"></a><span data-ttu-id="8f260-306">queryObjects</span><span class="sxs-lookup"><span data-stu-id="8f260-306">queryObjects</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-307">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-307">Console syntax</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="8f260-308">Este comando devuelve una matriz de objetos creados con el constructor especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-308">This command returns an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="8f260-309">El ámbito de `queryObjects()` es el contexto de tiempo de ejecución elegido actualmente en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="8f260-309">The scope of `queryObjects()` is the currently chosen runtime context in the **Console**.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-310">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-310">Console example</span></span>  

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="8f260-311">Devuelve todo `Promises` .</span><span class="sxs-lookup"><span data-stu-id="8f260-311">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="8f260-312">Devuelve todos los elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="8f260-312">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="8f260-313">Devuelve todos los objetos que se crearon instancias mediante `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="8f260-313">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="8f260-314">tabla</span><span class="sxs-lookup"><span data-stu-id="8f260-314">table</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-315">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-315">Console syntax</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="8f260-316">Este comando registra los datos del objeto con formato de tabla basado en el objeto de datos con encabezados de columna opcionales.</span><span class="sxs-lookup"><span data-stu-id="8f260-316">This command logs object data with table formatting based upon the data object in with optional column headings.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-317">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-317">Console example</span></span>  

<span data-ttu-id="8f260-318">En el siguiente ejemplo de código y figura, se muestra una lista de nombres que usan una tabla en la consola.</span><span class="sxs-lookup"><span data-stu-id="8f260-318">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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
   <span data-ttu-id="8f260-320">El resultado del `table()` método</span><span class="sxs-lookup"><span data-stu-id="8f260-320">The result of the `table()` method</span></span>  
:::image-end:::  

---  

## <a name="undebug"></a><span data-ttu-id="8f260-321">undebug</span><span class="sxs-lookup"><span data-stu-id="8f260-321">undebug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-322">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-322">Console syntax</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="8f260-323">Este comando detiene la depuración del método especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-323">This command stops the debug of the specified method.</span></span> <span data-ttu-id="8f260-324">Por lo tanto, cuando se solicita el método, el depurador ya no se invoca.</span><span class="sxs-lookup"><span data-stu-id="8f260-324">So when the method is requested, the debugger is no longer invoked.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-325">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-325">Console example</span></span>  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a><span data-ttu-id="8f260-326">unmonitor</span><span class="sxs-lookup"><span data-stu-id="8f260-326">unmonitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-327">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-327">Console syntax</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="8f260-328">Este comando detiene la supervisión del método especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-328">This command stops the monitoring of the specified method.</span></span>  <span data-ttu-id="8f260-329">Este método se usa en función del [método monitor().](#monitor)</span><span class="sxs-lookup"><span data-stu-id="8f260-329">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-330">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-330">Console example</span></span>  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a><span data-ttu-id="8f260-331">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="8f260-331">unmonitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-332">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-332">Console syntax</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="8f260-333">Este comando detiene la supervisión de eventos para el objeto y los eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="8f260-333">This command stops monitoring events for the specified object and events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-334">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-334">Console example</span></span>  

<span data-ttu-id="8f260-335">Por ejemplo, el siguiente fragmento de código detiene toda la supervisión de eventos en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="8f260-335">For example, the following code snippet stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="8f260-336">También puede detener selectivamente la supervisión de eventos específicos en un objeto.</span><span class="sxs-lookup"><span data-stu-id="8f260-336">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="8f260-337">Por ejemplo, el siguiente código inicia la supervisión de todos los eventos del elemento seleccionado actualmente y, a continuación, detiene la supervisión de eventos \(quizás para reducir el ruido en la salida de la `mouse` `mousemove` consola\).</span><span class="sxs-lookup"><span data-stu-id="8f260-337">For example, the following code starts monitoring all `mouse` events on the currently chosen element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a><span data-ttu-id="8f260-338">valores</span><span class="sxs-lookup"><span data-stu-id="8f260-338">values</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="8f260-339">Sintaxis de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-339">Console syntax</span></span>  

```console
values(object)
```  

<span data-ttu-id="8f260-340">Este comando devuelve una matriz que contiene los valores de todas las propiedades que pertenecen al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f260-340">This command returns an array containing the values of all properties belonging to the specified object.</span></span>  

### <a name="console-example"></a><span data-ttu-id="8f260-341">Ejemplo de consola</span><span class="sxs-lookup"><span data-stu-id="8f260-341">Console example</span></span>  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8f260-342">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f260-342">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir: referencia de api de consola | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Acelerar el tiempo de ejecución de JavaScript | Microsoft Docs"  

[CR1050237]: https://crbug.com/1050237 "Problema 1050237: debug(function) no funciona | Chromium errores"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> <span data-ttu-id="8f260-352">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f260-352">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8f260-353">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8f260-353">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8f260-355">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f260-355">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
