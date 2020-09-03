---
description: El modo eventos de escala de tiempo muestra todos los eventos desencadenados mientras se realiza una grabación.  Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.
title: Referencia de evento de línea de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 624035636e2231cf1f3cd1e2ba0fdda7e2e4fa00
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992851"
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





# <span data-ttu-id="f8311-105">Referencia de evento de línea de tiempo</span><span class="sxs-lookup"><span data-stu-id="f8311-105">Timeline Event Reference</span></span>   




<span data-ttu-id="f8311-106">El modo eventos de escala de tiempo muestra todos los eventos desencadenados mientras se realiza una grabación.</span><span class="sxs-lookup"><span data-stu-id="f8311-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="f8311-107">Use la referencia de evento de escala de tiempo para obtener más información sobre cada tipo de evento de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f8311-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="f8311-108">Propiedades de evento de escala de tiempo comunes</span><span class="sxs-lookup"><span data-stu-id="f8311-108">Common timeline event properties</span></span>  

<span data-ttu-id="f8311-109">Algunos detalles están presentes en eventos de todos los tipos, mientras que algunos solo se aplican a determinados tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8311-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="f8311-110">En esta sección se enumeran las propiedades comunes a los distintos tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8311-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="f8311-111">Las propiedades específicas de determinados tipos de eventos se muestran en las referencias de los siguientes tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8311-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="f8311-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8311-112">Property</span></span> | <span data-ttu-id="f8311-113">¿Cuándo se muestra?</span><span class="sxs-lookup"><span data-stu-id="f8311-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-114">Tiempo agregado</span><span class="sxs-lookup"><span data-stu-id="f8311-114">Aggregated time</span></span> | <span data-ttu-id="f8311-115">Para eventos con **eventos anidados**, el tiempo que toma cada categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8311-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="f8311-116">Pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="f8311-116">Call Stack</span></span> | <span data-ttu-id="f8311-117">Para eventos con **eventos secundarios**, el tiempo que toma cada categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8311-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="f8311-118">Tiempo de CPU</span><span class="sxs-lookup"><span data-stu-id="f8311-118">CPU time</span></span> | <span data-ttu-id="f8311-119">La cantidad de tiempo de CPU que tomó el evento registrado.</span><span class="sxs-lookup"><span data-stu-id="f8311-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="f8311-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="f8311-120">Details</span></span> | <span data-ttu-id="f8311-121">Otros detalles sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="f8311-121">Other details about the event.</span></span> |  
| <span data-ttu-id="f8311-122">Duration \ (en la marca de hora \)</span><span class="sxs-lookup"><span data-stu-id="f8311-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="f8311-123">Cuánto tiempo duró el evento con todos sus elementos secundarios para completar. TIMESTAMP es la hora en que se produjo el evento, en relación con la grabación iniciada.</span><span class="sxs-lookup"><span data-stu-id="f8311-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="f8311-124">Tiempo propio</span><span class="sxs-lookup"><span data-stu-id="f8311-124">Self time</span></span> | <span data-ttu-id="f8311-125">Cuánto tiempo lleva el evento sin ninguno de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f8311-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="f8311-126">Tamaño de montón usado</span><span class="sxs-lookup"><span data-stu-id="f8311-126">Used Heap Size</span></span> | <span data-ttu-id="f8311-127">Cantidad de memoria usada por la aplicación cuando se registró el evento y el cambio Delta \ (+/-\) en el tamaño de montón usado desde el último muestreo.</span><span class="sxs-lookup"><span data-stu-id="f8311-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="f8311-128">Cargando eventos</span><span class="sxs-lookup"><span data-stu-id="f8311-128">Loading events</span></span>  

<span data-ttu-id="f8311-129">En esta sección se enumeran los eventos que pertenecen a la categoría de carga y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8311-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="f8311-130">Evento</span><span class="sxs-lookup"><span data-stu-id="f8311-130">Event</span></span> | <span data-ttu-id="f8311-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-132">Analizar HTML</span><span class="sxs-lookup"><span data-stu-id="f8311-132">Parse HTML</span></span> |  <span data-ttu-id="f8311-133">Microsoft Edge ejecutó el algoritmo de análisis HTML.</span><span class="sxs-lookup"><span data-stu-id="f8311-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="f8311-134">Finalizar la carga</span><span class="sxs-lookup"><span data-stu-id="f8311-134">Finish Loading</span></span> |  <span data-ttu-id="f8311-135">Una solicitud de red completada.</span><span class="sxs-lookup"><span data-stu-id="f8311-135">A network request completed.</span></span> |  
| <span data-ttu-id="f8311-136">Recibir datos</span><span class="sxs-lookup"><span data-stu-id="f8311-136">Receive Data</span></span> |  <span data-ttu-id="f8311-137">Se recibieron datos para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8311-137">Data for a request was received.</span></span>  <span data-ttu-id="f8311-138">Hay uno o más eventos de datos de recepción.</span><span class="sxs-lookup"><span data-stu-id="f8311-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="f8311-139">Recibir respuesta</span><span class="sxs-lookup"><span data-stu-id="f8311-139">Receive Response</span></span> |  <span data-ttu-id="f8311-140">La respuesta HTTP inicial de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8311-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="f8311-141">Enviar solicitud</span><span class="sxs-lookup"><span data-stu-id="f8311-141">Send Request</span></span> |  <span data-ttu-id="f8311-142">Se ha enviado una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="f8311-142">A network request has been sent.</span></span> |  

### <span data-ttu-id="f8311-143">Cargando propiedades de evento</span><span class="sxs-lookup"><span data-stu-id="f8311-143">Loading event properties</span></span>  

| <span data-ttu-id="f8311-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8311-144">Property</span></span> | <span data-ttu-id="f8311-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-146">Recurso</span><span class="sxs-lookup"><span data-stu-id="f8311-146">Resource</span></span> | <span data-ttu-id="f8311-147">Dirección URL del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="f8311-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="f8311-148">Vista previa</span><span class="sxs-lookup"><span data-stu-id="f8311-148">Preview</span></span> | <span data-ttu-id="f8311-149">Vista previa del recurso solicitado \ (solo imágenes \).</span><span class="sxs-lookup"><span data-stu-id="f8311-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="f8311-150">Método de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8311-150">Request Method</span></span> | <span data-ttu-id="f8311-151">Método HTTP usado para la solicitud \ ( `GET` o `POST` , por ejemplo, \).</span><span class="sxs-lookup"><span data-stu-id="f8311-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="f8311-152">Código de estado</span><span class="sxs-lookup"><span data-stu-id="f8311-152">Status Code</span></span> | <span data-ttu-id="f8311-153">Código de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8311-153">HTTP response code.</span></span> |  
| <span data-ttu-id="f8311-154">Tipo MIME</span><span class="sxs-lookup"><span data-stu-id="f8311-154">MIME Type</span></span> | <span data-ttu-id="f8311-155">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="f8311-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="f8311-156">Longitud de datos codificados</span><span class="sxs-lookup"><span data-stu-id="f8311-156">Encoded Data Length</span></span> | <span data-ttu-id="f8311-157">Longitud del recurso solicitado en bytes.</span><span class="sxs-lookup"><span data-stu-id="f8311-157">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="f8311-158">Eventos de scripting</span><span class="sxs-lookup"><span data-stu-id="f8311-158">Scripting events</span></span>  

<span data-ttu-id="f8311-159">En esta sección se enumeran los eventos que pertenecen a la categoría de scripting y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8311-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="f8311-160">Evento</span><span class="sxs-lookup"><span data-stu-id="f8311-160">Event</span></span> | <span data-ttu-id="f8311-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-162">Marco de animación desencadenado</span><span class="sxs-lookup"><span data-stu-id="f8311-162">Animation Frame Fired</span></span> | <span data-ttu-id="f8311-163">Se activó un marco de animación programada y se llamará a su controlador de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f8311-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="f8311-164">Cancelar marco de animación</span><span class="sxs-lookup"><span data-stu-id="f8311-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="f8311-165">Se ha cancelado un marco de animación programado.</span><span class="sxs-lookup"><span data-stu-id="f8311-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="f8311-166">Evento GC</span><span class="sxs-lookup"><span data-stu-id="f8311-166">GC Event</span></span> |  <span data-ttu-id="f8311-167">Se realizó la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="f8311-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="f8311-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="f8311-168">DOMContentLoaded</span></span> |  <span data-ttu-id="f8311-169">El [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] fue desencadenado por el explorador.</span><span class="sxs-lookup"><span data-stu-id="f8311-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="f8311-170">Este evento se desencadena cuando todo el contenido de DOM de la página se ha cargado y analizado.</span><span class="sxs-lookup"><span data-stu-id="f8311-170">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="f8311-171">Evaluar script</span><span class="sxs-lookup"><span data-stu-id="f8311-171">Evaluate Script</span></span> | <span data-ttu-id="f8311-172">Se evaluó un script.</span><span class="sxs-lookup"><span data-stu-id="f8311-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="f8311-173">Evento</span><span class="sxs-lookup"><span data-stu-id="f8311-173">Event</span></span> | <span data-ttu-id="f8311-174">Un evento de JavaScript \ (por ejemplo, `mousedown` , o `key` \).</span><span class="sxs-lookup"><span data-stu-id="f8311-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="f8311-175">Llamada de función</span><span class="sxs-lookup"><span data-stu-id="f8311-175">Function Call</span></span> | <span data-ttu-id="f8311-176">Se realizó una llamada de función de JavaScript de nivel superior \ (solo aparece cuando el explorador escribe el motor de JavaScript \).</span><span class="sxs-lookup"><span data-stu-id="f8311-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="f8311-177">Instalar cronómetro</span><span class="sxs-lookup"><span data-stu-id="f8311-177">Install Timer</span></span> | <span data-ttu-id="f8311-178">Se creó un temporizador con [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] o [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="f8311-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="f8311-179">Marco de animación de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8311-179">Request Animation Frame</span></span> | <span data-ttu-id="f8311-180">Una `requestAnimationFrame()` llamada programó un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="f8311-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="f8311-181">Quitar cronómetro</span><span class="sxs-lookup"><span data-stu-id="f8311-181">Remove Timer</span></span> | <span data-ttu-id="f8311-182">Se borró un temporizador creado previamente.</span><span class="sxs-lookup"><span data-stu-id="f8311-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="f8311-183">Tiempo</span><span class="sxs-lookup"><span data-stu-id="f8311-183">Time</span></span> |  <span data-ttu-id="f8311-184">Un script denominado [Console. Time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="f8311-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="f8311-185">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="f8311-185">Time End</span></span> | <span data-ttu-id="f8311-186">Un script denominado [Console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="f8311-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="f8311-187">Cronómetro desencadenado</span><span class="sxs-lookup"><span data-stu-id="f8311-187">Timer Fired</span></span> | <span data-ttu-id="f8311-188">Un temporizador desencadenado que se programó con `setInterval()` o `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="f8311-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="f8311-189">Cambio de estado de XHR listo</span><span class="sxs-lookup"><span data-stu-id="f8311-189">XHR Ready State Change</span></span> | <span data-ttu-id="f8311-190">El estado de lista de un XMLHTTPRequest ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f8311-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="f8311-191">Carga de XHR</span><span class="sxs-lookup"><span data-stu-id="f8311-191">XHR Load</span></span> | <span data-ttu-id="f8311-192">`XMLHTTPRequest`Finalizó la carga.</span><span class="sxs-lookup"><span data-stu-id="f8311-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="f8311-193">Propiedades de eventos de scripting</span><span class="sxs-lookup"><span data-stu-id="f8311-193">Scripting event properties</span></span>  

| <span data-ttu-id="f8311-194">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8311-194">Property</span></span> | <span data-ttu-id="f8311-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-196">IDENTIFICADOR del temporizador</span><span class="sxs-lookup"><span data-stu-id="f8311-196">Timer ID</span></span> | <span data-ttu-id="f8311-197">IDENTIFICADOR del temporizador.</span><span class="sxs-lookup"><span data-stu-id="f8311-197">The timer ID.</span></span> |  
| <span data-ttu-id="f8311-198">Tiempo de espera agotado</span><span class="sxs-lookup"><span data-stu-id="f8311-198">Timeout</span></span> | <span data-ttu-id="f8311-199">El tiempo de espera especificado por el temporizador.</span><span class="sxs-lookup"><span data-stu-id="f8311-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="f8311-200">Repite</span><span class="sxs-lookup"><span data-stu-id="f8311-200">Repeats</span></span> | <span data-ttu-id="f8311-201">Valor booleano que especifica si el temporizador se repite.</span><span class="sxs-lookup"><span data-stu-id="f8311-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="f8311-202">Llamada de función</span><span class="sxs-lookup"><span data-stu-id="f8311-202">Function Call</span></span> | <span data-ttu-id="f8311-203">Una función que se invocó.</span><span class="sxs-lookup"><span data-stu-id="f8311-203">A function that was invoked.</span></span> |  

## <span data-ttu-id="f8311-204">Representar eventos</span><span class="sxs-lookup"><span data-stu-id="f8311-204">Rendering events</span></span>  

<span data-ttu-id="f8311-205">En esta sección se enumeran los eventos que pertenecen a la categoría de representación y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8311-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="f8311-206">Evento</span><span class="sxs-lookup"><span data-stu-id="f8311-206">Event</span></span> | <span data-ttu-id="f8311-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-208">Invalidar diseño</span><span class="sxs-lookup"><span data-stu-id="f8311-208">Invalidate layout</span></span> | <span data-ttu-id="f8311-209">Un cambio de DOM invalidó el diseño de página.</span><span class="sxs-lookup"><span data-stu-id="f8311-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="f8311-210">Diseño</span><span class="sxs-lookup"><span data-stu-id="f8311-210">Layout</span></span> | <span data-ttu-id="f8311-211">Se completó un diseño de página.</span><span class="sxs-lookup"><span data-stu-id="f8311-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="f8311-212">Recalcular estilo</span><span class="sxs-lookup"><span data-stu-id="f8311-212">Recalculate style</span></span> | <span data-ttu-id="f8311-213">Estilos de elemento recalculado de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f8311-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="f8311-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="f8311-214">Scroll</span></span> | <span data-ttu-id="f8311-215">Se ha desplazado el contenido de la vista anidada.</span><span class="sxs-lookup"><span data-stu-id="f8311-215">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="f8311-216">Representación de propiedades de eventos</span><span class="sxs-lookup"><span data-stu-id="f8311-216">Rendering event properties</span></span>  

| <span data-ttu-id="f8311-217">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8311-217">Property</span></span> | <span data-ttu-id="f8311-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-219">Diseño invalidado</span><span class="sxs-lookup"><span data-stu-id="f8311-219">Layout invalidated</span></span> | <span data-ttu-id="f8311-220">En los registros de diseño, el seguimiento de la pila del código que causó que se invalidara el diseño.</span><span class="sxs-lookup"><span data-stu-id="f8311-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="f8311-221">Nodos que necesitan diseño</span><span class="sxs-lookup"><span data-stu-id="f8311-221">Nodes that need layout</span></span> | <span data-ttu-id="f8311-222">En los registros de diseño, el número de nodos que se han marcado como que necesitan diseño antes de que se inicie el redistribución.</span><span class="sxs-lookup"><span data-stu-id="f8311-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="f8311-223">Suelen ser aquellos nodos que el código del desarrollador invalidó, además de una ruta de acceso ascendente para rediseñar la raíz.</span><span class="sxs-lookup"><span data-stu-id="f8311-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="f8311-224">Tamaño del árbol de diseño</span><span class="sxs-lookup"><span data-stu-id="f8311-224">Layout tree size</span></span> | <span data-ttu-id="f8311-225">En los registros de diseño, el número total de nodos en la raíz de redistribución \ (el nodo en el que Microsoft Edge inicia el rediseño \).</span><span class="sxs-lookup"><span data-stu-id="f8311-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="f8311-226">Ámbito de diseño</span><span class="sxs-lookup"><span data-stu-id="f8311-226">Layout scope</span></span> | <span data-ttu-id="f8311-227">Los valores posibles son `Partial` \ (el límite de redistribución es una parte del DOM \) o `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="f8311-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="f8311-228">Elementos afectados</span><span class="sxs-lookup"><span data-stu-id="f8311-228">Elements affected</span></span> | <span data-ttu-id="f8311-229">Para volver a calcular los registros de estilo, el número de elementos afectados por un nuevo cálculo de estilo.</span><span class="sxs-lookup"><span data-stu-id="f8311-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="f8311-230">Estilos invalidados</span><span class="sxs-lookup"><span data-stu-id="f8311-230">Styles invalidated</span></span> | <span data-ttu-id="f8311-231">Para recalcular los registros de estilo, proporciona el seguimiento de pila del código que causó la invalidación de estilo.</span><span class="sxs-lookup"><span data-stu-id="f8311-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="f8311-232">Eventos de pintura</span><span class="sxs-lookup"><span data-stu-id="f8311-232">Painting events</span></span>  

<span data-ttu-id="f8311-233">En esta sección se enumeran los eventos que pertenecen a la categoría de pintura y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8311-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="f8311-234">Evento</span><span class="sxs-lookup"><span data-stu-id="f8311-234">Event</span></span> | <span data-ttu-id="f8311-235">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-236">Capas compuestas</span><span class="sxs-lookup"><span data-stu-id="f8311-236">Composite Layers</span></span> | <span data-ttu-id="f8311-237">Las capas de imagen compuestas para el motor de representación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f8311-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="f8311-238">Descodificación de imagen</span><span class="sxs-lookup"><span data-stu-id="f8311-238">Image Decode</span></span> | <span data-ttu-id="f8311-239">Se ha descodificado un recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="f8311-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="f8311-240">Cambiar el tamaño de la imagen</span><span class="sxs-lookup"><span data-stu-id="f8311-240">Image Resize</span></span> | <span data-ttu-id="f8311-241">Se ha cambiado el tamaño de una imagen desde sus dimensiones nativas.</span><span class="sxs-lookup"><span data-stu-id="f8311-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="f8311-242">Paint</span><span class="sxs-lookup"><span data-stu-id="f8311-242">Paint</span></span> | <span data-ttu-id="f8311-243">Las capas compuestas se han pintado en una región de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f8311-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="f8311-244">Al mantener el puntero sobre un registro de pintura, se resalta la región de la pantalla que se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="f8311-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="f8311-245">Propiedades de evento de dibujo</span><span class="sxs-lookup"><span data-stu-id="f8311-245">Painting event properties</span></span>  

| <span data-ttu-id="f8311-246">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8311-246">Property</span></span> | <span data-ttu-id="f8311-247">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8311-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f8311-248">Ubicación</span><span class="sxs-lookup"><span data-stu-id="f8311-248">Location</span></span> | <span data-ttu-id="f8311-249">Para eventos de pintura, las coordenadas x e y del rectángulo de pintura.</span><span class="sxs-lookup"><span data-stu-id="f8311-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="f8311-250">Dimensiones</span><span class="sxs-lookup"><span data-stu-id="f8311-250">Dimensions</span></span> | <span data-ttu-id="f8311-251">Para eventos de pintura, el alto y el ancho de la región pintada.</span><span class="sxs-lookup"><span data-stu-id="f8311-251">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Referencia de la API de consola de hora"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd: referencia de la API de consola"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Ventana: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="f8311-257">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8311-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f8311-258">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Flavio Copes][FlavioCopes] \ (desarrollador de pila completa \).</span><span class="sxs-lookup"><span data-stu-id="f8311-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f8311-260">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8311-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
