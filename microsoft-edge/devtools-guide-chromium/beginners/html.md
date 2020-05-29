---
title: DevTools para principiantes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581590"
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

# <span data-ttu-id="c6506-103">DevTools para principiantes: Introducción a HTML y el DOM</span><span class="sxs-lookup"><span data-stu-id="c6506-103">DevTools for Beginners: Get Started with HTML and the DOM</span></span>   

<span data-ttu-id="c6506-104">Este es el primero de una serie de tutoriales que enseñan los conceptos básicos del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="c6506-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="c6506-105">También aprenderá un conjunto de herramientas para desarrolladores web denominado Microsoft Edge DevTools, que puede aumentar su productividad.</span><span class="sxs-lookup"><span data-stu-id="c6506-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="c6506-106">En este tutorial en particular, obtendrá información sobre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="c6506-107">HTML es una de las tecnologías básicas de desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="c6506-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="c6506-108">Es el lenguaje que controla la estructura y el contenido de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="c6506-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="c6506-109">El DOM también está relacionado con la estructura y el contenido de las páginas web, pero obtendrá más información sobre esto más adelante.</span><span class="sxs-lookup"><span data-stu-id="c6506-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="c6506-110">Principales</span><span class="sxs-lookup"><span data-stu-id="c6506-110">Goals</span></span>   

<span data-ttu-id="c6506-111">Va a aprender a usar el desarrollo web creando su propio sitio Web.</span><span class="sxs-lookup"><span data-stu-id="c6506-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="c6506-112">Cuando complete todos los tutoriales de la serie *DevTools para principiantes* , el sitio finalizado tendrá el aspecto que se muestra en la **Ilustración 1**.</span><span class="sxs-lookup"><span data-stu-id="c6506-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like **Figure 1**.</span></span>  

> ##### <span data-ttu-id="c6506-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="c6506-113">Figure 1</span></span>  
> <span data-ttu-id="c6506-114">El sitio finalizado</span><span class="sxs-lookup"><span data-stu-id="c6506-114">The finished site</span></span>  
> ![El sitio finalizado][ImageHtmlFinished]  

<span data-ttu-id="c6506-116">Al final de este tutorial, comprenderá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6506-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="c6506-117">Cómo los HTML y el DOM crean el contenido que se ve en las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="c6506-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="c6506-118">Cómo puede ayudarte Microsoft Edge DevTools a experimentar con los cambios de HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="c6506-119">La diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="c6506-120">También tendrá un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="c6506-120">You'll also have a real website!</span></span>  <span data-ttu-id="c6506-121">Puede usar este sitio para hospedar su currículum o su blog.</span><span class="sxs-lookup"><span data-stu-id="c6506-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="c6506-122">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c6506-122">Prerequisites</span></span>   

<span data-ttu-id="c6506-123">Antes de intentar este tutorial, complete los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="c6506-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="c6506-124">Si no está familiarizado con HTML, lea [Introducción a HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="c6506-124">If you're unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="c6506-125">Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="c6506-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="c6506-126">En este tutorial se usa un conjunto de herramientas de desarrollo web, denominado Microsoft Edge DevTools, que está integrado en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6506-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="c6506-127">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="c6506-127">Set up your code</span></span>   

<span data-ttu-id="c6506-128">Va a crear su sitio en un editor de código en línea denominado problema.</span><span class="sxs-lookup"><span data-stu-id="c6506-128">You're going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="c6506-129">Abra el [código fuente][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="c6506-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="c6506-130">Esta pestaña se denomina la **pestaña Editor** a lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="c6506-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    > ##### <span data-ttu-id="c6506-131">Figura 2</span><span class="sxs-lookup"><span data-stu-id="c6506-131">Figure 2</span></span>  
    > <span data-ttu-id="c6506-132">Ficha Editor</span><span class="sxs-lookup"><span data-stu-id="c6506-132">The editor tab</span></span>  
    > ![Ficha Editor][ImageHtmlSetup1]  

1.  <span data-ttu-id="c6506-134">Haga clic en **alluring-shock**.</span><span class="sxs-lookup"><span data-stu-id="c6506-134">Click **alluring-shock**.</span></span>  <span data-ttu-id="c6506-135">El menú opciones de proyecto se abre en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="c6506-135">The Project Options menu opens in the top-left corner.</span></span>  
    
    > #### <span data-ttu-id="c6506-136">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="c6506-136">Figure 3</span></span>  
    > <span data-ttu-id="c6506-137">El menú opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="c6506-137">The Project Options menu</span></span>  
    > ![El menú opciones del proyecto][ImageHtmlSetup2]  
    
1.  <span data-ttu-id="c6506-139">Haga clic en **Remix proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c6506-139">Click **Remix Project**.</span></span>  <span data-ttu-id="c6506-140">Problema crea una copia del proyecto que puede editar y genera de forma aleatoria un nombre nuevo para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="c6506-140">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="c6506-141">El contenido es el mismo que antes.</span><span class="sxs-lookup"><span data-stu-id="c6506-141">The content is the same as before.</span></span>  
    
    > ##### <span data-ttu-id="c6506-142">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="c6506-142">Figure 4</span></span>  
    > <span data-ttu-id="c6506-143">El proyecto remixto</span><span class="sxs-lookup"><span data-stu-id="c6506-143">The remixed project</span></span>  
    > ![El proyecto remixto][ImageHtmlSetup3]  
    
1.  <span data-ttu-id="c6506-145">Si planea completar el siguiente tutorial de esta serie, haga clic en **iniciar sesión** e inicie sesión en un problema con su cuenta de Github o Facebook.</span><span class="sxs-lookup"><span data-stu-id="c6506-145">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="c6506-146">Si no inicia sesión, perderá la posibilidad de editar este proyecto una vez que cierre la pestaña edición.</span><span class="sxs-lookup"><span data-stu-id="c6506-146">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="c6506-147">Haga clic en **Mostrar** y seleccione **en una ventana nueva**.</span><span class="sxs-lookup"><span data-stu-id="c6506-147">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="c6506-148">Se abre una nueva pestaña, que muestra la página en vivo.</span><span class="sxs-lookup"><span data-stu-id="c6506-148">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="c6506-149">Esta pestaña se denominará **pestaña en vivo** en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="c6506-149">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="c6506-150">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="c6506-150">Figure 5</span></span>  
    > <span data-ttu-id="c6506-151">La ficha en vivo</span><span class="sxs-lookup"><span data-stu-id="c6506-151">The live tab</span></span>  
    > ![La ficha en vivo][ImageHtmlSetup4]  
    
## <span data-ttu-id="c6506-153">Agregar contenido</span><span class="sxs-lookup"><span data-stu-id="c6506-153">Add content</span></span>   

<span data-ttu-id="c6506-154">Tu sitio está vacío.</span><span class="sxs-lookup"><span data-stu-id="c6506-154">Your site is pretty empty.</span></span>  <span data-ttu-id="c6506-155">Siga los pasos que se indican a continuación para agregar algo de contenido.</span><span class="sxs-lookup"><span data-stu-id="c6506-155">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="c6506-156">En la **pestaña Editor**, reemplace `<!-- You're "About Me" will go here.  -->` con `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="c6506-156">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="c6506-157">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="c6506-157">Figure 6</span></span>  
    > <span data-ttu-id="c6506-158">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="c6506-158">The new code is highlighted in the editor tab</span></span>  
    > ![El nuevo código está resaltado en la pestaña Editor][ImageHtmlAdd1]  
    
1.  <span data-ttu-id="c6506-160">Ver los cambios en la **ficha en vivo**.  El texto `About Me` está visible en la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-160">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="c6506-161">Es más grande que el resto del texto, porque el `<h1>` elemento representa un encabezado de sección.</span><span class="sxs-lookup"><span data-stu-id="c6506-161">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="c6506-162">El explorador Web estilos automáticamente los títulos en tamaños de fuente mayores.</span><span class="sxs-lookup"><span data-stu-id="c6506-162">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    > ##### <span data-ttu-id="c6506-163">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="c6506-163">Figure 7</span></span>  
    > <span data-ttu-id="c6506-164">El nuevo título está visible en la pestaña en vivo</span><span class="sxs-lookup"><span data-stu-id="c6506-164">The new heading is visible in the live tab</span></span>  
    > ![El nuevo título está visible en la pestaña en vivo][ImageHtmlAdd2]  
    
1.  <span data-ttu-id="c6506-166">De nuevo en la **pestaña Editor**, inserte `<p>I am learning HTML.  Recent accomplishments:</p>` en la línea debajo de la cual acaba de colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="c6506-166">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### <span data-ttu-id="c6506-167">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="c6506-167">Figure 8</span></span>  
    > <span data-ttu-id="c6506-168">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="c6506-168">The new code is highlighted in the editor tab</span></span>  
    > ![El nuevo código está resaltado en la pestaña Editor][ImageHtmlAdd3]  
    
1.  <span data-ttu-id="c6506-170">Ver el cambio en la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="c6506-170">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="c6506-171">En la **pestaña Editor**, agregue una lista de sus logros:</span><span class="sxs-lookup"><span data-stu-id="c6506-171">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="c6506-172">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="c6506-172">Figure 9</span></span>  
    > <span data-ttu-id="c6506-173">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="c6506-173">The new code is highlighted in the editor tab</span></span>  
    > ![El nuevo código está resaltado en la pestaña Editor][ImageHtmlAdd4]  
    
1.  <span data-ttu-id="c6506-175">De nuevo, vuelva a la **pestaña en vivo** para asegurarse de que el nuevo contenido se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6506-175">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    > ##### <span data-ttu-id="c6506-176">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="c6506-176">Figure 10</span></span>  
    > <span data-ttu-id="c6506-177">La nueva lista está visible en la pestaña en vivo</span><span class="sxs-lookup"><span data-stu-id="c6506-177">The new list is visible in the live tab</span></span>  
    > ![La nueva lista está visible en la pestaña en vivo][ImageHtmlAdd5]  
    
## <span data-ttu-id="c6506-179">Experimentar con los cambios de contenido en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c6506-179">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="c6506-180">Si estuviera desarrollando una gran página con un gran número de HTML, puede imaginarse que es algo tedioso de volver y adelante entre la pestaña Editor y la ficha en vivo centenares de veces para ver los cambios, sobre todo si no está seguro de lo que debe colocar exactamente en la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-180">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="c6506-181">Microsoft Edge DevTools puede ayudarte a experimentar con los cambios de contenido sin salir de la ficha en vivo.</span><span class="sxs-lookup"><span data-stu-id="c6506-181">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="c6506-182">Obtener información sobre la diferencia entre HTML y DOM</span><span class="sxs-lookup"><span data-stu-id="c6506-182">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="c6506-183">Antes de empezar a editar el contenido desde Microsoft Edge DevTools, resulta útil comprender la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-183">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="c6506-184">La mejor manera de aprender es por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c6506-184">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="c6506-185">Ir a la **ficha en vivo**.  En la parte inferior de la página verá el texto `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="c6506-185">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    > ###### <span data-ttu-id="c6506-186">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="c6506-186">Figure 11</span></span>  
    > <span data-ttu-id="c6506-187">En la parte inferior de la página `A new element!?!` se puede ver el texto.</span><span class="sxs-lookup"><span data-stu-id="c6506-187">At the bottom of the page the text `A new element!?!` can be seen</span></span>  
    > ![En la parte inferior de la página, el texto de un nuevo elemento!?!][ImageHtmlDom1]  
    
1.  <span data-ttu-id="c6506-190">Vuelva a la **pestaña Editor** y busque este texto `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c6506-190">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="c6506-191">¡ No está allí!</span><span class="sxs-lookup"><span data-stu-id="c6506-191">It's not there!</span></span>  
    
    > ##### <span data-ttu-id="c6506-192">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="c6506-192">Figure 12</span></span>  
    > <span data-ttu-id="c6506-193">El misterio `A new element!?!` no se encuentra en ningún</span><span class="sxs-lookup"><span data-stu-id="c6506-193">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    > ![El dedo texto un elemento nuevo!?!][ImageHtmlDom2]  
    
1.  <span data-ttu-id="c6506-196">Vuelva a la **ficha en vivo**, haga clic con el botón derecho `A new element!?!` y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="c6506-196">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="c6506-197">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="c6506-197">Figure 13</span></span>  
    > <span data-ttu-id="c6506-198">Inspeccionar texto</span><span class="sxs-lookup"><span data-stu-id="c6506-198">Inspecting some text</span></span>  
    > ![Inspeccionar texto][ImageHtmlDom3]  
    
    <span data-ttu-id="c6506-200">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-200">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="c6506-201">está resaltado en azul.</span><span class="sxs-lookup"><span data-stu-id="c6506-201">is highlighted blue.</span></span>  <span data-ttu-id="c6506-202">Aunque esta estructura de DevTools se parece al código HTML, realmente es el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="c6506-202">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    > ##### <span data-ttu-id="c6506-203">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="c6506-203">Figure 14</span></span>  
    > <span data-ttu-id="c6506-204">DevTools está abierto junto a la página</span><span class="sxs-lookup"><span data-stu-id="c6506-204">DevTools is open alongside the page</span></span>  
    > ![DevTools está abierto junto a la página][ImageHtmlDom4]  
    
<span data-ttu-id="c6506-206">Cuando se carga la página, el explorador toma el código HTML para crear el contenido *inicial* de la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-206">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="c6506-207">DOM representa el contenido *actual* de la página, que puede cambiar a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="c6506-207">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="c6506-208">El `<div>A new element!?!</div>` contenido misterioso se agrega a tu página debido a la `<script src="new.js"></script>` etiqueta de la parte inferior de tu HTML.</span><span class="sxs-lookup"><span data-stu-id="c6506-208">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="c6506-209">Esta etiqueta hace que se ejecute código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c6506-209">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="c6506-210">Obtendrá más información sobre JavaScript en un tutorial posterior, pero por ahora piense en él como un lenguaje de programación que puede cambiar el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-210">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="c6506-211">En este caso en particular, el código de JavaScript `<div>A new element!?!</div>` se agrega a la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-211">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="c6506-212">Este es el motivo por el que este texto de misterios está visible en tu página en vivo, pero no en tu HTML.</span><span class="sxs-lookup"><span data-stu-id="c6506-212">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="c6506-213">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="c6506-213">Edit the DOM</span></span>   

<span data-ttu-id="c6506-214">Si desea experimentar rápidamente cambios de contenido sin salir de la pestaña en vivo, pruebe DevTools.</span><span class="sxs-lookup"><span data-stu-id="c6506-214">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="c6506-215">En DevTools, haga clic con el botón derecho `Your site!` y seleccione **Editar como html**.</span><span class="sxs-lookup"><span data-stu-id="c6506-215">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  

    > ##### <span data-ttu-id="c6506-216">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="c6506-216">Figure 15</span></span>  
    > <span data-ttu-id="c6506-217">Editar el nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="c6506-217">Editing the node as HTML</span></span>  
    > ![Editar el nodo como HTML][ImageHtmlEdit1]  
    
1.  <span data-ttu-id="c6506-219">Reemplaza `<p>Your site!</p>` con el código a continuación.</span><span class="sxs-lookup"><span data-stu-id="c6506-219">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="c6506-220">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="c6506-220">Figure 16</span></span>  
    > <span data-ttu-id="c6506-221">Editar el nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="c6506-221">Editing the node as HTML</span></span>  
    > ![Editar el nodo como HTML][ImageHtmlEdit2]  
    
1.  <span data-ttu-id="c6506-223">Pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para guardar los cambios, o haga clic fuera del cuadro.</span><span class="sxs-lookup"><span data-stu-id="c6506-223">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="c6506-224">Los cambios se muestran automáticamente en la vista en vivo de la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-224">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="c6506-225">El texto `Your site!` ha sido reemplazado por el nuevo contenido.</span><span class="sxs-lookup"><span data-stu-id="c6506-225">The text `Your site!` has been replaced with the new content.</span></span>  
    
    > ##### <span data-ttu-id="c6506-226">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="c6506-226">Figure 17</span></span>  
    > <span data-ttu-id="c6506-227">El nuevo contenido se muestra inmediatamente en la página</span><span class="sxs-lookup"><span data-stu-id="c6506-227">The new content shows up immediately on the page</span></span>  
    > ![El nuevo contenido se muestra inmediatamente en la página][ImageHtmlEdit3]  
    
<span data-ttu-id="c6506-229">Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido.</span><span class="sxs-lookup"><span data-stu-id="c6506-229">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="c6506-230">Si vuelve a cargar la página o cierra la pestaña, los cambios desaparecerán para siempre.</span><span class="sxs-lookup"><span data-stu-id="c6506-230">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="c6506-231">Si está usando este flujo de trabajo y quiere guardar los cambios, debe copiar manualmente esos cambios en el código HTML.</span><span class="sxs-lookup"><span data-stu-id="c6506-231">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="c6506-232">El siguiente par de secciones le muestran algunas formas más de cambiar el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-232">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="c6506-233">Reordenar nodos</span><span class="sxs-lookup"><span data-stu-id="c6506-233">Reorder nodes</span></span>   

<span data-ttu-id="c6506-234">También puede cambiar el orden de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-234">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="c6506-235">Por ejemplo, en la página web el menú de navegación está cerca de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="c6506-235">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="c6506-236">Para moverlo a la parte superior:</span><span class="sxs-lookup"><span data-stu-id="c6506-236">To move it to the top:</span></span>  

1.  <span data-ttu-id="c6506-237">Busque el `<nav>` nodo en el **árbol DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c6506-237">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="c6506-238">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="c6506-238">Figure 18</span></span>  
    > <span data-ttu-id="c6506-239">El nodo NAV está resaltado en azul en DevTools</span><span class="sxs-lookup"><span data-stu-id="c6506-239">The nav node is highlighted blue in DevTools</span></span>  
    > ![El nodo NAV está resaltado en azul en DevTools][ImageHtmlReorder1]  
    
1.  <span data-ttu-id="c6506-241">Arrastre el `<nav>` nodo a la parte superior, de modo que sea el primer secundario debajo `<body>` del nodo.</span><span class="sxs-lookup"><span data-stu-id="c6506-241">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    > ##### <span data-ttu-id="c6506-242">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="c6506-242">Figure 19</span></span>  
    > <span data-ttu-id="c6506-243">Arrastrar el nodo NAV a la parte superior</span><span class="sxs-lookup"><span data-stu-id="c6506-243">Dragging the nav node to the top</span></span>  
    > ![Arrastrar el nodo NAV a la parte superior][ImageHtmlReorder2]  
    
    <span data-ttu-id="c6506-245">El `<nav>` nodo se muestra ahora en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="c6506-245">The `<nav>` node is now displaying at the top of your page.</span></span>  
    
    > ##### <span data-ttu-id="c6506-246">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="c6506-246">Figure 20</span></span>  
    > <span data-ttu-id="c6506-247">El nodo NAV está en la parte superior de la página</span><span class="sxs-lookup"><span data-stu-id="c6506-247">The nav node is at the top of the page</span></span>  
    > ![El nodo NAV está en la parte superior de la página][ImageHtmlReorder3]  
    
### <span data-ttu-id="c6506-249">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="c6506-249">Delete a node</span></span>   

<span data-ttu-id="c6506-250">También puede quitar nodos del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-250">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="c6506-251">En el **árbol DOM**, haga clic en `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="c6506-251">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="c6506-252">DevTools resalta el nodo azul.</span><span class="sxs-lookup"><span data-stu-id="c6506-252">DevTools highlights the node blue.</span></span>  
    
    > ##### <span data-ttu-id="c6506-253">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="c6506-253">Figure 21</span></span>  
    > <span data-ttu-id="c6506-254">Selección del nodo que se va a eliminar</span><span class="sxs-lookup"><span data-stu-id="c6506-254">Selecting the node to be deleted</span></span>  
    > ![Selección del nodo que se va a eliminar][ImageHtmlDelete1]  
    
1.  <span data-ttu-id="c6506-256">Presione la `Delete` tecla del teclado.</span><span class="sxs-lookup"><span data-stu-id="c6506-256">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="c6506-257">El `<div>A new element!?!</div>` nodo se elimina del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="c6506-257">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="c6506-258">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="c6506-258">Figure 22</span></span>  
    > <span data-ttu-id="c6506-259">El nodo ha sido eliminado</span><span class="sxs-lookup"><span data-stu-id="c6506-259">The node has been deleted</span></span>  
    > ![El nodo ha sido eliminado][ImageHtmlDelete2]  
    
## <span data-ttu-id="c6506-261">Copiar los cambios</span><span class="sxs-lookup"><span data-stu-id="c6506-261">Copy your changes</span></span>   

<span data-ttu-id="c6506-262">Ya casi lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="c6506-262">You're almost done.</span></span>  <span data-ttu-id="c6506-263">Ha realizado algunos cambios en la página en DevTools, pero aún no se han guardado en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="c6506-263">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="c6506-264">Actualice la **ficha en vivo**.  Los cambios que realizó en el árbol DOM desaparecen.</span><span class="sxs-lookup"><span data-stu-id="c6506-264">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="c6506-265">En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto `A new element!?!` vuelve a la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="c6506-265">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    > ##### <span data-ttu-id="c6506-266">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="c6506-266">Figure 23</span></span>  
    > <span data-ttu-id="c6506-267">Los cambios que ha realizado han desaparecido</span><span class="sxs-lookup"><span data-stu-id="c6506-267">The changes that you've made are gone</span></span>  
    > ![Los cambios que ha realizado han desaparecido][ImageHtmlCopy1]  

1.  <span data-ttu-id="c6506-269">Copia el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="c6506-269">Copy the code below.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  <span data-ttu-id="c6506-270">Vuelva a la **pestaña Editor** y reemplace el contenido del `index.html` archivo por el que acaba de copiar.</span><span class="sxs-lookup"><span data-stu-id="c6506-270">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    > ##### <span data-ttu-id="c6506-271">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="c6506-271">Figure 24</span></span>  
    > <span data-ttu-id="c6506-272">Aspecto del `index.html` archivo</span><span class="sxs-lookup"><span data-stu-id="c6506-272">How your `index.html` file should look</span></span>  
    > ![Cómo debería tener el archivo index. html][ImageHtmlCopy2]  
    
## <span data-ttu-id="c6506-274">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="c6506-274">Next steps</span></span>   

*   <span data-ttu-id="c6506-275">Complete el siguiente tutorial de esta serie, [Introducción a CSS][DevToolsBeginnersCss], para obtener información sobre cómo aplicar un estilo a la página y probar los cambios de estilo en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c6506-275">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="c6506-276">Lea [la introducción al Dom][MDNIntroductionDom] para obtener más información sobre el Dom.</span><span class="sxs-lookup"><span data-stu-id="c6506-276">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="c6506-277">Consulta un curso como la [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia de desarrollo web de manos libres.</span><span class="sxs-lookup"><span data-stu-id="c6506-277">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Ilustración 1: el sitio finalizado"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Ilustración 2: la ficha Editor"  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Ilustración 3: el menú de opciones del proyecto"  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Ilustración 4: el proyecto remixto"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Ilustración 5: la ficha en vivo"  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Ilustración 6: el nuevo código está resaltado en la pestaña Editor"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Ilustración 7: el nuevo título está visible en la pestaña en vivo"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Ilustración 8: el nuevo código está resaltado en la pestaña Editor"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Ilustración 9: el nuevo código está resaltado en la pestaña Editor"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Ilustración 10: la nueva lista está visible en la pestaña en vivo"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Ilustración 11: en la parte inferior de la página el texto de un nuevo elemento!?! se puede ver"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Ilustración 12: el dedo texto un elemento nuevo!?! no se encuentra en el índice. html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Ilustración 13: inspeccionar texto"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Ilustración 14: DevTools está abierto junto a la página"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Ilustración 15: editar el nodo como HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Ilustración 16: editar el nodo como HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Ilustración 17: el nuevo contenido se muestra inmediatamente en la página"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Ilustración 18: el nodo NAV está resaltado en azul en DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Ilustración 19: arrastrar el nodo NAV a la parte superior"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Ilustración 20: el nodo NAV se encuentra en la parte superior de la página"  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Ilustración 21: selección del nodo que se va a eliminar"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Ilustración 22: el nodo se ha eliminado"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Ilustración 23: los cambios que ha realizado han desaparecido"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Ilustración 24: el aspecto del archivo index. html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools para principiantes: Introducción a CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. html-alluring-shock | Intento"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="c6506-308">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c6506-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c6506-309">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="c6506-309">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c6506-311">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c6506-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
