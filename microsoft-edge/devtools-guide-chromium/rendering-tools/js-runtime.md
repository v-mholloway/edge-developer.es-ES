---
title: Acelerar el tiempo de ejecución de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0e198be3e1cef53590a24bfaa2382746ced299ed
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611874"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# <span data-ttu-id="60cdd-103">Acelerar el tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="60cdd-103">Speed Up JavaScript Runtime</span></span>   




<span data-ttu-id="60cdd-104">Identifica funciones caras usando el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="60cdd-104">Identify expensive functions using the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="60cdd-105">Figura 1</span><span class="sxs-lookup"><span data-stu-id="60cdd-105">Figure 1</span></span>  
> <span data-ttu-id="60cdd-106">Perfiles de muestreo</span><span class="sxs-lookup"><span data-stu-id="60cdd-106">Sampling Profiles</span></span>  
> ![Perfiles de muestreo][ImageCpuProfile]  

### <span data-ttu-id="60cdd-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="60cdd-108">Summary</span></span>  

*   <span data-ttu-id="60cdd-109">Registre exactamente las funciones a las que se llamó y la cantidad de memoria que requiere cada una con el muestreo de asignación en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="60cdd-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="60cdd-110">Visualice sus perfiles como un gráfico de llamas.</span><span class="sxs-lookup"><span data-stu-id="60cdd-110">Visualize your profiles as a flame chart.</span></span>  

## <span data-ttu-id="60cdd-111">Grabar un perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="60cdd-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="60cdd-112">Si observas Jank en tu JavaScript, recopila un perfil de muestreo.</span><span class="sxs-lookup"><span data-stu-id="60cdd-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="60cdd-113">Los perfiles de muestreo muestran dónde se gasta el tiempo de ejecución en las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="60cdd-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="60cdd-114">Vaya al panel **memoria** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="60cdd-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="60cdd-115">Seleccione el botón de opción **muestreo de asignación** .</span><span class="sxs-lookup"><span data-stu-id="60cdd-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="60cdd-116">Selecciona **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="60cdd-116">Select **Start**.</span></span>  
1.  <span data-ttu-id="60cdd-117">En función de lo que intente analizar, puede volver a cargar la página, interactuar con la página o simplemente permitir la ejecución de la página.</span><span class="sxs-lookup"><span data-stu-id="60cdd-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="60cdd-118">Haga clic en el botón **detener** cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="60cdd-118">Select the **Stop** button when you are finished.</span></span>  

> [!NOTE]
> <span data-ttu-id="60cdd-119">También puede usar la [API utilidades de consola][DevtoolsConsoleUtilities] para grabar y agrupar perfiles desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="60cdd-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="60cdd-120">Ver perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="60cdd-120">View Sampling Profile</span></span>  

<span data-ttu-id="60cdd-121">Cuando termine de grabar, DevTools rellenará automáticamente el panel **memoria** en **perfiles de muestreo** con los datos de su grabación.</span><span class="sxs-lookup"><span data-stu-id="60cdd-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="60cdd-122">La vista predeterminada es **gruesa \ (inferior arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="60cdd-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="60cdd-123">Esta vista le permite ver qué funciones tuvieron el mayor impacto en el rendimiento y examinar las rutas de llamadas a esas funciones.</span><span class="sxs-lookup"><span data-stu-id="60cdd-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="60cdd-124">Cambiar el criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="60cdd-124">Change sort order</span></span>   

<span data-ttu-id="60cdd-125">Para cambiar el orden de clasificación, seleccione el menú desplegable que se encuentra junto al icono de la función seleccionada para el foco de la **función** seleccionada ![ ][ImageFocusIcon] y, a continuación, elija una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="60cdd-125">To change the sorting order, select the dropdown menu next to the **focus selected function** ![focus selected function][ImageFocusIcon] icon and then choose one of the following options.</span></span>

<span data-ttu-id="60cdd-126">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="60cdd-126">**Chart**.</span></span>  <span data-ttu-id="60cdd-127">Muestra un gráfico cronológico de grabación.</span><span class="sxs-lookup"><span data-stu-id="60cdd-127">Displays a chronological chart of the recording.</span></span>  

> ##### <span data-ttu-id="60cdd-128">Figura 2</span><span class="sxs-lookup"><span data-stu-id="60cdd-128">Figure 2</span></span>  
> <span data-ttu-id="60cdd-129">Gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="60cdd-129">Flame chart</span></span>  
> ![Gráfico de llamas][ImageFlameChart]  

<span data-ttu-id="60cdd-131">**\ (Inferior arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="60cdd-131">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="60cdd-132">Enumera las funciones por su impacto en el rendimiento y permite examinar las rutas de la llamada a las funciones.</span><span class="sxs-lookup"><span data-stu-id="60cdd-132">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="60cdd-133">Esta es la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="60cdd-133">This is the default view.</span></span>  

> ##### <span data-ttu-id="60cdd-134">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="60cdd-134">Figure 3</span></span>  
> <span data-ttu-id="60cdd-135">Gráfico grueso</span><span class="sxs-lookup"><span data-stu-id="60cdd-135">Heavy chart</span></span>  
> ![Gráfico grueso][ImageHeavyChart]  

<span data-ttu-id="60cdd-137">**Tree \ (arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="60cdd-137">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="60cdd-138">Se muestra una imagen general de la estructura de llamadas, empezando en la parte superior de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="60cdd-138">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

> ##### <span data-ttu-id="60cdd-139">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="60cdd-139">Figure 4</span></span>  
> <span data-ttu-id="60cdd-140">Gráfico de árbol</span><span class="sxs-lookup"><span data-stu-id="60cdd-140">Tree chart</span></span>  
> ![Gráfico de árbol][ImageTreeChart]  

### <span data-ttu-id="60cdd-142">Excluir funciones</span><span class="sxs-lookup"><span data-stu-id="60cdd-142">Exclude functions</span></span>   

<span data-ttu-id="60cdd-143">Para excluir una función de su perfil de muestreo, selecciónela para seleccionarla y, a continuación, seleccione la **función** seleccionada ![ excluir la función seleccionada ][ImageExcludeIcon] .</span><span class="sxs-lookup"><span data-stu-id="60cdd-143">To exclude a function from your Sampling Profile, select it to select it and then select the **exclude selected function** ![exclude selected function][ImageExcludeIcon] icon.</span></span>  <span data-ttu-id="60cdd-144">La función de solicitud \ (primario \) de la función excluida \ (secundario \) se cobra con la memoria asignada a la función excluida \ (hijo \).</span><span class="sxs-lookup"><span data-stu-id="60cdd-144">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="60cdd-145">Seleccione el icono **restaurar** todas las funciones restaurar todas las funciones ![ ][ImageRestoreIcon] para volver a restaurar todas las funciones excluidas en la grabación.</span><span class="sxs-lookup"><span data-stu-id="60cdd-145">Select the **restore all functions** ![restore all functions][ImageRestoreIcon] icon to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="60cdd-146">Ver perfil de muestreo como gráfico</span><span class="sxs-lookup"><span data-stu-id="60cdd-146">View Sampling Profile as Chart</span></span>   

<span data-ttu-id="60cdd-147">La vista de gráfico proporciona una representación visual del perfil de muestreo a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="60cdd-147">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="60cdd-148">Después de [grabar un perfil de muestreo](#record-a-sampling-profile), visualice la grabación como un gráfico de llama [cambiando el criterio de ordenación](#change-sort-order) a **gráfico**.</span><span class="sxs-lookup"><span data-stu-id="60cdd-148">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

> ##### <span data-ttu-id="60cdd-149">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="60cdd-149">Figure 5</span></span>  
> <span data-ttu-id="60cdd-150">Vista de gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="60cdd-150">Flame chart view</span></span>  
> ![Vista de gráfico de llamas][ImageFlameChartView]  

<span data-ttu-id="60cdd-152">El gráfico de llamas se divide en dos partes.</span><span class="sxs-lookup"><span data-stu-id="60cdd-152">The flame chart is split into two parts.</span></span>  

| | <span data-ttu-id="60cdd-153">Elemento</span><span class="sxs-lookup"><span data-stu-id="60cdd-153">Part</span></span> | <span data-ttu-id="60cdd-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="60cdd-154">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="60cdd-155">uno</span><span class="sxs-lookup"><span data-stu-id="60cdd-155">1</span></span> | <span data-ttu-id="60cdd-156">Introducción</span><span class="sxs-lookup"><span data-stu-id="60cdd-156">Overview</span></span> | <span data-ttu-id="60cdd-157">Una vista de las aves de toda la grabación.</span><span class="sxs-lookup"><span data-stu-id="60cdd-157">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="60cdd-158">El alto de las barras corresponde a la profundidad de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="60cdd-158">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="60cdd-159">Por lo tanto, cuanto más alto es la barra, más profunda es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="60cdd-159">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="60cdd-160">1</span><span class="sxs-lookup"><span data-stu-id="60cdd-160">2</span></span> | <span data-ttu-id="60cdd-161">Pilas de llamadas</span><span class="sxs-lookup"><span data-stu-id="60cdd-161">Call Stacks</span></span> | <span data-ttu-id="60cdd-162">Esta es una vista en profundidad de las funciones a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="60cdd-162">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="60cdd-163">El eje horizontal es tiempo y eje vertical es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="60cdd-163">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="60cdd-164">Las pilas están organizadas de arriba a abajo.</span><span class="sxs-lookup"><span data-stu-id="60cdd-164">The stacks are organized top-down.</span></span>  <span data-ttu-id="60cdd-165">Por lo tanto, la función de la parte superior llamará a la que se encuentra debajo, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="60cdd-165">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="60cdd-166">Las funciones están coloreadas de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="60cdd-166">Functions are colored randomly.</span></span>  <span data-ttu-id="60cdd-167">No hay ninguna correlación de los colores que se usan en los otros paneles.</span><span class="sxs-lookup"><span data-stu-id="60cdd-167">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="60cdd-168">Sin embargo, las funciones siempre tienen el mismo color en todas las invocaciones, de modo que pueda ver los patrones en cada tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="60cdd-168">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

> ##### <span data-ttu-id="60cdd-169">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="60cdd-169">Figure 6</span></span>  
> <span data-ttu-id="60cdd-170">Gráfico de llamas con anotaciones</span><span class="sxs-lookup"><span data-stu-id="60cdd-170">Annotated flame chart</span></span>  
> ![Gráfico de llamas con anotaciones][ImageAnnotatedFlameChart]  

<span data-ttu-id="60cdd-172">Una pila de llamadas altas no es necesariamente importante, simplemente significa que se llamó a una gran cantidad de funciones.</span><span class="sxs-lookup"><span data-stu-id="60cdd-172">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="60cdd-173">Pero una barra amplia significa que una función tarda mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="60cdd-173">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="60cdd-174">Son candidatos para la optimización.</span><span class="sxs-lookup"><span data-stu-id="60cdd-174">These are candidates for optimization.</span></span>  

### <span data-ttu-id="60cdd-175">Acercar partes específicas de la grabación</span><span class="sxs-lookup"><span data-stu-id="60cdd-175">Zoom in on specific parts of recording</span></span>   

<span data-ttu-id="60cdd-176">Seleccione, mantenga y arrastre el ratón a la izquierda y a la derecha en la información general para acercar determinadas partes de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="60cdd-176">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="60cdd-177">Después de aplicar el zoom, la pila de llamadas muestra automáticamente la parte de la grabación que seleccionó.</span><span class="sxs-lookup"><span data-stu-id="60cdd-177">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

> ##### <span data-ttu-id="60cdd-178">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="60cdd-178">Figure 7</span></span>  
> <span data-ttu-id="60cdd-179">Gráfico ampliado</span><span class="sxs-lookup"><span data-stu-id="60cdd-179">Chart zoomed</span></span>  
> ![Gráfico ampliado][ImageFlameChartZoomed]  

### <span data-ttu-id="60cdd-181">Ver detalles de la función</span><span class="sxs-lookup"><span data-stu-id="60cdd-181">View function details</span></span>   

<span data-ttu-id="60cdd-182">Seleccione en una función para ver la definición en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="60cdd-182">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="60cdd-183">Pase el puntero sobre una función para mostrar el nombre y los datos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="60cdd-183">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="60cdd-184">Se proporciona la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="60cdd-184">The following information is provided.</span></span>  

| <span data-ttu-id="60cdd-185">Todo</span><span class="sxs-lookup"><span data-stu-id="60cdd-185">Detail</span></span> | <span data-ttu-id="60cdd-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="60cdd-186">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="60cdd-187">Name</span><span class="sxs-lookup"><span data-stu-id="60cdd-187">Name</span></span>** | <span data-ttu-id="60cdd-188">El nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="60cdd-188">The name of the function.</span></span>  |  
| **<span data-ttu-id="60cdd-189">Tamaño propio</span><span class="sxs-lookup"><span data-stu-id="60cdd-189">Self size</span></span>** | <span data-ttu-id="60cdd-190">Tamaño de la invocación actual de la función, incluidas solo las instrucciones de la función.</span><span class="sxs-lookup"><span data-stu-id="60cdd-190">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="60cdd-191">Tamaño total</span><span class="sxs-lookup"><span data-stu-id="60cdd-191">Total size</span></span>** | <span data-ttu-id="60cdd-192">Tamaño de la invocación actual de esta función y de las funciones a las que llamó.</span><span class="sxs-lookup"><span data-stu-id="60cdd-192">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="60cdd-193">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="60cdd-193">URL</span></span>** | <span data-ttu-id="60cdd-194">La ubicación de la definición de función en el formato de `base.js:261` donde `base.js` es el nombre del archivo en el que se define la función y `261` es el número de línea de la definición.</span><span class="sxs-lookup"><span data-stu-id="60cdd-194">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

> ##### <span data-ttu-id="60cdd-195">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="60cdd-195">Figure 8</span></span>  
> <span data-ttu-id="60cdd-196">Ver detalles de funciones en el gráfico</span><span class="sxs-lookup"><span data-stu-id="60cdd-196">Viewing functions details in chart</span></span>  
> ![Ver detalles de funciones en el gráfico][ImageFunctionsDetails]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageExcludeIcon]: /microsoft-edge/devtools-guide-chromium/media/exclude-icon.msft.png  
[ImageFocusIcon]: /microsoft-edge/devtools-guide-chromium/media/images/focus-icon.msft.png  
[ImageRestoreIcon]: /microsoft-edge/devtools-guide-chromium/media/images/restore-icon.msft.png  

[ImageCpuProfile]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Ilustración 1: perfiles de muestreo"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Ilustración 2: gráfico de llamas"  
[ImageHeavyChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Ilustración 3: gráfico grueso"  
[ImageTreeChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png "Ilustración 4: gráfico de árbol"  
[ImageFlameChartView]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Ilustración 5: vista de gráfico de llama"  
[ImageAnnotatedFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png "Ilustración 6: gráfico de llama anotado"  
[ImageFlameChartZoomed]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png "Ilustración 7: zoom de gráfico"  
[ImageFunctionsDetails]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png "Ilustración 8: ver detalles de las funciones en el gráfico"  

<!-- links -->  

[DevtoolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de API de utilidades de consola"  
[DevtoolsConsoleUtilitiesProfile]: /microsoft-edge/devtools-guide-chromium/console/utilities#profile "Perfil: referencia de API de utilidades de consola"  
[DevtoolsConsoleUtilitiesProfileEnd]: /microsoft-edge/devtools-guide-chromium/console/utilities#profileend "profileEnd: referencia de API de utilidades de consola"  

> [!NOTE]
> <span data-ttu-id="60cdd-209">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60cdd-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="60cdd-210">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="60cdd-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="60cdd-212">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60cdd-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
