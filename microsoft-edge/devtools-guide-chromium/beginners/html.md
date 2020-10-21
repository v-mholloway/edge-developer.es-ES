---
description: Introducción a HTML y el DOM
title: 'DevTools para principiantes: Introducción a HTML y el DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f17b68845ef746fa2612cdf4d02cc7e1003baabb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125303"
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

# <span data-ttu-id="286bb-104">DevTools para principiantes: Introducción a HTML y el DOM</span><span class="sxs-lookup"><span data-stu-id="286bb-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="286bb-105">Este es el primero de una serie de tutoriales que enseñan los conceptos básicos del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="286bb-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="286bb-106">También aprenderá un conjunto de herramientas para desarrolladores web denominado Microsoft Edge DevTools, que puede aumentar su productividad.</span><span class="sxs-lookup"><span data-stu-id="286bb-106">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="286bb-107">En este tutorial en particular, obtendrá información sobre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="286bb-108">HTML es una de las tecnologías básicas de desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="286bb-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="286bb-109">Es el lenguaje que controla la estructura y el contenido de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="286bb-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="286bb-110">El DOM también está relacionado con la estructura y el contenido de las páginas web, pero obtendrá más información sobre esto más adelante.</span><span class="sxs-lookup"><span data-stu-id="286bb-110">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="286bb-111">Principales</span><span class="sxs-lookup"><span data-stu-id="286bb-111">Goals</span></span>  

<span data-ttu-id="286bb-112">Va a aprender a usar el desarrollo web creando su propio sitio Web.</span><span class="sxs-lookup"><span data-stu-id="286bb-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="286bb-113">Cuando complete todos los tutoriales de la serie *DevTools para principiantes* , el sitio finalizado se verá como en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="286bb-113">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like in the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="286bb-115">El sitio finalizado</span><span class="sxs-lookup"><span data-stu-id="286bb-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="286bb-116">Al final de este tutorial, comprenderá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="286bb-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="286bb-117">Cómo los HTML y el DOM crean el contenido que se ve en las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="286bb-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="286bb-118">Cómo puede ayudarte Microsoft Edge DevTools a experimentar con los cambios de HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="286bb-119">La diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="286bb-120">También tendrá un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="286bb-120">You'll also have a real website!</span></span>  <span data-ttu-id="286bb-121">Puede usar este sitio para hospedar su currículum o su blog.</span><span class="sxs-lookup"><span data-stu-id="286bb-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="286bb-122">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="286bb-122">Prerequisites</span></span>  

<span data-ttu-id="286bb-123">Antes de intentar este tutorial, complete los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="286bb-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="286bb-124">Si no está familiarizado con HTML, lea [Introducción a HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="286bb-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="286bb-125">Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="286bb-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="286bb-126">En este tutorial se usa un conjunto de herramientas de desarrollo web, denominado Microsoft Edge DevTools, que está integrado en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="286bb-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="286bb-127">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="286bb-127">Set up your code</span></span>  

<span data-ttu-id="286bb-128">Va a crear su sitio en un editor de código en línea denominado problema.</span><span class="sxs-lookup"><span data-stu-id="286bb-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="286bb-129">Abra el [código fuente][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="286bb-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="286bb-130">Esta pestaña se denomina la **pestaña Editor** a lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="286bb-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="286bb-132">Ficha Editor</span><span class="sxs-lookup"><span data-stu-id="286bb-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-133">Elige **alluring**.</span><span class="sxs-lookup"><span data-stu-id="286bb-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="286bb-134">El menú opciones de proyecto se abre en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="286bb-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="286bb-136">El menú opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="286bb-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-137">Elija **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="286bb-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="286bb-138">Problema crea una copia del proyecto que puede editar y genera de forma aleatoria un nombre nuevo para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="286bb-138">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="286bb-139">El contenido es el mismo que antes.</span><span class="sxs-lookup"><span data-stu-id="286bb-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="286bb-141">El proyecto remixto</span><span class="sxs-lookup"><span data-stu-id="286bb-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-142">Si planea completar el siguiente tutorial de esta serie, elija **iniciar sesión** e iniciar sesión en un problema con su cuenta de Github o Facebook.</span><span class="sxs-lookup"><span data-stu-id="286bb-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="286bb-143">Si no inicia sesión, perderá la posibilidad de editar este proyecto una vez que cierre la pestaña edición.</span><span class="sxs-lookup"><span data-stu-id="286bb-143">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="286bb-144">Elija **Mostrar** y elija **una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="286bb-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="286bb-145">Se abre una nueva pestaña, que muestra la página en vivo.</span><span class="sxs-lookup"><span data-stu-id="286bb-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="286bb-146">Esta pestaña se denominará **pestaña en vivo** en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="286bb-146">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="286bb-148">La ficha en vivo</span><span class="sxs-lookup"><span data-stu-id="286bb-148">The live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="286bb-149">Agregar contenido</span><span class="sxs-lookup"><span data-stu-id="286bb-149">Add content</span></span>  

<span data-ttu-id="286bb-150">Tu sitio está vacío.</span><span class="sxs-lookup"><span data-stu-id="286bb-150">Your site is pretty empty.</span></span>  <span data-ttu-id="286bb-151">Siga los pasos que se indican a continuación para agregar algo de contenido.</span><span class="sxs-lookup"><span data-stu-id="286bb-151">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="286bb-152">En la **pestaña Editor**, reemplace `<!-- You're "About Me" will go here.  -->` con `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="286bb-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="286bb-154">El nuevo código está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="286bb-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="286bb-155">Ver los cambios en la **ficha en vivo**.  El texto `About Me` está visible en la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="286bb-156">Es más grande que el resto del texto, porque el `<h1>` elemento representa un encabezado de sección.</span><span class="sxs-lookup"><span data-stu-id="286bb-156">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="286bb-157">El explorador Web estilos automáticamente los títulos en tamaños de fuente mayores.</span><span class="sxs-lookup"><span data-stu-id="286bb-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="286bb-159">El nuevo título está visible en la pestaña en vivo</span><span class="sxs-lookup"><span data-stu-id="286bb-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-160">De nuevo en la **pestaña Editor**, inserte `<p>I am learning HTML.  Recent accomplishments:</p>` en la línea debajo de la cual acaba de colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="286bb-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="286bb-162">El código actualizado aparece resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="286bb-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="286bb-163">Ver el cambio en la **ficha en vivo**.</span><span class="sxs-lookup"><span data-stu-id="286bb-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="286bb-164">En la **pestaña Editor**, agregue una lista de sus logros:</span><span class="sxs-lookup"><span data-stu-id="286bb-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="286bb-166">El código actualizado también está resaltado en la pestaña Editor</span><span class="sxs-lookup"><span data-stu-id="286bb-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="286bb-167">De nuevo, vuelva a la **pestaña en vivo** para asegurarse de que el nuevo contenido se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="286bb-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="286bb-169">La nueva lista está visible en la pestaña en vivo</span><span class="sxs-lookup"><span data-stu-id="286bb-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="286bb-170">Experimentar con los cambios de contenido en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="286bb-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="286bb-171">Si estuviera desarrollando una gran página con un gran número de HTML, puede imaginarse que es algo tedioso de volver y adelante entre la pestaña Editor y la ficha en vivo centenares de veces para ver los cambios, sobre todo si no está seguro de lo que debe colocar exactamente en la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-171">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="286bb-172">Microsoft Edge DevTools puede ayudarte a experimentar con los cambios de contenido sin salir de la ficha en vivo.</span><span class="sxs-lookup"><span data-stu-id="286bb-172">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="286bb-173">Obtener información sobre la diferencia entre HTML y DOM</span><span class="sxs-lookup"><span data-stu-id="286bb-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="286bb-174">Antes de empezar a editar el contenido desde Microsoft Edge DevTools, resulta útil comprender la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-174">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="286bb-175">La mejor manera de aprender es por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="286bb-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="286bb-176">Ir a la **ficha en vivo**.  En la parte inferior de la página verá el texto `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="286bb-176">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="286bb-179">En la parte inferior de la página, el texto de un nuevo elemento!?!</span><span class="sxs-lookup"><span data-stu-id="286bb-179">At the bottom of the page the text A new element!?!</span></span> <span data-ttu-id="286bb-180">se puede ver</span><span class="sxs-lookup"><span data-stu-id="286bb-180">can be seen</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-181">Vuelva a la **pestaña Editor** y busque este texto `index.html` .</span><span class="sxs-lookup"><span data-stu-id="286bb-181">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="286bb-182">¡ No está allí!</span><span class="sxs-lookup"><span data-stu-id="286bb-182">It's not there!</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="286bb-185">El misterio `A new element!?!` no se encuentra en ningún</span><span class="sxs-lookup"><span data-stu-id="286bb-185">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-186">Vuelva a la **ficha en vivo**, haga clic con el botón derecho `A new element!?!` y elija **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="286bb-186">Go back to the **live tab**, right-click `A new element!?!`, and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="286bb-188">Inspeccionar texto</span><span class="sxs-lookup"><span data-stu-id="286bb-188">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="286bb-189">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-189">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="286bb-190">está resaltado en azul.</span><span class="sxs-lookup"><span data-stu-id="286bb-190">is highlighted blue.</span></span>  <span data-ttu-id="286bb-191">Aunque esta estructura de DevTools se parece al código HTML, realmente es el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="286bb-191">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="286bb-193">DevTools está abierto junto a la página</span><span class="sxs-lookup"><span data-stu-id="286bb-193">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="286bb-194">Cuando se carga la página, el explorador toma el código HTML para crear el contenido *inicial* de la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-194">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="286bb-195">DOM representa el contenido *actual* de la página, que puede cambiar a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="286bb-195">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="286bb-196">El `<div>A new element!?!</div>` contenido misterioso se agrega a tu página debido a la `<script src="new.js"></script>` etiqueta de la parte inferior de tu HTML.</span><span class="sxs-lookup"><span data-stu-id="286bb-196">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="286bb-197">Esta etiqueta hace que se ejecute código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="286bb-197">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="286bb-198">Obtendrá más información sobre JavaScript en un tutorial posterior, pero por ahora piense en él como un lenguaje de programación que puede cambiar el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-198">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="286bb-199">En este caso en particular, el código de JavaScript `<div>A new element!?!</div>` se agrega a la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-199">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="286bb-200">Este es el motivo por el que este texto de misterios está visible en tu página en vivo, pero no en tu HTML.</span><span class="sxs-lookup"><span data-stu-id="286bb-200">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="286bb-201">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="286bb-201">Edit the DOM</span></span>  

<span data-ttu-id="286bb-202">Si desea experimentar rápidamente cambios de contenido sin salir de la pestaña en vivo, pruebe DevTools.</span><span class="sxs-lookup"><span data-stu-id="286bb-202">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="286bb-203">En DevTools, haga clic con el botón derecho `Your site!` y elija **Editar como html**.</span><span class="sxs-lookup"><span data-stu-id="286bb-203">In DevTools, right-click `Your site!` and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="286bb-205">Editar el nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="286bb-205">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-206">Reemplaza `<p>Your site!</p>` con el código a continuación.</span><span class="sxs-lookup"><span data-stu-id="286bb-206">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="286bb-208">Actualizar el nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="286bb-208">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="286bb-209">Seleccione `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \) para guardar los cambios o haga clic fuera del cuadro.</span><span class="sxs-lookup"><span data-stu-id="286bb-209">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="286bb-210">Los cambios se muestran automáticamente en la vista en vivo de la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-210">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="286bb-211">El texto `Your site!` ha sido reemplazado por el nuevo contenido.</span><span class="sxs-lookup"><span data-stu-id="286bb-211">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="286bb-213">El nuevo contenido se muestra inmediatamente en la página</span><span class="sxs-lookup"><span data-stu-id="286bb-213">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="286bb-214">Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido.</span><span class="sxs-lookup"><span data-stu-id="286bb-214">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="286bb-215">Si vuelve a cargar la página o cierra la pestaña, los cambios desaparecerán para siempre.</span><span class="sxs-lookup"><span data-stu-id="286bb-215">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="286bb-216">Si está usando este flujo de trabajo y quiere guardar los cambios, debe copiar manualmente esos cambios en el código HTML.</span><span class="sxs-lookup"><span data-stu-id="286bb-216">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="286bb-217">El siguiente par de secciones le muestran algunas formas más de cambiar el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-217">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="286bb-218">Reordenar nodos</span><span class="sxs-lookup"><span data-stu-id="286bb-218">Reorder nodes</span></span>  

<span data-ttu-id="286bb-219">También puede cambiar el orden de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-219">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="286bb-220">Por ejemplo, en la página web el menú de navegación está cerca de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="286bb-220">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="286bb-221">Para moverlo a la parte superior:</span><span class="sxs-lookup"><span data-stu-id="286bb-221">To move it to the top:</span></span>  

1.  <span data-ttu-id="286bb-222">Busque el `<nav>` nodo en el **árbol DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="286bb-222">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="286bb-224">El nodo NAV está resaltado en azul en DevTools</span><span class="sxs-lookup"><span data-stu-id="286bb-224">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-225">Arrastre el `<nav>` nodo a la parte superior, de modo que sea el primer secundario debajo `<body>` del nodo.</span><span class="sxs-lookup"><span data-stu-id="286bb-225">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="286bb-227">Arrastrar el nodo NAV a la parte superior</span><span class="sxs-lookup"><span data-stu-id="286bb-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="286bb-228">El `<nav>` nodo se muestra ahora en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="286bb-228">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="286bb-230">El nodo NAV está en la parte superior de la página</span><span class="sxs-lookup"><span data-stu-id="286bb-230">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <span data-ttu-id="286bb-231">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="286bb-231">Delete a node</span></span>  

<span data-ttu-id="286bb-232">También puede quitar nodos del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-232">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="286bb-233">En el **árbol DOM**, haga clic en `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="286bb-233">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="286bb-234">DevTools resalta el nodo azul.</span><span class="sxs-lookup"><span data-stu-id="286bb-234">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="286bb-236">Selección del nodo que se va a eliminar</span><span class="sxs-lookup"><span data-stu-id="286bb-236">Selecting the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-237">Presione la `Delete` tecla del teclado.</span><span class="sxs-lookup"><span data-stu-id="286bb-237">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="286bb-238">El `<div>A new element!?!</div>` nodo se elimina del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="286bb-238">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="286bb-240">El nodo ha sido eliminado</span><span class="sxs-lookup"><span data-stu-id="286bb-240">The node has been deleted</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="286bb-241">Copiar los cambios</span><span class="sxs-lookup"><span data-stu-id="286bb-241">Copy your changes</span></span>  

<span data-ttu-id="286bb-242">Ya casi lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="286bb-242">You're almost done.</span></span>  <span data-ttu-id="286bb-243">Ha realizado algunos cambios en la página en DevTools, pero aún no se han guardado en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="286bb-243">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="286bb-244">Actualice la **ficha en vivo**.  Los cambios que realizó en el árbol DOM desaparecen.</span><span class="sxs-lookup"><span data-stu-id="286bb-244">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="286bb-245">En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto `A new element!?!` vuelve a la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="286bb-245">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="286bb-247">Los cambios que ha realizado han desaparecido</span><span class="sxs-lookup"><span data-stu-id="286bb-247">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="286bb-248">Copia el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="286bb-248">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="286bb-249">Vuelva a la **pestaña Editor** y reemplace el contenido del `index.html` archivo por el que acaba de copiar.</span><span class="sxs-lookup"><span data-stu-id="286bb-249">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="El sitio finalizado" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="286bb-251">Aspecto del `index.html` archivo</span><span class="sxs-lookup"><span data-stu-id="286bb-251">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="286bb-252">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="286bb-252">Next steps</span></span>  

*   <span data-ttu-id="286bb-253">Complete el siguiente tutorial de esta serie, [Introducción a CSS][DevToolsBeginnersCss], para obtener información sobre cómo aplicar un estilo a la página y probar los cambios de estilo en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="286bb-253">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="286bb-254">Lea [la introducción al Dom][MDNIntroductionDom] para obtener más información sobre el Dom.</span><span class="sxs-lookup"><span data-stu-id="286bb-254">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="286bb-255">Consulta un curso como la [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia de desarrollo web de manos libres.</span><span class="sxs-lookup"><span data-stu-id="286bb-255">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <span data-ttu-id="286bb-256">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="286bb-256">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para principiantes: Introducción a CSS | Microsoft docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring: descargas | Intento"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="286bb-263">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="286bb-263">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="286bb-264">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="286bb-264">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="286bb-266">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="286bb-266">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
