---
description: Inspeccione y modifique las animaciones con el Inspector de animaciones de Microsoft Edge DevTools.
title: Inspeccionar animaciones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: dba948087ca06015f686d17ba48584199373805a
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439545"
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

# <a name="inspect-animations"></a><span data-ttu-id="03ecd-104">Inspeccionar animaciones</span><span class="sxs-lookup"><span data-stu-id="03ecd-104">Inspect animations</span></span>  

<span data-ttu-id="03ecd-105">Inspeccione y modifique las animaciones con el Inspector de animaciones de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="03ecd-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="03ecd-107">inspector de animación</span><span class="sxs-lookup"><span data-stu-id="03ecd-107">animation inspector</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="03ecd-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="03ecd-108">Summary</span></span>  

*   <span data-ttu-id="03ecd-109">Captura animaciones abriendo el Inspector de animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="03ecd-110">El Inspector de animación detecta y ordena automáticamente las animaciones en grupos.</span><span class="sxs-lookup"><span data-stu-id="03ecd-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="03ecd-111">Inspeccione las animaciones ralentizando cada una, reprobando cada una o viendo el código fuente.</span><span class="sxs-lookup"><span data-stu-id="03ecd-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="03ecd-112">Modifique las animaciones cambiando el tiempo, el retraso, la duración o los desplazamientos de fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="03ecd-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <a name="overview"></a><span data-ttu-id="03ecd-113">Información general</span><span class="sxs-lookup"><span data-stu-id="03ecd-113">Overview</span></span>  

<span data-ttu-id="03ecd-114">El Inspector de animación de Microsoft Edge DevTools tiene dos propósitos principales.</span><span class="sxs-lookup"><span data-stu-id="03ecd-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="03ecd-115">Inspeccionar animaciones.</span><span class="sxs-lookup"><span data-stu-id="03ecd-115">Inspecting animations.</span></span>  <span data-ttu-id="03ecd-116">Quieres ralentizar, reproducir o inspeccionar el código fuente de un grupo de animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="03ecd-117">Modificar animaciones.</span><span class="sxs-lookup"><span data-stu-id="03ecd-117">Modifying animations.</span></span>  <span data-ttu-id="03ecd-118">Desea modificar los desplazamientos de tiempo, retraso, duración o fotograma clave de un grupo de animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="03ecd-119">Actualmente, no se admite la edición de bezier ni la edición de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="03ecd-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="03ecd-120">El Inspector de animación admite animaciones CSS, transiciones CSS y animaciones web.</span><span class="sxs-lookup"><span data-stu-id="03ecd-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="03ecd-121">actualmente no se admiten animaciones.</span><span class="sxs-lookup"><span data-stu-id="03ecd-121">animations are currently not supported.</span></span>  

### <a name="what-is-an-animation-group"></a><span data-ttu-id="03ecd-122">¿Qué es un grupo de animación?</span><span class="sxs-lookup"><span data-stu-id="03ecd-122">What is an Animation Group?</span></span>  

<span data-ttu-id="03ecd-123">Un grupo de animaciones es un grupo de animaciones que pueden estar relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="03ecd-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="03ecd-124">Actualmente, la web no tiene un concepto real de una animación de grupo, por lo que los diseñadores y desarrolladores de movimiento tienen que componer y dar tiempo a animaciones individuales para que las animaciones se representen como un efecto visual coherente.</span><span class="sxs-lookup"><span data-stu-id="03ecd-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="03ecd-125">El Inspector de animación predice qué animaciones están relacionadas en función de la hora de inicio \(excluyendo retrasos, y así sucesivamente\).</span><span class="sxs-lookup"><span data-stu-id="03ecd-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="03ecd-126">El Inspector de animación también agrupa las animaciones en paralelo.</span><span class="sxs-lookup"><span data-stu-id="03ecd-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="03ecd-127">En otras palabras, un conjunto de animaciones que se desencadenan en el mismo bloque de script se agrupan.</span><span class="sxs-lookup"><span data-stu-id="03ecd-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="03ecd-128">Si una animación es asincrónica, se coloca en un grupo independiente.</span><span class="sxs-lookup"><span data-stu-id="03ecd-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <a name="get-started"></a><span data-ttu-id="03ecd-129">Introducción</span><span class="sxs-lookup"><span data-stu-id="03ecd-129">Get started</span></span>  

<span data-ttu-id="03ecd-130">Hay dos formas de abrir el Inspector de animación:</span><span class="sxs-lookup"><span data-stu-id="03ecd-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="03ecd-131">Abra el **menú Personalizar y controlar DevTools**</span><span class="sxs-lookup"><span data-stu-id="03ecd-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="03ecd-132">Vaya al **submenú Más** herramientas.</span><span class="sxs-lookup"><span data-stu-id="03ecd-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="03ecd-133">Elegir **animaciones**:</span><span class="sxs-lookup"><span data-stu-id="03ecd-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animaciones con el menú principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="03ecd-135">**Animaciones con** el menú principal</span><span class="sxs-lookup"><span data-stu-id="03ecd-135">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="03ecd-136">Abrir el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="03ecd-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="03ecd-137">Escribe `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="03ecd-137">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="03ecd-138">El Inspector de animación se abre junto a la **herramienta Consola.**</span><span class="sxs-lookup"><span data-stu-id="03ecd-138">The Animation Inspector opens next to the **Console** tool.</span></span>  <span data-ttu-id="03ecd-139">Dado que el Inspector de animación es una herramienta de cajón, puedes usar el Inspector de animación desde cualquier panel DevTools.</span><span class="sxs-lookup"><span data-stu-id="03ecd-139">Since the Animation Inspector is a Drawer tool, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspector de animación vacío" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="03ecd-141">Inspector de animación vacío</span><span class="sxs-lookup"><span data-stu-id="03ecd-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-142">El Inspector de animación se agrupa en cuatro secciones principales \(o panes\).</span><span class="sxs-lookup"><span data-stu-id="03ecd-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="03ecd-143">Esta guía hace referencia a cada panel de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="03ecd-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="03ecd-144">Índice</span><span class="sxs-lookup"><span data-stu-id="03ecd-144">Index</span></span> | <span data-ttu-id="03ecd-145">Panel</span><span class="sxs-lookup"><span data-stu-id="03ecd-145">Pane</span></span> | <span data-ttu-id="03ecd-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="03ecd-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="03ecd-147">1</span><span class="sxs-lookup"><span data-stu-id="03ecd-147">1</span></span> | **<span data-ttu-id="03ecd-148">Controles</span><span class="sxs-lookup"><span data-stu-id="03ecd-148">Controls</span></span>** | <span data-ttu-id="03ecd-149">Desde aquí, puedes borrar todos los grupos de animación capturados actualmente o cambiar la velocidad del grupo de animación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="03ecd-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="03ecd-150">2</span><span class="sxs-lookup"><span data-stu-id="03ecd-150">2</span></span> | **<span data-ttu-id="03ecd-151">Información general</span><span class="sxs-lookup"><span data-stu-id="03ecd-151">Overview</span></span>** | <span data-ttu-id="03ecd-152">Elija un grupo de animación aquí para inspeccionarlo y modificarlo en el **panel** Detalles.</span><span class="sxs-lookup"><span data-stu-id="03ecd-152">Choose an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="03ecd-153">3</span><span class="sxs-lookup"><span data-stu-id="03ecd-153">3</span></span> | **<span data-ttu-id="03ecd-154">Línea de tiempo</span><span class="sxs-lookup"><span data-stu-id="03ecd-154">Timeline</span></span>** | <span data-ttu-id="03ecd-155">Pausa e inicia una animación desde aquí, o salta a un punto específico de la animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="03ecd-156">4</span><span class="sxs-lookup"><span data-stu-id="03ecd-156">4</span></span> | **<span data-ttu-id="03ecd-157">Detalles</span><span class="sxs-lookup"><span data-stu-id="03ecd-157">Details</span></span>** | <span data-ttu-id="03ecd-158">Inspeccione y modifique el grupo de animaciones seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="03ecd-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspector de animación anotado" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="03ecd-160">Inspector de animación anotado</span><span class="sxs-lookup"><span data-stu-id="03ecd-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-161">Para capturar una animación, simplemente realiza la interacción que desencadena la animación mientras el Inspector de animación está abierto.</span><span class="sxs-lookup"><span data-stu-id="03ecd-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="03ecd-162">Si se desencadena una animación al cargar la página, actualice la página con el Inspector de animación abierto para detectar la animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-162">If an animation is triggered on page load, refresh the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a><span data-ttu-id="03ecd-163">Inspeccionar animaciones</span><span class="sxs-lookup"><span data-stu-id="03ecd-163">Inspect animations</span></span>  

<span data-ttu-id="03ecd-164">Después de capturar una animación, hay varias maneras de reproducirla:</span><span class="sxs-lookup"><span data-stu-id="03ecd-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="03ecd-165">Mantenga el mouse en la miniatura del panel **Información** general para ver una vista previa de ella.</span><span class="sxs-lookup"><span data-stu-id="03ecd-165">Hover on the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="03ecd-166">Elija el grupo de animación en el **panel** Información  general \(para que se muestre en el panel Detalles\) y elija el icono **de** reproducción \( icono de reproducción ![ ](../media/replay-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="03ecd-166">Choose the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and choose the **replay** \(![replay icon](../media/replay-button-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="03ecd-167">La animación se reproduce en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="03ecd-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="03ecd-168">Elige los **iconos de velocidad de** animación \( iconos de velocidad de animación \) para cambiar la velocidad de vista previa del grupo de ![ ](../media/animation-speed-buttons-icon.msft.png) animaciones seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="03ecd-168">Choose the **animation speed** \(![animation speed icons](../media/animation-speed-buttons-icon.msft.png)\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="03ecd-169">Puede usar la barra vertical roja para cambiar la posición actual.</span><span class="sxs-lookup"><span data-stu-id="03ecd-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="03ecd-170">Elija y arrastre la barra vertical roja para limpiar la animación de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="03ecd-170">Choose and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <a name="view-animation-details"></a><span data-ttu-id="03ecd-171">Ver detalles de animación</span><span class="sxs-lookup"><span data-stu-id="03ecd-171">View animation details</span></span>  

<span data-ttu-id="03ecd-172">Después de capturar un grupo de animación, elige en él en el **panel** Información general para ver los detalles.</span><span class="sxs-lookup"><span data-stu-id="03ecd-172">After you capture an Animation Group, choose on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="03ecd-173">En el **panel Detalles,** se asigna una fila a cada animación individual.</span><span class="sxs-lookup"><span data-stu-id="03ecd-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Detalles del grupo de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="03ecd-175">Detalles del grupo de animación</span><span class="sxs-lookup"><span data-stu-id="03ecd-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-176">Mantenga el mouse sobre una animación para resaltarla en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="03ecd-176">Hover on an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="03ecd-177">Elija la animación para seleccionarla en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="03ecd-177">Choose the animation to select it in the **Elements** tool.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Mantenga el mouse sobre la animación para resaltarla en la ventanilla" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="03ecd-179">Mantenga el mouse sobre la animación para resaltarla en la ventanilla</span><span class="sxs-lookup"><span data-stu-id="03ecd-179">Hover on the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-180">La sección más izquierda y más oscura de una animación es la definición.</span><span class="sxs-lookup"><span data-stu-id="03ecd-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="03ecd-181">La sección derecha más atenuada representa iteraciones.</span><span class="sxs-lookup"><span data-stu-id="03ecd-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="03ecd-182">Por ejemplo, en la siguiente figura, las secciones dos y tres representan iteraciones de la sección uno.</span><span class="sxs-lookup"><span data-stu-id="03ecd-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagrama de iteraciones de animación" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="03ecd-184">Diagrama de iteraciones de animación</span><span class="sxs-lookup"><span data-stu-id="03ecd-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-185">Si se aplica la misma animación a dos elementos, el Inspector de animación asigna el mismo color a los elementos.</span><span class="sxs-lookup"><span data-stu-id="03ecd-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="03ecd-186">El color es aleatorio y no tiene importancia.</span><span class="sxs-lookup"><span data-stu-id="03ecd-186">The color is random and has no significance.</span></span>  <span data-ttu-id="03ecd-187">Por ejemplo, en la siguiente figura, los dos elementos y tienen la misma animación `div.cwccw.earlier` `div.cwccw.later` \( `spinrightleft` \) aplicada, al igual que los elementos `div.ccwcw.earlier` `div.ccwcw.later` and.</span><span class="sxs-lookup"><span data-stu-id="03ecd-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animaciones codificadas por colores" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="03ecd-189">Animaciones codificadas por colores</span><span class="sxs-lookup"><span data-stu-id="03ecd-189">Color-coded animations</span></span>  
:::image-end:::  

## <a name="modify-animations"></a><span data-ttu-id="03ecd-190">Modificar animaciones</span><span class="sxs-lookup"><span data-stu-id="03ecd-190">Modify animations</span></span>  

<span data-ttu-id="03ecd-191">Hay tres formas de modificar una animación con el Inspector de animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="03ecd-192">Duración de animación.</span><span class="sxs-lookup"><span data-stu-id="03ecd-192">Animation duration.</span></span>  
*   <span data-ttu-id="03ecd-193">Intervalos de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="03ecd-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="03ecd-194">Retraso de tiempo de inicio.</span><span class="sxs-lookup"><span data-stu-id="03ecd-194">Start time delay.</span></span>  
    
<span data-ttu-id="03ecd-195">En la siguiente figura, se representa la animación original.</span><span class="sxs-lookup"><span data-stu-id="03ecd-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animación original antes de la modificación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="03ecd-197">Animación original antes de la modificación</span><span class="sxs-lookup"><span data-stu-id="03ecd-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-198">Para cambiar la duración de una animación, elija y arrastre el primer o último círculo.</span><span class="sxs-lookup"><span data-stu-id="03ecd-198">To change the duration of an animation, choose and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Duración modificada" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="03ecd-200">Duración modificada</span><span class="sxs-lookup"><span data-stu-id="03ecd-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-201">Si la animación define alguna regla de fotograma clave, estas se representan como círculos interiores blancos.</span><span class="sxs-lookup"><span data-stu-id="03ecd-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="03ecd-202">Elija y arrastre uno de estos para cambiar el tiempo del fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="03ecd-202">Choose and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Fotograma clave modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="03ecd-204">Fotograma clave modificado</span><span class="sxs-lookup"><span data-stu-id="03ecd-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="03ecd-205">Para agregar un retraso a una animación, elige y arrástrala en cualquier lugar excepto en los círculos.</span><span class="sxs-lookup"><span data-stu-id="03ecd-205">To add a delay to an animation, choose and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retraso modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="03ecd-207">Retraso modificado</span><span class="sxs-lookup"><span data-stu-id="03ecd-207">Modified delay</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="03ecd-208">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="03ecd-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

<span data-ttu-id="03ecd-209">(.. /media/animation-speed-buttons-icon.msft.png): .. /media/animation-speed-buttons-icon.msft.png</span><span class="sxs-lookup"><span data-stu-id="03ecd-209">(../media/animation-speed-buttons-icon.msft.png): ../media/animation-speed-buttons-icon.msft.png</span></span>  
<span data-ttu-id="03ecd-210">(.. /media/replay-button-icon.msft.png): .. /media/replay-button-icon.msft.png</span><span class="sxs-lookup"><span data-stu-id="03ecd-210">(../media/replay-button-icon.msft.png): ../media/replay-button-icon.msft.png</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="03ecd-211">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03ecd-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="03ecd-212">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="03ecd-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="03ecd-214">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03ecd-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
