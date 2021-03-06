---
description: Referencia del protocolo DevTools versión 0.2 (EdgeHTML) para el dominio de página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.
title: 'Dominio de página: protocolo DevTools versión 0.2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398850"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="45045-104">Dominio de página: protocolo DevTools versión 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="45045-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="45045-105">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.</span><span class="sxs-lookup"><span data-stu-id="45045-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="45045-106">Clasificación</span><span class="sxs-lookup"><span data-stu-id="45045-106">Classification</span></span> | <span data-ttu-id="45045-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="45045-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="45045-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="45045-108">Methods</span></span>](#methods) | <span data-ttu-id="45045-109">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="45045-109">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |  
| [<span data-ttu-id="45045-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="45045-110">Events</span></span>](#events) | <span data-ttu-id="45045-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="45045-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |  
| [<span data-ttu-id="45045-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="45045-112">Types</span></span>](#types) | <span data-ttu-id="45045-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="45045-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |  

## <a name="methods"></a><span data-ttu-id="45045-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="45045-114">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="45045-115">habilitar</span><span class="sxs-lookup"><span data-stu-id="45045-115">enable</span></span>  

<span data-ttu-id="45045-116">Habilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="45045-116">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="45045-117">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="45045-117">disable</span></span>  

<span data-ttu-id="45045-118">Deshabilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="45045-118">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="45045-119">navegar</span><span class="sxs-lookup"><span data-stu-id="45045-119">navigate</span></span>  

<span data-ttu-id="45045-120">Navega a la página actual a la dirección URL determinada.</span><span class="sxs-lookup"><span data-stu-id="45045-120">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="45045-121">Parameters</span><span class="sxs-lookup"><span data-stu-id="45045-121">Parameters</span></span> | <span data-ttu-id="45045-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-122">Type</span></span> | <span data-ttu-id="45045-123">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-123">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-124">url</span><span class="sxs-lookup"><span data-stu-id="45045-124">url</span></span> | `string` | <span data-ttu-id="45045-125">DIRECCIÓN URL para navegar por la página.</span><span class="sxs-lookup"><span data-stu-id="45045-125">URL to navigate the page to.</span></span> |  
| <span data-ttu-id="45045-126">frameId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="45045-126">frameId \(optional\)</span></span> | [<span data-ttu-id="45045-127">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-127">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-128">Id. de marco para navegar.</span><span class="sxs-lookup"><span data-stu-id="45045-128">Frame id to navigate.</span></span>  <span data-ttu-id="45045-129">Si no se especifica, navegará por la página superior.</span><span class="sxs-lookup"><span data-stu-id="45045-129">If not specified, will navigate the top page.</span></span> |  

| <span data-ttu-id="45045-130">Devuelve</span><span class="sxs-lookup"><span data-stu-id="45045-130">Returns</span></span> | <span data-ttu-id="45045-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-131">Type</span></span> | <span data-ttu-id="45045-132">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-132">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-133">frameId</span><span class="sxs-lookup"><span data-stu-id="45045-133">frameId</span></span> | [<span data-ttu-id="45045-134">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-134">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-135">Identificador de marco que se navegará.</span><span class="sxs-lookup"><span data-stu-id="45045-135">Frame id that will be navigated.</span></span> |  

---  

### <a name="getframetree"></a><span data-ttu-id="45045-136">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="45045-136">getFrameTree</span></span>  

<span data-ttu-id="45045-137">Devuelve la estructura del árbol de marco actual.</span><span class="sxs-lookup"><span data-stu-id="45045-137">Returns present frame tree structure.</span></span>  

| <span data-ttu-id="45045-138">Devuelve</span><span class="sxs-lookup"><span data-stu-id="45045-138">Returns</span></span> | <span data-ttu-id="45045-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-139">Type</span></span> | <span data-ttu-id="45045-140">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-140">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-141">frameTree</span><span class="sxs-lookup"><span data-stu-id="45045-141">frameTree</span></span> | [<span data-ttu-id="45045-142">FrameTree</span><span class="sxs-lookup"><span data-stu-id="45045-142">FrameTree</span></span>](#frametree) | <span data-ttu-id="45045-143">Presentar estructura de árbol de marco.</span><span class="sxs-lookup"><span data-stu-id="45045-143">Present frame tree structure.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="45045-144">Eventos</span><span class="sxs-lookup"><span data-stu-id="45045-144">Events</span></span>  

### <a name="frameattached"></a><span data-ttu-id="45045-145">frameAttached</span><span class="sxs-lookup"><span data-stu-id="45045-145">frameAttached</span></span>  

<span data-ttu-id="45045-146">Se desencadena cuando el marco se ha unido a su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="45045-146">Fired when frame has been attached to its parent.</span></span>  

| <span data-ttu-id="45045-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="45045-147">Parameters</span></span> | <span data-ttu-id="45045-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-148">Type</span></span> | <span data-ttu-id="45045-149">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-149">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-150">frameId</span><span class="sxs-lookup"><span data-stu-id="45045-150">frameId</span></span> | [<span data-ttu-id="45045-151">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-151">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-152">Id. del marco que se ha adjuntado.</span><span class="sxs-lookup"><span data-stu-id="45045-152">Id of the frame that has been attached.</span></span> |  
| <span data-ttu-id="45045-153">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="45045-153">parentFrameId</span></span> | [<span data-ttu-id="45045-154">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-154">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-155">Identificador de fotograma primario.</span><span class="sxs-lookup"><span data-stu-id="45045-155">Parent frame identifier.</span></span> |  
| <span data-ttu-id="45045-156">stack \(optional\)</span><span class="sxs-lookup"><span data-stu-id="45045-156">stack \(optional\)</span></span> | [<span data-ttu-id="45045-157">Runtime.StackTrace</span><span class="sxs-lookup"><span data-stu-id="45045-157">Runtime.StackTrace</span></span>](./runtime.md#stacktrace) | <span data-ttu-id="45045-158">Seguimiento de pila de JavaScript de cuándo se adjunta el marco, solo se establece si el marco se inicia desde el script.</span><span class="sxs-lookup"><span data-stu-id="45045-158">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span> |  

---  

### <a name="framedetached"></a><span data-ttu-id="45045-159">frameDetached</span><span class="sxs-lookup"><span data-stu-id="45045-159">frameDetached</span></span>  

<span data-ttu-id="45045-160">Se desencadena cuando se ha desasociado el marco de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="45045-160">Fired when frame has been detached from its parent.</span></span>  

| <span data-ttu-id="45045-161">Parameters</span><span class="sxs-lookup"><span data-stu-id="45045-161">Parameters</span></span> | <span data-ttu-id="45045-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-162">Type</span></span> | <span data-ttu-id="45045-163">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-163">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-164">frameId</span><span class="sxs-lookup"><span data-stu-id="45045-164">frameId</span></span> | [<span data-ttu-id="45045-165">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-165">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-166">Identificador del marco que se ha desasociado.</span><span class="sxs-lookup"><span data-stu-id="45045-166">ID of the frame that has been detached.</span></span> |  

---  

### <a name="framenavigated"></a><span data-ttu-id="45045-167">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="45045-167">frameNavigated</span></span>  

<span data-ttu-id="45045-168">Se desencadena una vez completada la navegación del marco.</span><span class="sxs-lookup"><span data-stu-id="45045-168">Fired once navigation of the frame has completed.</span></span>  

| <span data-ttu-id="45045-169">Parameters</span><span class="sxs-lookup"><span data-stu-id="45045-169">Parameters</span></span> | <span data-ttu-id="45045-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-170">Type</span></span> | <span data-ttu-id="45045-171">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-171">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-172">marco</span><span class="sxs-lookup"><span data-stu-id="45045-172">frame</span></span> | [<span data-ttu-id="45045-173">Marco</span><span class="sxs-lookup"><span data-stu-id="45045-173">Frame</span></span>](#frame) | <span data-ttu-id="45045-174">Frame (objeto).</span><span class="sxs-lookup"><span data-stu-id="45045-174">Frame object.</span></span> |  

---  

### <a name="loadeventfired"></a><span data-ttu-id="45045-175">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="45045-175">loadEventFired</span></span>  

<span data-ttu-id="45045-176">Corresponde al `window.onload` evento.</span><span class="sxs-lookup"><span data-stu-id="45045-176">Corresponds to the `window.onload` event.</span></span>  

| <span data-ttu-id="45045-177">Parameters</span><span class="sxs-lookup"><span data-stu-id="45045-177">Parameters</span></span> | <span data-ttu-id="45045-178">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-178">Type</span></span> | <span data-ttu-id="45045-179">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-179">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-180">marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="45045-180">timestamp</span></span> | `number` | <span data-ttu-id="45045-181">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="45045-181">Number of milliseconds since epoch.</span></span> |  

---  

### <a name="domcontenteventfired"></a><span data-ttu-id="45045-182">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="45045-182">domContentEventFired</span></span>  

<span data-ttu-id="45045-183">Corresponde al `document.onDOMContentLoaded` evento.</span><span class="sxs-lookup"><span data-stu-id="45045-183">Corresponds to the `document.onDOMContentLoaded` event.</span></span>  

| <span data-ttu-id="45045-184">Parameters</span><span class="sxs-lookup"><span data-stu-id="45045-184">Parameters</span></span> | <span data-ttu-id="45045-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-185">Type</span></span> | <span data-ttu-id="45045-186">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-187">marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="45045-187">timestamp</span></span> | `number` | <span data-ttu-id="45045-188">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="45045-188">Number of milliseconds since epoch.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="45045-189">Tipos</span><span class="sxs-lookup"><span data-stu-id="45045-189">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="45045-190">Cadena FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-190">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="45045-191">Identificador de fotograma único.</span><span class="sxs-lookup"><span data-stu-id="45045-191">Unique frame identifier.</span></span>  

&nbsp;  

---  

### <a name="frame-object"></a><span data-ttu-id="45045-192">Frame (objeto)</span><span class="sxs-lookup"><span data-stu-id="45045-192">Frame object</span></span>  

<a name="frame"></a>  

<span data-ttu-id="45045-193">Información sobre el marco de la página.</span><span class="sxs-lookup"><span data-stu-id="45045-193">Information about the Frame on the Page.</span></span>  

| <span data-ttu-id="45045-194">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45045-194">Properties</span></span> | <span data-ttu-id="45045-195">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-195">Type</span></span> | <span data-ttu-id="45045-196">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-196">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-197">id</span><span class="sxs-lookup"><span data-stu-id="45045-197">id</span></span> | [<span data-ttu-id="45045-198">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-198">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-199">Identificador único de marco.</span><span class="sxs-lookup"><span data-stu-id="45045-199">Frame unique identifier.</span></span> |  
| <span data-ttu-id="45045-200">parentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="45045-200">parentId \(optional\)</span></span> | [<span data-ttu-id="45045-201">FrameId</span><span class="sxs-lookup"><span data-stu-id="45045-201">FrameId</span></span>](#frameid) | <span data-ttu-id="45045-202">Identificador único del marco primario.</span><span class="sxs-lookup"><span data-stu-id="45045-202">Parent frame unique identifier.</span></span> |  
| <span data-ttu-id="45045-203">nombre \(optional\)</span><span class="sxs-lookup"><span data-stu-id="45045-203">name \(optional\)</span></span> | `string` | <span data-ttu-id="45045-204">Nombre del marco tal como se especifica en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="45045-204">Frame's name as specified in the tag.</span></span> |  
| <span data-ttu-id="45045-205">url</span><span class="sxs-lookup"><span data-stu-id="45045-205">url</span></span> | `string` | <span data-ttu-id="45045-206">Dirección URL del documento de marco.</span><span class="sxs-lookup"><span data-stu-id="45045-206">Frame document's URL.</span></span> |  
| <span data-ttu-id="45045-207">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="45045-207">securityOrigin</span></span> | `string` | <span data-ttu-id="45045-208">Origen de seguridad del documento de marco.</span><span class="sxs-lookup"><span data-stu-id="45045-208">Frame document's security origin.</span></span> |  
| <span data-ttu-id="45045-209">mimeType</span><span class="sxs-lookup"><span data-stu-id="45045-209">mimeType</span></span> | `string` | <span data-ttu-id="45045-210">Frame mimeType del documento según lo determinado por el explorador.</span><span class="sxs-lookup"><span data-stu-id="45045-210">Frame document's mimeType as determined by the browser.</span></span> |  

---  

### <a name="frametree-object"></a><span data-ttu-id="45045-211">FrameTree (objeto)</span><span class="sxs-lookup"><span data-stu-id="45045-211">FrameTree object</span></span>  

<a name="frametree"></a>  

<span data-ttu-id="45045-212">Información sobre la jerarquía frame.</span><span class="sxs-lookup"><span data-stu-id="45045-212">Information about the Frame hierarchy.</span></span>  

| <span data-ttu-id="45045-213">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45045-213">Properties</span></span> | <span data-ttu-id="45045-214">Tipo</span><span class="sxs-lookup"><span data-stu-id="45045-214">Type</span></span> | <span data-ttu-id="45045-215">Detalles</span><span class="sxs-lookup"><span data-stu-id="45045-215">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="45045-216">marco</span><span class="sxs-lookup"><span data-stu-id="45045-216">frame</span></span> | [<span data-ttu-id="45045-217">Marco</span><span class="sxs-lookup"><span data-stu-id="45045-217">Frame</span></span>](#frame) | <span data-ttu-id="45045-218">Información de marco para este elemento de árbol.</span><span class="sxs-lookup"><span data-stu-id="45045-218">Frame information for this tree item.</span></span> |  
| <span data-ttu-id="45045-219">childFrames \(optional\)</span><span class="sxs-lookup"><span data-stu-id="45045-219">childFrames \(optional\)</span></span> | [<span data-ttu-id="45045-220">FrameTree[]</span><span class="sxs-lookup"><span data-stu-id="45045-220">FrameTree[]</span></span>](#frametree) | <span data-ttu-id="45045-221">Fotogramas secundarios.</span><span class="sxs-lookup"><span data-stu-id="45045-221">Child frames.</span></span> |  

---  
