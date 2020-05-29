---
description: Usar la línea de comandos de consola para interactuar con una página en ejecución
title: DevTools-consola-línea de comandos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, línea de comandos de consola
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574657"
---
# <span data-ttu-id="a0fd5-104">Línea de comandos de consola</span><span class="sxs-lookup"><span data-stu-id="a0fd5-104">Console command line</span></span>

<span data-ttu-id="a0fd5-105">Use la línea de comandos de consola para ver y cambiar los valores de una página y ejecutar código de depuración sobre la marcha, todo ello aprovechando la finalización de código automático de Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) .</span><span class="sxs-lookup"><span data-stu-id="a0fd5-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="a0fd5-106">Solo tienes que introducir cualquier JavaScript válido en la línea de comandos y pulsar `Enter` para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="a0fd5-107">Para la entrada de varias líneas `Shift+Enter` , agregue un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="a0fd5-108">Use las `Up` `Down` teclas de dirección para desplazarse por los comandos de consola anteriores que especificó durante la sesión de DevTools actual.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="a0fd5-109">Además de JavaScript estándar y la [API de consola](./console-api.md), la consola también admite los siguientes comandos para:</span><span class="sxs-lookup"><span data-stu-id="a0fd5-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="a0fd5-110">Selección de objetos DOM</span><span class="sxs-lookup"><span data-stu-id="a0fd5-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="a0fd5-111">Inspeccionar propiedades de objetos</span><span class="sxs-lookup"><span data-stu-id="a0fd5-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="a0fd5-112">Buscar todos los agentes de escucha de eventos en un objeto dado</span><span class="sxs-lookup"><span data-stu-id="a0fd5-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="a0fd5-113">La secuencia de comandos escrita en la línea de comandos se ejecuta en el [ámbito global](/scripting/javascript/advanced/variable-scope-javascript) de la ventana seleccionada en ese momento, a menos que la página se haya pausado en un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="a0fd5-114">Los comandos de consola introducidos mientras la página está en pausa se ejecutarán en el [ámbito local](/scripting/javascript/advanced/variable-scope-javascript) de la función actual dentro de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="a0fd5-115">La consola tiene un menú desplegable de ejecución de **destino** justo encima del área de salida de la consola.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="a0fd5-116">La selección predeterminada es el documento de nivel superior, **_top**.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="a0fd5-117">Los iframes en el documento o las extensiones que se ejecutan también aparecerán como opciones, lo que le permite ejecutar comandos de forma alternativa dentro de esos ámbitos.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="a0fd5-118">Selectores de DOM</span><span class="sxs-lookup"><span data-stu-id="a0fd5-118">DOM selectors</span></span>
<span data-ttu-id="a0fd5-119">Estos selectores de consola proporcionan abreviaciones sencillas para acceder rápidamente a los objetos dentro del DOM:</span><span class="sxs-lookup"><span data-stu-id="a0fd5-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="a0fd5-120">$ (*Cadena de selector CSS*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="a0fd5-121">Devuelve el primer elemento del documento que coincide con el [selector CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) (o el grupo de selectores separados por comas) especificado.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="a0fd5-122">Abreviatura de [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="a0fd5-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="a0fd5-123">Ejemplo: Abra la consola y escriba `$('#main')` para devolver el objeto div con `id='main'` en esta página.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Ejemplo de uso del selector "$"](../media/console_cmd_$.png)

### <span data-ttu-id="a0fd5-125">$ $ (*Cadena de selector CSS*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="a0fd5-126">Devuelve una matriz de elementos dentro del documento que coincide con el [selector CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) especificado (o la cadena de selectores separados por comas).</span><span class="sxs-lookup"><span data-stu-id="a0fd5-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="a0fd5-127">Abreviatura de [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="a0fd5-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="a0fd5-128">Ejemplo: Abra la consola y escriba `$$('.container')` para devolver todos los objetos div con `class='container'` en esta página.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Ejemplo de uso del selector $ $ '](../media/console_cmd_$$.png)

### <span data-ttu-id="a0fd5-130">$0, $1, $2,...</span><span class="sxs-lookup"><span data-stu-id="a0fd5-130">$0, $1, $2,...</span></span>
<span data-ttu-id="a0fd5-131">Devuelve los últimos elementos seleccionados en el panel [**elementos**](../elements.md) , donde `$0` representa el elemento seleccionado actualmente, `$1` y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="a0fd5-132">Ejemplo: Abra DevTools en la pestaña **elementos** , presione `CTRL + B` para activar la herramienta **Seleccionar elemento** y haga clic en un área de esta página con el mouse.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="a0fd5-133">Ahora abra la consola y escriba `$0` para devolver el elemento en el que acaba de hacer clic.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Ejemplo de uso del selector ' $0 '](../media/console_cmd_$0.png)

### <span data-ttu-id="a0fd5-135">$x (*expresión XPath*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="a0fd5-136">Devuelve una matriz de elementos coincidentes con la expresión [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) especificada.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="a0fd5-137">Ejemplo: Abra la consola y escriba `$x('//script[@defer]')` para devolver todos los `<script>` elementos de esta página que contienen un `defer` atributo.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Ejemplo de uso del selector ' $x '](../media/console_cmd_$x.png)

## <span data-ttu-id="a0fd5-139">Inspección de objetos</span><span class="sxs-lookup"><span data-stu-id="a0fd5-139">Object inspection</span></span>

<span data-ttu-id="a0fd5-140">Estos comandos proporcionan formas rápidas de inspeccionar las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="a0fd5-141">El objeto especificado debe definirse en el espacio de nombres global o en el ámbito actual del depurador.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="a0fd5-142">DIR (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-142">dir(*object*)</span></span>
<span data-ttu-id="a0fd5-143">Devuelve una lista de las propiedades del objeto especificado en vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="a0fd5-144">Ejemplo: Abra la consola y escriba `dir(document)` para ver las propiedades del objeto de documento que representa esta página.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Ejemplo de uso del método ' dir '](../media/console_cmd_dir.png)

### <span data-ttu-id="a0fd5-146">Keys (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-146">keys(*object*)</span></span>
<span data-ttu-id="a0fd5-147">Devuelve una matriz de nombres de propiedad adjuntos al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="a0fd5-148">Ejemplo: Abra la consola y escriba `keys(window)` para devolver todas las propiedades definidas en el objeto de ventana global.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Ejemplo de uso del método ' Keys '](../media/console_cmd_keys.png)

### <span data-ttu-id="a0fd5-150">Values (*Object*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-150">values(*object*)</span></span>
<span data-ttu-id="a0fd5-151">Devuelve una matriz de valores de propiedad asociada al objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="a0fd5-152">Ejemplo: Abra la consola y escriba `values(window)` para devolver los valores de todas las propiedades (claves) definidas en el objeto de ventana global.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Ejemplo de uso del método ' Values '](../media/console_cmd_values.png)

## <span data-ttu-id="a0fd5-154">Detectores de eventos</span><span class="sxs-lookup"><span data-stu-id="a0fd5-154">Event listeners</span></span>

<span data-ttu-id="a0fd5-155">Este comando le permite inspeccionar los agentes de escucha de eventos registrados en un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="a0fd5-156">El objeto especificado debe definirse en el espacio de nombres global o en el ámbito actual del depurador.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="a0fd5-157">getEventListeners (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a0fd5-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="a0fd5-158">Devuelve un objeto que contiene una clave para cada tipo de evento registrado en el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="a0fd5-159">El valor de cada clave es una matriz de agentes de escucha de eventos y su información relacionada.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="a0fd5-160">Ejemplo: Abra la consola y escriba `getEventListeners(document)` para ver todas las escuchas de eventos registradas en el objeto de documento de esta página.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Ejemplo de uso del método ' getEventListeners '](../media/console_cmd_getEventListeners.png)
