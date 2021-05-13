---
description: Identifique funciones costosas mediante el Microsoft Edge de memoria de DevTools.
title: Acelerar el tiempo de ejecución de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bbac00ab46e205fb692cc3de3e5f08ba854b0911
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565088"
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
# <a name="speed-up-javascript-runtime"></a><span data-ttu-id="6fa68-104">Acelerar el tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="6fa68-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="6fa68-105">Identificar funciones costosas mediante la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="6fa68-105">Identify expensive functions using the **Memory** tool.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfiles de ejemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="6fa68-107">Perfiles de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fa68-107">Sample Profiles</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="6fa68-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6fa68-108">Summary</span></span>  

*   <span data-ttu-id="6fa68-109">Registre exactamente qué funciones se llamaron y cuánta memoria necesita cada una con el muestreo de asignación en la **herramienta Memoria.**</span><span class="sxs-lookup"><span data-stu-id="6fa68-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** tool.</span></span>  
*   <span data-ttu-id="6fa68-110">Visualiza los perfiles como un gráfico de llamas.</span><span class="sxs-lookup"><span data-stu-id="6fa68-110">Visualize your profiles as a flame chart.</span></span>  
    
## <a name="record-a-sampling-profile"></a><span data-ttu-id="6fa68-111">Registrar un perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="6fa68-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="6fa68-112">Si observa jank en JavaScript, recopile un perfil de muestreo.</span><span class="sxs-lookup"><span data-stu-id="6fa68-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="6fa68-113">Los perfiles de muestreo muestran dónde se dedica el tiempo de ejecución en las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="6fa68-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="6fa68-114">Vaya a la **herramienta Memoria** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="6fa68-114">Navigate to the **Memory** tool of DevTools.</span></span>  
1.  <span data-ttu-id="6fa68-115">Elija el **botón de radio Asignación de** muestreo.</span><span class="sxs-lookup"><span data-stu-id="6fa68-115">Choose the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="6fa68-116">Elija **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="6fa68-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="6fa68-117">Según lo que intente analizar, puede actualizar la página, interactuar con la página o simplemente dejar que se ejecute la página.</span><span class="sxs-lookup"><span data-stu-id="6fa68-117">Depending on what you are trying to analyze, you may either refresh the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="6fa68-118">Elija el **botón** Detener cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="6fa68-118">Choose the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="6fa68-119">También puede usar la [API de utilidades de consola][DevtoolsConsoleUtilities] para registrar y agrupar perfiles desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6fa68-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <a name="view-sampling-profile"></a><span data-ttu-id="6fa68-120">Ver perfil de muestreo</span><span class="sxs-lookup"><span data-stu-id="6fa68-120">View Sampling Profile</span></span>  

<span data-ttu-id="6fa68-121">Cuando termine de grabar, DevTools rellena automáticamente el **panel** Memoria en **PERFILES** DE MUESTREO con los datos de la grabación.</span><span class="sxs-lookup"><span data-stu-id="6fa68-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="6fa68-122">La vista predeterminada es **Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="6fa68-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="6fa68-123">Esta vista le permite revisar qué funciones tuvieron más impacto en el rendimiento y examinar la ruta de acceso de solicitud para cada función.</span><span class="sxs-lookup"><span data-stu-id="6fa68-123">This view allows you to review which functions had the most impact on performance and examine the requesting path for each function.</span></span>  

### <a name="change-sort-order"></a><span data-ttu-id="6fa68-124">Cambiar criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="6fa68-124">Change sort order</span></span>  

<span data-ttu-id="6fa68-125">Para cambiar el orden de ordenación, seleccione el menú desplegable junto al icono de la función seleccionada de foco **\(** Función seleccionada por foco \) y, a continuación, elija una de ![ las siguientes ](../media/focus-icon.msft.png) opciones.</span><span class="sxs-lookup"><span data-stu-id="6fa68-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function](../media/focus-icon.msft.png)\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="6fa68-126">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="6fa68-126">**Chart**.</span></span>  <span data-ttu-id="6fa68-127">Muestra un gráfico cronológico de la grabación.</span><span class="sxs-lookup"><span data-stu-id="6fa68-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="6fa68-129">Gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="6fa68-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="6fa68-130">**Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="6fa68-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="6fa68-131">Enumera las funciones por impacto en el rendimiento y permite examinar las rutas de acceso de llamadas a las funciones.</span><span class="sxs-lookup"><span data-stu-id="6fa68-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="6fa68-132">Esta es la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6fa68-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico pesado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="6fa68-134">Gráfico pesado</span><span class="sxs-lookup"><span data-stu-id="6fa68-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="6fa68-135">**Tree \(Top Down\)**.</span><span class="sxs-lookup"><span data-stu-id="6fa68-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="6fa68-136">Muestra una imagen general de la estructura de llamadas, comenzando en la parte superior de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6fa68-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árbol" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="6fa68-138">Gráfico de árbol</span><span class="sxs-lookup"><span data-stu-id="6fa68-138">Tree chart</span></span>  
:::image-end:::  

### <a name="exclude-functions"></a><span data-ttu-id="6fa68-139">Funciones de exclusión</span><span class="sxs-lookup"><span data-stu-id="6fa68-139">Exclude functions</span></span>  

<span data-ttu-id="6fa68-140">Para excluir una función del perfil de muestreo, selecciónla y, a continuación, elija el botón excluir la función seleccionada **\(** ![ excluir la función seleccionada ](../media/exclude-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="6fa68-140">To exclude a function from your Sampling Profile, choose it and then choose the **exclude selected function** \(![exclude selected function](../media/exclude-icon.msft.png)\) button.</span></span>  <span data-ttu-id="6fa68-141">La función de solicitud \(parent\) de la función excluida \(child\) se carga con la memoria asignada a la función excluida \(child\).</span><span class="sxs-lookup"><span data-stu-id="6fa68-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="6fa68-142">Elija el **botón restaurar todas las funciones** \( restaurar todas las funciones \) para restaurar todas las funciones excluidas de nuevo en la ![ ](../media/restore-icon.msft.png) grabación.</span><span class="sxs-lookup"><span data-stu-id="6fa68-142">Choose the **restore all functions** \(![restore all functions](../media/restore-icon.msft.png)\) button to restore all excluded functions back into the recording.</span></span>  

## <a name="view-sampling-profile-as-chart"></a><span data-ttu-id="6fa68-143">Ver perfil de muestreo como gráfico</span><span class="sxs-lookup"><span data-stu-id="6fa68-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="6fa68-144">La vista Gráfico proporciona una representación visual del perfil de muestreo con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="6fa68-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="6fa68-145">Después de [grabar un perfil de muestreo,](#record-a-sampling-profile)vea la grabación como un gráfico de llama cambiando el criterio de [ordenación](#change-sort-order) a **Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="6fa68-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Vista gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="6fa68-147">Vista gráfico de llamas</span><span class="sxs-lookup"><span data-stu-id="6fa68-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="6fa68-148">El gráfico de llama se divide en dos partes.</span><span class="sxs-lookup"><span data-stu-id="6fa68-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="6fa68-149">index</span><span class="sxs-lookup"><span data-stu-id="6fa68-149">index</span></span> | <span data-ttu-id="6fa68-150">Parte</span><span class="sxs-lookup"><span data-stu-id="6fa68-150">Part</span></span> | <span data-ttu-id="6fa68-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fa68-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="6fa68-152">1</span><span class="sxs-lookup"><span data-stu-id="6fa68-152">1</span></span> | <span data-ttu-id="6fa68-153">Información general</span><span class="sxs-lookup"><span data-stu-id="6fa68-153">Overview</span></span> | <span data-ttu-id="6fa68-154">Una vista visual de toda la grabación.</span><span class="sxs-lookup"><span data-stu-id="6fa68-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="6fa68-155">El alto de las barras corresponde a la profundidad de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6fa68-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="6fa68-156">Por lo tanto, cuanto mayor sea la barra, más profunda será la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6fa68-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="6fa68-157">2</span><span class="sxs-lookup"><span data-stu-id="6fa68-157">2</span></span> | <span data-ttu-id="6fa68-158">Pilas de llamadas</span><span class="sxs-lookup"><span data-stu-id="6fa68-158">Call Stacks</span></span> | <span data-ttu-id="6fa68-159">Se trata de una vista detallada de las funciones a las que se llamó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="6fa68-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="6fa68-160">El eje horizontal es el tiempo y el eje vertical es la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6fa68-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="6fa68-161">Las pilas están organizadas de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="6fa68-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="6fa68-162">Por lo tanto, la función en la parte superior llamada a la que está debajo de ella, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="6fa68-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="6fa68-163">Las funciones se coloreadas aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="6fa68-163">Functions are colored randomly.</span></span>  <span data-ttu-id="6fa68-164">No hay ninguna correlación con los colores usados en los otros paneles.</span><span class="sxs-lookup"><span data-stu-id="6fa68-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="6fa68-165">Sin embargo, las funciones siempre tienen el mismo color entre invocaciones para que pueda observar patrones en cada tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6fa68-165">However, functions are always colored the same across invocations so that you may observe patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de llama anotado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="6fa68-167">Gráfico de llama anotado</span><span class="sxs-lookup"><span data-stu-id="6fa68-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="6fa68-168">Una pila de llamadas alta no es necesariamente significativa, solo significa que se llamaron a muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="6fa68-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="6fa68-169">Pero una barra ancha significa que una función tardó mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="6fa68-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="6fa68-170">Estos son los candidatos para la optimización.</span><span class="sxs-lookup"><span data-stu-id="6fa68-170">These are candidates for optimization.</span></span>  

### <a name="zoom-in-on-specific-parts-of-recording"></a><span data-ttu-id="6fa68-171">Acercar partes específicas de la grabación</span><span class="sxs-lookup"><span data-stu-id="6fa68-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="6fa68-172">Elija, mantenga presionado y arrastre el mouse hacia la izquierda y la derecha a través de la información general para acercarse a partes concretas de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6fa68-172">Choose, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="6fa68-173">Después de hacer zoom, la pila de llamadas muestra automáticamente la parte de la grabación que seleccionó.</span><span class="sxs-lookup"><span data-stu-id="6fa68-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico zoomed" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="6fa68-175">Gráfico zoomed</span><span class="sxs-lookup"><span data-stu-id="6fa68-175">Chart zoomed</span></span>  
:::image-end:::  

### <a name="view-function-details"></a><span data-ttu-id="6fa68-176">Ver detalles de la función</span><span class="sxs-lookup"><span data-stu-id="6fa68-176">View function details</span></span>  

<span data-ttu-id="6fa68-177">Elija una función para ver la definición en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="6fa68-177">Choose a function to view the definition in the **Sources** tool.</span></span>  

<span data-ttu-id="6fa68-178">Mantenga el mouse sobre una función para mostrar el nombre y los datos de temporización.</span><span class="sxs-lookup"><span data-stu-id="6fa68-178">Hover on a function to display the name and timing data.</span></span>  <span data-ttu-id="6fa68-179">Se proporciona la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="6fa68-179">The following information is provided.</span></span>  

| <span data-ttu-id="6fa68-180">Detalle</span><span class="sxs-lookup"><span data-stu-id="6fa68-180">Detail</span></span> | <span data-ttu-id="6fa68-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fa68-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="6fa68-182">Name</span><span class="sxs-lookup"><span data-stu-id="6fa68-182">Name</span></span>** | <span data-ttu-id="6fa68-183">Nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="6fa68-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="6fa68-184">Tamaño propio</span><span class="sxs-lookup"><span data-stu-id="6fa68-184">Self size</span></span>** | <span data-ttu-id="6fa68-185">Tamaño de la invocación actual de la función, incluidas solo las instrucciones de la función.</span><span class="sxs-lookup"><span data-stu-id="6fa68-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="6fa68-186">Tamaño total</span><span class="sxs-lookup"><span data-stu-id="6fa68-186">Total size</span></span>** | <span data-ttu-id="6fa68-187">El tamaño de la invocación actual de esta función y las funciones a las que llamó.</span><span class="sxs-lookup"><span data-stu-id="6fa68-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="6fa68-188">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="6fa68-188">URL</span></span>** | <span data-ttu-id="6fa68-189">La ubicación de la definición de función en forma de dónde es el nombre del archivo donde se define la función y es el número de línea `base.js:261` `base.js` de la `261` definición.</span><span class="sxs-lookup"><span data-stu-id="6fa68-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Ver detalles de funciones en el gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="6fa68-191">Ver detalles de funciones en el gráfico</span><span class="sxs-lookup"><span data-stu-id="6fa68-191">View functions details in chart</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6fa68-192">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6fa68-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referencia de API de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "perfil: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd: referencia de api de utilidades de consola | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="6fa68-196">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6fa68-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6fa68-197">La página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="6fa68-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6fa68-199">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6fa68-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
