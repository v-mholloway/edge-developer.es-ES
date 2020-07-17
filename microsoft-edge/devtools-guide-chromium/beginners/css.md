---
title: 'DevTools para principiantes: Introducción a CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882740"
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

# <span data-ttu-id="c3fd9-103">DevTools para principiantes: Introducción a CSS</span><span class="sxs-lookup"><span data-stu-id="c3fd9-103">DevTools for beginners: Get started with CSS</span></span>   

<span data-ttu-id="c3fd9-104">En este tutorial, aprenderá a usar CSS para aplicar un estilo a una página web.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="c3fd9-105">También aprenderá a usar Microsoft Edge DevTools para experimentar con cambios de CSS.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="c3fd9-106">Este es el segundo tutorial de una serie de tutoriales que le enseñan los conceptos básicos del desarrollo web y Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-106">This is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="c3fd9-107">Ganas experiencia práctica creando tu propio sitio Web.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="c3fd9-108">No es necesario que completes el primer tutorial antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-108">You don't have to complete the first tutorial before doing this one.</span></span>  <span data-ttu-id="c3fd9-109">Puedes empezar aquí.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-109">You can start here.</span></span>  <span data-ttu-id="c3fd9-110">[Configurar el código](#set-up-your-code) le muestra cómo realizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="c3fd9-111">Este tutorial está diseñado para principiantes y se centra en los **conceptos básicos del desarrollo web** y en los conceptos básicos del uso de DevTools para experimentar con CSS.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="c3fd9-112">Si desea un tutorial que solo se Centre en DevTools, consulte Introducción [a la visualización y el cambio de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="c3fd9-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="c3fd9-113">Actualmente su sitio tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-113">Currently your site looks like this:</span></span>  

> ##### <span data-ttu-id="c3fd9-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="c3fd9-114">Figure 1</span></span>  
> <span data-ttu-id="c3fd9-115">El aspecto de tu sitio en este momento</span><span class="sxs-lookup"><span data-stu-id="c3fd9-115">What your site currently looks like</span></span>  
> ![El aspecto de tu sitio en este momento][ImageCssIntro1]  

<span data-ttu-id="c3fd9-117">Después de completar el tutorial, tendrá el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-117">After completing the tutorial, it will look like this:</span></span>  

> ##### <span data-ttu-id="c3fd9-118">Figura 2</span><span class="sxs-lookup"><span data-stu-id="c3fd9-118">Figure 2</span></span>  
> <span data-ttu-id="c3fd9-119">El aspecto del sitio al final del tutorial</span><span class="sxs-lookup"><span data-stu-id="c3fd9-119">What your site will look like at the end of the tutorial</span></span>  
> ![El aspecto del sitio al final del tutorial][ImageCssIntro2]  

## <span data-ttu-id="c3fd9-121">Principales</span><span class="sxs-lookup"><span data-stu-id="c3fd9-121">Goals</span></span>   

<span data-ttu-id="c3fd9-122">Al final de este tutorial, comprenderá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-122">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="c3fd9-123">Cómo usar CSS para aplicar un estilo a una página web.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-123">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="c3fd9-124">Cómo usar Microsoft Edge DevTools para experimentar con CSS.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-124">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="c3fd9-125">La diferencia entre los marcos CSS y CSS.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-125">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="c3fd9-126">También tendrá un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-126">You'll also have a real website!</span></span>  

## <span data-ttu-id="c3fd9-127">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c3fd9-127">Prerequisites</span></span>   

<span data-ttu-id="c3fd9-128">Antes de intentar este tutorial, complete los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-128">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="c3fd9-129">Complete Introducción [a HTML y el Dom][DevToolsBeginnersHtml] , o asegúrese de que tiene conocimientos de HTML y Dom parecidos a los impartidos en ese tutorial.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-129">Complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what's taught in that tutorial.</span></span>  
*   <span data-ttu-id="c3fd9-130">Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-130">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="c3fd9-131">En este tutorial se usa un conjunto de herramientas de desarrollo web, denominado Microsoft Edge DevTools, que está integrado en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-131">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="c3fd9-132">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="c3fd9-132">Set up your code</span></span>   

<span data-ttu-id="c3fd9-133">Para empezar a crear su sitio, debe configurar el código:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-133">In order to start creating your site, you need to set up your code:</span></span>  

1.  **<span data-ttu-id="c3fd9-134">Si ya ha completado el primer tutorial de esta serie, omita esta sección.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-134">If you have already completed the first tutorial in this series, skip this section!</span></span>  <span data-ttu-id="c3fd9-135">Continúa usando el código del último tutorial, [Introducción a HTML y el Dom][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="c3fd9-135">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>**  
1.  <span data-ttu-id="c3fd9-136">Abra el [código fuente][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="c3fd9-136">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="c3fd9-137">Esta pestaña del explorador se llamará la **pestaña edición**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-137">This tab of your browser will be called the **editing tab**.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-138">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="c3fd9-138">Figure 3</span></span>  
    > <span data-ttu-id="c3fd9-139">La ficha edición</span><span class="sxs-lookup"><span data-stu-id="c3fd9-139">The editing tab</span></span>  
    > ![La ficha edición][ImageCssSetup1]  
    
1.  <span data-ttu-id="c3fd9-141">Haga clic en **cocinada-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-141">Click **cooked-amphibian**.</span></span>  <span data-ttu-id="c3fd9-142">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-142">A menu pops up.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-143">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="c3fd9-143">Figure 4</span></span>  
    > <span data-ttu-id="c3fd9-144">El menú opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="c3fd9-144">The Project Options menu</span></span>  
    > ![El menú opciones del proyecto][ImageCssSetup2]  

1.  <span data-ttu-id="c3fd9-146">Haga clic en **Remix proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-146">Click **Remix Project**.</span></span>  <span data-ttu-id="c3fd9-147">Problema crea una copia del proyecto que se puede editar.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-147">Glitch creates a copy of the project that you can edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c3fd9-148">El problema genera un nombre aleatorio para el nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-148">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="c3fd9-149">Haga clic en **Mostrar** y seleccione **en una ventana nueva**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-149">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="c3fd9-150">Se abre otra pestaña con una vista en vivo de su sitio.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-150">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="c3fd9-151">Esta pestaña del explorador se llamará la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-151">This tab of your browser will be called the **live tab**.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-152">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="c3fd9-152">Figure 5</span></span>  
    > <span data-ttu-id="c3fd9-153">La ficha en vivo</span><span class="sxs-lookup"><span data-stu-id="c3fd9-153">The live tab</span></span>  
    > ![La ficha en vivo][ImageCssSetup3]  

## <span data-ttu-id="c3fd9-155">Comprender CSS</span><span class="sxs-lookup"><span data-stu-id="c3fd9-155">Understand CSS</span></span>   

<span data-ttu-id="c3fd9-156">**CSS** es un lenguaje de equipos que determina el diseño y el estilo de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-156">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="c3fd9-157">Por ejemplo, a continuación se muestra un párrafo con un borde:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-157">For example, here is a paragraph with a border:</span></span>  

> ##### <span data-ttu-id="c3fd9-158">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="c3fd9-158">Figure 6</span></span>  
> <span data-ttu-id="c3fd9-159">Esto se ha aplicado con estilo CSS</span><span class="sxs-lookup"><span data-stu-id="c3fd9-159">This has been styled with CSS</span></span>  
> ![Esto se ha aplicado con estilo CSS][ImageCssStyled]  

<span data-ttu-id="c3fd9-161">Este es el código HTML y CSS usado para crear ese párrafo:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-161">Here is the HTML and CSS code used to create that paragraph:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="c3fd9-162">probablemente te parezcan.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-162">probably looks new to you.</span></span>  <span data-ttu-id="c3fd9-163">El resto debería ser familiar.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-163">The rest should look familiar.</span></span>  <span data-ttu-id="c3fd9-164">Si no es así, completa introducción [a HTML y al Dom][DevToolsBeginnersHtml] antes de intentar este tutorial.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-164">If not, complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] before attempting this tutorial.</span></span>  

## <span data-ttu-id="c3fd9-165">Agregar estilos en línea</span><span class="sxs-lookup"><span data-stu-id="c3fd9-165">Add inline styles</span></span>   

<span data-ttu-id="c3fd9-166">Use **estilos en línea** cuando desee aplicar estilos a un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-166">Use **inline styles** when you want to apply styles to a single element.</span></span>  <span data-ttu-id="c3fd9-167">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-167">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-168">Vuelva a la pestaña edición y Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-168">Go back to the editing tab and open `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-169">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="c3fd9-169">Figure 7</span></span>  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  <span data-ttu-id="c3fd9-171">Añadir `style="background-color: aliceblue;"` a tu `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-171">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="c3fd9-172">En el bloque de código siguiente, la cuarta línea de código es la que tiene que cambiar.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-172">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="c3fd9-173">El resto es solo allí para que puedas asegurarte de que el nuevo código está en el lugar correcto.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-173">The rest is just there so you can be sure that you're putting the new code in the right place.</span></span>  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  <span data-ttu-id="c3fd9-174">Vaya a la **pestaña en vivo** para ver los cambios.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-174">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="c3fd9-175">El fondo de la `<nav>` sección ahora es azul.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-175">The background of the `<nav>` section is now blue.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-176">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="c3fd9-176">Figure 8</span></span>  
    > <span data-ttu-id="c3fd9-177">El color de fondo de la Página principal y los vínculos de contacto ahora es azul</span><span class="sxs-lookup"><span data-stu-id="c3fd9-177">The background color behind the Home and Contact links is now blue</span></span>  
    > ![El color de fondo de la Página principal y los vínculos de contacto ahora es azul][ImageCssInline2]  

## <span data-ttu-id="c3fd9-179">Volver a usar estilos en una sola página con hojas de estilo internas</span><span class="sxs-lookup"><span data-stu-id="c3fd9-179">Re-use styles on a single page with internal stylesheets</span></span>   

<span data-ttu-id="c3fd9-180">Anteriormente, vimos un estilo en línea que aplicaba un estilo a una sola `<p>` etiqueta como esta:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-180">Earlier, you saw an inline style that applied a style to a single `<p>` tag like this:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="c3fd9-181">¿Qué ocurre si desea que todos los `<p>` elementos de la página web tengan el mismo estilo?</span><span class="sxs-lookup"><span data-stu-id="c3fd9-181">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="c3fd9-182">Tendría que copiar y pegar el código en cada `<p>` etiqueta del sitio.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-182">You'd have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="c3fd9-183">Eso es mucho tiempo y esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-183">That's a lot of time and effort.</span></span>  <span data-ttu-id="c3fd9-184">Y, si necesitara realizar una edición, deberás volver a cambiar todas las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-184">And, if you needed to make an edit, you'd have to change every tag again.</span></span>  <span data-ttu-id="c3fd9-185">Las **hojas de estilos internas** permiten escribir una CSS una vez para que se aplique a varios elementos.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-185">**Internal stylesheets** allow you to write your CSS once so that it applies to multiple elements.</span></span>  <span data-ttu-id="c3fd9-186">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-186">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-187">En la ficha en vivo, haga clic en **contacto** para ir a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-187">In the live tab, click **Contact** to go to the contact page.</span></span>  <span data-ttu-id="c3fd9-188">Observe la fuente de **Inicio** y de **contacto**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-188">Notice the font of **Home** and **Contact**.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-189">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="c3fd9-189">Figure 9</span></span>  
    > <span data-ttu-id="c3fd9-190">La página de contacto</span><span class="sxs-lookup"><span data-stu-id="c3fd9-190">The Contact page</span></span>  
    > ![La página de contacto][ImageCssInternal1]  

1.  <span data-ttu-id="c3fd9-192">En la **pestaña Editor**, vaya a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-192">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="c3fd9-193">Agregue el código siguiente a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-193">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="c3fd9-194">Recuerde que las líneas que comienzan con `<style>` y terminan con `</style>` son lo que necesita sumar.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-194">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="c3fd9-195">El otro código está allí para que sepa dónde colocar el nuevo código.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-195">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="c3fd9-196">Volver a la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-196">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="c3fd9-197">Haga clic en **contacto** para volver a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-197">Click **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="c3fd9-198">La fuente de **Inicio** y de **contacto** ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-198">The font of **Home** and **Contact** has changed.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-199">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="c3fd9-199">Figure 10</span></span>  
    > <span data-ttu-id="c3fd9-200">La fuente de los vínculos de contactos y de inicio ha cambiado</span><span class="sxs-lookup"><span data-stu-id="c3fd9-200">The font of the Home and Contact links has changed</span></span>  
    > ![La fuente de los vínculos de contactos y de inicio ha cambiado][ImageCssInternal2]  
    
### <span data-ttu-id="c3fd9-202">Comprender las hojas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="c3fd9-202">Understand internal stylesheets</span></span>   

<span data-ttu-id="c3fd9-203">Las hojas de estilo internas aplican estilos mediante **selectores**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-203">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="c3fd9-204">Los selectores son patrones que pueden aplicarse a uno o varios elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-204">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="c3fd9-205">Por ejemplo, en el código anterior:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-205">For example, in the previous code:</span></span>  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` <span data-ttu-id="c3fd9-206">es un selector que se traduce en "any `<li>` que contiene un `<a>` ".</span><span class="sxs-lookup"><span data-stu-id="c3fd9-206">is a selector that translates to "any `<li>` that contains an `<a>`".</span></span>  <span data-ttu-id="c3fd9-207">El explorador cambia la fuente de los vínculos de **contactos** y de **Inicio** porque coinciden con este patrón.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-207">The browser changes the font of the **Home** and **Contact** links because they match this pattern.</span></span>  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="c3fd9-208">es una **declaración**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-208">is a **declaration**.</span></span>  <span data-ttu-id="c3fd9-209">Una declaración consta de dos partes: una **propiedad** y un **valor**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-209">A declaration is made of two parts: a **property** and a **value**.</span></span>  `font-family` <span data-ttu-id="c3fd9-210">es la propiedad y `'Courier New', Courier, serif` es el valor de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-210">is the property, and `'Courier New', Courier, serif` is the value of that property.</span></span>  <span data-ttu-id="c3fd9-211">La propiedad describe una forma general de cambiar el estilo del elemento y el valor indica qué debe cambiar exactamente.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-211">The property describes a general way that you can change the element's style, and the value says how exactly it should change.</span></span>  <span data-ttu-id="c3fd9-212">Por ejemplo, `font-family: 'Courier New', Courier, serif` ofrece al explorador estas instrucciones: "establecer la fuente de los elementos que coinciden con el patrón `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-212">For example, `font-family: 'Courier New', Courier, serif` gives the browser this instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="c3fd9-213">Si la fuente no está disponible, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-213">If that font isn't available, use `Courier`.</span></span>  <span data-ttu-id="c3fd9-214">Si no está disponible, use `serif` ".</span><span class="sxs-lookup"><span data-stu-id="c3fd9-214">If that isn't available, use `serif`."</span></span>  

### <span data-ttu-id="c3fd9-215">Agregar varios selectores a un conjunto de reglas</span><span class="sxs-lookup"><span data-stu-id="c3fd9-215">Add multiple selectors to a ruleset</span></span>   

<span data-ttu-id="c3fd9-216">Un conjunto de códigos CSS, como el que se muestra a continuación, se denomina conjunto de **reglas**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-216">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="c3fd9-217">Use comas para agregar varios selectores a un conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-217">Use commas to add multiple selectors to a ruleset.</span></span>  <span data-ttu-id="c3fd9-218">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-218">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-219">En la **pestaña Editor**, Abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-219">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="c3fd9-220">Después del `li a` tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-220">After `li a` type `, h1`.</span></span>  

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

    <span data-ttu-id="c3fd9-221">Esto indica al explorador que debe aplicar estilo a los `<h1>` elementos de la misma manera en que estilos de los elementos que coinciden con el patrón `li a` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-221">This tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="c3fd9-222">Ir a la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-222">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="c3fd9-223">Haga clic en el vínculo de **contacto** para volver a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-223">Click the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="c3fd9-224">Ahora, **póngase en contacto conmigo.**</span><span class="sxs-lookup"><span data-stu-id="c3fd9-224">Now, **Contact Me!**</span></span> <span data-ttu-id="c3fd9-225">tiene la misma fuente que los vínculos de navegación.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-225">has the same font as the navigation links.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-226">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="c3fd9-226">Figure 11</span></span>  
    > <span data-ttu-id="c3fd9-227">El texto ' contactme! '</span><span class="sxs-lookup"><span data-stu-id="c3fd9-227">The text 'Contact Me!'</span></span> <span data-ttu-id="c3fd9-228">ahora tiene la misma fuente que los vínculos de contactos y de inicio</span><span class="sxs-lookup"><span data-stu-id="c3fd9-228">now has the same font as the Home and Contact links</span></span>  
    > ![El texto contactar conmigo.][ImageCssMultiple1]  

## <span data-ttu-id="c3fd9-231">Experimentar con DevTools</span><span class="sxs-lookup"><span data-stu-id="c3fd9-231">Experiment with DevTools</span></span>   

<span data-ttu-id="c3fd9-232">Mientras continúa con el desarrollo web maestro, encontrarás que CSS puede ser complicado.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-232">As you continue your journey to master web development, you'll find that CSS can be tricky.</span></span>  <span data-ttu-id="c3fd9-233">Escribirás algunas CSS y esperamos que se muestre de una forma, pero el explorador hace algo totalmente diferente.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-233">You'll write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="c3fd9-234">Con Microsoft Edge DevTools es fácil experimentar con los cambios y ver inmediatamente cómo afectan esos cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-234">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how those changes affect the page.</span></span>  

### <span data-ttu-id="c3fd9-235">Agregar una declaración a un Ruler existente en DevTools</span><span class="sxs-lookup"><span data-stu-id="c3fd9-235">Add a declaration to an existing rulest in DevTools</span></span>   

<span data-ttu-id="c3fd9-236">Cuando desee iterar en el estilo de un elemento existente, agregue una declaración a un conjunto de reglas existente.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-236">When you want to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  <span data-ttu-id="c3fd9-237">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-237">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-238">Haga clic con el botón derecho en el vínculo **Inicio** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-238">Right-click the **Home** link and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-239">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="c3fd9-239">Figure 12</span></span>  
    > <span data-ttu-id="c3fd9-240">Inspeccionar el vínculo Inicio</span><span class="sxs-lookup"><span data-stu-id="c3fd9-240">Inspecting the Home link</span></span>  
    > ![Inspeccionar el vínculo Inicio][ImageCssAdd1]  
    
    <span data-ttu-id="c3fd9-242">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-242">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="c3fd9-243">El código que representa el vínculo de inicio, `<a href="/">Home</a>` está resaltado en azul en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-243">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="c3fd9-244">Debe estar familiarizado [con la introducción a HTML y el Dom][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="c3fd9-244">This should be familiar from [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>  <span data-ttu-id="c3fd9-245">En la pestaña **estilos** , debajo del árbol DOM puede ver la `font-family: 'Courier New', Courier, serif` declaración que agregó a la `contact.html` anterior.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-245">In the **Styles** tab below the DOM Tree you can see the `font-family: 'Courier New', Courier, serif` declaration that you added to `contact.html` earlier.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-246">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="c3fd9-246">Figure 13</span></span>  
    > <span data-ttu-id="c3fd9-247">La pestaña estilos está debajo del árbol DOM</span><span class="sxs-lookup"><span data-stu-id="c3fd9-247">The Styles tab is below the DOM Tree</span></span>  
    > ![La pestaña estilos está debajo del árbol DOM][ImageCssAdd2]  
    
    <span data-ttu-id="c3fd9-249">Si la ventana de DevTools es ancha, la pestaña estilos está a la derecha del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-249">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-250">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="c3fd9-250">Figure 14</span></span>  
    > <span data-ttu-id="c3fd9-251">La pestaña estilos está a la derecha del árbol DOM</span><span class="sxs-lookup"><span data-stu-id="c3fd9-251">The Styles tab is to the right of the DOM Tree</span></span>  
    > ![La pestaña estilos está a la derecha del árbol DOM][ImageCssAdd3]  
    
1.  <span data-ttu-id="c3fd9-253">Haga clic en el espacio en blanco a continuación `font-family: 'Courier New', Courier, Serif` para agregar una declaración nueva.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-253">Click the whitespace below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-254">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="c3fd9-254">Figure 15</span></span>  
    > <span data-ttu-id="c3fd9-255">Agregar una declaración nueva</span><span class="sxs-lookup"><span data-stu-id="c3fd9-255">Adding a new declaration</span></span>  
    > ![Agregar una declaración nueva][ImageCssAdd4]  
    
1.  <span data-ttu-id="c3fd9-257">Escriba `color` y, a continuación, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-257">Type `color` and then press `Enter`.</span></span>  <span data-ttu-id="c3fd9-258">La interfaz de usuario de autocompletar sugiere opciones mientras escribe.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-258">The autocomplete UI suggests options as you type.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-259">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="c3fd9-259">Figure 16</span></span>  
    > <span data-ttu-id="c3fd9-260">Escritura</span><span class="sxs-lookup"><span data-stu-id="c3fd9-260">Typing</span></span> `color`  
    > ![Color de escritura][ImageCssAdd5]  

1.  <span data-ttu-id="c3fd9-262">Escriba `magenta` y, a continuación, `Enter` vuelva a presionar.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-262">Type `magenta` and then press `Enter` again.</span></span>  <span data-ttu-id="c3fd9-263">Todo el texto de la página de contacto ahora es magenta.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-263">All of the text on the contact page is now magenta.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-264">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="c3fd9-264">Figure 17</span></span>  
    > <span data-ttu-id="c3fd9-265">Escritura</span><span class="sxs-lookup"><span data-stu-id="c3fd9-265">Typing</span></span> `magenta`  
    > ![Escribir magenta][ImageCssAdd6]  
    
### <span data-ttu-id="c3fd9-267">Editar una declaración en DevTools</span><span class="sxs-lookup"><span data-stu-id="c3fd9-267">Edit a declaration in DevTools</span></span>   

<span data-ttu-id="c3fd9-268">También puede editar las declaraciones existentes en DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-268">You can also edit existing declarations in DevTools.</span></span>  <span data-ttu-id="c3fd9-269">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-269">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-270">Haga clic en el cuadrado magenta junto a `magenta` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-270">Click the magenta square next to `magenta`.</span></span>  <span data-ttu-id="c3fd9-271">Aparece un selector de color.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-271">A color picker pops up.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-272">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="c3fd9-272">Figure 18</span></span>  
    > <span data-ttu-id="c3fd9-273">El selector de colores</span><span class="sxs-lookup"><span data-stu-id="c3fd9-273">The Color Picker</span></span>  
    > ![El selector de colores][ImageCssEdit1]  
    
1.  <span data-ttu-id="c3fd9-275">Use el selector de colores para cambiar el texto de la fuente a un color que le guste.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-275">Use the color picker to change the font text to a color that you like.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-276">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="c3fd9-276">Figure 19</span></span>  
    > <span data-ttu-id="c3fd9-277">Cambiar el color de la fuente a púrpura con el selector de colores</span><span class="sxs-lookup"><span data-stu-id="c3fd9-277">Changing the font color to purple with the Color Picker</span></span>  
    > ![Cambiar el color de la fuente a púrpura con el selector de colores][ImageCssEdit2]  

### <span data-ttu-id="c3fd9-279">Agregar un nuevo conjunto de reglas en DevTools</span><span class="sxs-lookup"><span data-stu-id="c3fd9-279">Add a new ruleset in DevTools</span></span>   

<span data-ttu-id="c3fd9-280">También puede agregar nuevos conjuntos de conjuntos en DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-280">You can also add new rulesets in DevTools.</span></span>  <span data-ttu-id="c3fd9-281">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-281">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-282">Haga clic en **nueva regla de estilo** ![ nueva regla ][ImageNewStyleRuleIcon] de estilo que está junto a **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-282">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] which is next to **.cls**.</span></span>  <span data-ttu-id="c3fd9-283">Aparece un conjunto de reglas vacío con `a` el selector.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-283">An empty ruleset appears with `a` as the selector.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-284">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="c3fd9-284">Figure 20</span></span>  
    > <span data-ttu-id="c3fd9-285">Agregar una nueva regla</span><span class="sxs-lookup"><span data-stu-id="c3fd9-285">Adding a new rule</span></span>  
    > ![Agregar una nueva regla][ImageCssRule1]  
    
1.  <span data-ttu-id="c3fd9-287">Reemplazar `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-287">Replace `a` with `a:hover`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-288">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="c3fd9-288">Figure 21</span></span>  
    > <span data-ttu-id="c3fd9-289">Reemplazar `a` por</span><span class="sxs-lookup"><span data-stu-id="c3fd9-289">Replacing `a` with</span></span> `a:hover`  
    > ![Reemplazar un con a:hover][ImageCssRule2]  
    
    `:hover` <span data-ttu-id="c3fd9-291">es una **seudoclase**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-291">is a **pseudo-class**.</span></span>  <span data-ttu-id="c3fd9-292">Use las pseudo-clases para aplicar estilo a los elementos cuando entran en Estados especiales.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-292">Use pseudo-classes to style elements when they enter special states.</span></span>  <span data-ttu-id="c3fd9-293">Por ejemplo, el `a:hover` estilo solo surte efecto cuando se coloca el puntero sobre un `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-293">For example, the `a:hover` style only takes effect when you're hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="c3fd9-294">Haga clic entre los corchetes para agregar una declaración nueva.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-294">Click between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="c3fd9-295">Escriba `background-color` el nombre de la declaración y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-295">Type `background-color` for the declaration name and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-296">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="c3fd9-296">Figure 22</span></span>  
    > <span data-ttu-id="c3fd9-297">Escritura</span><span class="sxs-lookup"><span data-stu-id="c3fd9-297">Typing</span></span> `background-color`  
    > ![Escribir el color de fondo][ImageCssRule3]  
    
1.  <span data-ttu-id="c3fd9-299">Escriba `green` el valor de la declaración y, a continuación, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-299">Type `green` for the declaration value and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-300">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="c3fd9-300">Figure 23</span></span>  
    > <span data-ttu-id="c3fd9-301">Escritura</span><span class="sxs-lookup"><span data-stu-id="c3fd9-301">Typing</span></span> `green`  
    > ![Escritura de color verde][ImageCssRule4]  
    
1.  <span data-ttu-id="c3fd9-303">Mantenga el mouse sobre el vínculo **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-303">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="c3fd9-304">El fondo del vínculo se vuelve de color verde.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-304">The background of the link turns green.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-305">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="c3fd9-305">Figure 24</span></span>  
    > <span data-ttu-id="c3fd9-306">Situar el puntero sobre el vínculo de inicio para mostrar su fondo verde</span><span class="sxs-lookup"><span data-stu-id="c3fd9-306">Hovering over the Home link to reveal its green background</span></span>  
    > ![Situar el puntero sobre el vínculo de inicio para mostrar su fondo verde][ImageCssRule5]  
    
## <span data-ttu-id="c3fd9-308">Volver a usar estilos entre páginas con hojas de estilo externas</span><span class="sxs-lookup"><span data-stu-id="c3fd9-308">Re-use styles across pages with external stylesheets</span></span>   

<span data-ttu-id="c3fd9-309">Anteriormente, agregó esta hoja de estilos interna a `contact.html` :</span><span class="sxs-lookup"><span data-stu-id="c3fd9-309">Earlier you added this internal stylesheet to `contact.html`:</span></span>  

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

<span data-ttu-id="c3fd9-310">¿Qué sucede si desea aplicar estilo `index.html` de la misma manera?</span><span class="sxs-lookup"><span data-stu-id="c3fd9-310">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="c3fd9-311">¿Qué sucede si tenía *miles* de páginas y desea aplicar estos estilos a todas?</span><span class="sxs-lookup"><span data-stu-id="c3fd9-311">What if you had a *thousand* pages and you wanted to apply these styles to all of them?</span></span>  <span data-ttu-id="c3fd9-312">Tendría que copiar y pegar esta hoja de estilos interna en todas las páginas web del sitio.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-312">You'd have to copy and paste this internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="c3fd9-313">Las **hojas de estilo externas** le permiten escribir la CSS una vez, la aplica a varias páginas.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-313">**External stylesheets** allow you to write your CSS once yet apply it to multiple pages.</span></span>  <span data-ttu-id="c3fd9-314">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-314">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-315">En primer lugar, vuelva a cargar la ficha en vivo para quitar los cambios que realizó en DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-315">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-316">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="c3fd9-316">Figure 25</span></span>  
    >  <span data-ttu-id="c3fd9-317">Después de volver a cargar la página, los cambios realizados en DevTools desaparecen</span><span class="sxs-lookup"><span data-stu-id="c3fd9-317">After reloading the page the changes that were made in DevTools are gone</span></span>  
    > ![ <span data-ttu-id="c3fd9-318">Después de volver a cargar la página, los cambios realizados en DevTools desaparecen</span><span class="sxs-lookup"><span data-stu-id="c3fd9-318">After reloading the page the changes that were made in DevTools are gone</span></span>][ImageCssExternal01]  
    
1.  <span data-ttu-id="c3fd9-319">Vuelva a la **pestaña Editor** y Abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-319">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-320">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="c3fd9-320">Figure 26</span></span>  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  <span data-ttu-id="c3fd9-322">Elimine todo lo que hay entre `<style>` y `</style>` , incluidos `<style>` y `</style>` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-322">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-323">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="c3fd9-323">Figure 27</span></span>  
    > <span data-ttu-id="c3fd9-324">Se ha quitado la etiqueta de estilo</span><span class="sxs-lookup"><span data-stu-id="c3fd9-324">The style tag has been removed</span></span>  
    > ![Se ha quitado la etiqueta de estilo][ImageCssExternal03]  
    
1.  <span data-ttu-id="c3fd9-326">Ir a `index.html` y quitar `style="background-color: aliceblue;"` de la `<nav>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-326">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="c3fd9-327">Ahora ha quitado todas las CSS que agregó previamente a su sitio.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-327">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-328">Ilustración 28</span><span class="sxs-lookup"><span data-stu-id="c3fd9-328">Figure 28</span></span>  
    > <span data-ttu-id="c3fd9-329">El estilo insertado se ha quitado del elemento NAV</span><span class="sxs-lookup"><span data-stu-id="c3fd9-329">The inline style has been removed from the nav element</span></span>  
    > ![El estilo insertado se ha quitado del elemento NAV][ImageCssExternal04]  

1.  <span data-ttu-id="c3fd9-331">Haga clic en **nuevo archivo**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-331">Click **New File**.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-332">Ilustración 29</span><span class="sxs-lookup"><span data-stu-id="c3fd9-332">Figure 29</span></span>  
    > <span data-ttu-id="c3fd9-333">El cuadro de diálogo nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="c3fd9-333">The new file dialog</span></span>  
    > ![El cuadro de diálogo nuevo archivo][ImageCssExternal05]  
    
1.  <span data-ttu-id="c3fd9-335">Reemplazar `cool-file.js` por `style.css` y, a continuación, haga clic en **Agregar archivo**.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-335">Replace `cool-file.js` with `style.css` and then click **Add File**.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-336">Ilustración 30</span><span class="sxs-lookup"><span data-stu-id="c3fd9-336">Figure 30</span></span>  
    > <span data-ttu-id="c3fd9-337">Escritura</span><span class="sxs-lookup"><span data-stu-id="c3fd9-337">Typing</span></span> `style.css`  
    > ![Escribir Style. CSS][ImageCssExternal06]  
    
1.  <span data-ttu-id="c3fd9-339">Pega este código en `style.css` :</span><span class="sxs-lookup"><span data-stu-id="c3fd9-339">Paste this code into `style.css`:</span></span>  
    
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
    
    > ##### <span data-ttu-id="c3fd9-340">Ilustración 31</span><span class="sxs-lookup"><span data-stu-id="c3fd9-340">Figure 31</span></span>  
    > <span data-ttu-id="c3fd9-341">Agregar código a</span><span class="sxs-lookup"><span data-stu-id="c3fd9-341">Adding code to</span></span> `style.css`  
    > ![Agregar código a Style. CSS][ImageCssExternal07]  
    
    <span data-ttu-id="c3fd9-343">En este momento, ha creado una hoja de estilos externa, pero el código HTML no sabe que ya existe.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-343">At this point, you have created an external stylesheet, but your HTML doesn't know that it exists, yet.</span></span>  
    
1.  <span data-ttu-id="c3fd9-344">Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-344">Open `index.html`.</span></span>  
1.  <span data-ttu-id="c3fd9-345">Agrega `<link rel="stylesheet" href="style.css">` a tu HTML.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-345">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### <span data-ttu-id="c3fd9-346">Ilustración 32</span><span class="sxs-lookup"><span data-stu-id="c3fd9-346">Figure 32</span></span>  
    > <span data-ttu-id="c3fd9-347">Vincular a</span><span class="sxs-lookup"><span data-stu-id="c3fd9-347">Linking to</span></span> `style.css`  
    > ![Vincular a Style. CSS][ImageCssExternal08]  

1.  <span data-ttu-id="c3fd9-349">Vaya a `contact.html` y agregue el vínculo allí.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-349">Go to `contact.html` and add the link there, too.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-350">Ilustración 33</span><span class="sxs-lookup"><span data-stu-id="c3fd9-350">Figure 33</span></span>  
    > <span data-ttu-id="c3fd9-351">Vincular a `style.css` en</span><span class="sxs-lookup"><span data-stu-id="c3fd9-351">Linking to `style.css` in</span></span> `contact.html`  
    > ![Vincular a Style. CSS en contact.html][ImageCssExternal09]  

1.  <span data-ttu-id="c3fd9-353">Ir a la **ficha en vivo**.  La Página principal ahora tiene la misma fuente de la última sección y una sección de navegación azul.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-353">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-354">Ilustración 34</span><span class="sxs-lookup"><span data-stu-id="c3fd9-354">Figure 34</span></span>  
    > <span data-ttu-id="c3fd9-355">La Página principal</span><span class="sxs-lookup"><span data-stu-id="c3fd9-355">The home page</span></span>  
    > ![La Página principal][ImageCssExternal10]  
    
1.  <span data-ttu-id="c3fd9-357">Haga clic en el vínculo de **contacto** para ir a la página de contacto.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-357">Click the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="c3fd9-358">La página de contacto tiene el mismo formato que la Página principal.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-358">The contact page has the same formatting as the home page.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-359">Ilustración 35</span><span class="sxs-lookup"><span data-stu-id="c3fd9-359">Figure 35</span></span>  
    > <span data-ttu-id="c3fd9-360">La página de contacto</span><span class="sxs-lookup"><span data-stu-id="c3fd9-360">The contact page</span></span>  
    > ![La página de contacto][ImageCssExternal11]  
    
## <span data-ttu-id="c3fd9-362">Usar un marco CSS</span><span class="sxs-lookup"><span data-stu-id="c3fd9-362">Use a CSS framework</span></span>   

<span data-ttu-id="c3fd9-363">Los **Marcos CSS** son colecciones de estilos creados por otros programadores que facilitan la creación de atractivos sitios Web.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-363">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="c3fd9-364">En lugar de definir estilos usted mismo, un marco de trabajo le proporciona una colección de estilos que puede usar en los elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-364">Instead of defining styles yourself, a framework gives you a collection of styles that you can use on your page elements.</span></span>  

1.  <span data-ttu-id="c3fd9-365">Copie el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-365">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="c3fd9-366">Vaya a la pestaña edición y pegue el código en `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-366">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-367">Ilustración 36</span><span class="sxs-lookup"><span data-stu-id="c3fd9-367">Figure 36</span></span>  
    > <span data-ttu-id="c3fd9-368">Vinculación a Framework en</span><span class="sxs-lookup"><span data-stu-id="c3fd9-368">Linking to the framework in</span></span> `contact.html`  
    > ![Vinculación al marco en contact.html][ImageCssFramework1]  
    
1.  <span data-ttu-id="c3fd9-370">Pega también el código `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-370">Paste the code into `index.html`, as well.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-371">Ilustración 37</span><span class="sxs-lookup"><span data-stu-id="c3fd9-371">Figure 37</span></span>  
    > <span data-ttu-id="c3fd9-372">Vinculación a Framework en</span><span class="sxs-lookup"><span data-stu-id="c3fd9-372">Linking to the framework in</span></span> `index.html`  
    > ![Vinculación al marco en index.html][ImageCssFramework2]  
    
1.  <span data-ttu-id="c3fd9-374">Vuelva a la pestaña en vivo para ver los cambios.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-374">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="c3fd9-375">Aunque el color de fondo del `<nav>` y de la fuente de los `li a` elementos es el mismo, la fuente de los demás elementos ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-375">While the background color of the `<nav>` and the font of the `li a` elements are the same, the font of the other elements has changed.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-376">Ilustración 38</span><span class="sxs-lookup"><span data-stu-id="c3fd9-376">Figure 38</span></span>  
    > <span data-ttu-id="c3fd9-377">Algunas de las fuentes de la Página principal han cambiado debido al marco de trabajo</span><span class="sxs-lookup"><span data-stu-id="c3fd9-377">Some of the font on the home page has changed because of the framework</span></span>  
    > ![Algunas de las fuentes de la Página principal han cambiado debido al marco de trabajo][ImageCssFramework3]  

### <span data-ttu-id="c3fd9-379">Usar una clase</span><span class="sxs-lookup"><span data-stu-id="c3fd9-379">Use a class</span></span>   

<span data-ttu-id="c3fd9-380">En la última sección, agregó bootstrap a sus páginas web, que cambió las fuentes de algunos de los elementos de su sitio.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-380">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="c3fd9-381">Los marcos CSS pueden ayudarle a hacer cambios importantes en la página con muy poco código.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-381">CSS frameworks can help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="c3fd9-382">Pruébelo ahora cambiando el encabezado:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-382">Try it now by changing your header:</span></span>  

1.  <span data-ttu-id="c3fd9-383">Copia este código:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-383">Copy this code:</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="c3fd9-384">Agrega este código a tu `<header>` etiqueta en `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-384">Add this code to your `<header>` tag in `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-385">Ilustración 39</span><span class="sxs-lookup"><span data-stu-id="c3fd9-385">Figure 39</span></span>  
    > <span data-ttu-id="c3fd9-386">Agregar clases en</span><span class="sxs-lookup"><span data-stu-id="c3fd9-386">Adding classes in</span></span> `index.html`  
    > ![Agregar clases en index.html][ImageCssJumbotron1]  
    
1.  <span data-ttu-id="c3fd9-388">También puedes agregar el código a la `<header>` etiqueta `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-388">Add the code to your `<header>` tag in `contact.html`, too.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-389">Ilustración 40</span><span class="sxs-lookup"><span data-stu-id="c3fd9-389">Figure 40</span></span>  
    > <span data-ttu-id="c3fd9-390">Agregar clases en</span><span class="sxs-lookup"><span data-stu-id="c3fd9-390">Adding classes in</span></span> `contact.html`  
    > ![Agregar clases en contact.html][ImageCssJumbotron2]  
    
1.  <span data-ttu-id="c3fd9-392">Ver los cambios en la ficha en vivo.  Ahora hay un gran cuadro gris en la parte de tu encabezado.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-392">View your changes in the live tab.  There's a big, grey box around your header now.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-393">Ilustración 41</span><span class="sxs-lookup"><span data-stu-id="c3fd9-393">Figure 41</span></span>  
    > <span data-ttu-id="c3fd9-394">El encabezado ahora tiene un gran cuadro gris a su lado</span><span class="sxs-lookup"><span data-stu-id="c3fd9-394">The header now has a big, grey box around it</span></span>  
    > ![El encabezado ahora tiene un gran cuadro gris a su lado][ImageCssJumbotron3]  
    
### <span data-ttu-id="c3fd9-396">Comprender las clases</span><span class="sxs-lookup"><span data-stu-id="c3fd9-396">Understand classes</span></span>   

<span data-ttu-id="c3fd9-397">Las clases permiten asignar colecciones de estilos a elementos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-397">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="c3fd9-398">Por ejemplo, establecer el `class` atributo de las `<header>` etiquetas para `jumbotron` aplicar los estilos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-398">For example, setting the `class` attribute of the `<header>` tags to `jumbotron` applied the following styles to them:</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="c3fd9-399">Una ventaja de las clases es que permiten aplicar estilos a cualquier elemento que desee.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-399">One advantage of classes is that they let you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="c3fd9-400">Por ejemplo, suponga que desea establecer el color de fondo de *algunos* `<p>` elementos en púrpura, pero no en *todos* .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-400">For example, suppose you want to set the background color of *some* `<p>` elements to purple, but not *all* of them.</span></span>  <span data-ttu-id="c3fd9-401">Puede definir el estilo en una clase:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-401">You could define the style in a class:</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="c3fd9-402">Y, a continuación, aplique la clase solo a los `<p>` elementos a los que quiere aplicar un estilo:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-402">And then apply the class to only the `<p>` elements that you want to style:</span></span>  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### <span data-ttu-id="c3fd9-403">Alinear elementos</span><span class="sxs-lookup"><span data-stu-id="c3fd9-403">Align elements</span></span>   

<span data-ttu-id="c3fd9-404">Bootstrap también proporciona clases para alinear elementos.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-404">Bootstrap also provides classes for aligning elements.</span></span>  <span data-ttu-id="c3fd9-405">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="c3fd9-405">Try it now:</span></span>  

1.  <span data-ttu-id="c3fd9-406">Vuelva a la pestaña Editor y Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-406">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="c3fd9-407">Agregar `class="container-fluid"` a la `<body>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-407">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-408">Ilustración 42</span><span class="sxs-lookup"><span data-stu-id="c3fd9-408">Figure 42</span></span>  
    > <span data-ttu-id="c3fd9-409">Agregar la `container-fluid` clase</span><span class="sxs-lookup"><span data-stu-id="c3fd9-409">Adding the `container-fluid` class</span></span>  
    > ![Agregar la clase de fluidos contenedor][ImageCssAlign1]  

1.  <span data-ttu-id="c3fd9-411">Ajustar los `<nav>` `<main>` elementos y en `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="c3fd9-411">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="c3fd9-412">Asegúrate `</div>` de poner después `</main>` para cerrar correctamente la nueva etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-412">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-413">Ilustración 43</span><span class="sxs-lookup"><span data-stu-id="c3fd9-413">Figure 43</span></span>  
    > <span data-ttu-id="c3fd9-414">Agregar una fila</span><span class="sxs-lookup"><span data-stu-id="c3fd9-414">Adding a row</span></span>  
    > ![Agregar una fila][ImageCssAlign2]  
    
1.  <span data-ttu-id="c3fd9-416">Agregar `class="col-3"` a la `<nav>` etiqueta y `class="col-9"` a la `<main>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-416">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-417">Ilustración 44</span><span class="sxs-lookup"><span data-stu-id="c3fd9-417">Figure 44</span></span>  
    > <span data-ttu-id="c3fd9-418">Agregar las `col-3` `col-9` clases y</span><span class="sxs-lookup"><span data-stu-id="c3fd9-418">Adding the `col-3` and `col-9` classes</span></span>  
    > ![Agregar las clases col-3 y col-9][ImageCssAlign3]  
    
1.  <span data-ttu-id="c3fd9-420">Ver los cambios en la ficha en vivo.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-420">View your changes in the live tab.</span></span>  
    
    > ##### <span data-ttu-id="c3fd9-421">Ilustración 45</span><span class="sxs-lookup"><span data-stu-id="c3fd9-421">Figure 45</span></span>  
    > <span data-ttu-id="c3fd9-422">Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-422">The nav content is now to the left of the main content</span></span>  
    > ![Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal.][ImageCssAlign4]  
    
## <span data-ttu-id="c3fd9-424">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="c3fd9-424">Next steps</span></span>   

<span data-ttu-id="c3fd9-425">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="c3fd9-425">Congratulations!</span></span>  <span data-ttu-id="c3fd9-426">¡Has terminado!</span><span class="sxs-lookup"><span data-stu-id="c3fd9-426">You're done!</span></span>  

*   <span data-ttu-id="c3fd9-427">La mejor manera de mejorar el desarrollo web es crear más sitios.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-427">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="c3fd9-428">No te preocupes por la rotura de cosas.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-428">Don't worry about breaking stuff.</span></span>  <span data-ttu-id="c3fd9-429">Divertirte y aprender todo lo que puedes a lo largo del camino.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-429">Just have fun and learn as much as you can along the way.</span></span>  
*   <span data-ttu-id="c3fd9-430">Consulte [Introducción a CSS][MDNCssFirstSteps] para obtener más información sobre cómo aplicar estilos a páginas Web.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-430">Check out [Introduction to CSS][MDNCssFirstSteps] to learn lots more about styling web pages.</span></span>  
*   <span data-ttu-id="c3fd9-431">Siga nuestros tutoriales Introducción a la [visualización y el cambio de CSS][DevtoolsCssIndex] para obtener más información sobre cómo puede usar DevTools para experimentar con la CSS de una página.</span><span class="sxs-lookup"><span data-stu-id="c3fd9-431">Work through our [Get Started with Viewing and Changing CSS][DevtoolsCssIndex] tutorial to learn more about how you can use DevTools to experiment with a page's CSS.</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Ilustración 1: el aspecto de su sitio en este momento"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Ilustración 2: el aspecto que tendrá su sitio al final del tutorial"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Ilustración 3: la pestaña edición"  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Ilustración 4: el menú de opciones del proyecto"  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Ilustración 5: la ficha en vivo"  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Ilustración 6: esto se ha aplicado con estilo CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Ilustración 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Ilustración 8: el color de fondo de la Página principal y de los vínculos de contacto ahora es azul"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Ilustración 9: la página de contacto"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Ilustración 10: la fuente de los vínculos Home y Contact ha cambiado"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Ilustración 11: el texto ' contactme! ' ahora tiene la misma fuente que los vínculos Home y Contact"  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Ilustración 12: inspeccionar el vínculo de inicio"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Ilustración 13: la pestaña estilos está debajo del árbol DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Ilustración 14: la pestaña estilos está a la derecha del árbol DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Ilustración 15: agregar una declaración nueva"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Ilustración 16: escribir color"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Ilustración 17: escribir magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Ilustración 18: el selector de colores"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Ilustración 19: cambiar el color de la fuente a púrpura con el selector de colores"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Ilustración 20: agregar una nueva regla"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Ilustración 21: reemplazar un por a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Ilustración 22: escribir color de fondo"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Ilustración 23: escribir en verde"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Ilustración 24: mantener el puntero sobre el vínculo de inicio para mostrar su fondo verde"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Ilustración 25: después de volver a cargar la página, los cambios realizados en DevTools ya no están"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Ilustración 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Ilustración 27: se ha quitado la etiqueta Style"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Ilustración 28: el estilo insertado se ha quitado del elemento NAV"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Ilustración 29: el cuadro de diálogo nuevo archivo"  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Ilustración 30: escribir Style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Ilustración 31: agregar código a Style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Ilustración 32: vincular a Style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Ilustración 33: vincular a Style. CSS en contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Ilustración 34: la Página principal"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Ilustración 35: la página de contacto"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Ilustración 36: vinculación al marco en contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Ilustración 37: vinculación al marco en index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Ilustración 38: algunas de las fuentes de la Página principal han cambiado debido al marco de trabajo"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Ilustración 39: agregar clases en index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Ilustración 40: agregar clases en contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Ilustración 41: el encabezado ahora tiene un gran cuadro gris a su lado"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Ilustración 42: agregar la clase de fluidos contenedor"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Ilustración 43: agregar una fila"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Ilustración 44: agregar las clases col-3 y col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Ilustración 45: el contenido de NAV ahora está a la izquierda del contenido principal"  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools para principiantes: Introducción a HTML y el DOM"  
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cocinada-Amphibian | Intento"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeros pasos de CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="c3fd9-482">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3fd9-482">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c3fd9-483">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/css) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="c3fd9-483">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c3fd9-485">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3fd9-485">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
