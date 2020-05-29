---
title: Introducción a la visualización y el cambio de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601820"
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





# <span data-ttu-id="15cf6-103">Introducción a la visualización y el cambio de CSS</span><span class="sxs-lookup"><span data-stu-id="15cf6-103">Get Started With Viewing And Changing CSS</span></span>   



<span data-ttu-id="15cf6-104">Complete estos tutoriales interactivos para conocer los conceptos básicos de la visualización y el cambio de las CSS de una página con Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="15cf6-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="15cf6-105">Ejemplos de CSS abiertos</span><span class="sxs-lookup"><span data-stu-id="15cf6-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="15cf6-106">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplos de CSS** para abrir en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="15cf6-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="15cf6-107">Ejemplos de CSS</span><span class="sxs-lookup"><span data-stu-id="15cf6-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  

> [!NOTE]
> <span data-ttu-id="15cf6-108">Si desea [acoplar la ventana de DevTools][DevToolsCustomizePlacement] a la derecha de la ventanilla \ (que se muestra en la [figura 1](#figure-1)\), haga clic en **personalizar y controlar DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in [Figure 1](#figure-1)\), click **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="15cf6-109">En el menú desplegable **personalizar y controlar DevTools** , en la sección de **acoplamiento** , seleccione **acoplar a la derecha**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="15cf6-110">Ver la CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-110">View the CSS for an element</span></span>   

1.  <span data-ttu-id="15cf6-111">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="15cf6-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="15cf6-112">Haga clic con el botón derecho en el `Inspect Me!` texto y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-112">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="15cf6-113">En DevTools, en el panel **elementos** , en la pestaña **árbol DOM** , `Inspect Me!` se resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        > ##### <span data-ttu-id="15cf6-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="15cf6-114">Figure 1</span></span>  
        > <span data-ttu-id="15cf6-115">El elemento inspeccionado está resaltado en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="15cf6-115">The inspected element is highlighted in the **DOM Tree**</span></span>  
        > ![El elemento inspeccionado está resaltado en el árbol DOM][ImageInspect]  
        
    1.  <span data-ttu-id="15cf6-117">En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="15cf6-118">En la página, en el cuadro **de texto valor de `data-message` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="15cf6-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="15cf6-119">Haga clic con el botón derecho en el `Inspect Me!` texto y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-119">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    
    1.  <span data-ttu-id="15cf6-120">En DevTools, en el panel **elementos** , seleccione la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="15cf6-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="15cf6-121">En la pestaña **estilos** , `Inspect Me!` se resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="15cf6-122">En el `Inspect Me!` elemento, busque la `aloha` regla de clase.</span><span class="sxs-lookup"><span data-stu-id="15cf6-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="15cf6-123">Verá esta regla porque se está aplicando al `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="15cf6-124">En la `aloha` clase, busque el valor del `padding` estilo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        > ##### <span data-ttu-id="15cf6-125">Figura 2</span><span class="sxs-lookup"><span data-stu-id="15cf6-125">Figure 2</span></span>  
        > <span data-ttu-id="15cf6-126">Las clases CSS que se aplican al elemento seleccionado, como `aloha` , se muestran en la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="15cf6-126">CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        > ![Las clases CSS que se aplican al elemento inspeccionado se resaltan en la pestaña estilos.][ImageAloha]  
        
1.  <span data-ttu-id="15cf6-128">En la página, en el cuadro **de texto valor de `padding` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="15cf6-128">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="15cf6-129">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-129">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="15cf6-130">Use la pestaña **estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-130">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="15cf6-131">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-131">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="15cf6-132">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="15cf6-132">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="15cf6-133">Haga clic con el botón derecho en el `Add A Background Color To Me!` texto y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-133">Right-click the `Add A Background Color To Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="15cf6-134">Haga clic `element.style` cerca de la parte superior de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="15cf6-134">Click `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="15cf6-135">Escriba `background-color` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-135">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="15cf6-136">Escriba `honeydew` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-136">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="15cf6-137">En el **árbol DOM** , debería ver que se aplicó una declaración de estilo en línea al elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-137">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  

> ##### <span data-ttu-id="15cf6-138">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="15cf6-138">Figure 3</span></span>  
> <span data-ttu-id="15cf6-139">La `background-color:honeydew` declaración se ha aplicado al elemento mediante la `element.style` sección de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="15cf6-139">The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
> ![Agregar una declaración CSS al elemento mediante la pestaña estilos][ImageDeclaration]  

## <span data-ttu-id="15cf6-141">Agregar una clase CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-141">Add a CSS class to an element</span></span>   

<span data-ttu-id="15cf6-142">Use la pestaña **estilos** para ver el aspecto que tiene un elemento cuando se aplica o se quita una clase CSS de un elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-142">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="15cf6-143">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-143">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="15cf6-144">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="15cf6-144">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="15cf6-145">Haga clic con el botón derecho en el `Add A Class To Me!` elemento y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-145">Right-click the `Add A Class To Me!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="15cf6-146">Haga clic en **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-146">Click **.cls**.</span></span>  <span data-ttu-id="15cf6-147">DevTools revela un cuadro de texto en el que puede Agregar clases al elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="15cf6-147">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="15cf6-148">Escriba `color_me` el cuadro de texto **Agregar nueva clase** y, después, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-148">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="15cf6-149">Aparece una casilla debajo del cuadro de texto **Agregar nueva clase** , donde puede activar o desactivar la clase.</span><span class="sxs-lookup"><span data-stu-id="15cf6-149">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="15cf6-150">Si el `Add A Class To Me!` elemento tiene otras clases aplicadas, también podrá alternar entre aquí.</span><span class="sxs-lookup"><span data-stu-id="15cf6-150">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  

> ##### <span data-ttu-id="15cf6-151">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="15cf6-151">Figure 4</span></span>  
> <span data-ttu-id="15cf6-152">La `color_me` clase se ha aplicado al elemento mediante la sección **. CLS** de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="15cf6-152">The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
> ![Aplicar la clase color_me al elemento][ImageApplyClass]  

## <span data-ttu-id="15cf6-154">Agregar un PseudoState a una clase</span><span class="sxs-lookup"><span data-stu-id="15cf6-154">Add a pseudostate to a class</span></span>   

<span data-ttu-id="15cf6-155">Use la pestaña **estilos** para aplicar de forma permanente un PseudoState CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-155">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="15cf6-156">DevTools es compatible con `:active` ,, `:focus` `:hover` , y `:visited` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-156">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="15cf6-157">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-157">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="15cf6-158">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="15cf6-158">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="15cf6-159">Desplace el puntero sobre el `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="15cf6-159">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="15cf6-160">Cambia el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-160">The background color changes.</span></span>  
1.  <span data-ttu-id="15cf6-161">Haga clic con el botón derecho en el `Hover Over Me!` texto y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-161">Right-click the `Hover Over Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="15cf6-162">En la pestaña **estilos** , haga clic en **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-162">In the **Styles** tab, click **:hov**.</span></span>  
1.  <span data-ttu-id="15cf6-163">Active la casilla **: hover** .</span><span class="sxs-lookup"><span data-stu-id="15cf6-163">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="15cf6-164">El color de fondo cambia como antes, aunque no esté colocando el puntero sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-164">The background color changes like before, even though you are not actually hovering over the element.</span></span>  

> ##### <span data-ttu-id="15cf6-165">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="15cf6-165">Figure 5</span></span>  
> <span data-ttu-id="15cf6-166">Alternar el `:hover` PseudoState en un elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-166">Toggling the `:hover` pseudostate on an element</span></span>  
> ![Alternar el PseudoState hover en un elemento][ImageSetHover]  

## <span data-ttu-id="15cf6-168">Cambiar las dimensiones de un elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-168">Change the dimensions of an element</span></span>   

<span data-ttu-id="15cf6-169">Use el Diagrama interactivo del **modelo de cuadro** de la pestaña **estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.</span><span class="sxs-lookup"><span data-stu-id="15cf6-169">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="15cf6-170">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-170">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="15cf6-171">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="15cf6-171">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="15cf6-172">Haga clic con el botón derecho en el `Change My Margin!` elemento y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-172">Right-click the `Change My Margin!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="15cf6-173">En el diagrama de **modelo de cuadro** de la pestaña **estilos** , desplace el puntero sobre el **relleno**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-173">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="15cf6-174">El relleno de un elemento se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="15cf6-174">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="15cf6-175">Según el tamaño de la ventana de DevTools, es posible que tenga que desplazarse hasta la parte inferior de la pestaña **estilos** para ver el **modelo de cuadro**.</span><span class="sxs-lookup"><span data-stu-id="15cf6-175">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="15cf6-176">Haga doble clic en el margen izquierdo del **modelo de cuadro**, que tiene actualmente el valor de `-` significado que el elemento no tiene un margen izquierdo.</span><span class="sxs-lookup"><span data-stu-id="15cf6-176">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="15cf6-177">Escriba `100px` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-177">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="15cf6-178">El **modelo de cuadro** tiene un valor predeterminado de píxeles, pero también acepta otros valores, como `25%` , o `10vw` .</span><span class="sxs-lookup"><span data-stu-id="15cf6-178">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  

> ##### <span data-ttu-id="15cf6-179">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="15cf6-179">Figure 6</span></span>  
> <span data-ttu-id="15cf6-180">Mantener el mouse sobre el relleno del elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-180">Hovering over the padding of the element</span></span>  
> ![Mantener el mouse sobre el relleno del elemento][ImageShowPadding]  

> ##### <span data-ttu-id="15cf6-182">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="15cf6-182">Figure 7</span></span>  
> <span data-ttu-id="15cf6-183">Cambiar el margen izquierdo del elemento</span><span class="sxs-lookup"><span data-stu-id="15cf6-183">Changing the left-margin of the element</span></span>  
> ![Cambiar el margen izquierdo del elemento][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Ilustración 1: el elemento inspeccionado está resaltado en el árbol DOM"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Ilustración 2: las clases CSS que se están aplicando al elemento inspeccionado se resaltan en la pestaña estilos."  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Ilustración 3: agregar una declaración CSS al elemento mediante la pestaña estilos"  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Ilustración 4: aplicar la clase color_me al elemento"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Ilustración 5: alternar el PseudoState hover en un elemento"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Ilustración 6: mantener el mouse sobre el relleno del elemento"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Ilustración 7: cambiar el margen izquierdo del elemento"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (cromo) DevTools | Intento"  

> [!NOTE]
> <span data-ttu-id="15cf6-194">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15cf6-194">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="15cf6-195">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="15cf6-195">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="15cf6-197">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15cf6-197">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
