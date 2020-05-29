---
title: Inspeccionar animaciones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574478"
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





# <span data-ttu-id="29ad3-103">Inspeccionar animaciones</span><span class="sxs-lookup"><span data-stu-id="29ad3-103">Inspect animations</span></span>   



<span data-ttu-id="29ad3-104">Inspeccione y modifique las animaciones con el inspector de animación de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="29ad3-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

> ##### <span data-ttu-id="29ad3-105">Figura 1</span><span class="sxs-lookup"><span data-stu-id="29ad3-105">Figure 1</span></span>  
> <span data-ttu-id="29ad3-106">Inspector de animación</span><span class="sxs-lookup"><span data-stu-id="29ad3-106">Animation inspector</span></span>  
> ![Inspector de animación][ImageAnimationInspector]  

### <span data-ttu-id="29ad3-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="29ad3-108">Summary</span></span>  

*   <span data-ttu-id="29ad3-109">Capture animaciones abriendo el inspector de animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="29ad3-110">El inspector de animación detecta y ordena automáticamente las animaciones en grupos.</span><span class="sxs-lookup"><span data-stu-id="29ad3-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="29ad3-111">Inspeccione las animaciones y reduzca la velocidad de cada una de ellas, reproduzca cada una o vea el código de origen.</span><span class="sxs-lookup"><span data-stu-id="29ad3-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="29ad3-112">Modifique las animaciones cambiando los intervalos, el retraso, la duración o los desplazamientos de los fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="29ad3-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="29ad3-113">Introducción</span><span class="sxs-lookup"><span data-stu-id="29ad3-113">Overview</span></span>   

<span data-ttu-id="29ad3-114">El inspector de animación de Microsoft Edge DevTools tiene dos propósitos principales.</span><span class="sxs-lookup"><span data-stu-id="29ad3-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="29ad3-115">Inspeccionar animaciones.</span><span class="sxs-lookup"><span data-stu-id="29ad3-115">Inspecting animations.</span></span>  <span data-ttu-id="29ad3-116">Desea ralentizar, reproducir o inspeccionar el código fuente de un grupo de animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="29ad3-117">Modificar animaciones.</span><span class="sxs-lookup"><span data-stu-id="29ad3-117">Modifying animations.</span></span>  <span data-ttu-id="29ad3-118">Desea modificar el intervalo, el retraso, la duración o los desplazamientos de los fotogramas clave de un grupo de animaciones.</span><span class="sxs-lookup"><span data-stu-id="29ad3-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="29ad3-119">Actualmente, no se admite la edición de curvas y la edición de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="29ad3-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="29ad3-120">El inspector de animación admite animaciones CSS, transiciones CSS y animaciones web.</span><span class="sxs-lookup"><span data-stu-id="29ad3-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="29ad3-121">Actualmente, no se admiten las animaciones.</span><span class="sxs-lookup"><span data-stu-id="29ad3-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="29ad3-122">¿Qué es un grupo de animación?</span><span class="sxs-lookup"><span data-stu-id="29ad3-122">What is an Animation Group?</span></span>  

<span data-ttu-id="29ad3-123">Un grupo de animación es un grupo de animaciones que pueden estar relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="29ad3-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="29ad3-124">Por el momento, la web no tiene ningún concepto real de animación grupal, por lo que los diseñadores y los programadores de movimiento tienen que componer animaciones individuales para que las animaciones se representen como un efecto visual coherente.</span><span class="sxs-lookup"><span data-stu-id="29ad3-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="29ad3-125">El inspector de animación predice qué animaciones se relacionan según el tiempo de Inicio \ (excluyendo demoras, etc. \).</span><span class="sxs-lookup"><span data-stu-id="29ad3-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="29ad3-126">El inspector de animación también agrupa las animaciones en paralelo.</span><span class="sxs-lookup"><span data-stu-id="29ad3-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="29ad3-127">En otras palabras, se agrupan juntos un conjunto de animaciones que se desencadenan en el mismo bloque de script.</span><span class="sxs-lookup"><span data-stu-id="29ad3-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="29ad3-128">Si una animación es asincrónica, se coloca en un grupo independiente.</span><span class="sxs-lookup"><span data-stu-id="29ad3-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="29ad3-129">Comenzar</span><span class="sxs-lookup"><span data-stu-id="29ad3-129">Get started</span></span>  

<span data-ttu-id="29ad3-130">Hay dos formas de abrir el inspector de animación:</span><span class="sxs-lookup"><span data-stu-id="29ad3-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="29ad3-131">Abrir el menú de **DevTools personalizar y controlar**</span><span class="sxs-lookup"><span data-stu-id="29ad3-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="29ad3-132">Vaya al submenú **más herramientas** .</span><span class="sxs-lookup"><span data-stu-id="29ad3-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="29ad3-133">Seleccione **animaciones**:</span><span class="sxs-lookup"><span data-stu-id="29ad3-133">Select **Animations**:</span></span>  
        
        > ##### <span data-ttu-id="29ad3-134">Figura 2</span><span class="sxs-lookup"><span data-stu-id="29ad3-134">Figure 2</span></span>  
        > <span data-ttu-id="29ad3-135">Animaciones a través del menú principal</span><span class="sxs-lookup"><span data-stu-id="29ad3-135">Animations via Main Menu</span></span>  
        > ![Animaciones a través del menú principal][ImageAnimationsViaMainMenu]  
        
*   <span data-ttu-id="29ad3-137">Abrir el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="29ad3-137">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="29ad3-138">Escribe `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="29ad3-138">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="29ad3-139">El inspector de animación se abre como una pestaña junto al cajón de consola.</span><span class="sxs-lookup"><span data-stu-id="29ad3-139">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="29ad3-140">Como el inspector de animación es una pestaña de cajón, puede usar el inspector de animación desde cualquier panel de DevTools.</span><span class="sxs-lookup"><span data-stu-id="29ad3-140">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

> ##### <span data-ttu-id="29ad3-141">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="29ad3-141">Figure 3</span></span>  
> <span data-ttu-id="29ad3-142">Inspector de animación vacío</span><span class="sxs-lookup"><span data-stu-id="29ad3-142">Empty Animation Inspector</span></span>  
> ![Inspector de animación vacío][ImageEmptyAnimationInspector]  

<span data-ttu-id="29ad3-144">El inspector de animación se agrupa en cuatro secciones principales \ (o paneles \).</span><span class="sxs-lookup"><span data-stu-id="29ad3-144">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="29ad3-145">En esta guía se hace referencia a cada panel de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="29ad3-145">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="29ad3-146">Panel</span><span class="sxs-lookup"><span data-stu-id="29ad3-146">Pane</span></span> | <span data-ttu-id="29ad3-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="29ad3-147">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="29ad3-148">uno</span><span class="sxs-lookup"><span data-stu-id="29ad3-148">1</span></span> | **<span data-ttu-id="29ad3-149">Controles</span><span class="sxs-lookup"><span data-stu-id="29ad3-149">Controls</span></span>** | <span data-ttu-id="29ad3-150">Desde aquí puede borrar todos los grupos de animación capturados actualmente o cambiar la velocidad del grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="29ad3-150">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="29ad3-151">1</span><span class="sxs-lookup"><span data-stu-id="29ad3-151">2</span></span> | **<span data-ttu-id="29ad3-152">Introducción</span><span class="sxs-lookup"><span data-stu-id="29ad3-152">Overview</span></span>** | <span data-ttu-id="29ad3-153">Seleccione un grupo de animación aquí para inspeccionarlo y modificarlo en el panel de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="29ad3-153">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="29ad3-154">2</span><span class="sxs-lookup"><span data-stu-id="29ad3-154">3</span></span> | **<span data-ttu-id="29ad3-155">Línea de tiempo</span><span class="sxs-lookup"><span data-stu-id="29ad3-155">Timeline</span></span>** | <span data-ttu-id="29ad3-156">PAUSE e inicie una animación desde aquí, o vaya a un punto específico de la animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-156">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="29ad3-157">cuatro</span><span class="sxs-lookup"><span data-stu-id="29ad3-157">4</span></span> | **<span data-ttu-id="29ad3-158">Detalles</span><span class="sxs-lookup"><span data-stu-id="29ad3-158">Details</span></span>** | <span data-ttu-id="29ad3-159">Inspeccionar y modificar el grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="29ad3-159">Inspect and modify the currently selected Animation Group.</span></span> |  

> ##### <span data-ttu-id="29ad3-160">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="29ad3-160">Figure 4</span></span>  
> <span data-ttu-id="29ad3-161">Inspector de animación con anotaciones</span><span class="sxs-lookup"><span data-stu-id="29ad3-161">Annotated Animation Inspector</span></span>  
> ![Inspector de animación con anotaciones][ImageAnnotatedAnimationInspector]  

<span data-ttu-id="29ad3-163">Para capturar una animación, solo tiene que realizar la interacción que desencadena la animación mientras el inspector de animación está abierto.</span><span class="sxs-lookup"><span data-stu-id="29ad3-163">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="29ad3-164">Si se desencadena una animación durante la carga de la página, vuelva a cargar la página con el inspector de animación abierto para detectar la animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-164">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="29ad3-165">Inspeccionar animaciones</span><span class="sxs-lookup"><span data-stu-id="29ad3-165">Inspect animations</span></span>   

<span data-ttu-id="29ad3-166">Una vez capturada una animación, hay varias maneras de reproducirla:</span><span class="sxs-lookup"><span data-stu-id="29ad3-166">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="29ad3-167">Mantenga el mouse sobre la miniatura en el panel de **información general** para ver una vista previa de ella.</span><span class="sxs-lookup"><span data-stu-id="29ad3-167">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="29ad3-168">Seleccione el grupo animación en el panel de **Descripción general** \ (para que se muestre en el panel de **detalles** \) y pulse el icono **reproducir** volver a ![ reproducir ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="29ad3-168">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** ![replay icon][ImageReplayButtonIcon] icon.</span></span>  <span data-ttu-id="29ad3-169">La animación se reproduce en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="29ad3-169">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="29ad3-170">Haga clic en los iconos de iconos de velocidad de animación **velocidad** de animación ![ ][ImageAnimationSpeedButtonsIcon] para cambiar la velocidad de vista previa del grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="29ad3-170">Click on the **animation speed** ![animation speed icons][ImageAnimationSpeedButtonsIcon] icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="29ad3-171">Puede usar la barra vertical roja para cambiar la posición actual.</span><span class="sxs-lookup"><span data-stu-id="29ad3-171">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="29ad3-172">Haga clic y arrastre la barra vertical roja para borrar la animación de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="29ad3-172">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  

### <span data-ttu-id="29ad3-173">Ver detalles de la animación</span><span class="sxs-lookup"><span data-stu-id="29ad3-173">View animation details</span></span>  

<span data-ttu-id="29ad3-174">Después de capturar un grupo de animaciones, haga clic en él en el panel de **información general** para ver los detalles.</span><span class="sxs-lookup"><span data-stu-id="29ad3-174">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="29ad3-175">En el panel **detalles** , se asigna una fila a cada animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-175">In the **Details** pane each individual animation is assigned the a row.</span></span>  

> ##### <span data-ttu-id="29ad3-176">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="29ad3-176">Figure 5</span></span>  
> <span data-ttu-id="29ad3-177">Detalles del grupo animación</span><span class="sxs-lookup"><span data-stu-id="29ad3-177">Animation Group details</span></span>  
> ![Detalles del grupo animación][ImageAnimationGroupDetails]  

<span data-ttu-id="29ad3-179">Mantenga el mouse sobre una animación para resaltarla en el área de visualización.</span><span class="sxs-lookup"><span data-stu-id="29ad3-179">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="29ad3-180">Haga clic en la animación para seleccionarla en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="29ad3-180">Click on the animation to select it in the **Elements** panel.</span></span>  

> ##### <span data-ttu-id="29ad3-181">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="29ad3-181">Figure 6</span></span>  
> <span data-ttu-id="29ad3-182">Desplace el puntero sobre la animación para resaltarla en el área de visualización</span><span class="sxs-lookup"><span data-stu-id="29ad3-182">Hover over the animation to highlight it in viewport</span></span>  
> ![Desplace el puntero sobre la animación para resaltarla en el área de visualización][ImageHoverOverAnimationHighlightViewport]  

<span data-ttu-id="29ad3-184">La definición más a la izquierda es la más oscura de una animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-184">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="29ad3-185">La sección derecha, más atenuada representa las iteraciones.</span><span class="sxs-lookup"><span data-stu-id="29ad3-185">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="29ad3-186">Por ejemplo, en la [figura 7](#figure-7), las secciones dos y tres representan iteraciones de la sección uno.</span><span class="sxs-lookup"><span data-stu-id="29ad3-186">For example, in [Figure 7](#figure-7), sections two and three represent iterations of section one.</span></span>  

> ##### <span data-ttu-id="29ad3-187">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="29ad3-187">Figure 7</span></span>  
> <span data-ttu-id="29ad3-188">Diagrama de iteraciones de animación</span><span class="sxs-lookup"><span data-stu-id="29ad3-188">Diagram of animation iterations</span></span>  
> ![Diagrama de iteraciones de animación][ImageDiagramAnimationIterations]  

<span data-ttu-id="29ad3-190">Si se aplica la misma animación a dos elementos, el inspector de animación asigna el mismo color a los elementos.</span><span class="sxs-lookup"><span data-stu-id="29ad3-190">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="29ad3-191">El color es aleatorio y no tiene importancia.</span><span class="sxs-lookup"><span data-stu-id="29ad3-191">The color is random and has no significance.</span></span>  <span data-ttu-id="29ad3-192">Por ejemplo, en la [figura 8](#figure-8) los dos elementos `div.cwccw.earlier` y `div.cwccw.later` tienen la misma animación \ ( `spinrightleft` \) aplicada, como los `div.ccwcw.earlier` elementos y `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="29ad3-192">For example, in [Figure 8](#figure-8) the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

> ##### <span data-ttu-id="29ad3-193">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="29ad3-193">Figure 8</span></span>  
> <span data-ttu-id="29ad3-194">Animaciones con códigos de color</span><span class="sxs-lookup"><span data-stu-id="29ad3-194">Color-coded animations</span></span>  
> ![Animaciones con códigos de color][ImageColorCodedAnimations]  

## <span data-ttu-id="29ad3-196">Modificar animaciones</span><span class="sxs-lookup"><span data-stu-id="29ad3-196">Modify animations</span></span>   

<span data-ttu-id="29ad3-197">Hay tres maneras en las que puede modificar una animación con el inspector de animación:</span><span class="sxs-lookup"><span data-stu-id="29ad3-197">There are three ways you are able to modify an animation with the Animation Inspector:</span></span>  

*   <span data-ttu-id="29ad3-198">Duración de la animación.</span><span class="sxs-lookup"><span data-stu-id="29ad3-198">Animation duration.</span></span>  
*   <span data-ttu-id="29ad3-199">Intervalos de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="29ad3-199">Keyframe timings.</span></span>  
*   <span data-ttu-id="29ad3-200">Retardo de inicio.</span><span class="sxs-lookup"><span data-stu-id="29ad3-200">Start time delay.</span></span>  

<span data-ttu-id="29ad3-201">Para esta sección, suponga que la [figura 9](#figure-9) representa la animación original:</span><span class="sxs-lookup"><span data-stu-id="29ad3-201">For this section suppose that [Figure 9](#figure-9) represents the original animation:</span></span>  

> ##### <span data-ttu-id="29ad3-202">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="29ad3-202">Figure 9</span></span>  
> <span data-ttu-id="29ad3-203">Animación original antes de la modificación</span><span class="sxs-lookup"><span data-stu-id="29ad3-203">Original animation before modification</span></span>  
> ![Animación original antes de la modificación][ImageOriginalAnimationBeforeModification]  

<span data-ttu-id="29ad3-205">Para cambiar la duración de una animación, haga clic y arrastre el primer o el último círculo.</span><span class="sxs-lookup"><span data-stu-id="29ad3-205">To change the duration of an animation, click and drag the first or last circle.</span></span>  

> ##### <span data-ttu-id="29ad3-206">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="29ad3-206">Figure 10</span></span>  
> <span data-ttu-id="29ad3-207">Duración modificada</span><span class="sxs-lookup"><span data-stu-id="29ad3-207">Modified duration</span></span>  
> ![Duración modificada][ImageModifiedDuration]  

<span data-ttu-id="29ad3-209">Si la animación define reglas de fotograma clave, se representan como círculos interiores blancos.</span><span class="sxs-lookup"><span data-stu-id="29ad3-209">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="29ad3-210">Haga clic y arrastre uno de estos para cambiar los intervalos del fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="29ad3-210">Click and drag one of these to change the timing of the keyframe.</span></span>  

> ##### <span data-ttu-id="29ad3-211">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="29ad3-211">Figure 11</span></span>  
> <span data-ttu-id="29ad3-212">Fotograma clave modificado</span><span class="sxs-lookup"><span data-stu-id="29ad3-212">Modified keyframe</span></span>  
> ![Fotograma clave modificado][ImageModifiedKeyframe]  

<span data-ttu-id="29ad3-214">Para agregar un retraso a una animación, haga clic en él y arrástrelo a cualquier lugar excepto los círculos.</span><span class="sxs-lookup"><span data-stu-id="29ad3-214">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

> ##### <span data-ttu-id="29ad3-215">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="29ad3-215">Figure 12</span></span>  
> <span data-ttu-id="29ad3-216">Retraso modificado</span><span class="sxs-lookup"><span data-stu-id="29ad3-216">Modified delay</span></span>  
> ![Retraso modificado][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Ilustración 1: inspector de animación"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Ilustración 2: animaciones a través del menú principal"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Ilustración 3: inspector de animación vacío"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Ilustración 4: inspector de animación con anotaciones"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Ilustración 5: detalles del grupo animación"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Ilustración 6: Mantenga el mouse sobre la animación para resaltarla en el área de visualización"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Ilustración 7: Diagrama de las iteraciones de animación"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Ilustración 8: animaciones con código de color"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Ilustración 9: animación original antes de la modificación"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Ilustración 10: duración modificada"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Ilustración 11: fotograma clave modificado"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Ilustración 12: retraso modificado"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="29ad3-230">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="29ad3-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="29ad3-231">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="29ad3-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="29ad3-233">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="29ad3-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
