---
description: El modo de eventos de escala de tiempo muestra todos los eventos desencadenados al realizar una grabación.  Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.
title: Referencia de evento de escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b8a15dd3503a891698d1f96bdc99946163d738ff
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564213"
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
# <a name="timeline-event-reference"></a><span data-ttu-id="b531f-105">Referencia de evento de escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="b531f-105">Timeline Event reference</span></span>  

<span data-ttu-id="b531f-106">El modo de eventos de escala de tiempo muestra todos los eventos desencadenados al realizar una grabación.</span><span class="sxs-lookup"><span data-stu-id="b531f-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="b531f-107">Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b531f-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <a name="common-timeline-event-properties"></a><span data-ttu-id="b531f-108">Propiedades de eventos de escala de tiempo comunes</span><span class="sxs-lookup"><span data-stu-id="b531f-108">Common timeline event properties</span></span>  

<span data-ttu-id="b531f-109">Algunos detalles están presentes en eventos de todos los tipos, mientras que algunos solo se aplican a determinados tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="b531f-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="b531f-110">En esta sección se enumeran las propiedades comunes a diferentes tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="b531f-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="b531f-111">Las propiedades específicas de determinados tipos de eventos se enumeran en las referencias para los tipos de eventos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b531f-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="b531f-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b531f-112">Property</span></span> | <span data-ttu-id="b531f-113">Cuándo se muestra</span><span class="sxs-lookup"><span data-stu-id="b531f-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-114">Tiempo agregado</span><span class="sxs-lookup"><span data-stu-id="b531f-114">Aggregated time</span></span> | <span data-ttu-id="b531f-115">Para eventos con **eventos anidados**, el tiempo que toma cada categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="b531f-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="b531f-116">Pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="b531f-116">Call Stack</span></span> | <span data-ttu-id="b531f-117">Para eventos con **eventos secundarios**, el tiempo que toma cada categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="b531f-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="b531f-118">Tiempo de CPU</span><span class="sxs-lookup"><span data-stu-id="b531f-118">CPU time</span></span> | <span data-ttu-id="b531f-119">Cuánto tiempo de CPU tardó el evento grabado.</span><span class="sxs-lookup"><span data-stu-id="b531f-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="b531f-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="b531f-120">Details</span></span> | <span data-ttu-id="b531f-121">Otros detalles sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="b531f-121">Other details about the event.</span></span> |  
| <span data-ttu-id="b531f-122">Duración \(at time-stamp\)</span><span class="sxs-lookup"><span data-stu-id="b531f-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="b531f-123">Cuánto tiempo tardó el evento con todos sus secundarios en completarse; timestamp es la hora en la que se produjo el evento, en relación con el momento en que se inició la grabación.</span><span class="sxs-lookup"><span data-stu-id="b531f-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="b531f-124">Tiempo de autoservicio</span><span class="sxs-lookup"><span data-stu-id="b531f-124">Self time</span></span> | <span data-ttu-id="b531f-125">Cuánto tiempo tardó el evento sin ninguno de sus secundarios.</span><span class="sxs-lookup"><span data-stu-id="b531f-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="b531f-126">Tamaño de montón usado</span><span class="sxs-lookup"><span data-stu-id="b531f-126">Used Heap Size</span></span> | <span data-ttu-id="b531f-127">Cantidad de memoria que usa la aplicación cuando se registró el evento y el delta \(+/-\) cambia en el tamaño del montón usado desde el último muestreo.</span><span class="sxs-lookup"><span data-stu-id="b531f-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a><span data-ttu-id="b531f-128">Cargar eventos</span><span class="sxs-lookup"><span data-stu-id="b531f-128">Loading events</span></span>  

<span data-ttu-id="b531f-129">En esta sección se enumeran los eventos que pertenecen a la categoría Loading y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="b531f-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="b531f-130">Evento</span><span class="sxs-lookup"><span data-stu-id="b531f-130">Event</span></span> | <span data-ttu-id="b531f-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-132">ANALIZAR HTML</span><span class="sxs-lookup"><span data-stu-id="b531f-132">Parse HTML</span></span> |  <span data-ttu-id="b531f-133">Microsoft Edge el algoritmo de análisis HTML.</span><span class="sxs-lookup"><span data-stu-id="b531f-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="b531f-134">Finalizar la carga</span><span class="sxs-lookup"><span data-stu-id="b531f-134">Finish Loading</span></span> |  <span data-ttu-id="b531f-135">Una solicitud de red completada.</span><span class="sxs-lookup"><span data-stu-id="b531f-135">A network request completed.</span></span> |  
| <span data-ttu-id="b531f-136">Recibir datos</span><span class="sxs-lookup"><span data-stu-id="b531f-136">Receive Data</span></span> |  <span data-ttu-id="b531f-137">Se recibieron los datos de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b531f-137">Data for a request was received.</span></span>  <span data-ttu-id="b531f-138">Hay uno o varios eventos De recepción de datos.</span><span class="sxs-lookup"><span data-stu-id="b531f-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="b531f-139">Respuesta de recepción</span><span class="sxs-lookup"><span data-stu-id="b531f-139">Receive Response</span></span> |  <span data-ttu-id="b531f-140">La respuesta HTTP inicial de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b531f-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="b531f-141">Enviar solicitud</span><span class="sxs-lookup"><span data-stu-id="b531f-141">Send Request</span></span> |  <span data-ttu-id="b531f-142">Se ha enviado una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="b531f-142">A network request has been sent.</span></span> |  

### <a name="loading-event-properties"></a><span data-ttu-id="b531f-143">Cargar propiedades de evento</span><span class="sxs-lookup"><span data-stu-id="b531f-143">Loading event properties</span></span>  

| <span data-ttu-id="b531f-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b531f-144">Property</span></span> | <span data-ttu-id="b531f-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-146">Recurso</span><span class="sxs-lookup"><span data-stu-id="b531f-146">Resource</span></span> | <span data-ttu-id="b531f-147">Dirección URL del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="b531f-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="b531f-148">Vista previa</span><span class="sxs-lookup"><span data-stu-id="b531f-148">Preview</span></span> | <span data-ttu-id="b531f-149">Vista previa del recurso solicitado \(solo imágenes\).</span><span class="sxs-lookup"><span data-stu-id="b531f-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="b531f-150">Request (método)</span><span class="sxs-lookup"><span data-stu-id="b531f-150">Request Method</span></span> | <span data-ttu-id="b531f-151">Método HTTP usado para la solicitud \( `GET` o `POST` , por ejemplo\).</span><span class="sxs-lookup"><span data-stu-id="b531f-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="b531f-152">Código de estado</span><span class="sxs-lookup"><span data-stu-id="b531f-152">Status Code</span></span> | <span data-ttu-id="b531f-153">Código de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b531f-153">HTTP response code.</span></span> |  
| <span data-ttu-id="b531f-154">Tipo MIME</span><span class="sxs-lookup"><span data-stu-id="b531f-154">MIME Type</span></span> | <span data-ttu-id="b531f-155">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="b531f-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="b531f-156">Longitud de datos codificada</span><span class="sxs-lookup"><span data-stu-id="b531f-156">Encoded Data Length</span></span> | <span data-ttu-id="b531f-157">Longitud del recurso solicitado en bytes.</span><span class="sxs-lookup"><span data-stu-id="b531f-157">Length of requested resource in bytes.</span></span> |  

## <a name="scripting-events"></a><span data-ttu-id="b531f-158">Eventos de scripting</span><span class="sxs-lookup"><span data-stu-id="b531f-158">Scripting events</span></span>  

<span data-ttu-id="b531f-159">En esta sección se enumeran los eventos que pertenecen a la categoría Scripting y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="b531f-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="b531f-160">Evento</span><span class="sxs-lookup"><span data-stu-id="b531f-160">Event</span></span> | <span data-ttu-id="b531f-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-162">Fotograma de animación desencadenado</span><span class="sxs-lookup"><span data-stu-id="b531f-162">Animation Frame Fired</span></span> | <span data-ttu-id="b531f-163">Se desencadena un marco de animación programado y se invoca su controlador de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b531f-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="b531f-164">Cancelar fotograma de animación</span><span class="sxs-lookup"><span data-stu-id="b531f-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="b531f-165">Se canceló un marco de animación programado.</span><span class="sxs-lookup"><span data-stu-id="b531f-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="b531f-166">Evento GC</span><span class="sxs-lookup"><span data-stu-id="b531f-166">GC Event</span></span> |  <span data-ttu-id="b531f-167">Se produjo la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="b531f-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="b531f-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="b531f-168">DOMContentLoaded</span></span> |  <span data-ttu-id="b531f-169">El explorador despidió el evento [DOMContentLoaded.][MDNWindowDOMContentLoadedEvent]</span><span class="sxs-lookup"><span data-stu-id="b531f-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="b531f-170">Este evento se desencadena cuando se carga y analiza todo el contenido DOM de la página.</span><span class="sxs-lookup"><span data-stu-id="b531f-170">This event is fired when all of the DOM content of the page is loaded and parsed.</span></span> |  
| <span data-ttu-id="b531f-171">Evaluar script</span><span class="sxs-lookup"><span data-stu-id="b531f-171">Evaluate Script</span></span> | <span data-ttu-id="b531f-172">Se evaluó un script.</span><span class="sxs-lookup"><span data-stu-id="b531f-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="b531f-173">Evento</span><span class="sxs-lookup"><span data-stu-id="b531f-173">Event</span></span> | <span data-ttu-id="b531f-174">Un evento De JavaScript \(por ejemplo, `mousedown` o `key` \).</span><span class="sxs-lookup"><span data-stu-id="b531f-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="b531f-175">Llamada de función</span><span class="sxs-lookup"><span data-stu-id="b531f-175">Function Call</span></span> | <span data-ttu-id="b531f-176">Se realizó una llamada de función de JavaScript de nivel superior \(solo aparece cuando el explorador entra en el motor de JavaScript\).</span><span class="sxs-lookup"><span data-stu-id="b531f-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="b531f-177">Instalar temporizador</span><span class="sxs-lookup"><span data-stu-id="b531f-177">Install Timer</span></span> | <span data-ttu-id="b531f-178">Se creó un temporizador [con setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] o [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="b531f-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="b531f-179">Fotograma de animación de solicitud</span><span class="sxs-lookup"><span data-stu-id="b531f-179">Request Animation Frame</span></span> | <span data-ttu-id="b531f-180">Una `requestAnimationFrame()` llamada programó un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="b531f-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="b531f-181">Quitar temporizador</span><span class="sxs-lookup"><span data-stu-id="b531f-181">Remove Timer</span></span> | <span data-ttu-id="b531f-182">Se ha borrado un temporizador creado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b531f-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="b531f-183">Tiempo</span><span class="sxs-lookup"><span data-stu-id="b531f-183">Time</span></span> |  <span data-ttu-id="b531f-184">Un script denominado [console.time()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="b531f-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="b531f-185">Fin de la hora</span><span class="sxs-lookup"><span data-stu-id="b531f-185">Time End</span></span> | <span data-ttu-id="b531f-186">Un script denominado [console.timeEnd()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="b531f-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="b531f-187">Temporizador desencadenado</span><span class="sxs-lookup"><span data-stu-id="b531f-187">Timer Fired</span></span> | <span data-ttu-id="b531f-188">Temporizador desencadenado que estaba programado con `setInterval()` o `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="b531f-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="b531f-189">XHR Ready State Change</span><span class="sxs-lookup"><span data-stu-id="b531f-189">XHR Ready State Change</span></span> | <span data-ttu-id="b531f-190">Se ha cambiado el estado listo de un OBJETO XMLHTTPRequest.</span><span class="sxs-lookup"><span data-stu-id="b531f-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="b531f-191">Carga XHR</span><span class="sxs-lookup"><span data-stu-id="b531f-191">XHR Load</span></span> | <span data-ttu-id="b531f-192">Una `XMLHTTPRequest` carga finalizada.</span><span class="sxs-lookup"><span data-stu-id="b531f-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <a name="scripting-event-properties"></a><span data-ttu-id="b531f-193">Propiedades del evento Scripting</span><span class="sxs-lookup"><span data-stu-id="b531f-193">Scripting event properties</span></span>  

| <span data-ttu-id="b531f-194">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b531f-194">Property</span></span> | <span data-ttu-id="b531f-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-196">Id. del temporizador</span><span class="sxs-lookup"><span data-stu-id="b531f-196">Timer ID</span></span> | <span data-ttu-id="b531f-197">El identificador del temporizador.</span><span class="sxs-lookup"><span data-stu-id="b531f-197">The timer ID.</span></span> |  
| <span data-ttu-id="b531f-198">Tiempo de espera agotado</span><span class="sxs-lookup"><span data-stu-id="b531f-198">Timeout</span></span> | <span data-ttu-id="b531f-199">Tiempo de espera especificado por el temporizador.</span><span class="sxs-lookup"><span data-stu-id="b531f-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="b531f-200">Repeticiones</span><span class="sxs-lookup"><span data-stu-id="b531f-200">Repeats</span></span> | <span data-ttu-id="b531f-201">Boolean que especifica si el temporizador se repite.</span><span class="sxs-lookup"><span data-stu-id="b531f-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="b531f-202">Llamada de función</span><span class="sxs-lookup"><span data-stu-id="b531f-202">Function Call</span></span> | <span data-ttu-id="b531f-203">Función que se invocó.</span><span class="sxs-lookup"><span data-stu-id="b531f-203">A function that was invoked.</span></span> |  

## <a name="rendering-events"></a><span data-ttu-id="b531f-204">Eventos de representación</span><span class="sxs-lookup"><span data-stu-id="b531f-204">Rendering events</span></span>  

<span data-ttu-id="b531f-205">En esta sección se enumeran los eventos que pertenecen a la categoría Representación y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="b531f-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="b531f-206">Evento</span><span class="sxs-lookup"><span data-stu-id="b531f-206">Event</span></span> | <span data-ttu-id="b531f-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-208">Invalidar diseño</span><span class="sxs-lookup"><span data-stu-id="b531f-208">Invalidate layout</span></span> | <span data-ttu-id="b531f-209">El diseño de página se invalidó mediante un cambio de DOM.</span><span class="sxs-lookup"><span data-stu-id="b531f-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="b531f-210">Diseño</span><span class="sxs-lookup"><span data-stu-id="b531f-210">Layout</span></span> | <span data-ttu-id="b531f-211">Se completó un diseño de página.</span><span class="sxs-lookup"><span data-stu-id="b531f-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="b531f-212">Recalcular estilo</span><span class="sxs-lookup"><span data-stu-id="b531f-212">Recalculate style</span></span> | <span data-ttu-id="b531f-213">Microsoft Edge de elementos recalculados.</span><span class="sxs-lookup"><span data-stu-id="b531f-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="b531f-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="b531f-214">Scroll</span></span> | <span data-ttu-id="b531f-215">El contenido de la vista anidada se desplazó.</span><span class="sxs-lookup"><span data-stu-id="b531f-215">The content of nested view was scrolled.</span></span> |  

### <a name="rendering-event-properties"></a><span data-ttu-id="b531f-216">Propiedades de evento de representación</span><span class="sxs-lookup"><span data-stu-id="b531f-216">Rendering event properties</span></span>  

| <span data-ttu-id="b531f-217">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b531f-217">Property</span></span> | <span data-ttu-id="b531f-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-219">Diseño invalidado</span><span class="sxs-lookup"><span data-stu-id="b531f-219">Layout invalidated</span></span> | <span data-ttu-id="b531f-220">Para los registros de diseño, el seguimiento de pila del código que provocó la invalidación del diseño.</span><span class="sxs-lookup"><span data-stu-id="b531f-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="b531f-221">Nodos que necesitan diseño</span><span class="sxs-lookup"><span data-stu-id="b531f-221">Nodes that need layout</span></span> | <span data-ttu-id="b531f-222">Para los registros de diseño, el número de nodos que se marcaron como diseño necesario antes de que se iniciara el relayout.</span><span class="sxs-lookup"><span data-stu-id="b531f-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="b531f-223">Estos son normalmente los nodos que se invalidaron mediante código de desarrollador, además de una ruta hacia arriba para volver a la raíz de layout.</span><span class="sxs-lookup"><span data-stu-id="b531f-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="b531f-224">Tamaño del árbol de diseño</span><span class="sxs-lookup"><span data-stu-id="b531f-224">Layout tree size</span></span> | <span data-ttu-id="b531f-225">Para los registros layout, el número total de nodos bajo la raíz de relayout \(el nodo que Microsoft Edge inicia el relayout\).</span><span class="sxs-lookup"><span data-stu-id="b531f-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="b531f-226">Ámbito de diseño</span><span class="sxs-lookup"><span data-stu-id="b531f-226">Layout scope</span></span> | <span data-ttu-id="b531f-227">Los valores posibles `Partial` son \(el límite de nuevo diseño es una parte del DOM\) o `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="b531f-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="b531f-228">Elementos afectados</span><span class="sxs-lookup"><span data-stu-id="b531f-228">Elements affected</span></span> | <span data-ttu-id="b531f-229">Para volver a calcular los registros de estilo, el número de elementos afectados por una actualización de estilo.</span><span class="sxs-lookup"><span data-stu-id="b531f-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="b531f-230">Estilos invalidados</span><span class="sxs-lookup"><span data-stu-id="b531f-230">Styles invalidated</span></span> | <span data-ttu-id="b531f-231">Para volver a calcular los registros de estilo, proporciona el seguimiento de pila del código que provocó la invalidación del estilo.</span><span class="sxs-lookup"><span data-stu-id="b531f-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <a name="painting-events"></a><span data-ttu-id="b531f-232">Eventos de pintura</span><span class="sxs-lookup"><span data-stu-id="b531f-232">Painting events</span></span>  

<span data-ttu-id="b531f-233">En esta sección se enumeran los eventos que pertenecen a la categoría Painting y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="b531f-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="b531f-234">Evento</span><span class="sxs-lookup"><span data-stu-id="b531f-234">Event</span></span> | <span data-ttu-id="b531f-235">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-236">Capas compuestas</span><span class="sxs-lookup"><span data-stu-id="b531f-236">Composite Layers</span></span> | <span data-ttu-id="b531f-237">Las capas de imagen compuestas para el Microsoft Edge de representación.</span><span class="sxs-lookup"><span data-stu-id="b531f-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="b531f-238">Descodificación de imágenes</span><span class="sxs-lookup"><span data-stu-id="b531f-238">Image Decode</span></span> | <span data-ttu-id="b531f-239">Se descodificó un recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="b531f-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="b531f-240">Cambio de tamaño de imagen</span><span class="sxs-lookup"><span data-stu-id="b531f-240">Image Resize</span></span> | <span data-ttu-id="b531f-241">Se ha cambiado el tamaño de una imagen desde sus dimensiones nativas.</span><span class="sxs-lookup"><span data-stu-id="b531f-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="b531f-242">Paint</span><span class="sxs-lookup"><span data-stu-id="b531f-242">Paint</span></span> | <span data-ttu-id="b531f-243">Las capas compuestas se pintaron en una región de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b531f-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="b531f-244">Al pasar el mouse sobre Paint de datos se resalta la región de la pantalla que se actualizó.</span><span class="sxs-lookup"><span data-stu-id="b531f-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <a name="painting-event-properties"></a><span data-ttu-id="b531f-245">Propiedades del evento Painting</span><span class="sxs-lookup"><span data-stu-id="b531f-245">Painting event properties</span></span>  

| <span data-ttu-id="b531f-246">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b531f-246">Property</span></span> | <span data-ttu-id="b531f-247">Descripción</span><span class="sxs-lookup"><span data-stu-id="b531f-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b531f-248">Ubicación</span><span class="sxs-lookup"><span data-stu-id="b531f-248">Location</span></span> | <span data-ttu-id="b531f-249">Para Paint eventos, las coordenadas x e y del rectángulo de pintura.</span><span class="sxs-lookup"><span data-stu-id="b531f-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="b531f-250">Dimensiones</span><span class="sxs-lookup"><span data-stu-id="b531f-250">Dimensions</span></span> | <span data-ttu-id="b531f-251">Para Paint eventos, el alto y el ancho de la región pintada.</span><span class="sxs-lookup"><span data-stu-id="b531f-251">For Paint events, the height and width of the painted region.</span></span> |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b531f-252">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b531f-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time: Referencia de api de consola"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd: referencia de api de consola"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Ventana: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> <span data-ttu-id="b531f-258">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b531f-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b531f-259">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) y es creado por [Meggin Kearney][MegginKearney] \(Tech Writer\) y [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span><span class="sxs-lookup"><span data-stu-id="b531f-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b531f-261">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b531f-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors#flavio-copes  
