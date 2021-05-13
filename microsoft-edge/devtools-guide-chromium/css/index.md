---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para ver y cambiar el CSS de una página.
title: Introducción a cómo ver y cambiar CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bc629286530e709bef0e04a671f1a0e56eee48ea
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564451"
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
# <a name="get-started-with-viewing-and-changing-css"></a><span data-ttu-id="cdd8a-104">Introducción a cómo ver y cambiar CSS</span><span class="sxs-lookup"><span data-stu-id="cdd8a-104">Get started with viewing and changing CSS</span></span>  

<span data-ttu-id="cdd8a-105">Complete estos tutoriales interactivos para aprender los conceptos básicos de ver y cambiar el CSS de una página mediante Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <a name="open-css-examples"></a><span data-ttu-id="cdd8a-106">Ejemplos de CSS abiertos</span><span class="sxs-lookup"><span data-stu-id="cdd8a-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="cdd8a-107">Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija **Ejemplos de CSS** para abrirse en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="cdd8a-108">Ejemplos de CSS</span><span class="sxs-lookup"><span data-stu-id="cdd8a-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="cdd8a-109">Si desea acoplar la ventana [DevTools][DevToolsCustomizePlacement] a la derecha de la ventanilla \(se muestra en la siguiente figura\), elija Personalizar y **controlar DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), choose **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="cdd8a-110">En el **menú desplegable Personalizar y controlar DevTools,** en la sección Lado **dock,** elija **Acoplar a la derecha.**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose **Dock to right**.</span></span>  
    
## <a name="view-the-css-for-an-element"></a><span data-ttu-id="cdd8a-111">Ver el CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="cdd8a-112">[Abrir ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="cdd8a-113">Mantenga el mouse `Inspect Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="cdd8a-114">En DevTools, en la **herramienta Elementos,** en el panel Árbol **DOM,** se `Inspect Me!` resalta el elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-114">In DevTools, on the **Elements** tool, in the **DOM Tree** panel, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="El elemento inspeccionado se resalta en el árbol DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="cdd8a-116">El elemento inspeccionado se resalta en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-116">The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="cdd8a-117">En el `Inspect Me!` elemento, busque el valor del `data-message` atributo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="cdd8a-118">En la página, en el **cuadro de texto Valor de `data-message` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="cdd8a-119">Mantenga el mouse `Inspect Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="cdd8a-120">En DevTools, en la **herramienta Elementos,** seleccione el panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-120">In DevTools, on the **Elements** tool, select the **Styles** panel.</span></span>  
    1.  <span data-ttu-id="cdd8a-121">En el panel **Estilos,** el `Inspect Me!` elemento está resaltado.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-121">In the **Styles** panel, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="cdd8a-122">En el `Inspect Me!` elemento, busque la regla `aloha` de clase.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="cdd8a-123">Esta regla se muestra, ya que se está aplicando al `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-123">This rule is displayed, because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="cdd8a-124">En la `aloha` clase, busque el valor del `padding` estilo y cópielo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Las clases CSS se aplican al elemento inspeccionado y se resaltan en el panel Estilos" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="cdd8a-126">Las clases CSS se aplican al elemento seleccionado, como , se muestran `aloha` en el panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-126">CSS classes is applied to the selected element, such as `aloha`, are displayed in the **Styles** panel</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="cdd8a-127">En la página, en el **cuadro de texto Valor de `padding` :** , escriba el valor.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="cdd8a-128">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="cdd8a-129">Use el panel **Estilos** cuando desee cambiar o agregar declaraciones CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-129">Use the **Styles** panel when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="cdd8a-130">Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="cdd8a-131">[Abrir ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="cdd8a-132">Mantenga el mouse `Add A Background Color To Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="cdd8a-133">Elija `element.style` cerca de la parte superior del panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-133">Choose `element.style` near the top of the **Styles** panel.</span></span>  
1.  <span data-ttu-id="cdd8a-134">Escriba `background-color` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-134">Type `background-color` and select `Enter`.</span></span>  
1.  <span data-ttu-id="cdd8a-135">Escriba `honeydew` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-135">Type `honeydew` and select `Enter`.</span></span>  <span data-ttu-id="cdd8a-136">En el **árbol DOM,** se muestra una declaración de estilo en línea aplicada al elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-136">In the **DOM Tree**, an inline style declaration applied to the element is displayed.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Agregar una declaración CSS al elemento mediante el panel Estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="cdd8a-138">La `background-color:honeydew` declaración se aplica al elemento mediante la sección del panel `element.style` **Estilos**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-138">The `background-color:honeydew` declaration is applied to the element using the `element.style` section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a><span data-ttu-id="cdd8a-139">Agregar una clase CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="cdd8a-140">Para mostrar el aspecto de un elemento cuando se aplica o quita una clase CSS de un elemento, vaya al panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-140">To display how an element looks when a CSS class is applied to or removed from an element, navigate to the **Styles** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="cdd8a-141">Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="cdd8a-142">[Abrir ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="cdd8a-143">Mantenga el mouse `Add A Class To Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="cdd8a-144">Elija **.cls**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-144">Choose **.cls**.</span></span>  <span data-ttu-id="cdd8a-145">DevTools muestra un cuadro de texto donde puede agregar clases al elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="cdd8a-146">Escriba `color_me` en el cuadro de texto Agregar nueva **clase** y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-146">Type `color_me` in the **Add new class** text box and then select `Enter`.</span></span>  <span data-ttu-id="cdd8a-147">Aparece una casilla debajo del cuadro de texto **Agregar** nueva clase, donde puede activar y desactivar la clase.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="cdd8a-148">Si el elemento tiene otras clases aplicadas, también puedes alternar cada `Add A Class To Me!` una desde aquí.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar la clase color_me al elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="cdd8a-150">La `color_me` clase se aplica al elemento mediante la sección **.cls** del panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-150">The `color_me` class is applied to the element using the **.cls** section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a><span data-ttu-id="cdd8a-151">Agregar un pseudoestado a una clase</span><span class="sxs-lookup"><span data-stu-id="cdd8a-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="cdd8a-152">Use el panel **Estilos** para aplicar permanentemente un pseudoestado CSS a un elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-152">Use the **Styles** panel to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="cdd8a-153">DevTools admite `:active` , `:focus` , y `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="cdd8a-154">Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="cdd8a-155">[Abrir ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="cdd8a-156">Mantenga el mouse sobre el `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-156">Hover on the `Hover Over Me!` text.</span></span>  <span data-ttu-id="cdd8a-157">Cambia el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-157">The background color changes.</span></span>  
1.  <span data-ttu-id="cdd8a-158">Mantenga el mouse `Hover Over Me!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="cdd8a-159">En el panel **Estilos,** elija **:hov**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-159">In the **Styles** panel, choose **:hov**.</span></span>  
1.  <span data-ttu-id="cdd8a-160">Active la **casilla :hover.**</span><span class="sxs-lookup"><span data-stu-id="cdd8a-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="cdd8a-161">El color de fondo cambia como antes, aunque no se mantenga el mouse sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar la pseudoestación activa en un elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="cdd8a-163">Alternar el `:hover` pseudostate en un elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-163">Toggle the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a><span data-ttu-id="cdd8a-164">Cambiar las dimensiones de un elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="cdd8a-165">Use el **diagrama interactivo Modelo** de cuadro en el panel **Estilos** para cambiar el ancho, alto, relleno, margen o longitud de borde de un elemento.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-165">Use the **Box Model** interactive diagram in the **Styles** panel to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="cdd8a-166">Complete el [tutorial Ver el CSS de un elemento](#view-the-css-for-an-element) antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="cdd8a-167">[Abrir ejemplos de CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="cdd8a-168">Mantenga el mouse `Change My Margin!` sobre el texto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="cdd8a-169">En el **diagrama Modelo de** cuadro del panel **Estilos,** mantenga el mouse sobre **el relleno**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-169">In the **Box Model** diagram in the **Styles** panel, hover on **padding**.</span></span>  <span data-ttu-id="cdd8a-170">El relleno de un elemento se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="cdd8a-171">Según el tamaño de la ventana DevTools, es posible que deba desplazarse hasta la parte inferior del panel **Estilos** para mostrar **el modelo de cuadro**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** panel to display the **Box Model**.</span></span>  

1.  <span data-ttu-id="cdd8a-172">Haga doble clic en el margen izquierdo del **Modelo**de cuadro , que actualmente tiene un valor que significa que el elemento `-` no tiene un margen izquierdo.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="cdd8a-173">Escriba `100px` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-173">Type `100px` and select `Enter`.</span></span>  <span data-ttu-id="cdd8a-174">El **modelo de** cuadro tiene el valor predeterminado de píxeles, pero también acepta otros valores, como , o `25%` `10vw` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Mantenga el mouse sobre el relleno del elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="cdd8a-176">Mantenga el mouse sobre el relleno del elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-176">Hover on the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Cambiar el margen izquierdo del elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="cdd8a-178">Cambiar el margen izquierdo del elemento</span><span class="sxs-lookup"><span data-stu-id="cdd8a-178">Change the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a><span data-ttu-id="cdd8a-179">Depuración de consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="cdd8a-179">Debugging Media Queries</span></span>  

<span data-ttu-id="cdd8a-180">[Las consultas multimedia][MDNUsingMediaGueries] son una forma de hacer que el producto web reaccione a los cambios en las opciones de configuración de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="cdd8a-181">El caso de uso más significativo es proporcionar al producto un diseño CSS diferente en función de las dimensiones de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="cdd8a-182">El uso de diseños independientes permite un diseño de una columna para dispositivos móviles y diseños de varias columnas cuando hay más estado de pantalla disponible.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="cdd8a-183">Si desea depurar o probar las consultas multimedia que definió en su CSS, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="cdd8a-184">Abra las herramientas de desarrollador y seleccione el icono **de** la barra de herramientas Alternar dispositivo en la parte superior izquierda o `Ctrl` + `Shift` + `M` seleccione \( `Cmd` + `Shift` + `M` en macOS\).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or select `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abrir la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="cdd8a-186">Abrir la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="cdd8a-186">Open the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cdd8a-187">Con la barra de herramientas del dispositivo abierta, seleccione el menú de la parte superior derecha y `...` elija Ver consultas **multimedia**.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-187">With the device toolbar open, select the `...` menu on the top-right and choose **View Media Queries**.</span></span>  <span data-ttu-id="cdd8a-188">Las barras de colores que se muestran encima de la página web representan las distintas consultas multimedia.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-188">The colored bars displayed above the webpage represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar consultas multimedia en la barra de herramientas del dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="cdd8a-190">Mostrar consultas multimedia en la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="cdd8a-190">Show Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cdd8a-191">Mantenga el mouse sobre los límites de las barras para mostrar los valores de las distintas consultas multimedia.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-191">Hover on the boundaries in the bars to display the values of the different media queries.</span></span>  <span data-ttu-id="cdd8a-192">Elija cada una para cambiar el tamaño de la página web que desea que coincida.</span><span class="sxs-lookup"><span data-stu-id="cdd8a-192">Choose each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Elegir consulta multimedia en la barra de vista previa" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="cdd8a-194">Elegir consulta multimedia en la barra de vista previa</span><span class="sxs-lookup"><span data-stu-id="cdd8a-194">Choose Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cdd8a-195">Para depurar consultas multimedia y abrir el archivo CSS en el editor; mantenga el mouse en cualquiera de los segmentos de barra, abra el menú contextual \(hacer clic con el botón `Sources` secundario\) y seleccione `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="cdd8a-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Mostrar consultas multimedia en el Editor de orígenes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="cdd8a-197">Mostrar consultas multimedia en el Editor de orígenes</span><span class="sxs-lookup"><span data-stu-id="cdd8a-197">Reveal Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="cdd8a-198">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cdd8a-198">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar Microsoft Edge ubicación de DevTools (desacoplar, acoplar a abajo, acoplar a la izquierda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Ejemplos de CSS: Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Uso de consultas multimedia | MDN"  

> [!NOTE]
> <span data-ttu-id="cdd8a-202">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cdd8a-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cdd8a-203">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="cdd8a-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cdd8a-205">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cdd8a-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
