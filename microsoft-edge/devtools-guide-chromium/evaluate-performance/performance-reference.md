---
title: Referencia de evento de escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611723"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="633ca-103">Referencia de evento de escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="633ca-103">Timeline Event Reference</span></span>   




<span data-ttu-id="633ca-104">El modo eventos de escala de tiempo muestra todos los eventos desencadenados mientras se realiza una grabación.</span><span class="sxs-lookup"><span data-stu-id="633ca-104">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="633ca-105">Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="633ca-105">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="633ca-106">Propiedades de evento de escala de tiempo comunes</span><span class="sxs-lookup"><span data-stu-id="633ca-106">Common timeline event properties</span></span>  

<span data-ttu-id="633ca-107">Algunos detalles están presentes en eventos de todos los tipos, mientras que algunos solo se aplican a determinados tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="633ca-107">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="633ca-108">En esta sección se enumeran las propiedades comunes a los distintos tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="633ca-108">This section lists properties common to different event types.</span></span>  <span data-ttu-id="633ca-109">Las propiedades específicas de determinados tipos de eventos se muestran en las referencias de los siguientes tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="633ca-109">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="633ca-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="633ca-110">Property</span></span> | <span data-ttu-id="633ca-111">¿Cuándo se muestra?</span><span class="sxs-lookup"><span data-stu-id="633ca-111">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-112">Tiempo agregado</span><span class="sxs-lookup"><span data-stu-id="633ca-112">Aggregated time</span></span> | <span data-ttu-id="633ca-113">Para eventos con **eventos anidados**, el tiempo que toma cada categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="633ca-113">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="633ca-114">Pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="633ca-114">Call Stack</span></span> | <span data-ttu-id="633ca-115">Para eventos con **eventos secundarios**, el tiempo que toma cada categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="633ca-115">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="633ca-116">Tiempo de CPU</span><span class="sxs-lookup"><span data-stu-id="633ca-116">CPU time</span></span> | <span data-ttu-id="633ca-117">La cantidad de tiempo de CPU que tomó el evento registrado.</span><span class="sxs-lookup"><span data-stu-id="633ca-117">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="633ca-118">Detalles</span><span class="sxs-lookup"><span data-stu-id="633ca-118">Details</span></span> | <span data-ttu-id="633ca-119">Otros detalles sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="633ca-119">Other details about the event.</span></span> |  
| <span data-ttu-id="633ca-120">Duration \ (en la marca de hora \)</span><span class="sxs-lookup"><span data-stu-id="633ca-120">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="633ca-121">Cuánto tiempo duró el evento con todos sus elementos secundarios para completar. TIMESTAMP es la hora en que se produjo el evento, en relación con la grabación iniciada.</span><span class="sxs-lookup"><span data-stu-id="633ca-121">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="633ca-122">Tiempo propio</span><span class="sxs-lookup"><span data-stu-id="633ca-122">Self time</span></span> | <span data-ttu-id="633ca-123">Cuánto tiempo lleva el evento sin ninguno de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="633ca-123">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="633ca-124">Tamaño de montón usado</span><span class="sxs-lookup"><span data-stu-id="633ca-124">Used Heap Size</span></span> | <span data-ttu-id="633ca-125">Cantidad de memoria usada por la aplicación cuando se registró el evento y el cambio Delta \ (+/-\) en el tamaño de montón usado desde el último muestreo.</span><span class="sxs-lookup"><span data-stu-id="633ca-125">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="633ca-126">Cargando eventos</span><span class="sxs-lookup"><span data-stu-id="633ca-126">Loading events</span></span>  

<span data-ttu-id="633ca-127">En esta sección se enumeran los eventos que pertenecen a la categoría de carga y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="633ca-127">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="633ca-128">Evento</span><span class="sxs-lookup"><span data-stu-id="633ca-128">Event</span></span> | <span data-ttu-id="633ca-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-129">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-130">Analizar HTML</span><span class="sxs-lookup"><span data-stu-id="633ca-130">Parse HTML</span></span> |  <span data-ttu-id="633ca-131">Microsoft Edge ejecutó el algoritmo de análisis HTML.</span><span class="sxs-lookup"><span data-stu-id="633ca-131">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="633ca-132">Finalizar la carga</span><span class="sxs-lookup"><span data-stu-id="633ca-132">Finish Loading</span></span> |  <span data-ttu-id="633ca-133">Una solicitud de red completada.</span><span class="sxs-lookup"><span data-stu-id="633ca-133">A network request completed.</span></span> |  
| <span data-ttu-id="633ca-134">Recibir datos</span><span class="sxs-lookup"><span data-stu-id="633ca-134">Receive Data</span></span> |  <span data-ttu-id="633ca-135">Se recibieron datos para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="633ca-135">Data for a request was received.</span></span>  <span data-ttu-id="633ca-136">Hay uno o más eventos de datos de recepción.</span><span class="sxs-lookup"><span data-stu-id="633ca-136">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="633ca-137">Recibir respuesta</span><span class="sxs-lookup"><span data-stu-id="633ca-137">Receive Response</span></span> |  <span data-ttu-id="633ca-138">La respuesta HTTP inicial de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="633ca-138">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="633ca-139">Enviar solicitud</span><span class="sxs-lookup"><span data-stu-id="633ca-139">Send Request</span></span> |  <span data-ttu-id="633ca-140">Se ha enviado una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="633ca-140">A network request has been sent.</span></span> |  

### <span data-ttu-id="633ca-141">Cargando propiedades de evento</span><span class="sxs-lookup"><span data-stu-id="633ca-141">Loading event properties</span></span>  

| <span data-ttu-id="633ca-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="633ca-142">Property</span></span> | <span data-ttu-id="633ca-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-143">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-144">Recurso</span><span class="sxs-lookup"><span data-stu-id="633ca-144">Resource</span></span> | <span data-ttu-id="633ca-145">Dirección URL del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="633ca-145">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="633ca-146">Vista previa</span><span class="sxs-lookup"><span data-stu-id="633ca-146">Preview</span></span> | <span data-ttu-id="633ca-147">Vista previa del recurso solicitado \ (solo imágenes \).</span><span class="sxs-lookup"><span data-stu-id="633ca-147">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="633ca-148">Método de solicitud</span><span class="sxs-lookup"><span data-stu-id="633ca-148">Request Method</span></span> | <span data-ttu-id="633ca-149">Método HTTP usado para la solicitud \ ( `GET` o `POST` , por ejemplo, \).</span><span class="sxs-lookup"><span data-stu-id="633ca-149">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="633ca-150">Código de estado</span><span class="sxs-lookup"><span data-stu-id="633ca-150">Status Code</span></span> | <span data-ttu-id="633ca-151">Código de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="633ca-151">HTTP response code.</span></span> |  
| <span data-ttu-id="633ca-152">Tipo MIME</span><span class="sxs-lookup"><span data-stu-id="633ca-152">MIME Type</span></span> | <span data-ttu-id="633ca-153">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="633ca-153">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="633ca-154">Longitud de datos codificados</span><span class="sxs-lookup"><span data-stu-id="633ca-154">Encoded Data Length</span></span> | <span data-ttu-id="633ca-155">Longitud del recurso solicitado en bytes.</span><span class="sxs-lookup"><span data-stu-id="633ca-155">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="633ca-156">Eventos de scripting</span><span class="sxs-lookup"><span data-stu-id="633ca-156">Scripting events</span></span>  

<span data-ttu-id="633ca-157">En esta sección se enumeran los eventos que pertenecen a la categoría de scripting y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="633ca-157">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="633ca-158">Evento</span><span class="sxs-lookup"><span data-stu-id="633ca-158">Event</span></span> | <span data-ttu-id="633ca-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-159">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-160">Marco de animación desencadenado</span><span class="sxs-lookup"><span data-stu-id="633ca-160">Animation Frame Fired</span></span> | <span data-ttu-id="633ca-161">Se activó un marco de animación programada y se llamará a su controlador de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="633ca-161">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="633ca-162">Cancelar marco de animación</span><span class="sxs-lookup"><span data-stu-id="633ca-162">Cancel Animation Frame</span></span> |  <span data-ttu-id="633ca-163">Se ha cancelado un marco de animación programado.</span><span class="sxs-lookup"><span data-stu-id="633ca-163">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="633ca-164">Evento GC</span><span class="sxs-lookup"><span data-stu-id="633ca-164">GC Event</span></span> |  <span data-ttu-id="633ca-165">Se realizó la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="633ca-165">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="633ca-166">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="633ca-166">DOMContentLoaded</span></span> |  <span data-ttu-id="633ca-167">El [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] fue desencadenado por el explorador.</span><span class="sxs-lookup"><span data-stu-id="633ca-167">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="633ca-168">Este evento se desencadena cuando todo el contenido de DOM de la página se ha cargado y analizado.</span><span class="sxs-lookup"><span data-stu-id="633ca-168">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="633ca-169">Evaluar script</span><span class="sxs-lookup"><span data-stu-id="633ca-169">Evaluate Script</span></span> | <span data-ttu-id="633ca-170">Se evaluó un script.</span><span class="sxs-lookup"><span data-stu-id="633ca-170">A script was evaluated.</span></span> |  
| <span data-ttu-id="633ca-171">Evento</span><span class="sxs-lookup"><span data-stu-id="633ca-171">Event</span></span> | <span data-ttu-id="633ca-172">Un evento de JavaScript \ (por ejemplo, `mousedown` , o `key` \).</span><span class="sxs-lookup"><span data-stu-id="633ca-172">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="633ca-173">Llamada de función</span><span class="sxs-lookup"><span data-stu-id="633ca-173">Function Call</span></span> | <span data-ttu-id="633ca-174">Se realizó una llamada de función de JavaScript de nivel superior \ (solo aparece cuando el explorador escribe el motor de JavaScript \).</span><span class="sxs-lookup"><span data-stu-id="633ca-174">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="633ca-175">Instalar cronómetro</span><span class="sxs-lookup"><span data-stu-id="633ca-175">Install Timer</span></span> | <span data-ttu-id="633ca-176">Se creó un temporizador con [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] o [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="633ca-176">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="633ca-177">Marco de animación de la solicitud</span><span class="sxs-lookup"><span data-stu-id="633ca-177">Request Animation Frame</span></span> | <span data-ttu-id="633ca-178">Una `requestAnimationFrame()` llamada programó un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="633ca-178">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="633ca-179">Quitar cronómetro</span><span class="sxs-lookup"><span data-stu-id="633ca-179">Remove Timer</span></span> | <span data-ttu-id="633ca-180">Se borró un temporizador creado previamente.</span><span class="sxs-lookup"><span data-stu-id="633ca-180">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="633ca-181">Tiempo</span><span class="sxs-lookup"><span data-stu-id="633ca-181">Time</span></span> |  <span data-ttu-id="633ca-182">Un script denominado [Console. Time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="633ca-182">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="633ca-183">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="633ca-183">Time End</span></span> | <span data-ttu-id="633ca-184">Un script denominado [Console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="633ca-184">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="633ca-185">Cronómetro desencadenado</span><span class="sxs-lookup"><span data-stu-id="633ca-185">Timer Fired</span></span> | <span data-ttu-id="633ca-186">Un temporizador desencadenado que se programó con `setInterval()` o `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="633ca-186">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="633ca-187">Cambio de estado de XHR listo</span><span class="sxs-lookup"><span data-stu-id="633ca-187">XHR Ready State Change</span></span> | <span data-ttu-id="633ca-188">El estado de lista de un XMLHTTPRequest ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="633ca-188">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="633ca-189">Carga de XHR</span><span class="sxs-lookup"><span data-stu-id="633ca-189">XHR Load</span></span> | <span data-ttu-id="633ca-190">`XMLHTTPRequest`Finalizó la carga.</span><span class="sxs-lookup"><span data-stu-id="633ca-190">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="633ca-191">Propiedades de eventos de scripting</span><span class="sxs-lookup"><span data-stu-id="633ca-191">Scripting event properties</span></span>  

| <span data-ttu-id="633ca-192">Propiedad</span><span class="sxs-lookup"><span data-stu-id="633ca-192">Property</span></span> | <span data-ttu-id="633ca-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-193">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-194">IDENTIFICADOR del temporizador</span><span class="sxs-lookup"><span data-stu-id="633ca-194">Timer ID</span></span> | <span data-ttu-id="633ca-195">IDENTIFICADOR del temporizador.</span><span class="sxs-lookup"><span data-stu-id="633ca-195">The timer ID.</span></span> |  
| <span data-ttu-id="633ca-196">Tiempo de espera agotado</span><span class="sxs-lookup"><span data-stu-id="633ca-196">Timeout</span></span> | <span data-ttu-id="633ca-197">El tiempo de espera especificado por el temporizador.</span><span class="sxs-lookup"><span data-stu-id="633ca-197">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="633ca-198">Repite</span><span class="sxs-lookup"><span data-stu-id="633ca-198">Repeats</span></span> | <span data-ttu-id="633ca-199">Valor booleano que especifica si el temporizador se repite.</span><span class="sxs-lookup"><span data-stu-id="633ca-199">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="633ca-200">Llamada de función</span><span class="sxs-lookup"><span data-stu-id="633ca-200">Function Call</span></span> | <span data-ttu-id="633ca-201">Una función que se invocó.</span><span class="sxs-lookup"><span data-stu-id="633ca-201">A function that was invoked.</span></span> |  

## <span data-ttu-id="633ca-202">Representar eventos</span><span class="sxs-lookup"><span data-stu-id="633ca-202">Rendering events</span></span>  

<span data-ttu-id="633ca-203">En esta sección se enumeran los eventos que pertenecen a la categoría de representación y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="633ca-203">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="633ca-204">Evento</span><span class="sxs-lookup"><span data-stu-id="633ca-204">Event</span></span> | <span data-ttu-id="633ca-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-205">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-206">Invalidar diseño</span><span class="sxs-lookup"><span data-stu-id="633ca-206">Invalidate layout</span></span> | <span data-ttu-id="633ca-207">Un cambio de DOM invalidó el diseño de página.</span><span class="sxs-lookup"><span data-stu-id="633ca-207">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="633ca-208">Diseño</span><span class="sxs-lookup"><span data-stu-id="633ca-208">Layout</span></span> | <span data-ttu-id="633ca-209">Se completó un diseño de página.</span><span class="sxs-lookup"><span data-stu-id="633ca-209">A page layout was completed.</span></span> |  
| <span data-ttu-id="633ca-210">Recalcular estilo</span><span class="sxs-lookup"><span data-stu-id="633ca-210">Recalculate style</span></span> | <span data-ttu-id="633ca-211">Estilos de elemento recalculado de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="633ca-211">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="633ca-212">Scroll</span><span class="sxs-lookup"><span data-stu-id="633ca-212">Scroll</span></span> | <span data-ttu-id="633ca-213">Se ha desplazado el contenido de la vista anidada.</span><span class="sxs-lookup"><span data-stu-id="633ca-213">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="633ca-214">Representación de propiedades de eventos</span><span class="sxs-lookup"><span data-stu-id="633ca-214">Rendering event properties</span></span>  

| <span data-ttu-id="633ca-215">Propiedad</span><span class="sxs-lookup"><span data-stu-id="633ca-215">Property</span></span> | <span data-ttu-id="633ca-216">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-216">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-217">Diseño invalidado</span><span class="sxs-lookup"><span data-stu-id="633ca-217">Layout invalidated</span></span> | <span data-ttu-id="633ca-218">En los registros de diseño, el seguimiento de la pila del código que causó que se invalidara el diseño.</span><span class="sxs-lookup"><span data-stu-id="633ca-218">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="633ca-219">Nodos que necesitan diseño</span><span class="sxs-lookup"><span data-stu-id="633ca-219">Nodes that need layout</span></span> | <span data-ttu-id="633ca-220">En los registros de diseño, el número de nodos que se han marcado como que necesitan diseño antes de que se inicie el redistribución.</span><span class="sxs-lookup"><span data-stu-id="633ca-220">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="633ca-221">Suelen ser aquellos nodos que el código del desarrollador invalidó, además de una ruta de acceso ascendente para rediseñar la raíz.</span><span class="sxs-lookup"><span data-stu-id="633ca-221">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="633ca-222">Tamaño del árbol de diseño</span><span class="sxs-lookup"><span data-stu-id="633ca-222">Layout tree size</span></span> | <span data-ttu-id="633ca-223">En los registros de diseño, el número total de nodos en la raíz de redistribución \ (el nodo en el que Microsoft Edge inicia el rediseño \).</span><span class="sxs-lookup"><span data-stu-id="633ca-223">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="633ca-224">Ámbito de diseño</span><span class="sxs-lookup"><span data-stu-id="633ca-224">Layout scope</span></span> | <span data-ttu-id="633ca-225">Los valores posibles son `Partial` \ (el límite de redistribución es una parte del DOM \) o `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="633ca-225">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="633ca-226">Elementos afectados</span><span class="sxs-lookup"><span data-stu-id="633ca-226">Elements affected</span></span> | <span data-ttu-id="633ca-227">Para volver a calcular los registros de estilo, el número de elementos afectados por un nuevo cálculo de estilo.</span><span class="sxs-lookup"><span data-stu-id="633ca-227">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="633ca-228">Estilos invalidados</span><span class="sxs-lookup"><span data-stu-id="633ca-228">Styles invalidated</span></span> | <span data-ttu-id="633ca-229">Para recalcular los registros de estilo, proporciona el seguimiento de pila del código que causó la invalidación de estilo.</span><span class="sxs-lookup"><span data-stu-id="633ca-229">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="633ca-230">Eventos de pintura</span><span class="sxs-lookup"><span data-stu-id="633ca-230">Painting events</span></span>  

<span data-ttu-id="633ca-231">En esta sección se enumeran los eventos que pertenecen a la categoría de pintura y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="633ca-231">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="633ca-232">Evento</span><span class="sxs-lookup"><span data-stu-id="633ca-232">Event</span></span> | <span data-ttu-id="633ca-233">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-233">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-234">Capas compuestas</span><span class="sxs-lookup"><span data-stu-id="633ca-234">Composite Layers</span></span> | <span data-ttu-id="633ca-235">Las capas de imagen compuestas para el motor de representación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="633ca-235">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="633ca-236">Descodificación de imagen</span><span class="sxs-lookup"><span data-stu-id="633ca-236">Image Decode</span></span> | <span data-ttu-id="633ca-237">Se ha descodificado un recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="633ca-237">An image resource was decoded.</span></span> |  
| <span data-ttu-id="633ca-238">Cambiar el tamaño de la imagen</span><span class="sxs-lookup"><span data-stu-id="633ca-238">Image Resize</span></span> | <span data-ttu-id="633ca-239">Se ha cambiado el tamaño de una imagen desde sus dimensiones nativas.</span><span class="sxs-lookup"><span data-stu-id="633ca-239">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="633ca-240">Paint</span><span class="sxs-lookup"><span data-stu-id="633ca-240">Paint</span></span> | <span data-ttu-id="633ca-241">Las capas compuestas se han pintado en una región de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="633ca-241">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="633ca-242">Al mantener el puntero sobre un registro de pintura, se resalta la región de la pantalla que se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="633ca-242">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="633ca-243">Propiedades de evento de dibujo</span><span class="sxs-lookup"><span data-stu-id="633ca-243">Painting event properties</span></span>  

| <span data-ttu-id="633ca-244">Propiedad</span><span class="sxs-lookup"><span data-stu-id="633ca-244">Property</span></span> | <span data-ttu-id="633ca-245">Descripción</span><span class="sxs-lookup"><span data-stu-id="633ca-245">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="633ca-246">Ubicación</span><span class="sxs-lookup"><span data-stu-id="633ca-246">Location</span></span> | <span data-ttu-id="633ca-247">Para eventos de pintura, las coordenadas x e y del rectángulo de pintura.</span><span class="sxs-lookup"><span data-stu-id="633ca-247">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="633ca-248">Dimensiones</span><span class="sxs-lookup"><span data-stu-id="633ca-248">Dimensions</span></span> | <span data-ttu-id="633ca-249">Para eventos de pintura, el alto y el ancho de la región pintada.</span><span class="sxs-lookup"><span data-stu-id="633ca-249">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Referencia de la API de consola de hora"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd: referencia de la API de consola"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Ventana: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="633ca-255">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="633ca-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="633ca-256">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Flavio Copes][FlavioCopes] \ (desarrollador de pila completa \).</span><span class="sxs-lookup"><span data-stu-id="633ca-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="633ca-258">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="633ca-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
