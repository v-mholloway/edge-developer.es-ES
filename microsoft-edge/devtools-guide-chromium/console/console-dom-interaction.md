---
description: Información general sobre cómo interactuar con la página web actual en el explorador mediante la herramienta Consola
title: Usar la consola para interactuar con el DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 80b0e4368b1c8feaf28a58ac2e3bd9c1ea2f1f92
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483664"
---
# <a name="use-the-console-to-interact-with-the-dom"></a><span data-ttu-id="18bbc-104">Usar la consola para interactuar con el DOM</span><span class="sxs-lookup"><span data-stu-id="18bbc-104">Use the Console to interact with the DOM</span></span>

<span data-ttu-id="18bbc-105">La **herramienta Consola** no es solo para la información de [registro][DevtoolsConsoleConsoleLog] o para [ejecutar JavaScript arbitrario.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="18bbc-105">The **Console** tool isn't only for [logging information][DevtoolsConsoleConsoleLog] or to [run arbitrary JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  <span data-ttu-id="18bbc-106">También es una excelente manera de interactuar con la página web en el explorador.</span><span class="sxs-lookup"><span data-stu-id="18bbc-106">It also is a great way to interact with the webpage in the browser.</span></span>  <span data-ttu-id="18bbc-107">Conste que es una versión de entorno de script de **la herramienta Inspeccionar.**</span><span class="sxs-lookup"><span data-stu-id="18bbc-107">Consider it a script-environment version of the **Inspect** tool.</span></span>  

## <a name="read-from-the-dom"></a><span data-ttu-id="18bbc-108">Leer desde el DOM</span><span class="sxs-lookup"><span data-stu-id="18bbc-108">Read from the DOM</span></span>

<span data-ttu-id="18bbc-109">Para hacer referencia al encabezado de la página web, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-109">To reference the header of the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="18bbc-110">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-110">Open the **Console**.</span></span>
    *   <span data-ttu-id="18bbc-111">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="18bbc-111">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="18bbc-112">Escriba o copie y pegue el siguiente fragmento de código en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-112">Type or copy and paste the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Para obtener una referencia al encabezado en la consola, use document.querySelector" lightbox="../media/console-dom-get-reference.msft.png":::
    <span data-ttu-id="18bbc-114">Para obtener una referencia al encabezado en la consola, use</span><span class="sxs-lookup"><span data-stu-id="18bbc-114">To get a reference to the header in console, use</span></span> `document.querySelector`  
:::image-end:::  

<span data-ttu-id="18bbc-115">Si selecciona o `Shift` + `Tab` mueve el cursor del mouse sobre el resultado HTML, DevTools resalta el encabezado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-115">If you select `Shift`+`Tab` or move your mouse cursor over the HTML result, DevTools highlights the header for you.</span></span>  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools resalta la sección que elija en la consola" lightbox="../media/console-dom-highlight-element.msft.png":::
    <span data-ttu-id="18bbc-117">DevTools resalta la sección que elija en la **consola**</span><span class="sxs-lookup"><span data-stu-id="18bbc-117">DevTools highlights the section you choose in the **Console**</span></span>  
:::image-end:::  

## <a name="manipulate-the-dom"></a><span data-ttu-id="18bbc-118">Manipular el DOM</span><span class="sxs-lookup"><span data-stu-id="18bbc-118">Manipulate the DOM</span></span>

<span data-ttu-id="18bbc-119">También puede manipular la página web.</span><span class="sxs-lookup"><span data-stu-id="18bbc-119">You may manipulate the webpage, too.</span></span>  <span data-ttu-id="18bbc-120">Por ejemplo, si copia y pega o escribe lo siguiente en la **Consola,** se muestra un borde verde alrededor del encabezado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-120">For example, if you copy and paste or type the following into the **Console**, a green border displays around the header.</span></span>

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Para agregar un borde a un elemento, use la consola" lightbox="../media/console-dom-add-border.msft.png":::
    <span data-ttu-id="18bbc-122">Para agregar un borde a un elemento, use la **consola**</span><span class="sxs-lookup"><span data-stu-id="18bbc-122">To add a border to an element, use the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-123">Según la complejidad de la página web, puede resultar desalentador encontrar el elemento adecuado para manipular.</span><span class="sxs-lookup"><span data-stu-id="18bbc-123">Depending on the complexity of the webpage, It may be daunting to find the right element to manipulate.</span></span>  <span data-ttu-id="18bbc-124">Pero puede usar la herramienta **Inspeccionar** para ayudarle.</span><span class="sxs-lookup"><span data-stu-id="18bbc-124">But you may use the **Inspect** tool to help you.</span></span>  <span data-ttu-id="18bbc-125">Diga que desea manipular la `Documentation` parte del encabezado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-125">Say you want to manipulate the `Documentation` part in the header.</span></span>

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Mostrar el elemento que inspecciona en la pantalla" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    <span data-ttu-id="18bbc-127">Mostrar el elemento que inspecciona en la pantalla</span><span class="sxs-lookup"><span data-stu-id="18bbc-127">Display the element that you inspect on the screen</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-128">Para obtener una referencia directa al elemento que se debe manipular, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-128">To get a direct reference to the element to manipulate, complete the following actions.</span></span>  

1.  <span data-ttu-id="18bbc-129">Use la **herramienta Inspeccionar** para elegir el elemento.</span><span class="sxs-lookup"><span data-stu-id="18bbc-129">Use the **Inspect** tool to choose the element.</span></span>  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Para elegir un elemento, use la herramienta Inspector" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        <span data-ttu-id="18bbc-131">Para elegir un elemento, use la **herramienta Inspector**</span><span class="sxs-lookup"><span data-stu-id="18bbc-131">To choose an element, use the **Inspector** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18bbc-132">Seleccióne y DevTools saltará a la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="18bbc-132">Choose it and DevTools jumps to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="18bbc-133">Elija el `...` menú situado junto al elemento en la vista DOM.</span><span class="sxs-lookup"><span data-stu-id="18bbc-133">Choose the `...` menu next to the element in the DOM view.</span></span>  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="El elemento elegido se muestra en el árbol DOM de la herramienta Elementos, elija el menú desbordamiento para obtener más características" lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        <span data-ttu-id="18bbc-135">El elemento elegido se muestra en el árbol DOM de la **herramienta Elementos,** elija el menú desbordamiento para obtener más características</span><span class="sxs-lookup"><span data-stu-id="18bbc-135">The chosen element displays in the DOM tree of the **Elements** tool, choose the overflow menu to get more features</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18bbc-136">Abra el menú contextual y elija `Copy`  >  `Copy JS Path` .</span><span class="sxs-lookup"><span data-stu-id="18bbc-136">Open the contextual menu and choose `Copy` > `Copy JS Path`.</span></span>  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Copiar la ruta de acceso de JavaScript desde un elemento en la vista DOM de la herramienta Elementos" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        <span data-ttu-id="18bbc-138">Copiar la ruta de acceso de JavaScript desde un elemento en la vista DOM de **la herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="18bbc-138">Copy the JavaScript path from an element in the DOM view of the **Elements** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18bbc-139">Vuelva a la **consola y** pegue el comando.</span><span class="sxs-lookup"><span data-stu-id="18bbc-139">Go back to the **Console** and paste the command.</span></span>  
    
<span data-ttu-id="18bbc-140">Para cambiar el texto del vínculo a `My Playground` , agregue al comando que ha `.textContent = "My Playground"` pegado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18bbc-140">To change the text of the link to `My Playground`, add `.textContent = "My Playground"` to the command you previously pasted.</span></span>  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Usar la consola para cambiar el contenido de un elemento" lightbox="../media/console-dom-change-content.msft.png":::
    <span data-ttu-id="18bbc-142">Usar la **consola** para cambiar el contenido de un elemento</span><span class="sxs-lookup"><span data-stu-id="18bbc-142">Use the **Console** to change the content of an element</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-143">Use las manipulaciones dom de JavaScript que desee hacer en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-143">Use any JavaScript DOM manipulations you want to do in the **Console**.</span></span>  <span data-ttu-id="18bbc-144">Para que sea más conveniente, **la consola** viene con algunos métodos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="18bbc-144">To make it more convenient, the **Console** comes with a few helper methods.</span></span>  

## <a name="helpful-console-utility-methods"></a><span data-ttu-id="18bbc-145">Métodos de utilidad de consola útiles</span><span class="sxs-lookup"><span data-stu-id="18bbc-145">Helpful Console utility methods</span></span>  

<span data-ttu-id="18bbc-146">Hay muchos métodos de comodidad y accesos directos disponibles como [Utilidades de consola.][DevtoolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="18bbc-146">Many convenience methods and shortcuts are available to you as [Console Utilities][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="18bbc-147">Algunos de los métodos son increíblemente eficaces y son cosas que probablemente escribiste como una serie `console.log()` de instrucciones en el pasado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-147">Some of the methods are incredibly powerful and are things you probably wrote as a series of `console.log()` statements in the past.</span></span>

### <a name="the-power-to-the-"></a><span data-ttu-id="18bbc-148">La potencia de $</span><span class="sxs-lookup"><span data-stu-id="18bbc-148">The power to the $</span></span>

<span data-ttu-id="18bbc-149">El `$` tiene poderes especiales en **la consola** y puede recordarlo desde jQuery.</span><span class="sxs-lookup"><span data-stu-id="18bbc-149">The `$` has special powers in **Console** and you may remember that from jQuery.</span></span>

*   `$_` <span data-ttu-id="18bbc-150">almacena el resultado del último comando.</span><span class="sxs-lookup"><span data-stu-id="18bbc-150">stores the result of the last command.</span></span>  <span data-ttu-id="18bbc-151">Por lo tanto, si escribe `2 + 2` y selecciona `Enter` y, a continuación, escribe `$_` , la **consola** le muestra `4` .</span><span class="sxs-lookup"><span data-stu-id="18bbc-151">So, if you type `2 + 2` and select `Enter`, and then type `$_`, the **Console** displays you `4`.</span></span>
*   `$0` <span data-ttu-id="18bbc-152">to `$4` es una pila de los últimos elementos inspeccionados es siempre la más `$0` reciente.</span><span class="sxs-lookup"><span data-stu-id="18bbc-152">to `$4` is a stack of the last inspected elements `$0` is always the newest one.</span></span>  <span data-ttu-id="18bbc-153">Por lo tanto, en el ejemplo anterior, simplemente eligió el elemento de la herramienta **Inspector** y escriba `$0.textContent = "My Playground"` para obtener el mismo efecto.</span><span class="sxs-lookup"><span data-stu-id="18bbc-153">So in the earlier example, you just chose the element in the **Inspector** tool and type `$0.textContent = "My Playground"` to get the same effect.</span></span>
*   `$x()` <span data-ttu-id="18bbc-154">permite elegir elementos DOM con XPATH.</span><span class="sxs-lookup"><span data-stu-id="18bbc-154">allows you to choose DOM elements using XPATH.</span></span>
*   `$()` <span data-ttu-id="18bbc-155">y `$$()` son versiones más cortas de for y `document.querySelector()` `document.querySelectorAll()` .</span><span class="sxs-lookup"><span data-stu-id="18bbc-155">and `$$()` are shorter versions of for `document.querySelector()` and `document.querySelectorAll()`.</span></span>  
    
<span data-ttu-id="18bbc-156">Por ejemplo, el siguiente fragmento de código recupera todos los vínculos de la página web \(as is short for \) y muestra los vínculos como una tabla ordenable para copiar y pegar, por ejemplo, en `$$('a')` `document.querySelectorAll('a')` Excel.</span><span class="sxs-lookup"><span data-stu-id="18bbc-156">For example, the following code snippet retrieves all the links in the webpage \(as `$$('a')` is short for `document.querySelectorAll('a')`\) and displays the links as a sortable table to copy and paste, for example, into Excel.</span></span>

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Obtener todos los vínculos de la página web y mostrar el resultado como una tabla" lightbox="../media/console-dom-get-all-links.msft.png":::
    <span data-ttu-id="18bbc-158">Obtener todos los vínculos de la página web y mostrar el resultado como una tabla</span><span class="sxs-lookup"><span data-stu-id="18bbc-158">Get all links in the webpage and display the result as a table</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-159">Sin embargo, si no desea mostrar la información, pero desea tomarla como datos.</span><span class="sxs-lookup"><span data-stu-id="18bbc-159">However, if you don't want to display the information, but you want to grab it as data.</span></span>  <span data-ttu-id="18bbc-160">El `$$('a')` acceso directo proporciona los vínculos de delimitador y todas las propiedades de cada uno.</span><span class="sxs-lookup"><span data-stu-id="18bbc-160">The `$$('a')` shortcut provides the anchor links and all of the properties for each one.</span></span>  <span data-ttu-id="18bbc-161">El problema es que solo desea los vínculos y el texto relacionado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-161">The problem is that you only want the links and the related text.</span></span>  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="El método abreviado $$ devuelve demasiada información" lightbox="../media/console-dom-too-much-link-information.msft.png":::
    <span data-ttu-id="18bbc-163">El `$$` acceso directo devuelve demasiada información</span><span class="sxs-lookup"><span data-stu-id="18bbc-163">The `$$` shortcut returns far too much information</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-164">El `$$` acceso directo tiene una característica adicional interesante.</span><span class="sxs-lookup"><span data-stu-id="18bbc-164">The `$$` shortcut has an interesting extra feature.</span></span>  <span data-ttu-id="18bbc-165">En lugar de devolver un `NodeList` tipo `document.querySelectorAll()` puro, el `$$` acceso directo le ofrece todos los `Array` métodos.</span><span class="sxs-lookup"><span data-stu-id="18bbc-165">Instead of returning a pure `NodeList` like `document.querySelectorAll()`, the `$$` shortcut gives you all of the `Array` methods.</span></span>  <span data-ttu-id="18bbc-166">Use `map()` el método para reducir la información a lo que necesita.</span><span class="sxs-lookup"><span data-stu-id="18bbc-166">Use `map()` method to reduce the information to what you need.</span></span>  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

<span data-ttu-id="18bbc-167">El fragmento de código devuelve una matriz de todos los vínculos como objetos `url` con y `text` propiedades.</span><span class="sxs-lookup"><span data-stu-id="18bbc-167">The code snippet returns an Array of all the links as objects with `url` and `text` properties.</span></span>  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Usar la asignación en $$ para filtrar la información al mínimo mínimo" lightbox="../media/console-dom-filter-link-data.msft.png":::
    <span data-ttu-id="18bbc-169">Usar la asignación `$$` para filtrar la información al mínimo mínimo</span><span class="sxs-lookup"><span data-stu-id="18bbc-169">Use map on `$$` to filter information down to the bare minimum</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-170">Aún no ha terminado, varios vínculos son vínculos internos a la página web o tienen texto vacío.</span><span class="sxs-lookup"><span data-stu-id="18bbc-170">You aren't done yet, several links are internal links to the webpage or have empty text.</span></span>  <span data-ttu-id="18bbc-171">Use el método filter para deshacerse de los vínculos internos.</span><span class="sxs-lookup"><span data-stu-id="18bbc-171">Use the filter method to get rid of the internal links.</span></span>  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Obtener los vínculos que no están vacíos y son externos" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    <span data-ttu-id="18bbc-173">Obtener los vínculos que no están vacíos y son externos</span><span class="sxs-lookup"><span data-stu-id="18bbc-173">Get the links that aren't empty and are external</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-174">Como se muestra al principio de la página web, también puede cambiar estos elementos.</span><span class="sxs-lookup"><span data-stu-id="18bbc-174">As displayed at the start of the webpage, you may also change these elements.</span></span>  <span data-ttu-id="18bbc-175">Por ejemplo, el siguiente fragmento de código crea un borde verde alrededor de todos los vínculos externos:</span><span class="sxs-lookup"><span data-stu-id="18bbc-175">For example, the following code snippet creates a green border around all external links:</span></span>

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Para resaltar todos los vínculos externos, agregue un borde verde alrededor de cada uno" lightbox="../media/console-dom-highlight-links.msft.png":::
    <span data-ttu-id="18bbc-177">Para resaltar todos los vínculos externos, agregue un borde verde alrededor de cada uno</span><span class="sxs-lookup"><span data-stu-id="18bbc-177">To highlight all external links, add a green border around each</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-178">En lugar de escribir JavaScript complejo para filtrar resultados, usa la potencia de los selectores CSS.</span><span class="sxs-lookup"><span data-stu-id="18bbc-178">Instead of writing complex JavaScript to filter results, use the power of CSS selectors.</span></span>  

<span data-ttu-id="18bbc-179">Para crear una tabla de la información y para todas las imágenes de la página web que no son imágenes en `src` `alt` línea, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-179">To create a table of the `src` and `alt` information for all images on the webpage that aren't inline images, complete the following actions.</span></span>  

1.  <span data-ttu-id="18bbc-180">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="18bbc-181">Escriba o copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="18bbc-181">Type or copy and paste the following code snippet.</span></span>  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Para elegir elementos, use un selector CSS complejo" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    <span data-ttu-id="18bbc-183">Para elegir elementos, use un selector CSS complejo</span><span class="sxs-lookup"><span data-stu-id="18bbc-183">To choose elements, use a complex CSS selector</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-184">¿Listo para un ejemplo aún más complejo?</span><span class="sxs-lookup"><span data-stu-id="18bbc-184">Ready for an even more complex example?</span></span>  <span data-ttu-id="18bbc-185">Las páginas web HTML generadas a partir de markdown como este artículo tienen valores de id. automáticos para cada encabezado que le permiten vincular profundamente a esa sección.</span><span class="sxs-lookup"><span data-stu-id="18bbc-185">HTML webpages generated from markdown like this article, have automatic ID values for each heading to allow you to deep link to that section.</span></span>  <span data-ttu-id="18bbc-186">Por ejemplo, un `# New features` cambio en `<h1 id="new-features">New features</h1>` .</span><span class="sxs-lookup"><span data-stu-id="18bbc-186">For example, a `# New features` changes to `<h1 id="new-features">New features</h1>`.</span></span>  

<span data-ttu-id="18bbc-187">Para enumerar todos los encabezados automáticos que se van a copiar y pegar, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-187">To list of all of the automatic headings to copy and paste, complete the following actions.</span></span>  

1.  <span data-ttu-id="18bbc-188">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="18bbc-189">Escriba o copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="18bbc-189">Type or copy and paste the following code snippet.</span></span>  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

<span data-ttu-id="18bbc-190">El resultado es texto que contiene contenido para cada encabezado seguido de la dirección URL completa que apunta a él.</span><span class="sxs-lookup"><span data-stu-id="18bbc-190">The result is text that contains content for each heading followed by the full URL that points to it.</span></span>  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Obtener todos los encabezados y las direcciones URL generadas de la página web" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    <span data-ttu-id="18bbc-192">Obtener todos los encabezados y las direcciones URL generadas de la página web</span><span class="sxs-lookup"><span data-stu-id="18bbc-192">Get all the headings and the generated URLs from the webpage</span></span>  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a><span data-ttu-id="18bbc-193">Limpiar con borrar y copiar</span><span class="sxs-lookup"><span data-stu-id="18bbc-193">Clean up with clear and copy</span></span>

<span data-ttu-id="18bbc-194">Cuando se desarrolla en la **consola,** las cosas pueden resultar desordenas.</span><span class="sxs-lookup"><span data-stu-id="18bbc-194">When developing in the **Console**, things may get messy.</span></span>  <span data-ttu-id="18bbc-195">Puede resultar frustrante intentar elegir resultados mientras copia y pega.</span><span class="sxs-lookup"><span data-stu-id="18bbc-195">You may find it frustrating to try to choose results while you copy and paste.</span></span>  <span data-ttu-id="18bbc-196">Los dos métodos de utilidad siguientes le ayudan.</span><span class="sxs-lookup"><span data-stu-id="18bbc-196">The following two utility methods help you.</span></span>  

*   `copy()` <span data-ttu-id="18bbc-197">copia lo que le des al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="18bbc-197">copies whatever you give it to the clipboard.</span></span>  <span data-ttu-id="18bbc-198">El `copy()` método es especialmente útil cuando se mezcla con que copia el último `$_` resultado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-198">The `copy()` method is especially useful when you mix it with `$_` that copies the last result.</span></span>
*   `clear()` <span data-ttu-id="18bbc-199">borra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-199">clears the **Console**.</span></span>

### <a name="read-and-monitor-events"></a><span data-ttu-id="18bbc-200">Leer y supervisar eventos</span><span class="sxs-lookup"><span data-stu-id="18bbc-200">Read and monitor events</span></span>

<span data-ttu-id="18bbc-201">Otros dos métodos de utilidad interesantes de **la consola tratan** el control de eventos.</span><span class="sxs-lookup"><span data-stu-id="18bbc-201">Two other interesting utility methods of **Console** deal with event handling.</span></span>

*   `getEventListeners(node)` <span data-ttu-id="18bbc-202">enumera todos los agentes de escucha de eventos de un nodo.</span><span class="sxs-lookup"><span data-stu-id="18bbc-202">lists all the event listeners of a node.</span></span>
*   `monitorEvents(node, events)` <span data-ttu-id="18bbc-203">supervisa y registra los eventos que ocurren en un nodo.</span><span class="sxs-lookup"><span data-stu-id="18bbc-203">monitors and logs the events that happen on a node.</span></span>

<span data-ttu-id="18bbc-204">Para enumerar todo el agente de escucha de eventos asignado al primer formulario de la página web, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-204">To list all of the event listener assigned to the first form in the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="18bbc-205">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-205">Open the **Console**.</span></span>  
1.  <span data-ttu-id="18bbc-206">Escriba o copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="18bbc-206">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Obtener todos los agentes de escucha de eventos para el primer formulario de la página web" lightbox="../media/console-dom-get-form-events.msft.png":::
    <span data-ttu-id="18bbc-208">Obtener todos los agentes de escucha de eventos para el primer formulario de la página web</span><span class="sxs-lookup"><span data-stu-id="18bbc-208">Get all events listeners for the first form in the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-209">Al supervisar, se obtiene una notificación en la **consola** cada vez que algo cambia en los elementos especificados.</span><span class="sxs-lookup"><span data-stu-id="18bbc-209">When you monitor, you to get a notification in the **Console** every time something changes to the specified elements.</span></span>  <span data-ttu-id="18bbc-210">Defina los eventos que desea escuchar como un segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="18bbc-210">You define the events you want to listen to as a second parameter.</span></span>  <span data-ttu-id="18bbc-211">Es importante que defina los eventos que desea supervisar, de lo contrario, se notifica cualquier evento que se produce en el elemento.</span><span class="sxs-lookup"><span data-stu-id="18bbc-211">It is important for you to define the events that you want to monitor, otherwise any event happening to the element is reported.</span></span>

<span data-ttu-id="18bbc-212">Para obtener una notificación en la **Consola** cada vez que se desplaza, cambie el tamaño de la ventana o cuando el usuario los tipos en el formulario de búsqueda, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-212">To get a notification in the **Console** every time you scroll, resize the window, or when the user types in the search form, complete the following actions.</span></span>  

1.  <span data-ttu-id="18bbc-213">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-213">Open the **Console**.</span></span>  
1.  <span data-ttu-id="18bbc-214">Escriba o copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="18bbc-214">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="La consola muestra todos los eventos de desplazamiento que se produce en la ventana" lightbox="../media/console-dom-monitor-events.msft.png":::
    <span data-ttu-id="18bbc-216">**La** consola muestra todos los eventos de desplazamiento que se produce en la ventana</span><span class="sxs-lookup"><span data-stu-id="18bbc-216">**Console** displays every scroll event that happens on the Window</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-217">Para registrar cualquier acción clave en el elemento seleccionado actualmente, céntrate en el formulario de búsqueda en el encabezado y selecciona algunas claves.</span><span class="sxs-lookup"><span data-stu-id="18bbc-217">To log any key action on the currently chosen element, focus on the search form in the header and select some keys.</span></span>  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="La consola muestra los eventos keyup que se suceden en el formulario" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    <span data-ttu-id="18bbc-219">**La** consola muestra `keyup` los eventos que ocurren en el formulario</span><span class="sxs-lookup"><span data-stu-id="18bbc-219">**Console** displays `keyup` events that happen on the form</span></span>  
:::image-end:::  

<span data-ttu-id="18bbc-220">Para detenerlo, quite la supervisión que estableció con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="18bbc-220">To stop it, remove the monitoring you set using the following code snippet.</span></span>  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a><span data-ttu-id="18bbc-221">Reutilizar scripts de manipulación dom</span><span class="sxs-lookup"><span data-stu-id="18bbc-221">Reuse DOM manipulation scripts</span></span>

<span data-ttu-id="18bbc-222">Puede resultar útil manipular el DOM desde la **consola**.</span><span class="sxs-lookup"><span data-stu-id="18bbc-222">You may find it useful to manipulate the DOM from the **Console**.</span></span>  <span data-ttu-id="18bbc-223">Pronto puede encontrarse con las limitaciones de la **consola como** plataforma de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="18bbc-223">You may soon run into the limitations of the **Console** as a development platform.</span></span>  <span data-ttu-id="18bbc-224">La buena noticia es que la [herramienta Orígenes][DevtoolsSourcesIndex] de DevTools ofrece un entorno de desarrollo totalmente destacado.</span><span class="sxs-lookup"><span data-stu-id="18bbc-224">The good news is that the [Sources][DevtoolsSourcesIndex] tool in DevTools offers a fully featured development environment.</span></span>  <span data-ttu-id="18bbc-225">En la **herramienta Orígenes,** puede completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="18bbc-225">In the **Sources** tool, you may complete the following actions.</span></span>  

*   <span data-ttu-id="18bbc-226">Almacene los scripts de la **consola como** [fragmentos de código][DevToolsJavascriptSnippets].</span><span class="sxs-lookup"><span data-stu-id="18bbc-226">Store your scripts for the **Console** as [Snippets][DevToolsJavascriptSnippets].</span></span>  
*   <span data-ttu-id="18bbc-227">Ejecute los scripts en una página web con un método abreviado de teclado o el editor.</span><span class="sxs-lookup"><span data-stu-id="18bbc-227">Run the scripts in a webpage using a keyboard shortcut or the editor.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="18bbc-228">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="18bbc-228">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Consola como entorno de JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Inicia sesión en la herramienta consola | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
