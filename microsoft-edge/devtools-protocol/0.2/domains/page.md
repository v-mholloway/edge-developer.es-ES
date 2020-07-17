---
description: Referencia del dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: DevTools Protocol versión 0,2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 864515eefbcb809e280f2ab1d81015018272c398
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882845"
---
# <span data-ttu-id="de1ba-104">Dominio de la página: DevTools Protocol versión 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="de1ba-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="de1ba-105">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.</span><span class="sxs-lookup"><span data-stu-id="de1ba-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="de1ba-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="de1ba-106">Methods</span></span>**](#methods) | <span data-ttu-id="de1ba-107">[Habilitar](#enable), [deshabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="de1ba-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="de1ba-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="de1ba-108">Events</span></span>**](#events) | <span data-ttu-id="de1ba-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="de1ba-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="de1ba-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="de1ba-110">Types</span></span>**](#types) | <span data-ttu-id="de1ba-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="de1ba-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="de1ba-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="de1ba-112">Methods</span></span>

### <span data-ttu-id="de1ba-113">habilitar</span><span class="sxs-lookup"><span data-stu-id="de1ba-113">enable</span></span>
<span data-ttu-id="de1ba-114">Habilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="de1ba-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="de1ba-115">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="de1ba-115">disable</span></span>
<span data-ttu-id="de1ba-116">Deshabilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="de1ba-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="de1ba-117">navegar</span><span class="sxs-lookup"><span data-stu-id="de1ba-117">navigate</span></span>
<span data-ttu-id="de1ba-118">Desplaza la página actual a la dirección URL dada.</span><span class="sxs-lookup"><span data-stu-id="de1ba-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="de1ba-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-120">url</span><span class="sxs-lookup"><span data-stu-id="de1ba-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="de1ba-121">Dirección URL para navegar por la página.</span><span class="sxs-lookup"><span data-stu-id="de1ba-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-122">frameId</span><span class="sxs-lookup"><span data-stu-id="de1ba-122">frameId</span></span> <br/> <i><span data-ttu-id="de1ba-123">opcional</span><span class="sxs-lookup"><span data-stu-id="de1ba-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-124">Identificador de trama para navegar.</span><span class="sxs-lookup"><span data-stu-id="de1ba-124">Frame id to navigate.</span></span> <span data-ttu-id="de1ba-125">Si no se especifica, se desplazará por la página superior.</span><span class="sxs-lookup"><span data-stu-id="de1ba-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-126">Devuelve</span><span class="sxs-lookup"><span data-stu-id="de1ba-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-127">frameId</span><span class="sxs-lookup"><span data-stu-id="de1ba-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-128">Identificador del fotograma en el que se va a navegar.</span><span class="sxs-lookup"><span data-stu-id="de1ba-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="de1ba-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="de1ba-129">getFrameTree</span></span>
<span data-ttu-id="de1ba-130">Devuelve la estructura de árbol de fotogramas actual.</span><span class="sxs-lookup"><span data-stu-id="de1ba-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-131">Devuelve</span><span class="sxs-lookup"><span data-stu-id="de1ba-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="de1ba-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="de1ba-133">Presentar estructura de árbol de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="de1ba-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="de1ba-134">Eventos</span><span class="sxs-lookup"><span data-stu-id="de1ba-134">Events</span></span>

### <span data-ttu-id="de1ba-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="de1ba-135">frameAttached</span></span>
<span data-ttu-id="de1ba-136">Se desencadena cuando el marco se ha adjuntado a su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="de1ba-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-137">Parameters</span><span class="sxs-lookup"><span data-stu-id="de1ba-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-138">frameId</span><span class="sxs-lookup"><span data-stu-id="de1ba-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-139">Identificador de la trama que se ha adjuntado.</span><span class="sxs-lookup"><span data-stu-id="de1ba-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="de1ba-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-141">Identificador de marco primario.</span><span class="sxs-lookup"><span data-stu-id="de1ba-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-142">apilable</span><span class="sxs-lookup"><span data-stu-id="de1ba-142">stack</span></span> <br/> <i><span data-ttu-id="de1ba-143">opcional</span><span class="sxs-lookup"><span data-stu-id="de1ba-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="de1ba-144">Seguimiento de la pila de JavaScript del momento en que se asoció el marco, establecido solo si el marco se inició desde el script.</span><span class="sxs-lookup"><span data-stu-id="de1ba-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="de1ba-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="de1ba-145">frameDetached</span></span>
<span data-ttu-id="de1ba-146">Se desencadena cuando se ha desvinculado el marco de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="de1ba-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="de1ba-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-148">frameId</span><span class="sxs-lookup"><span data-stu-id="de1ba-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-149">Identificador de la trama que se ha desvinculado.</span><span class="sxs-lookup"><span data-stu-id="de1ba-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="de1ba-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="de1ba-150">frameNavigated</span></span>
<span data-ttu-id="de1ba-151">Se activa una vez que se ha completado la navegación del marco.</span><span class="sxs-lookup"><span data-stu-id="de1ba-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-152">Parameters</span><span class="sxs-lookup"><span data-stu-id="de1ba-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-153">bastidor</span><span class="sxs-lookup"><span data-stu-id="de1ba-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="de1ba-154">Objeto Frame.</span><span class="sxs-lookup"><span data-stu-id="de1ba-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="de1ba-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="de1ba-155">loadEventFired</span></span>
<span data-ttu-id="de1ba-156">Corresponde al evento Window. onload.</span><span class="sxs-lookup"><span data-stu-id="de1ba-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="de1ba-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-158">marca</span><span class="sxs-lookup"><span data-stu-id="de1ba-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="de1ba-159">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="de1ba-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="de1ba-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="de1ba-160">domContentEventFired</span></span>
<span data-ttu-id="de1ba-161">Corresponde al evento document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="de1ba-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="de1ba-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-163">marca</span><span class="sxs-lookup"><span data-stu-id="de1ba-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="de1ba-164">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="de1ba-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="de1ba-165">Tipos</span><span class="sxs-lookup"><span data-stu-id="de1ba-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="de1ba-166">FrameId</span><span class="sxs-lookup"><span data-stu-id="de1ba-166">FrameId</span></span> `string`

<span data-ttu-id="de1ba-167">Identificador de trama único.</span><span class="sxs-lookup"><span data-stu-id="de1ba-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="de1ba-168">Marco</span><span class="sxs-lookup"><span data-stu-id="de1ba-168">Frame</span></span> `object`

<span data-ttu-id="de1ba-169">Información sobre el marco de la página.</span><span class="sxs-lookup"><span data-stu-id="de1ba-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-170">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de1ba-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-171">id</span><span class="sxs-lookup"><span data-stu-id="de1ba-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-172">Identificador único de marco.</span><span class="sxs-lookup"><span data-stu-id="de1ba-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-173">parentId</span><span class="sxs-lookup"><span data-stu-id="de1ba-173">parentId</span></span> <br/> <i><span data-ttu-id="de1ba-174">opcional</span><span class="sxs-lookup"><span data-stu-id="de1ba-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="de1ba-175">Identificador único del marco primario.</span><span class="sxs-lookup"><span data-stu-id="de1ba-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-176">name</span><span class="sxs-lookup"><span data-stu-id="de1ba-176">name</span></span> <br/> <i><span data-ttu-id="de1ba-177">opcional</span><span class="sxs-lookup"><span data-stu-id="de1ba-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="de1ba-178">Nombre del marco según se especifica en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="de1ba-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-179">url</span><span class="sxs-lookup"><span data-stu-id="de1ba-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="de1ba-180">Dirección URL del documento de marco.</span><span class="sxs-lookup"><span data-stu-id="de1ba-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="de1ba-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="de1ba-182">Origen del documento de marco.</span><span class="sxs-lookup"><span data-stu-id="de1ba-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-183">mimeType</span><span class="sxs-lookup"><span data-stu-id="de1ba-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="de1ba-184">MIME del marco según lo determine el explorador.</span><span class="sxs-lookup"><span data-stu-id="de1ba-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="de1ba-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="de1ba-185">FrameTree</span></span> `object`

<span data-ttu-id="de1ba-186">Información sobre la jerarquía de Marcos.</span><span class="sxs-lookup"><span data-stu-id="de1ba-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="de1ba-187">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de1ba-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="de1ba-188">bastidor</span><span class="sxs-lookup"><span data-stu-id="de1ba-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="de1ba-189">Información de fotograma para este elemento de árbol.</span><span class="sxs-lookup"><span data-stu-id="de1ba-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="de1ba-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="de1ba-190">childFrames</span></span> <br/> <i><span data-ttu-id="de1ba-191">opcional</span><span class="sxs-lookup"><span data-stu-id="de1ba-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="de1ba-192">Marcos secundarios.</span><span class="sxs-lookup"><span data-stu-id="de1ba-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
