---
description: Inspeccione y modifique las animaciones con el inspector de animación de Microsoft Edge DevTools.
title: Inspeccionar animaciones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fed686c07acd0648ac512dac131d85a317fb64eb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124778"
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

# <span data-ttu-id="33bd6-104">Inspeccionar animaciones</span><span class="sxs-lookup"><span data-stu-id="33bd6-104">Inspect animations</span></span>  

<span data-ttu-id="33bd6-105">Inspeccione y modifique las animaciones con el inspector de animación de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="33bd6-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="33bd6-107">Inspector de animación</span><span class="sxs-lookup"><span data-stu-id="33bd6-107">animation inspector</span></span>  
:::image-end:::  

### <span data-ttu-id="33bd6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="33bd6-108">Summary</span></span>  

*   <span data-ttu-id="33bd6-109">Capture animaciones abriendo el inspector de animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="33bd6-110">El inspector de animación detecta y ordena automáticamente las animaciones en grupos.</span><span class="sxs-lookup"><span data-stu-id="33bd6-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="33bd6-111">Inspeccione las animaciones y reduzca la velocidad de cada una de ellas, reproduzca cada una o vea el código de origen.</span><span class="sxs-lookup"><span data-stu-id="33bd6-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="33bd6-112">Modifique las animaciones cambiando los intervalos, el retraso, la duración o los desplazamientos de los fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="33bd6-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="33bd6-113">Introducción</span><span class="sxs-lookup"><span data-stu-id="33bd6-113">Overview</span></span>  

<span data-ttu-id="33bd6-114">El inspector de animación de Microsoft Edge DevTools tiene dos propósitos principales.</span><span class="sxs-lookup"><span data-stu-id="33bd6-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="33bd6-115">Inspeccionar animaciones.</span><span class="sxs-lookup"><span data-stu-id="33bd6-115">Inspecting animations.</span></span>  <span data-ttu-id="33bd6-116">Desea ralentizar, reproducir o inspeccionar el código fuente de un grupo de animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="33bd6-117">Modificar animaciones.</span><span class="sxs-lookup"><span data-stu-id="33bd6-117">Modifying animations.</span></span>  <span data-ttu-id="33bd6-118">Desea modificar el intervalo, el retraso, la duración o los desplazamientos de los fotogramas clave de un grupo de animaciones.</span><span class="sxs-lookup"><span data-stu-id="33bd6-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="33bd6-119">Actualmente, no se admite la edición de curvas y la edición de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="33bd6-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="33bd6-120">El inspector de animación admite animaciones CSS, transiciones CSS y animaciones web.</span><span class="sxs-lookup"><span data-stu-id="33bd6-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="33bd6-121">Actualmente, no se admiten las animaciones.</span><span class="sxs-lookup"><span data-stu-id="33bd6-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="33bd6-122">¿Qué es un grupo de animación?</span><span class="sxs-lookup"><span data-stu-id="33bd6-122">What is an Animation Group?</span></span>  

<span data-ttu-id="33bd6-123">Un grupo de animación es un grupo de animaciones que pueden estar relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="33bd6-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="33bd6-124">Por el momento, la web no tiene ningún concepto real de animación grupal, por lo que los diseñadores y los programadores de movimiento tienen que componer animaciones individuales para que las animaciones se representen como un efecto visual coherente.</span><span class="sxs-lookup"><span data-stu-id="33bd6-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="33bd6-125">El inspector de animación predice qué animaciones se relacionan según el tiempo de Inicio \ (excluyendo demoras, etc. \).</span><span class="sxs-lookup"><span data-stu-id="33bd6-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="33bd6-126">El inspector de animación también agrupa las animaciones en paralelo.</span><span class="sxs-lookup"><span data-stu-id="33bd6-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="33bd6-127">En otras palabras, se agrupan juntos un conjunto de animaciones que se desencadenan en el mismo bloque de script.</span><span class="sxs-lookup"><span data-stu-id="33bd6-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="33bd6-128">Si una animación es asincrónica, se coloca en un grupo independiente.</span><span class="sxs-lookup"><span data-stu-id="33bd6-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="33bd6-129">Comenzar</span><span class="sxs-lookup"><span data-stu-id="33bd6-129">Get started</span></span>  

<span data-ttu-id="33bd6-130">Hay dos formas de abrir el inspector de animación:</span><span class="sxs-lookup"><span data-stu-id="33bd6-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="33bd6-131">Abrir el menú de **DevTools personalizar y controlar**</span><span class="sxs-lookup"><span data-stu-id="33bd6-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="33bd6-132">Vaya al submenú **más herramientas** .</span><span class="sxs-lookup"><span data-stu-id="33bd6-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="33bd6-133">Elegir **animaciones**:</span><span class="sxs-lookup"><span data-stu-id="33bd6-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="33bd6-135">**Animaciones** con el menú principal</span><span class="sxs-lookup"><span data-stu-id="33bd6-135">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="33bd6-136">Abrir el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="33bd6-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="33bd6-137">Escribe `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="33bd6-137">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="33bd6-138">El inspector de animación se abre como una pestaña junto al cajón de consola.</span><span class="sxs-lookup"><span data-stu-id="33bd6-138">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="33bd6-139">Como el inspector de animación es una pestaña de cajón, puede usar el inspector de animación desde cualquier panel de DevTools.</span><span class="sxs-lookup"><span data-stu-id="33bd6-139">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="33bd6-141">Inspector de animación vacío</span><span class="sxs-lookup"><span data-stu-id="33bd6-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-142">El inspector de animación se agrupa en cuatro secciones principales \ (o paneles \).</span><span class="sxs-lookup"><span data-stu-id="33bd6-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="33bd6-143">En esta guía se hace referencia a cada panel de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="33bd6-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="33bd6-144">Índice</span><span class="sxs-lookup"><span data-stu-id="33bd6-144">Index</span></span> | <span data-ttu-id="33bd6-145">Panel</span><span class="sxs-lookup"><span data-stu-id="33bd6-145">Pane</span></span> | <span data-ttu-id="33bd6-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="33bd6-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="33bd6-147">uno</span><span class="sxs-lookup"><span data-stu-id="33bd6-147">1</span></span> | **<span data-ttu-id="33bd6-148">Controles</span><span class="sxs-lookup"><span data-stu-id="33bd6-148">Controls</span></span>** | <span data-ttu-id="33bd6-149">Desde aquí puede borrar todos los grupos de animación capturados actualmente o cambiar la velocidad del grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="33bd6-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="33bd6-150">1</span><span class="sxs-lookup"><span data-stu-id="33bd6-150">2</span></span> | **<span data-ttu-id="33bd6-151">Introducción</span><span class="sxs-lookup"><span data-stu-id="33bd6-151">Overview</span></span>** | <span data-ttu-id="33bd6-152">Seleccione un grupo de animación aquí para inspeccionarlo y modificarlo en el panel de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="33bd6-152">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="33bd6-153">2</span><span class="sxs-lookup"><span data-stu-id="33bd6-153">3</span></span> | **<span data-ttu-id="33bd6-154">Línea de tiempo</span><span class="sxs-lookup"><span data-stu-id="33bd6-154">Timeline</span></span>** | <span data-ttu-id="33bd6-155">PAUSE e inicie una animación desde aquí, o vaya a un punto específico de la animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="33bd6-156">cuatro</span><span class="sxs-lookup"><span data-stu-id="33bd6-156">4</span></span> | **<span data-ttu-id="33bd6-157">Detalles</span><span class="sxs-lookup"><span data-stu-id="33bd6-157">Details</span></span>** | <span data-ttu-id="33bd6-158">Inspeccionar y modificar el grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="33bd6-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="33bd6-160">Inspector de animación con anotaciones</span><span class="sxs-lookup"><span data-stu-id="33bd6-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-161">Para capturar una animación, solo tiene que realizar la interacción que desencadena la animación mientras el inspector de animación está abierto.</span><span class="sxs-lookup"><span data-stu-id="33bd6-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="33bd6-162">Si se desencadena una animación durante la carga de la página, vuelva a cargar la página con el inspector de animación abierto para detectar la animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-162">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="33bd6-163">Inspeccionar animaciones</span><span class="sxs-lookup"><span data-stu-id="33bd6-163">Inspect animations</span></span>  

<span data-ttu-id="33bd6-164">Una vez capturada una animación, hay varias maneras de reproducirla:</span><span class="sxs-lookup"><span data-stu-id="33bd6-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="33bd6-165">Mantenga el mouse sobre la miniatura en el panel de **información general** para ver una vista previa de ella.</span><span class="sxs-lookup"><span data-stu-id="33bd6-165">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="33bd6-166">Seleccione el grupo animación en el panel de **Descripción general** \ (para que se muestre en el panel de **detalles** \) y pulse el icono **reproducir** \ ( ![ icono de reproducción ][ImageReplayButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="33bd6-166">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="33bd6-167">La animación se reproduce en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="33bd6-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="33bd6-168">Haga clic en los iconos **velocidad de animación** \ ( ![ iconos de velocidad ][ImageAnimationSpeedButtonsIcon] de animación \) para cambiar la velocidad de vista previa del grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="33bd6-168">Click on the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="33bd6-169">Puede usar la barra vertical roja para cambiar la posición actual.</span><span class="sxs-lookup"><span data-stu-id="33bd6-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="33bd6-170">Haga clic y arrastre la barra vertical roja para borrar la animación de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="33bd6-170">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <span data-ttu-id="33bd6-171">Ver detalles de la animación</span><span class="sxs-lookup"><span data-stu-id="33bd6-171">View animation details</span></span>  

<span data-ttu-id="33bd6-172">Después de capturar un grupo de animaciones, haga clic en él en el panel de **información general** para ver los detalles.</span><span class="sxs-lookup"><span data-stu-id="33bd6-172">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="33bd6-173">En el panel **detalles** , se asigna una fila a cada animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="33bd6-175">Detalles del grupo animación</span><span class="sxs-lookup"><span data-stu-id="33bd6-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-176">Mantenga el mouse sobre una animación para resaltarla en el área de visualización.</span><span class="sxs-lookup"><span data-stu-id="33bd6-176">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="33bd6-177">Haga clic en la animación para seleccionarla en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="33bd6-177">Click on the animation to select it in the **Elements** panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="33bd6-179">Desplace el puntero sobre la animación para resaltarla en el área de visualización</span><span class="sxs-lookup"><span data-stu-id="33bd6-179">Hover over the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-180">La definición más a la izquierda es la más oscura de una animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="33bd6-181">La sección derecha, más atenuada representa las iteraciones.</span><span class="sxs-lookup"><span data-stu-id="33bd6-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="33bd6-182">Por ejemplo, en la siguiente ilustración, las secciones dos y tres representan iteraciones de la sección uno.</span><span class="sxs-lookup"><span data-stu-id="33bd6-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="33bd6-184">Diagrama de iteraciones de animación</span><span class="sxs-lookup"><span data-stu-id="33bd6-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-185">Si se aplica la misma animación a dos elementos, el inspector de animación asigna el mismo color a los elementos.</span><span class="sxs-lookup"><span data-stu-id="33bd6-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="33bd6-186">El color es aleatorio y no tiene importancia.</span><span class="sxs-lookup"><span data-stu-id="33bd6-186">The color is random and has no significance.</span></span>  <span data-ttu-id="33bd6-187">Por ejemplo, en la siguiente ilustración, los dos elementos `div.cwccw.earlier` y `div.cwccw.later` tienen la misma animación \ ( `spinrightleft` \) aplicada, como los `div.ccwcw.earlier` elementos y `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="33bd6-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="33bd6-189">Animaciones con códigos de color</span><span class="sxs-lookup"><span data-stu-id="33bd6-189">Color-coded animations</span></span>  
:::image-end:::  

## <span data-ttu-id="33bd6-190">Modificar animaciones</span><span class="sxs-lookup"><span data-stu-id="33bd6-190">Modify animations</span></span>  

<span data-ttu-id="33bd6-191">Hay tres maneras en las que puede modificar una animación con el inspector de animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="33bd6-192">Duración de la animación.</span><span class="sxs-lookup"><span data-stu-id="33bd6-192">Animation duration.</span></span>  
*   <span data-ttu-id="33bd6-193">Intervalos de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="33bd6-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="33bd6-194">Retardo de inicio.</span><span class="sxs-lookup"><span data-stu-id="33bd6-194">Start time delay.</span></span>  
    
<span data-ttu-id="33bd6-195">En la siguiente ilustración, se representa la animación original.</span><span class="sxs-lookup"><span data-stu-id="33bd6-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="33bd6-197">Animación original antes de la modificación</span><span class="sxs-lookup"><span data-stu-id="33bd6-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-198">Para cambiar la duración de una animación, haga clic y arrastre el primer o el último círculo.</span><span class="sxs-lookup"><span data-stu-id="33bd6-198">To change the duration of an animation, click and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="33bd6-200">Duración modificada</span><span class="sxs-lookup"><span data-stu-id="33bd6-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-201">Si la animación define reglas de fotograma clave, se representan como círculos interiores blancos.</span><span class="sxs-lookup"><span data-stu-id="33bd6-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="33bd6-202">Haga clic y arrastre uno de estos para cambiar los intervalos del fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="33bd6-202">Click and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="33bd6-204">Fotograma clave modificado</span><span class="sxs-lookup"><span data-stu-id="33bd6-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="33bd6-205">Para agregar un retraso a una animación, haga clic en él y arrástrelo a cualquier lugar excepto los círculos.</span><span class="sxs-lookup"><span data-stu-id="33bd6-205">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="33bd6-207">Retraso modificado</span><span class="sxs-lookup"><span data-stu-id="33bd6-207">Modified delay</span></span>  
:::image-end:::  

## <span data-ttu-id="33bd6-208">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="33bd6-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="33bd6-209">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="33bd6-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="33bd6-210">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="33bd6-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="33bd6-212">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="33bd6-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
