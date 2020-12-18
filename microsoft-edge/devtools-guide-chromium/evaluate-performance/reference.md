---
description: Una referencia sobre todas las formas de registrar y analizar el rendimiento en Microsoft Edge DevTools.
title: Referencia de análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d5b6be92c1419ba880a94c62c3f586a740816622
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230764"
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

# <span data-ttu-id="a6647-104">Referencia de análisis de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a6647-104">Performance analysis reference</span></span>  

<span data-ttu-id="a6647-105">Esta página es una referencia completa de las características de Microsoft Edge DevTools relacionadas con el análisis del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a6647-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="a6647-106">Navegue para empezar a [analizar el rendimiento en tiempo de ejecución][DevtoolsEvaluatePerformanceGettingStarted] para un tutorial guiado sobre cómo analizar el rendimiento de una página con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="a6647-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="a6647-107">Registrar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="a6647-107">Record performance</span></span>  

### <span data-ttu-id="a6647-108">Registrar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="a6647-108">Record runtime performance</span></span>  

<span data-ttu-id="a6647-109">Grabe el rendimiento en tiempo de ejecución cuando desee analizar el rendimiento de una página mientras se está ejecutando, en lugar de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="a6647-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="a6647-110">Vaya a la página que desea analizar.</span><span class="sxs-lookup"><span data-stu-id="a6647-110">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="a6647-111">Elija la pestaña **rendimiento** en DevTools.</span><span class="sxs-lookup"><span data-stu-id="a6647-111">Choose the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="a6647-112">Elija **grabar** \ ( ![ icono de registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a6647-112">Choose **Record** \(![Record icon][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Grabar" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="a6647-114">Grabar</span><span class="sxs-lookup"><span data-stu-id="a6647-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="a6647-115">Interactúe con la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-115">Interact with the page.</span></span>  <span data-ttu-id="a6647-116">DevTools registra toda la actividad de la página que se produce como resultado de las interacciones.</span><span class="sxs-lookup"><span data-stu-id="a6647-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="a6647-117">Vuelva a elegir **grabar** o elija **detener** para detener la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="a6647-118">Registrar el rendimiento de la carga</span><span class="sxs-lookup"><span data-stu-id="a6647-118">Record load performance</span></span>  

<span data-ttu-id="a6647-119">Registre el rendimiento de la carga cuando desee analizar el rendimiento de una página mientras se está cargando, en lugar de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="a6647-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="a6647-120">Vaya a la página que desea analizar.</span><span class="sxs-lookup"><span data-stu-id="a6647-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="a6647-121">Abra el panel **rendimiento** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a6647-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="a6647-122">Elija **Actualizar página** \ ( ![ Actualizar página ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a6647-122">Choose **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="a6647-123">DevTools registra las métricas de rendimiento mientras se actualiza la página y, a continuación, detiene automáticamente la grabación un par de segundos después de que finalice la carga.</span><span class="sxs-lookup"><span data-stu-id="a6647-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Actualizar página" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="a6647-125">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="a6647-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="a6647-126">DevTools automáticamente acerca de la parte de la grabación donde se produjo la mayor parte de la actividad.</span><span class="sxs-lookup"><span data-stu-id="a6647-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Una grabación de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="a6647-128">Una grabación de página</span><span class="sxs-lookup"><span data-stu-id="a6647-128">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-129">Capturar capturas de pantallas durante la grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="a6647-130">Active la casilla **capturas** de pantalla para capturar una captura de pantalla de cada fotograma mientras graba.</span><span class="sxs-lookup"><span data-stu-id="a6647-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="La casilla de verificación capturas de pantallas" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="a6647-132">La casilla de verificación **capturas de pantallas**</span><span class="sxs-lookup"><span data-stu-id="a6647-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-133">Desplácese hasta [ver una captura de pantalla](#view-a-screenshot) para obtener información sobre cómo interactuar con las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6647-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="a6647-134">Forzar recolección de elementos no utilizados al grabar</span><span class="sxs-lookup"><span data-stu-id="a6647-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="a6647-135">Mientras graba una página, elija **recopilar basura** \ ( ![ recopilar icono de basura ][ImageCollectGarbageIcon] \) para forzar la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="a6647-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Recopilar basura" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="a6647-137">Recopilar basura</span><span class="sxs-lookup"><span data-stu-id="a6647-137">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-138">Mostrar configuración de grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-138">Show recording settings</span></span>  

<span data-ttu-id="a6647-139">Elija **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureSettingsIcon] \) para exponer más opciones de configuración relacionadas con el modo en que DevTools captura las grabaciones de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a6647-139">Choose **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="La sección configuración de captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="a6647-141">La sección **configuración de captura**</span><span class="sxs-lookup"><span data-stu-id="a6647-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-142">Deshabilitar ejemplos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="a6647-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="a6647-143">De forma predeterminada, la sección **principal** de una grabación muestra las pilas de llamadas detalladas de las funciones de JavaScript a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="a6647-144">Para deshabilitar estas pilas de llamadas:</span><span class="sxs-lookup"><span data-stu-id="a6647-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="a6647-145">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="a6647-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a6647-146">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a6647-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a6647-147">Active la casilla **deshabilitar ejemplos de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="a6647-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="a6647-148">Realizar una grabación de la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="a6647-149">Las 2 figuras siguientes muestran la diferencia entre deshabilitar y habilitar muestras de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a6647-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="a6647-150">La sección **principal** de la grabación es mucho más corta cuando el muestreo está deshabilitado, porque omite todas las pilas de llamadas de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a6647-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="a6647-152">Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS</span><span class="sxs-lookup"><span data-stu-id="a6647-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Ejemplo de una grabación cuando se activan los ejemplos de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="a6647-154">Ejemplo de una grabación cuando se activan los ejemplos de JS</span><span class="sxs-lookup"><span data-stu-id="a6647-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="a6647-155">Limitar la red durante la grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-155">Throttle the network while recording</span></span>  

<span data-ttu-id="a6647-156">Para limitar la red durante la grabación:</span><span class="sxs-lookup"><span data-stu-id="a6647-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="a6647-157">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="a6647-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a6647-158">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a6647-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a6647-159">Establezca **red** en el nivel deseado de limitación.</span><span class="sxs-lookup"><span data-stu-id="a6647-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="a6647-160">Limitar la CPU durante la grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="a6647-161">Para limitar la CPU durante la grabación:</span><span class="sxs-lookup"><span data-stu-id="a6647-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="a6647-162">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="a6647-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a6647-163">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a6647-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a6647-164">Establezca la **CPU** en el nivel deseado de limitación.</span><span class="sxs-lookup"><span data-stu-id="a6647-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="a6647-165">El límite es relativo a las capacidades de su equipo.</span><span class="sxs-lookup"><span data-stu-id="a6647-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="a6647-166">Por ejemplo, la opción **2x ralentización** hace que la CPU funcione 2 veces más lentas de lo normal.</span><span class="sxs-lookup"><span data-stu-id="a6647-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="a6647-167">DevTools no simulan verdaderamente las CPU de los dispositivos móviles, porque la arquitectura de los dispositivos móviles es muy diferente de la de los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="a6647-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="a6647-168">Activar la instrumentación avanzada de pintura</span><span class="sxs-lookup"><span data-stu-id="a6647-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="a6647-169">Para ver la instrumentación de pintura detallada:</span><span class="sxs-lookup"><span data-stu-id="a6647-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="a6647-170">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="a6647-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a6647-171">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a6647-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a6647-172">Active la casilla **Habilitar el instrumental de pintura avanzada (lento)** .</span><span class="sxs-lookup"><span data-stu-id="a6647-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="a6647-173">Para obtener información sobre cómo interactuar con la información de las pinturas, vaya a [Ver capas](#view-layers-information) y [Ver generador de perfiles de pintura](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="a6647-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="a6647-174">Guardar una grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-174">Save a recording</span></span>  

<span data-ttu-id="a6647-175">Para guardar una grabación, abra el menú contextual \ (haga clic con el botón derecho \) y elija **Guardar perfil**.</span><span class="sxs-lookup"><span data-stu-id="a6647-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Guardar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="a6647-177">Guardar perfil</span><span class="sxs-lookup"><span data-stu-id="a6647-177">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="a6647-178">Cargar una grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-178">Load a recording</span></span>  

<span data-ttu-id="a6647-179">Para cargar una grabación, abra el menú contextual \ (haga clic con el botón derecho \) y elija **cargar perfil**.</span><span class="sxs-lookup"><span data-stu-id="a6647-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Cargar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="a6647-181">Cargar perfil</span><span class="sxs-lookup"><span data-stu-id="a6647-181">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="a6647-182">Borrar la grabación anterior</span><span class="sxs-lookup"><span data-stu-id="a6647-182">Clear the previous recording</span></span>  

<span data-ttu-id="a6647-183">Después de realizar una grabación, pulse **Borrar grabación** \ ( ![ Borrar icono ][ImageClearRecordingIcon] de grabación \) para borrar esa grabación del panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="a6647-183">After making a recording, press **Clear recording** \(![Clear recording icon][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Borrar grabación" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="a6647-185">Borrar grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-185">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="a6647-186">Analizar una grabación de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a6647-186">Analyze a performance recording</span></span>  

<span data-ttu-id="a6647-187">Después de [grabar el rendimiento en tiempo de ejecución](#record-runtime-performance) o el rendimiento de la [carga de registros](#record-load-performance), el panel **rendimiento** proporciona una gran cantidad de datos para analizar el rendimiento de lo que sucedió.</span><span class="sxs-lookup"><span data-stu-id="a6647-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="a6647-188">Seleccionar una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-188">Select a portion of a recording</span></span>  

<span data-ttu-id="a6647-189">Arrastre el ratón hacia la izquierda o hacia la derecha en la **información general** para seleccionar una parte de una grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="a6647-190">La **información general** es la sección que contiene los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="a6647-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arrastre el mouse por la información general para aplicar zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="a6647-192">Arrastre el mouse por la **información general** para aplicar zoom</span><span class="sxs-lookup"><span data-stu-id="a6647-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-193">Para seleccionar una parte con el teclado:</span><span class="sxs-lookup"><span data-stu-id="a6647-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="a6647-194">Elija el fondo de la sección **principal** o cualquiera de las secciones que hay junto a él, como **interacciones**, **red**o **GPU**.</span><span class="sxs-lookup"><span data-stu-id="a6647-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="a6647-195">Este flujo de trabajo de teclado solo funciona cuando una de estas secciones está en el foco.</span><span class="sxs-lookup"><span data-stu-id="a6647-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="a6647-196">Use las `W` teclas,, `A` `S` , `D` para acercar, mover a la izquierda, alejar y desplazar a la derecha, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a6647-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="a6647-197">Para seleccionar una parte con un panel táctil, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="a6647-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="a6647-198">Mantenga el mouse sobre la sección **Descripción general** o en la sección de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="a6647-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="a6647-199">La sección de **información general** es el área que contiene los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="a6647-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="a6647-200">La sección de **detalles** es el área que contiene la sección **principal** , la sección **interacciones** , etc.</span><span class="sxs-lookup"><span data-stu-id="a6647-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="a6647-201">Con dos dedos, deslice el dedo hacia arriba para alejar, deslice el dedo hacia la izquierda, deslice el dedo hacia abajo y deslice el dedo hacia la derecha para desplazarse hacia la derecha.</span><span class="sxs-lookup"><span data-stu-id="a6647-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="a6647-202">Para desplazarse por un gráfico de llamas largo en la sección **principal** o en cualquiera de los vecinos, seleccione y mantenga presionado mientras arrastra hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="a6647-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="a6647-203">Arrastre hacia la izquierda y hacia la derecha para mover la parte de la grabación elegida.</span><span class="sxs-lookup"><span data-stu-id="a6647-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <span data-ttu-id="a6647-204">Buscar actividades</span><span class="sxs-lookup"><span data-stu-id="a6647-204">Search activities</span></span>  

<span data-ttu-id="a6647-205">Seleccione `Control` + `F` \ (Windows, Linux \) o `Command` + `F` \ (MacOS \) para abrir el cuadro de búsqueda en la parte inferior del panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="a6647-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="El cuadro de búsqueda" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="a6647-207">El cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="a6647-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-208">Para navegar por las actividades que coinciden con la consulta:</span><span class="sxs-lookup"><span data-stu-id="a6647-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="a6647-209">Use los \*\*\*\* botones \ ( ![ anterior ][ImagePreviousIcon] \) y **siguiente** \ ( ![ siguiente ][ImageNextIcon] \) anteriores.</span><span class="sxs-lookup"><span data-stu-id="a6647-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="a6647-210">Seleccione `Shift` + `Enter` para seleccionar la anterior o `Enter` para seleccionar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="a6647-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="a6647-211">Para modificar la configuración de la consulta:</span><span class="sxs-lookup"><span data-stu-id="a6647-211">To modify query settings:</span></span>  

*   <span data-ttu-id="a6647-212">Presione **distinción de mayúsculas y minúsculas** \ ( ![ distingue mayúsculas de minúsculas ][ImageSearchCaseIcon] \) para hacer distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6647-212">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="a6647-213">Presione **Regex** \ ( ![ regex ][ImageSearchRegexIcon] \) para usar una expresión regular en la consulta.</span><span class="sxs-lookup"><span data-stu-id="a6647-213">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="a6647-214">Para ocultar el cuadro de búsqueda, presione **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="a6647-214">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="a6647-215">Ver actividad de subproceso principal</span><span class="sxs-lookup"><span data-stu-id="a6647-215">View main thread activity</span></span>  

<span data-ttu-id="a6647-216">Use la sección **principal** para ver la actividad que se produjo en el subproceso principal de la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="La sección principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="a6647-218">La sección **principal**</span><span class="sxs-lookup"><span data-stu-id="a6647-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-219">Elija un evento para ver más información sobre él en la pestaña **Resumen** .  DevTools describe el evento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a6647-219">Choose an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Más información sobre la función anónima en la pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="a6647-221">Más información sobre la `anonymous` función en la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="a6647-221">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-222">DevTools representa la actividad principal del subproceso con un gráfico de llama.</span><span class="sxs-lookup"><span data-stu-id="a6647-222">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="a6647-223">El eje x representa la grabación a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="a6647-223">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="a6647-224">El eje y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a6647-224">The y-axis represents the call stack.</span></span>  <span data-ttu-id="a6647-225">Los eventos en la parte superior provocan los eventos que se encuentran por debajo.</span><span class="sxs-lookup"><span data-stu-id="a6647-225">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Un gráfico de llamas" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="a6647-227">Un gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="a6647-227">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-228">En la ilustración anterior, un `click` evento produjo un `Function Call` en `activitytabs.js` en la línea 53.</span><span class="sxs-lookup"><span data-stu-id="a6647-228">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="a6647-229">A continuación `Function Call` , revise que se ejecutó una función anónima.</span><span class="sxs-lookup"><span data-stu-id="a6647-229">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="a6647-230">La función anónima solicitada, que solicitó `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="a6647-230">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="a6647-231">DevTools asigna scripts a colores aleatorios.</span><span class="sxs-lookup"><span data-stu-id="a6647-231">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="a6647-232">En la ilustración anterior, las solicitudes de función de un script se muestran coloreadas en verde.</span><span class="sxs-lookup"><span data-stu-id="a6647-232">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="a6647-233">Las solicitudes de otra secuencia de comandos tienen colores beige.</span><span class="sxs-lookup"><span data-stu-id="a6647-233">Requests from another script are colored beige.</span></span>  <span data-ttu-id="a6647-234">El amarillo más oscuro representa la actividad de scripting y el evento morado representa la actividad de representación.</span><span class="sxs-lookup"><span data-stu-id="a6647-234">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="a6647-235">Estos eventos amarillos y amarillos más oscuros son coherentes en todas las grabaciones.</span><span class="sxs-lookup"><span data-stu-id="a6647-235">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="a6647-236">Navegue a [deshabilitar muestras de JavaScript](#disable-javascript-samples) si desea ocultar el gráfico detallado de llamas de solicitudes de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a6647-236">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="a6647-237">Cuando se deshabilitan los ejemplos de JS, solo se muestran los eventos de alto nivel, como `Event: click` y `Function Call` de la ilustración anterior `str` .</span><span class="sxs-lookup"><span data-stu-id="a6647-237">When JS samples are disabled, only high-level events such as `Event: click` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <span data-ttu-id="a6647-238">Ver actividades en una tabla</span><span class="sxs-lookup"><span data-stu-id="a6647-238">View activities in a table</span></span>  

<span data-ttu-id="a6647-239">Después de grabar una página, no es necesario basarse únicamente en la sección **principal** para analizar las actividades.</span><span class="sxs-lookup"><span data-stu-id="a6647-239">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="a6647-240">DevTools también proporciona tres vistas tabulares para analizar actividades.</span><span class="sxs-lookup"><span data-stu-id="a6647-240">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="a6647-241">Cada vista le ofrece una perspectiva diferente en las actividades:</span><span class="sxs-lookup"><span data-stu-id="a6647-241">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="a6647-242">Cuando desee ver las actividades raíz que producen el mayor trabajo, use [la pestaña árbol de llamadas](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-242">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="a6647-243">Cuando desee ver las actividades en las que el más tiempo se dedicó directamente, use [la pestaña Bottom-Up](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-243">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="a6647-244">Cuando desee ver las actividades en el orden en el que se produjeron durante la grabación, use [la pestaña registro de eventos](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-244">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="a6647-245">Las tres secciones siguientes hacen referencia a la misma demostración.</span><span class="sxs-lookup"><span data-stu-id="a6647-245">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="a6647-246">Ejecute la demostración usted mismo en la [demostración de pestañas de actividad][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="a6647-246">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="a6647-247">Actividades raíz</span><span class="sxs-lookup"><span data-stu-id="a6647-247">Root activities</span></span>  

<span data-ttu-id="a6647-248">A continuación se explica el concepto de **actividades raíz** que se menciona en las secciones **árbol de llamadas** , pestaña **ascendente** y registro de **eventos** .</span><span class="sxs-lookup"><span data-stu-id="a6647-248">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="a6647-249">Las actividades raíz son aquellas que hacen que el explorador realice algún trabajo.</span><span class="sxs-lookup"><span data-stu-id="a6647-249">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="a6647-250">Por ejemplo, cuando elige una página web, el explorador ejecuta una `Event` actividad como actividad raíz.</span><span class="sxs-lookup"><span data-stu-id="a6647-250">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="a6647-251">Esto `Event` puede hacer que se ejecute un controlador, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="a6647-251">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="a6647-252">En el gráfico de llamas de la sección **principal** , las actividades raíz se encuentran en la parte superior del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a6647-252">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="a6647-253">En las pestañas **árbol de llamadas** y **registro de eventos** , las actividades raíz son los elementos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a6647-253">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="a6647-254">Vaya a [la pestaña árbol de llamadas](#the-call-tree-tab) para obtener un ejemplo de actividades raíz.</span><span class="sxs-lookup"><span data-stu-id="a6647-254">Navigate to [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="a6647-255">La ficha árbol de llamadas</span><span class="sxs-lookup"><span data-stu-id="a6647-255">The Call Tree tab</span></span>  

<span data-ttu-id="a6647-256">Use la pestaña **árbol de llamadas** para ver qué actividades de [raíz](#root-activities) hacen la mayor parte del trabajo.</span><span class="sxs-lookup"><span data-stu-id="a6647-256">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="a6647-257">La pestaña **árbol de llamadas** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-257">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="a6647-258">Desplácese para [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.</span><span class="sxs-lookup"><span data-stu-id="a6647-258">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="La ficha árbol de llamadas" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="a6647-260">La ficha **árbol de llamadas**</span><span class="sxs-lookup"><span data-stu-id="a6647-260">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-261">En la ilustración anterior, el nivel superior de los elementos de la columna **actividad** , como `Evaluate Script` y `Parse HTML` son las actividades raíz.</span><span class="sxs-lookup"><span data-stu-id="a6647-261">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="a6647-262">El anidamiento representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a6647-262">The nesting represents the call stack.</span></span>  <span data-ttu-id="a6647-263">Por ejemplo, en la ilustración anterior, `Parse HTML` que causó el origen `Evaluate Script` `Compile Script` y el `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="a6647-263">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="a6647-264">El **tiempo propio** representa el tiempo que pasa directamente en esa actividad.</span><span class="sxs-lookup"><span data-stu-id="a6647-264">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="a6647-265">**Tiempo total** representa el tiempo invertido en esa actividad o en cualquiera de los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a6647-265">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="a6647-266">Elija **autohora**, **tiempo total**o **actividad** para ordenar la tabla por esa columna.</span><span class="sxs-lookup"><span data-stu-id="a6647-266">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="a6647-267">Use el cuadro de texto **filtrar** para filtrar eventos por nombre de actividad.</span><span class="sxs-lookup"><span data-stu-id="a6647-267">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="a6647-268">De forma predeterminada, el menú **agrupar** se establece en **sin agrupar**.</span><span class="sxs-lookup"><span data-stu-id="a6647-268">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="a6647-269">Use el menú **agrupar** para ordenar la tabla actividad según varios criterios.</span><span class="sxs-lookup"><span data-stu-id="a6647-269">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="a6647-270">Elija **Mostrar pila más pesada** \ ( ![ Mostrar pila más pesada ][ImageShowHeaviestStackIcon] \) para mostrar otra tabla a la derecha de la tabla **actividad** .</span><span class="sxs-lookup"><span data-stu-id="a6647-270">Choose **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="a6647-271">Elija una actividad para rellenar la tabla de **pila más pesada** .</span><span class="sxs-lookup"><span data-stu-id="a6647-271">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="a6647-272">La tabla de **pilas más pesada** muestra qué elementos secundarios de la actividad seleccionada tardaron más tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="a6647-272">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="a6647-273">La ficha Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="a6647-273">The Bottom-Up tab</span></span>  

<span data-ttu-id="a6647-274">Use la pestaña **de abajo** para ver las actividades que se ocuparon directamente la mayor parte del tiempo en el agregado.</span><span class="sxs-lookup"><span data-stu-id="a6647-274">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="a6647-275">La pestaña de la **parte inferior** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-275">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="a6647-276">Desplácese para [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.</span><span class="sxs-lookup"><span data-stu-id="a6647-276">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="La ficha Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="a6647-278">La pestaña **abajo**</span><span class="sxs-lookup"><span data-stu-id="a6647-278">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-279">En la sección **principal** , diagrama de llamas de la ilustración anterior, navegue hasta que casi prácticamente todo el tiempo se dedicó a ejecutarse `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="a6647-279">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="a6647-280">La actividad superior de la pestaña de la **parte inferior** de la figura anterior es `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="a6647-280">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="a6647-281">Vaya a la pestaña **de la parte inferior** , la actividad más costosa es `Layout` .</span><span class="sxs-lookup"><span data-stu-id="a6647-281">Navigate to the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="a6647-282">La columna **Self Time** representa el tiempo agregado directamente en esa actividad, en todas las apariciones.</span><span class="sxs-lookup"><span data-stu-id="a6647-282">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="a6647-283">La columna **tiempo total** representa el tiempo agregado invertido en esa actividad o en cualquiera de los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a6647-283">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="a6647-284">La ficha registro de eventos</span><span class="sxs-lookup"><span data-stu-id="a6647-284">The Event Log tab</span></span>  

<span data-ttu-id="a6647-285">Use la pestaña **registro de eventos** para ver las actividades en el orden en el que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-285">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="a6647-286">La pestaña **registro de eventos** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-286">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="a6647-287">Desplácese para [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.</span><span class="sxs-lookup"><span data-stu-id="a6647-287">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="La ficha registro de eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="a6647-289">La ficha **registro de eventos**</span><span class="sxs-lookup"><span data-stu-id="a6647-289">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-290">La columna **hora de inicio** representa el punto en el que se inició la actividad, en relación con el inicio de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-290">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="a6647-291">Por ejemplo, la hora de inicio del `175.7 ms` elemento seleccionado en la figura anterior significa que la actividad comenzó el 175,7 ms después de que se iniciara la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-291">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="a6647-292">La columna **Self Time** representa el tiempo invertido directamente en esa actividad.</span><span class="sxs-lookup"><span data-stu-id="a6647-292">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="a6647-293">La columna **tiempo total** representa el tiempo invertido directamente en esa actividad o en cualquiera de los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a6647-293">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="a6647-294">Elija **hora de inicio**, **tiempo propio**o **tiempo total** para ordenar la tabla por esa columna.</span><span class="sxs-lookup"><span data-stu-id="a6647-294">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="a6647-295">Use el cuadro de texto **filtrar** para filtrar las actividades por nombre.</span><span class="sxs-lookup"><span data-stu-id="a6647-295">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="a6647-296">Use el menú **duración** para filtrar todas las actividades que hayan tardado menos de 1 ms o de 15 ms.</span><span class="sxs-lookup"><span data-stu-id="a6647-296">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="a6647-297">De forma predeterminada, el menú **duración** se establece en **todos**, lo que significa que se muestran todas las actividades.</span><span class="sxs-lookup"><span data-stu-id="a6647-297">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="a6647-298">Deshabilite las casillas de verificación **cargar**, **scripting**, **procesamiento**o **pintura** para filtrar todas las actividades de esas categorías.</span><span class="sxs-lookup"><span data-stu-id="a6647-298">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="a6647-299">Ver actividad de la GPU</span><span class="sxs-lookup"><span data-stu-id="a6647-299">View GPU activity</span></span>  

<span data-ttu-id="a6647-300">Ver la actividad de la GPU en la sección **GPU** .</span><span class="sxs-lookup"><span data-stu-id="a6647-300">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="La sección GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="a6647-302">La sección **GPU**</span><span class="sxs-lookup"><span data-stu-id="a6647-302">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-303">Ver actividad rasterizada</span><span class="sxs-lookup"><span data-stu-id="a6647-303">View raster activity</span></span>  

<span data-ttu-id="a6647-304">Ver la actividad rasterizada en la sección de **trama** .</span><span class="sxs-lookup"><span data-stu-id="a6647-304">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="La sección trama" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="a6647-306">La sección **trama**</span><span class="sxs-lookup"><span data-stu-id="a6647-306">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-307">Ver interacciones</span><span class="sxs-lookup"><span data-stu-id="a6647-307">View interactions</span></span>  

<span data-ttu-id="a6647-308">Use la sección **interacciones** para buscar y analizar las interacciones del usuario que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-308">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="La sección interacciones" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="a6647-310">La sección **interacciones**</span><span class="sxs-lookup"><span data-stu-id="a6647-310">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-311">Una línea roja en la parte inferior de una interacción representa el tiempo dedicado a esperar el subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="a6647-311">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="a6647-312">Elija una interacción para ver más información sobre ella en la pestaña **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="a6647-312">Choose an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="a6647-313">Analizar fotogramas por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="a6647-313">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="a6647-314">DevTools proporciona numerosas formas de analizar fotogramas por segundo:</span><span class="sxs-lookup"><span data-stu-id="a6647-314">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="a6647-315">Use [el gráfico de fps](#the-fps-chart) para obtener una visión general de los FPS durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-315">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="a6647-316">Use [la sección Marcos](#the-frames-section) para ver cuánto tarda un marco en particular.</span><span class="sxs-lookup"><span data-stu-id="a6647-316">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="a6647-317">Use el **medidor de fps** para una estimación en tiempo real de fps a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-317">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="a6647-318">Vaya a [Ver fotogramas por segundo en tiempo real con el medidor de fps](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="a6647-318">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="a6647-319">El gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="a6647-319">The FPS chart</span></span>  

<span data-ttu-id="a6647-320">El gráfico **fps** proporciona una descripción general de la velocidad de fotogramas en toda la duración de una grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-320">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="a6647-321">En general, cuanto más alto sea la barra verde, mejor será la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a6647-321">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="a6647-322">Una barra roja encima del gráfico de **fps** es una advertencia de que la velocidad de fotogramas ha disminuido tan poco que probablemente se ha dañado la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="a6647-322">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="El gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="a6647-324">El gráfico de **fps**</span><span class="sxs-lookup"><span data-stu-id="a6647-324">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="a6647-325">La sección marcos</span><span class="sxs-lookup"><span data-stu-id="a6647-325">The Frames section</span></span>  

<span data-ttu-id="a6647-326">La sección **Marcos** le indica exactamente cuánto tarda un marco en particular.</span><span class="sxs-lookup"><span data-stu-id="a6647-326">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="a6647-327">Mantenga el mouse sobre un marco para ver una información sobre herramientas con más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="a6647-327">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Desplazar el puntero sobre un marco" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="a6647-329">Desplazar el puntero sobre un marco</span><span class="sxs-lookup"><span data-stu-id="a6647-329">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-330">Elija un marco para ver más información sobre el marco en la pestaña **Resumen** .  DevTools esquematiza el fotograma seleccionado en azul.</span><span class="sxs-lookup"><span data-stu-id="a6647-330">Choose a frame to view more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Ver un marco en la pestaña Resumen" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="a6647-332">Ver un marco en la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="a6647-332">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-333">Ver solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="a6647-333">View network requests</span></span>  

<span data-ttu-id="a6647-334">Expanda la sección **red** para ver una cascada de solicitudes de red que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-334">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="La sección red" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="a6647-336">La sección **red**</span><span class="sxs-lookup"><span data-stu-id="a6647-336">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-337">Las solicitudes se codifican en colores de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a6647-337">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="a6647-338">HTML: azul</span><span class="sxs-lookup"><span data-stu-id="a6647-338">HTML: Blue</span></span>  
*   <span data-ttu-id="a6647-339">CSS: morado</span><span class="sxs-lookup"><span data-stu-id="a6647-339">CSS: Purple</span></span>  
*   <span data-ttu-id="a6647-340">JS: amarillo</span><span class="sxs-lookup"><span data-stu-id="a6647-340">JS: Yellow</span></span>  
*   <span data-ttu-id="a6647-341">Imágenes: verde</span><span class="sxs-lookup"><span data-stu-id="a6647-341">Images: Green</span></span>  
    
<span data-ttu-id="a6647-342">Elija una solicitud para ver más información sobre ella en la pestaña **Resumen** .  Por ejemplo, en la ilustración anterior, la pestaña **Resumen** muestra más información sobre la solicitud azul seleccionada en la sección **red** .</span><span class="sxs-lookup"><span data-stu-id="a6647-342">Choose a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="a6647-343">Un cuadrado de color azul más oscuro en la parte superior izquierda de una solicitud significa que es una solicitud de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="a6647-343">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="a6647-344">Un cuadrado más claro significa menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="a6647-344">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="a6647-345">Por ejemplo, en la ilustración anterior, el azul, la solicitud seleccionada es de mayor prioridad y el verde que está debajo es de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="a6647-345">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="a6647-346">En el 1º de los siguientes valores, la solicitud de `www.bing.com` se representa mediante una línea a la izquierda, una barra en el centro con una parte oscura y una parte oscura y una línea a la derecha.</span><span class="sxs-lookup"><span data-stu-id="a6647-346">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="a6647-347">En la segunda de las siguientes figuras, se muestra la representación correspondiente de la misma solicitud en la ficha **intervalos** del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="a6647-347">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="a6647-348">A continuación se muestra cómo se asignan entre sí estas dos representaciones:</span><span class="sxs-lookup"><span data-stu-id="a6647-348">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="a6647-349">La línea izquierda es todo hasta el `Connection Start` grupo de eventos, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a6647-349">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="a6647-350">En otras palabras, es todo lo antes `Request Sent` y exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a6647-350">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="a6647-351">La parte clara de la barra es `Request Sent` y `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="a6647-351">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="a6647-352">La parte oscura de la barra es `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="a6647-352">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="a6647-353">Esencialmente, la línea adecuada es el tiempo dedicado a esperar el hilo principal.</span><span class="sxs-lookup"><span data-stu-id="a6647-353">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="a6647-354">Esto no se representa en la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="a6647-354">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="La representación de barra de línea de la solicitud www.bing.com" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="a6647-356">Representación de barra de línea de la `www.bing.com` solicitud</span><span class="sxs-lookup"><span data-stu-id="a6647-356">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="La herramienta red" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="a6647-358">La herramienta **red**</span><span class="sxs-lookup"><span data-stu-id="a6647-358">The **Network** tool</span></span>  
<span data-ttu-id="a6647-359">::: Image-end:::</span><span class="sxs-lookup"><span data-stu-id="a6647-359">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="a6647-360">Ver métricas de memoria</span><span class="sxs-lookup"><span data-stu-id="a6647-360">View memory metrics</span></span>  

<span data-ttu-id="a6647-361">Active la casilla **memoria** para ver las métricas de memoria de la última grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-361">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="La casilla memoria" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="a6647-363">La casilla **memoria**</span><span class="sxs-lookup"><span data-stu-id="a6647-363">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-364">DevTools muestra un nuevo gráfico de **memoria** , encima de la pestaña **Resumen** .  También hay un nuevo gráfico debajo del gráfico **net** , denominado **montón**.</span><span class="sxs-lookup"><span data-stu-id="a6647-364">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="a6647-365">El gráfico de **montones** proporciona la misma información que la línea de **montón JS** en el gráfico de **memoria** .</span><span class="sxs-lookup"><span data-stu-id="a6647-365">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memoria" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="a6647-367">Métricas de memoria</span><span class="sxs-lookup"><span data-stu-id="a6647-367">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-368">Las líneas de color del gráfico se asignan a las casillas coloreadas encima del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a6647-368">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="a6647-369">Desactive una casilla para ocultar la categoría en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="a6647-369">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="a6647-370">El gráfico solo muestra la región de la grabación que está seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="a6647-370">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="a6647-371">Por ejemplo, en la ilustración anterior, el gráfico de **memoria** solo muestra el uso de memoria de aproximadamente la marca de MS 400 a la marca de 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="a6647-371">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="a6647-372">Ver la duración de una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-372">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="a6647-373">Al analizar una sección como la **red** o **Main**, a veces necesitarás una estimación más precisa de cuánto tiempo han tardado determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="a6647-373">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="a6647-374">Espera `Shift` , elige y mantén presionado, y arrastra hacia la izquierda o la derecha para seleccionar una parte de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-374">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="a6647-375">En la parte inferior de la selección, DevTools muestra cuánto tiempo duró esa parte.</span><span class="sxs-lookup"><span data-stu-id="a6647-375">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Ver la duración de una parte de una grabación" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="a6647-377">Ver la duración de una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="a6647-377">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-378">Ver una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="a6647-378">View a screenshot</span></span>  

<span data-ttu-id="a6647-379">Vaya a capturar capturas de [pantallas mientras graba](#capture-screenshots-while-recording) para obtener información sobre cómo activar las capturas de pantallas.</span><span class="sxs-lookup"><span data-stu-id="a6647-379">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="a6647-380">Pase el puntero por la **información general** para ver una captura de pantalla de cómo se vio la página durante ese momento de la grabación.</span><span class="sxs-lookup"><span data-stu-id="a6647-380">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="a6647-381">La **información general** es la sección que contiene los gráficos de **CPU**, **fps**y **net** .</span><span class="sxs-lookup"><span data-stu-id="a6647-381">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Ver una captura de pantalla" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="a6647-383">Ver una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="a6647-383">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-384">También puede ver capturas de pantallas si elige un marco en la sección **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="a6647-384">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="a6647-385">DevTools muestra una versión reducida de la captura de pantalla en la pestaña **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="a6647-385">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Ver una captura de pantalla en la pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="a6647-387">Ver una captura de pantalla en la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="a6647-387">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-388">Elija la miniatura en la pestaña **Resumen** para acercar la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6647-388">Choose the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Ampliar la captura de pantalla desde la pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="a6647-390">Ampliar la captura de pantalla desde la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="a6647-390">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="a6647-391">Ver información de capas</span><span class="sxs-lookup"><span data-stu-id="a6647-391">View layers information</span></span>  

<span data-ttu-id="a6647-392">Para ver la información sobre las capas avanzadas de un marco:</span><span class="sxs-lookup"><span data-stu-id="a6647-392">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="a6647-393">[Activar el instrumental de pintura avanzado](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="a6647-393">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="a6647-394">Seleccione un marco de la sección **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="a6647-394">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="a6647-395">DevTools muestra información sobre las capas en la ficha nuevas **capas** , junto a la ficha **registro de eventos** .</span><span class="sxs-lookup"><span data-stu-id="a6647-395">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="El panel capas" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="a6647-397">El panel **capas**</span><span class="sxs-lookup"><span data-stu-id="a6647-397">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="a6647-398">Desplace el puntero sobre una capa para resaltarla en el diagrama.</span><span class="sxs-lookup"><span data-stu-id="a6647-398">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Resaltar una capa" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="a6647-400">Resaltar una capa</span><span class="sxs-lookup"><span data-stu-id="a6647-400">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="a6647-401">Para mover el diagrama:</span><span class="sxs-lookup"><span data-stu-id="a6647-401">To move the diagram:</span></span>  

*   <span data-ttu-id="a6647-402">Elija **modo panorámico** \ ( ![ modo panorámico ][ImagePanModeIcon] \) para desplazarse por los ejes X e y.</span><span class="sxs-lookup"><span data-stu-id="a6647-402">Choose **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="a6647-403">Elija **modo de rotación** \ ( ![ modo ][ImageRotateModeIcon] de giro \) para girar a lo largo del eje Z.</span><span class="sxs-lookup"><span data-stu-id="a6647-403">Choose **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="a6647-404">Elija **restablecer transformación** \ ( ![ restablecer transformación ][ImageResetTransformIcon] \) para restablecer el diagrama a la posición original.</span><span class="sxs-lookup"><span data-stu-id="a6647-404">Choose **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="a6647-405">Ver generador de perfiles de pintura</span><span class="sxs-lookup"><span data-stu-id="a6647-405">View paint profiler</span></span>  

<span data-ttu-id="a6647-406">Para ver información avanzada sobre un evento de pintura:</span><span class="sxs-lookup"><span data-stu-id="a6647-406">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="a6647-407">[Activar](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="a6647-407">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="a6647-408">Seleccione un evento de **pintura** en la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="a6647-408">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Pestaña generador de perfiles de pintura" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="a6647-410">Pestaña **generador de perfiles de pintura**</span><span class="sxs-lookup"><span data-stu-id="a6647-410">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a6647-411">Analizar el rendimiento de la representación con la pestaña representación</span><span class="sxs-lookup"><span data-stu-id="a6647-411">Analyze rendering performance with the Rendering tab</span></span>  

<span data-ttu-id="a6647-412">Use las características de la pestaña **representación** para poder visualizar el rendimiento de la representación de la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-412">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="a6647-413">Para abrir la pestaña **representación** :</span><span class="sxs-lookup"><span data-stu-id="a6647-413">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="a6647-414">[Abrir el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="a6647-414">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="a6647-415">Empiece `Rendering` a escribir y seleccione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="a6647-415">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="a6647-416">DevTools muestra la ficha **representación** en la parte inferior de la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a6647-416">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="La pestaña representación" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="a6647-418">La pestaña **representación**</span><span class="sxs-lookup"><span data-stu-id="a6647-418">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="a6647-419">Ver fotogramas por segundo en tiempo real con el medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="a6647-419">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="a6647-420">El **medidor de fps** es una superposición que aparece en la esquina superior derecha de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="a6647-420">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="a6647-421">Proporciona una estimación en tiempo real de FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-421">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="a6647-422">Para abrir el **medidor de fps**:</span><span class="sxs-lookup"><span data-stu-id="a6647-422">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="a6647-423">Abra la pestaña **representación** .  Na [analiza el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-423">Open the **Rendering** tab.  Na [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a6647-424">Active la casilla de verificación de **medidor de fps** .</span><span class="sxs-lookup"><span data-stu-id="a6647-424">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="El medidor de FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="a6647-426">El **medidor de fps**</span><span class="sxs-lookup"><span data-stu-id="a6647-426">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="a6647-427">Ver los eventos de pintura en tiempo real con parpadeo de pintura</span><span class="sxs-lookup"><span data-stu-id="a6647-427">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="a6647-428">Use las intermitencias de pintura para obtener una vista en tiempo real de todos los eventos de pintura en la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-428">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="a6647-429">Cada vez que se vuelve a pintar una parte de la página, DevTools esquematiza esa sección en verde.</span><span class="sxs-lookup"><span data-stu-id="a6647-429">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="a6647-430">Para activar los parpadeos de pintura, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="a6647-430">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="a6647-431">Abra la pestaña **representación** .  Desplácese hasta [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-431">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a6647-432">Active la casilla de **pintura parpadeante** .</span><span class="sxs-lookup"><span data-stu-id="a6647-432">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Pintura parpadeante" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="a6647-434">Pintura parpadeante</span><span class="sxs-lookup"><span data-stu-id="a6647-434">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="a6647-435">Ver una superposición de capas con bordes de capas</span><span class="sxs-lookup"><span data-stu-id="a6647-435">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="a6647-436">Use **bordes de capas** para ver una superposición de los bordes de la capa y los mosaicos en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-436">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="a6647-437">Para activar los bordes de capas, complete las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a6647-437">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="a6647-438">Abra la pestaña **representación** .  Desplácese hasta [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-438">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a6647-439">Active la casilla **bordes de capas** .</span><span class="sxs-lookup"><span data-stu-id="a6647-439">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordes de capas" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="a6647-441">Bordes de capas</span><span class="sxs-lookup"><span data-stu-id="a6647-441">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="a6647-442">Navegue hasta los comentarios de [debug_colors. CC][ChromiumDebugColors] para obtener una explicación de los códigos de colores.</span><span class="sxs-lookup"><span data-stu-id="a6647-442">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="a6647-443">Buscar problemas de rendimiento de desplazamiento en tiempo real</span><span class="sxs-lookup"><span data-stu-id="a6647-443">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="a6647-444">Use los problemas de rendimiento de desplazamiento para identificar los elementos de la página que tienen detectores de eventos relacionados con el desplazamiento que pueden dañar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="a6647-444">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="a6647-445">DevTools subraya los elementos potencialmente problemáticos de verde azulado.</span><span class="sxs-lookup"><span data-stu-id="a6647-445">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="a6647-446">Para ver los problemas de rendimiento del desplazamiento, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="a6647-446">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="a6647-447">Abra la pestaña **representación** .  Desplácese hasta [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a6647-447">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a6647-448">Active la casilla de verificación de **problemas de rendimiento de desplazamiento** .</span><span class="sxs-lookup"><span data-stu-id="a6647-448">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Los problemas de rendimiento de desplazamiento indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="a6647-450">Los **problemas de rendimiento de desplazamiento** indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento</span><span class="sxs-lookup"><span data-stu-id="a6647-450">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a6647-451">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a6647-451">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abrir el menú de comandos: ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Introducción al análisis de rendimiento en tiempo de ejecución | Microsoft docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demostración de las pestañas actividad | intento"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc: búsqueda de código"  

> [!NOTE]
> <span data-ttu-id="a6647-457">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a6647-457">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a6647-458">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a6647-458">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a6647-460">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a6647-460">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
