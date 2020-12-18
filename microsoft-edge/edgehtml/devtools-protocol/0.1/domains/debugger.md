---
description: DevTools Protocol version 0,1 (EdgeHTML) Reference for the Debugger domain. El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.
title: Dominio de depuración-DevTools Protocol versión 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5160e6e69ec76f8c584f1bdb969464d805c7afa7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236354"
---
# <span data-ttu-id="ca797-105">Dominio de depuración-DevTools Protocol versión 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="ca797-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="ca797-106">El dominio del depurador expone capacidades de depuración de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca797-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="ca797-107">Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.</span><span class="sxs-lookup"><span data-stu-id="ca797-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="ca797-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca797-108">Methods</span></span>**](#methods) | <span data-ttu-id="ca797-109">[enable](#enable), [Disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [ancho](#stepover) [de es, stepInto](#stepinto) [, stepOut](#stepout), [PAUSE](#pause), [resume](#resume) [, getScriptSource, setPauseOnExceptions](#getscriptsource) [, evaluateOnCallFrame](#setpauseonexceptions) [,](#evaluateoncallframe) [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns) [, msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="ca797-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="ca797-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="ca797-110">Events</span></span>**](#events) | <span data-ttu-id="ca797-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [reanudado](#resumed)</span><span class="sxs-lookup"><span data-stu-id="ca797-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="ca797-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="ca797-112">Types</span></span>**](#types) | <span data-ttu-id="ca797-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Ubicación](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [ámbito](#scope)</span><span class="sxs-lookup"><span data-stu-id="ca797-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="ca797-114">Dependencias</span><span class="sxs-lookup"><span data-stu-id="ca797-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="ca797-115">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ca797-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="ca797-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca797-116">Methods</span></span>

### <span data-ttu-id="ca797-117">habilitar</span><span class="sxs-lookup"><span data-stu-id="ca797-117">enable</span></span>
<span data-ttu-id="ca797-118">Habilita el depurador para la página dada.</span><span class="sxs-lookup"><span data-stu-id="ca797-118">Enables debugger for the given page.</span></span> <span data-ttu-id="ca797-119">Los clientes no deben suponer que la depuración se ha habilitado hasta que se reciba el resultado de este comando.</span><span class="sxs-lookup"><span data-stu-id="ca797-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="ca797-120">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="ca797-120">disable</span></span>
<span data-ttu-id="ca797-121">Deshabilita el depurador para la página dada.</span><span class="sxs-lookup"><span data-stu-id="ca797-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="ca797-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="ca797-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="ca797-123">Devuelve posibles ubicaciones para el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="ca797-124">scriptId en las ubicaciones de intervalo de inicio y de finalización deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="ca797-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-126">start</span><span class="sxs-lookup"><span data-stu-id="ca797-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-127">Inicio del rango para buscar posibles ubicaciones de puntos de interrupción en.</span><span class="sxs-lookup"><span data-stu-id="ca797-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-128">terminar</span><span class="sxs-lookup"><span data-stu-id="ca797-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-129">Fin del rango para buscar posibles ubicaciones de puntos de interrupción en (excepto).</span><span class="sxs-lookup"><span data-stu-id="ca797-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="ca797-130">Cuando no se especifica, el final de las secuencias de comandos se usa como fin del rango.</span><span class="sxs-lookup"><span data-stu-id="ca797-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-131">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ca797-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-132">sitios</span><span class="sxs-lookup"><span data-stu-id="ca797-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="ca797-133">Lista de posibles ubicaciones de los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="ca797-134">setBreakpointsActive</span></span>
<span data-ttu-id="ca797-135">Activa o desactiva todos los puntos de interrupción de la página.</span><span class="sxs-lookup"><span data-stu-id="ca797-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-137">activa</span><span class="sxs-lookup"><span data-stu-id="ca797-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="ca797-138">Nuevo valor para puntos de interrupción activo estado.</span><span class="sxs-lookup"><span data-stu-id="ca797-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="ca797-139">setBreakpointByUrl</span></span>
<span data-ttu-id="ca797-140">Establece un punto de interrupción de JavaScript en la ubicación especificada, por dirección URL o dirección URL Regex.</span><span class="sxs-lookup"><span data-stu-id="ca797-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="ca797-141">Una vez que se haya emitido este comando, todos los scripts analizados existentes tendrán los puntos de interrupción resueltos y devueltos en la <code>locations</code> propiedad.</span><span class="sxs-lookup"><span data-stu-id="ca797-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="ca797-142">Además, el análisis de scripts más parecido dará como resultado <code>breakpointResolved</code> eventos posteriores.</span><span class="sxs-lookup"><span data-stu-id="ca797-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="ca797-143">Este punto de interrupción lógico afectará a las recargas de páginas.</span><span class="sxs-lookup"><span data-stu-id="ca797-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-144">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-146">Número de línea para establecer el punto de interrupción en.</span><span class="sxs-lookup"><span data-stu-id="ca797-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-147">url</span><span class="sxs-lookup"><span data-stu-id="ca797-147">url</span></span> <br/> <i><span data-ttu-id="ca797-148">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-149">Dirección URL de los recursos para establecer el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="ca797-150">urlRegex</span></span> <br/> <i><span data-ttu-id="ca797-151">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-152">Patrón de Regex para las direcciones URL de los recursos para establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="ca797-153"><code>url</code>O <code>urlRegex</code> debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="ca797-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-154">columnNumber</span></span> <br/> <i><span data-ttu-id="ca797-155">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-156">Desplazamiento en la línea para establecer el punto de interrupción en.</span><span class="sxs-lookup"><span data-stu-id="ca797-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-157">requisito</span><span class="sxs-lookup"><span data-stu-id="ca797-157">condition</span></span> <br/> <i><span data-ttu-id="ca797-158">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-159">Expresión que se va a usar como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="ca797-160">Cuando se especifica, Debugger solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="ca797-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-161">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ca797-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="ca797-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="ca797-163">Identificador del punto de interrupción creado para referencia adicional.</span><span class="sxs-lookup"><span data-stu-id="ca797-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-164">sitios</span><span class="sxs-lookup"><span data-stu-id="ca797-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="ca797-165">Lista de las ubicaciones en las que se ha resuelto este punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="ca797-166">setBreakpoint</span></span>
<span data-ttu-id="ca797-167">Establece un punto de interrupción de JavaScript en una ubicación determinada.</span><span class="sxs-lookup"><span data-stu-id="ca797-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-168">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-169">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ca797-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-170">Ubicación en la que se establecerá el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-171">requisito</span><span class="sxs-lookup"><span data-stu-id="ca797-171">condition</span></span> <br/> <i><span data-ttu-id="ca797-172">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-173">Expresión que se va a usar como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="ca797-174">Cuando se especifica, Debugger solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="ca797-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-175">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ca797-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="ca797-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="ca797-177">Identificador del punto de interrupción creado para referencia adicional.</span><span class="sxs-lookup"><span data-stu-id="ca797-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="ca797-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-179">Ubicación en la que se resuelve este punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="ca797-180">removeBreakpoint</span></span>
<span data-ttu-id="ca797-181">Quita el punto de interrupción de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca797-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-182">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="ca797-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-184">Pasadas</span><span class="sxs-lookup"><span data-stu-id="ca797-184">stepOver</span></span>
<span data-ttu-id="ca797-185">Pasos sobre la instrucción.</span><span class="sxs-lookup"><span data-stu-id="ca797-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="ca797-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="ca797-186">stepInto</span></span>
<span data-ttu-id="ca797-187">Recorre los pasos de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="ca797-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="ca797-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="ca797-188">stepOut</span></span>
<span data-ttu-id="ca797-189">Recorre los pasos de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="ca797-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="ca797-190">pause</span><span class="sxs-lookup"><span data-stu-id="ca797-190">pause</span></span>
<span data-ttu-id="ca797-191">Se detiene en la siguiente instrucción de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca797-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="ca797-192">resume</span><span class="sxs-lookup"><span data-stu-id="ca797-192">resume</span></span>
<span data-ttu-id="ca797-193">Reanuda la ejecución de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca797-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="ca797-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="ca797-194">getScriptSource</span></span>
<span data-ttu-id="ca797-195">Devuelve el origen del script con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="ca797-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-196">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="ca797-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="ca797-198">Identificador del script para el que se va a obtener el origen.</span><span class="sxs-lookup"><span data-stu-id="ca797-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-199">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ca797-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="ca797-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-201">Origen de script.</span><span class="sxs-lookup"><span data-stu-id="ca797-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="ca797-202">setPauseOnExceptions</span></span>
<span data-ttu-id="ca797-203">Define la pausa en el estado de las excepciones.</span><span class="sxs-lookup"><span data-stu-id="ca797-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="ca797-204">Puede establecerse en detener en todas las excepciones, excepciones no detectadas o sin excepciones.</span><span class="sxs-lookup"><span data-stu-id="ca797-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="ca797-205">El estado de pausa inicial en excepciones es de <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="ca797-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-207">situación</span><span class="sxs-lookup"><span data-stu-id="ca797-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="ca797-208">Valores permitidos: ninguno, no detectados, todos</span><span class="sxs-lookup"><span data-stu-id="ca797-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="ca797-209">Pausar en el modo de excepciones.</span><span class="sxs-lookup"><span data-stu-id="ca797-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="ca797-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="ca797-211">Evalúa Expression en un marco de llamada dado.</span><span class="sxs-lookup"><span data-stu-id="ca797-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="ca797-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="ca797-214">Identificador de marco de llamada que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="ca797-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-215">Expression</span><span class="sxs-lookup"><span data-stu-id="ca797-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-216">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="ca797-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-217">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ca797-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-218">resultado</span><span class="sxs-lookup"><span data-stu-id="ca797-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="ca797-219">Contenedor de objetos para el resultado de evaluación.</span><span class="sxs-lookup"><span data-stu-id="ca797-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="ca797-220">setVariableValue</span></span>
<span data-ttu-id="ca797-221">Cambia el valor de la variable en un callframe.</span><span class="sxs-lookup"><span data-stu-id="ca797-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="ca797-222">Los ámbitos basados en objetos no son compatibles y se deben mutar manualmente.</span><span class="sxs-lookup"><span data-stu-id="ca797-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-223">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-225">número de base cero de ámbito que se mostraba en la cadena de ámbitos.</span><span class="sxs-lookup"><span data-stu-id="ca797-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="ca797-226">Solo se permiten los tipos de ámbito ' local ', ' cierre ' y ' Catch '.</span><span class="sxs-lookup"><span data-stu-id="ca797-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="ca797-227">Es posible manipular otros ámbitos de forma manual.</span><span class="sxs-lookup"><span data-stu-id="ca797-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-228">variableName</span><span class="sxs-lookup"><span data-stu-id="ca797-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-229">Nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="ca797-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-230">Nuevovalor</span><span class="sxs-lookup"><span data-stu-id="ca797-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="ca797-231">Nuevo valor de variable.</span><span class="sxs-lookup"><span data-stu-id="ca797-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="ca797-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="ca797-233">Identificador de callframe que contiene la variable.</span><span class="sxs-lookup"><span data-stu-id="ca797-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="ca797-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="ca797-235">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-235">Experimental.</span></span> </b></span><span data-ttu-id="ca797-236">Reemplazar patrones de Blackbox anteriores por los que se hayan pasado.</span><span class="sxs-lookup"><span data-stu-id="ca797-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="ca797-237">Fuerza que el back-end omita la ejecución paso a paso en scripts con una dirección URL que coincide con uno de los patrones.</span><span class="sxs-lookup"><span data-stu-id="ca797-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="ca797-238">El depurador intentará dejar la secuencia de comandos de blackboxed realizando ' paso a paso ' varias veces, por último, recurriendo a ' paso hacia fuera ' si no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca797-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-240">modos</span><span class="sxs-lookup"><span data-stu-id="ca797-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="ca797-241">Matriz de RegExpS que se usará para comprobar la dirección URL del script para el estado de Blackbox.</span><span class="sxs-lookup"><span data-stu-id="ca797-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="ca797-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="ca797-243">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-243">Experimental.</span></span> </b></span><span data-ttu-id="ca797-244">Microsoft: establece la propiedad de depurador especificada en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ca797-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="ca797-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-247">Microsoft: el identificador de propiedad (es decir, msDebuggerPropertyId) que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="ca797-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-248">Nuevovalor</span><span class="sxs-lookup"><span data-stu-id="ca797-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="ca797-249">Eventos</span><span class="sxs-lookup"><span data-stu-id="ca797-249">Events</span></span>

### <span data-ttu-id="ca797-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="ca797-250">scriptParsed</span></span>
<span data-ttu-id="ca797-251">Se desencadena cuando se analiza el script.</span><span class="sxs-lookup"><span data-stu-id="ca797-251">Fired when the script is parsed.</span></span> <span data-ttu-id="ca797-252">Este evento también se desencadena para todos los scripts conocidos y no recopilados al habilitar el depurador.</span><span class="sxs-lookup"><span data-stu-id="ca797-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-253">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="ca797-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="ca797-255">Identificador de la secuencia de comandos analizada.</span><span class="sxs-lookup"><span data-stu-id="ca797-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-256">url</span><span class="sxs-lookup"><span data-stu-id="ca797-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-257">Dirección URL o nombre de la secuencia de comandos analizada (si hay alguna).</span><span class="sxs-lookup"><span data-stu-id="ca797-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-258">startLine</span><span class="sxs-lookup"><span data-stu-id="ca797-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-259">Desplazamiento de línea del script en el recurso con la dirección URL dada (para etiquetas de script).</span><span class="sxs-lookup"><span data-stu-id="ca797-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-260">Columnainicio</span><span class="sxs-lookup"><span data-stu-id="ca797-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-261">Desplazamiento de columna de la secuencia de comandos en el recurso con la dirección URL proporcionada.</span><span class="sxs-lookup"><span data-stu-id="ca797-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-262">Fin</span><span class="sxs-lookup"><span data-stu-id="ca797-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-263">Última línea de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="ca797-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-264">Columnafin</span><span class="sxs-lookup"><span data-stu-id="ca797-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-265">Longitud de la última línea de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="ca797-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="ca797-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="ca797-267">Especifica el contexto de creación de script.</span><span class="sxs-lookup"><span data-stu-id="ca797-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="ca797-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="ca797-269">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-270">Dirección URL de la asignación de origen asociada con el script (si existe).</span><span class="sxs-lookup"><span data-stu-id="ca797-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-271">longitud</span><span class="sxs-lookup"><span data-stu-id="ca797-271">length</span></span> <br/> <i><span data-ttu-id="ca797-272">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="ca797-273">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-273">Experimental.</span></span> </b></span><span data-ttu-id="ca797-274">Esta longitud de script.</span><span class="sxs-lookup"><span data-stu-id="ca797-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="ca797-275">msParentId</span></span> <br/> <i><span data-ttu-id="ca797-276">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="ca797-277">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-277">Experimental.</span></span> </b></span><span data-ttu-id="ca797-278">Este es el identificador de documento principal.</span><span class="sxs-lookup"><span data-stu-id="ca797-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="ca797-279">msMimeType</span></span> <br/> <i><span data-ttu-id="ca797-280">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="ca797-281">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-281">Experimental.</span></span> </b></span><span data-ttu-id="ca797-282">Este es el tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="ca797-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="ca797-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="ca797-284">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="ca797-285">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-285">Experimental.</span></span> </b></span><span data-ttu-id="ca797-286">Indica si se trata de código dinámico.</span><span class="sxs-lookup"><span data-stu-id="ca797-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="ca797-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="ca797-288">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="ca797-289">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-289">Experimental.</span></span> </b></span><span data-ttu-id="ca797-290">Este es el identificador de documento largo.</span><span class="sxs-lookup"><span data-stu-id="ca797-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="ca797-291">breakpointResolved</span></span>
<span data-ttu-id="ca797-292">Se desencadena cuando el punto de interrupción se resuelve como una secuencia de comandos y una ubicación reales.</span><span class="sxs-lookup"><span data-stu-id="ca797-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-293">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="ca797-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="ca797-295">Identificador único de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-296">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ca797-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-297">Ubicación real del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-298">msLength</span><span class="sxs-lookup"><span data-stu-id="ca797-298">msLength</span></span> <br/> <i><span data-ttu-id="ca797-299">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="ca797-300">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-300">Experimental.</span></span> </b></span><span data-ttu-id="ca797-301">Microsoft: longitud del código (es decir, número de caracteres) en la ubicación del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-302">en pausa</span><span class="sxs-lookup"><span data-stu-id="ca797-302">paused</span></span>
<span data-ttu-id="ca797-303">Se desencadena cuando los depuradores se interrumpen por un punto de interrupción o una excepción.</span><span class="sxs-lookup"><span data-stu-id="ca797-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-304">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca797-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="ca797-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="ca797-306">Pila de llamadas: el depurador ha dejado de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="ca797-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-307">tanto</span><span class="sxs-lookup"><span data-stu-id="ca797-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="ca797-308">Valores permitidos: punto de interrupción, paso, excepción, otro</span><span class="sxs-lookup"><span data-stu-id="ca797-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="ca797-309">Motivo de la pausa.</span><span class="sxs-lookup"><span data-stu-id="ca797-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-310">data</span><span class="sxs-lookup"><span data-stu-id="ca797-310">data</span></span> <br/> <i><span data-ttu-id="ca797-311">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="ca797-312">Objeto que contiene propiedades auxiliares específicas de ruptura.</span><span class="sxs-lookup"><span data-stu-id="ca797-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="ca797-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="ca797-314">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="ca797-315">Identificadores de puntos de interrupción del posicionamiento</span><span class="sxs-lookup"><span data-stu-id="ca797-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="ca797-316">retomada</span><span class="sxs-lookup"><span data-stu-id="ca797-316">resumed</span></span>
<span data-ttu-id="ca797-317">Se desencadena cuando el depurador reanuda la ejecución.</span><span class="sxs-lookup"><span data-stu-id="ca797-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="ca797-318">Tipos</span><span class="sxs-lookup"><span data-stu-id="ca797-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="ca797-319">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="ca797-319">BreakpointId</span></span> `string`

<span data-ttu-id="ca797-320">Identificador de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ca797-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="ca797-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="ca797-321">CallFrameId</span></span> `string`

<span data-ttu-id="ca797-322">Identificador del marco de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="ca797-323">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ca797-323">Location</span></span> `object`

<span data-ttu-id="ca797-324">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ca797-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-325">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca797-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-326">scriptId</span><span class="sxs-lookup"><span data-stu-id="ca797-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="ca797-327">Identificador de script tal y como se indica en el <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="ca797-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-328">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-329">Número de línea en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="ca797-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-330">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-330">columnNumber</span></span> <br/> <i><span data-ttu-id="ca797-331">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-332">Número de columna en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="ca797-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-333">msLength</span><span class="sxs-lookup"><span data-stu-id="ca797-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-334">Microsoft: longitud del código (es decir, número de caracteres) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="ca797-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="ca797-335">BreakLocation</span></span> `object`

<span data-ttu-id="ca797-336">Interrumpir la ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ca797-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-337">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca797-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-338">scriptId</span><span class="sxs-lookup"><span data-stu-id="ca797-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="ca797-339">Identificador de script tal y como se indica en el <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="ca797-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-340">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-341">Número de línea en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="ca797-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-342">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ca797-342">columnNumber</span></span> <br/> <i><span data-ttu-id="ca797-343">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-344">Número de columna en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="ca797-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-345">msLength</span><span class="sxs-lookup"><span data-stu-id="ca797-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ca797-346">Microsoft: longitud del código (es decir, número de caracteres) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-347">tipo</span><span class="sxs-lookup"><span data-stu-id="ca797-347">type</span></span> <br/> <i><span data-ttu-id="ca797-348">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-349">Valores permitidos: debuggerStatement, Call, Return.</span><span class="sxs-lookup"><span data-stu-id="ca797-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="ca797-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="ca797-350">CallFrame</span></span> `object`

<span data-ttu-id="ca797-351">Marco de llamada de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca797-351">JavaScript call frame.</span></span> <span data-ttu-id="ca797-352">Matriz de marcos de llamadas que forman la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ca797-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-353">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca797-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="ca797-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="ca797-355">Identificador del marco de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-355">Call frame identifier.</span></span> <span data-ttu-id="ca797-356">Este identificador solo es válido cuando el depurador está en pausa.</span><span class="sxs-lookup"><span data-stu-id="ca797-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-357">functionName</span><span class="sxs-lookup"><span data-stu-id="ca797-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-358">Nombre de la función de JavaScript a la que se llama en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="ca797-359">functionLocation</span></span> <br/> <i><span data-ttu-id="ca797-360">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="ca797-361">Montaje.</span><span class="sxs-lookup"><span data-stu-id="ca797-361">Experimental.</span></span> </b></span><span data-ttu-id="ca797-362">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ca797-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-363">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ca797-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-364">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ca797-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-365">url</span><span class="sxs-lookup"><span data-stu-id="ca797-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ca797-366">Nombre de script o URL de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca797-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="ca797-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="ca797-368">Cadena de ámbitos para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-369">el</span><span class="sxs-lookup"><span data-stu-id="ca797-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="ca797-370">objeto para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="ca797-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-371">Vuelto</span><span class="sxs-lookup"><span data-stu-id="ca797-371">returnValue</span></span> <br/> <i><span data-ttu-id="ca797-372">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="ca797-373">Valor que se devuelve, si la función está en el punto devuelto.</span><span class="sxs-lookup"><span data-stu-id="ca797-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="ca797-374">Ámbito</span><span class="sxs-lookup"><span data-stu-id="ca797-374">Scope</span></span> `object`

<span data-ttu-id="ca797-375">Descripción del ámbito.</span><span class="sxs-lookup"><span data-stu-id="ca797-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ca797-376">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca797-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ca797-377">tipo</span><span class="sxs-lookup"><span data-stu-id="ca797-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="ca797-378">Valores permitidos: global, local, con, cierre, Catch, Block, script, eval, módulo</span><span class="sxs-lookup"><span data-stu-id="ca797-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="ca797-379">Tipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ca797-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-380">objeto</span><span class="sxs-lookup"><span data-stu-id="ca797-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="ca797-381">Objeto que representa el ámbito.</span><span class="sxs-lookup"><span data-stu-id="ca797-381">Object representing the scope.</span></span> <span data-ttu-id="ca797-382">Para <code>global</code> y <code>with</code> ámbitos, representa el objeto real; para el resto de los ámbitos, se trata de las variables de ámbito de la enumeración de objetos transitorias artificiales como sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="ca797-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-383">name</span><span class="sxs-lookup"><span data-stu-id="ca797-383">name</span></span> <br/> <i><span data-ttu-id="ca797-384">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-385">startLocation</span><span class="sxs-lookup"><span data-stu-id="ca797-385">startLocation</span></span> <br/> <i><span data-ttu-id="ca797-386">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-387">Ubicación en el código fuente donde comienza el ámbito</span><span class="sxs-lookup"><span data-stu-id="ca797-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ca797-388">endLocation</span><span class="sxs-lookup"><span data-stu-id="ca797-388">endLocation</span></span> <br/> <i><span data-ttu-id="ca797-389">opcional</span><span class="sxs-lookup"><span data-stu-id="ca797-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="ca797-390">Ubicación en el código fuente donde el ámbito finaliza</span><span class="sxs-lookup"><span data-stu-id="ca797-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="ca797-391">Dependencias</span><span class="sxs-lookup"><span data-stu-id="ca797-391">Dependencies</span></span>

[<span data-ttu-id="ca797-392">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ca797-392">Runtime</span></span>](runtime.md)
