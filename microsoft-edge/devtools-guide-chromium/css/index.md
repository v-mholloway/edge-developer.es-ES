---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para ver y cambiar las CSS de una página.
title: Introducción a cómo ver y cambiar CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f055606ff6140652341627097e7fe7b270dc929c
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993068"
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

# <span data-ttu-id="7d094-104">Introducción a cómo ver y cambiar CSS</span><span class="sxs-lookup"><span data-stu-id="7d094-104">Get Started With Viewing And Changing CSS</span></span>  

<span data-ttu-id="7d094-105">Complete estos tutoriales interactivos para conocer los conceptos básicos de la visualización y el cambio de las CSS de una página con Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d094-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="7d094-106">Ejemplos de CSS abiertos</span><span class="sxs-lookup"><span data-stu-id="7d094-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="7d094-107">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y seleccione **ejemplos de CSS** para abrir en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="7d094-107">Hold `Control` \(Windows\) or `Command` \(macOS\) and select **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="7d094-108">Ejemplos de CSS</span><span class="sxs-lookup"><span data-stu-id="7d094-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="7d094-109">Si deseas [acoplar la ventana de DevTools][DevToolsCustomizePlacement] a la derecha de tu ventanilla \ (se muestra en la siguiente ilustración \), selecciona **personalizar y controla la DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="7d094-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), select **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="7d094-110">En el menú desplegable **personalizar y controlar DevTools** , en la sección de **acoplamiento** , seleccione **acoplar a la derecha**.</span><span class="sxs-lookup"><span data-stu-id="7d094-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="7d094-111">Ver la CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="7d094-112">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7d094-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7d094-113">Desplace el puntero sobre el `Inspect Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7d094-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7d094-114">En DevTools, en el panel **elementos** , en la pestaña **árbol DOM** , `Inspect Me!` se resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-114">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="El elemento inspeccionado está resaltado en el árbol DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="7d094-116">Ilustración 1: el elemento inspeccionado está resaltado en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="7d094-116">Figure 1:  The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="7d094-117">En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="7d094-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="7d094-118">En la página, en el cuadro **de texto valor de `data-message` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="7d094-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="7d094-119">Desplace el puntero sobre el `Inspect Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7d094-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7d094-120">En DevTools, en el panel **elementos** , seleccione la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="7d094-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="7d094-121">En la pestaña **estilos** , `Inspect Me!` se resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="7d094-122">En el `Inspect Me!` elemento, busque la `aloha` regla de clase.</span><span class="sxs-lookup"><span data-stu-id="7d094-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="7d094-123">Verá esta regla porque se está aplicando al `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="7d094-124">En la `aloha` clase, busque el valor del `padding` estilo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="7d094-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Las clases CSS que se aplican al elemento inspeccionado se resaltan en la pestaña estilos." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="7d094-126">Ilustración 2: las clases CSS que se están aplicando al elemento seleccionado, como `aloha` , se muestran en la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="7d094-126">Figure 2:  CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="7d094-127">En la página, en el cuadro **de texto valor de `padding` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="7d094-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="7d094-128">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="7d094-129">Use la pestaña **estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-129">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d094-130">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="7d094-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7d094-131">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7d094-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7d094-132">Desplace el puntero sobre el `Add A Background Color To Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7d094-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7d094-133">Seleccione `element.style` cerca de la parte superior de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="7d094-133">Select `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="7d094-134">Escriba `background-color` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7d094-134">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="7d094-135">Escriba `honeydew` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7d094-135">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="7d094-136">En el **árbol DOM** , debería ver que se aplicó una declaración de estilo en línea al elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-136">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Agregar una declaración CSS al elemento mediante la pestaña estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="7d094-138">Ilustración 3: la `background-color:honeydew` declaración se ha aplicado al elemento mediante la `element.style` sección de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="7d094-138">Figure 3:  The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7d094-139">Agregar una clase CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="7d094-140">Use la pestaña **estilos** para ver el aspecto que tiene un elemento cuando se aplica o se quita una clase CSS de un elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-140">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d094-141">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="7d094-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7d094-142">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7d094-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7d094-143">Desplace el puntero sobre el `Add A Class To Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7d094-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7d094-144">Seleccione **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="7d094-144">Select **.cls**.</span></span>  <span data-ttu-id="7d094-145">DevTools revela un cuadro de texto en el que puede Agregar clases al elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7d094-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="7d094-146">Escriba `color_me` el cuadro de texto **Agregar nueva clase** y, después, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7d094-146">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="7d094-147">Aparece una casilla debajo del cuadro de texto **Agregar nueva clase** , donde puede activar o desactivar la clase.</span><span class="sxs-lookup"><span data-stu-id="7d094-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="7d094-148">Si el `Add A Class To Me!` elemento tiene otras clases aplicadas, también podrá alternar entre aquí.</span><span class="sxs-lookup"><span data-stu-id="7d094-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar la clase color_me al elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="7d094-150">Ilustración 4: se ha `color_me` aplicado la clase al elemento con la sección **. CLS** de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="7d094-150">Figure 4:  The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7d094-151">Agregar un PseudoState a una clase</span><span class="sxs-lookup"><span data-stu-id="7d094-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="7d094-152">Use la pestaña **estilos** para aplicar de forma permanente un PseudoState CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-152">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="7d094-153">DevTools es compatible con `:active` ,, `:focus` `:hover` , y `:visited` .</span><span class="sxs-lookup"><span data-stu-id="7d094-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d094-154">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="7d094-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7d094-155">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7d094-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7d094-156">Desplace el puntero sobre el `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="7d094-156">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="7d094-157">Cambia el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="7d094-157">The background color changes.</span></span>  
1.  <span data-ttu-id="7d094-158">Desplace el puntero sobre el `Hover Over Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7d094-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7d094-159">En la pestaña **estilos** , seleccione **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="7d094-159">In the **Styles** tab, select **:hov**.</span></span>  
1.  <span data-ttu-id="7d094-160">Active la casilla **: hover** .</span><span class="sxs-lookup"><span data-stu-id="7d094-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="7d094-161">El color de fondo cambia como antes, aunque no esté colocando el puntero sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar el PseudoState hover en un elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="7d094-163">Ilustración 5: alternar el `:hover` PseudoState en un elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-163">Figure 5:  Toggling the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7d094-164">Cambiar las dimensiones de un elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="7d094-165">Use el Diagrama interactivo del **modelo de cuadro** de la pestaña **estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.</span><span class="sxs-lookup"><span data-stu-id="7d094-165">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d094-166">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="7d094-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7d094-167">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7d094-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7d094-168">Desplace el puntero sobre el `Change My Margin!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7d094-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7d094-169">En el diagrama de **modelo de cuadro** de la pestaña **estilos** , desplace el puntero sobre el **relleno**.</span><span class="sxs-lookup"><span data-stu-id="7d094-169">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="7d094-170">El relleno de un elemento se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="7d094-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="7d094-171">Según el tamaño de la ventana de DevTools, es posible que tenga que desplazarse hasta la parte inferior de la pestaña **estilos** para ver el **modelo de cuadro**.</span><span class="sxs-lookup"><span data-stu-id="7d094-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="7d094-172">Haga doble clic en el margen izquierdo del **modelo de cuadro**, que tiene actualmente el valor de `-` significado que el elemento no tiene un margen izquierdo.</span><span class="sxs-lookup"><span data-stu-id="7d094-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="7d094-173">Escriba `100px` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7d094-173">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="7d094-174">El **modelo de cuadro** tiene un valor predeterminado de píxeles, pero también acepta otros valores, como `25%` , o `10vw` .</span><span class="sxs-lookup"><span data-stu-id="7d094-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Mantener el mouse sobre el relleno del elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="7d094-176">Ilustración 6: mantener el mouse sobre el relleno del elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-176">Figure 6:  Hovering over the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Cambiar el margen izquierdo del elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="7d094-178">Ilustración 7: cambiar el margen izquierdo del elemento</span><span class="sxs-lookup"><span data-stu-id="7d094-178">Figure 7:  Changing the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="7d094-179">Depurar consultas de medios</span><span class="sxs-lookup"><span data-stu-id="7d094-179">Debugging Media Queries</span></span>  

<span data-ttu-id="7d094-180">[Las consultas de medios][MDNUsingMediaGueries] son una forma de hacer que el producto Web reaccione ante los cambios en la configuración de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="7d094-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="7d094-181">El caso de uso más importante es proporcionar a tu producto un diseño CSS diferente según las dimensiones de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="7d094-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="7d094-182">El uso de diseños independientes permite un diseño de una columna para dispositivos móviles y diseños de varias columnas cuando hay más pantalla disponible.</span><span class="sxs-lookup"><span data-stu-id="7d094-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="7d094-183">Si desea depurar o probar las consultas de medios definidas en su CSS, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7d094-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="7d094-184">Abra las herramientas de desarrollo y seleccione el icono de la **barra de herramientas del dispositivo de alternancia** en la parte superior izquierda o pulse `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` en MacOS \).</span><span class="sxs-lookup"><span data-stu-id="7d094-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or press `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abrir la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="7d094-186">Ilustración 8: abrir la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d094-186">Figure 8:  Opening the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7d094-187">Con la barra de herramientas dispositivo abierta, seleccione el `...` menú en la parte superior derecha y, a continuación, seleccione **Ver consultas de medios**.</span><span class="sxs-lookup"><span data-stu-id="7d094-187">With the device toolbar open, select the `...` menu on the top-right and select **View Media Queries**.</span></span>  <span data-ttu-id="7d094-188">Debería ver barras de colores encima de la visualización de la página que representan las diferentes consultas de medios.</span><span class="sxs-lookup"><span data-stu-id="7d094-188">You should see colored bars above the display of the page that represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar las consultas multimedia en la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="7d094-190">Ilustración 9: mostrar las consultas multimedia en la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d094-190">Figure 9:  Showing Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7d094-191">Mantenga el mouse sobre los límites de las barras para ver los valores de las diferentes consultas de medios.</span><span class="sxs-lookup"><span data-stu-id="7d094-191">Hover over the boundaries in the bars to see the values of the different media queries.</span></span> <span data-ttu-id="7d094-192">Seleccione cada una para cambiar el tamaño de la página web para que coincidan.</span><span class="sxs-lookup"><span data-stu-id="7d094-192">Select each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Seleccionar una consulta multimedia desde la barra de vista previa" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="7d094-194">Ilustración 10: seleccionar una consulta multimedia desde la barra de vista previa</span><span class="sxs-lookup"><span data-stu-id="7d094-194">Figure 10:  Selecting Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7d094-195">Para depurar consultas de elementos multimedia y abrir el archivo CSS en el `Sources` Editor; Coloque el puntero sobre cualquiera de los segmentos de la barra, abra el menú contextual \ (haga clic con el botón secundario del mouse \) y seleccione `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="7d094-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Mostrar consultas de medios en el editor de orígenes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="7d094-197">Ilustración 11: revelación de consultas de medios en el editor de orígenes</span><span class="sxs-lookup"><span data-stu-id="7d094-197">Figure 11:  Revealing Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (cromo) DevTools | Intento"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usar consultas multimedia | MDN"  

> [!NOTE]
> <span data-ttu-id="7d094-201">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7d094-201">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7d094-202">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7d094-202">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7d094-204">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7d094-204">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
