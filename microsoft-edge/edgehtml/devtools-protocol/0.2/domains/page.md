---
description: DevTools Protocol versión 0,2 (EdgeHTML) Reference para el dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: DevTools Protocol versión 0,2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1849a2e2aa2f53cef9dff5d03ac991d368a6f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235963"
---
# <span data-ttu-id="8a258-104">Dominio de la página: DevTools Protocol versión 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="8a258-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="8a258-105">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.</span><span class="sxs-lookup"><span data-stu-id="8a258-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="8a258-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a258-106">Methods</span></span>**](#methods) | <span data-ttu-id="8a258-107">[Habilitar](#enable), [deshabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="8a258-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="8a258-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="8a258-108">Events</span></span>**](#events) | <span data-ttu-id="8a258-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="8a258-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="8a258-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="8a258-110">Types</span></span>**](#types) | <span data-ttu-id="8a258-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="8a258-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="8a258-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a258-112">Methods</span></span>

### <span data-ttu-id="8a258-113">habilitar</span><span class="sxs-lookup"><span data-stu-id="8a258-113">enable</span></span>
<span data-ttu-id="8a258-114">Habilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="8a258-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="8a258-115">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="8a258-115">disable</span></span>
<span data-ttu-id="8a258-116">Deshabilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="8a258-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="8a258-117">navegar</span><span class="sxs-lookup"><span data-stu-id="8a258-117">navigate</span></span>
<span data-ttu-id="8a258-118">Desplaza la página actual a la dirección URL dada.</span><span class="sxs-lookup"><span data-stu-id="8a258-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a258-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-120">url</span><span class="sxs-lookup"><span data-stu-id="8a258-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8a258-121">Dirección URL para navegar por la página.</span><span class="sxs-lookup"><span data-stu-id="8a258-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-122">frameId</span><span class="sxs-lookup"><span data-stu-id="8a258-122">frameId</span></span> <br/> <i><span data-ttu-id="8a258-123">opcional</span><span class="sxs-lookup"><span data-stu-id="8a258-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-124">Identificador de trama para navegar.</span><span class="sxs-lookup"><span data-stu-id="8a258-124">Frame id to navigate.</span></span> <span data-ttu-id="8a258-125">Si no se especifica, se desplazará por la página superior.</span><span class="sxs-lookup"><span data-stu-id="8a258-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-126">Devuelve</span><span class="sxs-lookup"><span data-stu-id="8a258-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-127">frameId</span><span class="sxs-lookup"><span data-stu-id="8a258-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-128">Identificador del fotograma en el que se va a navegar.</span><span class="sxs-lookup"><span data-stu-id="8a258-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="8a258-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="8a258-129">getFrameTree</span></span>
<span data-ttu-id="8a258-130">Devuelve la estructura de árbol de fotogramas actual.</span><span class="sxs-lookup"><span data-stu-id="8a258-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-131">Devuelve</span><span class="sxs-lookup"><span data-stu-id="8a258-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="8a258-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="8a258-133">Presentar estructura de árbol de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8a258-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="8a258-134">Eventos</span><span class="sxs-lookup"><span data-stu-id="8a258-134">Events</span></span>

### <span data-ttu-id="8a258-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="8a258-135">frameAttached</span></span>
<span data-ttu-id="8a258-136">Se desencadena cuando el marco se ha adjuntado a su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="8a258-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-137">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a258-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-138">frameId</span><span class="sxs-lookup"><span data-stu-id="8a258-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-139">Identificador de la trama que se ha adjuntado.</span><span class="sxs-lookup"><span data-stu-id="8a258-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="8a258-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-141">Identificador de marco primario.</span><span class="sxs-lookup"><span data-stu-id="8a258-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-142">apilable</span><span class="sxs-lookup"><span data-stu-id="8a258-142">stack</span></span> <br/> <i><span data-ttu-id="8a258-143">opcional</span><span class="sxs-lookup"><span data-stu-id="8a258-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="8a258-144">Seguimiento de la pila de JavaScript del momento en que se asoció el marco, establecido solo si el marco se inició desde el script.</span><span class="sxs-lookup"><span data-stu-id="8a258-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="8a258-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="8a258-145">frameDetached</span></span>
<span data-ttu-id="8a258-146">Se desencadena cuando se ha desvinculado el marco de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="8a258-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a258-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-148">frameId</span><span class="sxs-lookup"><span data-stu-id="8a258-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-149">Identificador de la trama que se ha desvinculado.</span><span class="sxs-lookup"><span data-stu-id="8a258-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="8a258-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="8a258-150">frameNavigated</span></span>
<span data-ttu-id="8a258-151">Se activa una vez que se ha completado la navegación del marco.</span><span class="sxs-lookup"><span data-stu-id="8a258-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-152">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a258-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-153">bastidor</span><span class="sxs-lookup"><span data-stu-id="8a258-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="8a258-154">Objeto Frame.</span><span class="sxs-lookup"><span data-stu-id="8a258-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="8a258-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="8a258-155">loadEventFired</span></span>
<span data-ttu-id="8a258-156">Corresponde al evento Window. onload.</span><span class="sxs-lookup"><span data-stu-id="8a258-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a258-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-158">marca</span><span class="sxs-lookup"><span data-stu-id="8a258-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="8a258-159">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="8a258-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="8a258-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="8a258-160">domContentEventFired</span></span>
<span data-ttu-id="8a258-161">Corresponde al evento document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="8a258-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a258-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-163">marca</span><span class="sxs-lookup"><span data-stu-id="8a258-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="8a258-164">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="8a258-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="8a258-165">Tipos</span><span class="sxs-lookup"><span data-stu-id="8a258-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="8a258-166">FrameId</span><span class="sxs-lookup"><span data-stu-id="8a258-166">FrameId</span></span> `string`

<span data-ttu-id="8a258-167">Identificador de trama único.</span><span class="sxs-lookup"><span data-stu-id="8a258-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="8a258-168">Marco</span><span class="sxs-lookup"><span data-stu-id="8a258-168">Frame</span></span> `object`

<span data-ttu-id="8a258-169">Información sobre el marco de la página.</span><span class="sxs-lookup"><span data-stu-id="8a258-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-170">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a258-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-171">id</span><span class="sxs-lookup"><span data-stu-id="8a258-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-172">Identificador único de marco.</span><span class="sxs-lookup"><span data-stu-id="8a258-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-173">parentId</span><span class="sxs-lookup"><span data-stu-id="8a258-173">parentId</span></span> <br/> <i><span data-ttu-id="8a258-174">opcional</span><span class="sxs-lookup"><span data-stu-id="8a258-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="8a258-175">Identificador único del marco primario.</span><span class="sxs-lookup"><span data-stu-id="8a258-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-176">name</span><span class="sxs-lookup"><span data-stu-id="8a258-176">name</span></span> <br/> <i><span data-ttu-id="8a258-177">opcional</span><span class="sxs-lookup"><span data-stu-id="8a258-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8a258-178">Nombre del marco según se especifica en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="8a258-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-179">url</span><span class="sxs-lookup"><span data-stu-id="8a258-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8a258-180">Dirección URL del documento de marco.</span><span class="sxs-lookup"><span data-stu-id="8a258-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="8a258-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8a258-182">Origen del documento de marco.</span><span class="sxs-lookup"><span data-stu-id="8a258-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-183">mimeType</span><span class="sxs-lookup"><span data-stu-id="8a258-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8a258-184">MIME del marco según lo determine el explorador.</span><span class="sxs-lookup"><span data-stu-id="8a258-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="8a258-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="8a258-185">FrameTree</span></span> `object`

<span data-ttu-id="8a258-186">Información sobre la jerarquía de Marcos.</span><span class="sxs-lookup"><span data-stu-id="8a258-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8a258-187">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a258-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8a258-188">bastidor</span><span class="sxs-lookup"><span data-stu-id="8a258-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="8a258-189">Información de fotograma para este elemento de árbol.</span><span class="sxs-lookup"><span data-stu-id="8a258-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8a258-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="8a258-190">childFrames</span></span> <br/> <i><span data-ttu-id="8a258-191">opcional</span><span class="sxs-lookup"><span data-stu-id="8a258-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="8a258-192">Marcos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8a258-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
