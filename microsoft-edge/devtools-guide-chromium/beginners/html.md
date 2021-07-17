---
description: Introducción a HTML y el DOM
title: 'DevTools para principiantes: Introducción a HTML y el DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, devtools para principiantes, devtools de HTML para principiantes, devtools del DOM para principiantes, tutorial de devtools de html, tutorial de devtools del DOM, tutorial de devtools del document object model
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643572"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="1c4c3-104">DevTools para principiantes: Introducción a HTML y el DOM</span><span class="sxs-lookup"><span data-stu-id="1c4c3-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="1c4c3-105">Este es el primero de una serie de tutoriales que le enseñarán los conceptos básicos del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span> <span data-ttu-id="1c4c3-106">Obtenga información sobre un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, que pueden aumentar su productividad.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="1c4c3-107">En este tutorial se describe HTML y el [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="1c4c3-107">This tutorial describes HTML and the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span></span> <span data-ttu-id="1c4c3-108">HTML es una de las tecnologías principales del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-108">HTML is one of the core technologies of web development.</span></span> <span data-ttu-id="1c4c3-109">Es el lenguaje que controla la estructura y el contenido de las páginas web.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-109">It is the language that controls the structure and content of webpages.</span></span> <span data-ttu-id="1c4c3-110">El DOM también está relacionado con la estructura y el contenido de las páginas web, sobre los que aprenderemos más adelante.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-110">The DOM is also related to the structure and content of webpages, which we learn more about later.</span></span>

## <a name="goals"></a><span data-ttu-id="1c4c3-111">Objetivos</span><span class="sxs-lookup"><span data-stu-id="1c4c3-111">Goals</span></span>  

<span data-ttu-id="1c4c3-112">Aprenderá desarrollo web mediante la creación de un sitio web.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-112">You're going to learn web development by building a website.</span></span>  <span data-ttu-id="1c4c3-113">Cuando complete todos los tutoriales de la serie **DevTools para principiantes**, el sitio terminado puede tener un aspecto similar al de la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="El sitio terminado" lightbox="media/beginners-html-finished.msft.png":::
   <span data-ttu-id="1c4c3-115">El sitio terminado</span><span class="sxs-lookup"><span data-stu-id="1c4c3-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="1c4c3-116">Al final de este tutorial, debe comprender los siguientes conceptos.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-116">By the end of this tutorial, you should understand the following concepts.</span></span>  

*   <span data-ttu-id="1c4c3-117">Cómo HTML y el DOM crean el contenido que se muestra en las páginas web.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-117">How HTML and the DOM create the content displayed on webpages.</span></span>  
*   <span data-ttu-id="1c4c3-118">Cómo Microsoft Edge DevTools puede ayudarle a experimentar con los cambios de HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="1c4c3-119">Diferencia entre HTML y el DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="1c4c3-120">También tendrá un sitio web en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-120">You will also have a working website.</span></span> <span data-ttu-id="1c4c3-121">Puede usar el sitio para hospedar su currículo o blog.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="1c4c3-122">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1c4c3-122">Prerequisites</span></span>  

<span data-ttu-id="1c4c3-123">Antes de iniciar este tutorial, complete los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="1c4c3-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="1c4c3-124">Si no está familiarizado con HTML, lea [Tareas iniciales con HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="1c4c3-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="1c4c3-125">Descargue el explorador web [Microsoft Edge][MicrosoftEdgeInsider].</span><span class="sxs-lookup"><span data-stu-id="1c4c3-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="1c4c3-126">En este tutorial se usa un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, que están integradas en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="1c4c3-127">Configurar el código</span><span class="sxs-lookup"><span data-stu-id="1c4c3-127">Set up your code</span></span>  

<span data-ttu-id="1c4c3-128">Va a crear un sitio en el editor de código en línea Glitch.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-128">You are going to build a site in the Glitch online code editor.</span></span>  

1.  <span data-ttu-id="1c4c3-129">Abra el [código fuente][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="1c4c3-129">Open the [source code][GlitchAlluringShockIndex].</span></span> <span data-ttu-id="1c4c3-130">Esta pestaña se denomina **pestaña del editor** a lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="La pestaña del editor" lightbox="media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="1c4c3-132">La pestaña del editor</span><span class="sxs-lookup"><span data-stu-id="1c4c3-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c4c3-133">Elija **alluring-shock**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-133">Choose **alluring-shock**.</span></span> <span data-ttu-id="1c4c3-134">Se abre el menú**Opciones del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-134">The **Project Options** menu opens.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menú Opciones del proyecto" lightbox="media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="1c4c3-136">Menú Opciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="1c4c3-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c4c3-137">Elija **Replicar proyecto**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-137">Choose **Remix Project**.</span></span> <span data-ttu-id="1c4c3-138">Glitch crea una copia del proyecto que puede editar y genera aleatoriamente un nuevo nombre para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span> <span data-ttu-id="1c4c3-139">El contenido es el mismo que antes.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="El proyecto replicado" lightbox="media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="1c4c3-141">El proyecto replicado</span><span class="sxs-lookup"><span data-stu-id="1c4c3-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c4c3-142">Si tiene previsto completar el siguiente tutorial de esta serie, elija **Iniciar sesión** en Glitch con su cuenta de Facebook, GitHub o Google; o envíese un vínculo mágico por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-142">If you plan to complete the next tutorial in this series, choose **Sign In** to Glitch using your Facebook, GitHub, or Google account; or email yourself a magic link.</span></span> <span data-ttu-id="1c4c3-143">Si decide no iniciar sesión en una cuenta, no podrá editar el proyecto después de cerrar la pestaña del editor.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-143">If you choose not to sign in to an account, you cannot edit the project after closing the editor tab.</span></span>

1.  <span data-ttu-id="1c4c3-144">Elija **Mostrar** \> **En una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-144">Choose **Show** \> **In a New Window**.</span></span>  <span data-ttu-id="1c4c3-145">Se abre una nueva pestaña que muestra la página en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-145">A new tab opens, showing the live page.</span></span> <span data-ttu-id="1c4c3-146">Esta pestaña se denomina **pestaña en tiempo real** a lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="La pestaña en tiempo real" lightbox="media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="1c4c3-148">La pestaña en tiempo real</span><span class="sxs-lookup"><span data-stu-id="1c4c3-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="1c4c3-149">Agregar contenido</span><span class="sxs-lookup"><span data-stu-id="1c4c3-149">Add content</span></span>  

<span data-ttu-id="1c4c3-150">El sitio necesita más información.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-150">Your site needs more information.</span></span> <span data-ttu-id="1c4c3-151">Complete los siguientes pasos para agregar contenido.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-151">Complete the following steps to add some content.</span></span>  

1. <span data-ttu-id="1c4c3-152">En la **pestaña del editor**, reemplace `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>`.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="El nuevo código está resaltado en la pestaña del editor" lightbox="media/beginners-html-add1.msft.png":::
        <span data-ttu-id="1c4c3-154">El nuevo código está resaltado en la pestaña del editor</span><span class="sxs-lookup"><span data-stu-id="1c4c3-154">The new code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="1c4c3-155">Vea los cambios en la **pestaña en tiempo real**. El texto `About Me` está visible en la página.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-155">View your changes in the **live tab**. The text `About Me` is visible on the page.</span></span> <span data-ttu-id="1c4c3-156">El texto es mayor que el texto adyacente porque el elemento `<h1>` representa un Título 1.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-156">The text is larger than the surrounding text because the `<h1>` element represents a Heading 1.</span></span>  <span data-ttu-id="1c4c3-157">El explorador web aplica estilos automáticamente a los títulos en tamaños de fuente más grandes.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="El nuevo título está visible en la pestaña en tiempo real" lightbox="media/beginners-html-add2.msft.png":::
       <span data-ttu-id="1c4c3-159">El nuevo título está visible en la pestaña en tiempo real</span><span class="sxs-lookup"><span data-stu-id="1c4c3-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="1c4c3-160">De nuevo en la **pestaña del editor**, inserte `<p>I am learning web development. Recent accomplishments:</p>` en la línea después de  `<h1>About Me</h1>`.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-160">Back in the **editor tab**, insert `<p>I am learning web development. Recent accomplishments:</p>` on the line below  `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="El código actualizado está resaltado en la pestaña del editor" lightbox="media/beginners-html-add3.msft.png":::
        <span data-ttu-id="1c4c3-162">El código actualizado está resaltado en la pestaña del editor</span><span class="sxs-lookup"><span data-stu-id="1c4c3-162">The updated code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="1c4c3-163">Vea el cambio en la **pestaña en tiempo real**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-163">View your change in the **live tab**.</span></span>

1. <span data-ttu-id="1c4c3-164">De nuevo en la **pestaña del editor**, agregue una lista de sus logros con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-164">Back in the **editor tab**, add a list of your accomplishments using the following code.</span></span>
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="El código actualizado también está resaltado en la pestaña del editor" lightbox="media/beginners-html-add4.msft.png":::
        <span data-ttu-id="1c4c3-166">El código actualizado también está resaltado en la pestaña del editor</span><span class="sxs-lookup"><span data-stu-id="1c4c3-166">The updated code is also highlighted in the editor tab</span></span>  
    :::image-end:::  

1. <span data-ttu-id="1c4c3-167">Vea la **pestaña en tiempo real** para asegurarse de que el nuevo contenido se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-167">View the **live tab** to make sure that the new content displays correctly.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="La nueva lista está visible en la pestaña en tiempo real" lightbox="media/beginners-html-add5.msft.png":::
       <span data-ttu-id="1c4c3-169">La nueva lista está visible en la pestaña en tiempo real</span><span class="sxs-lookup"><span data-stu-id="1c4c3-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="1c4c3-170">Experimentar con los cambios de contenido en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c4c3-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="1c4c3-171">Si está desarrollando una página con mucho HTML, resulta tedioso ir y retroceder entre la pestaña del editor y la pestaña en tiempo real para ver los cambios.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-171">If you are developing a page with a lot of HTML, it becomes tedious to go back-and-forth between the editor tab and the live tab to see your changes.</span></span> <span data-ttu-id="1c4c3-172">Microsoft Edge DevTools le ayuda a experimentar con los cambios de contenido sin salir de la **pestaña en tiempo real**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="1c4c3-173">Conozca la diferencia entre HTML y el DOM</span><span class="sxs-lookup"><span data-stu-id="1c4c3-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="1c4c3-174">Antes de editar el contenido de Microsoft Edge DevTools, vamos a comprender la diferencia entre HTML y el DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-174">Before editing content from Microsoft Edge DevTools, let's understand the difference between HTML and the DOM.</span></span> <span data-ttu-id="1c4c3-175">Continúe con los siguientes pasos para aprender a partir de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-175">Proceed with the following steps to learn from an example.</span></span>

1. <span data-ttu-id="1c4c3-176">Vaya a la **pestaña en tiempo real**. En la parte inferior de la página, se mostrará el texto `A new element!?!`.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-176">Navigate to the **live tab**. At the bottom of your page, the text `A new element!?!` displays.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. <span data-ttu-id="1c4c3-177">Abra la **pestaña del editor** e intente encontrar el texto en `index.html`.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-177">Open the **editor tab** and try to find the text in `index.html`.</span></span> <span data-ttu-id="1c4c3-178">El texto no se muestra en esta vista.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-178">The text does not display in this view.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. <span data-ttu-id="1c4c3-179">Abra la **pestaña en tiempo real**, mantenga el puntero sobre `A new element!?!`, abra el menú contextual (haga clic con el botón derecho) y, a continuación, elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-179">Open the **live tab**, hover over `A new element!?!`, open the contextual menu (right-click) and then choose **Inspect**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Inspeccionando texto" lightbox="media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="1c4c3-181">Inspeccionando texto</span><span class="sxs-lookup"><span data-stu-id="1c4c3-181">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="1c4c3-182">DevTools se abrirá junto a la página.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-182">DevTools opens up alongside your page.</span></span> `<div>A new element!?!</div>` <span data-ttu-id="1c4c3-183">está resaltado.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-183">is highlighted.</span></span> <span data-ttu-id="1c4c3-184">Aunque esta estructura de DevTools se parece a HTML, es el **árbol del DOM**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-184">Although this structure in DevTools looks like HTML, it is the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools está abierto junto a la página" lightbox="media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="1c4c3-186">DevTools está abierto junto a la página</span><span class="sxs-lookup"><span data-stu-id="1c4c3-186">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1c4c3-187">Cuando se carga la página, el explorador usa el código HTML para crear el contenido inicial de la página.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-187">When your page loads, the browser uses the HTML to create the initial content of the page.</span></span> <span data-ttu-id="1c4c3-188">El DOM representa el contenido actual de la página, que puede cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-188">The DOM represents the current content of the page, which may change over time.</span></span> 

<span data-ttu-id="1c4c3-189">El contenido de `<div>A new element!?!</div>` se agrega a la página debido a la etiqueta `<script src="new.js"></script>` en la parte inferior del código HTML.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-189">The `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span> <span data-ttu-id="1c4c3-190">Esta etiqueta hace que se ejecute algún código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-190">This tag causes some JavaScript code to run.</span></span> <span data-ttu-id="1c4c3-191">Obtenga más información sobre JavaScript en un [tutorial posterior](../javascript/index.md).</span><span class="sxs-lookup"><span data-stu-id="1c4c3-191">Learn more about JavaScript in a [later tutorial](../javascript/index.md).</span></span>

<span data-ttu-id="1c4c3-192">Por ahora, piense en él como un lenguaje de computación que puede cambiar el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-192">For now, think of it as a scripting language that may change the content of your page.</span></span> <span data-ttu-id="1c4c3-193">En este caso, el código JavaScript agrega `<div>A new element!?!</div>` a la página.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-193">In this case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span> <span data-ttu-id="1c4c3-194">Este es el motivo por el que este texto se muestra en la pestaña **en tiempo real**, pero no en el código HTML.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-194">That is why this text is displayed in the **live** tab, but not in the HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="1c4c3-195">Edición del DOM</span><span class="sxs-lookup"><span data-stu-id="1c4c3-195">Edit the DOM</span></span>  

<span data-ttu-id="1c4c3-196">Si quiere experimentar rápidamente con los cambios de contenido sin salir de la pestaña en tiempo real, pruebe DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-196">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="1c4c3-197">En DevTools, mantenga el puntero sobre `Your site!`, abra el menú contextual (clic con el botón derecho) y elija **Editar como HTML**.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-197">In DevTools, hover over `Your site!`, open the contextual menu (right-click) and choose **Edit as HTML**.</span></span>  
    
1.  <span data-ttu-id="1c4c3-198">Reemplace `<p>Your site!</p>` por el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-198">Replace `<p>Your site!</p>` with the following code.</span></span>  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Actualización del nodo como HTML" lightbox="media/beginners-html-edit2.msft.png":::
    <span data-ttu-id="1c4c3-200">Actualización del nodo como HTML</span><span class="sxs-lookup"><span data-stu-id="1c4c3-200">Updating the node as HTML</span></span>  
<span data-ttu-id="1c4c3-201">::image-end:::</span><span class="sxs-lookup"><span data-stu-id="1c4c3-201">::image-end:::</span></span>  

1.  <span data-ttu-id="1c4c3-202">Seleccione `Control`+`Enter` \(Windows, Linux\) o `Command`+`Enter` \(macOS\) para guardar los cambios, o seleccione fuera del cuadro.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-202">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or select outside the box.</span></span> <span data-ttu-id="1c4c3-203">Los cambios se muestran automáticamente en la vista en tiempo real de la página.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-203">Your changes automatically show up in the live view of your page.</span></span> <span data-ttu-id="1c4c3-204">El texto `Your site!` se ha reemplazado por el nuevo contenido.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-204">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="El nuevo contenido se muestra inmediatamente en la página" lightbox="media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="1c4c3-206">El nuevo contenido se muestra inmediatamente en la página</span><span class="sxs-lookup"><span data-stu-id="1c4c3-206">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1c4c3-207">Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-207">This workflow is only suitable for experimenting with content changes.</span></span> <span data-ttu-id="1c4c3-208">Si actualiza la página o cierra la pestaña, se perderán los cambios.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-208">If you refresh the page or close the tab, your changes are lost.</span></span> <span data-ttu-id="1c4c3-209">Si desea guardar los cambios, copie manualmente el código en el archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-209">If you want to save your changes, manually copy the code to your HTML file.</span></span> <span data-ttu-id="1c4c3-210">En las dos secciones siguientes se muestran otras formas de cambiar el contenido del árbol del DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-210">The next couple of sections show you some more ways to change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="1c4c3-211">Reordenar nodos</span><span class="sxs-lookup"><span data-stu-id="1c4c3-211">Reorder nodes</span></span>

<span data-ttu-id="1c4c3-212">También puede cambiar el orden de los nodos del DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-212">You may also change the order of DOM nodes.</span></span> <span data-ttu-id="1c4c3-213">Por ejemplo, en la página web, el menú de navegación está cerca de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-213">For example, on your web page the navigation menu is near the bottom.</span></span> <span data-ttu-id="1c4c3-214">Para moverlo a la parte superior, realice los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-214">To move it to the top, perform the following steps.</span></span>  

1.  <span data-ttu-id="1c4c3-215">Busque el nodo `<nav>` en el **árbol del DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-215">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="El nodo de navegación está resaltado en DevTools" lightbox="media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="1c4c3-217">El nodo de navegación está resaltado en DevTools</span><span class="sxs-lookup"><span data-stu-id="1c4c3-217">The nav node is highlighted in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c4c3-218">Arrastre el nodo `<nav>` a la parte superior para que el nodo sea el primer elemento secundario después del nodo `<body>`.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-218">Drag the `<nav>` node to the top, so that the node is the first child after the `<body>` node.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="El nodo de navegación está en la parte superior de la página" lightbox="media/beginners-html-reorder3.msft.png":::
        <span data-ttu-id="1c4c3-220">El nodo de navegación está en la parte superior de la página</span><span class="sxs-lookup"><span data-stu-id="1c4c3-220">The nav node is at the top of the page</span></span>  
    :::image-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="1c4c3-221">Eliminación de un nodo</span><span class="sxs-lookup"><span data-stu-id="1c4c3-221">Delete a node</span></span>

<span data-ttu-id="1c4c3-222">También puede quitar nodos del árbol del DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-222">You may also remove nodes from the DOM Tree.</span></span> <span data-ttu-id="1c4c3-223">Para ello, realice los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="1c4c3-223">Perform the following steps.</span></span>

1.  <span data-ttu-id="1c4c3-224">En el **árbol del DOM**, elija `<div>A new element!?!</div>`.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-224">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span> <span data-ttu-id="1c4c3-225">DevTools resaltará el nodo.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-225">DevTools highlights the node.</span></span> 
    
1.  <span data-ttu-id="1c4c3-226">Seleccione la tecla `Delete` del teclado.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-226">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="1c4c3-227">El nodo `<div>A new element!?!</div>` se quitará del árbol del DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-227">The `<div>A new element!?!</div>` node is removed from the DOM Tree.</span></span>  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="El nodo se ha eliminado" lightbox="media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="1c4c3-229">El nodo se ha eliminado</span><span class="sxs-lookup"><span data-stu-id="1c4c3-229">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="1c4c3-230">Copie los cambios</span><span class="sxs-lookup"><span data-stu-id="1c4c3-230">Copy your changes</span></span>  

<span data-ttu-id="1c4c3-231">Ya casi ha terminado.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-231">You're almost done.</span></span> <span data-ttu-id="1c4c3-232">Ha realizado algunos cambios a la página en DevTools, pero estos no se guardan en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-232">You made a few changes to the page in DevTools, but they're not saved to your source code.</span></span>  

1.  <span data-ttu-id="1c4c3-233">Actualice la **pestaña en tiempo real**. Los cambios realizados en el árbol DOM desaparecerán.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-233">Refresh the **live tab**. The changes that you made in the DOM Tree disappear.</span></span> <span data-ttu-id="1c4c3-234">En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto `A new element!?!` vuelve a la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-234">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Los cambios realizados han desaparecido" lightbox="media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="1c4c3-236">Los cambios realizados han desaparecido</span><span class="sxs-lookup"><span data-stu-id="1c4c3-236">The changes that you made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c4c3-237">Copie el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-237">Copy the following code.</span></span>  
    
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
    
1.  <span data-ttu-id="1c4c3-238">Vuelva a la **pestaña del editor** y reemplace el contenido del archivo `index.html` por el código que copió.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-238">Go back to the **editor tab** and replace the content of your `index.html` file with the code that you copied.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Aspecto que debería tener el archivo index.html" lightbox="media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="1c4c3-240">El aspecto que debería tener el archivo `index.html`</span><span class="sxs-lookup"><span data-stu-id="1c4c3-240">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="1c4c3-241">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="1c4c3-241">Next steps</span></span>  

*   <span data-ttu-id="1c4c3-242">Complete el siguiente tutorial en esta serie, [Introducción a CSS][DevToolsBeginnersCss], para aprender a aplicar estilo a la página y experimentar con cambios de estilo en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-242">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="1c4c3-243">Lea [Introducción al DOM][MDNIntroductionDom] para obtener más información sobre el DOM.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-243">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="1c4c3-244">Consulte un curso como [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia práctica de desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="1c4c3-244">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] for more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1c4c3-245">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c4c3-245">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para principiantes: Introducción a CSS | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - alluring-shock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción al DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="1c4c3-252">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c4c3-252">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1c4c3-253">La página original se encontró [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y fue creada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="1c4c3-253">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1c4c3-255">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c4c3-255">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
