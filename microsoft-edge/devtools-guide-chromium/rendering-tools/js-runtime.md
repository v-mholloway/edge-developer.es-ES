---
title: Acelerar el tiempo de ejecución de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2f05ef2911c855df39d60fa732ff5f784ab49473
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984895"
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





# <span data-ttu-id="ee3d4-103">Acelerar el tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ee3d4-103">Speed up JavaScript runtime</span></span>   




<span data-ttu-id="ee3d4-104">Identifica funciones caras usando el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="ee3d4-104">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfiles de muestreo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="ee3d4-106">Perfiles de muestreo</span><span class="sxs-lookup"><span data-stu-id="ee3d4-106">Sampling Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="ee3d4-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="ee3d4-107">Summary</span></span>  

*   <span data-ttu-id="ee3d4-108">Registre exactamente las funciones a las que se llamó y la cantidad de memoria que requiere cada una con el muestreo de asignación en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="ee3d4-108">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="ee3d4-109">Visualice sus perfiles como un gráfico de llamas.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-109">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="ee3d4-110">Grabar un perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="ee3d4-110">Record a Sampling Profile</span></span>  

<span data-ttu-id="ee3d4-111">Si observas Jank en tu JavaScript, recopila un perfil de muestreo.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-111">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="ee3d4-112">Los perfiles de muestreo muestran dónde se gasta el tiempo de ejecución en las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-112">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="ee3d4-113">Vaya al panel **memoria** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-113">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="ee3d4-114">Seleccione el botón de opción **muestreo de asignación** .</span><span class="sxs-lookup"><span data-stu-id="ee3d4-114">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="ee3d4-115">Selecciona **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-115">Select **Start**.</span></span>  
1.  <span data-ttu-id="ee3d4-116">En función de lo que intente analizar, puede volver a cargar la página, interactuar con la página o simplemente permitir la ejecución de la página.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-116">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="ee3d4-117">Haga clic en el botón **detener** cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-117">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="ee3d4-118">También puede usar la [API utilidades de consola][DevtoolsConsoleUtilities] para grabar y agrupar perfiles desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-118">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="ee3d4-119">Ver perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="ee3d4-119">View Sampling Profile</span></span>  

<span data-ttu-id="ee3d4-120">Cuando termine de grabar, DevTools rellenará automáticamente el panel **memoria** en **perfiles de muestreo** con los datos de su grabación.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-120">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="ee3d4-121">La vista predeterminada es **gruesa \ (inferior arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-121">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="ee3d4-122">Esta vista le permite ver qué funciones tuvieron el mayor impacto en el rendimiento y examinar las rutas de llamadas a esas funciones.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-122">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="ee3d4-123">Cambiar el criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="ee3d4-123">Change sort order</span></span>   

<span data-ttu-id="ee3d4-124">Para cambiar el orden de clasificación, seleccione el menú desplegable junto al icono **función seleccionada** \ ( ![ enfoque seleccionado de la función ][ImageFocusIcon] \) y, a continuación, elija una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-124">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="ee3d4-125">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-125">**Chart**.</span></span>  <span data-ttu-id="ee3d4-126">Muestra un gráfico cronológico de grabación.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-126">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="ee3d4-128">Gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="ee3d4-128">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="ee3d4-129">**\ (Inferior arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-129">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="ee3d4-130">Enumera las funciones por su impacto en el rendimiento y permite examinar las rutas de la llamada a las funciones.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-130">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="ee3d4-131">Esta es la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-131">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico grueso" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="ee3d4-133">Gráfico grueso</span><span class="sxs-lookup"><span data-stu-id="ee3d4-133">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="ee3d4-134">**Tree \ (arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-134">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="ee3d4-135">Se muestra una imagen general de la estructura de llamadas, empezando en la parte superior de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-135">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árbol" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="ee3d4-137">Gráfico de árbol</span><span class="sxs-lookup"><span data-stu-id="ee3d4-137">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="ee3d4-138">Excluir funciones</span><span class="sxs-lookup"><span data-stu-id="ee3d4-138">Exclude functions</span></span>   

<span data-ttu-id="ee3d4-139">Para excluir una función de su perfil de muestreo, selecciónela para seleccionarla y, a continuación, seleccione el icono **excluir la función** seleccionada \ ( ![ excluir la función seleccionada ][ImageExcludeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ee3d4-139">To exclude a function from your Sampling Profile, select it to select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) icon.</span></span>  <span data-ttu-id="ee3d4-140">La función de solicitud \ (primario \) de la función excluida \ (secundario \) se cobra con la memoria asignada a la función excluida \ (hijo \).</span><span class="sxs-lookup"><span data-stu-id="ee3d4-140">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="ee3d4-141">Seleccione el icono **restaurar todas las funciones** \ ( ![ restaurar todas las funciones ][ImageRestoreIcon] \) para volver a restaurar todas las funciones excluidas en la grabación.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-141">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) icon to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="ee3d4-142">Ver perfil de muestreo como gráfico</span><span class="sxs-lookup"><span data-stu-id="ee3d4-142">View Sampling Profile as Chart</span></span>   

<span data-ttu-id="ee3d4-143">La vista de gráfico proporciona una representación visual del perfil de muestreo a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-143">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="ee3d4-144">Después de [grabar un perfil de muestreo](#record-a-sampling-profile), visualice la grabación como un gráfico de llama [cambiando el criterio de ordenación](#change-sort-order) a **gráfico**.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-144">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Vista de gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="ee3d4-146">Vista de gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="ee3d4-146">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="ee3d4-147">El gráfico de llamas se divide en dos partes.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-147">The flame chart is split into two parts.</span></span>  

| | <span data-ttu-id="ee3d4-148">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee3d4-148">Part</span></span> | <span data-ttu-id="ee3d4-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee3d4-149">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="ee3d4-150">uno</span><span class="sxs-lookup"><span data-stu-id="ee3d4-150">1</span></span> | <span data-ttu-id="ee3d4-151">Introducción</span><span class="sxs-lookup"><span data-stu-id="ee3d4-151">Overview</span></span> | <span data-ttu-id="ee3d4-152">Una vista de las aves de toda la grabación.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-152">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="ee3d4-153">El alto de las barras corresponde a la profundidad de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-153">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="ee3d4-154">Por lo tanto, cuanto más alto es la barra, más profunda es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-154">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="ee3d4-155">1</span><span class="sxs-lookup"><span data-stu-id="ee3d4-155">2</span></span> | <span data-ttu-id="ee3d4-156">Pilas de llamadas</span><span class="sxs-lookup"><span data-stu-id="ee3d4-156">Call Stacks</span></span> | <span data-ttu-id="ee3d4-157">Esta es una vista en profundidad de las funciones a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-157">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="ee3d4-158">El eje horizontal es tiempo y eje vertical es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-158">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="ee3d4-159">Las pilas están organizadas de arriba a abajo.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-159">The stacks are organized top-down.</span></span>  <span data-ttu-id="ee3d4-160">Por lo tanto, la función de la parte superior llamará a la que se encuentra debajo, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-160">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="ee3d4-161">Las funciones están coloreadas de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-161">Functions are colored randomly.</span></span>  <span data-ttu-id="ee3d4-162">No hay ninguna correlación de los colores que se usan en los otros paneles.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-162">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="ee3d4-163">Sin embargo, las funciones siempre tienen el mismo color en todas las invocaciones, de modo que pueda ver los patrones en cada tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-163">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de llamas con anotaciones" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="ee3d4-165">Gráfico de llamas con anotaciones</span><span class="sxs-lookup"><span data-stu-id="ee3d4-165">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="ee3d4-166">Una pila de llamadas altas no es necesariamente importante, simplemente significa que se llamó a una gran cantidad de funciones.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-166">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="ee3d4-167">Pero una barra amplia significa que una función tarda mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-167">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="ee3d4-168">Son candidatos para la optimización.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-168">These are candidates for optimization.</span></span>  

### <span data-ttu-id="ee3d4-169">Acercar partes específicas de la grabación</span><span class="sxs-lookup"><span data-stu-id="ee3d4-169">Zoom in on specific parts of recording</span></span>   

<span data-ttu-id="ee3d4-170">Seleccione, mantenga y arrastre el ratón a la izquierda y a la derecha en la información general para acercar determinadas partes de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-170">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="ee3d4-171">Después de aplicar el zoom, la pila de llamadas muestra automáticamente la parte de la grabación que seleccionó.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-171">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico ampliado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="ee3d4-173">Gráfico ampliado</span><span class="sxs-lookup"><span data-stu-id="ee3d4-173">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="ee3d4-174">Ver detalles de la función</span><span class="sxs-lookup"><span data-stu-id="ee3d4-174">View function details</span></span>   

<span data-ttu-id="ee3d4-175">Seleccione en una función para ver la definición en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="ee3d4-175">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="ee3d4-176">Pase el puntero sobre una función para mostrar el nombre y los datos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-176">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="ee3d4-177">Se proporciona la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-177">The following information is provided.</span></span>  

| <span data-ttu-id="ee3d4-178">Todo</span><span class="sxs-lookup"><span data-stu-id="ee3d4-178">Detail</span></span> | <span data-ttu-id="ee3d4-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee3d4-179">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="ee3d4-180">Name</span><span class="sxs-lookup"><span data-stu-id="ee3d4-180">Name</span></span>** | <span data-ttu-id="ee3d4-181">El nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-181">The name of the function.</span></span>  |  
| **<span data-ttu-id="ee3d4-182">Tamaño propio</span><span class="sxs-lookup"><span data-stu-id="ee3d4-182">Self size</span></span>** | <span data-ttu-id="ee3d4-183">Tamaño de la invocación actual de la función, incluidas solo las instrucciones de la función.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-183">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="ee3d4-184">Tamaño total</span><span class="sxs-lookup"><span data-stu-id="ee3d4-184">Total size</span></span>** | <span data-ttu-id="ee3d4-185">Tamaño de la invocación actual de esta función y de las funciones a las que llamó.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-185">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="ee3d4-186">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="ee3d4-186">URL</span></span>** | <span data-ttu-id="ee3d4-187">La ubicación de la definición de función en el formato de `base.js:261` donde `base.js` es el nombre del archivo en el que se define la función y `261` es el número de línea de la definición.</span><span class="sxs-lookup"><span data-stu-id="ee3d4-187">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Ver detalles de funciones en el gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="ee3d4-189">Ver detalles de funciones en el gráfico</span><span class="sxs-lookup"><span data-stu-id="ee3d4-189">Viewing functions details in chart</span></span>  
:::image-end:::  

<!--  
## Feedback   


-->  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Perfil: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd: referencia de API de utilidades de consola | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="ee3d4-193">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee3d4-193">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ee3d4-194">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="ee3d4-194">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ee3d4-196">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee3d4-196">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
