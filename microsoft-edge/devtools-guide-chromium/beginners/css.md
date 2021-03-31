---
description: Introducción a CSS
title: 'DevTools para principiantes: Introducción a CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 6a7135e144123917535e7c43e6a3cd608ec0c8a7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439440"
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

# <a name="devtools-for-beginners-get-started-with-css"></a><span data-ttu-id="a5e6b-104">DevTools para principiantes: Introducción a CSS</span><span class="sxs-lookup"><span data-stu-id="a5e6b-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="a5e6b-105">En este tutorial, aprenderá a usar CSS para dar estilo a una página web.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="a5e6b-106">También aprenderá a usar Microsoft Edge DevTools para experimentar con los cambios css.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="a5e6b-107">El siguiente artículo es el segundo tutorial de una serie de tutoriales que le enseña los conceptos básicos del desarrollo web y Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="a5e6b-108">Para obtener experiencia práctica, cree su propio sitio web.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="a5e6b-109">No es necesario completar el primer tutorial antes de seguir el segundo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="a5e6b-110">[Configurar el código muestra](#set-up-your-code) cómo configurarse.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5e6b-111">Este tutorial está diseñado para principiantes absolutos y se centra en los **conceptos básicos** del desarrollo web y los conceptos básicos del uso de DevTools para experimentar con CSS.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="a5e6b-112">Si desea un tutorial que solo se centre en DevTools, vaya a Introducción a [Ver y cambiar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-112">If you want a tutorial that only focuses on DevTools, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="a5e6b-113">Al principio del tutorial, el sitio debe ser parecido a la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Cómo es el sitio actualmente" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="a5e6b-115">Cómo es el sitio actualmente</span><span class="sxs-lookup"><span data-stu-id="a5e6b-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="a5e6b-116">Después de completar el tutorial, el sitio debe ser parecido a la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Cómo debe ser el sitio al final del tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="a5e6b-118">Cómo debe ser el sitio al final del tutorial</span><span class="sxs-lookup"><span data-stu-id="a5e6b-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <a name="goals"></a><span data-ttu-id="a5e6b-119">Objetivos</span><span class="sxs-lookup"><span data-stu-id="a5e6b-119">Goals</span></span>  

<span data-ttu-id="a5e6b-120">Siga este tutorial para comprender mejor los siguientes conceptos y tareas.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="a5e6b-121">Cómo usar CSS para dar estilo a una página web.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="a5e6b-122">Cómo usar Microsoft Edge DevTools para experimentar con CSS.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="a5e6b-123">La diferencia entre los marcos CSS y CSS.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="a5e6b-124">Está creando un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-124">You are building a real website.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="a5e6b-125">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a5e6b-125">Prerequisites</span></span>  

<span data-ttu-id="a5e6b-126">Antes de intentar este tutorial, complete los siguientes requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="a5e6b-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] o asegúrese de que tiene una comprensión de HTML y DOM similar a lo que se enseña en ese tutorial.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="a5e6b-128">Descargue el explorador web [de Microsoft Edge.][MicrosoftEdgeInsider]</span><span class="sxs-lookup"><span data-stu-id="a5e6b-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="a5e6b-129">En el siguiente tutorial se usa un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, integradas en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="a5e6b-130">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="a5e6b-130">Set up your code</span></span>  

<span data-ttu-id="a5e6b-131">Para crear el sitio, primero debe completar las siguientes acciones para configurar el código.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5e6b-132">Si ya ha completado el primer tutorial de la serie, vaya a la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="a5e6b-133">Siga usando el código del último tutorial, [Introducción a HTML y DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="a5e6b-134">Abra el [código fuente][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="a5e6b-135">Se hace referencia a la pestaña en el foco del explorador como la **pestaña de edición**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="La pestaña de edición" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="a5e6b-137">La **pestaña de** edición</span><span class="sxs-lookup"><span data-stu-id="a5e6b-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-138">Elija **cooked-amphibian**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="a5e6b-139">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menú Opciones del proyecto" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="a5e6b-141">Menú Opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="a5e6b-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="a5e6b-142">Elija **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="a5e6b-143">Glitch crea una copia del proyecto que puede editar.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a5e6b-144">Glitch genera un nombre aleatorio para el nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="a5e6b-145">Elija **Mostrar** y **elija En una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-145">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="a5e6b-146">Se abre otra pestaña con una vista en directo del sitio.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="a5e6b-147">Se hace referencia a la pestaña en el foco del explorador como la **pestaña activa**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="La pestaña activa" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="a5e6b-149">La **pestaña activa**</span><span class="sxs-lookup"><span data-stu-id="a5e6b-149">The **live tab**</span></span>  
    :::image-end:::  

## <a name="understand-css"></a><span data-ttu-id="a5e6b-150">Comprender CSS</span><span class="sxs-lookup"><span data-stu-id="a5e6b-150">Understand CSS</span></span>  

<span data-ttu-id="a5e6b-151">**CSS** es un idioma de equipo que determina el diseño y el estilo de las páginas web.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="a5e6b-152">La siguiente figura es un párrafo con un borde.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="El texto se ha estilo con CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="a5e6b-154">El texto se ha estilo con CSS</span><span class="sxs-lookup"><span data-stu-id="a5e6b-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="a5e6b-155">El siguiente fragmento de código es el código HTML y CSS usado para crear el párrafo de la figura anterior.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="a5e6b-156">probablemente tenga un aspecto nuevo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-156">probably looks new to you.</span></span>  <span data-ttu-id="a5e6b-157">El resto debería ser familiar.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-157">The rest should look familiar.</span></span>  <span data-ttu-id="a5e6b-158">Si no es así, complete [Introducción con HTML y DOM][DevtoolsBeginnersHtml] antes de intentar las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <a name="add-inline-styles"></a><span data-ttu-id="a5e6b-159">Agregar estilos en línea</span><span class="sxs-lookup"><span data-stu-id="a5e6b-159">Add inline styles</span></span>  

<span data-ttu-id="a5e6b-160">Complete las siguientes acciones para usar **estilos en línea** para aplicar estilos a un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="a5e6b-161">Vuelva a la pestaña de edición y abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="a5e6b-163">Abrir `index.html` en la pestaña de edición</span><span class="sxs-lookup"><span data-stu-id="a5e6b-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-164">Agregar `style="background-color: aliceblue;"` a su `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="a5e6b-165">En el bloque de código siguiente, la cuarta línea de código es la que necesita cambiar.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="a5e6b-166">El resto está justo ahí, por lo que puede asegurarse de que está colocando el nuevo código en el lugar correcto.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
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
    
1.  <span data-ttu-id="a5e6b-167">Para mostrar los cambios, vaya a la **pestaña activa**.  El fondo de la `<nav>` sección es ahora azul.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-167">To display the changes, navigate to the **live tab**.  The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="El color de fondo detrás de los vínculos Inicio y Contacto ahora es azul" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="a5e6b-169">El color de fondo detrás de los **vínculos Inicio** **y** Contacto ahora es azul</span><span class="sxs-lookup"><span data-stu-id="a5e6b-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a><span data-ttu-id="a5e6b-170">Volver a usar estilos en una sola página con hojas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="a5e6b-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="a5e6b-171">En un fragmento de código anterior, un estilo en línea aplicó un estilo a una sola `<p>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="a5e6b-172">¿Qué sucede si desea que todos los elementos de la página web se den el mismo `<p>` estilo?</span><span class="sxs-lookup"><span data-stu-id="a5e6b-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="a5e6b-173">Debe copiar y pegar el código en todas las `<p>` etiquetas del sitio.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-173">You have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="a5e6b-174">Eso es mucho tiempo y esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="a5e6b-175">Y, si necesita realizar una edición, debe cambiar todas las etiquetas de nuevo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-175">And, if you needed to make an edit, you have to change every tag again.</span></span>  <span data-ttu-id="a5e6b-176">Complete las siguientes acciones para usar una hoja de estilos **interna** para escribir el CSS una vez para que se aplique a varios elementos.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="a5e6b-177">En la pestaña activa, elija **Contacto** para navegar a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-177">In the live tab, choose **Contact** to navigate to the contact page.</span></span>  <span data-ttu-id="a5e6b-178">Observe la fuente de **Inicio** y **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="La página Contacto" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="a5e6b-180">La página Contacto</span><span class="sxs-lookup"><span data-stu-id="a5e6b-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-181">En la **pestaña editor**, abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-181">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="a5e6b-182">Agregue el siguiente código a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="a5e6b-183">Recuerde que las líneas que comienzan `<style>` con y terminan con son las que necesita `</style>` agregar.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="a5e6b-184">El otro código está justo ahí para que sepa dónde colocar el nuevo código.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-184">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="a5e6b-185">Vuelva a la **pestaña activa**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="a5e6b-186">Elija **Contacto** para volver a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="a5e6b-187">La fuente de **Inicio** y **Contacto** ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La fuente de los vínculos Inicio y Contacto ha cambiado" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="a5e6b-189">La fuente de los **vínculos Inicio** **y** Contacto ha cambiado</span><span class="sxs-lookup"><span data-stu-id="a5e6b-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a><span data-ttu-id="a5e6b-190">Comprender hojas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="a5e6b-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="a5e6b-191">Las hojas de estilos internas aplican estilos mediante **selectores**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="a5e6b-192">Los selectores son patrones que pueden aplicarse a uno o varios elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="a5e6b-193">El fragmento de código anterior agregó el siguiente estilo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="a5e6b-194">es un selector que se traduce a "cualquier `<li>` elemento que contenga un `<a>` elemento".</span><span class="sxs-lookup"><span data-stu-id="a5e6b-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="a5e6b-195">El explorador cambia la fuente de los vínculos **Inicio** y **Contacto** porque cada uno de los grupos de etiquetas coincide con el patrón.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="a5e6b-196">es una **declaración**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-196">is a **declaration**.</span></span>  <span data-ttu-id="a5e6b-197">Se realiza una declaración de dos partes siguientes.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="a5e6b-198">propiedad</span><span class="sxs-lookup"><span data-stu-id="a5e6b-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a5e6b-199">La propiedad describe una forma general de cambiar el estilo del elemento.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="a5e6b-200">value</span><span class="sxs-lookup"><span data-stu-id="a5e6b-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a5e6b-201">El valor describe exactamente cómo debe cambiar el estilo del elemento.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a5e6b-202">Por ejemplo, `font-family: 'Courier New', Courier, serif` proporciona al explorador la siguiente instrucción: "Establecer la fuente de los elementos que coinciden con el patrón en `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="a5e6b-203">Si esa fuente no está disponible, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="a5e6b-204">Si no está disponible, use `serif` ."</span><span class="sxs-lookup"><span data-stu-id="a5e6b-204">If that is not available, use `serif`."</span></span>  

### <a name="add-multiple-selectors-to-a-ruleset"></a><span data-ttu-id="a5e6b-205">Agregar varios selectores a un conjunto de reglas</span><span class="sxs-lookup"><span data-stu-id="a5e6b-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="a5e6b-206">Un bloque de código CSS como el siguiente fragmento de código se denomina conjunto **de reglas**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-206">A block of CSS code like the following code snippet is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="a5e6b-207">Complete las siguientes acciones para usar comas para agregar varios selectores a un conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="a5e6b-208">En la **pestaña editor**, abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="a5e6b-209">Después `li a` del tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="a5e6b-210">El fragmento de código anterior indica al explorador que le de estilo a los elementos de la misma forma que estilos `<h1>` de elementos que coinciden con el patrón `li a` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="a5e6b-211">Vaya a la **pestaña activa**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-211">Navigate to the **live tab**.</span></span>  
1.  <span data-ttu-id="a5e6b-212">Elija el **vínculo** Contacto para volver a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="a5e6b-213">Ahora, **Póngase en contacto conmigo.**</span><span class="sxs-lookup"><span data-stu-id="a5e6b-213">Now, **Contact Me!**</span></span> <span data-ttu-id="a5e6b-214">tiene la misma fuente que los vínculos de navegación.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="¡El texto Póngase en contacto conmigo!  ahora tiene la misma fuente que los vínculos Inicio y Contacto" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="a5e6b-217">¡El texto **Póngase en contacto conmigo!**</span><span class="sxs-lookup"><span data-stu-id="a5e6b-217">The text **Contact Me!**</span></span> <span data-ttu-id="a5e6b-218">ahora tiene la misma fuente que los vínculos **Inicio** **y** Contacto</span><span class="sxs-lookup"><span data-stu-id="a5e6b-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a><span data-ttu-id="a5e6b-219">Experimentar con DevTools</span><span class="sxs-lookup"><span data-stu-id="a5e6b-219">Experiment with DevTools</span></span>  

<span data-ttu-id="a5e6b-220">A medida que continúa su viaje para convertirse en un experto en desarrollo web, puede que encuentre que CSS es complicado.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="a5e6b-221">Puede escribir algún CSS y esperar que se muestre de una manera, pero el explorador hace algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="a5e6b-222">Microsoft Edge DevTools facilita la experimentación con los cambios y muestra inmediatamente cómo afectan los cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately display how the changes affect the page.</span></span>  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a><span data-ttu-id="a5e6b-223">Agregar una declaración a un rulest existente en DevTools</span><span class="sxs-lookup"><span data-stu-id="a5e6b-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="a5e6b-224">Complete las siguientes acciones para iterar en el estilo de un elemento existente y agregue una declaración a un conjunto de reglas existente.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="a5e6b-225">Mantenga el mouse en **el vínculo** Inicio, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-225">Hover on the **Home** link, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspeccionar el vínculo Inicio" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="a5e6b-227">Inspeccionar el vínculo Inicio</span><span class="sxs-lookup"><span data-stu-id="a5e6b-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="a5e6b-228">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="a5e6b-229">El código que representa el vínculo Inicio, `<a href="/">Home</a>` se resalta en azul en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="a5e6b-230">El fragmento de código y la vista previa deben estar familiarizados con [Introducción a HTML y DOM.][DevtoolsBeginnersHtml]</span><span class="sxs-lookup"><span data-stu-id="a5e6b-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="a5e6b-231">En la siguiente figura, la declaración que agregó anteriormente se muestra en la pestaña Estilos debajo `font-family: 'Courier New', Courier, serif` `contact.html` del árbol DOM. </span><span class="sxs-lookup"><span data-stu-id="a5e6b-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is displayed in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="La pestaña Estilos está debajo del árbol DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="a5e6b-233">La **pestaña Estilos** está debajo del árbol DOM</span><span class="sxs-lookup"><span data-stu-id="a5e6b-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="a5e6b-234">Si la ventana DevTools es amplia, la pestaña Estilos está a la derecha del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="La pestaña Estilos está a la derecha del árbol DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="a5e6b-236">La **pestaña Estilos** está a la derecha del árbol DOM</span><span class="sxs-lookup"><span data-stu-id="a5e6b-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="a5e6b-237">Elija la línea vacía siguiente `font-family: 'Courier New', Courier, Serif` para agregar una nueva declaración.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Agregar una nueva declaración" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="a5e6b-239">Agregar una nueva declaración</span><span class="sxs-lookup"><span data-stu-id="a5e6b-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-240">Escriba `color` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="a5e6b-241">La interfaz de usuario de autocompletar sugiere opciones a medida que escribe.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Color de tipo" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="a5e6b-243">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-244">Escriba `magenta` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="a5e6b-245">Todo el texto de la página de contacto ahora es magenta.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Tipo magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="a5e6b-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a><span data-ttu-id="a5e6b-248">Editar una declaración en DevTools</span><span class="sxs-lookup"><span data-stu-id="a5e6b-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="a5e6b-249">Complete las siguientes acciones para editar las declaraciones existentes en DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="a5e6b-250">Elija el cuadrado magenta junto a `magenta` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="a5e6b-251">Aparece un selector de colores.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Selector de colores" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="a5e6b-253">Selector de colores</span><span class="sxs-lookup"><span data-stu-id="a5e6b-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-254">Use el selector de colores para cambiar el texto de fuente a un color que quiera.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Cambiar el color de fuente a púrpura con el Selector de colores" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="a5e6b-256">Cambiar el color de fuente a púrpura con el Selector de colores</span><span class="sxs-lookup"><span data-stu-id="a5e6b-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a><span data-ttu-id="a5e6b-257">Agregar un nuevo conjunto de reglas en DevTools</span><span class="sxs-lookup"><span data-stu-id="a5e6b-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="a5e6b-258">Complete las siguientes acciones para agregar nuevos conjuntos de reglas en DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="a5e6b-259">Elija **Nueva regla de estilo** \( Nueva regla de estilo ![ ](../media/new-style-rule-icon.msft.png) \) que está junto a **.cls**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-259">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) which is next to **.cls**.</span></span>  <span data-ttu-id="a5e6b-260">Aparece un conjunto de reglas vacío `a` con como selector.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Agregar una nueva regla" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="a5e6b-262">Agregar una nueva regla</span><span class="sxs-lookup"><span data-stu-id="a5e6b-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-263">Reemplace `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Reemplazar a con a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="a5e6b-265">Reemplazar `a` por</span><span class="sxs-lookup"><span data-stu-id="a5e6b-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="a5e6b-266">es una **pseudo-clase**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="a5e6b-267">Use pseudo-clases para elementos de estilo que puedan entrar en estados especiales.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="a5e6b-268">Por ejemplo, el estilo solo tiene efecto cuando se pasa el `a:hover` mouse sobre un `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="a5e6b-269">Elija entre corchetes para agregar una nueva declaración.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="a5e6b-270">Escriba `background-color` el nombre de declaración y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Tipo de fondo-color" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="a5e6b-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-273">Escriba `green` para el valor de declaración y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Escriba verde" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="a5e6b-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-276">Mantenga el mouse sobre el **vínculo** Inicio.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="a5e6b-277">El fondo del vínculo se vuelve verde.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Mantenga el mouse en el vínculo Inicio para mostrar su fondo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="a5e6b-279">Mantenga el mouse en el vínculo Inicio para mostrar su fondo verde</span><span class="sxs-lookup"><span data-stu-id="a5e6b-279">Hover on the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a><span data-ttu-id="a5e6b-280">Volver a usar estilos en páginas con hojas de estilos externas</span><span class="sxs-lookup"><span data-stu-id="a5e6b-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="a5e6b-281">En un paso anterior, agregó el siguiente fragmento de código como hoja de estilos interna a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

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

<span data-ttu-id="a5e6b-282">¿Qué sucede si quieres dar `index.html` el mismo estilo?</span><span class="sxs-lookup"><span data-stu-id="a5e6b-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="a5e6b-283">¿Qué sucede si tuviera un gran número de páginas a las que desea aplicar sus estilos?</span><span class="sxs-lookup"><span data-stu-id="a5e6b-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="a5e6b-284">Debe copiar y pegar la hoja de estilos interna en cada página web del sitio.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-284">You have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="a5e6b-285">Complete las siguientes acciones para agregar una hoja de estilos **externa** que le permita escribir el CSS una vez y aplicarlo a varias páginas.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="a5e6b-286">En primer lugar, actualice la pestaña activa para quitar los cambios realizados en DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-286">First, refresh the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Después de actualizar la página, los cambios realizados en DevTools han desaparecido" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="a5e6b-288">Después de actualizar la página, los cambios realizados en DevTools han desaparecido</span><span class="sxs-lookup"><span data-stu-id="a5e6b-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-289">Vuelva a la **pestaña editor y** abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="a5e6b-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="a5e6b-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-292">Elimine todo lo `<style>` que esté entre y , `</style>` `<style>` incluidos y `</style>` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Se ha quitado la etiqueta de estilo" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="a5e6b-294">Se ha quitado la etiqueta de estilo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-295">Abra `index.html` y quite de la `style="background-color: aliceblue;"` `<nav>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-295">Open `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="a5e6b-296">Ahora ha quitado todo el CSS que agregó anteriormente al sitio.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="El estilo en línea se ha quitado del elemento nav" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="a5e6b-298">El estilo en línea se ha quitado del elemento nav</span><span class="sxs-lookup"><span data-stu-id="a5e6b-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-299">Elija **Nuevo archivo**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="El nuevo cuadro de diálogo de archivo" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="a5e6b-301">El nuevo cuadro de diálogo de archivo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-302">Reemplace `cool-file.js` por y elija Agregar `style.css` **archivo**.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Tipo style.css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="a5e6b-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e6b-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-305">Agregue el siguiente fragmento de código al `style.css` archivo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-305">Add the following code snippet to your `style.css` file.</span></span>  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Agregar código a style.css" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="a5e6b-307">Agregar código a</span><span class="sxs-lookup"><span data-stu-id="a5e6b-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="a5e6b-308">Asegúrese de que ha creado una hoja de estilos externa.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="a5e6b-309">El CÓDIGO HTML no es consciente de que existe.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="a5e6b-310">Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="a5e6b-311">Agregue `<link rel="stylesheet" href="style.css">` a su HTML.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Vínculo a style.css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="a5e6b-313">Vínculo a</span><span class="sxs-lookup"><span data-stu-id="a5e6b-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-314">Abra el `contact.html` archivo y agregue el vínculo allí.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Vínculo a style.css en contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="a5e6b-316">Vincular a `style.css` en</span><span class="sxs-lookup"><span data-stu-id="a5e6b-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-317">Vaya a la **pestaña activa**.  La página principal ahora tiene la misma fuente de la última sección y una sección de navegación azul.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-317">Navigate to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="La página principal" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="a5e6b-319">La página principal</span><span class="sxs-lookup"><span data-stu-id="a5e6b-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-320">Elija el **vínculo** Contacto para navegar a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-320">Choose the **Contact** link to navigate to the contact page.</span></span>  <span data-ttu-id="a5e6b-321">La página de contacto tiene el mismo formato que la página principal.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="La página de contacto" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="a5e6b-323">La página de contacto</span><span class="sxs-lookup"><span data-stu-id="a5e6b-323">The contact page</span></span>  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a><span data-ttu-id="a5e6b-324">Usar un marco CSS</span><span class="sxs-lookup"><span data-stu-id="a5e6b-324">Use a CSS framework</span></span>  

<span data-ttu-id="a5e6b-325">**Los marcos CSS** son colecciones de estilos creados por otros desarrolladores que facilitan la creación de sitios web atractivos.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="a5e6b-326">En lugar de definir estilos usted mismo, un marco le proporciona una colección de estilos que puede usar en los elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="a5e6b-327">Copie el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5e6b-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="a5e6b-328">Abra la pestaña de edición y pegue el código en `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-328">Open the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Vínculo al marco en contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="a5e6b-330">Vínculo al marco en</span><span class="sxs-lookup"><span data-stu-id="a5e6b-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-331">Abra el `index.html` archivo y agregue el código allí.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Vínculo al marco en index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="a5e6b-333">Vínculo al marco en</span><span class="sxs-lookup"><span data-stu-id="a5e6b-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-334">Vuelva a la pestaña activa para ver los cambios.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="a5e6b-335">Aunque el color de fondo del elemento y la fuente de los elementos y son los mismos, la fuente `<nav>` de los otros elementos ha `<li>` `<a>` cambiado.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Parte de la fuente de la página principal ha cambiado debido al marco" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="a5e6b-337">Parte de la fuente de la página principal ha cambiado debido al marco</span><span class="sxs-lookup"><span data-stu-id="a5e6b-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <a name="use-a-class"></a><span data-ttu-id="a5e6b-338">Usar una clase</span><span class="sxs-lookup"><span data-stu-id="a5e6b-338">Use a class</span></span>  

<span data-ttu-id="a5e6b-339">En la última sección, agregó Bootstrap a las páginas web, lo que cambió las fuentes de algunos de los elementos del sitio.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="a5e6b-340">Los marcos CSS le ayudan a realizar cambios importantes en la página con muy poco código.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="a5e6b-341">Complete las siguientes acciones para cambiar el encabezado.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="a5e6b-342">Copie el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="a5e6b-343">Agregue el fragmento de código anterior a la `<header>` etiqueta en `index.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Agregar clases en index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="a5e6b-345">Agregar clases</span><span class="sxs-lookup"><span data-stu-id="a5e6b-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-346">Agregue el código a la `<header>` etiqueta en `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Agregar clases en contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="a5e6b-348">Agregar clases</span><span class="sxs-lookup"><span data-stu-id="a5e6b-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-349">Ver los cambios en la pestaña activa.  Hay un cuadro grande y gris alrededor del encabezado.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="El encabezado ahora tiene un cuadro grande y gris alrededor de él" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="a5e6b-351">El encabezado ahora tiene un cuadro grande y gris alrededor de él</span><span class="sxs-lookup"><span data-stu-id="a5e6b-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <a name="understand-classes"></a><span data-ttu-id="a5e6b-352">Comprender clases</span><span class="sxs-lookup"><span data-stu-id="a5e6b-352">Understand classes</span></span>  

<span data-ttu-id="a5e6b-353">Las clases permiten asignar colecciones de estilos a elementos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="a5e6b-354">Use el siguiente fragmento de código para aplicar varios estilos al `<header>` elemento después de establecer el atributo en `class` `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="a5e6b-355">Una ventaja de una clase es que le permite aplicar estilos a los elementos que desee.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="a5e6b-356">Por ejemplo, supongamos que desea establecer el color de fondo de algunos `<p>` elementos en púrpura, pero no todos los `<p>` elementos.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="a5e6b-357">Use el siguiente fragmento de código para definir el estilo de una clase.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="a5e6b-358">A continuación, aplique la clase solo a los `<p>` elementos que desee aplicar estilo.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a><span data-ttu-id="a5e6b-359">Alinear elementos</span><span class="sxs-lookup"><span data-stu-id="a5e6b-359">Align elements</span></span>  

<span data-ttu-id="a5e6b-360">Complete las siguientes acciones para arrancar y proporcionar clases para alinear elementos.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="a5e6b-361">Vuelva a la pestaña editor y abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="a5e6b-362">Agregue `class="container-fluid"` a la `<body>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Agregar la clase container-fluid" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="a5e6b-364">Agregar la `container-fluid` clase</span><span class="sxs-lookup"><span data-stu-id="a5e6b-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-365">Ajuste los `<nav>` elementos `<main>` y en `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="a5e6b-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="a5e6b-366">Asegúrese de colocar `</div>` después `</main>` para cerrar correctamente la nueva etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Agregar una fila" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="a5e6b-368">Agregar una fila</span><span class="sxs-lookup"><span data-stu-id="a5e6b-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-369">Agregue `class="col-3"` a la etiqueta y a la `<nav>` `class="col-9"` `<main>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Agregar las clases col-3 y col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="a5e6b-371">Agregar las `col-3` clases y `col-9`</span><span class="sxs-lookup"><span data-stu-id="a5e6b-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5e6b-372">Ver los cambios en la pestaña activa.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="El contenido de navegación está ahora a la izquierda del contenido principal" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="a5e6b-374">El contenido de navegación está ahora a la izquierda del contenido principal</span><span class="sxs-lookup"><span data-stu-id="a5e6b-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="a5e6b-375">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="a5e6b-375">Next steps</span></span>  

<span data-ttu-id="a5e6b-376">Enhorabuena, ha terminado.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="a5e6b-377">La mejor forma de mejorar el desarrollo web es crear más sitios.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="a5e6b-378">No te preocupes por las cosas que se rompen.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="a5e6b-379">Simplemente diviértase y aprenda lo más posible a lo largo del camino.</span><span class="sxs-lookup"><span data-stu-id="a5e6b-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="a5e6b-380">Para obtener más información sobre el estilo de páginas web, vaya a [Introducción a CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-380">To learn more about styling web pages, navigate to [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="a5e6b-381">Para obtener más información sobre cómo usar DevTools para experimentar con el CSS de una página, vaya a Introducción a Ver [y cambiar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-381">To learn more about how to use DevTools to experiment with the CSS of a page, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a5e6b-382">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a5e6b-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para principiantes: Introducción a HTML y dom | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html- cocinado-anfibio | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeros pasos de CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="a5e6b-388">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a5e6b-389">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/css) y es creado por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="a5e6b-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a5e6b-391">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5e6b-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
