---
title: Navegar por Microsoft Edge DevTools con tecnología de asistencia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573246"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="db890-103">Navegar por Microsoft Edge DevTools con tecnología de asistencia</span><span class="sxs-lookup"><span data-stu-id="db890-103">Navigate Microsoft Edge DevTools With Assistive Technology</span></span>   



<span data-ttu-id="db890-104">Esta guía pretende ayudar a los usuarios que principalmente dependen de la tecnología de asistencia, como los lectores de pantalla, para acceder y usar Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="db890-104">This guide aims to help users who primarily rely on assistive technology like screen readers access and use Microsoft Edge DevTools.</span></span>  <span data-ttu-id="db890-105">Microsoft Edge DevTools es un conjunto de herramientas para desarrolladores web integrado en el explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db890-105">Microsoft Edge DevTools is a suite of web developer tools built into the Microsoft Edge browser.</span></span>  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

<span data-ttu-id="db890-106">La accesibilidad de DevTools es un trabajo en curso.</span><span class="sxs-lookup"><span data-stu-id="db890-106">The accessibility of DevTools is a work-in-progress.</span></span>  <span data-ttu-id="db890-107">Algunos paneles y pestañas funcionan mejor con la tecnología de asistencia que otros.</span><span class="sxs-lookup"><span data-stu-id="db890-107">Some panels and tabs work better with assistive technology than others.</span></span>  <span data-ttu-id="db890-108">Esta guía le guiará a través de los paneles que son los problemas específicos más accesibles y resaltados que puede encontrarse durante el proceso.</span><span class="sxs-lookup"><span data-stu-id="db890-108">This guide walks you through the panels which are the most accessible and highlights specific issues you may encounter along the way.</span></span>  

## <span data-ttu-id="db890-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="db890-109">Overview</span></span>   

<span data-ttu-id="db890-110">Antes de comenzar, ayuda a tener un modelo mental de estructurar la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="db890-110">Before starting, it helps to have a mental model of how the DevTools UI is structured.</span></span>  <span data-ttu-id="db890-111">DevTools se divide en una serie de paneles que se organizan en [un `tablist` Aria ][W3CWaiAriaTablist].</span><span class="sxs-lookup"><span data-stu-id="db890-111">DevTools is divided into a series of panels which are organized into an [ARIA `tablist`][W3CWaiAriaTablist].</span></span>  

<span data-ttu-id="db890-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="db890-112">For example:</span></span>  

*   <span data-ttu-id="db890-113">El panel **elementos** le permite ver y cambiar nodos DOM o [CSS] [DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="db890-113">The **Elements** panel lets you view and change DOM nodes or [CSS][DevtoolsCssIndex].</span></span>  
*   <span data-ttu-id="db890-114">El [panel de**consola** ] [DevtoolsConsoleIndex] le permite leer registros de JavaScript y objetos de edición en vivo.</span><span class="sxs-lookup"><span data-stu-id="db890-114">The [**Console** panel][DevtoolsConsoleIndex] lets you read JavaScript logs and live edit objects.</span></span>  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

<span data-ttu-id="db890-115">Dentro del área de contenido de cada panel hay varias herramientas diferentes, a menudo denominadas fichas o paneles en la documentación.</span><span class="sxs-lookup"><span data-stu-id="db890-115">Within the content area of each panel, there are a number of different tools, often referred to as tabs or panes in the documentation.</span></span>  
<span data-ttu-id="db890-116">Por ejemplo, el panel **elementos** contiene pestañas adicionales para inspeccionar detectores de eventos, el árbol de accesibilidad y mucho más.</span><span class="sxs-lookup"><span data-stu-id="db890-116">For instance, the **Elements** panel contains additional tabs to inspect event listeners, the accessibility tree, and much more.</span></span>  <span data-ttu-id="db890-117">La distinción entre las pestañas y los paneles es algo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="db890-117">The distinction between tabs and panes is somewhat arbitrary.</span></span>  <span data-ttu-id="db890-118">El único motivo por el que puedes ver un término u otro es mantener la coherencia con el resto de la documentación oficial de DevTools.</span><span class="sxs-lookup"><span data-stu-id="db890-118">The only reason you may see one term or the other is to maintain consistency with the rest of the official DevTools documentation.</span></span>  

## <span data-ttu-id="db890-119">Métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="db890-119">Keyboard shortcuts</span></span>   

<span data-ttu-id="db890-120">La [referencia de métodos abreviados de teclado de DevTools] [DevtoolsShortcuts] es una Cheatsheet útil.</span><span class="sxs-lookup"><span data-stu-id="db890-120">The [DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] is a helpful cheatsheet.</span></span>  <span data-ttu-id="db890-121">Asegúrese de marcarlo y hacer referencia a él mientras explora los distintos paneles.</span><span class="sxs-lookup"><span data-stu-id="db890-121">Be sure to bookmark it and refer back to it as you explore the different panels.</span></span>  

## <span data-ttu-id="db890-122">Abrir DevTools</span><span class="sxs-lookup"><span data-stu-id="db890-122">Open DevTools</span></span>   

<span data-ttu-id="db890-123">Para comenzar, Lee [abrir Microsoft Edge DevTools] [DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="db890-123">To get started, read through [Open Microsoft Edge DevTools][DevtoolsOpen].</span></span>  <span data-ttu-id="db890-124">Hay varias maneras de abrir DevTools, ya sea mediante métodos abreviados de teclado o elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="db890-124">There are a number of ways to open DevTools, either through keyboard shortcuts or menu items.</span></span>  

## <span data-ttu-id="db890-125">Navegar entre paneles</span><span class="sxs-lookup"><span data-stu-id="db890-125">Navigate between panels</span></span>   

### <span data-ttu-id="db890-126">Navegar por el teclado</span><span class="sxs-lookup"><span data-stu-id="db890-126">Navigate by keyboard</span></span>   

*   <span data-ttu-id="db890-127">Con DevTools abierto, pulse `Control` + `]` \ (Windows \) o `Command` + `]` \ (MacOS \) para centrarse en el siguiente panel.</span><span class="sxs-lookup"><span data-stu-id="db890-127">With DevTools open, press `Control`+`]` \(Windows\) or `Command`+`]` \(macOS\) to focus the next panel.</span></span>  
*   <span data-ttu-id="db890-128">Pulse `Control` + `[` \ (Windows \) o `Command` + `[` \ (MacOS \) para centrarse en el panel anterior.</span><span class="sxs-lookup"><span data-stu-id="db890-128">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) to focus the previous panel.</span></span>  
*   <span data-ttu-id="db890-129">También es posible usar `Shift` + `Tab` para mover el foco al [ `tablist` Aria][W3CWaiAriaTablist] de un panel y usar las teclas de dirección para cambiar los paneles, aunque puede ser más rápido usar los accesos directos mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="db890-129">It is also possible to use `Shift`+`Tab` to move focus into the [ARIA `tablist`][W3CWaiAriaTablist] of a panel and use the arrow keys to change panels, though it may be faster to use the previously mentioned shortcuts.</span></span>  

#### <span data-ttu-id="db890-130">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-130">Known issues</span></span>   

*   <span data-ttu-id="db890-131">Algunos paneles, como la **consola** y el panel de **rendimiento** , pueden mover el foco a su área de contenido tan pronto como se activen.</span><span class="sxs-lookup"><span data-stu-id="db890-131">Some panels, such as the **Console** and **Performance** panels, may move focus into their content area as soon as they are activated.</span></span>  <span data-ttu-id="db890-132">Esto puede dificultar la navegación por las teclas de dirección.</span><span class="sxs-lookup"><span data-stu-id="db890-132">This may make navigating by arrow keys difficult.</span></span>  
*   <span data-ttu-id="db890-133">Se anuncia el nombre del panel seleccionado, pero solo después de que haya leído el contenido centrado en el panel.</span><span class="sxs-lookup"><span data-stu-id="db890-133">The name of the selected panel is announced, but only after it has read the focused content in the panel.</span></span>  <span data-ttu-id="db890-134">Esto puede resultar muy fácil de perder.</span><span class="sxs-lookup"><span data-stu-id="db890-134">This may make it very easy to miss.</span></span>  

### <span data-ttu-id="db890-135">Navegar por el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="db890-135">Navigate by Command Menu</span></span>   

<span data-ttu-id="db890-136">Para centrar un panel específico, use el [**menú de comandos**] [DevtoolsCommandMenuIndex]:</span><span class="sxs-lookup"><span data-stu-id="db890-136">To focus a specific panel, use the [**Command Menu**][DevtoolsCommandMenuIndex]:</span></span>  

1.  <span data-ttu-id="db890-137">Con DevTools abierto, pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="db890-137">With DevTools open, press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    <span data-ttu-id="db890-138">El **menú comando** es un ComboBox de autocompletar de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="db890-138">The **Command Menu** is a fuzzy search autocomplete combobox.</span></span>  
1.  <span data-ttu-id="db890-139">Escriba el nombre del panel que desea abrir y, después, use el `Down Arrow` teclado para desplazarse a la opción correcta.</span><span class="sxs-lookup"><span data-stu-id="db890-139">Type the name of the panel you want to open, then use the `Down Arrow` on the keyboard to navigate to the correct option.</span></span>  
1.  <span data-ttu-id="db890-140">Pulse `Enter` para ejecutar un comando.</span><span class="sxs-lookup"><span data-stu-id="db890-140">Press `Enter` to run a command.</span></span>  

<span data-ttu-id="db890-141">Por ejemplo, para abrir el panel **elementos** :</span><span class="sxs-lookup"><span data-stu-id="db890-141">For example, to open the **Elements** panel:</span></span>  

1.  <span data-ttu-id="db890-142">Abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="db890-142">Open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="db890-143">Escriba `E` a continuación `L` .</span><span class="sxs-lookup"><span data-stu-id="db890-143">Type `E` then `L`.</span></span>  <span data-ttu-id="db890-144">La opción **Panel > Mostrar elementos** está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="db890-144">The **Panel > Show Elements** option is selected.</span></span>  
1.  <span data-ttu-id="db890-145">Pulse `Enter` para ejecutar el comando que abre el panel.</span><span class="sxs-lookup"><span data-stu-id="db890-145">Press `Enter` to run the command that opens the panel.</span></span>  

<span data-ttu-id="db890-146">Al abrir un panel de esta forma, se dirige el foco al contenido del panel.</span><span class="sxs-lookup"><span data-stu-id="db890-146">Opening a panel this way directs focus to the contents of the panel.</span></span>  <span data-ttu-id="db890-147">En el caso del panel **elementos** , el foco se mueve al **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="db890-147">In the case of the **Elements** panel, focus moves into the **DOM Tree**.</span></span>  

## <span data-ttu-id="db890-148">Panel elementos</span><span class="sxs-lookup"><span data-stu-id="db890-148">Elements panel</span></span>   

### <span data-ttu-id="db890-149">Inspeccionar un elemento de la página</span><span class="sxs-lookup"><span data-stu-id="db890-149">Inspect an element on the page</span></span>   

1.  <span data-ttu-id="db890-150">Vaya al elemento que desea inspeccionar usando el cursor en el lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="db890-150">Navigate to the element you want to inspect using the cursor in the screen reader.</span></span>  
1.  <span data-ttu-id="db890-151">Simula un clic con el botón secundario del mouse en el elemento para abrir el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="db890-151">Simulate a right-mouse click on the element to open the context menu.</span></span>  
1.  <span data-ttu-id="db890-152">Elija la opción **inspeccionar** .</span><span class="sxs-lookup"><span data-stu-id="db890-152">Choose the **Inspect** option.</span></span>  <span data-ttu-id="db890-153">Esto abre el panel **elementos** y se centra en el elemento del **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="db890-153">This opens the **Elements** panel and focuses the element in the **DOM Tree**.</span></span>  

<!--todo:  add dom nodes (elements pane) section when available  -->  

<span data-ttu-id="db890-154">El **árbol DOM** se coloca como [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="db890-154">The **DOM Tree** is laid out as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### <span data-ttu-id="db890-155">Copiar el código de un elemento en el árbol DOM</span><span class="sxs-lookup"><span data-stu-id="db890-155">Copy the code for an element in the DOM Tree</span></span>   

1.  <span data-ttu-id="db890-156">Con el foco en un nodo del **árbol DOM**, mostrar el menú contextual del botón secundario.</span><span class="sxs-lookup"><span data-stu-id="db890-156">With focus on a node in the **DOM Tree**, bring up the right-click context menu.</span></span>  
1.  <span data-ttu-id="db890-157">Expanda la opción **copiar** .</span><span class="sxs-lookup"><span data-stu-id="db890-157">Expand the **Copy** option.</span></span>  
1.  <span data-ttu-id="db890-158">Seleccione **copiar outerHTML**.</span><span class="sxs-lookup"><span data-stu-id="db890-158">Select **Copy outerHTML**.</span></span>  

#### <span data-ttu-id="db890-159">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-159">Known issues</span></span>   

*   <span data-ttu-id="db890-160">La **copia outerHTML** a menudo no selecciona el nodo actual, sino que selecciona el nodo primario.</span><span class="sxs-lookup"><span data-stu-id="db890-160">**Copy outerHTML** often does not select the current node but instead selects the parent node.</span></span>  <span data-ttu-id="db890-161">Sin embargo, el contenido del elemento aún debe estar en el outerHTML copiado.</span><span class="sxs-lookup"><span data-stu-id="db890-161">However, the contents of the element should still be in the copied outerHTML.</span></span>  

### <span data-ttu-id="db890-162">Modificar los atributos de un elemento en el árbol DOM</span><span class="sxs-lookup"><span data-stu-id="db890-162">Modify the attributes of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="db890-163">Con el foco en un nodo del **árbol DOM**, púlselo `Enter` para que sea editable.</span><span class="sxs-lookup"><span data-stu-id="db890-163">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="db890-164">Pulse `Tab` para desplazarse entre valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="db890-164">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="db890-165">Cuando escuche "Space", se encuentra dentro de una entrada de texto vacía y puede escribir un nuevo valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="db890-165">When you hear "space" you are inside of an empty text input and are able to type a new attribute value.</span></span>  
*   <span data-ttu-id="db890-166">Pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para aceptar el cambio y oír todo el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="db890-166">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change and hear the entire contents of the element.</span></span>  

#### <span data-ttu-id="db890-167">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-167">Known issues</span></span>   

*   <span data-ttu-id="db890-168">Cuando escribes en la entrada de texto, no obtienes Comentarios.</span><span class="sxs-lookup"><span data-stu-id="db890-168">When you type into the text input you get no feedback.</span></span>  <span data-ttu-id="db890-169">Si hace un error ortográfico y usa las teclas de dirección para explorar la entrada, tampoco recibirá Comentarios.</span><span class="sxs-lookup"><span data-stu-id="db890-169">If you make a typo and use the arrow keys to explore your input you also get no feedback.</span></span>  <span data-ttu-id="db890-170">La manera más sencilla de comprobar su trabajo es aceptar el cambio y, a continuación, escuchar que se anuncie todo el elemento.</span><span class="sxs-lookup"><span data-stu-id="db890-170">The easiest way to check your work is to accept the change, then listen for the entire element to be announced.</span></span>  

### <span data-ttu-id="db890-171">Editar el código HTML de un elemento en el árbol DOM</span><span class="sxs-lookup"><span data-stu-id="db890-171">Edit the HTML of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="db890-172">Con el foco en un nodo del **árbol DOM**, púlselo `Enter` para que sea editable.</span><span class="sxs-lookup"><span data-stu-id="db890-172">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="db890-173">Pulse `Tab` para desplazarse entre valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="db890-173">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="db890-174">Al oír el nombre del elemento, por ejemplo, "H2", se encuentra dentro de una entrada de texto y puede cambiar el tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="db890-174">When you hear the name of the element, for instance, "h2", you are inside of a text input and may change the type of the element.</span></span>  
*   <span data-ttu-id="db890-175">Pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para aceptar el cambio.</span><span class="sxs-lookup"><span data-stu-id="db890-175">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change.</span></span>  

<span data-ttu-id="db890-176">Por ejemplo, si escribe `h3` y presiona `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) cambia las etiquetas de apertura y final del elemento a `h3` .</span><span class="sxs-lookup"><span data-stu-id="db890-176">For example, typing `h3` and pressing `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) changes the start and end tags of the element to `h3`.</span></span>  

## <span data-ttu-id="db890-177">Pestañas del panel elementos</span><span class="sxs-lookup"><span data-stu-id="db890-177">Elements panel tabs</span></span>   

<span data-ttu-id="db890-178">El panel **elementos** contiene pestañas adicionales para inspeccionar cosas como la CSS aplicada a un elemento o al lugar relevante en el árbol de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="db890-178">The **Elements** panel contains additional tabs for inspecting things like the CSS applied to an element or the relevant place in the accessibility tree.</span></span>  

*   <span data-ttu-id="db890-179">Con el foco en un nodo del **árbol DOM**, presione `Tab` hasta que escuche que el panel **estilos** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="db890-179">With focus on a node in the **DOM Tree**, press `Tab` until you hear that the **Styles** pane is selected.</span></span>  
*   <span data-ttu-id="db890-180">Use el `Right Arrow` para explorar otras pestañas disponibles.</span><span class="sxs-lookup"><span data-stu-id="db890-180">Use the `Right Arrow` to explore other available tabs.</span></span>  

<span data-ttu-id="db890-181">El **árbol DOM** convierte los elementos con `href` atributos en vínculos activables, por lo que es posible que tenga que presionar `Tab` más de una vez para llegar al panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="db890-181">The **DOM Tree** turns elements with `href` attributes into focusable links, so you may need to press `Tab` more than once to reach the **Styles** pane.</span></span>  

### <span data-ttu-id="db890-182">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-182">Known issues</span></span>   

<span data-ttu-id="db890-183">Las pestañas **puntos de interrupción** y **propiedades** de Dom no son accesibles desde el teclado.</span><span class="sxs-lookup"><span data-stu-id="db890-183">The **DOM Breakpoints** and **Properties** tabs are not keyboard accessible.</span></span>  

### <span data-ttu-id="db890-184">Panel estilos</span><span class="sxs-lookup"><span data-stu-id="db890-184">Styles pane</span></span>   

<span data-ttu-id="db890-185">En el panel **estilos** encontrará controles para filtrar estilos, alternar Estados de elementos \ (como [`:active`][MDNActive] y [`:focus`][MDNFocus] \), alternar clases y agregar nuevas clases.</span><span class="sxs-lookup"><span data-stu-id="db890-185">In the **Styles** pane find controls for filtering styles, toggling element states \(such as [`:active`][MDNActive] and [`:focus`][MDNFocus]\), toggling classes, and adding new classes.</span></span>  <span data-ttu-id="db890-186">También hay una herramienta de inspección de estilo eficaz para explorar y modificar los estilos aplicados actualmente al elemento que se encuentra en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="db890-186">There is also a powerful style inspection tool to explore and modify styles currently applied to the element that is in focus in the **DOM Tree**.</span></span>  

<span data-ttu-id="db890-187">El concepto clave que se debe comprender sobre el panel **estilos** es que solo muestra los estilos para el nodo seleccionado en ese momento en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="db890-187">The key concept to understand about the **Styles** pane is that it only shows styles for the currently-selected node in the **DOM Tree**.</span></span>  <span data-ttu-id="db890-188">Por ejemplo, supongamos que ha terminado de inspeccionar los estilos de un `<header>` nodo y ahora desea ver los estilos de un `<footer>` nodo.</span><span class="sxs-lookup"><span data-stu-id="db890-188">For example, suppose you are done inspecting the styles of a `<header>` node, and now you want to look at the styles for a `<footer>` node.</span></span>  <span data-ttu-id="db890-189">Para ello, primero debe seleccionar el `<footer>` nodo en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="db890-189">To do that, you first need to select the `<footer>` node in the **DOM Tree**.</span></span>  <span data-ttu-id="db890-190">Es posible que le resulte más rápido usar [el flujo de trabajo para inspeccionar](#inspect-an-element-on-the-page) un nodo que se encuentra en la general del `footer` nodo \ (como un vínculo dentro del pie de página \), que se centra en el **árbol DOM**y, a continuación, usar el teclado para navegar hasta el nodo exacto en el que esté interesado.</span><span class="sxs-lookup"><span data-stu-id="db890-190">You may find it faster to use the [Inspect](#inspect-an-element-on-the-page) workflow to inspect a node that is in the general vicinity of the `footer` node \(such as a link within the footer\), which focuses the **DOM Tree**, and then use your keyboard to navigate to the exact node in which you are interested.</span></span>  

#### <span data-ttu-id="db890-191">Navegar por el panel estilos</span><span class="sxs-lookup"><span data-stu-id="db890-191">Navigate the Styles pane</span></span>   

<span data-ttu-id="db890-192">Puesto que todas las herramientas de estilo se conectan de una forma u otra al panel **estilos** , tiene sentido dominar esta herramienta en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="db890-192">Because all of the style tools connect in one way or another back to the **Styles** pane, it makes sense to master this tool first.</span></span>  

*   <span data-ttu-id="db890-193">Con el foco en el panel **estilos** , presione `Tab` para mover el foco dentro y explorar el contenido.</span><span class="sxs-lookup"><span data-stu-id="db890-193">With focus on the **Styles** pane, press `Tab` to move focus inside and explore the contents.</span></span>  
*   <span data-ttu-id="db890-194">Presione `Tab` hasta que el primer estilo se active.</span><span class="sxs-lookup"><span data-stu-id="db890-194">Press `Tab` until the first style becomes active.</span></span>  <span data-ttu-id="db890-195">Si está usando un lector de pantalla, este primer estilo se anuncia como "Element. style {} ".</span><span class="sxs-lookup"><span data-stu-id="db890-195">If you are using a screen reader this first style is announced as "element.style {}".</span></span>  
*   <span data-ttu-id="db890-196">Pulse `Down Arrow` para desplazarse por la lista de estilos por orden de especificidad.</span><span class="sxs-lookup"><span data-stu-id="db890-196">Press `Down Arrow` to navigate the list of styles in order of specificity.</span></span>  <span data-ttu-id="db890-197">Un lector de pantalla anuncia cada estilo empezando por el nombre del archivo CSS, el número de línea en el que aparece el estilo y el nombre del estilo.</span><span class="sxs-lookup"><span data-stu-id="db890-197">A screen reader announces each style starting with the name of the CSS file, the line number on which the style appears, and the name of the style.</span></span>  <span data-ttu-id="db890-198">Por ejemplo: "Main. CSS: 233. card__img {} "</span><span class="sxs-lookup"><span data-stu-id="db890-198">For example: "main.css:233 .card__img {}"</span></span>  
*   <span data-ttu-id="db890-199">Pulse `Enter` para inspeccionar un estilo de forma más detallada.</span><span class="sxs-lookup"><span data-stu-id="db890-199">Press `Enter` to inspect a style in more detail.</span></span>  <span data-ttu-id="db890-200">El foco comienza en una versión editable del nombre de estilo.</span><span class="sxs-lookup"><span data-stu-id="db890-200">Focus begins on an editable version of the style name.</span></span>  
*   <span data-ttu-id="db890-201">Pulse `Tab` para desplazarse entre las versiones editables de cada propiedad de CSS y sus valores correspondientes.</span><span class="sxs-lookup"><span data-stu-id="db890-201">Press `Tab` to move between editable versions of each CSS property and their corresponding values.</span></span>  <span data-ttu-id="db890-202">Al final de cada bloque de estilo hay un campo de texto editable en blanco que puede usar para agregar propiedades de CSS adicionales.</span><span class="sxs-lookup"><span data-stu-id="db890-202">At the end of each style block is a blank editable text field which you may use to add additional CSS properties.</span></span>  
*   <span data-ttu-id="db890-203">Puede seguir presionando `Tab` para desplazarse por la lista de estilos o presionar `Escape` para salir de este modo y volver a navegar por las teclas de dirección.</span><span class="sxs-lookup"><span data-stu-id="db890-203">You may continue to press `Tab` to move through the list of styles, or press `Escape` to exit this mode and go back to navigating by arrow keys.</span></span>  

<span data-ttu-id="db890-204">Asegúrese de leer la [Referencia del teclado del panel de estilos] [DevtoolsShortcutsStylesPaneKeyboard] para obtener métodos abreviados adicionales.</span><span class="sxs-lookup"><span data-stu-id="db890-204">Be sure to read through the [Styles pane keyboard reference][DevtoolsShortcutsStylesPaneKeyboard] for additional shortcuts.</span></span>  

##### <span data-ttu-id="db890-205">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-205">Known Issues</span></span>   

*   <span data-ttu-id="db890-206">Si usa el campo de texto editable **filtro** , ya no podrá navegar por la lista de estilos.</span><span class="sxs-lookup"><span data-stu-id="db890-206">If you use the **Filter** editable text field, you are no longer be able to navigate the list of styles.</span></span>  

#### <span data-ttu-id="db890-207">Alternar estado del elemento</span><span class="sxs-lookup"><span data-stu-id="db890-207">Toggle element state</span></span>   

<span data-ttu-id="db890-208">Para alternar el estado de un elemento, como `:active` o `:focus` :</span><span class="sxs-lookup"><span data-stu-id="db890-208">To toggle the state of an element, such as `:active` or `:focus`:</span></span>  

1.  <span data-ttu-id="db890-209">Vaya al panel **estilos** y presione `Tab` hasta que el botón **Estado del elemento de alternancia** tenga el foco.</span><span class="sxs-lookup"><span data-stu-id="db890-209">Navigate to the **Styles** pane and press `Tab` until the **Toggle Element State** button has focus.</span></span>  
1.  <span data-ttu-id="db890-210">Pulse `Enter` para expandir la colección de Estados de elementos.</span><span class="sxs-lookup"><span data-stu-id="db890-210">Press `Enter` to expand the collection of element states.</span></span>  <span data-ttu-id="db890-211">Los Estados de los elementos se presentan como un grupo de casillas de verificación.</span><span class="sxs-lookup"><span data-stu-id="db890-211">The element states are presented as a group of checkboxes.</span></span>  
1.  <span data-ttu-id="db890-212">Presione `Tab` hasta el primer estado, `:active` , que tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="db890-212">Press `Tab` until the first state, `:active`, has focus.</span></span>  
1.  <span data-ttu-id="db890-213">Púlselo `Space` para habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="db890-213">Press `Space` to enable it.</span></span>  <span data-ttu-id="db890-214">Si el elemento seleccionado actualmente en el árbol DOM tiene un `:active` estilo, ahora se aplica.</span><span class="sxs-lookup"><span data-stu-id="db890-214">If the currently-selected element in the DOM Tree has an `:active` style, it is now applied.</span></span>  
1.  <span data-ttu-id="db890-215">Siga presionando `Tab` para explorar todos los Estados disponibles.</span><span class="sxs-lookup"><span data-stu-id="db890-215">Continue pressing `Tab` to explore all of the available states.</span></span>  

#### <span data-ttu-id="db890-216">Agregar una clase existente</span><span class="sxs-lookup"><span data-stu-id="db890-216">Add an existing class</span></span>   

<span data-ttu-id="db890-217">Junto al botón de **Estado del elemento de alternancia** se encuentra el botón clases de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="db890-217">Adjacent to the **Toggle Element State** button is the **Element Classes** button.</span></span>  <span data-ttu-id="db890-218">Para mover el foco a él `Tab` , pulsa en `Enter` .</span><span class="sxs-lookup"><span data-stu-id="db890-218">Move focus to it by pressing `Tab` then `Enter`.</span></span>  <span data-ttu-id="db890-219">El foco se mueve a un campo de texto de edición denominado **Agregar nueva clase**.</span><span class="sxs-lookup"><span data-stu-id="db890-219">Focus moves into an edit text field labeled **Add New Class**.</span></span>  

<span data-ttu-id="db890-220">El botón **clases de elementos** se usa principalmente para agregar clases existentes a un elemento.</span><span class="sxs-lookup"><span data-stu-id="db890-220">The **Element Classes** button is primarily used for adding existing classes to an element.</span></span>  <span data-ttu-id="db890-221">Por ejemplo, si la hoja de estilos contiene una clase auxiliar denominada `.clearfix` , puede presionar `.` dentro del campo editar texto para ver una lista de sugerencias de clases y usar el `Down Arrow` para buscar la `.clearfix` sugerencia.</span><span class="sxs-lookup"><span data-stu-id="db890-221">For example, if your stylesheet contained a helper class named `.clearfix` you may press `.` inside of the edit text field to see a suggestion list of classes and use the `Down Arrow` to find the `.clearfix` suggestion.</span></span>  <span data-ttu-id="db890-222">O bien, escriba el nombre de la clase y pulse `Enter` para aplicarlo.</span><span class="sxs-lookup"><span data-stu-id="db890-222">Or type the class name out yourself and press `Enter` to apply it.</span></span>  

#### <span data-ttu-id="db890-223">Agregar una nueva regla de estilo</span><span class="sxs-lookup"><span data-stu-id="db890-223">Add a new style rule</span></span>   

<span data-ttu-id="db890-224">Junto al botón **clases de elementos** se encuentra el botón **nueva regla de estilo** .</span><span class="sxs-lookup"><span data-stu-id="db890-224">Adjacent to the **Element Classes** button is the **New Style Rule** button.</span></span>  <span data-ttu-id="db890-225">Mueva el foco pulsando `Tab` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="db890-225">Move focus to it by pressing `Tab` and press `Enter`.</span></span>  <span data-ttu-id="db890-226">El foco se mueve a un campo de texto editable dentro del inspector de estilo.</span><span class="sxs-lookup"><span data-stu-id="db890-226">Focus moves into an editable text field inside of the style inspector.</span></span>  <span data-ttu-id="db890-227">El contenido de texto inicial del campo es el nombre de etiqueta del elemento que está seleccionado en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="db890-227">The initial text content of the field is the tag name of the element that is selected in the **DOM Tree**.</span></span>  
<span data-ttu-id="db890-228">Puede escribir el nombre de la clase que desee en este campo y, a continuación, presionar `Tab` para asignarle propiedades de CSS.</span><span class="sxs-lookup"><span data-stu-id="db890-228">You may type any class name you want into this field and then press `Tab` to assign CSS properties to it.</span></span>  

### <span data-ttu-id="db890-229">Pestaña calculada</span><span class="sxs-lookup"><span data-stu-id="db890-229">Computed tab</span></span>   

<span data-ttu-id="db890-230">Con el foco en la pestaña **calculada** , presione `Tab` para mover el foco dentro y explorar el contenido.</span><span class="sxs-lookup"><span data-stu-id="db890-230">With focus on the **Computed** tab, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="db890-231">En la pestaña **calculada** hay controles para explorar qué propiedades de CSS se aplican realmente a un elemento en orden de especificidad.</span><span class="sxs-lookup"><span data-stu-id="db890-231">Within the **Computed** tab there are controls for exploring which CSS properties are actually applied to an element in order of specificity.</span></span>  

<!--todo: add computed tab section when available  -->  

#### <span data-ttu-id="db890-232">Explorar todos los estilos calculados</span><span class="sxs-lookup"><span data-stu-id="db890-232">Explore all computed styles</span></span>   

<span data-ttu-id="db890-233">Presione `Tab` hasta que llegue a la colección de estilos calculados.</span><span class="sxs-lookup"><span data-stu-id="db890-233">Press `Tab` until you reach the collection of computed styles.</span></span>  <span data-ttu-id="db890-234">Se presentan como [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="db890-234">These are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="db890-235">Al expandir un control ListBox, se revela qué selectores CSS están aplicando el estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="db890-235">Expanding a listbox reveals which CSS selectors are applying the computed style.</span></span>  <span data-ttu-id="db890-236">Estos selectores están organizados por especificidad.</span><span class="sxs-lookup"><span data-stu-id="db890-236">These selectors are organized by specificity.</span></span>  <span data-ttu-id="db890-237">Un lector de pantalla anuncia el valor calculado, que actualmente coincide con el selector de CSS, el nombre de archivo de la hoja de estilos que contiene el selector y el número de línea del selector.</span><span class="sxs-lookup"><span data-stu-id="db890-237">A screen reader announces the computed value, which CSS selector is currently matching, the filename of the stylesheet that contains the selector, and the line number for the selector.</span></span>  

#### <span data-ttu-id="db890-238">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-238">Known issues</span></span>   

*   <span data-ttu-id="db890-239">Si usa el campo de texto de **filtro** , ya no podrá inspeccionar estilos.</span><span class="sxs-lookup"><span data-stu-id="db890-239">If you use the **Filter** text field, you are no longer able to inspect styles.</span></span>  

### <span data-ttu-id="db890-240">Pestaña detectores de eventos</span><span class="sxs-lookup"><span data-stu-id="db890-240">Event listeners tab</span></span>   

<span data-ttu-id="db890-241">Desde el panel **elementos** , puede inspeccionar las escuchas de eventos que se aplican a un elemento mediante la pestaña **detectores de eventos** .  Con el foco en el panel **estilos** , pulse el `Right Arrow` para ir a la pestaña **detectores de eventos** .</span><span class="sxs-lookup"><span data-stu-id="db890-241">From within the **Elements** panel you may inspect the event listeners applied to an element using the **Event Listeners** tab.  With focus on the **Styles** pane, press the `Right Arrow` to navigate to the **Event Listeners** tab.</span></span>  

#### <span data-ttu-id="db890-242">Explorar detectores de eventos</span><span class="sxs-lookup"><span data-stu-id="db890-242">Explore event listeners</span></span>   

<span data-ttu-id="db890-243">Los detectores de eventos se presentan [como `tree` Aria ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="db890-243">Event listeners are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="db890-244">Puede usar las teclas de dirección para desplazarse.</span><span class="sxs-lookup"><span data-stu-id="db890-244">You may use the arrow keys to navigate them.</span></span>  <span data-ttu-id="db890-245">Un lector de pantalla anuncia el nombre del objeto DOM al que está asociada la escucha de eventos, así como el nombre de archivo en el que se define el agente de escucha de eventos y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="db890-245">A screen reader announces the name of the DOM object that the event listener is attached to, as well as the file name where the event listener is defined and the line number.</span></span>  

### <span data-ttu-id="db890-246">Panel Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="db890-246">Accessibility pane</span></span>   

<span data-ttu-id="db890-247">Con el foco en el panel **accesibilidad** , presione `Tab` para mover el foco dentro y explorar el contenido.</span><span class="sxs-lookup"><span data-stu-id="db890-247">With focus on the **Accessibility** pane, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="db890-248">En el panel **accesibilidad** , hay controles para explorar el árbol de accesibilidad, los atributos de Aria que se aplican a un elemento y las propiedades de accesibilidad calculadas.</span><span class="sxs-lookup"><span data-stu-id="db890-248">Within the **Accessibility** pane there are controls for exploring the accessibility tree, the ARIA attributes applied to an element, and the computed accessibility properties.</span></span>  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### <span data-ttu-id="db890-249">Árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="db890-249">Accessibility Tree</span></span>   

<span data-ttu-id="db890-250">El **árbol de accesibilidad** se presenta como [Aria `tree` ][W3CWaiAriaTree] , donde cada uno `treeitem` corresponde a un elemento en el Dom.</span><span class="sxs-lookup"><span data-stu-id="db890-250">The **Accessibility Tree** is presented as an [ARIA `tree`][W3CWaiAriaTree] where each `treeitem` corresponds to an element in the DOM.</span></span>  <span data-ttu-id="db890-251">El árbol anuncia el rol calculado para el nodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="db890-251">The tree announces the computed role for the selected node.</span></span>  <span data-ttu-id="db890-252">Elementos genéricos como `div` y `span` se anuncian como "GenericContainer" en el árbol.</span><span class="sxs-lookup"><span data-stu-id="db890-252">Generic elements like `div` and `span` are announced as "GenericContainer" in the tree.</span></span>  <span data-ttu-id="db890-253">Use las teclas de dirección para desplazarse por el árbol y explorar las relaciones de elementos primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="db890-253">Use the arrow keys to traverse the tree and explore parent-child relationships.</span></span>  

#### <span data-ttu-id="db890-254">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-254">Known issues</span></span>   

*   <span data-ttu-id="db890-255">Es posible que el tipo de [Aria `tree` ][W3CWaiAriaTree] usada por el panel de **accesibilidad** no se exponga correctamente en Microsoft Edge para lectores de pantalla de MacOS, como VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="db890-255">The type of [ARIA `tree`][W3CWaiAriaTree] used by the **Accessibility** pane may not be properly exposed in Microsoft Edge for macOS screen readers like VoiceOver.</span></span>  <span data-ttu-id="db890-256">Suscríbase al [problema de cromo #868480][ChromiumIssues868480] para estar informado sobre el progreso de este problema.</span><span class="sxs-lookup"><span data-stu-id="db890-256">Subscribe to [Chromium issue #868480][ChromiumIssues868480] to be informed about progress on this issue.</span></span>  
*   <span data-ttu-id="db890-257">Cada uno de los **atributos de Aria** y las secciones de **propiedades calculadas** se marcan como [ `tree` Aria ][W3CWaiAriaTree], pero en este momento no hay administración de foco y no es compatible con el teclado.</span><span class="sxs-lookup"><span data-stu-id="db890-257">Each of the **ARIA Attributes** and **Computed Properties** sections are marked up as an [ARIA `tree`][W3CWaiAriaTree], but each does not currently have focus management and is not keyboard operable.</span></span>  

## <span data-ttu-id="db890-258">Panel auditorías</span><span class="sxs-lookup"><span data-stu-id="db890-258">Audits panel</span></span>   

<span data-ttu-id="db890-259">El panel **Auditoría** debe ejecutar una serie de pruebas en un sitio para comprobar problemas comunes relacionados con el rendimiento, la accesibilidad, la SEO y un número de otras categorías.</span><span class="sxs-lookup"><span data-stu-id="db890-259">The **Audits** panel you should run a series of tests against a site to check for common issues related to performance, accessibility, SEO, and a number of other categories.</span></span>  

### <span data-ttu-id="db890-260">Configurar y ejecutar una auditoría</span><span class="sxs-lookup"><span data-stu-id="db890-260">Configure and run an audit</span></span>   

1.  <span data-ttu-id="db890-261">Cuando se abre por primera vez el panel **auditorías** , el foco se coloca en el botón **Ejecutar auditoría** al final del formulario.</span><span class="sxs-lookup"><span data-stu-id="db890-261">When the **Audits** panel is first opened, focus is placed on the **Run Audit** button at the end of the form.</span></span>  <span data-ttu-id="db890-262">De forma predeterminada, el formulario está configurado para ejecutar auditorías de todas las categorías con emulación móvil en una conexión 3G simulada.</span><span class="sxs-lookup"><span data-stu-id="db890-262">By default the form is configured to run audits for every category using mobile emulation on a simulated 3G connection.</span></span>  
1.  <span data-ttu-id="db890-263">Use `Shift` + `Tab` o desplácese hacia atrás en el modo de exploración para cambiar la configuración de auditoría.</span><span class="sxs-lookup"><span data-stu-id="db890-263">Use `Shift`+`Tab` or navigate back in Browse mode to change the audit settings.</span></span>  
1.  <span data-ttu-id="db890-264">Cuando esté listo para ejecutar la auditoría, vuelva al botón **Ejecutar auditoría** y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="db890-264">When you are ready to run the audit, navigate back to the **Run Audit** button and press `Enter`.</span></span>  
1.  <span data-ttu-id="db890-265">El foco se mueve a una ventana modal con un botón **Cancelar** que le permite salir de la auditoría.</span><span class="sxs-lookup"><span data-stu-id="db890-265">Focus moves into a modal window with a **Cancel** button which allows you to exit the audit.</span></span>  <span data-ttu-id="db890-266">Es posible que oiga una serie de earcons mientras se ejecuta la auditoría y se actualiza la página varias veces.</span><span class="sxs-lookup"><span data-stu-id="db890-266">You may hear a series of earcons as the audit runs and refreshes the page multiple times.</span></span>  

#### <span data-ttu-id="db890-267">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="db890-267">Known issues</span></span>   

*   <span data-ttu-id="db890-268">Las diferentes secciones del formulario de configuración no se marcan actualmente con un `fieldset` elemento.</span><span class="sxs-lookup"><span data-stu-id="db890-268">The different sections of the configuration form are not currently marked up with a `fieldset` element.</span></span>  <span data-ttu-id="db890-269">Puede ser más fácil encontrarlos en el modo de exploración para averiguar qué controles están asociados con cada sección.</span><span class="sxs-lookup"><span data-stu-id="db890-269">It may be easier to navigate them in Browse mode to figure out which controls are associated with each section.</span></span>  
*   <span data-ttu-id="db890-270">No hay ningún anuncio de Earcon ni de región en vivo cuando la auditoría termina de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="db890-270">There is no earcon or live region announcement when the audit is finished running.</span></span>  <span data-ttu-id="db890-271">Generalmente, tarda unos 30 segundos, después de los cuales debería poder navegar a los resultados.</span><span class="sxs-lookup"><span data-stu-id="db890-271">Generally it takes about 30 seconds, after which you should be able to navigate to the results.</span></span>  <span data-ttu-id="db890-272">Usar el modo de exploración puede ser la manera más fácil de alcanzar los resultados.</span><span class="sxs-lookup"><span data-stu-id="db890-272">Using Browse mode may be the easiest way to reach the results.</span></span>  

### <span data-ttu-id="db890-273">Navegar por el informe de auditoría</span><span class="sxs-lookup"><span data-stu-id="db890-273">Navigate the audit report</span></span>   

<span data-ttu-id="db890-274">El informe de auditoría se organiza en secciones que corresponden a cada una de las categorías de auditoría.</span><span class="sxs-lookup"><span data-stu-id="db890-274">The audit report is organized into sections that correspond with each of the audit categories.</span></span>  <span data-ttu-id="db890-275">El informe se abre con una lista de puntuaciones para cada categoría.</span><span class="sxs-lookup"><span data-stu-id="db890-275">The report opens with a list of scores for each category.</span></span>  <span data-ttu-id="db890-276">Estas puntuaciones también son vínculos que se pueden usar para saltar a las secciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="db890-276">These scores are also links which are able to be used to skip to the relevant sections.</span></span>  <span data-ttu-id="db890-277">Dentro de cada sección se incluyen `details` elementos expansibles, que contienen información relacionada con auditorías pasadas o fallidas.</span><span class="sxs-lookup"><span data-stu-id="db890-277">Within each section are expandable `details` elements, which contain information relating to passed or failed audits.</span></span>  <span data-ttu-id="db890-278">De forma predeterminada, solo se muestran las auditorías con errores.</span><span class="sxs-lookup"><span data-stu-id="db890-278">By default, only failing audits are shown.</span></span>  <span data-ttu-id="db890-279">Cada sección termina con un `details` elemento final que contiene todas las auditorías pasadas.</span><span class="sxs-lookup"><span data-stu-id="db890-279">Each section ends with a final `details` element which contains all of the passed audits.</span></span>  

<span data-ttu-id="db890-280">Para ejecutar una nueva auditoría, use `Shift` + `Tab` para salir del informe y busque el botón **realizar una auditoría** .</span><span class="sxs-lookup"><span data-stu-id="db890-280">To run a new audit, use `Shift`+`Tab` to exit the report and look for the **Perform An Audit** button.</span></span>  

## <span data-ttu-id="db890-281">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db890-281">Feedback</span></span>   

*   <span data-ttu-id="db890-282">Envíe informes de errores de DevTools o solicitudes de características a [rastreador de problemas de cromo][MonorailChromiumIssues].</span><span class="sxs-lookup"><span data-stu-id="db890-282">Send DevTools bug reports or feature requests to [Chromium Issue Tracker][MonorailChromiumIssues].</span></span>  
*   <span data-ttu-id="db890-283">Enviar comentarios relacionados con este documento a [GitHub][GithubEdgeDeveloperNewIssue].</span><span class="sxs-lookup"><span data-stu-id="db890-283">Send any feedback related to this document to [GitHub][GithubEdgeDeveloperNewIssue].</span></span>  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-menu/index.MD "ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevtoolsConsoleIndex]: .. /Console/index.MD "Descripción general de la consola"  
[DevtoolsCssIndex]: .. /CSS/index.MD "Introducción a la visualización y el cambio de CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /open.md "abrir Microsoft Edge DevTools"  
[DevtoolsShortcuts]: .. /shortcuts.md "métodos abreviados de teclado de Microsoft Edge DevTools"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # Styles-panel-teclado de accesos directos "métodos abreviados de teclado del panel de estilos-Microsoft Edge DevTools métodos abreviados de teclado"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problema 868480: exponer árboles de ARIA como tablas en la accesibilidad de Mac"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nuevo problema: MicrosoftDocs/Edge-Developer | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": activo | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Focus | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Problemas-cromo-monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "Tablist (función): aplicaciones de Internet enriquecidas accesibles (WAI-ARIA) 1,1 | RELATIVA"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "árbol (función): aplicaciones de Internet enriquecidas accesibles (WAI-ARIA) 1,1 | RELATIVA"  

> [!NOTE]
> <span data-ttu-id="db890-297">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db890-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="db890-298">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) y está creada por [Rob Dodson][RobDodson] \ (colaborador, Google webfundamentals \).</span><span class="sxs-lookup"><span data-stu-id="db890-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) and is authored by [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="db890-300">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db890-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
