---
description: Una referencia sobre todas las formas de registrar y analizar el rendimiento en Microsoft Edge DevTools.
title: Referencia de análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e7774dc0aab647b8cf2bf47699368fafe6c21d70
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439692"
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

# <a name="performance-analysis-reference"></a><span data-ttu-id="63b5c-104">Referencia de análisis de rendimiento</span><span class="sxs-lookup"><span data-stu-id="63b5c-104">Performance analysis reference</span></span>  

<span data-ttu-id="63b5c-105">Esta página es una referencia completa de las características de Microsoft Edge DevTools relacionadas con el análisis del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="63b5c-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="63b5c-106">Vaya a [Introducción al análisis del rendimiento][DevtoolsEvaluatePerformanceGettingStarted] en tiempo de ejecución para obtener un tutorial guiado sobre cómo analizar el rendimiento de una página mediante Microsoft Edge [DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="63b5c-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="record-performance"></a><span data-ttu-id="63b5c-107">Rendimiento del registro</span><span class="sxs-lookup"><span data-stu-id="63b5c-107">Record performance</span></span>  

### <a name="record-runtime-performance"></a><span data-ttu-id="63b5c-108">Rendimiento del tiempo de ejecución de registro</span><span class="sxs-lookup"><span data-stu-id="63b5c-108">Record runtime performance</span></span>  

<span data-ttu-id="63b5c-109">Registre el rendimiento en tiempo de ejecución cuando desee analizar el rendimiento de una página mientras se está ejecutando, en lugar de cargarla.</span><span class="sxs-lookup"><span data-stu-id="63b5c-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="63b5c-110">Vaya a la página que desea analizar.</span><span class="sxs-lookup"><span data-stu-id="63b5c-110">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="63b5c-111">Abra la **herramienta Rendimiento** en DevTools.</span><span class="sxs-lookup"><span data-stu-id="63b5c-111">Open the **Performance** tool in DevTools.</span></span>  
1.  <span data-ttu-id="63b5c-112">Elija **Grabar** \( ![ Icono de registro ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="63b5c-112">Choose **Record** \(![Record icon](../media/record-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Grabar" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="63b5c-114">Grabar</span><span class="sxs-lookup"><span data-stu-id="63b5c-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="63b5c-115">Interactuar con la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-115">Interact with the page.</span></span>  <span data-ttu-id="63b5c-116">DevTools registra toda la actividad de página que se produce como resultado de las interacciones.</span><span class="sxs-lookup"><span data-stu-id="63b5c-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="63b5c-117">Elija **Grabar de** nuevo o Detener **para** detener la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <a name="record-load-performance"></a><span data-ttu-id="63b5c-118">Rendimiento de carga de registro</span><span class="sxs-lookup"><span data-stu-id="63b5c-118">Record load performance</span></span>  

<span data-ttu-id="63b5c-119">Registre el rendimiento de carga cuando desee analizar el rendimiento de una página mientras se carga, en lugar de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="63b5c-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="63b5c-120">Vaya a la página que desea analizar.</span><span class="sxs-lookup"><span data-stu-id="63b5c-120">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="63b5c-121">Abra **el** panel Rendimiento de DevTools.</span><span class="sxs-lookup"><span data-stu-id="63b5c-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="63b5c-122">Elija **Actualizar página** \( Actualizar página ![ ](../media/refresh-page-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="63b5c-122">Choose **Refresh page** \(![Refresh Page](../media/refresh-page-icon.msft.png)\).</span></span>  <span data-ttu-id="63b5c-123">DevTools registra las métricas de rendimiento mientras la página se actualiza y, a continuación, detiene automáticamente la grabación un par de segundos después de que finalice la carga.</span><span class="sxs-lookup"><span data-stu-id="63b5c-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Página Actualizar" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="63b5c-125">Página Actualizar</span><span class="sxs-lookup"><span data-stu-id="63b5c-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="63b5c-126">DevTools acerca automáticamente la parte de la grabación donde se produjo la mayor parte de la actividad.</span><span class="sxs-lookup"><span data-stu-id="63b5c-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Una grabación de carga de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="63b5c-128">Una grabación de carga de página</span><span class="sxs-lookup"><span data-stu-id="63b5c-128">A page-load recording</span></span>  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a><span data-ttu-id="63b5c-129">Capturar capturas de pantalla durante la grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="63b5c-130">Activa la casilla **Capturas de pantalla** para capturar una captura de pantalla de cada fotograma durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="La casilla Capturas de pantalla" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="63b5c-132">La **casilla Capturas de** pantalla</span><span class="sxs-lookup"><span data-stu-id="63b5c-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-133">Vaya a [Ver una captura de pantalla](#view-a-screenshot) para obtener información sobre cómo interactuar con las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="63b5c-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <a name="force-garbage-collection-while-recording"></a><span data-ttu-id="63b5c-134">Forzar la recolección de elementos no utilizados durante la grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="63b5c-135">Mientras graba una página, elija **Recopilar elementos no** utilizados \( Recopilar icono de elementos no utilizados ![ ](../media/collect-garbage-icon.msft.png) \) para forzar la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="63b5c-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon](../media/collect-garbage-icon.msft.png)\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Recopilar elementos no utilizados" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="63b5c-137">Recopilar elementos no utilizados</span><span class="sxs-lookup"><span data-stu-id="63b5c-137">Collect garbage</span></span>  
:::image-end:::  

### <a name="show-recording-settings"></a><span data-ttu-id="63b5c-138">Mostrar configuración de grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-138">Show recording settings</span></span>  

<span data-ttu-id="63b5c-139">Elija **Configuración de captura** \( Configuración de captura \) para exponer más opciones relacionadas con la forma en que ![ ](../media/capture-settings-icon.msft.png) DevTools captura las grabaciones de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="63b5c-139">Choose **Capture settings** \(![Capture settings](../media/capture-settings-icon.msft.png)\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Sección Configuración de captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="63b5c-141">Sección **Configuración de** captura</span><span class="sxs-lookup"><span data-stu-id="63b5c-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <a name="disable-javascript-samples"></a><span data-ttu-id="63b5c-142">Deshabilitar ejemplos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="63b5c-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="63b5c-143">De forma predeterminada, la **sección Main** de una grabación muestra las pilas de llamadas detalladas de las funciones de JavaScript a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="63b5c-144">Para deshabilitar estas pilas de llamadas:</span><span class="sxs-lookup"><span data-stu-id="63b5c-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="63b5c-145">Abra el **menú Configuración de** captura.</span><span class="sxs-lookup"><span data-stu-id="63b5c-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="63b5c-146">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="63b5c-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="63b5c-147">Active la casilla **Deshabilitar ejemplos de JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="63b5c-148">Haga una grabación de la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="63b5c-149">Las dos cifras siguientes muestran la diferencia entre deshabilitar y habilitar ejemplos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63b5c-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="63b5c-150">La **sección Principal** de la grabación es mucho más corta cuando se deshabilita el muestreo, ya que omite todas las pilas de llamadas de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63b5c-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Un ejemplo de una grabación cuando se deshabilitan los ejemplos de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="63b5c-152">Un ejemplo de una grabación cuando se deshabilitan los ejemplos de JS</span><span class="sxs-lookup"><span data-stu-id="63b5c-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Un ejemplo de una grabación cuando se han activado las muestras de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="63b5c-154">Un ejemplo de una grabación cuando se han activado las muestras de JS</span><span class="sxs-lookup"><span data-stu-id="63b5c-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a><span data-ttu-id="63b5c-155">Limitar la red durante la grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-155">Throttle the network while recording</span></span>  

<span data-ttu-id="63b5c-156">Para limitar la red durante la grabación:</span><span class="sxs-lookup"><span data-stu-id="63b5c-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="63b5c-157">Abra el **menú Configuración de** captura.</span><span class="sxs-lookup"><span data-stu-id="63b5c-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="63b5c-158">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="63b5c-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="63b5c-159">Establezca **Red** en el nivel deseado de limitación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <a name="throttle-the-cpu-while-recording"></a><span data-ttu-id="63b5c-160">Limitar la CPU durante la grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="63b5c-161">Para limitar la CPU durante la grabación:</span><span class="sxs-lookup"><span data-stu-id="63b5c-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="63b5c-162">Abra el **menú Configuración de** captura.</span><span class="sxs-lookup"><span data-stu-id="63b5c-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="63b5c-163">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="63b5c-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="63b5c-164">Establece **la CPU** en el nivel deseado de limitación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="63b5c-165">La limitación es relativa a las capacidades del equipo.</span><span class="sxs-lookup"><span data-stu-id="63b5c-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="63b5c-166">Por ejemplo, la **opción de ralentización 2x** hace que la CPU funcione 2 veces más lento de lo normal.</span><span class="sxs-lookup"><span data-stu-id="63b5c-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="63b5c-167">DevTools no simula realmente las CPU de los dispositivos móviles, ya que la arquitectura de los dispositivos móviles es muy diferente de la de los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="63b5c-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <a name="turn-on-advanced-paint-instrumentation"></a><span data-ttu-id="63b5c-168">Activar instrumentación de pintura avanzada</span><span class="sxs-lookup"><span data-stu-id="63b5c-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="63b5c-169">Para ver instrumentación de pintura detallada:</span><span class="sxs-lookup"><span data-stu-id="63b5c-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="63b5c-170">Abra el **menú Configuración de** captura.</span><span class="sxs-lookup"><span data-stu-id="63b5c-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="63b5c-171">Vaya a [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="63b5c-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="63b5c-172">Active la casilla **Habilitar instrumentación avanzada de pintura (lento).**</span><span class="sxs-lookup"><span data-stu-id="63b5c-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="63b5c-173">Para obtener información sobre cómo interactuar con la información de pintura, vaya [a Ver capas](#view-layers-information) y Ver [perfiles de pintura.](#view-paint-profiler)</span><span class="sxs-lookup"><span data-stu-id="63b5c-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <a name="save-a-recording"></a><span data-ttu-id="63b5c-174">Guardar una grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-174">Save a recording</span></span>  

<span data-ttu-id="63b5c-175">Para guardar una grabación, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Guardar perfil**.</span><span class="sxs-lookup"><span data-stu-id="63b5c-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Guardar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="63b5c-177">Guardar perfil</span><span class="sxs-lookup"><span data-stu-id="63b5c-177">Save Profile</span></span>**  
:::image-end:::  

## <a name="load-a-recording"></a><span data-ttu-id="63b5c-178">Cargar una grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-178">Load a recording</span></span>  

<span data-ttu-id="63b5c-179">Para cargar una grabación, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Cargar perfil**.</span><span class="sxs-lookup"><span data-stu-id="63b5c-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Perfil de carga" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="63b5c-181">Perfil de carga</span><span class="sxs-lookup"><span data-stu-id="63b5c-181">Load Profile</span></span>**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a><span data-ttu-id="63b5c-182">Borrar la grabación anterior</span><span class="sxs-lookup"><span data-stu-id="63b5c-182">Clear the previous recording</span></span>  

<span data-ttu-id="63b5c-183">Después de realizar una grabación, elija **Borrar grabación** \( Borrar icono de grabación \) para borrar esa grabación desde el ![ panel ](../media/clear-recording-icon.msft.png) Rendimiento. </span><span class="sxs-lookup"><span data-stu-id="63b5c-183">After making a recording, choose **Clear recording** \(![Clear recording icon](../media/clear-recording-icon.msft.png)\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Borrar grabación" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="63b5c-185">Borrar grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-185">Clear recording</span></span>**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a><span data-ttu-id="63b5c-186">Analizar una grabación de rendimiento</span><span class="sxs-lookup"><span data-stu-id="63b5c-186">Analyze a performance recording</span></span>  

<span data-ttu-id="63b5c-187">Después de [registrar el rendimiento en tiempo](#record-runtime-performance) de ejecución o el rendimiento de carga de registros, el panel Rendimiento proporciona una gran cantidad de datos para analizar el rendimiento de lo que acaba de suceder. [](#record-load-performance) </span><span class="sxs-lookup"><span data-stu-id="63b5c-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <a name="select-a-portion-of-a-recording"></a><span data-ttu-id="63b5c-188">Seleccionar una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-188">Select a portion of a recording</span></span>  

<span data-ttu-id="63b5c-189">Arrastre el mouse a la izquierda o a la derecha a través de **información** general para seleccionar una parte de una grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="63b5c-190">Overview **es** la sección que contiene los gráficos **FPS,** **CPU**y **NET.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arrastre el mouse a través de información general para acercar" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="63b5c-192">Arrastre el mouse a través de **información general** para acercar</span><span class="sxs-lookup"><span data-stu-id="63b5c-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-193">Para seleccionar una parte con el teclado:</span><span class="sxs-lookup"><span data-stu-id="63b5c-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="63b5c-194">Elija el fondo de la **sección Principal** o cualquiera de las secciones que hay junto a ella, como **Interacciones,** **Red**o **GPU.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="63b5c-195">Este flujo de trabajo de teclado solo funciona cuando una de estas secciones está en el foco.</span><span class="sxs-lookup"><span data-stu-id="63b5c-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="63b5c-196">Usa las teclas , , , para acercar, mover a la izquierda, alejar y mover a la `W` `A` `S` `D` derecha, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="63b5c-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="63b5c-197">Para seleccionar una parte con un trackpad, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="63b5c-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="63b5c-198">Mantenga el mouse sobre la **sección Información** general o la **sección** Detalles.</span><span class="sxs-lookup"><span data-stu-id="63b5c-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="63b5c-199">La **sección Información** general es el área que contiene los gráficos **FPS,** **CPU**y **NET.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="63b5c-200">La **sección** Detalles es el área que contiene la **sección Principal,** la **sección Interacciones,** y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="63b5c-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="63b5c-201">Con dos dedos, desliza el dedo hacia arriba para alejarse, desliza el dedo hacia la izquierda para moverte a la izquierda, desliza el dedo hacia abajo para acercar y desliza el dedo hacia la derecha para moverte a la derecha.</span><span class="sxs-lookup"><span data-stu-id="63b5c-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="63b5c-202">Para desplazarse por un gráfico de llama largo en la **sección Principal** o cualquiera de los vecinos, elija y mantenga presionado mientras arrastra hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="63b5c-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="63b5c-203">Arrastre a la izquierda y a la derecha para mover la parte de la grabación elegida.</span><span class="sxs-lookup"><span data-stu-id="63b5c-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <a name="search-activities"></a><span data-ttu-id="63b5c-204">Actividades de búsqueda</span><span class="sxs-lookup"><span data-stu-id="63b5c-204">Search activities</span></span>  

<span data-ttu-id="63b5c-205">Seleccione `Control` + `F` \(Windows, Linux\) o `Command` + `F` \(macOS\)  para abrir el cuadro de búsqueda en la parte inferior del panel Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="63b5c-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="El cuadro de búsqueda" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="63b5c-207">El cuadro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="63b5c-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-208">Para navegar por actividades que coincidan con la consulta:</span><span class="sxs-lookup"><span data-stu-id="63b5c-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="63b5c-209">Use los **botones** Previous \( ![ Previous ](../media/previous-icon.msft.png) \) y **Next** \( ![ Next ](../media/next-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="63b5c-209">Use the **Previous** \(![Previous](../media/previous-icon.msft.png)\) and **Next** \(![Next](../media/next-icon.msft.png)\) buttons.</span></span>  
*   <span data-ttu-id="63b5c-210">Seleccione `Shift` + `Enter` para seleccionar la anterior `Enter` o para seleccionar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="63b5c-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="63b5c-211">Para modificar la configuración de consulta:</span><span class="sxs-lookup"><span data-stu-id="63b5c-211">To modify query settings:</span></span>  

*   <span data-ttu-id="63b5c-212">Elija **Distingue mayúsculas de** minúsculas ![ \( Distingue mayúsculas de ](../media/search-case-icon.msft.png) minúsculas \) para que la consulta sea confidencial.</span><span class="sxs-lookup"><span data-stu-id="63b5c-212">Choose **Case sensitive** \(![Case sensitive](../media/search-case-icon.msft.png)\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="63b5c-213">Elija **Regex** \( ![ Regex ](../media/search-regex-icon.msft.png) \) para usar una expresión regular en la consulta.</span><span class="sxs-lookup"><span data-stu-id="63b5c-213">Choose **Regex** \(![Regex](../media/search-regex-icon.msft.png)\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="63b5c-214">Para ocultar el cuadro de búsqueda, elija **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="63b5c-214">To hide the search box, choose **Cancel**.</span></span>  

### <a name="view-main-thread-activity"></a><span data-ttu-id="63b5c-215">Ver actividad de subprocesos principales</span><span class="sxs-lookup"><span data-stu-id="63b5c-215">View main thread activity</span></span>  

<span data-ttu-id="63b5c-216">Use la **sección Main** para ver la actividad que se produjo en el subproceso principal de la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Sección Principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="63b5c-218">Sección  Principal</span><span class="sxs-lookup"><span data-stu-id="63b5c-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-219">Elija un evento para ver más información sobre él en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-219">Choose an event to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="63b5c-220">DevTools describe el evento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="63b5c-220">DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Más información sobre la función anónima en el panel Resumen" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="63b5c-222">Más información sobre la `anonymous` función en el panel **Resumen**</span><span class="sxs-lookup"><span data-stu-id="63b5c-222">More information about the `anonymous` function in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-223">DevTools representa la actividad del subproceso principal con un gráfico de llamas.</span><span class="sxs-lookup"><span data-stu-id="63b5c-223">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="63b5c-224">El eje X representa la grabación con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="63b5c-224">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="63b5c-225">El eje Y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="63b5c-225">The y-axis represents the call stack.</span></span>  <span data-ttu-id="63b5c-226">Los eventos en la parte superior provocan los eventos debajo de él.</span><span class="sxs-lookup"><span data-stu-id="63b5c-226">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Un gráfico de llamas" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="63b5c-228">Un gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="63b5c-228">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-229">En la figura anterior, `click` un evento provocó una `Function Call` entrada en la línea `activitytabs.js` 53.</span><span class="sxs-lookup"><span data-stu-id="63b5c-229">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="63b5c-230">A `Function Call` continuación, revise que se ha ejecutado una función anónima.</span><span class="sxs-lookup"><span data-stu-id="63b5c-230">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="63b5c-231">La función anónima solicitada `a` , que `wait` solicitó , que solicitó `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-231">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="63b5c-232">DevTools asigna scripts de colores aleatorios.</span><span class="sxs-lookup"><span data-stu-id="63b5c-232">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="63b5c-233">En la figura anterior, las solicitudes de función de un script son de color verde claro.</span><span class="sxs-lookup"><span data-stu-id="63b5c-233">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="63b5c-234">Las solicitudes de otro script son de color beis.</span><span class="sxs-lookup"><span data-stu-id="63b5c-234">Requests from another script are colored beige.</span></span>  <span data-ttu-id="63b5c-235">El amarillo más oscuro representa la actividad de scripting y el evento púrpura representa la actividad de representación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-235">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="63b5c-236">Estos eventos amarillos y púrpuras más oscuros son coherentes en todas las grabaciones.</span><span class="sxs-lookup"><span data-stu-id="63b5c-236">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="63b5c-237">Vaya a [Deshabilitar ejemplos de JavaScript](#disable-javascript-samples) si desea ocultar el gráfico detallado de llamas de las solicitudes de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63b5c-237">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="63b5c-238">Cuando se deshabilitan los ejemplos de JS, solo se muestran eventos de alto nivel, como y `Event: choose` `Function Call` de la figura `str` anterior.</span><span class="sxs-lookup"><span data-stu-id="63b5c-238">When JS samples are disabled, only high-level events such as `Event: choose` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <a name="view-activities-in-a-table"></a><span data-ttu-id="63b5c-239">Ver actividades en una tabla</span><span class="sxs-lookup"><span data-stu-id="63b5c-239">View activities in a table</span></span>  

<span data-ttu-id="63b5c-240">Después de grabar una página, no es necesario depender únicamente de la **sección Principal** para analizar las actividades.</span><span class="sxs-lookup"><span data-stu-id="63b5c-240">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="63b5c-241">DevTools también proporciona tres vistas tabulares para analizar actividades.</span><span class="sxs-lookup"><span data-stu-id="63b5c-241">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="63b5c-242">Cada vista le ofrece una perspectiva diferente sobre las actividades:</span><span class="sxs-lookup"><span data-stu-id="63b5c-242">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="63b5c-243">Cuando desee ver las actividades raíz que más funcionan, use el panel [Árbol de](#the-call-tree-panel) llamadas.</span><span class="sxs-lookup"><span data-stu-id="63b5c-243">When you want to view the root activities that cause the most work, use the [Call Tree](#the-call-tree-panel) panel.</span></span>  
*   <span data-ttu-id="63b5c-244">Cuando desee ver las actividades en las que se ha dedicado más tiempo directamente, use el panel [Inferior](#the-bottom-up-panel) hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="63b5c-244">When you want to view the activities where the most time was directly spent, use the [Bottom-Up](#the-bottom-up-panel) panel.</span></span>  
*   <span data-ttu-id="63b5c-245">Cuando desee ver las actividades en el orden en que se produjeron durante la grabación, use el panel [Registro de](#the-event-log-panel) eventos.</span><span class="sxs-lookup"><span data-stu-id="63b5c-245">When you want to view the activities in the order in which they occurred during the recording, use the [Event Log](#the-event-log-panel) panel.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="63b5c-246">Las tres secciones siguientes hacen referencia a la misma demostración.</span><span class="sxs-lookup"><span data-stu-id="63b5c-246">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="63b5c-247">Ejecute la demostración usted mismo [en La demostración de pestañas de actividad][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="63b5c-247">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <a name="root-activities"></a><span data-ttu-id="63b5c-248">Actividades raíz</span><span class="sxs-lookup"><span data-stu-id="63b5c-248">Root activities</span></span>  

<span data-ttu-id="63b5c-249">Esta es una explicación del concepto **de actividades** raíz que se menciona en el **panel** Árbol de **llamadas,** el panel inferior arriba y el panel **Registro de** eventos.</span><span class="sxs-lookup"><span data-stu-id="63b5c-249">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** panel, **Bottom-Up** panel, and **Event Log** panel.</span></span>  

<span data-ttu-id="63b5c-250">Las actividades raíz son las que hacen que el explorador realice algún trabajo.</span><span class="sxs-lookup"><span data-stu-id="63b5c-250">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="63b5c-251">Por ejemplo, al elegir una página web, el explorador ejecuta una `Event` actividad como actividad raíz.</span><span class="sxs-lookup"><span data-stu-id="63b5c-251">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="63b5c-252">Esto `Event` puede hacer que se ejecute un controlador, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="63b5c-252">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="63b5c-253">En el gráfico de llama de la **sección Principal,** las actividades raíz se encuentran en la parte superior del gráfico.</span><span class="sxs-lookup"><span data-stu-id="63b5c-253">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="63b5c-254">En los **paneles Árbol de llamadas** y Registro **de** eventos, las actividades raíz son los elementos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="63b5c-254">In the **Call Tree** and **Event Log** panels, root activities are the top-level items.</span></span>  

<span data-ttu-id="63b5c-255">Vaya al panel [Árbol de llamadas](#the-call-tree-panel) para ver un ejemplo de actividades raíz.</span><span class="sxs-lookup"><span data-stu-id="63b5c-255">Navigate to the [Call Tree](#the-call-tree-panel) panel for an example of root activities.</span></span>  

#### <a name="the-call-tree-panel"></a><span data-ttu-id="63b5c-256">Panel Árbol de llamadas</span><span class="sxs-lookup"><span data-stu-id="63b5c-256">The Call Tree panel</span></span>  

<span data-ttu-id="63b5c-257">Use el **panel Árbol de llamadas** para ver qué actividades [raíz](#root-activities) causan más trabajo.</span><span class="sxs-lookup"><span data-stu-id="63b5c-257">Use the **Call Tree** panel to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="63b5c-258">El **panel Árbol de** llamadas solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-258">The **Call Tree** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="63b5c-259">Vaya [a Seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.</span><span class="sxs-lookup"><span data-stu-id="63b5c-259">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Panel Árbol de llamadas" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="63b5c-261">Panel **Árbol de llamadas**</span><span class="sxs-lookup"><span data-stu-id="63b5c-261">The **Call Tree** panel</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-262">En la figura anterior, el nivel superior de los elementos de la columna **Actividad,** como `Evaluate Script` y son actividades `Parse HTML` raíz.</span><span class="sxs-lookup"><span data-stu-id="63b5c-262">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="63b5c-263">El anidamiento representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="63b5c-263">The nesting represents the call stack.</span></span>  <span data-ttu-id="63b5c-264">Por ejemplo, en la figura anterior, `Parse HTML` que `Evaluate Script` causó la `Compile Script` causa y `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-264">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="63b5c-265">**Self Time** representa el tiempo invertido directamente en esa actividad.</span><span class="sxs-lookup"><span data-stu-id="63b5c-265">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="63b5c-266">**El tiempo total** representa el tiempo invertido en esa actividad o en cualquiera de los secundarios.</span><span class="sxs-lookup"><span data-stu-id="63b5c-266">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="63b5c-267">Elija **Self Time**, Total **Time**o **Activity** para ordenar la tabla por esa columna.</span><span class="sxs-lookup"><span data-stu-id="63b5c-267">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="63b5c-268">Use el **cuadro de** texto Filtrar para filtrar eventos por nombre de actividad.</span><span class="sxs-lookup"><span data-stu-id="63b5c-268">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="63b5c-269">De forma **predeterminada, el menú** Agrupación se establece en Sin **agrupación**.</span><span class="sxs-lookup"><span data-stu-id="63b5c-269">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="63b5c-270">Use el **menú Agrupación** para ordenar la tabla de actividad según varios criterios.</span><span class="sxs-lookup"><span data-stu-id="63b5c-270">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="63b5c-271">Elija **Mostrar pila más pesada** \( Mostrar pila más pesada \) para mostrar otra tabla a la derecha de la tabla ![ ](../media/show-heaviest-stack-icon.msft.png) **Actividad.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-271">Choose **Show Heaviest Stack** \(![Show Heaviest Stack](../media/show-heaviest-stack-icon.msft.png)\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="63b5c-272">Elija una actividad para rellenar la **tabla De pila más** pesada.</span><span class="sxs-lookup"><span data-stu-id="63b5c-272">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="63b5c-273">La **tabla Pila más pesada** muestra los elementos secundarios de la actividad seleccionada que tardaron más tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="63b5c-273">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <a name="the-bottom-up-panel"></a><span data-ttu-id="63b5c-274">El panel Bottom-Up panel</span><span class="sxs-lookup"><span data-stu-id="63b5c-274">The Bottom-Up panel</span></span>  

<span data-ttu-id="63b5c-275">Use el **panel Inferior arriba** para ver qué actividades tomaron directamente la mayor parte del tiempo agregado.</span><span class="sxs-lookup"><span data-stu-id="63b5c-275">Use the **Bottom-Up** panel to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="63b5c-276">El **panel inferior arriba** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-276">The **Bottom-Up** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="63b5c-277">Vaya [a Seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.</span><span class="sxs-lookup"><span data-stu-id="63b5c-277">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="El panel Bottom-Up panel" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="63b5c-279">Panel **inferior arriba**</span><span class="sxs-lookup"><span data-stu-id="63b5c-279">The **Bottom-Up** panel</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-280">En el **gráfico de** llama de sección principal de la figura anterior, vaya a ese prácticamente todo el tiempo que se ha dedicado a ejecutar `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-280">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="63b5c-281">La actividad superior del panel **inferior arriba** de la figura anterior es `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-281">The top activity in the **Bottom-Up** panel of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="63b5c-282">Navegue hasta el panel **Inferior arriba,** la siguiente actividad más costosa es `Layout` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-282">Navigate to the **Bottom-Up** panel, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="63b5c-283">La **columna Self Time** representa el tiempo agregado invertido directamente en esa actividad, en todas las repeticiones.</span><span class="sxs-lookup"><span data-stu-id="63b5c-283">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="63b5c-284">La **columna Tiempo total** representa el tiempo agregado invertido en esa actividad o en cualquiera de los secundarios.</span><span class="sxs-lookup"><span data-stu-id="63b5c-284">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <a name="the-event-log-panel"></a><span data-ttu-id="63b5c-285">Panel Registro de eventos</span><span class="sxs-lookup"><span data-stu-id="63b5c-285">The Event Log panel</span></span>  

<span data-ttu-id="63b5c-286">Use el **panel Registro de** eventos para ver las actividades en el orden en que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-286">Use the **Event Log** panel to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="63b5c-287">El **panel Registro de** eventos solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-287">The **Event Log** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="63b5c-288">Vaya [a Seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.</span><span class="sxs-lookup"><span data-stu-id="63b5c-288">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Panel Registro de eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="63b5c-290">Panel **Registro de eventos**</span><span class="sxs-lookup"><span data-stu-id="63b5c-290">The **Event Log** panel</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-291">La **columna Hora de** inicio representa el punto en el que se inició esa actividad, en relación con el inicio de la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-291">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="63b5c-292">Por ejemplo, la hora de inicio del elemento seleccionado en la figura anterior significa que la actividad se inició `175.7 ms` 175,7 ms después de que se iniciara la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-292">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="63b5c-293">La **columna Tiempo de** autoservicio representa el tiempo invertido directamente en esa actividad.</span><span class="sxs-lookup"><span data-stu-id="63b5c-293">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="63b5c-294">Las **columnas Tiempo total** representan el tiempo invertido directamente en esa actividad o en cualquiera de los secundarios.</span><span class="sxs-lookup"><span data-stu-id="63b5c-294">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="63b5c-295">Elija **Hora de inicio,** **Hora de**autoservicio o Tiempo **total** para ordenar la tabla por esa columna.</span><span class="sxs-lookup"><span data-stu-id="63b5c-295">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="63b5c-296">Use el **cuadro de** texto Filtrar para filtrar las actividades por su nombre.</span><span class="sxs-lookup"><span data-stu-id="63b5c-296">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="63b5c-297">Use el **menú** Duración para filtrar las actividades que tardaron menos de 1 ms o 15 ms.</span><span class="sxs-lookup"><span data-stu-id="63b5c-297">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="63b5c-298">De forma predeterminada, **el menú** Duración se establece en **Todo**, lo que significa que se muestran todas las actividades.</span><span class="sxs-lookup"><span data-stu-id="63b5c-298">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="63b5c-299">Deshabilita las **casillas Carga,** **Scripting,** **Representación**o **Pintura** para filtrar todas las actividades de dichas categorías.</span><span class="sxs-lookup"><span data-stu-id="63b5c-299">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <a name="view-gpu-activity"></a><span data-ttu-id="63b5c-300">Ver actividad de GPU</span><span class="sxs-lookup"><span data-stu-id="63b5c-300">View GPU activity</span></span>  

<span data-ttu-id="63b5c-301">Ver actividad de GPU en la **sección GPU.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-301">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Sección GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="63b5c-303">Sección **GPU**</span><span class="sxs-lookup"><span data-stu-id="63b5c-303">The **GPU** section</span></span>  
:::image-end:::  

### <a name="view-raster-activity"></a><span data-ttu-id="63b5c-304">Ver actividad de trama</span><span class="sxs-lookup"><span data-stu-id="63b5c-304">View raster activity</span></span>  

<span data-ttu-id="63b5c-305">Ver actividad de trama en la **sección Raster.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-305">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Sección Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="63b5c-307">Sección **Raster**</span><span class="sxs-lookup"><span data-stu-id="63b5c-307">The **Raster** section</span></span>  
:::image-end:::  

### <a name="view-interactions"></a><span data-ttu-id="63b5c-308">Ver interacciones</span><span class="sxs-lookup"><span data-stu-id="63b5c-308">View interactions</span></span>  

<span data-ttu-id="63b5c-309">Use la **sección Interacciones** para buscar y analizar las interacciones del usuario que se han producido durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-309">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Sección Interacciones" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="63b5c-311">Sección **Interacciones**</span><span class="sxs-lookup"><span data-stu-id="63b5c-311">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-312">Una línea roja en la parte inferior de una interacción representa el tiempo invertido en esperar el subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="63b5c-312">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="63b5c-313">Elija una interacción para ver más información al respecto en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-313">Choose an interaction to view more information about it in the **Summary** panel.</span></span>  

### <a name="analyze-frames-per-second-fps"></a><span data-ttu-id="63b5c-314">Analizar fotogramas por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="63b5c-314">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="63b5c-315">DevTools proporciona numerosas formas de analizar fotogramas por segundo:</span><span class="sxs-lookup"><span data-stu-id="63b5c-315">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="63b5c-316">Usa [el gráfico FPS para](#the-fps-chart) obtener información general sobre FPS durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-316">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="63b5c-317">Use [la sección Marcos para](#the-frames-section) ver cuánto tiempo tardó un fotograma determinado.</span><span class="sxs-lookup"><span data-stu-id="63b5c-317">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="63b5c-318">Usa el **medidor fps para** una estimación en tiempo real de FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-318">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="63b5c-319">Vaya a [Ver fotogramas por segundo en tiempo real con el medidor FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="63b5c-319">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <a name="the-fps-chart"></a><span data-ttu-id="63b5c-320">Gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="63b5c-320">The FPS chart</span></span>  

<span data-ttu-id="63b5c-321">El **gráfico FPS** proporciona información general sobre la velocidad de fotogramas durante toda la duración de una grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-321">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="63b5c-322">En general, cuanto mayor sea la barra verde, mejor será la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="63b5c-322">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="63b5c-323">Una barra roja encima del **gráfico FPS** es una advertencia de que la velocidad de fotogramas se ha reducido tan bajo que probablemente dañe la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="63b5c-323">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="63b5c-325">Gráfico **de FPS**</span><span class="sxs-lookup"><span data-stu-id="63b5c-325">The **FPS** chart</span></span>  
:::image-end:::  

#### <a name="the-frames-section"></a><span data-ttu-id="63b5c-326">Sección Marcos</span><span class="sxs-lookup"><span data-stu-id="63b5c-326">The Frames section</span></span>  

<span data-ttu-id="63b5c-327">La **sección** Marcos le indica exactamente cuánto tiempo tardó un fotograma en particular.</span><span class="sxs-lookup"><span data-stu-id="63b5c-327">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="63b5c-328">Mantenga el mouse sobre un marco para ver una información sobre herramientas con más información sobre él.</span><span class="sxs-lookup"><span data-stu-id="63b5c-328">Hover on a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Mantener el mouse en un marco" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="63b5c-330">Mantener el mouse en un marco</span><span class="sxs-lookup"><span data-stu-id="63b5c-330">Hover on a frame</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-331">Elija un marco para ver más información sobre el marco en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-331">Choose a frame to view more information about the frame in the **Summary** panel.</span></span>  <span data-ttu-id="63b5c-332">DevTools describe el marco seleccionado en azul.</span><span class="sxs-lookup"><span data-stu-id="63b5c-332">DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Ver un marco en el panel Resumen" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="63b5c-334">Ver un marco en el panel **Resumen**</span><span class="sxs-lookup"><span data-stu-id="63b5c-334">View a frame in the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-network-requests"></a><span data-ttu-id="63b5c-335">Ver solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="63b5c-335">View network requests</span></span>  

<span data-ttu-id="63b5c-336">Expanda la **sección Red** para ver una cascada de solicitudes de red que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-336">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Sección Red" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="63b5c-338">Sección **Red**</span><span class="sxs-lookup"><span data-stu-id="63b5c-338">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-339">Las solicitudes tienen un código de color como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="63b5c-339">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="63b5c-340">HTML: azul</span><span class="sxs-lookup"><span data-stu-id="63b5c-340">HTML: Blue</span></span>  
*   <span data-ttu-id="63b5c-341">CSS: púrpura</span><span class="sxs-lookup"><span data-stu-id="63b5c-341">CSS: Purple</span></span>  
*   <span data-ttu-id="63b5c-342">JS: amarillo</span><span class="sxs-lookup"><span data-stu-id="63b5c-342">JS: Yellow</span></span>  
*   <span data-ttu-id="63b5c-343">Imágenes: Verde</span><span class="sxs-lookup"><span data-stu-id="63b5c-343">Images: Green</span></span>  
    
<span data-ttu-id="63b5c-344">Elija una solicitud para ver más información al respecto en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-344">Choose a request to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="63b5c-345">Por ejemplo, en la figura anterior, el **panel** Resumen muestra más información sobre la solicitud azul seleccionada en la **sección** Red.</span><span class="sxs-lookup"><span data-stu-id="63b5c-345">For example, in the previous figure, the **Summary** panel is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="63b5c-346">Un cuadrado azul oscuro en la parte superior izquierda de una solicitud significa que es una solicitud de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="63b5c-346">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="63b5c-347">Un cuadrado azul claro significa prioridad inferior.</span><span class="sxs-lookup"><span data-stu-id="63b5c-347">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="63b5c-348">Por ejemplo, en la figura anterior, la solicitud azul seleccionada es de mayor prioridad y la verde debajo de ella es de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="63b5c-348">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="63b5c-349">En la 1ª de las siguientes figuras, la solicitud de se representa mediante una línea a la izquierda, una barra en el centro con una parte oscura y una parte ligera, y una línea a la `www.bing.com` derecha.</span><span class="sxs-lookup"><span data-stu-id="63b5c-349">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="63b5c-350">En la 2ª de las siguientes figuras se muestra la representación correspondiente de la misma solicitud en el **panel** Temporización de la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-350">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** panel of the **Network** tool.</span></span>  <span data-ttu-id="63b5c-351">Esta es la forma en que estas dos representaciones se asignan entre sí:</span><span class="sxs-lookup"><span data-stu-id="63b5c-351">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="63b5c-352">La línea izquierda es todo hasta el `Connection Start` grupo de eventos, inclusive.</span><span class="sxs-lookup"><span data-stu-id="63b5c-352">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="63b5c-353">En otras palabras, es todo lo anterior `Request Sent` a , exclusive.</span><span class="sxs-lookup"><span data-stu-id="63b5c-353">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="63b5c-354">La parte ligera de la barra es `Request Sent` y `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-354">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="63b5c-355">La parte oscura de la barra es `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-355">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="63b5c-356">La línea correcta es básicamente el tiempo que se pasa esperando el subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="63b5c-356">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="63b5c-357">Esto no se representa en el panel **Temporización.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-357">This is not represented in the **Timing** panel.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Representación de barra de línea de la www.bing.com solicitud" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="63b5c-359">Representación de barra de línea de la `www.bing.com` solicitud</span><span class="sxs-lookup"><span data-stu-id="63b5c-359">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="La herramienta Red" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="63b5c-361">La **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="63b5c-361">The **Network** tool</span></span>  
<span data-ttu-id="63b5c-362">: ::image-end:::</span><span class="sxs-lookup"><span data-stu-id="63b5c-362">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a><span data-ttu-id="63b5c-363">Ver métricas de memoria</span><span class="sxs-lookup"><span data-stu-id="63b5c-363">View memory metrics</span></span>  

<span data-ttu-id="63b5c-364">Activa la casilla **Memoria** para ver las métricas de memoria de la última grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-364">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="La casilla Memoria" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="63b5c-366">La **casilla Memoria**</span><span class="sxs-lookup"><span data-stu-id="63b5c-366">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-367">DevTools muestra un nuevo gráfico **de** memoria, encima **del** panel Resumen.</span><span class="sxs-lookup"><span data-stu-id="63b5c-367">DevTools displays a new **Memory** chart, above the **Summary** panel.</span></span>  <span data-ttu-id="63b5c-368">También hay un nuevo gráfico debajo del **gráfico NET,** denominado **HEAP**.</span><span class="sxs-lookup"><span data-stu-id="63b5c-368">There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="63b5c-369">El **gráfico HEAP** proporciona la misma información que la línea **de montón JS** en el gráfico **memoria.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-369">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memoria" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="63b5c-371">Métricas de memoria</span><span class="sxs-lookup"><span data-stu-id="63b5c-371">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-372">Las líneas coloreadas del gráfico se asignan a las casillas de color situadas encima del gráfico.</span><span class="sxs-lookup"><span data-stu-id="63b5c-372">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="63b5c-373">Deshabilite una casilla para ocultar esa categoría del gráfico.</span><span class="sxs-lookup"><span data-stu-id="63b5c-373">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="63b5c-374">El gráfico solo muestra la región de la grabación que está seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="63b5c-374">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="63b5c-375">Por ejemplo, en la  figura anterior, el gráfico de memoria solo muestra el uso de memoria de alrededor de la marca de 400 ms a la marca de 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="63b5c-375">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a><span data-ttu-id="63b5c-376">Ver la duración de una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-376">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="63b5c-377">Al analizar una sección como **Red** o **Principal**, a veces se necesita una estimación más precisa del tiempo que tardaron determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="63b5c-377">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="63b5c-378">Mantenga presionado , elija y mantenga presionado y arrastre hacia la izquierda o la `Shift` derecha para seleccionar una parte de la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-378">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="63b5c-379">En la parte inferior de la selección, DevTools muestra cuánto tiempo tardó esa parte.</span><span class="sxs-lookup"><span data-stu-id="63b5c-379">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Ver la duración de una parte de una grabación" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="63b5c-381">Ver la duración de una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="63b5c-381">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <a name="view-a-screenshot"></a><span data-ttu-id="63b5c-382">Ver una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="63b5c-382">View a screenshot</span></span>  

<span data-ttu-id="63b5c-383">Ve a [Capturar capturas de pantalla mientras grabas](#capture-screenshots-while-recording) para obtener información sobre cómo activar capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="63b5c-383">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="63b5c-384">Mantenga el mouse sobre **la información** general para ver una captura de pantalla de cómo se ve la página durante ese momento de la grabación.</span><span class="sxs-lookup"><span data-stu-id="63b5c-384">Hover on the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="63b5c-385">Overview **es** la sección que contiene los gráficos **CPU,** **FPS**y **NET.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-385">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Ver una captura de pantalla" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="63b5c-387">Ver una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="63b5c-387">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-388">También puede ver capturas de pantalla eligiendo un marco en la **sección** Marcos.</span><span class="sxs-lookup"><span data-stu-id="63b5c-388">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="63b5c-389">DevTools muestra una versión pequeña de la captura de pantalla en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-389">DevTools displays a small version of the screenshot in the **Summary** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Ver una captura de pantalla en el panel Resumen" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="63b5c-391">Ver una captura de pantalla en el panel **Resumen**</span><span class="sxs-lookup"><span data-stu-id="63b5c-391">View a screenshot in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-392">Elija la miniatura del panel **Resumen** para acercar la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="63b5c-392">Choose the thumbnail in the **Summary** panel to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Acercar una captura de pantalla desde el panel Resumen" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="63b5c-394">Acercar una captura de pantalla desde el panel **Resumen**</span><span class="sxs-lookup"><span data-stu-id="63b5c-394">Zoom into a screenshot from the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-layers-information"></a><span data-ttu-id="63b5c-395">Ver información de capas</span><span class="sxs-lookup"><span data-stu-id="63b5c-395">View layers information</span></span>  

<span data-ttu-id="63b5c-396">Para ver información de capas avanzadas sobre un marco:</span><span class="sxs-lookup"><span data-stu-id="63b5c-396">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="63b5c-397">[Activar instrumentación de pintura avanzada](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="63b5c-397">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="63b5c-398">Elija un marco en la **sección Marcos.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-398">Choose a frame in the **Frames** section.</span></span>  <span data-ttu-id="63b5c-399">DevTools muestra información sobre las capas del nuevo panel **Capas,** junto al panel **Registro de** eventos.</span><span class="sxs-lookup"><span data-stu-id="63b5c-399">DevTools displays information about the layers in the new **Layers** panel, next to the **Event Log** panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Panel Capas" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="63b5c-401">Panel **Capas**</span><span class="sxs-lookup"><span data-stu-id="63b5c-401">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="63b5c-402">Mantenga el mouse sobre una capa para resaltarla en el diagrama.</span><span class="sxs-lookup"><span data-stu-id="63b5c-402">Hover on a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Resaltar una capa" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="63b5c-404">Resaltar una capa</span><span class="sxs-lookup"><span data-stu-id="63b5c-404">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="63b5c-405">Para mover el diagrama:</span><span class="sxs-lookup"><span data-stu-id="63b5c-405">To move the diagram:</span></span>  

*   <span data-ttu-id="63b5c-406">Elija **Modo panorámica** \( Modo panorámica ![ \) para desplazarse por los ](../media/pan-mode-icon.msft.png) ejes X e Y.</span><span class="sxs-lookup"><span data-stu-id="63b5c-406">Choose **Pan Mode** \(![Pan Mode](../media/pan-mode-icon.msft.png)\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="63b5c-407">Elija **Girar modo** \( Girar modo \) para girar a lo largo del eje ![ ](../media/rotate-mode-icon.msft.png) Z.</span><span class="sxs-lookup"><span data-stu-id="63b5c-407">Choose **Rotate Mode** \(![Rotate Mode](../media/rotate-mode-icon.msft.png)\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="63b5c-408">Elija **Restablecer transformación** \( Restablecer transformación ![ ](../media/reset-transform-icon.msft.png) \) para restablecer el diagrama a la posición original.</span><span class="sxs-lookup"><span data-stu-id="63b5c-408">Choose **Reset Transform** \(![Reset Transform](../media/reset-transform-icon.msft.png)\) to reset the diagram to the original position.</span></span>  
    
### <a name="view-paint-profiler"></a><span data-ttu-id="63b5c-409">Ver el perfilador de pintura</span><span class="sxs-lookup"><span data-stu-id="63b5c-409">View paint profiler</span></span>  

<span data-ttu-id="63b5c-410">Para ver información avanzada sobre un evento de pintura:</span><span class="sxs-lookup"><span data-stu-id="63b5c-410">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="63b5c-411">[Activar](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="63b5c-411">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="63b5c-412">Elija un **evento Paint** en la **sección** Main.</span><span class="sxs-lookup"><span data-stu-id="63b5c-412">Choose a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Panel De perfiles de pintura" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="63b5c-414">Panel **De perfiles de pintura**</span><span class="sxs-lookup"><span data-stu-id="63b5c-414">The **Paint Profiler** panel</span></span>  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a><span data-ttu-id="63b5c-415">Analizar el rendimiento de representación con la herramienta de representación</span><span class="sxs-lookup"><span data-stu-id="63b5c-415">Analyze rendering performance with the Rendering tool</span></span>  

<span data-ttu-id="63b5c-416">Use las características del panel **Representación** para ayudar a visualizar el rendimiento de representación de la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-416">Use the features of the **Rendering** panel to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="63b5c-417">Para abrir la **herramienta de** representación:</span><span class="sxs-lookup"><span data-stu-id="63b5c-417">To open the **Rendering** tool:</span></span>  

1.  <span data-ttu-id="63b5c-418">[Abra el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="63b5c-418">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="63b5c-419">Comience a escribir `Rendering` y seleccione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="63b5c-419">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="63b5c-420">DevTools muestra la **herramienta de** representación en la parte inferior de la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="63b5c-420">DevTools displays the **Rendering** tool at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="La herramienta de representación" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="63b5c-422">La **herramienta de representación**</span><span class="sxs-lookup"><span data-stu-id="63b5c-422">The **Rendering** tool</span></span>  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a><span data-ttu-id="63b5c-423">Ver fotogramas por segundo en tiempo real con el medidor FPS</span><span class="sxs-lookup"><span data-stu-id="63b5c-423">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="63b5c-424">El **medidor FPS** es una superposición que aparece en la esquina superior derecha de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="63b5c-424">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="63b5c-425">Proporciona una estimación en tiempo real de FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-425">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="63b5c-426">Para abrir el **medidor FPS:**</span><span class="sxs-lookup"><span data-stu-id="63b5c-426">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="63b5c-427">Abra la **herramienta De representación.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-427">Open the **Rendering** tool.</span></span>  <span data-ttu-id="63b5c-428">[Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).</span><span class="sxs-lookup"><span data-stu-id="63b5c-428">[Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="63b5c-429">Activa la casilla **Fps Meter.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-429">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="El medidor fps" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="63b5c-431">El **medidor fps**</span><span class="sxs-lookup"><span data-stu-id="63b5c-431">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a><span data-ttu-id="63b5c-432">Ver eventos de pintura en tiempo real con Paint Flashing</span><span class="sxs-lookup"><span data-stu-id="63b5c-432">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="63b5c-433">Use Paint Flashing para obtener una vista en tiempo real de todos los eventos de pintura de la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-433">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="63b5c-434">Cada vez que se vuelve a pintar una parte de la página, DevTools describe esa sección en verde.</span><span class="sxs-lookup"><span data-stu-id="63b5c-434">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="63b5c-435">Para activar Paint Flashing, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="63b5c-435">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="63b5c-436">Abra la **herramienta De representación.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-436">Open the **Rendering** tool.</span></span>  <span data-ttu-id="63b5c-437">Vaya a [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).</span><span class="sxs-lookup"><span data-stu-id="63b5c-437">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="63b5c-438">Activa la casilla **Destello de pintura.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-438">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Flashing" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="63b5c-440">Paint Flashing</span><span class="sxs-lookup"><span data-stu-id="63b5c-440">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a><span data-ttu-id="63b5c-441">Ver una superposición de capas con bordes de capa</span><span class="sxs-lookup"><span data-stu-id="63b5c-441">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="63b5c-442">Usa **Bordes de capa** para ver una superposición de bordes de capa y mosaicos en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-442">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="63b5c-443">Para activar bordes de capa, realice las siguientes acciones,</span><span class="sxs-lookup"><span data-stu-id="63b5c-443">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="63b5c-444">Abra la **herramienta De representación.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-444">Open the **Rendering** tool.</span></span>  <span data-ttu-id="63b5c-445">Vaya a [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).</span><span class="sxs-lookup"><span data-stu-id="63b5c-445">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="63b5c-446">Activa la casilla **Bordes de** capa.</span><span class="sxs-lookup"><span data-stu-id="63b5c-446">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordes de capa" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="63b5c-448">Bordes de capa</span><span class="sxs-lookup"><span data-stu-id="63b5c-448">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="63b5c-449">Vaya a los comentarios de [debug_colors.cc para][ChromiumDebugColors] obtener una explicación de las codificaciones de color.</span><span class="sxs-lookup"><span data-stu-id="63b5c-449">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <a name="find-scroll-performance-issues-in-realtime"></a><span data-ttu-id="63b5c-450">Buscar problemas de rendimiento de desplazamiento en tiempo real</span><span class="sxs-lookup"><span data-stu-id="63b5c-450">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="63b5c-451">Use Problemas de rendimiento de desplazamiento para identificar los elementos de la página que tienen escuchas de eventos relacionadas con el desplazamiento que pueden dañar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="63b5c-451">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="63b5c-452">DevTools describe los elementos potencialmente problemáticos en la teal.</span><span class="sxs-lookup"><span data-stu-id="63b5c-452">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="63b5c-453">Para ver problemas de rendimiento de desplazamiento, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="63b5c-453">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="63b5c-454">Abra la **herramienta De representación.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-454">Open the **Rendering** tool.</span></span>  <span data-ttu-id="63b5c-455">Vaya a [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).</span><span class="sxs-lookup"><span data-stu-id="63b5c-455">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="63b5c-456">Active la casilla **Problemas de rendimiento de desplazamiento.**</span><span class="sxs-lookup"><span data-stu-id="63b5c-456">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Problemas de rendimiento de desplazamiento indica que los objetos restringidos por ventanilla sin capa pueden dañar el rendimiento del desplazamiento" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="63b5c-458">**Problemas de rendimiento de desplazamiento** indica que los objetos restringidos por ventanilla sin capa pueden dañar el rendimiento del desplazamiento</span><span class="sxs-lookup"><span data-stu-id="63b5c-458">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="63b5c-459">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63b5c-459">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abra el menú Comando: ejecute comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Introducción al análisis del rendimiento en tiempo de ejecución | Microsoft Docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demostración de pestañas de actividad | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc: búsqueda de código"  

> [!NOTE]
> <span data-ttu-id="63b5c-465">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63b5c-465">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63b5c-466">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="63b5c-466">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="63b5c-468">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63b5c-468">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
