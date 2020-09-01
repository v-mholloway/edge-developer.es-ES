---
title: 'DevTools para principiantes: Introducción a HTML y el DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 50dfd8595c270a2532f55b71307b42c3636bba3c
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983103"
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

# <span data-ttu-id="ab748-103">DevTools para principiantes: Introducción a HTML y el DOM</span><span class="sxs-lookup"><span data-stu-id="ab748-103">DevTools for beginners: Get started with HTML and the DOM</span></span>   

<span data-ttu-id="ab748-104">Este es el primero de una serie de tutoriales que enseñan los conceptos básicos del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="ab748-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="ab748-105">También aprenderá un conjunto de herramientas para desarrolladores web denominado Microsoft Edge DevTools, que puede aumentar su productividad.</span><span class="sxs-lookup"><span data-stu-id="ab748-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="ab748-106">En este tutorial en particular, obtendrá información sobre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="ab748-107">HTML es una de las tecnologías básicas de desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="ab748-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="ab748-108">Es el lenguaje que controla la estructura y el contenido de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="ab748-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="ab748-109">El DOM también está relacionado con la estructura y el contenido de las páginas web, pero obtendrá más información sobre esto más adelante.</span><span class="sxs-lookup"><span data-stu-id="ab748-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="ab748-110">Principales</span><span class="sxs-lookup"><span data-stu-id="ab748-110">Goals</span></span>   

<span data-ttu-id="ab748-111">Va a aprender a usar el desarrollo web creando su propio sitio Web.</span><span class="sxs-lookup"><span data-stu-id="ab748-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="ab748-112">Cuando complete todos los tutoriales de la serie *DevTools para principiantes* , el sitio finalizado se verá como en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ab748-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like in the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="ab748-114">El sitio finalizado</span><span class="sxs-lookup"><span data-stu-id="ab748-114">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="ab748-115">Al final de este tutorial, comprenderá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab748-115">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="ab748-116">Cómo los HTML y el DOM crean el contenido que se ve en las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="ab748-116">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="ab748-117">Cómo puede ayudarte Microsoft Edge DevTools a experimentar con los cambios de HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-117">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="ab748-118">La diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-118">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="ab748-119">También tendrá un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="ab748-119">You'll also have a real website!</span></span>  <span data-ttu-id="ab748-120">Puede usar este sitio para hospedar su currículum o su blog.</span><span class="sxs-lookup"><span data-stu-id="ab748-120">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="ab748-121">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ab748-121">Prerequisites</span></span>   

<span data-ttu-id="ab748-122">Antes de intentar este tutorial, complete los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="ab748-122">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="ab748-123">Si no está familiarizado con HTML, lea [Introducción a HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="ab748-123">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="ab748-124">Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="ab748-124">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="ab748-125">En este tutorial se usa un conjunto de herramientas de desarrollo web, denominado Microsoft Edge DevTools, que está integrado en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab748-125">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="ab748-126">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="ab748-126">Set up your code</span></span>   

<span data-ttu-id="ab748-127">Va a crear su sitio en un editor de código en línea denominado problema.</span><span class="sxs-lookup"><span data-stu-id="ab748-127">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="ab748-128">Abra el [código fuente][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="ab748-128">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="ab748-129">Esta pestaña se denomina la **pestaña Editor** a lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="ab748-129">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Ficha Editor" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="ab748-131">Ficha Editor</span><span class="sxs-lookup"><span data-stu-id="ab748-131">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-132">Haga clic en **alluring-shock**.</span><span class="sxs-lookup"><span data-stu-id="ab748-132">Click **alluring-shock**.</span></span>  <span data-ttu-id="ab748-133">El menú opciones de proyecto se abre en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="ab748-133">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="El menú opciones del proyecto" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="ab748-135">El menú opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="ab748-135">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-136">Haga clic en **Remix proyecto**.</span><span class="sxs-lookup"><span data-stu-id="ab748-136">Click **Remix Project**.</span></span>  <span data-ttu-id="ab748-137">Problema crea una copia del proyecto que puede editar y genera de forma aleatoria un nombre nuevo para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ab748-137">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="ab748-138">El contenido es el mismo que antes.</span><span class="sxs-lookup"><span data-stu-id="ab748-138">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="El proyecto remixto" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="ab748-140">El proyecto remixto</span><span class="sxs-lookup"><span data-stu-id="ab748-140">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-141">Si planea completar el siguiente tutorial de esta serie, haga clic en **iniciar sesión** e inicie sesión en un problema con su cuenta de Github o Facebook.</span><span class="sxs-lookup"><span data-stu-id="ab748-141">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="ab748-142">Si no inicia sesión, perderá la posibilidad de editar este proyecto una vez que cierre la pestaña edición.</span><span class="sxs-lookup"><span data-stu-id="ab748-142">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="ab748-143">Haga clic en **Mostrar** y seleccione **en una ventana nueva**.</span><span class="sxs-lookup"><span data-stu-id="ab748-143">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="ab748-144">Se abre una nueva pestaña, que muestra la página en vivo.</span><span class="sxs-lookup"><span data-stu-id="ab748-144">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="ab748-145">Esta pestaña se denominará **pestaña en vivo** en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="ab748-145">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="La ficha en vivo" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="ab748-147">La ficha en vivo</span><span class="sxs-lookup"><span data-stu-id="ab748-147">The live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ab748-148">Agregar contenido</span><span class="sxs-lookup"><span data-stu-id="ab748-148">Add content</span></span>   

<span data-ttu-id="ab748-149">Tu sitio está vacío.</span><span class="sxs-lookup"><span data-stu-id="ab748-149">Your site is pretty empty.</span></span>  <span data-ttu-id="ab748-150">Siga los pasos que se indican a continuación para agregar algo de contenido.</span><span class="sxs-lookup"><span data-stu-id="ab748-150">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="ab748-151">En la **pestaña Editor**, reemplace `<!-- You're "About Me" will go here.  -->` con `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="ab748-151">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="El nuevo código está resaltado en la pestaña Editor" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="ab748-153">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="ab748-153">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="ab748-154">Ver los cambios en la **ficha en vivo**.  El texto `About Me` está visible en la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-154">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="ab748-155">Es más grande que el resto del texto, porque el `<h1>` elemento representa un encabezado de sección.</span><span class="sxs-lookup"><span data-stu-id="ab748-155">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="ab748-156">El explorador Web estilos automáticamente los títulos en tamaños de fuente mayores.</span><span class="sxs-lookup"><span data-stu-id="ab748-156">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="El nuevo título está visible en la pestaña en vivo" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="ab748-158">El nuevo título está visible en la pestaña en vivo</span><span class="sxs-lookup"><span data-stu-id="ab748-158">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-159">De nuevo en la **pestaña Editor**, inserte `<p>I am learning HTML.  Recent accomplishments:</p>` en la línea debajo de la cual acaba de colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="ab748-159">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="El nuevo código está resaltado en la pestaña Editor" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="ab748-161">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="ab748-161">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="ab748-162">Ver el cambio en la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="ab748-162">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="ab748-163">En la **pestaña Editor**, agregue una lista de sus logros:</span><span class="sxs-lookup"><span data-stu-id="ab748-163">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="El nuevo código está resaltado en la pestaña Editor" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="ab748-165">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="ab748-165">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="ab748-166">De nuevo, vuelva a la **pestaña en vivo** para asegurarse de que el nuevo contenido se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab748-166">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="La nueva lista está visible en la pestaña en vivo" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="ab748-168">La nueva lista está visible en la pestaña en vivo</span><span class="sxs-lookup"><span data-stu-id="ab748-168">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ab748-169">Experimentar con los cambios de contenido en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ab748-169">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="ab748-170">Si estuviera desarrollando una gran página con un gran número de HTML, puede imaginarse que es algo tedioso de volver y adelante entre la pestaña Editor y la ficha en vivo centenares de veces para ver los cambios, sobre todo si no está seguro de lo que debe colocar exactamente en la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-170">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="ab748-171">Microsoft Edge DevTools puede ayudarte a experimentar con los cambios de contenido sin salir de la ficha en vivo.</span><span class="sxs-lookup"><span data-stu-id="ab748-171">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="ab748-172">Obtener información sobre la diferencia entre HTML y DOM</span><span class="sxs-lookup"><span data-stu-id="ab748-172">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="ab748-173">Antes de empezar a editar el contenido desde Microsoft Edge DevTools, resulta útil comprender la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-173">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="ab748-174">La mejor manera de aprender es por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ab748-174">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="ab748-175">Ir a la **ficha en vivo**.  En la parte inferior de la página verá el texto `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="ab748-175">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="En la parte inferior de la página, el texto de un nuevo elemento!?! se puede ver" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="ab748-178">En la parte inferior de la página, el texto de un nuevo elemento!?!</span><span class="sxs-lookup"><span data-stu-id="ab748-178">At the bottom of the page the text A new element!?!</span></span> <span data-ttu-id="ab748-179">se puede ver</span><span class="sxs-lookup"><span data-stu-id="ab748-179">can be seen</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-180">Vuelva a la **pestaña Editor** y busque este texto `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ab748-180">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="ab748-181">¡ No está allí!</span><span class="sxs-lookup"><span data-stu-id="ab748-181">It's not there!</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="El dedo texto un elemento nuevo!?! no se encuentra en index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="ab748-184">El misterio `A new element!?!` no se encuentra en ningún</span><span class="sxs-lookup"><span data-stu-id="ab748-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-185">Vuelva a la **ficha en vivo**, haga clic con el botón derecho `A new element!?!` y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="ab748-185">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspeccionar texto" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="ab748-187">Inspeccionar texto</span><span class="sxs-lookup"><span data-stu-id="ab748-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ab748-188">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="ab748-189">está resaltado en azul.</span><span class="sxs-lookup"><span data-stu-id="ab748-189">is highlighted blue.</span></span>  <span data-ttu-id="ab748-190">Aunque esta estructura de DevTools se parece al código HTML, realmente es el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="ab748-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools está abierto junto a la página" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="ab748-192">DevTools está abierto junto a la página</span><span class="sxs-lookup"><span data-stu-id="ab748-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ab748-193">Cuando se carga la página, el explorador toma el código HTML para crear el contenido *inicial* de la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="ab748-194">DOM representa el contenido *actual* de la página, que puede cambiar a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="ab748-194">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="ab748-195">El `<div>A new element!?!</div>` contenido misterioso se agrega a tu página debido a la `<script src="new.js"></script>` etiqueta de la parte inferior de tu HTML.</span><span class="sxs-lookup"><span data-stu-id="ab748-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="ab748-196">Esta etiqueta hace que se ejecute código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ab748-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="ab748-197">Obtendrá más información sobre JavaScript en un tutorial posterior, pero por ahora piense en él como un lenguaje de programación que puede cambiar el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-197">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="ab748-198">En este caso en particular, el código de JavaScript `<div>A new element!?!</div>` se agrega a la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="ab748-199">Este es el motivo por el que este texto de misterios está visible en tu página en vivo, pero no en tu HTML.</span><span class="sxs-lookup"><span data-stu-id="ab748-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="ab748-200">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="ab748-200">Edit the DOM</span></span>   

<span data-ttu-id="ab748-201">Si desea experimentar rápidamente cambios de contenido sin salir de la pestaña en vivo, pruebe DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab748-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="ab748-202">En DevTools, haga clic con el botón derecho `Your site!` y seleccione **Editar como html**.</span><span class="sxs-lookup"><span data-stu-id="ab748-202">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Editar el nodo como HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="ab748-204">Editar el nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="ab748-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-205">Reemplaza `<p>Your site!</p>` con el código a continuación.</span><span class="sxs-lookup"><span data-stu-id="ab748-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Editar el nodo como HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="ab748-207">Editar el nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="ab748-207">Editing the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="ab748-208">Pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para guardar los cambios, o haga clic fuera del cuadro.</span><span class="sxs-lookup"><span data-stu-id="ab748-208">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="ab748-209">Los cambios se muestran automáticamente en la vista en vivo de la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="ab748-210">El texto `Your site!` ha sido reemplazado por el nuevo contenido.</span><span class="sxs-lookup"><span data-stu-id="ab748-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="El nuevo contenido se muestra inmediatamente en la página" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="ab748-212">El nuevo contenido se muestra inmediatamente en la página</span><span class="sxs-lookup"><span data-stu-id="ab748-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ab748-213">Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido.</span><span class="sxs-lookup"><span data-stu-id="ab748-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="ab748-214">Si vuelve a cargar la página o cierra la pestaña, los cambios desaparecerán para siempre.</span><span class="sxs-lookup"><span data-stu-id="ab748-214">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="ab748-215">Si está usando este flujo de trabajo y quiere guardar los cambios, debe copiar manualmente esos cambios en el código HTML.</span><span class="sxs-lookup"><span data-stu-id="ab748-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="ab748-216">El siguiente par de secciones le muestran algunas formas más de cambiar el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-216">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="ab748-217">Reordenar nodos</span><span class="sxs-lookup"><span data-stu-id="ab748-217">Reorder nodes</span></span>   

<span data-ttu-id="ab748-218">También puede cambiar el orden de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-218">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="ab748-219">Por ejemplo, en la página web el menú de navegación está cerca de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="ab748-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="ab748-220">Para moverlo a la parte superior:</span><span class="sxs-lookup"><span data-stu-id="ab748-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="ab748-221">Busque el `<nav>` nodo en el **árbol DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab748-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="El nodo NAV está resaltado en azul en DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="ab748-223">El nodo NAV está resaltado en azul en DevTools</span><span class="sxs-lookup"><span data-stu-id="ab748-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-224">Arrastre el `<nav>` nodo a la parte superior, de modo que sea el primer secundario debajo `<body>` del nodo.</span><span class="sxs-lookup"><span data-stu-id="ab748-224">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Arrastrar el nodo NAV a la parte superior" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="ab748-226">Arrastrar el nodo NAV a la parte superior</span><span class="sxs-lookup"><span data-stu-id="ab748-226">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="ab748-227">El `<nav>` nodo se muestra ahora en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="ab748-227">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="El nodo NAV está en la parte superior de la página" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="ab748-229">El nodo NAV está en la parte superior de la página</span><span class="sxs-lookup"><span data-stu-id="ab748-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <span data-ttu-id="ab748-230">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="ab748-230">Delete a node</span></span>   

<span data-ttu-id="ab748-231">También puede quitar nodos del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-231">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="ab748-232">En el **árbol DOM**, haga clic en `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="ab748-232">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="ab748-233">DevTools resalta el nodo azul.</span><span class="sxs-lookup"><span data-stu-id="ab748-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Selección del nodo que se va a eliminar" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="ab748-235">Selección del nodo que se va a eliminar</span><span class="sxs-lookup"><span data-stu-id="ab748-235">Selecting the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-236">Presione la `Delete` tecla del teclado.</span><span class="sxs-lookup"><span data-stu-id="ab748-236">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="ab748-237">El `<div>A new element!?!</div>` nodo se elimina del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="ab748-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="El nodo ha sido eliminado" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="ab748-239">El nodo ha sido eliminado</span><span class="sxs-lookup"><span data-stu-id="ab748-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ab748-240">Copiar los cambios</span><span class="sxs-lookup"><span data-stu-id="ab748-240">Copy your changes</span></span>   

<span data-ttu-id="ab748-241">Ya casi lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="ab748-241">You're almost done.</span></span>  <span data-ttu-id="ab748-242">Ha realizado algunos cambios en la página en DevTools, pero aún no se han guardado en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ab748-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="ab748-243">Actualice la **ficha en vivo**.  Los cambios que realizó en el árbol DOM desaparecen.</span><span class="sxs-lookup"><span data-stu-id="ab748-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="ab748-244">En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto `A new element!?!` vuelve a la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="ab748-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Los cambios que ha realizado han desaparecido" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="ab748-246">Los cambios que ha realizado han desaparecido</span><span class="sxs-lookup"><span data-stu-id="ab748-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ab748-247">Copia el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="ab748-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="ab748-248">Vuelva a la **pestaña Editor** y reemplace el contenido del `index.html` archivo por el que acaba de copiar.</span><span class="sxs-lookup"><span data-stu-id="ab748-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Cómo debería tener el archivo index.html" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="ab748-250">Aspecto del `index.html` archivo</span><span class="sxs-lookup"><span data-stu-id="ab748-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ab748-251">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="ab748-251">Next steps</span></span>   

*   <span data-ttu-id="ab748-252">Complete el siguiente tutorial de esta serie, [Introducción a CSS][DevToolsBeginnersCss], para obtener información sobre cómo aplicar un estilo a la página y probar los cambios de estilo en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab748-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="ab748-253">Lea [la introducción al Dom][MDNIntroductionDom] para obtener más información sobre el Dom.</span><span class="sxs-lookup"><span data-stu-id="ab748-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="ab748-254">Consulta un curso como la [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia de desarrollo web de manos libres.</span><span class="sxs-lookup"><span data-stu-id="ab748-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para principiantes: Introducción a CSS | Microsoft docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring: descargas | Intento"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="ab748-261">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab748-261">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ab748-262">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="ab748-262">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ab748-264">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab748-264">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
