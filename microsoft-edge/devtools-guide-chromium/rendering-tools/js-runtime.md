---
description: Identifica las funciones costosas mediante el panel memoria de Microsoft Edge DevTools.
title: Acelerar el tiempo de ejecución de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 27afe999083470cde0cc0fabf76d0d1ab54e6562
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993586"
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

# <span data-ttu-id="fe31c-104">Acelerar el tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="fe31c-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="fe31c-105">Identifica funciones caras usando el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="fe31c-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfiles de ejemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="fe31c-107">Perfiles de ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe31c-107">Sample Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="fe31c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="fe31c-108">Summary</span></span>  

*   <span data-ttu-id="fe31c-109">Registre exactamente las funciones a las que se llamó y la cantidad de memoria que requiere cada una con el muestreo de asignación en el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="fe31c-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="fe31c-110">Visualice sus perfiles como un gráfico de llamas.</span><span class="sxs-lookup"><span data-stu-id="fe31c-110">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="fe31c-111">Grabar un perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="fe31c-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="fe31c-112">Si observas Jank en tu JavaScript, recopila un perfil de muestreo.</span><span class="sxs-lookup"><span data-stu-id="fe31c-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="fe31c-113">Los perfiles de muestreo muestran dónde se gasta el tiempo de ejecución en las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="fe31c-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="fe31c-114">Vaya al panel **memoria** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="fe31c-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="fe31c-115">Seleccione el botón de opción **muestreo de asignación** .</span><span class="sxs-lookup"><span data-stu-id="fe31c-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="fe31c-116">Selecciona **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="fe31c-116">Select **Start**.</span></span>  
1.  <span data-ttu-id="fe31c-117">En función de lo que intente analizar, puede volver a cargar la página, interactuar con la página o simplemente permitir la ejecución de la página.</span><span class="sxs-lookup"><span data-stu-id="fe31c-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="fe31c-118">Haga clic en el botón **detener** cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="fe31c-118">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="fe31c-119">También puede usar la [API utilidades de consola][DevtoolsConsoleUtilities] para grabar y agrupar perfiles desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fe31c-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="fe31c-120">Ver perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="fe31c-120">View Sampling Profile</span></span>  

<span data-ttu-id="fe31c-121">Cuando termine de grabar, DevTools rellenará automáticamente el panel **memoria** en **perfiles de muestreo** con los datos de su grabación.</span><span class="sxs-lookup"><span data-stu-id="fe31c-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="fe31c-122">La vista predeterminada es **gruesa \ (inferior arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="fe31c-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="fe31c-123">Esta vista le permite ver qué funciones tuvieron el mayor impacto en el rendimiento y examinar las rutas de llamadas a esas funciones.</span><span class="sxs-lookup"><span data-stu-id="fe31c-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="fe31c-124">Cambiar el criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="fe31c-124">Change sort order</span></span>  

<span data-ttu-id="fe31c-125">Para cambiar el orden de clasificación, seleccione el menú desplegable junto al icono **función seleccionada** \ ( ![ enfoque seleccionado de la función ][ImageFocusIcon] \) y, a continuación, elija una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="fe31c-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="fe31c-126">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="fe31c-126">**Chart**.</span></span>  <span data-ttu-id="fe31c-127">Muestra un gráfico cronológico de grabación.</span><span class="sxs-lookup"><span data-stu-id="fe31c-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="fe31c-129">Gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="fe31c-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="fe31c-130">**\ (Inferior arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="fe31c-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="fe31c-131">Enumera las funciones por su impacto en el rendimiento y permite examinar las rutas de la llamada a las funciones.</span><span class="sxs-lookup"><span data-stu-id="fe31c-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="fe31c-132">Esta es la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fe31c-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico grueso" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="fe31c-134">Gráfico grueso</span><span class="sxs-lookup"><span data-stu-id="fe31c-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="fe31c-135">**Tree \ (arriba \)**.</span><span class="sxs-lookup"><span data-stu-id="fe31c-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="fe31c-136">Se muestra una imagen general de la estructura de llamadas, empezando en la parte superior de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="fe31c-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árbol" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="fe31c-138">Gráfico de árbol</span><span class="sxs-lookup"><span data-stu-id="fe31c-138">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="fe31c-139">Excluir funciones</span><span class="sxs-lookup"><span data-stu-id="fe31c-139">Exclude functions</span></span>  

<span data-ttu-id="fe31c-140">Para excluir una función de su perfil de muestreo, selecciónela y, a continuación, seleccione el botón **excluir la función** seleccionada \ ( ![ excluir función seleccionada ][ImageExcludeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="fe31c-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="fe31c-141">La función de solicitud \ (primario \) de la función excluida \ (secundario \) se cobra con la memoria asignada a la función excluida \ (hijo \).</span><span class="sxs-lookup"><span data-stu-id="fe31c-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="fe31c-142">Seleccione el botón **restaurar todas las funciones** \ ( ![ restaurar todas las funciones ][ImageRestoreIcon] \) para volver a restaurar todas las funciones excluidas en la grabación.</span><span class="sxs-lookup"><span data-stu-id="fe31c-142">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="fe31c-143">Ver perfil de muestreo como gráfico</span><span class="sxs-lookup"><span data-stu-id="fe31c-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="fe31c-144">La vista de gráfico proporciona una representación visual del perfil de muestreo a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="fe31c-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="fe31c-145">Después de [grabar un perfil de muestreo](#record-a-sampling-profile), visualice la grabación como un gráfico de llama [cambiando el criterio de ordenación](#change-sort-order) a **gráfico**.</span><span class="sxs-lookup"><span data-stu-id="fe31c-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Vista de gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="fe31c-147">Vista de gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="fe31c-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="fe31c-148">El gráfico de llamas se divide en dos partes.</span><span class="sxs-lookup"><span data-stu-id="fe31c-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="fe31c-149">clasificación</span><span class="sxs-lookup"><span data-stu-id="fe31c-149">index</span></span> | <span data-ttu-id="fe31c-150">Elemento</span><span class="sxs-lookup"><span data-stu-id="fe31c-150">Part</span></span> | <span data-ttu-id="fe31c-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe31c-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="fe31c-152">uno</span><span class="sxs-lookup"><span data-stu-id="fe31c-152">1</span></span> | <span data-ttu-id="fe31c-153">Introducción</span><span class="sxs-lookup"><span data-stu-id="fe31c-153">Overview</span></span> | <span data-ttu-id="fe31c-154">Una vista de las aves de toda la grabación.</span><span class="sxs-lookup"><span data-stu-id="fe31c-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="fe31c-155">El alto de las barras corresponde a la profundidad de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="fe31c-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="fe31c-156">Por lo tanto, cuanto más alto es la barra, más profunda es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="fe31c-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="fe31c-157">1</span><span class="sxs-lookup"><span data-stu-id="fe31c-157">2</span></span> | <span data-ttu-id="fe31c-158">Pilas de llamadas</span><span class="sxs-lookup"><span data-stu-id="fe31c-158">Call Stacks</span></span> | <span data-ttu-id="fe31c-159">Esta es una vista en profundidad de las funciones a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="fe31c-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="fe31c-160">El eje horizontal es tiempo y eje vertical es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="fe31c-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="fe31c-161">Las pilas están organizadas de arriba a abajo.</span><span class="sxs-lookup"><span data-stu-id="fe31c-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="fe31c-162">Por lo tanto, la función de la parte superior llamará a la que se encuentra debajo, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="fe31c-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="fe31c-163">Las funciones están coloreadas de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="fe31c-163">Functions are colored randomly.</span></span>  <span data-ttu-id="fe31c-164">No hay ninguna correlación de los colores que se usan en los otros paneles.</span><span class="sxs-lookup"><span data-stu-id="fe31c-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="fe31c-165">Sin embargo, las funciones siempre tienen el mismo color en todas las invocaciones, de modo que pueda ver los patrones en cada tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="fe31c-165">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de llamas con anotaciones" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="fe31c-167">Gráfico de llamas con anotaciones</span><span class="sxs-lookup"><span data-stu-id="fe31c-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="fe31c-168">Una pila de llamadas altas no es necesariamente importante, simplemente significa que se llamó a una gran cantidad de funciones.</span><span class="sxs-lookup"><span data-stu-id="fe31c-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="fe31c-169">Pero una barra amplia significa que una función tarda mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="fe31c-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="fe31c-170">Son candidatos para la optimización.</span><span class="sxs-lookup"><span data-stu-id="fe31c-170">These are candidates for optimization.</span></span>  

### <span data-ttu-id="fe31c-171">Acercar partes específicas de la grabación</span><span class="sxs-lookup"><span data-stu-id="fe31c-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="fe31c-172">Seleccione, mantenga y arrastre el ratón a la izquierda y a la derecha en la información general para acercar determinadas partes de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="fe31c-172">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="fe31c-173">Después de aplicar el zoom, la pila de llamadas muestra automáticamente la parte de la grabación que seleccionó.</span><span class="sxs-lookup"><span data-stu-id="fe31c-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico ampliado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="fe31c-175">Gráfico ampliado</span><span class="sxs-lookup"><span data-stu-id="fe31c-175">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="fe31c-176">Ver detalles de la función</span><span class="sxs-lookup"><span data-stu-id="fe31c-176">View function details</span></span>  

<span data-ttu-id="fe31c-177">Seleccione en una función para ver la definición en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="fe31c-177">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="fe31c-178">Pase el puntero sobre una función para mostrar el nombre y los datos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fe31c-178">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="fe31c-179">Se proporciona la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="fe31c-179">The following information is provided.</span></span>  

| <span data-ttu-id="fe31c-180">Todo</span><span class="sxs-lookup"><span data-stu-id="fe31c-180">Detail</span></span> | <span data-ttu-id="fe31c-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe31c-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="fe31c-182">Name</span><span class="sxs-lookup"><span data-stu-id="fe31c-182">Name</span></span>** | <span data-ttu-id="fe31c-183">El nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="fe31c-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="fe31c-184">Tamaño propio</span><span class="sxs-lookup"><span data-stu-id="fe31c-184">Self size</span></span>** | <span data-ttu-id="fe31c-185">Tamaño de la invocación actual de la función, incluidas solo las instrucciones de la función.</span><span class="sxs-lookup"><span data-stu-id="fe31c-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="fe31c-186">Tamaño total</span><span class="sxs-lookup"><span data-stu-id="fe31c-186">Total size</span></span>** | <span data-ttu-id="fe31c-187">Tamaño de la invocación actual de esta función y de las funciones a las que llamó.</span><span class="sxs-lookup"><span data-stu-id="fe31c-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="fe31c-188">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="fe31c-188">URL</span></span>** | <span data-ttu-id="fe31c-189">La ubicación de la definición de función en el formato de `base.js:261` donde `base.js` es el nombre del archivo en el que se define la función y `261` es el número de línea de la definición.</span><span class="sxs-lookup"><span data-stu-id="fe31c-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Ver detalles de las funciones en el gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="fe31c-191">Ver detalles de las funciones en el gráfico</span><span class="sxs-lookup"><span data-stu-id="fe31c-191">View functions details in chart</span></span>  
:::image-end:::  

## <span data-ttu-id="fe31c-192">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fe31c-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Perfil: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd: referencia de API de utilidades de consola | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="fe31c-196">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fe31c-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fe31c-197">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="fe31c-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fe31c-199">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fe31c-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
