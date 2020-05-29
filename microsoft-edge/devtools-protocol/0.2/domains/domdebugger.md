---
description: Referencia del dominio DOMDebugger. La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos. La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.
title: 'DOMDebugger Domain: DevTools Protocol versión 0,2'
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573734"
---
# <span data-ttu-id="1356b-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="1356b-105">DOMDebugger</span></span>
<span data-ttu-id="1356b-106">La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos.</span><span class="sxs-lookup"><span data-stu-id="1356b-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="1356b-107">La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.</span><span class="sxs-lookup"><span data-stu-id="1356b-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="1356b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="1356b-108">Methods</span></span>**](#methods) | <span data-ttu-id="1356b-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="1356b-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="1356b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1356b-110">Methods</span></span>

### <span data-ttu-id="1356b-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="1356b-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="1356b-112">Montaje.</span><span class="sxs-lookup"><span data-stu-id="1356b-112">Experimental.</span></span> </b></span><span data-ttu-id="1356b-113">Establece un punto de interrupción en un evento nativo determinado.</span><span class="sxs-lookup"><span data-stu-id="1356b-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1356b-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="1356b-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1356b-115">nombreDeEvento</span><span class="sxs-lookup"><span data-stu-id="1356b-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="1356b-116">Nombre de la instrumentación que se va a detener.</span><span class="sxs-lookup"><span data-stu-id="1356b-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="1356b-117">Valores válidos: ' scriptFirstStatement '.</span><span class="sxs-lookup"><span data-stu-id="1356b-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="1356b-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="1356b-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="1356b-119">Montaje.</span><span class="sxs-lookup"><span data-stu-id="1356b-119">Experimental.</span></span> </b></span><span data-ttu-id="1356b-120">Quita un punto de interrupción de un evento nativo en particular.</span><span class="sxs-lookup"><span data-stu-id="1356b-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1356b-121">Parameters</span><span class="sxs-lookup"><span data-stu-id="1356b-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1356b-122">nombreDeEvento</span><span class="sxs-lookup"><span data-stu-id="1356b-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="1356b-123">Nombre de la instrumentación que se va a detener.</span><span class="sxs-lookup"><span data-stu-id="1356b-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="1356b-124">Valores válidos: ' scriptFirstStatement '.</span><span class="sxs-lookup"><span data-stu-id="1356b-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
