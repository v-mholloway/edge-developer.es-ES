---
title: Introducción a cómo ver y cambiar CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 346145a7deb9e8ac951ed0578a5060da72817463
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710388"
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

# <span data-ttu-id="3edc4-103">Introducción a cómo ver y cambiar CSS</span><span class="sxs-lookup"><span data-stu-id="3edc4-103">Get Started With Viewing And Changing CSS</span></span>  

<span data-ttu-id="3edc4-104">Complete estos tutoriales interactivos para conocer los conceptos básicos de la visualización y el cambio de las CSS de una página con Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3edc4-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="3edc4-105">Ejemplos de CSS abiertos</span><span class="sxs-lookup"><span data-stu-id="3edc4-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="3edc4-106">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y seleccione **ejemplos de CSS** para abrir en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="3edc4-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and select **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="3edc4-107">Ejemplos de CSS</span><span class="sxs-lookup"><span data-stu-id="3edc4-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="3edc4-108">Si deseas [acoplar la ventana de DevTools][DevToolsCustomizePlacement] a la derecha de tu ventanilla \ (se muestra en la siguiente ilustración \), selecciona **personalizar y controla la DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), select **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="3edc4-109">En el menú desplegable **personalizar y controlar DevTools** , en la sección de **acoplamiento** , seleccione **acoplar a la derecha**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="3edc4-110">Ver la CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-110">View the CSS for an element</span></span>  

1.  <span data-ttu-id="3edc4-111">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="3edc4-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="3edc4-112">Desplace el puntero sobre el `Inspect Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-112">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3edc4-113">En DevTools, en el panel **elementos** , en la pestaña **árbol DOM** , `Inspect Me!` se resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="El elemento inspeccionado está resaltado en el árbol DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="3edc4-115">Ilustración 1: el elemento inspeccionado está resaltado en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="3edc4-115">Figure 1:  The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="3edc4-116">En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-116">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="3edc4-117">En la página, en el cuadro **de texto valor de `data-message` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="3edc4-117">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="3edc4-118">Desplace el puntero sobre el `Inspect Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-118">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3edc4-119">En DevTools, en el panel **elementos** , seleccione la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-119">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="3edc4-120">En la pestaña **estilos** , `Inspect Me!` se resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-120">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="3edc4-121">En el `Inspect Me!` elemento, busque la `aloha` regla de clase.</span><span class="sxs-lookup"><span data-stu-id="3edc4-121">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="3edc4-122">Verá esta regla porque se está aplicando al `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-122">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="3edc4-123">En la `aloha` clase, busque el valor del `padding` estilo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-123">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Las clases CSS que se aplican al elemento inspeccionado se resaltan en la pestaña estilos." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="3edc4-125">Ilustración 2: las clases CSS que se están aplicando al elemento seleccionado, como `aloha` , se muestran en la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-125">Figure 2:  CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="3edc4-126">En la página, en el cuadro **de texto valor de `padding` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="3edc4-126">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="3edc4-127">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-127">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="3edc4-128">Use la pestaña **estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-128">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="3edc4-129">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-129">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="3edc4-130">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="3edc4-130">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="3edc4-131">Desplace el puntero sobre el `Add A Background Color To Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-131">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="3edc4-132">Seleccione `element.style` cerca de la parte superior de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-132">Select `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="3edc4-133">Escriba `background-color` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-133">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="3edc4-134">Escriba `honeydew` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-134">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="3edc4-135">En el **árbol DOM** , debería ver que se aplicó una declaración de estilo en línea al elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-135">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Agregar una declaración CSS al elemento mediante la pestaña estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="3edc4-137">Ilustración 3: la `background-color:honeydew` declaración se ha aplicado al elemento mediante la `element.style` sección de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-137">Figure 3:  The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3edc4-138">Agregar una clase CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-138">Add a CSS class to an element</span></span>  

<span data-ttu-id="3edc4-139">Use la pestaña **estilos** para ver el aspecto que tiene un elemento cuando se aplica o se quita una clase CSS de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-139">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="3edc4-140">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-140">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="3edc4-141">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="3edc4-141">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="3edc4-142">Desplace el puntero sobre el `Add A Class To Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-142">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="3edc4-143">Seleccione **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-143">Select **.cls**.</span></span>  <span data-ttu-id="3edc4-144">DevTools revela un cuadro de texto en el que puede Agregar clases al elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3edc4-144">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="3edc4-145">Escriba `color_me` el cuadro de texto **Agregar nueva clase** y, después, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-145">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="3edc4-146">Aparece una casilla debajo del cuadro de texto **Agregar nueva clase** , donde puede activar o desactivar la clase.</span><span class="sxs-lookup"><span data-stu-id="3edc4-146">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="3edc4-147">Si el `Add A Class To Me!` elemento tiene otras clases aplicadas, también podrá alternar entre aquí.</span><span class="sxs-lookup"><span data-stu-id="3edc4-147">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar la clase color_me al elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="3edc4-149">Ilustración 4: se ha `color_me` aplicado la clase al elemento con la sección **. CLS** de la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-149">Figure 4:  The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3edc4-150">Agregar un PseudoState a una clase</span><span class="sxs-lookup"><span data-stu-id="3edc4-150">Add a pseudostate to a class</span></span>  

<span data-ttu-id="3edc4-151">Use la pestaña **estilos** para aplicar de forma permanente un PseudoState CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-151">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="3edc4-152">DevTools es compatible con `:active` ,, `:focus` `:hover` , y `:visited` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-152">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="3edc4-153">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-153">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="3edc4-154">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="3edc4-154">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="3edc4-155">Desplace el puntero sobre el `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="3edc4-155">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="3edc4-156">Cambia el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-156">The background color changes.</span></span>  
1.  <span data-ttu-id="3edc4-157">Desplace el puntero sobre el `Hover Over Me!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-157">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="3edc4-158">En la pestaña **estilos** , seleccione **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-158">In the **Styles** tab, select **:hov**.</span></span>  
1.  <span data-ttu-id="3edc4-159">Active la casilla **: hover** .</span><span class="sxs-lookup"><span data-stu-id="3edc4-159">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="3edc4-160">El color de fondo cambia como antes, aunque no esté colocando el puntero sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-160">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar el PseudoState hover en un elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="3edc4-162">Ilustración 5: alternar el `:hover` PseudoState en un elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-162">Figure 5:  Toggling the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3edc4-163">Cambiar las dimensiones de un elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-163">Change the dimensions of an element</span></span>  

<span data-ttu-id="3edc4-164">Use el Diagrama interactivo del **modelo de cuadro** de la pestaña **estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3edc4-164">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="3edc4-165">Complete el tutorial [ver la CSS para un elemento antes de](#view-the-css-for-an-element) hacerlo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-165">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="3edc4-166">[Abra ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="3edc4-166">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="3edc4-167">Desplace el puntero sobre el `Change My Margin!` texto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-167">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="3edc4-168">En el diagrama de **modelo de cuadro** de la pestaña **estilos** , desplace el puntero sobre el **relleno**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-168">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="3edc4-169">El relleno de un elemento se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="3edc4-169">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="3edc4-170">Según el tamaño de la ventana de DevTools, es posible que tenga que desplazarse hasta la parte inferior de la pestaña **estilos** para ver el **modelo de cuadro**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-170">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="3edc4-171">Haga doble clic en el margen izquierdo del **modelo de cuadro**, que tiene actualmente el valor de `-` significado que el elemento no tiene un margen izquierdo.</span><span class="sxs-lookup"><span data-stu-id="3edc4-171">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="3edc4-172">Escriba `100px` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-172">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="3edc4-173">El **modelo de cuadro** tiene un valor predeterminado de píxeles, pero también acepta otros valores, como `25%` , o `10vw` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-173">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Mantener el mouse sobre el relleno del elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="3edc4-175">Ilustración 6: mantener el mouse sobre el relleno del elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-175">Figure 6:  Hovering over the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Cambiar el margen izquierdo del elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="3edc4-177">Ilustración 7: cambiar el margen izquierdo del elemento</span><span class="sxs-lookup"><span data-stu-id="3edc4-177">Figure 7:  Changing the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="3edc4-178">Depurar consultas de medios</span><span class="sxs-lookup"><span data-stu-id="3edc4-178">Debugging Media Queries</span></span>  

<span data-ttu-id="3edc4-179">[Las consultas de medios][MDNUsingMediaGueries] son una forma de hacer que el producto Web reaccione ante los cambios en la configuración de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="3edc4-179">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="3edc4-180">El caso de uso más importante es proporcionar a tu producto un diseño CSS diferente según las dimensiones de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="3edc4-180">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="3edc4-181">El uso de diseños independientes permite un diseño de una columna para dispositivos móviles y diseños de varias columnas cuando hay más pantalla disponible.</span><span class="sxs-lookup"><span data-stu-id="3edc4-181">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="3edc4-182">Si desea depurar o probar las consultas de medios definidas en su CSS, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="3edc4-182">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="3edc4-183">Abra las herramientas de desarrollo y seleccione el icono de la **barra de herramientas del dispositivo de alternancia** en la parte superior izquierda o pulse `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` en MacOS \).</span><span class="sxs-lookup"><span data-stu-id="3edc4-183">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or press `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abrir la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="3edc4-185">Ilustración 8: abrir la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3edc4-185">Figure 8:  Opening the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3edc4-186">Con la barra de herramientas dispositivo abierta, seleccione el `...` menú en la parte superior derecha y, a continuación, seleccione **Ver consultas de medios**.</span><span class="sxs-lookup"><span data-stu-id="3edc4-186">With the device toolbar open, select the `...` menu on the top-right and select **View Media Queries**.</span></span>  <span data-ttu-id="3edc4-187">Debería ver barras de colores encima de la visualización de la página que representan las diferentes consultas de medios.</span><span class="sxs-lookup"><span data-stu-id="3edc4-187">You should see colored bars above the display of the page that represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar las consultas multimedia en la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="3edc4-189">Ilustración 9: mostrar las consultas multimedia en la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3edc4-189">Figure 9:  Showing Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3edc4-190">Mantenga el mouse sobre los límites de las barras para ver los valores de las diferentes consultas de medios.</span><span class="sxs-lookup"><span data-stu-id="3edc4-190">Hover over the boundaries in the bars to see the values of the different media queries.</span></span> <span data-ttu-id="3edc4-191">Seleccione cada una para cambiar el tamaño de la página web para que coincidan.</span><span class="sxs-lookup"><span data-stu-id="3edc4-191">Select each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Seleccionar una consulta multimedia desde la barra de vista previa" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="3edc4-193">Ilustración 10: seleccionar una consulta multimedia desde la barra de vista previa</span><span class="sxs-lookup"><span data-stu-id="3edc4-193">Figure 10:  Selecting Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3edc4-194">Para depurar consultas de elementos multimedia y abrir el archivo CSS en el `Sources` Editor; Coloque el puntero sobre cualquiera de los segmentos de la barra, abra el menú contextual \ (haga clic con el botón secundario del mouse \) y seleccione `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="3edc4-194">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Mostrar consultas de medios en el editor de orígenes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="3edc4-196">Ilustración 11: revelación de consultas de medios en el editor de orígenes</span><span class="sxs-lookup"><span data-stu-id="3edc4-196">Figure 11:  Revealing Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (cromo) DevTools | Intento"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usar consultas multimedia | MDN"  

> [!NOTE]
> <span data-ttu-id="3edc4-200">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3edc4-200">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3edc4-201">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3edc4-201">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3edc4-203">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3edc4-203">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
