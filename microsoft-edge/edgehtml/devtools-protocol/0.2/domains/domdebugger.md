---
description: Referencia del dominio DOMDebugger. La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos. La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.
title: 'DOMDebugger Domain: DevTools Protocol versión 0,2'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235964"
---
# <span data-ttu-id="4d0c3-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="4d0c3-105">DOMDebugger</span></span>

<span data-ttu-id="4d0c3-106">La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="4d0c3-107">La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="4d0c3-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d0c3-108">Methods</span></span>**](#methods) | <span data-ttu-id="4d0c3-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="4d0c3-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="4d0c3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d0c3-110">Methods</span></span>

### <span data-ttu-id="4d0c3-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="4d0c3-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="4d0c3-112">Montaje.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-112">Experimental.</span></span> </b></span><span data-ttu-id="4d0c3-113">Establece un punto de interrupción en un evento nativo determinado.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d0c3-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="4d0c3-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d0c3-115">nombreDeEvento</span><span class="sxs-lookup"><span data-stu-id="4d0c3-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d0c3-116">Nombre de la instrumentación que se va a detener.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="4d0c3-117">Valores válidos: ' scriptFirstStatement '.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="4d0c3-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="4d0c3-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="4d0c3-119">Montaje.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-119">Experimental.</span></span> </b></span><span data-ttu-id="4d0c3-120">Quita un punto de interrupción de un evento nativo en particular.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d0c3-121">Parameters</span><span class="sxs-lookup"><span data-stu-id="4d0c3-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d0c3-122">nombreDeEvento</span><span class="sxs-lookup"><span data-stu-id="4d0c3-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d0c3-123">Nombre de la instrumentación que se va a detener.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="4d0c3-124">Valores válidos: ' scriptFirstStatement '.</span><span class="sxs-lookup"><span data-stu-id="4d0c3-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
