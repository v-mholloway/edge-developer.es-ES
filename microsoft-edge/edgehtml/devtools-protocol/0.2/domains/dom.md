---
description: Referencia del dominio DOM. Este dominio expone las operaciones de lectura y escritura de DOM. Cada nodo DOM se representa con su objeto reflejado que tiene una `id` . Esto `id` se puede usar para obtener información adicional sobre el nodo, resolverlo en el contenedor de objetos de JavaScript, etc. Es importante que el cliente reciba eventos DOM solo para los nodos que son conocidos para el cliente. El back-end realiza un seguimiento de los nodos que se enviaron al cliente y nunca envía dos veces el mismo nodo. Es responsabilidad del cliente recopilar información acerca de los nodos que se enviaron al cliente.<p>Tenga en cuenta que `iframe` los elementos propietarios devolverán los elementos del documento correspondientes como sus nodos secundarios.</p>
title: 'Dominio DOM: DevTools Protocol versión 0,2'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236342"
---
# <span data-ttu-id="b54b2-109">DOM</span><span class="sxs-lookup"><span data-stu-id="b54b2-109">DOM</span></span>

<span data-ttu-id="b54b2-110">Este dominio expone las operaciones de lectura y escritura de DOM.</span><span class="sxs-lookup"><span data-stu-id="b54b2-110">This domain exposes DOM read/write operations.</span></span> <span data-ttu-id="b54b2-111">Cada nodo DOM se representa con su objeto reflejado que tiene una `id` .</span><span class="sxs-lookup"><span data-stu-id="b54b2-111">Each DOM Node is represented with its mirror object that has an `id`.</span></span> <span data-ttu-id="b54b2-112">Esto `id` se puede usar para obtener información adicional sobre el nodo, resolverlo en el contenedor de objetos de JavaScript, etc. Es importante que el cliente reciba eventos DOM solo para los nodos que son conocidos para el cliente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-112">This `id` can be used to get additional information on the Node, resolve it into the JavaScript object wrapper, etc. It is important that client receives DOM events only for the nodes that are known to the client.</span></span> <span data-ttu-id="b54b2-113">El back-end realiza un seguimiento de los nodos que se enviaron al cliente y nunca envía dos veces el mismo nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-113">Backend keeps track of the nodes that were sent to the client and never sends the same node twice.</span></span> <span data-ttu-id="b54b2-114">Es responsabilidad del cliente recopilar información acerca de los nodos que se enviaron al cliente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-114">It is client's responsibility to collect information about the nodes that were sent to the client.</span></span><p><span data-ttu-id="b54b2-115">Tenga en cuenta que `iframe` los elementos propietarios devolverán los elementos del documento correspondientes como sus nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b54b2-115">Note that `iframe` owner elements will return corresponding document elements as their child nodes.</span></span></p>

| | |
|-|-|
| [**<span data-ttu-id="b54b2-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="b54b2-116">Methods</span></span>**](#methods) | <span data-ttu-id="b54b2-117">[enable](#enable), [Disable](#disable), [getdocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), requestNode, [](#setinspectednode) [resolveNode](#requestnode) [, setInspectedNode](#resolvenode)</span><span class="sxs-lookup"><span data-stu-id="b54b2-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span></span> |
| [**<span data-ttu-id="b54b2-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="b54b2-118">Events</span></span>**](#events) | <span data-ttu-id="b54b2-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span><span class="sxs-lookup"><span data-stu-id="b54b2-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span></span> |
| [**<span data-ttu-id="b54b2-120">Tipos</span><span class="sxs-lookup"><span data-stu-id="b54b2-120">Types</span></span>**](#types) | <span data-ttu-id="b54b2-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span><span class="sxs-lookup"><span data-stu-id="b54b2-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span></span> |
| [**<span data-ttu-id="b54b2-122">Dependencias</span><span class="sxs-lookup"><span data-stu-id="b54b2-122">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="b54b2-123">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b54b2-123">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="b54b2-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="b54b2-124">Methods</span></span>

### <span data-ttu-id="b54b2-125">habilitar</span><span class="sxs-lookup"><span data-stu-id="b54b2-125">enable</span></span>
<span data-ttu-id="b54b2-126">Habilita el agente DOM para la página dada.</span><span class="sxs-lookup"><span data-stu-id="b54b2-126">Enables DOM agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="b54b2-127">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="b54b2-127">disable</span></span>
<span data-ttu-id="b54b2-128">Deshabilita el agente DOM para la página dada.</span><span class="sxs-lookup"><span data-stu-id="b54b2-128">Disables DOM agent for the given page.</span></span> <span data-ttu-id="b54b2-129">Al deshabilitar el DOM, se invalidará cualquier nodeIds válido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-129">Disabling the DOM will invalidate any previously valid nodeIds.</span></span>

</p>

---

### <span data-ttu-id="b54b2-130">getDocument</span><span class="sxs-lookup"><span data-stu-id="b54b2-130">getDocument</span></span>
<span data-ttu-id="b54b2-131">Devuelve el nodo DOM raíz (y, opcionalmente, el subárbol) al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b54b2-131">Returns the root DOM node (and optionally the subtree) to the caller.</span></span> <span data-ttu-id="b54b2-132">`getDocument`Las llamadas invalidarán cualquier nodeIds válida anterior</span><span class="sxs-lookup"><span data-stu-id="b54b2-132">Calling `getDocument` will invalidate any previously valid nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-133">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-133">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-134">Prof</span><span class="sxs-lookup"><span data-stu-id="b54b2-134">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b54b2-135">La profundidad máxima a la que se deben recuperar los niños; el valor predeterminado es 2.</span><span class="sxs-lookup"><span data-stu-id="b54b2-135">The maximum depth at which children should be retrieved, defaults to 2.</span></span> <span data-ttu-id="b54b2-136">Use-1 para todo el subárbol.</span><span class="sxs-lookup"><span data-stu-id="b54b2-136">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-137">atraviese</span><span class="sxs-lookup"><span data-stu-id="b54b2-137">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b54b2-138">Si se debe atravesar iframes o no al devolver el subárbol (el valor predeterminado es false).</span><span class="sxs-lookup"><span data-stu-id="b54b2-138">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-139">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-139">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-140">carpeta</span><span class="sxs-lookup"><span data-stu-id="b54b2-140">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="b54b2-141">Nodo resultante.</span><span class="sxs-lookup"><span data-stu-id="b54b2-141">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-142">highlightNode</span><span class="sxs-lookup"><span data-stu-id="b54b2-142">highlightNode</span></span>
<span data-ttu-id="b54b2-143">Higlights un nodo DOM con identificador determinado o contenedor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-143">Higlights DOM node with given id or object wrapper.</span></span> <span data-ttu-id="b54b2-144">se debe especificar nodeId, backendNodeId o objectId.</span><span class="sxs-lookup"><span data-stu-id="b54b2-144">nodeId, backendNodeId, or objectId must be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-145">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-145">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-146">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-146">nodeId</span></span> <br/> <i><span data-ttu-id="b54b2-147">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-147">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-148">Identificador del nodo que se va a resaltar.</span><span class="sxs-lookup"><span data-stu-id="b54b2-148">Identifier of the node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-149">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-149">backendNodeId</span></span> <br/> <i><span data-ttu-id="b54b2-150">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-150">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="b54b2-151">Identificador del nodo de back-end que se va a resaltar.</span><span class="sxs-lookup"><span data-stu-id="b54b2-151">Identifier of the backend node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-152">ID</span><span class="sxs-lookup"><span data-stu-id="b54b2-152">objectId</span></span> <br/> <i><span data-ttu-id="b54b2-153">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-153">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b54b2-154">Identificador de objeto de JavaScript del nodo que se va a resaltar.</span><span class="sxs-lookup"><span data-stu-id="b54b2-154">JavaScript object id of the node to be highlighted.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-155">higlightConfig</span><span class="sxs-lookup"><span data-stu-id="b54b2-155">higlightConfig</span></span></td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td><span data-ttu-id="b54b2-156">Descriptor de la apariencia del resaltado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-156">Descriptor of the highlight appearance.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-157">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-157">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-158">carpeta</span><span class="sxs-lookup"><span data-stu-id="b54b2-158">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="b54b2-159">Nodo resultante.</span><span class="sxs-lookup"><span data-stu-id="b54b2-159">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-160">hideHighlight</span><span class="sxs-lookup"><span data-stu-id="b54b2-160">hideHighlight</span></span>
<span data-ttu-id="b54b2-161">Oculta cualquier resaltado del nodo DOM actual.</span><span class="sxs-lookup"><span data-stu-id="b54b2-161">Hides any current DOM node highlight.</span></span>

</p>

---

### <span data-ttu-id="b54b2-162">requestChildNodes</span><span class="sxs-lookup"><span data-stu-id="b54b2-162">requestChildNodes</span></span>
<span data-ttu-id="b54b2-163">Solicitudes que los elementos secundarios del nodo con el identificador dado se devuelven a la persona que llama a GHE en forma de `setChildNodes` eventos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-163">Requests that children of the node with given id are returned to ghe caller in the form of `setChildNodes` events.</span></span> `setChildNodes` <span data-ttu-id="b54b2-164">se desencadenará para cada nodo que no haya devuelto anteriormente a elementos secundarios, empezando desde el nodo solicitado hasta la profundidad especificada.</span><span class="sxs-lookup"><span data-stu-id="b54b2-164">will be fired for each node that has not previously returned it's children, starting from the requested node down to the specified depth.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-165">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-165">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-166">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-166">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-167">Identificador del nodo del que se obtendrán los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b54b2-167">Id of the node to get children from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-168">Prof</span><span class="sxs-lookup"><span data-stu-id="b54b2-168">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b54b2-169">La profundidad máxima a la que se deben recuperar los niños; el valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="b54b2-169">The maximum depth at which children should be retrieved, defaults to 1.</span></span> <span data-ttu-id="b54b2-170">Use-1 para todo el subárbol.</span><span class="sxs-lookup"><span data-stu-id="b54b2-170">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-171">atraviese</span><span class="sxs-lookup"><span data-stu-id="b54b2-171">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b54b2-172">Si se debe atravesar iframes o no al devolver el subárbol (el valor predeterminado es false).</span><span class="sxs-lookup"><span data-stu-id="b54b2-172">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-173">getAttributes</span><span class="sxs-lookup"><span data-stu-id="b54b2-173">getAttributes</span></span>
<span data-ttu-id="b54b2-174">Devuelve los atributos del nodo especificado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-174">Returns attributes for the specified node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-175">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-175">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-176">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-176">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-177">Identificador del nodo para el que se va a recuperar el attibutes.</span><span class="sxs-lookup"><span data-stu-id="b54b2-177">Id of the node to retrieve attibutes for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-178">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-178">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-179">atributos</span><span class="sxs-lookup"><span data-stu-id="b54b2-179">attributes</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="b54b2-180">Matriz intercalada de nombres y valores de atributos de nodos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-180">An interleaved array of node attribute names and values.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-181">getOuterHTML</span><span class="sxs-lookup"><span data-stu-id="b54b2-181">getOuterHTML</span></span>
<span data-ttu-id="b54b2-182">Devuelve el formato HTML del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-182">Returns node's HTML markup.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-183">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-183">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-184">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-184">nodeId</span></span> <br/> <i><span data-ttu-id="b54b2-185">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-185">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-186">Identificador del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-186">Identifier of the node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-187">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-187">backendNodeId</span></span> <br/> <i><span data-ttu-id="b54b2-188">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-188">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="b54b2-189">Identificador del nodo back-end.</span><span class="sxs-lookup"><span data-stu-id="b54b2-189">Identifier of the backend node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-190">ID</span><span class="sxs-lookup"><span data-stu-id="b54b2-190">objectId</span></span> <br/> <i><span data-ttu-id="b54b2-191">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-191">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b54b2-192">Identificador de objeto de JavaScript del contenedor del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-192">JavaScript object id of the node wrapper.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-193">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-193">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-194">outerHTML</span><span class="sxs-lookup"><span data-stu-id="b54b2-194">outerHTML</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-195">Formato HTML externo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-195">Outer HTML markup.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-196">pushNodesByBackendIdsToFrontend</span><span class="sxs-lookup"><span data-stu-id="b54b2-196">pushNodesByBackendIdsToFrontend</span></span>
<span data-ttu-id="b54b2-197">Busca identificadores de nodo y resuelve todos los elementos primarios de los identificadores de nodo de back-end especificados</span><span class="sxs-lookup"><span data-stu-id="b54b2-197">Looks up Node Ids and resolves all parents for the specified Backend Node Ids</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-198">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-198">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-199">backendNodeIds</span><span class="sxs-lookup"><span data-stu-id="b54b2-199">backendNodeIds</span></span></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td><span data-ttu-id="b54b2-200">Identificadores de nodo back-end de los nodos que se van a resolver</span><span class="sxs-lookup"><span data-stu-id="b54b2-200">Backend Node IDs of the nodes to resolve</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-201">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-201">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-202">nodeIds</span><span class="sxs-lookup"><span data-stu-id="b54b2-202">nodeIds</span></span></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="b54b2-203">Identificadores de nodo de los nodos resueltos</span><span class="sxs-lookup"><span data-stu-id="b54b2-203">Node Ids of the resolved nodes</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-204">querySelector</span><span class="sxs-lookup"><span data-stu-id="b54b2-204">querySelector</span></span>
<span data-ttu-id="b54b2-205">Se ejecuta `querySelector` en un nodo determinado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-205">Executes `querySelector` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-207">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-207">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-208">Identificador del nodo sobre el que se realizará la consulta.</span><span class="sxs-lookup"><span data-stu-id="b54b2-208">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-209">lector</span><span class="sxs-lookup"><span data-stu-id="b54b2-209">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-210">La cadena de selector.</span><span class="sxs-lookup"><span data-stu-id="b54b2-210">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-211">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-211">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-212">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-212">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-213">Resultado del selector de consultas.</span><span class="sxs-lookup"><span data-stu-id="b54b2-213">Query selector result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-214">querySelectorAll</span><span class="sxs-lookup"><span data-stu-id="b54b2-214">querySelectorAll</span></span>
<span data-ttu-id="b54b2-215">Se ejecuta `querySelectorAll` en un nodo determinado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-215">Executes `querySelectorAll` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-216">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-216">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-217">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-217">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-218">Identificador del nodo sobre el que se realizará la consulta.</span><span class="sxs-lookup"><span data-stu-id="b54b2-218">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-219">lector</span><span class="sxs-lookup"><span data-stu-id="b54b2-219">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-220">La cadena de selector.</span><span class="sxs-lookup"><span data-stu-id="b54b2-220">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-221">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-221">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-222">nodeIds</span><span class="sxs-lookup"><span data-stu-id="b54b2-222">nodeIds</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="b54b2-223">Resultados del selector de consultas.</span><span class="sxs-lookup"><span data-stu-id="b54b2-223">Query selector results.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-224">requestNode</span><span class="sxs-lookup"><span data-stu-id="b54b2-224">requestNode</span></span>
<span data-ttu-id="b54b2-225">Solicita que se envíe al autor de la llamada el nodo con el identificador de objeto remoto dado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-225">Requests that the node with given remote object Id is sent to caller.</span></span> <span data-ttu-id="b54b2-226">Todos los nodos que forman la ruta de acceso del nodo a la raíz también se envían al cliente como una serie de `setChildNodes` notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b54b2-226">All nodes that form the path from the node to the root are also sent to the client as a series of `setChildNodes` notifications.</span></span> <span data-ttu-id="b54b2-227">devuelve 0 si el cliente no ha solicitado previamente el documento que contiene el nodo solicitado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-227">returns 0 if the document containing the requested node has not previously been requested by the client.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-228">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-228">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-229">ID</span><span class="sxs-lookup"><span data-stu-id="b54b2-229">objectId</span></span></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b54b2-230">Identificador de objeto de JavaScript para convertir en nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-230">JavaScript object Id to convert into node.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-231">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-231">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-232">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-232">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-233">Identificador del nodo para el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-233">Node Id for given object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-234">resolveNode</span><span class="sxs-lookup"><span data-stu-id="b54b2-234">resolveNode</span></span>
<span data-ttu-id="b54b2-235">Resuelve el objeto de nodo de JavaScript para un NodeId o BackendNodeId determinado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-235">Resolves the JavaScript node object for a given NodeId or BackendNodeId.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-236">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-236">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-237">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-237">nodeId</span></span> <br/> <i><span data-ttu-id="b54b2-238">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-238">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-239">Identificador del nodo que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="b54b2-239">Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-240">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-240">backendNodeId</span></span> <br/> <i><span data-ttu-id="b54b2-241">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-241">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="b54b2-242">Identificador del nodo back-end del nodo que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="b54b2-242">Backend Node Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-243">objectGroup</span><span class="sxs-lookup"><span data-stu-id="b54b2-243">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-244">Nombre de grupo simbólico que se puede usar para liberar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-244">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-245">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b54b2-245">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-246">objeto</span><span class="sxs-lookup"><span data-stu-id="b54b2-246">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="b54b2-247">Contenedor de objeto de JavaScript para el nodo determinado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-247">JavaScript object wrapper for given node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-248">setInspectedNode</span><span class="sxs-lookup"><span data-stu-id="b54b2-248">setInspectedNode</span></span>
<span><b><span data-ttu-id="b54b2-249">Montaje.</span><span class="sxs-lookup"><span data-stu-id="b54b2-249">Experimental.</span></span> </b></span><span data-ttu-id="b54b2-250">Permite a la consola referirse al nodo inspeccionado anterior con el identificador dado a través de $0-$ 4.</span><span class="sxs-lookup"><span data-stu-id="b54b2-250">Enables console to refer to the previous inspected node with given id via $0-$4.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-251">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-252">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-252">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-253">Identificador de nodo DOM al que se puede acceder mediante $0-$ 4 en la API de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-253">DOM node id to be accessible by means of $0-$4 in command line API.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="b54b2-254">Eventos</span><span class="sxs-lookup"><span data-stu-id="b54b2-254">Events</span></span>

### <span data-ttu-id="b54b2-255">setChildNodes</span><span class="sxs-lookup"><span data-stu-id="b54b2-255">setChildNodes</span></span>
<span data-ttu-id="b54b2-256">Se desencadena cuando el servidor desea proporcionar al cliente una estructura DOM que falta.</span><span class="sxs-lookup"><span data-stu-id="b54b2-256">Fired when the backend wishes to provide client with missing DOM structure.</span></span> <span data-ttu-id="b54b2-257">Esto sucede en la mayoría de las llamadas que solicitan nodeIds</span><span class="sxs-lookup"><span data-stu-id="b54b2-257">This happens upon most calls requesting nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-258">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-258">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-259">parentId</span><span class="sxs-lookup"><span data-stu-id="b54b2-259">parentId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-260">Nodo principal para poplate con elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b54b2-260">Parent node to poplate with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-261">node</span><span class="sxs-lookup"><span data-stu-id="b54b2-261">nodes</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="b54b2-262">Matriz de nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b54b2-262">Child nodes array.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-263">attributeModified</span><span class="sxs-lookup"><span data-stu-id="b54b2-263">attributeModified</span></span>
<span data-ttu-id="b54b2-264">Se desencadena cuando el `Element` atributo de se modifica.</span><span class="sxs-lookup"><span data-stu-id="b54b2-264">Fired when `Element`'s attribute is modified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-265">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-265">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-266">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-266">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-267">Identificador del nodo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-267">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-268">name</span><span class="sxs-lookup"><span data-stu-id="b54b2-268">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-269">Nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-269">Attribute name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-270">value</span><span class="sxs-lookup"><span data-stu-id="b54b2-270">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-271">Valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-271">Attribute value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-272">attributeRemoved</span><span class="sxs-lookup"><span data-stu-id="b54b2-272">attributeRemoved</span></span>
<span data-ttu-id="b54b2-273">Se desencadena cuando `Element` se quita el atributo de.</span><span class="sxs-lookup"><span data-stu-id="b54b2-273">Fired when `Element`'s attribute is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-274">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-274">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-275">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-275">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-276">Identificador del nodo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-276">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-277">name</span><span class="sxs-lookup"><span data-stu-id="b54b2-277">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-278">Nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-278">Attribute name.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-279">characterDataModified</span><span class="sxs-lookup"><span data-stu-id="b54b2-279">characterDataModified</span></span>
<span data-ttu-id="b54b2-280">`DOMCharacterDataModified`Evento Mirror.</span><span class="sxs-lookup"><span data-stu-id="b54b2-280">Mirrors `DOMCharacterDataModified` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-281">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-281">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-282">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-282">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-283">Identificador del nodo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-283">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-284">charcterData</span><span class="sxs-lookup"><span data-stu-id="b54b2-284">charcterData</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-285">Nuevo valor de texto.</span><span class="sxs-lookup"><span data-stu-id="b54b2-285">New text value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-286">childNodeInserted</span><span class="sxs-lookup"><span data-stu-id="b54b2-286">childNodeInserted</span></span>
<span data-ttu-id="b54b2-287">`DOMNodeInserted`Evento Mirror.</span><span class="sxs-lookup"><span data-stu-id="b54b2-287">Mirrors `DOMNodeInserted` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-288">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-288">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-289">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-289">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-290">Identificador del nodo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-290">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-291">previousNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-291">previousNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-292">Identificador del elemento anterior del mismo nivel del nodo insertado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-292">Id of the inserted node's previous sibling.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-293">nodo</span><span class="sxs-lookup"><span data-stu-id="b54b2-293">node</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="b54b2-294">Datos de nodo insertados.</span><span class="sxs-lookup"><span data-stu-id="b54b2-294">Inserted node data.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-295">childNodeRemoved</span><span class="sxs-lookup"><span data-stu-id="b54b2-295">childNodeRemoved</span></span>
<span data-ttu-id="b54b2-296">`DOMNodeRemoved`Evento Mirror.</span><span class="sxs-lookup"><span data-stu-id="b54b2-296">Mirrors `DOMNodeRemoved` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-297">Parameters</span><span class="sxs-lookup"><span data-stu-id="b54b2-297">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-298">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-298">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-299">Identificador del nodo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-299">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-300">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-300">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-301">Identificador del nodo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="b54b2-301">Id of the node that has been removed.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b54b2-302">documentUpdated</span><span class="sxs-lookup"><span data-stu-id="b54b2-302">documentUpdated</span></span>
<span data-ttu-id="b54b2-303">Se activa cuando se `Document` ha actualizado totalmente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-303">Fired when `Document` has been totally updated.</span></span> <span data-ttu-id="b54b2-304">Los identificadores de nodo ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-304">Node ids are no longer valid.</span></span>

</p>

---

## <span data-ttu-id="b54b2-305">Tipos</span><span class="sxs-lookup"><span data-stu-id="b54b2-305">Types</span></span>

### <a name="rgba"></a> <span data-ttu-id="b54b2-306">RGBA</span><span class="sxs-lookup"><span data-stu-id="b54b2-306">RGBA</span></span> `object`

<span data-ttu-id="b54b2-307">Estructura que contiene un color RGBA.</span><span class="sxs-lookup"><span data-stu-id="b54b2-307">A Structure holding an RGBA color.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-308">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b54b2-308">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-309">d</span><span class="sxs-lookup"><span data-stu-id="b54b2-309">r</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b54b2-310">El componente rojo, en el rango de [0-255].</span><span class="sxs-lookup"><span data-stu-id="b54b2-310">The red component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-311">cuentas</span><span class="sxs-lookup"><span data-stu-id="b54b2-311">g</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b54b2-312">El componente verde, en el rango de [0-255].</span><span class="sxs-lookup"><span data-stu-id="b54b2-312">The green component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-313">letra</span><span class="sxs-lookup"><span data-stu-id="b54b2-313">b</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b54b2-314">El componente azul, en el rango [0-255].</span><span class="sxs-lookup"><span data-stu-id="b54b2-314">The blue component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-315">a</span><span class="sxs-lookup"><span data-stu-id="b54b2-315">a</span></span> <br/> <i><span data-ttu-id="b54b2-316">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-316">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="b54b2-317">El componente alfa, en el rango de [0-1].</span><span class="sxs-lookup"><span data-stu-id="b54b2-317">The alpha component, in the [0-1] range.</span></span> <span data-ttu-id="b54b2-318">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="b54b2-318">Default is 1.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> <span data-ttu-id="b54b2-319">HighlightConfig</span><span class="sxs-lookup"><span data-stu-id="b54b2-319">HighlightConfig</span></span> `object`

<span data-ttu-id="b54b2-320">Datos de configuración para resaltar los elementos de la página.</span><span class="sxs-lookup"><span data-stu-id="b54b2-320">Configuration data for highlighting of page elements.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-321">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b54b2-321">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-322">contentColor</span><span class="sxs-lookup"><span data-stu-id="b54b2-322">contentColor</span></span> <br/> <i><span data-ttu-id="b54b2-323">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-323">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="b54b2-324">Color de relleno de resaltado del cuadro de contenido.</span><span class="sxs-lookup"><span data-stu-id="b54b2-324">The content box highlight fill color.</span></span> <span data-ttu-id="b54b2-325">El valor predeterminado es transparente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-325">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-326">paddingColor</span><span class="sxs-lookup"><span data-stu-id="b54b2-326">paddingColor</span></span> <br/> <i><span data-ttu-id="b54b2-327">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-327">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="b54b2-328">Color de relleno resaltado de relleno.</span><span class="sxs-lookup"><span data-stu-id="b54b2-328">The padding highlight fill color.</span></span> <span data-ttu-id="b54b2-329">El valor predeterminado es transparente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-329">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-330">ColorDeLosBordes</span><span class="sxs-lookup"><span data-stu-id="b54b2-330">borderColor</span></span> <br/> <i><span data-ttu-id="b54b2-331">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-331">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="b54b2-332">Color de relleno de resaltado de borde.</span><span class="sxs-lookup"><span data-stu-id="b54b2-332">The border highlight fill color.</span></span> <span data-ttu-id="b54b2-333">El valor predeterminado es transparente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-333">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-334">marginColor</span><span class="sxs-lookup"><span data-stu-id="b54b2-334">marginColor</span></span> <br/> <i><span data-ttu-id="b54b2-335">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-335">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="b54b2-336">Color de relleno de resaltado de margen.</span><span class="sxs-lookup"><span data-stu-id="b54b2-336">The margin highlight fill color.</span></span> <span data-ttu-id="b54b2-337">El valor predeterminado es transparente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-337">Default is transparent.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> <span data-ttu-id="b54b2-338">NodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-338">NodeId</span></span> `integer`

<span data-ttu-id="b54b2-339">Identificador de nodo DOM único</span><span class="sxs-lookup"><span data-stu-id="b54b2-339">Unique DOM node identifier</span></span>

</p>

---

### <a name="node"></a> <span data-ttu-id="b54b2-340">Nodo</span><span class="sxs-lookup"><span data-stu-id="b54b2-340">Node</span></span> `object`

<span data-ttu-id="b54b2-341">Objeto Mirror que representa los nodos DOM reales.</span><span class="sxs-lookup"><span data-stu-id="b54b2-341">Mirror object that represents the actual DOM nodes.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b54b2-342">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b54b2-342">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b54b2-343">nodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-343">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-344">Identificador de nodo usado para hacer referencia a este nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-344">Node Identifier used to reference this node.</span></span> <span data-ttu-id="b54b2-345">El back-end desencadenará eventos de DOM para los nodos que tengan un nodeId conocido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="b54b2-345">Backend will fire DOM events for nodes that have a nodeId that is known to the client</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-346">parentId</span><span class="sxs-lookup"><span data-stu-id="b54b2-346">parentId</span></span> <br/> <i><span data-ttu-id="b54b2-347">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-347">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-348">Identificador de nodo del nodo principal, si existe.</span><span class="sxs-lookup"><span data-stu-id="b54b2-348">Node Identifier of the parent Node, if any.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-349">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-349">backendNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="b54b2-350">Identificador del nodo back-end del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-350">Backend Node identifier of the node.</span></span> <span data-ttu-id="b54b2-351">BackendNodeIds los nodos de referencia que pueden ser conocidos para el cliente, pero no insertan eventos DOM sobre este nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-351">BackendNodeIds reference Nodes that can be known to the client, but do not push DOM events about this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-352">Nodo</span><span class="sxs-lookup"><span data-stu-id="b54b2-352">nodeType</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`<span data-ttu-id="b54b2-353">nodeType de la.</span><span class="sxs-lookup"><span data-stu-id="b54b2-353">'s nodeType.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-354">nombreDeNodo</span><span class="sxs-lookup"><span data-stu-id="b54b2-354">nodeName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="b54b2-355">nodeName de.</span><span class="sxs-lookup"><span data-stu-id="b54b2-355">'s nodeName.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-356">Local</span><span class="sxs-lookup"><span data-stu-id="b54b2-356">localName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="b54b2-357">localName de</span><span class="sxs-lookup"><span data-stu-id="b54b2-357">'s localName</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-358">nodeValue</span><span class="sxs-lookup"><span data-stu-id="b54b2-358">nodeValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="b54b2-359">nodeValue de la</span><span class="sxs-lookup"><span data-stu-id="b54b2-359">'s nodeValue</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-360">childNodeCount</span><span class="sxs-lookup"><span data-stu-id="b54b2-360">childNodeCount</span></span> <br/> <i><span data-ttu-id="b54b2-361">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-361">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b54b2-362">Recuento secundario de los `Container` nodos.</span><span class="sxs-lookup"><span data-stu-id="b54b2-362">Child count for `Container` nodes.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-363">niños</span><span class="sxs-lookup"><span data-stu-id="b54b2-363">children</span></span> <br/> <i><span data-ttu-id="b54b2-364">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-364">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="b54b2-365">Nodos secundarios de este nodo cuando se solicitan con elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b54b2-365">Child nodes of this node when requested with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-366">atributos</span><span class="sxs-lookup"><span data-stu-id="b54b2-366">attributes</span></span> <br/> <i><span data-ttu-id="b54b2-367">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-367">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="b54b2-368">Atributos de `Element` los nodos en el formulario de una matriz plana ' [nombre1, valor1, nombre2, valor2]</span><span class="sxs-lookup"><span data-stu-id="b54b2-368">Attributes of `Element` nodes in the form of a flat array \`[name1, value1, name2, value2]</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-369">documentURL</span><span class="sxs-lookup"><span data-stu-id="b54b2-369">documentURL</span></span> <br/> <i><span data-ttu-id="b54b2-370">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-370">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-371">Dirección URL del documento a la que los `Document` nodos apuntan.</span><span class="sxs-lookup"><span data-stu-id="b54b2-371">Document URL that `Document` nodes point to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-372">baseURL</span><span class="sxs-lookup"><span data-stu-id="b54b2-372">baseURL</span></span> <br/> <i><span data-ttu-id="b54b2-373">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-373">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b54b2-374">Dirección URL del documento que `Document` usan los nodos para la finalización de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b54b2-374">Document URL that `Document` nodes use for URL completion.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-375">publicId</span><span class="sxs-lookup"><span data-stu-id="b54b2-375">publicId</span></span> <br/> <i><span data-ttu-id="b54b2-376">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-376">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="b54b2-377">PublicId del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-377">Node's publicId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-378">systemId</span><span class="sxs-lookup"><span data-stu-id="b54b2-378">systemId</span></span> <br/> <i><span data-ttu-id="b54b2-379">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-379">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="b54b2-380">SystemId del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-380">Node's systemId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-381">internalSubset</span><span class="sxs-lookup"><span data-stu-id="b54b2-381">internalSubset</span></span> <br/> <i><span data-ttu-id="b54b2-382">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-382">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="b54b2-383">InternalSubset del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-383">Node's internalSubset.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-384">xmlVersion</span><span class="sxs-lookup"><span data-stu-id="b54b2-384">xmlVersion</span></span> <br/> <i><span data-ttu-id="b54b2-385">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-385">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` <span data-ttu-id="b54b2-386">Versión XML del nodo en el caso de documentos XML.</span><span class="sxs-lookup"><span data-stu-id="b54b2-386">Node's xml version in the case of XML documents.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-387">name</span><span class="sxs-lookup"><span data-stu-id="b54b2-387">name</span></span> <br/> <i><span data-ttu-id="b54b2-388">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-388">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="b54b2-389">Nombre del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-389">Node's name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-390">value</span><span class="sxs-lookup"><span data-stu-id="b54b2-390">value</span></span> <br/> <i><span data-ttu-id="b54b2-391">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-391">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="b54b2-392">Valor del nodo.</span><span class="sxs-lookup"><span data-stu-id="b54b2-392">Node's value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-393">frameId</span><span class="sxs-lookup"><span data-stu-id="b54b2-393">frameId</span></span> <br/> <i><span data-ttu-id="b54b2-394">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-394">optional</span></span></i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td><span data-ttu-id="b54b2-395">IDENTIFICADOR del fotograma de los elementos de propietario del marco.</span><span class="sxs-lookup"><span data-stu-id="b54b2-395">Frame ID for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-396">contentDocument</span><span class="sxs-lookup"><span data-stu-id="b54b2-396">contentDocument</span></span> <br/> <i><span data-ttu-id="b54b2-397">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-397">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="b54b2-398">Documento de contenido de los elementos de propietario del marco.</span><span class="sxs-lookup"><span data-stu-id="b54b2-398">Content document for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b54b2-399">isSVG</span><span class="sxs-lookup"><span data-stu-id="b54b2-399">isSVG</span></span> <br/> <i><span data-ttu-id="b54b2-400">opcional</span><span class="sxs-lookup"><span data-stu-id="b54b2-400">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b54b2-401">True si el nodo es SVG.</span><span class="sxs-lookup"><span data-stu-id="b54b2-401">True if the node is SVG.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> <span data-ttu-id="b54b2-402">BackendNodeId</span><span class="sxs-lookup"><span data-stu-id="b54b2-402">BackendNodeId</span></span> `integer`

<span data-ttu-id="b54b2-403">Identificador de nodo DOM único que se usa para hacer referencia a un nodo que es posible que no se haya insertado en el front-end.</span><span class="sxs-lookup"><span data-stu-id="b54b2-403">Unique DOM node identifier used to reference a node that may not have been pushed to the front-end.</span></span>

</p>

---

### <a name="pseudotype"></a> <span data-ttu-id="b54b2-404">PseudoType</span><span class="sxs-lookup"><span data-stu-id="b54b2-404">PseudoType</span></span> `string`

<span data-ttu-id="b54b2-405">Tipo de seudoelemento.</span><span class="sxs-lookup"><span data-stu-id="b54b2-405">Pseudo element type.</span></span>

##### <span data-ttu-id="b54b2-406">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="b54b2-406">Allowed Values</span></span>
<span data-ttu-id="b54b2-407">selección de la primera línea, primera letra, antes, después y selección</span><span class="sxs-lookup"><span data-stu-id="b54b2-407">first-line, first-letter, before, after, selection</span></span>
</p>

---

## <span data-ttu-id="b54b2-408">Dependencias</span><span class="sxs-lookup"><span data-stu-id="b54b2-408">Dependencies</span></span>

[<span data-ttu-id="b54b2-409">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b54b2-409">Runtime</span></span>](runtime.md)
