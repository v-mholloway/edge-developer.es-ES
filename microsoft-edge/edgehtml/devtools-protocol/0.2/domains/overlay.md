---
description: Referencia para el dominio de superposición. El dominio de superposición expone elementos visuales y la interacción de selección de nodos
title: Dominio de superposición-protocolo de DevTools versión 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235962"
---
# <span data-ttu-id="27f69-104">Overlay</span><span class="sxs-lookup"><span data-stu-id="27f69-104">Overlay</span></span>

<span data-ttu-id="27f69-105">El dominio de superposición expone elementos visuales y la interacción de selección de nodos</span><span class="sxs-lookup"><span data-stu-id="27f69-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="27f69-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="27f69-106">Methods</span></span>**](#methods) | <span data-ttu-id="27f69-107">[Habilitar](#enable), [deshabilitar](#disable), [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="27f69-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="27f69-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="27f69-108">Events</span></span>**](#events) | <span data-ttu-id="27f69-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="27f69-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="27f69-110">Dependencias</span><span class="sxs-lookup"><span data-stu-id="27f69-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="27f69-111">DOM</span><span class="sxs-lookup"><span data-stu-id="27f69-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="27f69-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="27f69-112">Methods</span></span>

### <span data-ttu-id="27f69-113">habilitar</span><span class="sxs-lookup"><span data-stu-id="27f69-113">enable</span></span>
<span data-ttu-id="27f69-114">Permite la creación de informes <code>nodeHighlightRequested</code> y <code>inspectElementRequested</code> eventos</span><span class="sxs-lookup"><span data-stu-id="27f69-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="27f69-115">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="27f69-115">disable</span></span>
<span data-ttu-id="27f69-116">Deshabilita los informes de eventos de dominio de superposición</span><span class="sxs-lookup"><span data-stu-id="27f69-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="27f69-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="27f69-117">setInspectMode</span></span>
<span data-ttu-id="27f69-118">Establece el modo de selección de elementos para el cliente.</span><span class="sxs-lookup"><span data-stu-id="27f69-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="27f69-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="27f69-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="27f69-120">mode</span><span class="sxs-lookup"><span data-stu-id="27f69-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="27f69-121">El modo de inspección.</span><span class="sxs-lookup"><span data-stu-id="27f69-121">The inspection mode.</span></span>  <span data-ttu-id="27f69-122">Los valores válidos son ' searchForNode ' y ' none '.</span><span class="sxs-lookup"><span data-stu-id="27f69-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="27f69-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="27f69-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="27f69-124">opcional</span><span class="sxs-lookup"><span data-stu-id="27f69-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="27f69-125">La configuración de resaltado que se usará durante la inspección</span><span class="sxs-lookup"><span data-stu-id="27f69-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="27f69-126">Eventos</span><span class="sxs-lookup"><span data-stu-id="27f69-126">Events</span></span>

### <span data-ttu-id="27f69-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="27f69-127">inspectNodeRequested</span></span>
<span data-ttu-id="27f69-128">Notifica al cliente que el usuario ha solicitado inspeccionar un nodo determinado</span><span class="sxs-lookup"><span data-stu-id="27f69-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="27f69-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="27f69-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="27f69-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="27f69-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="27f69-131">El identificador del nodo back-end del nodo solicitado</span><span class="sxs-lookup"><span data-stu-id="27f69-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="27f69-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="27f69-132">nodeHighlightRequested</span></span>
<span data-ttu-id="27f69-133">Indica que el usuario ha activado el nodo y puede inspeccionar el nodo</span><span class="sxs-lookup"><span data-stu-id="27f69-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="27f69-134">Parameters</span><span class="sxs-lookup"><span data-stu-id="27f69-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="27f69-135">nodeId</span><span class="sxs-lookup"><span data-stu-id="27f69-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="27f69-136">El identificador de nodo del nodo que se está considerando</span><span class="sxs-lookup"><span data-stu-id="27f69-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="27f69-137">Dependencias</span><span class="sxs-lookup"><span data-stu-id="27f69-137">Dependencies</span></span>

[<span data-ttu-id="27f69-138">DOM</span><span class="sxs-lookup"><span data-stu-id="27f69-138">DOM</span></span>](dom.md)
