---
title: 'DevTools para principiantes: Introducción a CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6e005f4107764a13934f0c8f3b3cde0ab9bf98c2
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931822"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="e0a28-103">DevTools para principiantes: Introducción a CSS</span><span class="sxs-lookup"><span data-stu-id="e0a28-103">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="e0a28-104">En este tutorial, aprenderá a usar CSS para aplicar un estilo a una página web.</span><span class="sxs-lookup"><span data-stu-id="e0a28-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="e0a28-105">También aprenderá a usar Microsoft Edge DevTools para experimentar con cambios de CSS.</span><span class="sxs-lookup"><span data-stu-id="e0a28-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="e0a28-106">El siguiente artículo es el segundo tutorial de una serie de tutoriales que le enseñan los conceptos básicos del desarrollo web y Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0a28-106">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="e0a28-107">Ganas experiencia práctica creando tu propio sitio Web.</span><span class="sxs-lookup"><span data-stu-id="e0a28-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="e0a28-108">No es necesario completar el primer tutorial antes de seguir con el segundo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-108">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="e0a28-109">[Configurar el código](#set-up-your-code) le muestra cómo realizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="e0a28-109">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="e0a28-110">Este tutorial está diseñado para principiantes y se centra en los **conceptos básicos del desarrollo web** y en los conceptos básicos del uso de DevTools para experimentar con CSS.</span><span class="sxs-lookup"><span data-stu-id="e0a28-110">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="e0a28-111">Si desea un tutorial que solo se Centre en DevTools, consulte Introducción [a la visualización y el cambio de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="e0a28-111">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="e0a28-112">Al principio del tutorial, el sitio debe tener un aspecto similar al de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="e0a28-112">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="e0a28-114">El aspecto de tu sitio en este momento</span><span class="sxs-lookup"><span data-stu-id="e0a28-114">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="e0a28-115">Después de completar el tutorial, el sitio debe tener una apariencia similar a la de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="e0a28-115">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Aspecto del sitio al final del tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="e0a28-117">Aspecto del sitio al final del tutorial</span><span class="sxs-lookup"><span data-stu-id="e0a28-117">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="e0a28-118">Principales</span><span class="sxs-lookup"><span data-stu-id="e0a28-118">Goals</span></span>  

<span data-ttu-id="e0a28-119">Siga este tutorial para comprender mejor los conceptos y las tareas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e0a28-119">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="e0a28-120">Cómo usar CSS para aplicar un estilo a una página web.</span><span class="sxs-lookup"><span data-stu-id="e0a28-120">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="e0a28-121">Cómo usar Microsoft Edge DevTools para experimentar con CSS.</span><span class="sxs-lookup"><span data-stu-id="e0a28-121">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="e0a28-122">La diferencia entre los marcos CSS y CSS.</span><span class="sxs-lookup"><span data-stu-id="e0a28-122">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="e0a28-123">Estás creando un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="e0a28-123">You are building a real website.</span></span>  

## <span data-ttu-id="e0a28-124">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e0a28-124">Prerequisites</span></span>  

<span data-ttu-id="e0a28-125">Antes de intentar este tutorial, complete los siguientes requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="e0a28-125">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="e0a28-126">Complete Introducción [a HTML y el Dom][DevtoolsBeginnersHtml] , o asegúrese de que tiene conocimientos de HTML y Dom parecidos a los impartidos en ese tutorial.</span><span class="sxs-lookup"><span data-stu-id="e0a28-126">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="e0a28-127">Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="e0a28-127">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="e0a28-128">El siguiente tutorial usa un conjunto de herramientas de desarrollo web, llamadas Microsoft Edge DevTools, que están integradas en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e0a28-128">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="e0a28-129">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="e0a28-129">Set up your code</span></span>  

<span data-ttu-id="e0a28-130">Para crear su sitio, primero debe completar las siguientes acciones para configurar su código.</span><span class="sxs-lookup"><span data-stu-id="e0a28-130">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="e0a28-131">Si ya ha completado el primer tutorial de la serie, vaya a la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0a28-131">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="e0a28-132">Continúa usando el código del último tutorial, [Introducción a HTML y el Dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="e0a28-132">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="e0a28-133">Abra el [código fuente][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="e0a28-133">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="e0a28-134">Se hace referencia a la pestaña de foco del explorador como la **pestaña edición**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-134">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="La ficha edición" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="e0a28-136">La ficha **edición**</span><span class="sxs-lookup"><span data-stu-id="e0a28-136">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-137">Seleccione **cocido-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-137">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="e0a28-138">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="e0a28-138">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="El menú opciones del proyecto" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="e0a28-140">El menú opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="e0a28-140">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="e0a28-141">Elija **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-141">Choose **Remix Project**.</span></span>  <span data-ttu-id="e0a28-142">Problema crea una copia del proyecto que se puede editar.</span><span class="sxs-lookup"><span data-stu-id="e0a28-142">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e0a28-143">El problema genera un nombre aleatorio para el nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="e0a28-143">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="e0a28-144">Elija **Mostrar** y seleccione **en una ventana nueva**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-144">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="e0a28-145">Se abre otra pestaña con una vista en vivo de su sitio.</span><span class="sxs-lookup"><span data-stu-id="e0a28-145">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="e0a28-146">Se hace referencia a la pestaña en el foco del explorador como la **pestaña en vivo**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-146">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="La ficha en vivo" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="e0a28-148">La **ficha en vivo**</span><span class="sxs-lookup"><span data-stu-id="e0a28-148">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="e0a28-149">Comprender CSS</span><span class="sxs-lookup"><span data-stu-id="e0a28-149">Understand CSS</span></span>  

<span data-ttu-id="e0a28-150">**CSS** es un lenguaje de equipos que determina el diseño y el estilo de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="e0a28-150">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="e0a28-151">La siguiente ilustración es un párrafo con borde.</span><span class="sxs-lookup"><span data-stu-id="e0a28-151">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="El texto se ha aplicado con estilo CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="e0a28-153">El texto se ha aplicado con estilo CSS</span><span class="sxs-lookup"><span data-stu-id="e0a28-153">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="e0a28-154">El siguiente fragmento de código es el código HTML y CSS utilizado para crear el párrafo en la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="e0a28-154">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="e0a28-155">probablemente te parezcan.</span><span class="sxs-lookup"><span data-stu-id="e0a28-155">probably looks new to you.</span></span>  <span data-ttu-id="e0a28-156">El resto debería ser familiar.</span><span class="sxs-lookup"><span data-stu-id="e0a28-156">The rest should look familiar.</span></span>  <span data-ttu-id="e0a28-157">Si no es así, complete Introducción [a HTML y al Dom][DevtoolsBeginnersHtml] antes de intentar las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="e0a28-157">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="e0a28-158">Agregar estilos en línea</span><span class="sxs-lookup"><span data-stu-id="e0a28-158">Add inline styles</span></span>  

<span data-ttu-id="e0a28-159">Complete las siguientes acciones para usar **estilos alineados** para aplicar estilos a un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="e0a28-159">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="e0a28-160">Vuelva a la pestaña edición y Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-160">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="e0a28-162">Abrir `index.html` en la pestaña edición</span><span class="sxs-lookup"><span data-stu-id="e0a28-162">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-163">Añadir `style="background-color: aliceblue;"` a tu `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-163">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="e0a28-164">En el bloque de código siguiente, la cuarta línea de código es la que tiene que cambiar.</span><span class="sxs-lookup"><span data-stu-id="e0a28-164">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="e0a28-165">El resto solo está allí, por lo que puedes asegurarte de poner el nuevo código en el lugar correcto.</span><span class="sxs-lookup"><span data-stu-id="e0a28-165">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="e0a28-166">Vaya a la **pestaña en vivo** para ver los cambios.</span><span class="sxs-lookup"><span data-stu-id="e0a28-166">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="e0a28-167">El fondo de la `<nav>` sección ahora es azul.</span><span class="sxs-lookup"><span data-stu-id="e0a28-167">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="El color de fondo de la Página principal y los vínculos de contacto ahora es azul" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="e0a28-169">El color de fondo de la **Página principal** y los vínculos de **contacto** ahora es azul</span><span class="sxs-lookup"><span data-stu-id="e0a28-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0a28-170">Volver a usar estilos en una sola página con hojas de estilo internas</span><span class="sxs-lookup"><span data-stu-id="e0a28-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="e0a28-171">En un fragmento de código anterior, un estilo en línea aplicó un estilo a una sola `<p>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0a28-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="e0a28-172">¿Qué ocurre si desea que todos los `<p>` elementos de la página web tengan el mismo estilo?</span><span class="sxs-lookup"><span data-stu-id="e0a28-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="e0a28-173">Tendría que copiar y pegar el código en cada `<p>` etiqueta del sitio.</span><span class="sxs-lookup"><span data-stu-id="e0a28-173">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="e0a28-174">Eso es mucho tiempo y esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="e0a28-175">Y, si necesita realizar una edición, tendrá que volver a cambiar todas las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="e0a28-175">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="e0a28-176">Complete las siguientes acciones para usar una **hoja de estilos interna** para escribir la CSS una vez, de modo que se aplique a varios elementos.</span><span class="sxs-lookup"><span data-stu-id="e0a28-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="e0a28-177">En la ficha en vivo, elija **contacto** para ir a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="e0a28-177">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="e0a28-178">Observe la fuente de **Inicio** y de **contacto**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="La página de contacto" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="e0a28-180">La página de contacto</span><span class="sxs-lookup"><span data-stu-id="e0a28-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-181">En la **pestaña Editor**, vaya a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-181">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="e0a28-182">Agregue el código siguiente a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="e0a28-183">Recuerde que las líneas que comienzan con `<style>` y terminan con `</style>` son lo que necesita sumar.</span><span class="sxs-lookup"><span data-stu-id="e0a28-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="e0a28-184">El otro código está allí para que sepa dónde colocar el nuevo código.</span><span class="sxs-lookup"><span data-stu-id="e0a28-184">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="e0a28-185">Volver a la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="e0a28-186">Elija **contacto** para volver a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="e0a28-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="e0a28-187">La fuente de **Inicio** y de **contacto** ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e0a28-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La fuente de los vínculos de contactos y de inicio ha cambiado" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="e0a28-189">La fuente de los vínculos de **contactos** y de **Inicio** ha cambiado</span><span class="sxs-lookup"><span data-stu-id="e0a28-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0a28-190">Comprender las hojas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="e0a28-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="e0a28-191">Las hojas de estilo internas aplican estilos mediante **selectores**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="e0a28-192">Los selectores son patrones que pueden aplicarse a uno o varios elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="e0a28-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="e0a28-193">El fragmento de código anterior agregó el siguiente estilo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="e0a28-194">es un selector que se traduce en "cualquier `<li>` elemento que contiene un `<a>` elemento".</span><span class="sxs-lookup"><span data-stu-id="e0a28-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="e0a28-195">El explorador cambia la fuente de los vínculos de **contactos** y de **Inicio** , ya que cada uno de los grupos de etiquetas coincide con el patrón.</span><span class="sxs-lookup"><span data-stu-id="e0a28-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="e0a28-196">es una **declaración**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-196">is a **declaration**.</span></span>  <span data-ttu-id="e0a28-197">Una declaración consta de dos partes siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0a28-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e0a28-198">propiedad</span><span class="sxs-lookup"><span data-stu-id="e0a28-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e0a28-199">La propiedad describe una forma general de cambiar el estilo del elemento.</span><span class="sxs-lookup"><span data-stu-id="e0a28-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e0a28-200">value</span><span class="sxs-lookup"><span data-stu-id="e0a28-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e0a28-201">El valor describe exactamente cómo debe cambiar el estilo del elemento.</span><span class="sxs-lookup"><span data-stu-id="e0a28-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e0a28-202">Por ejemplo, `font-family: 'Courier New', Courier, serif` proporciona al explorador las siguientes instrucciones: "establecer la fuente de los elementos que coinciden con el patrón `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="e0a28-203">Si esa fuente no está disponible, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="e0a28-204">Si no está disponible, use `serif` ".</span><span class="sxs-lookup"><span data-stu-id="e0a28-204">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="e0a28-205">Agregar varios selectores a un conjunto de reglas</span><span class="sxs-lookup"><span data-stu-id="e0a28-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="e0a28-206">Un conjunto de códigos CSS, como el que se muestra a continuación, se denomina conjunto de **reglas**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-206">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="e0a28-207">Complete las siguientes acciones para usar comas para agregar varios selectores a un conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="e0a28-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="e0a28-208">En la **pestaña Editor**, Abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="e0a28-209">Después del `li a` tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="e0a28-210">El fragmento de código anterior indica al explorador que debe aplicar estilo a los elementos `<h1>` de la misma manera en que estilos de los elementos que coinciden con el patrón `li a` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="e0a28-211">Ir a la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-211">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="e0a28-212">Elija el vínculo de **contacto** para volver a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="e0a28-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="e0a28-213">Ahora, **póngase en contacto conmigo.**</span><span class="sxs-lookup"><span data-stu-id="e0a28-213">Now, **Contact Me!**</span></span> <span data-ttu-id="e0a28-214">tiene la misma fuente que los vínculos de navegación.</span><span class="sxs-lookup"><span data-stu-id="e0a28-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="El texto contactar conmigo.  ahora tiene la misma fuente que los vínculos de contactos y de inicio" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="e0a28-217">El texto **contactar conmigo.**</span><span class="sxs-lookup"><span data-stu-id="e0a28-217">The text **Contact Me!**</span></span> <span data-ttu-id="e0a28-218">ahora tiene la misma fuente que los vínculos de **contactos** y de **Inicio**</span><span class="sxs-lookup"><span data-stu-id="e0a28-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0a28-219">Experimentar con DevTools</span><span class="sxs-lookup"><span data-stu-id="e0a28-219">Experiment with DevTools</span></span>  

<span data-ttu-id="e0a28-220">A medida que continúe con el camino para convertirse en un experto en el desarrollo web, puede encontrarse con que CSS es complicado.</span><span class="sxs-lookup"><span data-stu-id="e0a28-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="e0a28-221">Puede escribir algo de CSS y esperar que se muestre de una forma, pero el explorador hace algo totalmente diferente.</span><span class="sxs-lookup"><span data-stu-id="e0a28-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="e0a28-222">Microsoft Edge DevTools permite experimentar con los cambios y ver inmediatamente cómo afectan los cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="e0a28-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="e0a28-223">Agregar una declaración a un Ruler existente en DevTools</span><span class="sxs-lookup"><span data-stu-id="e0a28-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="e0a28-224">Complete las siguientes acciones para iterar en el estilo de un elemento existente, agregue una declaración a un conjunto de reglas existente.</span><span class="sxs-lookup"><span data-stu-id="e0a28-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="e0a28-225">Desplace el puntero en el vínculo **Inicio** , abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-225">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspeccionar el vínculo de inicio" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="e0a28-227">Inspeccionar el vínculo de inicio</span><span class="sxs-lookup"><span data-stu-id="e0a28-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e0a28-228">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="e0a28-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="e0a28-229">El código que representa el vínculo de inicio, `<a href="/">Home</a>` está resaltado en azul en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e0a28-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="e0a28-230">El fragmento de código y la vista previa deben conocer la [Introducción a HTML y el Dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="e0a28-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="e0a28-231">En la siguiente ilustración, la `font-family: 'Courier New', Courier, serif` declaración a la que ha agregado previamente `contact.html` se ve en la pestaña **estilos** , debajo del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e0a28-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="La pestaña estilos está debajo del árbol DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="e0a28-233">La pestaña **estilos** está debajo del árbol DOM</span><span class="sxs-lookup"><span data-stu-id="e0a28-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="e0a28-234">Si la ventana de DevTools es ancha, la pestaña estilos está a la derecha del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e0a28-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="La pestaña estilos está a la derecha del árbol DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="e0a28-236">La pestaña **estilos** está a la derecha del árbol DOM</span><span class="sxs-lookup"><span data-stu-id="e0a28-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="e0a28-237">Elija la línea vacía a continuación `font-family: 'Courier New', Courier, Serif` para agregar una declaración nueva.</span><span class="sxs-lookup"><span data-stu-id="e0a28-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Agregar una declaración nueva" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="e0a28-239">Agregar una declaración nueva</span><span class="sxs-lookup"><span data-stu-id="e0a28-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-240">Escriba `color` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="e0a28-241">La interfaz de usuario de autocompletar sugiere opciones mientras escribe.</span><span class="sxs-lookup"><span data-stu-id="e0a28-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Color de texto" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="e0a28-243">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0a28-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-244">Escriba `magenta` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="e0a28-245">Todo el texto de la página de contacto ahora es magenta.</span><span class="sxs-lookup"><span data-stu-id="e0a28-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Tipo magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="e0a28-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0a28-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="e0a28-248">Editar una declaración en DevTools</span><span class="sxs-lookup"><span data-stu-id="e0a28-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="e0a28-249">Complete las siguientes acciones para editar las declaraciones existentes en DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0a28-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="e0a28-250">Elija el cuadrado magenta junto a `magenta` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="e0a28-251">Aparece un selector de color.</span><span class="sxs-lookup"><span data-stu-id="e0a28-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="El selector de colores" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="e0a28-253">El selector de colores</span><span class="sxs-lookup"><span data-stu-id="e0a28-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-254">Use el selector de colores para cambiar el texto de la fuente a un color que le guste.</span><span class="sxs-lookup"><span data-stu-id="e0a28-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Cambiar el color de la fuente a púrpura con el selector de colores" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="e0a28-256">Cambiar el color de la fuente a púrpura con el selector de colores</span><span class="sxs-lookup"><span data-stu-id="e0a28-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0a28-257">Agregar un nuevo conjunto de reglas en DevTools</span><span class="sxs-lookup"><span data-stu-id="e0a28-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="e0a28-258">Complete las acciones siguientes para agregar nuevos conjuntos de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0a28-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="e0a28-259">Elija **nueva regla de estilo** \ ( ![ nueva regla de estilo ][ImageNewStyleRuleIcon] \) que está junto a **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="e0a28-260">Aparece un conjunto de reglas vacío con `a` el selector.</span><span class="sxs-lookup"><span data-stu-id="e0a28-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Agregar una nueva regla" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="e0a28-262">Agregar una nueva regla</span><span class="sxs-lookup"><span data-stu-id="e0a28-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-263">Reemplazar `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Reemplazar a con a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="e0a28-265">Reemplazar `a` por</span><span class="sxs-lookup"><span data-stu-id="e0a28-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="e0a28-266">es una **seudoclase**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="e0a28-267">Use las pseudo-clases para los elementos de estilo que pueden entrar en Estados especiales.</span><span class="sxs-lookup"><span data-stu-id="e0a28-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="e0a28-268">Por ejemplo, el `a:hover` estilo solo surte efecto cuando se coloca el puntero sobre un `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="e0a28-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="e0a28-269">Elija entre los corchetes para agregar una declaración nueva.</span><span class="sxs-lookup"><span data-stu-id="e0a28-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="e0a28-270">Escriba `background-color` el nombre de la declaración y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Tipo background-color" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="e0a28-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0a28-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-273">Escriba `green` el valor de declaración y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Tipo verde" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="e0a28-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0a28-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-276">Mantenga el mouse sobre el vínculo **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="e0a28-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="e0a28-277">El fondo del vínculo se vuelve de color verde.</span><span class="sxs-lookup"><span data-stu-id="e0a28-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Desplace el puntero sobre el vínculo Inicio para mostrar su fondo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="e0a28-279">Desplace el puntero sobre el vínculo Inicio para mostrar su fondo verde</span><span class="sxs-lookup"><span data-stu-id="e0a28-279">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0a28-280">Volver a usar estilos entre páginas con hojas de estilo externas</span><span class="sxs-lookup"><span data-stu-id="e0a28-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="e0a28-281">En un paso anterior, agregó el siguiente fragmento de código como una hoja de estilos interna `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="e0a28-282">¿Qué sucede si desea aplicar estilo `index.html` de la misma manera?</span><span class="sxs-lookup"><span data-stu-id="e0a28-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="e0a28-283">¿Qué ocurre si tiene una gran cantidad de páginas a las que desea aplicar los estilos?</span><span class="sxs-lookup"><span data-stu-id="e0a28-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="e0a28-284">Tendría que copiar y pegar la hoja de estilos interna en todas las páginas web del sitio.</span><span class="sxs-lookup"><span data-stu-id="e0a28-284">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="e0a28-285">Complete las siguientes acciones para agregar una **hoja de estilos externa** que le permita escribir una vez su CSS y aplicarlo a varias páginas.</span><span class="sxs-lookup"><span data-stu-id="e0a28-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="e0a28-286">En primer lugar, vuelva a cargar la ficha en vivo para quitar los cambios que realizó en DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0a28-286">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Después de actualizar la página, los cambios realizados en DevTools desaparecen" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="e0a28-288">Después de actualizar la página, los cambios realizados en DevTools desaparecen</span><span class="sxs-lookup"><span data-stu-id="e0a28-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-289">Vuelva a la **pestaña Editor** y Abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="e0a28-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="e0a28-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-292">Elimine todo lo que hay entre `<style>` y `</style>` , incluidos `<style>` y `</style>` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Se ha quitado la etiqueta de estilo" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="e0a28-294">Se ha quitado la etiqueta de estilo</span><span class="sxs-lookup"><span data-stu-id="e0a28-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-295">Ir a `index.html` y quitar `style="background-color: aliceblue;"` de la `<nav>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0a28-295">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="e0a28-296">Ahora ha quitado todas las CSS que agregó previamente a su sitio.</span><span class="sxs-lookup"><span data-stu-id="e0a28-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="El estilo insertado se ha quitado del elemento NAV" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="e0a28-298">El estilo insertado se ha quitado del elemento NAV</span><span class="sxs-lookup"><span data-stu-id="e0a28-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-299">Elija **nuevo archivo**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="El cuadro de diálogo nuevo archivo" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="e0a28-301">El cuadro de diálogo nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="e0a28-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-302">Reemplazar `cool-file.js` por `style.css` y elija **Agregar archivo**.</span><span class="sxs-lookup"><span data-stu-id="e0a28-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Tipo Style. CSS" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="e0a28-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0a28-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-305">Agregue el siguiente fragmento de código al `style.css` archivo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-305">Add the following code snippet to your `style.css` file.</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Agregar código a Style. CSS" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="e0a28-307">Agregar código a</span><span class="sxs-lookup"><span data-stu-id="e0a28-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="e0a28-308">Asegúrese de haber creado una hoja de estilos externa.</span><span class="sxs-lookup"><span data-stu-id="e0a28-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="e0a28-309">El código HTML no es consciente de que existe.</span><span class="sxs-lookup"><span data-stu-id="e0a28-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="e0a28-310">Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="e0a28-311">Agrega `<link rel="stylesheet" href="style.css">` a tu HTML.</span><span class="sxs-lookup"><span data-stu-id="e0a28-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Vínculo a Style. CSS" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="e0a28-313">Vínculo a</span><span class="sxs-lookup"><span data-stu-id="e0a28-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-314">Abra el `contact.html` archivo y agregue el vínculo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Vínculo a Style. CSS en contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="e0a28-316">Vincular a `style.css` en</span><span class="sxs-lookup"><span data-stu-id="e0a28-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-317">Ir a la **ficha en vivo**.  La Página principal ahora tiene la misma fuente de la última sección y una sección de navegación azul.</span><span class="sxs-lookup"><span data-stu-id="e0a28-317">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="La Página principal" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="e0a28-319">La Página principal</span><span class="sxs-lookup"><span data-stu-id="e0a28-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-320">Elija el vínculo de **contacto** para ir a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="e0a28-320">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="e0a28-321">La página de contacto tiene el mismo formato que la Página principal.</span><span class="sxs-lookup"><span data-stu-id="e0a28-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="La página de contacto" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="e0a28-323">La página de contacto</span><span class="sxs-lookup"><span data-stu-id="e0a28-323">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0a28-324">Usar un marco CSS</span><span class="sxs-lookup"><span data-stu-id="e0a28-324">Use a CSS framework</span></span>  

<span data-ttu-id="e0a28-325">Los **Marcos CSS** son colecciones de estilos creados por otros programadores que facilitan la creación de atractivos sitios Web.</span><span class="sxs-lookup"><span data-stu-id="e0a28-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="e0a28-326">En lugar de definir estilos usted mismo, un marco de trabajo le proporciona una colección de estilos que puede usar en los elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="e0a28-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="e0a28-327">Copie el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="e0a28-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="e0a28-328">Vaya a la pestaña edición y pegue el código en `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-328">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Vínculo al marco en contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="e0a28-330">Vínculo al marco en</span><span class="sxs-lookup"><span data-stu-id="e0a28-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-331">Abra el `index.html` archivo y agregue el código allí.</span><span class="sxs-lookup"><span data-stu-id="e0a28-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Vínculo al marco en index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="e0a28-333">Vínculo al marco en</span><span class="sxs-lookup"><span data-stu-id="e0a28-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-334">Vuelva a la pestaña en vivo para ver los cambios.</span><span class="sxs-lookup"><span data-stu-id="e0a28-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="e0a28-335">Aunque el color de fondo del `<nav>` elemento y la fuente de los `<li>` `<a>` elementos y son iguales, la fuente del resto de los elementos ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e0a28-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Se cambió parte de la fuente de la Página principal a causa del marco de trabajo" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="e0a28-337">Se cambió parte de la fuente de la Página principal a causa del marco de trabajo</span><span class="sxs-lookup"><span data-stu-id="e0a28-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0a28-338">Usar una clase</span><span class="sxs-lookup"><span data-stu-id="e0a28-338">Use a class</span></span>  

<span data-ttu-id="e0a28-339">En la última sección, agregó bootstrap a sus páginas web, que cambió las fuentes de algunos de los elementos de su sitio.</span><span class="sxs-lookup"><span data-stu-id="e0a28-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="e0a28-340">Los marcos CSS le ayudan a hacer cambios importantes en la página con muy poco código.</span><span class="sxs-lookup"><span data-stu-id="e0a28-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="e0a28-341">Complete las acciones siguientes para cambiar el encabezado.</span><span class="sxs-lookup"><span data-stu-id="e0a28-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="e0a28-342">Copie el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e0a28-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="e0a28-343">Agregue el fragmento de código anterior a la `<header>` etiqueta en `index.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Agregar clases en index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="e0a28-345">Agregar clases en</span><span class="sxs-lookup"><span data-stu-id="e0a28-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-346">Agrega el código a tu `<header>` etiqueta en `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Agregar clases en contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="e0a28-348">Agregar clases en</span><span class="sxs-lookup"><span data-stu-id="e0a28-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-349">Ver los cambios en la ficha en vivo.  Hay un cuadro gris grande en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="e0a28-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="El encabezado ahora tiene un gran cuadro gris a su lado" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="e0a28-351">El encabezado ahora tiene un gran cuadro gris a su lado</span><span class="sxs-lookup"><span data-stu-id="e0a28-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e0a28-352">Comprender las clases</span><span class="sxs-lookup"><span data-stu-id="e0a28-352">Understand classes</span></span>  

<span data-ttu-id="e0a28-353">Las clases permiten asignar colecciones de estilos a elementos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="e0a28-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="e0a28-354">Use el siguiente fragmento de código para aplicar varios estilos al `<header>` elemento después de establecer el `class` atributo en `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="e0a28-355">Una de las ventajas de una clase es que le permite aplicar estilos a cualquier elemento que desee.</span><span class="sxs-lookup"><span data-stu-id="e0a28-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="e0a28-356">Por ejemplo, suponga que desea establecer el color de fondo de algunos `<p>` elementos en morado, pero no en todos los `<p>` elementos.</span><span class="sxs-lookup"><span data-stu-id="e0a28-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="e0a28-357">Use el siguiente fragmento de código para definir el estilo de una clase.</span><span class="sxs-lookup"><span data-stu-id="e0a28-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="e0a28-358">A continuación, aplique la clase solo a los `<p>` elementos a los que quiere aplicar un estilo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="e0a28-359">Alinear elementos</span><span class="sxs-lookup"><span data-stu-id="e0a28-359">Align elements</span></span>  

<span data-ttu-id="e0a28-360">Complete las siguientes acciones para iniciar y proporcionar clases para alinear elementos.</span><span class="sxs-lookup"><span data-stu-id="e0a28-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="e0a28-361">Vuelva a la pestaña Editor y Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="e0a28-362">Agregar `class="container-fluid"` a la `<body>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0a28-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Agregar la clase de fluidos contenedor" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="e0a28-364">Agregar la `container-fluid` clase</span><span class="sxs-lookup"><span data-stu-id="e0a28-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-365">Ajustar los `<nav>` `<main>` elementos y en `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="e0a28-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="e0a28-366">Asegúrate `</div>` de poner después `</main>` para cerrar correctamente la nueva etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0a28-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Agregar una fila" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="e0a28-368">Agregar una fila</span><span class="sxs-lookup"><span data-stu-id="e0a28-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-369">Agregar `class="col-3"` a la `<nav>` etiqueta y `class="col-9"` a la `<main>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0a28-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Agregar las clases col-3 y col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="e0a28-371">Agregar las `col-3` `col-9` clases y</span><span class="sxs-lookup"><span data-stu-id="e0a28-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0a28-372">Ver los cambios en la ficha en vivo.</span><span class="sxs-lookup"><span data-stu-id="e0a28-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal." lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="e0a28-374">Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal.</span><span class="sxs-lookup"><span data-stu-id="e0a28-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0a28-375">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e0a28-375">Next steps</span></span>  

<span data-ttu-id="e0a28-376">Ya ha terminado.</span><span class="sxs-lookup"><span data-stu-id="e0a28-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="e0a28-377">La mejor manera de mejorar el desarrollo web es crear más sitios.</span><span class="sxs-lookup"><span data-stu-id="e0a28-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="e0a28-378">No te preocupes por la rotura de cosas.</span><span class="sxs-lookup"><span data-stu-id="e0a28-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="e0a28-379">Divertirte y aprender lo máximo posible en el camino.</span><span class="sxs-lookup"><span data-stu-id="e0a28-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="e0a28-380">Para obtener más información sobre cómo aplicar estilos a páginas web, consulte [Introducción a CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="e0a28-380">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="e0a28-381">Para obtener más información sobre cómo usar DevTools para experimentar con las CSS de una página, consulte Introducción a la [visualización y el cambio de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="e0a28-381">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para principiantes: Introducción a HTML y DOM | Microsoft docs"  
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cocinada-Amphibian | Intento"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeros pasos de CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="e0a28-387">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e0a28-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e0a28-388">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/css) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="e0a28-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e0a28-390">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e0a28-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
