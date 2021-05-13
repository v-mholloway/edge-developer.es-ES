---
description: Introducción con HTML y DOM
title: 'DevTools para principiantes: Introducción a HTML y DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564570"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="3bf42-104">DevTools para principiantes: Introducción a HTML y DOM</span><span class="sxs-lookup"><span data-stu-id="3bf42-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="3bf42-105">Este es el primero de una serie de tutoriales que le enseñarán los conceptos básicos del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="3bf42-106">Obtenga información sobre un conjunto de herramientas de desarrollador web, denominadas Microsoft Edge DevTools, que pueden aumentar su productividad.</span><span class="sxs-lookup"><span data-stu-id="3bf42-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="3bf42-107">En este tutorial en particular, aprenderá acerca de HTML y dom.</span><span class="sxs-lookup"><span data-stu-id="3bf42-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="3bf42-108">HTML es una de las tecnologías principales del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="3bf42-109">Es el idioma que controla la estructura y el contenido de las páginas web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="3bf42-110">El DOM también está relacionado con la estructura y el contenido de las páginas web, obtenga más información sobre esto más adelante.</span><span class="sxs-lookup"><span data-stu-id="3bf42-110">The DOM is also related to the structure and content of webpages, learn more about that later.</span></span>  

## <a name="goals"></a><span data-ttu-id="3bf42-111">Objetivos</span><span class="sxs-lookup"><span data-stu-id="3bf42-111">Goals</span></span>  

<span data-ttu-id="3bf42-112">Vas a aprender el desarrollo web creando tu propio sitio web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="3bf42-113">Para cuando complete todos los tutoriales de la serie **DevTools para** principiantes, el sitio terminado puede tener el aspecto siguiente.</span><span class="sxs-lookup"><span data-stu-id="3bf42-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="El sitio terminado" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="3bf42-115">El sitio terminado</span><span class="sxs-lookup"><span data-stu-id="3bf42-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="3bf42-116">Al final de este tutorial, debe comprender los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="3bf42-116">By the end of this tutorial, you should understand the following topics.</span></span>  

*   <span data-ttu-id="3bf42-117">Cómo HTML y DOM crean el contenido que se muestra en las páginas web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-117">How HTML and the DOM create the content that are displayed on webpages.</span></span>  
*   <span data-ttu-id="3bf42-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span><span class="sxs-lookup"><span data-stu-id="3bf42-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="3bf42-119">La diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="3bf42-120">También tiene un sitio web real.</span><span class="sxs-lookup"><span data-stu-id="3bf42-120">You also have a real website.</span></span>  <span data-ttu-id="3bf42-121">Puede usar el sitio para hospedar su currículum vitae o blog.</span><span class="sxs-lookup"><span data-stu-id="3bf42-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="3bf42-122">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3bf42-122">Prerequisites</span></span>  

<span data-ttu-id="3bf42-123">Antes de intentar este tutorial, complete los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="3bf42-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="3bf42-124">Si no está familiarizado con HTML, lea [Introducción a HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="3bf42-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="3bf42-125">Descargue el [Microsoft Edge][MicrosoftEdgeInsider] web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="3bf42-126">Este tutorial usa un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, integradas en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3bf42-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="3bf42-127">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="3bf42-127">Set up your code</span></span>  

<span data-ttu-id="3bf42-128">Va a crear el sitio en un editor de código en línea llamado Glitch.</span><span class="sxs-lookup"><span data-stu-id="3bf42-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="3bf42-129">Abra el [código fuente][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="3bf42-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="3bf42-130">Esta pestaña se denomina pestaña **editor a** lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="3bf42-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Pestaña editor" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="3bf42-132">Pestaña editor</span><span class="sxs-lookup"><span data-stu-id="3bf42-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-133">Elija **alluring-shock**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="3bf42-134">El menú Project opciones se abre en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="3bf42-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Menú Project opciones" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="3bf42-136">Menú Project opciones</span><span class="sxs-lookup"><span data-stu-id="3bf42-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-137">Elija **Remezcla Project**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="3bf42-138">Glitch crea una copia del proyecto que puede editar y genera aleatoriamente un nuevo nombre para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="3bf42-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="3bf42-139">El contenido es el mismo que antes.</span><span class="sxs-lookup"><span data-stu-id="3bf42-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="El proyecto remezclado" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="3bf42-141">El proyecto remezclado</span><span class="sxs-lookup"><span data-stu-id="3bf42-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-142">Si tienes previsto completar el siguiente tutorial \*\*\*\* de esta serie, elige Iniciar sesión e iniciar sesión en Glitch con tu cuenta GitHub o Facebook.</span><span class="sxs-lookup"><span data-stu-id="3bf42-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign into Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="3bf42-143">Si decide no iniciar sesión en su cuenta, perderá la capacidad de editar el proyecto después de cerrar la pestaña de edición.</span><span class="sxs-lookup"><span data-stu-id="3bf42-143">If you choose to not sign into your account, you lose the ability to edit the project after you close the editing tab.</span></span>  
1.  <span data-ttu-id="3bf42-144">Elija **Mostrar** y **elija En una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="3bf42-145">Se abre una pestaña nueva que muestra la página activa.</span><span class="sxs-lookup"><span data-stu-id="3bf42-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="3bf42-146">Esta pestaña se denomina pestaña **activa a** lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="3bf42-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="La pestaña activa" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="3bf42-148">La pestaña activa</span><span class="sxs-lookup"><span data-stu-id="3bf42-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="3bf42-149">Agregar contenido</span><span class="sxs-lookup"><span data-stu-id="3bf42-149">Add content</span></span>  

<span data-ttu-id="3bf42-150">El sitio está bastante vacío.</span><span class="sxs-lookup"><span data-stu-id="3bf42-150">Your site is pretty empty.</span></span>  <span data-ttu-id="3bf42-151">Siga los pasos siguientes para agregarle contenido.</span><span class="sxs-lookup"><span data-stu-id="3bf42-151">Follow the steps below to add some content to it.</span></span>  

1.  <span data-ttu-id="3bf42-152">En la **pestaña editor**, reemplace `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="3bf42-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="El nuevo código se resalta en la pestaña editor" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="3bf42-154">El nuevo código se resalta en la pestaña editor</span><span class="sxs-lookup"><span data-stu-id="3bf42-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="3bf42-155">Ver los cambios en la **pestaña activa**.  El texto `About Me` está visible en la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="3bf42-156">El texto es mayor que el texto que lo rodea, ya que `<h1>` el elemento representa un encabezado de sección.</span><span class="sxs-lookup"><span data-stu-id="3bf42-156">The text larger than the surrounding text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="3bf42-157">El explorador web aplica estilos automáticamente a los encabezados en tamaños de fuente más grandes.</span><span class="sxs-lookup"><span data-stu-id="3bf42-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="El nuevo encabezado está visible en la pestaña activa" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="3bf42-159">El nuevo encabezado está visible en la pestaña activa</span><span class="sxs-lookup"><span data-stu-id="3bf42-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-160">Vuelva a la **pestaña editor**, inserte en la línea siguiente donde acaba de `<p>I am learning HTML.  Recent accomplishments:</p>` colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="3bf42-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="El código actualizado se resalta en la pestaña editor" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="3bf42-162">El código actualizado se resalta en la pestaña editor</span><span class="sxs-lookup"><span data-stu-id="3bf42-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="3bf42-163">Ver el cambio en la **pestaña activa**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="3bf42-164">De vuelta en la **pestaña editor,** agregue una lista de sus logros:</span><span class="sxs-lookup"><span data-stu-id="3bf42-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="El código actualizado también se resalta en la pestaña editor" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="3bf42-166">El código actualizado también se resalta en la pestaña editor</span><span class="sxs-lookup"><span data-stu-id="3bf42-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="3bf42-167">De nuevo, vuelva a la **pestaña activa** para asegurarse de que el nuevo contenido se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="3bf42-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="La nueva lista está visible en la pestaña activa" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="3bf42-169">La nueva lista está visible en la pestaña activa</span><span class="sxs-lookup"><span data-stu-id="3bf42-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="3bf42-170">Experimentar con cambios de contenido en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3bf42-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3bf42-171">Si estaba desarrollando una página grande con mucho HTML, es algo tedioso ir y venir entre la pestaña editor y la pestaña activa cientos de veces para mostrar los cambios, especialmente si no está seguro de qué colocar exactamente en la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-171">If you were developing a big page with a lot of HTML, it is somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to display your changes, especially if you are unsure what exactly to put on the page.</span></span>  <span data-ttu-id="3bf42-172">Microsoft Edge DevTools le ayuda a experimentar con los cambios de contenido sin salir nunca de **la pestaña en directo.**</span><span class="sxs-lookup"><span data-stu-id="3bf42-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="3bf42-173">Obtenga información sobre la diferencia entre HTML y DOM</span><span class="sxs-lookup"><span data-stu-id="3bf42-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="3bf42-174">Antes de empezar a editar el contenido desde Microsoft Edge DevTools, debe comprender la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-174">Before you start editing your content from Microsoft Edge DevTools, you should understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="3bf42-175">La mejor manera de aprender es por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3bf42-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="3bf42-176">Vaya a la **pestaña activa**.  En la parte inferior de la página, se `A new element!?!` muestra el texto.</span><span class="sxs-lookup"><span data-stu-id="3bf42-176">Navigate to the **live tab**.  At the bottom of your page, the text `A new element!?!` is displayed.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="En la parte inferior de la página, el texto Un nuevo elemento!?! se muestra" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="3bf42-179">En la parte inferior de la página se `A new element!?!` muestra el texto</span><span class="sxs-lookup"><span data-stu-id="3bf42-179">At the bottom of the page the text `A new element!?!` is displayed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-180">Vuelva a la **pestaña editor e** intente encontrar el texto en `index.html` .</span><span class="sxs-lookup"><span data-stu-id="3bf42-180">Go back to the **editor tab** and try to find the text in `index.html`.</span></span>  <span data-ttu-id="3bf42-181">El texto no está ahí.</span><span class="sxs-lookup"><span data-stu-id="3bf42-181">The text is not there.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Texto misterioso Un nuevo elemento!?! no se encuentra en ninguna parte en index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="3bf42-184">El texto `A new element!?!` misterioso no se encuentra en ninguna parte</span><span class="sxs-lookup"><span data-stu-id="3bf42-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-185">Vuelva a la pestaña **activa**, mantenga el mouse sobre , abra el menú contextual \(haga clic con el `A new element!?!` botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-185">Go back to the **live tab**, hover on `A new element!?!`, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspección de texto" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="3bf42-187">Inspección de texto</span><span class="sxs-lookup"><span data-stu-id="3bf42-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="3bf42-188">DevTools se abre junto a la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="3bf42-189">se resalta en azul.</span><span class="sxs-lookup"><span data-stu-id="3bf42-189">is highlighted blue.</span></span>  <span data-ttu-id="3bf42-190">Aunque esta estructura en DevTools se parece al HTML, en realidad es el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools está abierto junto a la página" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="3bf42-192">DevTools está abierto junto a la página</span><span class="sxs-lookup"><span data-stu-id="3bf42-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3bf42-193">Cuando se carga la página, el explorador toma el HTML para crear el *contenido inicial* de la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="3bf42-194">El DOM representa el *contenido* actual de la página, que puede cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="3bf42-194">The DOM represents the *current* content of the page, which may change over time.</span></span>  <span data-ttu-id="3bf42-195">El contenido `<div>A new element!?!</div>` misterioso se agrega a tu página debido a la etiqueta en la parte inferior del `<script src="new.js"></script>` HTML.</span><span class="sxs-lookup"><span data-stu-id="3bf42-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="3bf42-196">Esta etiqueta hace que se ejecute algún código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3bf42-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="3bf42-197">Obtenga más información sobre JavaScript en un tutorial posterior, pero por ahora piense en él como un lenguaje de programación que puede cambiar el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-197">Learn more about JavaScript in a later tutorial, but for now think of it as a programming language that may change the content of your page.</span></span>  <span data-ttu-id="3bf42-198">En este caso concreto, el código JavaScript se `<div>A new element!?!</div>` agrega a la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="3bf42-199">Por eso, este texto misterioso está visible en la página en directo, pero no en el HTML.</span><span class="sxs-lookup"><span data-stu-id="3bf42-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="3bf42-200">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="3bf42-200">Edit the DOM</span></span>  

<span data-ttu-id="3bf42-201">Si quieres experimentar rápidamente con cambios de contenido sin salir de la pestaña en directo, prueba DevTools.</span><span class="sxs-lookup"><span data-stu-id="3bf42-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="3bf42-202">En DevTools, mantenga el mouse en , abra el menú contextual \(haga clic con el `Your site!` botón secundario\) y elija Editar como **HTML**.</span><span class="sxs-lookup"><span data-stu-id="3bf42-202">In DevTools, hover on `Your site!`, open the contextual menu \(right-click\), and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Edición del nodo como HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="3bf42-204">Edición del nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="3bf42-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-205">Reemplace `<p>Your site!</p>` por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="3bf42-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Actualización del nodo como HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="3bf42-207">Actualización del nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="3bf42-207">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="3bf42-208">Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\) para guardar los cambios o elija fuera del cuadro.</span><span class="sxs-lookup"><span data-stu-id="3bf42-208">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or choose outside of the box.</span></span>  <span data-ttu-id="3bf42-209">Los cambios se muestran automáticamente en la vista en directo de la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="3bf42-210">El texto `Your site!` se ha reemplazado por el nuevo contenido.</span><span class="sxs-lookup"><span data-stu-id="3bf42-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="El nuevo contenido se muestra inmediatamente en la página" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="3bf42-212">El nuevo contenido se muestra inmediatamente en la página</span><span class="sxs-lookup"><span data-stu-id="3bf42-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3bf42-213">Este flujo de trabajo solo es bueno para experimentar con cambios de contenido.</span><span class="sxs-lookup"><span data-stu-id="3bf42-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="3bf42-214">Si actualiza la página o cierra la pestaña, los cambios desaparecerán para siempre.</span><span class="sxs-lookup"><span data-stu-id="3bf42-214">If you refresh the page or close the tab, your changes are gone forever.</span></span>  <span data-ttu-id="3bf42-215">Si usa este flujo de trabajo y desea guardar los cambios, debe copiar manualmente esos cambios en su HTML.</span><span class="sxs-lookup"><span data-stu-id="3bf42-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="3bf42-216">En las siguientes secciones se muestran algunas formas más de cambiar el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-216">The next couple of sections show you some more ways that you may change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="3bf42-217">Reordenar nodos</span><span class="sxs-lookup"><span data-stu-id="3bf42-217">Reorder nodes</span></span>  

<span data-ttu-id="3bf42-218">También puede cambiar el orden de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-218">You may also change the order of DOM nodes.</span></span>  <span data-ttu-id="3bf42-219">Por ejemplo, en la página web, el menú de navegación está cerca de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="3bf42-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="3bf42-220">Para moverlo a la parte superior:</span><span class="sxs-lookup"><span data-stu-id="3bf42-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="3bf42-221">Busque el `<nav>` nodo en el árbol **DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3bf42-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="El nodo de navegación se resalta en azul en DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="3bf42-223">El nodo de navegación se resalta en azul en DevTools</span><span class="sxs-lookup"><span data-stu-id="3bf42-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-224">Arrastre el nodo a la parte superior, de modo `<nav>` que el nodo sea el primer elemento secundario del `<body>` nodo.</span><span class="sxs-lookup"><span data-stu-id="3bf42-224">Drag the `<nav>` node to the top, so that the node is the first child of the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="3bf42-225">El `<nav>` nodo se muestra ahora en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="3bf42-225">The `<nav>` node is now displaying at the top of your page.</span></span>  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Arrastrar el nodo de navegación a la parte superior" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="3bf42-227">Arrastrar el nodo de navegación a la parte superior</span><span class="sxs-lookup"><span data-stu-id="3bf42-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="El nodo de navegación está en la parte superior de la página" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="3bf42-229">El nodo de navegación está en la parte superior de la página</span><span class="sxs-lookup"><span data-stu-id="3bf42-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="3bf42-230">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="3bf42-230">Delete a node</span></span>  

<span data-ttu-id="3bf42-231">También puede quitar nodos del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-231">You may also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="3bf42-232">En el **árbol DOM,** elija `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="3bf42-232">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="3bf42-233">DevTools resalta el color azul del nodo.</span><span class="sxs-lookup"><span data-stu-id="3bf42-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Elegir el nodo que se va a eliminar" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="3bf42-235">Elegir el nodo que se va a eliminar</span><span class="sxs-lookup"><span data-stu-id="3bf42-235">Choose the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-236">Seleccione la `Delete` tecla del teclado.</span><span class="sxs-lookup"><span data-stu-id="3bf42-236">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="3bf42-237">El `<div>A new element!?!</div>` nodo se quita del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="El nodo se ha eliminado" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="3bf42-239">El nodo se ha eliminado</span><span class="sxs-lookup"><span data-stu-id="3bf42-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="3bf42-240">Copiar los cambios</span><span class="sxs-lookup"><span data-stu-id="3bf42-240">Copy your changes</span></span>  

<span data-ttu-id="3bf42-241">Casi ha terminado.</span><span class="sxs-lookup"><span data-stu-id="3bf42-241">You're almost done.</span></span>  <span data-ttu-id="3bf42-242">Has realizado algunos cambios en tu página en DevTools, pero aún no se guardan en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="3bf42-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="3bf42-243">Actualice la **pestaña activa**.  Los cambios realizados en el árbol DOM desaparecen.</span><span class="sxs-lookup"><span data-stu-id="3bf42-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="3bf42-244">En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto vuelve a la parte `A new element!?!` inferior.</span><span class="sxs-lookup"><span data-stu-id="3bf42-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Los cambios que ha realizado han desaparecido" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="3bf42-246">Los cambios que ha realizado han desaparecido</span><span class="sxs-lookup"><span data-stu-id="3bf42-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3bf42-247">Copie el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="3bf42-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="3bf42-248">Vuelva a la **pestaña editor y** reemplace el contenido del archivo por el código que acaba de `index.html` copiar.</span><span class="sxs-lookup"><span data-stu-id="3bf42-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Cómo debe index.htmel archivo l" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="3bf42-250">Aspecto del `index.html` archivo</span><span class="sxs-lookup"><span data-stu-id="3bf42-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="3bf42-251">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="3bf42-251">Next steps</span></span>  

*   <span data-ttu-id="3bf42-252">Complete el siguiente tutorial de esta serie, [Introducción con CSS][DevToolsBeginnersCss], para aprender a dar estilo a su página y experimentar con los cambios de estilo en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3bf42-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="3bf42-253">Lea [Introducción al DOM][MDNIntroductionDom] para obtener más información sobre el DOM.</span><span class="sxs-lookup"><span data-stu-id="3bf42-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="3bf42-254">Consulte un curso como [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia práctica en el desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="3bf42-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3bf42-255">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3bf42-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para principiantes: Introducción con CSS | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html- alluring-shock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a html | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción al dom | MDN"  

> [!NOTE]
> <span data-ttu-id="3bf42-262">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3bf42-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3bf42-263">La página original se encontró [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y fue creado por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="3bf42-263">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3bf42-265">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3bf42-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
