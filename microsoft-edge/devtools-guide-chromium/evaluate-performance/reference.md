---
title: Referencia de análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611751"
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







# <span data-ttu-id="e9536-103">Referencia de análisis de rendimiento</span><span class="sxs-lookup"><span data-stu-id="e9536-103">Performance Analysis Reference</span></span>   



<span data-ttu-id="e9536-104">Esta página es una referencia completa de las características de Microsoft Edge DevTools relacionadas con el análisis del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e9536-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="e9536-105">Vea [empezar a analizar el rendimiento en tiempo de ejecución][DevtoolsEvaluatePerformanceGettingStarted] para obtener un tutorial guiado sobre cómo analizar el rendimiento de una página con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="e9536-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="e9536-106">Registrar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="e9536-106">Record performance</span></span>   

### <span data-ttu-id="e9536-107">Registrar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e9536-107">Record runtime performance</span></span>   

<span data-ttu-id="e9536-108">Grabe el rendimiento en tiempo de ejecución cuando desee analizar el rendimiento de una página mientras se está ejecutando, en lugar de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="e9536-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="e9536-109">Vaya a la página que desea analizar.</span><span class="sxs-lookup"><span data-stu-id="e9536-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="e9536-110">Haga clic en la pestaña **rendimiento** en DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9536-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="e9536-111">Haga **clic en grabar** ![ Registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="e9536-111">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    
    > ##### <span data-ttu-id="e9536-112">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e9536-112">Figure 1</span></span>  
    > **<span data-ttu-id="e9536-113">Grabar</span><span class="sxs-lookup"><span data-stu-id="e9536-113">Record</span></span>**  
    > ![Grabar][ImageRecord]  

1.  <span data-ttu-id="e9536-115">Interactúe con la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-115">Interact with the page.</span></span>  <span data-ttu-id="e9536-116">DevTools registra toda la actividad de la página que se produce como resultado de las interacciones.</span><span class="sxs-lookup"><span data-stu-id="e9536-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="e9536-117">Vuelva a hacer clic en **grabar** o haga clic en **detener** para detener la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-117">Click **Record** again or click **Stop** to stop recording.</span></span>  

### <span data-ttu-id="e9536-118">Registrar el rendimiento de la carga</span><span class="sxs-lookup"><span data-stu-id="e9536-118">Record load performance</span></span>   

<span data-ttu-id="e9536-119">Registre el rendimiento de la carga cuando desee analizar el rendimiento de una página mientras se está cargando, en lugar de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e9536-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="e9536-120">Vaya a la página que desea analizar.</span><span class="sxs-lookup"><span data-stu-id="e9536-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="e9536-121">Abra el panel **rendimiento** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9536-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="e9536-122">Haga clic en actualizar página de actualización de **Página** ![ ][ImageRefreshPageIcon] .</span><span class="sxs-lookup"><span data-stu-id="e9536-122">Click **Refresh page** ![Refresh Page][ImageRefreshPageIcon].</span></span>  <span data-ttu-id="e9536-123">DevTools registra las métricas de rendimiento mientras se actualiza la página y, a continuación, detiene automáticamente la grabación un par de segundos después de que finalice la carga.</span><span class="sxs-lookup"><span data-stu-id="e9536-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    > ##### <span data-ttu-id="e9536-124">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e9536-124">Figure 2</span></span>  
    > **<span data-ttu-id="e9536-125">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="e9536-125">Refresh page</span></span>**  
    > ![Actualizar página][ImageRefreshPage]  

<span data-ttu-id="e9536-127">DevTools automáticamente acerca de la parte de la grabación donde se produjo la mayor parte de la actividad.</span><span class="sxs-lookup"><span data-stu-id="e9536-127">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

> ##### <span data-ttu-id="e9536-128">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="e9536-128">Figure 3</span></span>  
> <span data-ttu-id="e9536-129">Una grabación de página</span><span class="sxs-lookup"><span data-stu-id="e9536-129">A page-load recording</span></span>  
> ![Una grabación de página][ImageLoadRecording]  

### <span data-ttu-id="e9536-131">Capturar capturas de pantallas durante la grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-131">Capture screenshots while recording</span></span>   

<span data-ttu-id="e9536-132">Active la casilla **capturas** de pantalla para capturar una captura de pantalla de cada fotograma mientras graba.</span><span class="sxs-lookup"><span data-stu-id="e9536-132">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

> ##### <span data-ttu-id="e9536-133">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="e9536-133">Figure 4</span></span>  
> <span data-ttu-id="e9536-134">La casilla de verificación **capturas de pantallas**</span><span class="sxs-lookup"><span data-stu-id="e9536-134">The **Screenshots** checkbox</span></span>  
> ![La casilla de verificación capturas de pantallas][ImageScreenshots]  

<span data-ttu-id="e9536-136">Consulte [ver una captura de pantalla](#view-a-screenshot) para obtener información sobre cómo interactuar con capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9536-136">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="e9536-137">Forzar recolección de elementos no utilizados al grabar</span><span class="sxs-lookup"><span data-stu-id="e9536-137">Force garbage collection while recording</span></span>   

<span data-ttu-id="e9536-138">Mientras graba una página, haga clic en **recopilar** elementos no usados recolectar basura ![ ][ImageCollectGarbageIcon] para forzar la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="e9536-138">While you are recording a page, click **Collect garbage** ![Collect garbage][ImageCollectGarbageIcon] to force garbage collection.</span></span>  

> ##### <span data-ttu-id="e9536-139">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="e9536-139">Figure 5</span></span>  
> <span data-ttu-id="e9536-140">Recopilar basura</span><span class="sxs-lookup"><span data-stu-id="e9536-140">Collect garbage</span></span>  
> ![Recopilar basura][ImageCollectGarbage]  

### <span data-ttu-id="e9536-142">Mostrar configuración de grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-142">Show recording settings</span></span>   

<span data-ttu-id="e9536-143">Haga clic en **capturar** ![ configuración ][ImageCaptureSettingsIcon] de captura de configuración para exponer más opciones de configuración relacionadas con el modo en que DevTools captura las grabaciones de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e9536-143">Click **Capture settings** ![Capture settings][ImageCaptureSettingsIcon] to expose more settings related to how DevTools captures performance recordings.</span></span>  

> ##### <span data-ttu-id="e9536-144">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="e9536-144">Figure 6</span></span>  
> <span data-ttu-id="e9536-145">La sección **configuración de captura**</span><span class="sxs-lookup"><span data-stu-id="e9536-145">The **Capture settings** section</span></span>  
> ![La sección configuración de captura][ImageCaptureSettings]  

### <span data-ttu-id="e9536-147">Deshabilitar ejemplos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="e9536-147">Disable JavaScript samples</span></span>   

<span data-ttu-id="e9536-148">De forma predeterminada, la sección **principal** de una grabación muestra las pilas de llamadas detalladas de las funciones de JavaScript a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-148">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="e9536-149">Para deshabilitar estas pilas de llamadas:</span><span class="sxs-lookup"><span data-stu-id="e9536-149">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="e9536-150">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="e9536-150">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="e9536-151">Consulte [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="e9536-151">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="e9536-152">Active la casilla **deshabilitar ejemplos de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="e9536-152">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="e9536-153">Realizar una grabación de la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-153">Take a recording of the page.</span></span>  

<span data-ttu-id="e9536-154">En las [figuras 7](#figure-7) y [8](#figure-8) se muestra la diferencia entre deshabilitar y habilitar ejemplos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9536-154">[Figure 7](#figure-7) and [Figure 8](#figure-8) show the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="e9536-155">La sección **principal** de la grabación es mucho más corta cuando el muestreo está deshabilitado, porque omite todas las pilas de llamadas de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9536-155">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

> ##### <span data-ttu-id="e9536-156">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="e9536-156">Figure 7</span></span>  
> <span data-ttu-id="e9536-157">Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS</span><span class="sxs-lookup"><span data-stu-id="e9536-157">An example of a recording when JS samples are disabled</span></span>  
> ![Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS][ImageJSSamplesDisabled]  

> ##### <span data-ttu-id="e9536-159">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="e9536-159">Figure 8</span></span>  
> <span data-ttu-id="e9536-160">Ejemplo de una grabación cuando se habilitan ejemplos de JS</span><span class="sxs-lookup"><span data-stu-id="e9536-160">An example of a recording when JS samples are enabled</span></span>  
> ![Ejemplo de una grabación cuando se habilitan ejemplos de JS][ImageJSSamplesEnabled]  

### <span data-ttu-id="e9536-162">Limitar la red durante la grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-162">Throttle the network while recording</span></span>   

<span data-ttu-id="e9536-163">Para limitar la red durante la grabación:</span><span class="sxs-lookup"><span data-stu-id="e9536-163">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="e9536-164">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="e9536-164">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="e9536-165">Consulte [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="e9536-165">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="e9536-166">Establezca **red** en el nivel deseado de limitación.</span><span class="sxs-lookup"><span data-stu-id="e9536-166">Set **Network** to the desired level of throttling.</span></span>  

### <span data-ttu-id="e9536-167">Limitar la CPU durante la grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-167">Throttle the CPU while recording</span></span>   

<span data-ttu-id="e9536-168">Para limitar la CPU durante la grabación:</span><span class="sxs-lookup"><span data-stu-id="e9536-168">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="e9536-169">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="e9536-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="e9536-170">Consulte [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="e9536-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="e9536-171">Establezca la **CPU** en el nivel deseado de limitación.</span><span class="sxs-lookup"><span data-stu-id="e9536-171">Set **CPU** to the desired level of throttling.</span></span>  

<span data-ttu-id="e9536-172">El límite es relativo a las capacidades de su equipo.</span><span class="sxs-lookup"><span data-stu-id="e9536-172">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="e9536-173">Por ejemplo, la opción **2x ralentización** hace que la CPU funcione 2 veces más lentas de lo normal.</span><span class="sxs-lookup"><span data-stu-id="e9536-173">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="e9536-174">DevTools no simulan verdaderamente las CPU de los dispositivos móviles, porque la arquitectura de los dispositivos móviles es muy diferente de la de los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="e9536-174">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="e9536-175">Habilitar la instrumentación avanzada de pintura</span><span class="sxs-lookup"><span data-stu-id="e9536-175">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="e9536-176">Para ver la instrumentación de pintura detallada:</span><span class="sxs-lookup"><span data-stu-id="e9536-176">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="e9536-177">Abra el menú de **configuración de captura** .</span><span class="sxs-lookup"><span data-stu-id="e9536-177">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="e9536-178">Consulte [Mostrar configuración de grabación](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="e9536-178">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="e9536-179">Active la casilla **Habilitar el instrumental de pintura avanzada (lento)** .</span><span class="sxs-lookup"><span data-stu-id="e9536-179">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="e9536-180">Para obtener información sobre cómo interactuar con la información de las pinturas, consulte [Ver capas](#view-layers-information) y [Ver generador de perfiles de pintura](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="e9536-180">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="e9536-181">Guardar una grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-181">Save a recording</span></span>   

<span data-ttu-id="e9536-182">Para guardar una grabación, haga clic con el botón derecho y seleccione **Guardar perfil**.</span><span class="sxs-lookup"><span data-stu-id="e9536-182">To save a recording, right-click and select **Save Profile**.</span></span>  

> ##### <span data-ttu-id="e9536-183">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="e9536-183">Figure 9</span></span>  
> **<span data-ttu-id="e9536-184">Guardar perfil</span><span class="sxs-lookup"><span data-stu-id="e9536-184">Save Profile</span></span>**  
> ![Guardar perfil][ImageSaveProfile]  

## <span data-ttu-id="e9536-186">Cargar una grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-186">Load a recording</span></span>   

<span data-ttu-id="e9536-187">Para cargar una grabación, haga clic con el botón derecho y seleccione **cargar perfil**.</span><span class="sxs-lookup"><span data-stu-id="e9536-187">To load a recording, right-click and select **Load Profile**.</span></span>  

> ##### <span data-ttu-id="e9536-188">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="e9536-188">Figure 10</span></span>  
> **<span data-ttu-id="e9536-189">Cargar perfil</span><span class="sxs-lookup"><span data-stu-id="e9536-189">Load Profile</span></span>**  
> ![Cargar perfil][ImageLoadProfile]  

## <span data-ttu-id="e9536-191">Borrar la grabación anterior</span><span class="sxs-lookup"><span data-stu-id="e9536-191">Clear the previous recording</span></span>   

<span data-ttu-id="e9536-192">Después de realizar una grabación, presione **Borrar** grabación ![ Borrar grabación ][ImageClearRecordingIcon] para borrar esa grabación en el panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="e9536-192">After making a recording, press **Clear recording** ![Clear recording][ImageClearRecordingIcon] to clear that recording from the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="e9536-193">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="e9536-193">Figure 11</span></span>  
> <span data-ttu-id="e9536-194">Borrar grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-194">Clear recording</span></span>  
> ![Borrar grabación][ImageClearRecording]  

## <span data-ttu-id="e9536-196">Analizar una grabación de rendimiento</span><span class="sxs-lookup"><span data-stu-id="e9536-196">Analyze a performance recording</span></span>   

<span data-ttu-id="e9536-197">Después de [grabar el rendimiento en tiempo de ejecución](#record-runtime-performance) o el rendimiento de la [carga de registros](#record-load-performance), el panel **rendimiento** proporciona una gran cantidad de datos para analizar el rendimiento de lo que sucedió.</span><span class="sxs-lookup"><span data-stu-id="e9536-197">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="e9536-198">Seleccionar una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-198">Select a portion of a recording</span></span>   

<span data-ttu-id="e9536-199">Arrastre el ratón hacia la izquierda o hacia la derecha en la **información general** para seleccionar una parte de una grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-199">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="e9536-200">La **información general** es la sección que contiene los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="e9536-200">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="e9536-201">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="e9536-201">Figure 12</span></span>  
> <span data-ttu-id="e9536-202">Arrastrar el mouse por la información general para zoom</span><span class="sxs-lookup"><span data-stu-id="e9536-202">Dragging the mouse across the Overview to zoom</span></span>  
> ![Arrastrar el mouse por la información general para zoom][ImageZoom]  

<span data-ttu-id="e9536-204">Para seleccionar una parte con el teclado:</span><span class="sxs-lookup"><span data-stu-id="e9536-204">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="e9536-205">Haga clic en el fondo de la sección **principal** o en cualquiera de las secciones que hay junto a ella, como **interacciones**, **red**o **GPU**.</span><span class="sxs-lookup"><span data-stu-id="e9536-205">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="e9536-206">Este flujo de trabajo de teclado solo funciona cuando una de estas secciones está en el foco.</span><span class="sxs-lookup"><span data-stu-id="e9536-206">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="e9536-207">Use las `W` teclas,, `A` `S` , `D` para acercar, mover a la izquierda, alejar y desplazar a la derecha, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e9536-207">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="e9536-208">Para seleccionar una parte con un panel táctil:</span><span class="sxs-lookup"><span data-stu-id="e9536-208">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="e9536-209">Mantenga el mouse sobre la sección **Descripción general** o en la sección de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="e9536-209">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="e9536-210">La sección de **información general** es el área que contiene los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="e9536-210">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="e9536-211">La sección de **detalles** es el área que contiene la sección **principal** , la sección **interacciones** , etc.</span><span class="sxs-lookup"><span data-stu-id="e9536-211">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="e9536-212">Con dos dedos, deslice el dedo hacia arriba para alejar, deslice el dedo hacia la izquierda, deslice el dedo hacia abajo y deslice el dedo hacia la derecha para desplazarse hacia la derecha.</span><span class="sxs-lookup"><span data-stu-id="e9536-212">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="e9536-213">Para desplazarse por un gráfico de llamas largo en la sección **principal** o en cualquiera de los vecinos, haga clic y mantenga presionado mientras arrastra hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="e9536-213">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="e9536-214">Arrastre hacia la izquierda y hacia la derecha para mover qué parte de la grabación está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="e9536-214">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="e9536-215">Buscar actividades</span><span class="sxs-lookup"><span data-stu-id="e9536-215">Search activities</span></span>   

<span data-ttu-id="e9536-216">Pulse `Control` + `F` \ (Windows \) o `Command` + `F` \ (MacOS \) para abrir el cuadro de búsqueda en la parte inferior del panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="e9536-216">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="e9536-217">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="e9536-217">Figure 13</span></span>  
> <span data-ttu-id="e9536-218">Uso de Regex en el cuadro de búsqueda de la parte inferior de la ventana para encontrar cualquier actividad que comience con</span><span class="sxs-lookup"><span data-stu-id="e9536-218">Using regex in the search box at the bottom of the window to find any activity that begins with</span></span> `E`  
> ![El cuadro de búsqueda][ImageSearch]  

<span data-ttu-id="e9536-220">Para navegar por las actividades que coinciden con la consulta:</span><span class="sxs-lookup"><span data-stu-id="e9536-220">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="e9536-221">Use los **Previous** ![ botones anterior ][ImagePreviousIcon] y **siguiente** ![ siguiente ][ImageNextIcon] .</span><span class="sxs-lookup"><span data-stu-id="e9536-221">Use the **Previous** ![Previous][ImagePreviousIcon] and **Next** ![Next][ImageNextIcon] buttons.</span></span>  
*   <span data-ttu-id="e9536-222">Pulse `Shift` + `Enter` para seleccionar la anterior o `Enter` para seleccionar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9536-222">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="e9536-223">Para modificar la configuración de la consulta:</span><span class="sxs-lookup"><span data-stu-id="e9536-223">To modify query settings:</span></span>  

*   <span data-ttu-id="e9536-224">Pulse mayúsculas de minúsculas **distingue mayúsculas** ![ de minúsculas ][ImageSearchCaseIcon] para hacer distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e9536-224">Press **Case sensitive** ![Case sensitive][ImageSearchCaseIcon] to make the query case sensitive.</span></span>  
*   <span data-ttu-id="e9536-225">Presione **Regex** ![ regex ][ImageSearchRegexIcon] para usar una expresión regular en la consulta.</span><span class="sxs-lookup"><span data-stu-id="e9536-225">Press **Regex** ![Regex][ImageSearchRegexIcon] to use a regular expression in your query.</span></span>  

<span data-ttu-id="e9536-226">Para ocultar el cuadro de búsqueda, presione **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="e9536-226">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="e9536-227">Ver actividad de subproceso principal</span><span class="sxs-lookup"><span data-stu-id="e9536-227">View main thread activity</span></span>   

<span data-ttu-id="e9536-228">Use la sección **principal** para ver la actividad que se produjo en el subproceso principal de la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-228">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

> ##### <span data-ttu-id="e9536-229">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="e9536-229">Figure 14</span></span>  
> <span data-ttu-id="e9536-230">La sección **principal**</span><span class="sxs-lookup"><span data-stu-id="e9536-230">The **Main** section</span></span>  
> ![La sección principal][ImageMain]  

<span data-ttu-id="e9536-232">Haga clic en un evento para ver más información sobre él en la pestaña **Resumen** .  DevTools describe el evento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e9536-232">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

> ##### <span data-ttu-id="e9536-233">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="e9536-233">Figure 15</span></span>  
> <span data-ttu-id="e9536-234">Más información sobre la `anonymous` función en la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="e9536-234">More information about the `anonymous` function in the **Summary** tab</span></span>  
> ![Más información sobre la función anónima en la pestaña Resumen][ImageMainEventSummary]  

<span data-ttu-id="e9536-236">DevTools representa la actividad principal del subproceso con un gráfico de llama.</span><span class="sxs-lookup"><span data-stu-id="e9536-236">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="e9536-237">El eje x representa la grabación a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="e9536-237">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="e9536-238">El eje y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e9536-238">The y-axis represents the call stack.</span></span>  <span data-ttu-id="e9536-239">Los eventos en la parte superior provocan los eventos que se encuentran por debajo.</span><span class="sxs-lookup"><span data-stu-id="e9536-239">The events on top cause the events below it.</span></span>  

> ##### <span data-ttu-id="e9536-240">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="e9536-240">Figure 16</span></span>  
> <span data-ttu-id="e9536-241">Un gráfico de llama en la sección **principal**</span><span class="sxs-lookup"><span data-stu-id="e9536-241">A flame chart in the **Main** section</span></span>  
> ![Un gráfico de llamas][ImageFlameChart]  

<span data-ttu-id="e9536-243">En la [figura 16](#figure-16), un `click` evento ha provocado un `Function Call` en en la `activitytabs.js` línea 53.</span><span class="sxs-lookup"><span data-stu-id="e9536-243">In [Figure 16](#figure-16), a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="e9536-244">A continuación `Function Call` , verá que se llamó a una función anónima.</span><span class="sxs-lookup"><span data-stu-id="e9536-244">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="e9536-245">La función anónima a la que se llamó, a la que llamó `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="e9536-245">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="e9536-246">DevTools asigna scripts a colores aleatorios.</span><span class="sxs-lookup"><span data-stu-id="e9536-246">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="e9536-247">En la [figura 16](#figure-16), las llamadas de función de un script se muestran coloreadas en verde.</span><span class="sxs-lookup"><span data-stu-id="e9536-247">In [Figure 16](#figure-16), function calls from one script are colored light green.</span></span>  <span data-ttu-id="e9536-248">Las llamadas desde otra secuencia de comandos tienen color beige.</span><span class="sxs-lookup"><span data-stu-id="e9536-248">Calls from another script are colored beige.</span></span>  <span data-ttu-id="e9536-249">El amarillo más oscuro representa la actividad de scripting y el evento morado representa la actividad de representación.</span><span class="sxs-lookup"><span data-stu-id="e9536-249">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="e9536-250">Estos eventos amarillos y amarillos más oscuros son coherentes en todas las grabaciones.</span><span class="sxs-lookup"><span data-stu-id="e9536-250">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="e9536-251">Consulte [deshabilitar muestras de JavaScript](#disable-javascript-samples) si desea ocultar el gráfico detallado de llamadas de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9536-251">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="e9536-252">Cuando se deshabilitan los ejemplos de JS, solo verá eventos de alto nivel, como `Event: click` y `Function Call` de la [figura 16](#figure-16).</span><span class="sxs-lookup"><span data-stu-id="e9536-252">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from [Figure 16](#figure-16).</span></span>  

### <span data-ttu-id="e9536-253">Ver actividades en una tabla</span><span class="sxs-lookup"><span data-stu-id="e9536-253">View activities in a table</span></span>   

<span data-ttu-id="e9536-254">Después de grabar una página, no es necesario basarse únicamente en la sección **principal** para analizar las actividades.</span><span class="sxs-lookup"><span data-stu-id="e9536-254">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="e9536-255">DevTools también proporciona tres vistas tabulares para analizar actividades.</span><span class="sxs-lookup"><span data-stu-id="e9536-255">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="e9536-256">Cada vista le ofrece una perspectiva diferente en las actividades:</span><span class="sxs-lookup"><span data-stu-id="e9536-256">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="e9536-257">Cuando desee ver las actividades raíz que producen el mayor trabajo, use [la pestaña **árbol de llamadas** ](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-257">When you want to view the root activities that cause the most work, use [the **Call Tree** tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="e9536-258">Cuando desee ver las actividades en las que el más tiempo se dedicó directamente, use [la pestaña **de la parte inferior** ](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-258">When you want to view the activities where the most time was directly spent, use [the **Bottom-Up** tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="e9536-259">Cuando desee ver las actividades en el orden en el que se produjeron durante la grabación, use [la pestaña **registro de eventos** ](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-259">When you want to view the activities in the order in which they occurred during the recording, use [the **Event Log** tab](#the-event-log-tab).</span></span>  

> [!NOTE]
> <span data-ttu-id="e9536-260">Las tres secciones siguientes hacen referencia a la misma demostración.</span><span class="sxs-lookup"><span data-stu-id="e9536-260">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="e9536-261">Ejecute la demostración usted mismo en la [demostración de pestañas de actividad][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="e9536-261">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="e9536-262">Actividades raíz</span><span class="sxs-lookup"><span data-stu-id="e9536-262">Root activities</span></span>   

<span data-ttu-id="e9536-263">A continuación se explica el concepto de **actividades raíz** que se menciona en las secciones **árbol de llamadas** , pestaña **ascendente** y registro de **eventos** .</span><span class="sxs-lookup"><span data-stu-id="e9536-263">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="e9536-264">Las actividades raíz son aquellas que hacen que el explorador realice algún trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9536-264">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="e9536-265">Por ejemplo, al hacer clic en una página, el explorador desencadena una `Event` actividad como la actividad raíz.</span><span class="sxs-lookup"><span data-stu-id="e9536-265">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="e9536-266">Esto `Event` puede hacer que se ejecute un controlador, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="e9536-266">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="e9536-267">En el gráfico de llamas de la sección **principal** , las actividades raíz se encuentran en la parte superior del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e9536-267">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="e9536-268">En las pestañas **árbol de llamadas** y **registro de eventos** , las actividades raíz son los elementos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e9536-268">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="e9536-269">Para obtener un ejemplo de actividades raíz, consulte [la ficha árbol de llamadas](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="e9536-269">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="e9536-270">La ficha árbol de llamadas</span><span class="sxs-lookup"><span data-stu-id="e9536-270">The Call Tree tab</span></span>   

<span data-ttu-id="e9536-271">Use la pestaña **árbol de llamadas** para ver qué actividades de [raíz](#root-activities) hacen la mayor parte del trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9536-271">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="e9536-272">La pestaña **árbol de llamadas** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-272">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="e9536-273">Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="e9536-273">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="e9536-274">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="e9536-274">Figure 17</span></span>  
> <span data-ttu-id="e9536-275">La ficha **árbol de llamadas**</span><span class="sxs-lookup"><span data-stu-id="e9536-275">The **Call Tree** tab</span></span>  
> ![La ficha árbol de llamadas][ImageCallTree]  

<span data-ttu-id="e9536-277">En la [ilustración 17](#figure-17), el nivel superior de los elementos de la columna **actividad** , como `Evaluate Script` y `Parse HTML` son las actividades raíz.</span><span class="sxs-lookup"><span data-stu-id="e9536-277">In [Figure 17](#figure-17), the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="e9536-278">El anidamiento representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e9536-278">The nesting represents the call stack.</span></span>  <span data-ttu-id="e9536-279">Por ejemplo, en la [figura 17](#figure-17), `Parse HTML` que causó `Evaluate Script` el `Compile Script` `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="e9536-279">For example, in [Figure 17](#figure-17), `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="e9536-280">El **tiempo propio** representa el tiempo que pasa directamente en esa actividad.</span><span class="sxs-lookup"><span data-stu-id="e9536-280">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="e9536-281">**Tiempo total** representa el tiempo invertido en esa actividad o en cualquiera de los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e9536-281">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="e9536-282">Haga clic en **tiempo propio**, en **tiempo total**o en **actividad** para ordenar la tabla por esa columna.</span><span class="sxs-lookup"><span data-stu-id="e9536-282">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="e9536-283">Use el cuadro de texto **filtrar** para filtrar eventos por nombre de actividad.</span><span class="sxs-lookup"><span data-stu-id="e9536-283">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="e9536-284">De forma predeterminada, el menú **agrupar** se establece en **sin agrupar**.</span><span class="sxs-lookup"><span data-stu-id="e9536-284">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="e9536-285">Use el menú **agrupar** para ordenar la tabla actividad según varios criterios.</span><span class="sxs-lookup"><span data-stu-id="e9536-285">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="e9536-286">Haga clic en **Mostrar pila más pesado** ![ Mostrar pila más pesada ][ImageShowHeaviestStackIcon] para revelar otra tabla a la derecha de la tabla **actividad** .</span><span class="sxs-lookup"><span data-stu-id="e9536-286">Click **Show Heaviest Stack** ![Show Heaviest Stack][ImageShowHeaviestStackIcon] to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="e9536-287">Haga clic en una actividad para rellenar la tabla de **pila más intensa** .</span><span class="sxs-lookup"><span data-stu-id="e9536-287">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="e9536-288">La tabla **pila más pesada** muestra qué elementos secundarios de la actividad seleccionada tardaron más tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e9536-288">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="e9536-289">La pestaña abajo</span><span class="sxs-lookup"><span data-stu-id="e9536-289">The Bottom-Up tab</span></span>   

<span data-ttu-id="e9536-290">Use la pestaña **de abajo** para ver las actividades que se ocuparon directamente la mayor parte del tiempo en el agregado.</span><span class="sxs-lookup"><span data-stu-id="e9536-290">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="e9536-291">La pestaña de la **parte inferior** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-291">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="e9536-292">Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="e9536-292">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="e9536-293">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="e9536-293">Figure 18</span></span>  
> <span data-ttu-id="e9536-294">La pestaña **abajo**</span><span class="sxs-lookup"><span data-stu-id="e9536-294">The **Bottom-Up** tab</span></span>  
> ![La pestaña abajo][ImageBottomUp]  

<span data-ttu-id="e9536-296">En el gráfico de llama de la sección **principal** de la [figura 18](#figure-18), vea que casi prácticamente todo el tiempo se dedicó a ejecutarse `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="e9536-296">In the **Main** section flame chart of [Figure 18](#figure-18), see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="e9536-297">La actividad principal en la pestaña de la **parte inferior** de la [figura 18](#figure-18) es `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="e9536-297">The top activity in the **Bottom-Up** tab of [Figure 18](#figure-18) is `Parse HTML`.</span></span>  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="e9536-298">Consulte en la pestaña de la **parte inferior** , la actividad más costosa es `Layout` .</span><span class="sxs-lookup"><span data-stu-id="e9536-298">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="e9536-299">La columna **Self Time** representa el tiempo agregado directamente en esa actividad, en todas las apariciones.</span><span class="sxs-lookup"><span data-stu-id="e9536-299">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="e9536-300">La columna **tiempo total** representa el tiempo agregado invertido en esa actividad o en cualquiera de los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e9536-300">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="e9536-301">La ficha registro de eventos</span><span class="sxs-lookup"><span data-stu-id="e9536-301">The Event Log tab</span></span>   

<span data-ttu-id="e9536-302">Use la pestaña **registro de eventos** para ver las actividades en el orden en el que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-302">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="e9536-303">La pestaña **registro de eventos** solo muestra actividades durante la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-303">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="e9536-304">Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="e9536-304">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="e9536-305">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="e9536-305">Figure 19</span></span>  
> <span data-ttu-id="e9536-306">La ficha **registro de eventos**</span><span class="sxs-lookup"><span data-stu-id="e9536-306">The **Event Log** tab</span></span>  
> ![La ficha registro de eventos][ImageEventLog]  

<span data-ttu-id="e9536-308">La columna **hora de inicio** representa el punto en el que se inició la actividad, en relación con el inicio de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-308">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="e9536-309">Por ejemplo, la hora de inicio del `175.7 ms` elemento seleccionado en la [figura 19](#figure-19) significa que la actividad comenzó el 175,7 ms después de que se iniciara la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-309">For example, the start time of `175.7 ms` for the selected item in [Figure 19](#figure-19) means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="e9536-310">La columna **Self Time** representa el tiempo invertido directamente en esa actividad.</span><span class="sxs-lookup"><span data-stu-id="e9536-310">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="e9536-311">La columna **tiempo total** representa el tiempo invertido directamente en esa actividad o en cualquiera de los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e9536-311">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="e9536-312">Haga clic en **hora de inicio**, tiempo **propio**o **tiempo total** para ordenar la tabla por esa columna.</span><span class="sxs-lookup"><span data-stu-id="e9536-312">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="e9536-313">Use el cuadro de texto **filtrar** para filtrar las actividades por nombre.</span><span class="sxs-lookup"><span data-stu-id="e9536-313">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="e9536-314">Use el menú **duración** para filtrar todas las actividades que hayan tardado menos de 1 ms o de 15 ms.</span><span class="sxs-lookup"><span data-stu-id="e9536-314">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="e9536-315">De forma predeterminada, el menú **duración** se establece en **todos**, lo que significa que se muestran todas las actividades.</span><span class="sxs-lookup"><span data-stu-id="e9536-315">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="e9536-316">Deshabilite las casillas de verificación **cargar**, **scripting**, **procesamiento**o **pintura** para filtrar todas las actividades de esas categorías.</span><span class="sxs-lookup"><span data-stu-id="e9536-316">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="e9536-317">Ver actividad de la GPU</span><span class="sxs-lookup"><span data-stu-id="e9536-317">View GPU activity</span></span>   

<span data-ttu-id="e9536-318">Ver la actividad de la GPU en la sección **GPU** .</span><span class="sxs-lookup"><span data-stu-id="e9536-318">View GPU activity in the **GPU** section.</span></span>  

> ##### <span data-ttu-id="e9536-319">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="e9536-319">Figure 20</span></span>  
> <span data-ttu-id="e9536-320">La sección **GPU**</span><span class="sxs-lookup"><span data-stu-id="e9536-320">The **GPU** section</span></span>  
> ![La sección GPU][ImageGpu]  

### <span data-ttu-id="e9536-322">Ver actividad rasterizada</span><span class="sxs-lookup"><span data-stu-id="e9536-322">View raster activity</span></span>   

<span data-ttu-id="e9536-323">Ver la actividad rasterizada en la sección de **trama** .</span><span class="sxs-lookup"><span data-stu-id="e9536-323">View raster activity in the **Raster** section.</span></span>  

> ##### <span data-ttu-id="e9536-324">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="e9536-324">Figure 21</span></span>  
> <span data-ttu-id="e9536-325">La sección **trama**</span><span class="sxs-lookup"><span data-stu-id="e9536-325">The **Raster** section</span></span>  
> ![La sección trama][ImageRaster]  

### <span data-ttu-id="e9536-327">Ver interacciones</span><span class="sxs-lookup"><span data-stu-id="e9536-327">View interactions</span></span>   

<span data-ttu-id="e9536-328">Use la sección **interacciones** para buscar y analizar las interacciones del usuario que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-328">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

> ##### <span data-ttu-id="e9536-329">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="e9536-329">Figure 22</span></span>  
> <span data-ttu-id="e9536-330">La sección **interacciones**</span><span class="sxs-lookup"><span data-stu-id="e9536-330">The **Interactions** section</span></span>  
> ![La sección interacciones][ImageInteractions]  

<span data-ttu-id="e9536-332">Una línea roja en la parte inferior de una interacción representa el tiempo dedicado a esperar el subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="e9536-332">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="e9536-333">Haga clic en una interacción para ver más información sobre ella en la pestaña **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="e9536-333">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="e9536-334">Analizar fotogramas por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="e9536-334">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="e9536-335">DevTools proporciona numerosas formas de analizar fotogramas por segundo:</span><span class="sxs-lookup"><span data-stu-id="e9536-335">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="e9536-336">Use [el gráfico de **fps** ](#the-fps-chart) para obtener una visión general de los FPS durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-336">Use [the **FPS** chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="e9536-337">Use [la sección **Marcos** ](#the-frames-section) para ver cuánto tarda un marco en particular.</span><span class="sxs-lookup"><span data-stu-id="e9536-337">Use [the **Frames** section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="e9536-338">Use el **medidor de fps** para una estimación en tiempo real de fps a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-338">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="e9536-339">Consulte [Ver fotogramas por segundo en tiempo real con el medidor de fps](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="e9536-339">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  

#### <span data-ttu-id="e9536-340">El gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="e9536-340">The FPS chart</span></span>   

<span data-ttu-id="e9536-341">El gráfico **fps** proporciona una descripción general de la velocidad de fotogramas en toda la duración de una grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-341">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="e9536-342">En general, cuanto más alto sea la barra verde, mejor será la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e9536-342">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="e9536-343">Una barra roja encima del gráfico de **fps** es una advertencia de que la velocidad de fotogramas ha disminuido tan poco que probablemente se ha dañado la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="e9536-343">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

> ##### <span data-ttu-id="e9536-344">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="e9536-344">Figure 23</span></span>  
> <span data-ttu-id="e9536-345">El gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="e9536-345">The FPS chart</span></span>  
> ![El gráfico de FPS][ImageFpsChart]  

#### <span data-ttu-id="e9536-347">La sección marcos</span><span class="sxs-lookup"><span data-stu-id="e9536-347">The Frames section</span></span>   

<span data-ttu-id="e9536-348">La sección **Marcos** le indica exactamente cuánto tarda un marco en particular.</span><span class="sxs-lookup"><span data-stu-id="e9536-348">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="e9536-349">Mantenga el mouse sobre un marco para ver una información sobre herramientas con más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="e9536-349">Hover over a frame to view a tooltip with more information about it.</span></span>  

> ##### <span data-ttu-id="e9536-350">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="e9536-350">Figure 24</span></span>  
> <span data-ttu-id="e9536-351">Mantener el puntero sobre un marco</span><span class="sxs-lookup"><span data-stu-id="e9536-351">Hovering over a frame</span></span>  
> ![Mantener el puntero sobre un marco][ImageFramesSection]  

<span data-ttu-id="e9536-353">Haga clic en un marco para ver más información sobre el marco en la pestaña **Resumen** .  DevTools esquematiza el fotograma seleccionado en azul.</span><span class="sxs-lookup"><span data-stu-id="e9536-353">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

> ##### <span data-ttu-id="e9536-354">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="e9536-354">Figure 25</span></span>  
> <span data-ttu-id="e9536-355">Visualización de un marco en la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="e9536-355">Viewing a frame in the **Summary** tab</span></span>  
> ![Visualización de un marco en la pestaña Resumen][ImageFrameSummary]  

### <span data-ttu-id="e9536-357">Ver solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="e9536-357">View network requests</span></span>   

<span data-ttu-id="e9536-358">Expanda la sección **red** para ver una cascada de solicitudes de red que se produjeron durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-358">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

> ##### <span data-ttu-id="e9536-359">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="e9536-359">Figure 26</span></span>  
> <span data-ttu-id="e9536-360">La sección **red**</span><span class="sxs-lookup"><span data-stu-id="e9536-360">The **Network** section</span></span>  
> ![La sección red][ImageNetworkRequest]  

<span data-ttu-id="e9536-362">Las solicitudes se codifican en colores de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e9536-362">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="e9536-363">HTML: azul</span><span class="sxs-lookup"><span data-stu-id="e9536-363">HTML: Blue</span></span>  
*   <span data-ttu-id="e9536-364">CSS: morado</span><span class="sxs-lookup"><span data-stu-id="e9536-364">CSS: Purple</span></span>  
*   <span data-ttu-id="e9536-365">JS: amarillo</span><span class="sxs-lookup"><span data-stu-id="e9536-365">JS: Yellow</span></span>  
*   <span data-ttu-id="e9536-366">Imágenes: verde</span><span class="sxs-lookup"><span data-stu-id="e9536-366">Images: Green</span></span>  

<span data-ttu-id="e9536-367">Haga clic en una solicitud para ver más información sobre ella en la pestaña **Resumen** .  Por ejemplo, en la [figura 26](#figure-26) , la pestaña **Resumen** muestra más información sobre la solicitud azul seleccionada en la sección **red** .</span><span class="sxs-lookup"><span data-stu-id="e9536-367">Click on a request to view more information about it in the **Summary** tab.  For example, in [Figure 26](#figure-26) the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="e9536-368">Un cuadrado de color azul más oscuro en la parte superior izquierda de una solicitud significa que es una solicitud de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="e9536-368">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="e9536-369">Un cuadrado más claro significa menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="e9536-369">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="e9536-370">Por ejemplo, en la [figura 26](#figure-26) , el azul, la solicitud seleccionada es de mayor prioridad y el verde que está debajo es de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="e9536-370">For example, in [Figure 26](#figure-26) the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="e9536-371">En la [ilustración 27](#figure-27), la solicitud de `www.bing.com` se representa mediante una línea en la parte izquierda, una barra en el centro con una parte oscura y una parte clara, y una línea a la derecha.</span><span class="sxs-lookup"><span data-stu-id="e9536-371">In [Figure 27](#figure-27), the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="e9536-372">En la [Ilustración 28](#figure-28) se muestra la representación correspondiente de la misma solicitud en la pestaña **intervalos** del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="e9536-372">[Figure 28](#figure-28) shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="e9536-373">A continuación se muestra cómo se asignan entre sí estas dos representaciones:</span><span class="sxs-lookup"><span data-stu-id="e9536-373">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="e9536-374">La línea izquierda es todo hasta el `Connection Start` grupo de eventos, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="e9536-374">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="e9536-375">En otras palabras, es todo lo antes `Request Sent` y exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e9536-375">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="e9536-376">La parte clara de la barra es `Request Sent` y `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="e9536-376">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="e9536-377">La parte oscura de la barra es `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="e9536-377">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="e9536-378">Esencialmente, la línea adecuada es el tiempo dedicado a esperar el hilo principal.</span><span class="sxs-lookup"><span data-stu-id="e9536-378">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="e9536-379">Esto no se representa en la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="e9536-379">This is not represented in the **Timing** tab.</span></span>  

> ##### <span data-ttu-id="e9536-380">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="e9536-380">Figure 27</span></span>  
> <span data-ttu-id="e9536-381">Representación de barra de línea de la `www.bing.com` solicitud</span><span class="sxs-lookup"><span data-stu-id="e9536-381">The line-bar representation of the `www.bing.com` request</span></span>  
> ![La representación de barra de línea de la solicitud www.bing.com][ImageLineBar]  

> ##### <span data-ttu-id="e9536-383">Ilustración 28</span><span class="sxs-lookup"><span data-stu-id="e9536-383">Figure 28</span></span>  
> <span data-ttu-id="e9536-384">Representación de la ficha **intervalos** de la `www.bing.com` solicitud</span><span class="sxs-lookup"><span data-stu-id="e9536-384">The **Timing** tab representation of the `www.bing.com` request</span></span>  
> ![La sección red][ImageTiming]  

### <span data-ttu-id="e9536-386">Ver métricas de memoria</span><span class="sxs-lookup"><span data-stu-id="e9536-386">View memory metrics</span></span>   

<span data-ttu-id="e9536-387">Active la casilla **memoria** para ver las métricas de memoria de la última grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-387">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

> ##### <span data-ttu-id="e9536-388">Ilustración 29</span><span class="sxs-lookup"><span data-stu-id="e9536-388">Figure 29</span></span>  
> <span data-ttu-id="e9536-389">La casilla **memoria**</span><span class="sxs-lookup"><span data-stu-id="e9536-389">The **Memory** checkbox</span></span>  
> ![La casilla memoria][ImageMemory]  

<span data-ttu-id="e9536-391">DevTools muestra un nuevo gráfico de **memoria** , encima de la pestaña **Resumen** .  También hay un nuevo gráfico debajo del gráfico **net** , denominado **montón**.</span><span class="sxs-lookup"><span data-stu-id="e9536-391">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="e9536-392">El gráfico de **montones** proporciona la misma información que la línea de **montón JS** en el gráfico de **memoria** .</span><span class="sxs-lookup"><span data-stu-id="e9536-392">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

> ##### <span data-ttu-id="e9536-393">Ilustración 30</span><span class="sxs-lookup"><span data-stu-id="e9536-393">Figure 30</span></span>  
> <span data-ttu-id="e9536-394">Métrica de memoria, encima de la pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="e9536-394">Memory metrics, above the **Summary** tab</span></span>  
> ![Métricas de memoria][ImageMemoryMetrics]  

<span data-ttu-id="e9536-396">Las líneas de color del gráfico se asignan a las casillas coloreadas encima del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e9536-396">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="e9536-397">Desactive una casilla para ocultar la categoría en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="e9536-397">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="e9536-398">El gráfico solo muestra la región de la grabación que está seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="e9536-398">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="e9536-399">Por ejemplo, en la [figura 30](#figure-30), el gráfico de **memoria** solo muestra el uso de memoria de aproximadamente la marca de MS 400 a la marca de 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="e9536-399">For example, in [Figure 30](#figure-30), the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="e9536-400">Ver la duración de una parte de una grabación</span><span class="sxs-lookup"><span data-stu-id="e9536-400">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="e9536-401">Al analizar una sección como la **red** o **Main**, a veces necesitarás una estimación más precisa de cuánto tiempo han tardado determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="e9536-401">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="e9536-402">Espera `Shift` , haga clic y mantenga presionado y arrastre hacia la izquierda o la derecha para seleccionar una parte de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-402">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="e9536-403">En la parte inferior de la selección, DevTools muestra cuánto tiempo duró esa parte.</span><span class="sxs-lookup"><span data-stu-id="e9536-403">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

> ##### <span data-ttu-id="e9536-404">Ilustración 31</span><span class="sxs-lookup"><span data-stu-id="e9536-404">Figure 31</span></span>  
> <span data-ttu-id="e9536-405">La `9.47ms` marca de tiempo de la parte inferior de la parte seleccionada indica cuánto tiempo duró esa parte</span><span class="sxs-lookup"><span data-stu-id="e9536-405">The `9.47ms` timestamp at the bottom of the selected portion indicates how long that portion took</span></span>  
> ![Visualización de la duración de una parte de una grabación][ImageDuration]  

### <span data-ttu-id="e9536-407">Ver una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="e9536-407">View a screenshot</span></span>   

<span data-ttu-id="e9536-408">Consulte [capturar capturas de pantallas mientras graba](#capture-screenshots-while-recording) para obtener información sobre cómo habilitar capturas de pantallas.</span><span class="sxs-lookup"><span data-stu-id="e9536-408">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="e9536-409">Pase el puntero por la **información general** para ver una captura de pantalla de cómo se vio la página durante ese momento de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e9536-409">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="e9536-410">La **información general** es la sección que contiene los gráficos de **CPU**, **fps**y **net** .</span><span class="sxs-lookup"><span data-stu-id="e9536-410">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="e9536-411">Ilustración 32</span><span class="sxs-lookup"><span data-stu-id="e9536-411">Figure 32</span></span>  
> <span data-ttu-id="e9536-412">Ver una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="e9536-412">Viewing a screenshot</span></span>  
> ![Ver una captura de pantalla][ImageViewScreenshot]  

<span data-ttu-id="e9536-414">También puede ver capturas de pantallas haciendo clic en un marco de la sección **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="e9536-414">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="e9536-415">DevTools muestra una versión reducida de la captura de pantalla en la pestaña **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="e9536-415">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

> ##### <span data-ttu-id="e9536-416">Ilustración 33</span><span class="sxs-lookup"><span data-stu-id="e9536-416">Figure 33</span></span>  
> <span data-ttu-id="e9536-417">Después de hacer clic `233.9ms` en el marco de la sección de **Marcos** , se muestra la captura de pantalla de ese marco en la pestaña **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="e9536-417">After clicking the `233.9ms` frame in the **Frames** section, the screenshot for that frame is displayed in the **Summary** tab</span></span>  
> ![Ver una captura de pantalla en la pestaña Resumen][ImageFrameScreenshotSummary]  

<span data-ttu-id="e9536-419">Para acercar la captura de pantalla, haga clic en la miniatura de la pestaña **Resumen** .</span><span class="sxs-lookup"><span data-stu-id="e9536-419">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

> ##### <span data-ttu-id="e9536-420">Ilustración 34</span><span class="sxs-lookup"><span data-stu-id="e9536-420">Figure 34</span></span>  
> <span data-ttu-id="e9536-421">Después de hacer clic en la miniatura en la pestaña **Resumen** , DevTools acerca la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9536-421">After clicking the thumbnail in the **Summary** tab, DevTools zooms in on the screenshot</span></span>  
> ![Acercar una captura de pantalla de la pestaña Resumen][ImageFrameScreenshotZoom]  

### <span data-ttu-id="e9536-423">Ver información de capas</span><span class="sxs-lookup"><span data-stu-id="e9536-423">View layers information</span></span>   

<span data-ttu-id="e9536-424">Para ver la información sobre las capas avanzadas de un marco:</span><span class="sxs-lookup"><span data-stu-id="e9536-424">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="e9536-425">[Habilitar la instrumentación avanzada de pintura](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="e9536-425">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="e9536-426">Seleccione un marco de la sección **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="e9536-426">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="e9536-427">DevTools muestra información sobre las capas en la ficha nuevas **capas** , junto a la ficha **registro de eventos** .</span><span class="sxs-lookup"><span data-stu-id="e9536-427">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    > ##### <span data-ttu-id="e9536-428">Ilustración 35</span><span class="sxs-lookup"><span data-stu-id="e9536-428">Figure 35</span></span>  
    > <span data-ttu-id="e9536-429">El panel **capas**</span><span class="sxs-lookup"><span data-stu-id="e9536-429">The **Layers** pane</span></span>  
    > ![El panel capas][ImageLayers]  
    
<span data-ttu-id="e9536-431">Desplace el puntero sobre una capa para resaltarla en el diagrama.</span><span class="sxs-lookup"><span data-stu-id="e9536-431">Hover over a layer to highlight it in the diagram.</span></span>  

> ##### <span data-ttu-id="e9536-432">Ilustración 36</span><span class="sxs-lookup"><span data-stu-id="e9536-432">Figure 36</span></span>  
> <span data-ttu-id="e9536-433">Resaltar **#39** de capa</span><span class="sxs-lookup"><span data-stu-id="e9536-433">Highlighting layer **#39**</span></span>  
> ![Resaltar una capa][ImageLayerHover]  

<span data-ttu-id="e9536-435">Para mover el diagrama:</span><span class="sxs-lookup"><span data-stu-id="e9536-435">To move the diagram:</span></span>  

*   <span data-ttu-id="e9536-436">Haga clic en modo **panorámico** ![ panorámico ][ImagePanModeIcon] para desplazarse por los ejes X e y.</span><span class="sxs-lookup"><span data-stu-id="e9536-436">Click **Pan Mode** ![Pan Mode][ImagePanModeIcon] to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="e9536-437">Haga clic en modo **rotar** ![ modo ][ImageRotateModeIcon] de giro para rotar a lo largo del eje Z.</span><span class="sxs-lookup"><span data-stu-id="e9536-437">Click **Rotate Mode** ![Rotate Mode][ImageRotateModeIcon] to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="e9536-438">Haga clic en **restablecer** transformación de restablecimiento de transformaciones ![ ][ImageResetTransformIcon] para restablecer el diagrama a la posición original.</span><span class="sxs-lookup"><span data-stu-id="e9536-438">Click **Reset Transform** ![Reset Transform][ImageResetTransformIcon] to reset the diagram to the original position.</span></span>  

### <span data-ttu-id="e9536-439">Ver generador de perfiles de pintura</span><span class="sxs-lookup"><span data-stu-id="e9536-439">View paint profiler</span></span>   

<span data-ttu-id="e9536-440">Para ver información avanzada sobre un evento de pintura:</span><span class="sxs-lookup"><span data-stu-id="e9536-440">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="e9536-441">[Habilitar la instrumentación avanzada de pintura](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="e9536-441">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="e9536-442">Seleccione un evento de **pintura** en la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="e9536-442">Select a **Paint** event in the **Main** section.</span></span>  
    
    > ##### <span data-ttu-id="e9536-443">Ilustración 37</span><span class="sxs-lookup"><span data-stu-id="e9536-443">Figure 37</span></span>  
    > <span data-ttu-id="e9536-444">Pestaña **generador de perfiles de pintura**</span><span class="sxs-lookup"><span data-stu-id="e9536-444">The **Paint Profiler** tab</span></span>  
    > ![Pestaña generador de perfiles de pintura][ImagePaintProfiler]  
    
## <span data-ttu-id="e9536-446">Analizar el rendimiento de la representación con la pestaña representación</span><span class="sxs-lookup"><span data-stu-id="e9536-446">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="e9536-447">Use las características de la pestaña **representación** para poder visualizar el rendimiento de la representación de la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-447">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="e9536-448">Para abrir la pestaña **representación** :</span><span class="sxs-lookup"><span data-stu-id="e9536-448">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="e9536-449">[Abrir el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="e9536-449">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="e9536-450">Empiece `Rendering` a escribir y seleccione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="e9536-450">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="e9536-451">DevTools muestra la ficha **representación** en la parte inferior de la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9536-451">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    > ##### <span data-ttu-id="e9536-452">Ilustración 38</span><span class="sxs-lookup"><span data-stu-id="e9536-452">Figure 38</span></span>  
    > <span data-ttu-id="e9536-453">La pestaña **representación**</span><span class="sxs-lookup"><span data-stu-id="e9536-453">The **Rendering** tab</span></span>  
    > ![La pestaña representación][ImageRenderingTab]  
    
### <span data-ttu-id="e9536-455">Ver fotogramas por segundo en tiempo real con el medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="e9536-455">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="e9536-456">El **medidor de fps** es una superposición que aparece en la esquina superior derecha de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="e9536-456">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="e9536-457">Proporciona una estimación en tiempo real de FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-457">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="e9536-458">Para abrir el **medidor de fps**:</span><span class="sxs-lookup"><span data-stu-id="e9536-458">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="e9536-459">Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-459">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="e9536-460">Active la casilla de verificación de **medidor de fps** .</span><span class="sxs-lookup"><span data-stu-id="e9536-460">Enable the **FPS Meter** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="e9536-461">Ilustración 39</span><span class="sxs-lookup"><span data-stu-id="e9536-461">Figure 39</span></span>  
    > <span data-ttu-id="e9536-462">El medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="e9536-462">The FPS meter</span></span>  
    > ![El medidor de FPS][ImageFpsMeter]  
    
### <span data-ttu-id="e9536-464">Ver los eventos de pintura en tiempo real con parpadeo de pintura</span><span class="sxs-lookup"><span data-stu-id="e9536-464">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="e9536-465">Use las intermitencias de pintura para obtener una vista en tiempo real de todos los eventos de pintura en la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-465">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="e9536-466">Cada vez que se vuelve a pintar una parte de la página, DevTools esquematiza esa sección en verde.</span><span class="sxs-lookup"><span data-stu-id="e9536-466">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="e9536-467">Para habilitar los parpadeos de pintura:</span><span class="sxs-lookup"><span data-stu-id="e9536-467">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="e9536-468">Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-468">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="e9536-469">Active la casilla de **pintura parpadeante** .</span><span class="sxs-lookup"><span data-stu-id="e9536-469">Enable the **Paint Flashing** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="e9536-470">Ilustración 40</span><span class="sxs-lookup"><span data-stu-id="e9536-470">Figure 40</span></span>  
    > **<span data-ttu-id="e9536-471">Pintura parpadeante</span><span class="sxs-lookup"><span data-stu-id="e9536-471">Paint Flashing</span></span>**  
    > ![Pintura parpadeante][ImagePaintFlashing]  
    
### <span data-ttu-id="e9536-473">Ver una superposición de capas con bordes de capas</span><span class="sxs-lookup"><span data-stu-id="e9536-473">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="e9536-474">Use **bordes de capas** para ver una superposición de los bordes de la capa y los mosaicos en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-474">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="e9536-475">Para habilitar los bordes de capas:</span><span class="sxs-lookup"><span data-stu-id="e9536-475">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="e9536-476">Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-476">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="e9536-477">Active la casilla **bordes de capas** .</span><span class="sxs-lookup"><span data-stu-id="e9536-477">Enable the **Layer Borders** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="e9536-478">Ilustración 41</span><span class="sxs-lookup"><span data-stu-id="e9536-478">Figure 41</span></span>  
    > **<span data-ttu-id="e9536-479">Bordes de capas</span><span class="sxs-lookup"><span data-stu-id="e9536-479">Layer Borders</span></span>**  
    > ![Bordes de capas][ImageLayerBorders]  
    
<span data-ttu-id="e9536-481">Vea los comentarios en [`debug_colors.cc`][ChromiumDebugColors] para obtener una explicación de los códigos de color.</span><span class="sxs-lookup"><span data-stu-id="e9536-481">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="e9536-482">Buscar problemas de rendimiento de desplazamiento en tiempo real</span><span class="sxs-lookup"><span data-stu-id="e9536-482">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="e9536-483">Use los problemas de rendimiento de desplazamiento para identificar los elementos de la página que tienen detectores de eventos relacionados con el desplazamiento que pueden dañar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="e9536-483">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="e9536-484">DevTools subraya los elementos potencialmente problemáticos de verde azulado.</span><span class="sxs-lookup"><span data-stu-id="e9536-484">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="e9536-485">Para ver los problemas de rendimiento del desplazamiento:</span><span class="sxs-lookup"><span data-stu-id="e9536-485">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="e9536-486">Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="e9536-486">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="e9536-487">Active la casilla de verificación de **problemas de rendimiento de desplazamiento** .</span><span class="sxs-lookup"><span data-stu-id="e9536-487">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
 
    > ##### <span data-ttu-id="e9536-488">Ilustración 42</span><span class="sxs-lookup"><span data-stu-id="e9536-488">Figure 42</span></span>  
    > <span data-ttu-id="e9536-489">Los **problemas de rendimiento de desplazamiento** indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento</span><span class="sxs-lookup"><span data-stu-id="e9536-489">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    > ![Los problemas de rendimiento de desplazamiento indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Ilustración 1: registro"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Ilustración 2: actualizar página"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Ilustración 3: una grabación de carga de página"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Figura 4: la casilla de verificación capturas de pantallas"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Ilustración 5: recopilar los elementos no usados"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Ilustración 6: la sección de configuración de captura"  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Ilustración 7: un ejemplo de una grabación cuando se deshabilitan los ejemplos de JS"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Ilustración 8: un ejemplo de una grabación cuando se habilitan los ejemplos de JS"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Ilustración 9: guardar perfil"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Ilustración 10: cargar perfil"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Ilustración 11: borrar grabación"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Ilustración 12: arrastrar el mouse por la información general para zoom"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Ilustración 13: el cuadro de búsqueda"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Ilustración 14: la sección principal"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Ilustración 15: más información sobre la función anónima en la pestaña Resumen"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Ilustración 16: un gráfico de llama"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Ilustración 17: la ficha árbol de llamadas"  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Ilustración 18: la pestaña de abajo arriba"  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Ilustración 19: ficha registro de eventos"  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Ilustración 20: la sección GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Ilustración 21: la sección de trama"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Ilustración 22: la sección Interactions"  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Ilustración 23: el gráfico de FPS"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Ilustración 24: mantener el puntero sobre un marco"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Ilustración 25: visualización de un marco en la pestaña Resumen"  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Ilustración 26: la sección red"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Ilustración 27: representación de barra de línea de la solicitud www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Ilustración 28: la sección red"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Ilustración 29: la casilla memoria"  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Ilustración 30: métrica de memoria"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Ilustración 31: visualización de la duración de una parte de una grabación"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Ilustración 32: ver una captura de pantalla"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Ilustración 33: ver una captura de pantalla en la pestaña Resumen"  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Ilustración 34: zoom en una captura de pantalla de la pestaña Resumen"  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Ilustración 35: el panel capas"  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Ilustración 36: resaltado de una capa"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Ilustración 37: la pestaña generador de perfiles de Paint"  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Ilustración 38: la pestaña representación"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Ilustración 39: el medidor de FPS"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Ilustración 40: parpadeo de la pintura"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Ilustración 41: bordes de capas"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Ilustración 42: los problemas de rendimiento de desplazamiento indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Abrir el menú de comandos: ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Empezar a analizar el rendimiento en tiempo de ejecución"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demostración de pestañas de actividades"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc: búsqueda de código"  

> [!NOTE]
> <span data-ttu-id="e9536-538">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e9536-538">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e9536-539">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e9536-539">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e9536-541">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e9536-541">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
