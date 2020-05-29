---
description: Referencia del dominio de depuración. El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.
title: Dominio de depuración-DevTools Protocol versión 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 6c5d668f943a731e5ba86ed5aa2294007a432ce6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573762"
---
# <span data-ttu-id="6e319-105">Depurador</span><span class="sxs-lookup"><span data-stu-id="6e319-105">Debugger</span></span>
<span data-ttu-id="6e319-106">El dominio del depurador expone capacidades de depuración de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6e319-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="6e319-107">Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.</span><span class="sxs-lookup"><span data-stu-id="6e319-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="6e319-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e319-108">Methods</span></span>**](#methods) | <span data-ttu-id="6e319-109">[enable](#enable), [Disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [ancho](#stepover) [de es, stepInto](#stepinto) [, stepOut](#stepout), [PAUSE](#pause), [resume](#resume) [, getScriptSource, setPauseOnExceptions](#getscriptsource) [, evaluateOnCallFrame](#setpauseonexceptions) [,](#evaluateoncallframe) [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns) [, msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="6e319-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="6e319-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="6e319-110">Events</span></span>**](#events) | <span data-ttu-id="6e319-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [reanudado](#resumed)</span><span class="sxs-lookup"><span data-stu-id="6e319-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="6e319-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="6e319-112">Types</span></span>**](#types) | <span data-ttu-id="6e319-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Ubicación](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [ámbito](#scope)</span><span class="sxs-lookup"><span data-stu-id="6e319-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="6e319-114">Dependencias</span><span class="sxs-lookup"><span data-stu-id="6e319-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="6e319-115">Motores</span><span class="sxs-lookup"><span data-stu-id="6e319-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="6e319-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e319-116">Methods</span></span>

### <span data-ttu-id="6e319-117">habilitar</span><span class="sxs-lookup"><span data-stu-id="6e319-117">enable</span></span>
<span data-ttu-id="6e319-118">Habilita el depurador para la página dada.</span><span class="sxs-lookup"><span data-stu-id="6e319-118">Enables debugger for the given page.</span></span> <span data-ttu-id="6e319-119">Los clientes no deben suponer que la depuración se ha habilitado hasta que se reciba el resultado de este comando.</span><span class="sxs-lookup"><span data-stu-id="6e319-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="6e319-120">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="6e319-120">disable</span></span>
<span data-ttu-id="6e319-121">Deshabilita el depurador para la página dada.</span><span class="sxs-lookup"><span data-stu-id="6e319-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="6e319-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="6e319-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="6e319-123">Devuelve posibles ubicaciones para el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="6e319-124">scriptId en las ubicaciones de intervalo de inicio y de finalización deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="6e319-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-126">start</span><span class="sxs-lookup"><span data-stu-id="6e319-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-127">Inicio del rango para buscar posibles ubicaciones de puntos de interrupción en.</span><span class="sxs-lookup"><span data-stu-id="6e319-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-128">terminar</span><span class="sxs-lookup"><span data-stu-id="6e319-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-129">Fin del rango para buscar posibles ubicaciones de puntos de interrupción en (excepto).</span><span class="sxs-lookup"><span data-stu-id="6e319-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="6e319-130">Cuando no se especifica, el final de las secuencias de comandos se usa como fin del rango.</span><span class="sxs-lookup"><span data-stu-id="6e319-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-131">Devuelve</span><span class="sxs-lookup"><span data-stu-id="6e319-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-132">sitios</span><span class="sxs-lookup"><span data-stu-id="6e319-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="6e319-133">Lista de posibles ubicaciones de los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="6e319-134">setBreakpointsActive</span></span>
<span data-ttu-id="6e319-135">Activa o desactiva todos los puntos de interrupción de la página.</span><span class="sxs-lookup"><span data-stu-id="6e319-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-137">activa</span><span class="sxs-lookup"><span data-stu-id="6e319-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6e319-138">Nuevo valor para puntos de interrupción activo estado.</span><span class="sxs-lookup"><span data-stu-id="6e319-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="6e319-139">setBreakpointByUrl</span></span>
<span data-ttu-id="6e319-140">Establece un punto de interrupción de JavaScript en la ubicación especificada, por dirección URL o dirección URL Regex.</span><span class="sxs-lookup"><span data-stu-id="6e319-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="6e319-141">Una vez que se haya emitido este comando, todos los scripts analizados existentes tendrán los puntos de interrupción resueltos y devueltos en la <code>locations</code> propiedad.</span><span class="sxs-lookup"><span data-stu-id="6e319-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="6e319-142">Además, el análisis de scripts más parecido dará como resultado <code>breakpointResolved</code> eventos posteriores.</span><span class="sxs-lookup"><span data-stu-id="6e319-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="6e319-143">Este punto de interrupción lógico afectará a las recargas de páginas.</span><span class="sxs-lookup"><span data-stu-id="6e319-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-144">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-146">Número de línea para establecer el punto de interrupción en.</span><span class="sxs-lookup"><span data-stu-id="6e319-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-147">url</span><span class="sxs-lookup"><span data-stu-id="6e319-147">url</span></span> <br/> <i><span data-ttu-id="6e319-148">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-149">Dirección URL de los recursos para establecer el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="6e319-150">urlRegex</span></span> <br/> <i><span data-ttu-id="6e319-151">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-152">Patrón de Regex para las direcciones URL de los recursos para establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="6e319-153"><code>url</code>O <code>urlRegex</code> debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="6e319-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-154">columnNumber</span></span> <br/> <i><span data-ttu-id="6e319-155">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-156">Desplazamiento en la línea para establecer el punto de interrupción en.</span><span class="sxs-lookup"><span data-stu-id="6e319-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-157">requisito</span><span class="sxs-lookup"><span data-stu-id="6e319-157">condition</span></span> <br/> <i><span data-ttu-id="6e319-158">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-159">Expresión que se va a usar como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="6e319-160">Cuando se especifica, Debugger solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="6e319-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-161">Devuelve</span><span class="sxs-lookup"><span data-stu-id="6e319-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="6e319-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="6e319-163">Identificador del punto de interrupción creado para referencia adicional.</span><span class="sxs-lookup"><span data-stu-id="6e319-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-164">sitios</span><span class="sxs-lookup"><span data-stu-id="6e319-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="6e319-165">Lista de las ubicaciones en las que se ha resuelto este punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="6e319-166">setBreakpoint</span></span>
<span data-ttu-id="6e319-167">Establece un punto de interrupción de JavaScript en una ubicación determinada.</span><span class="sxs-lookup"><span data-stu-id="6e319-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-168">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-169">Ubicación</span><span class="sxs-lookup"><span data-stu-id="6e319-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-170">Ubicación en la que se establecerá el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-171">requisito</span><span class="sxs-lookup"><span data-stu-id="6e319-171">condition</span></span> <br/> <i><span data-ttu-id="6e319-172">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-173">Expresión que se va a usar como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="6e319-174">Cuando se especifica, Debugger solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="6e319-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-175">Devuelve</span><span class="sxs-lookup"><span data-stu-id="6e319-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="6e319-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="6e319-177">Identificador del punto de interrupción creado para referencia adicional.</span><span class="sxs-lookup"><span data-stu-id="6e319-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="6e319-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-179">Ubicación en la que se resuelve este punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="6e319-180">removeBreakpoint</span></span>
<span data-ttu-id="6e319-181">Quita el punto de interrupción de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6e319-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-182">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="6e319-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-184">Pasadas</span><span class="sxs-lookup"><span data-stu-id="6e319-184">stepOver</span></span>
<span data-ttu-id="6e319-185">Pasos sobre la instrucción.</span><span class="sxs-lookup"><span data-stu-id="6e319-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="6e319-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="6e319-186">stepInto</span></span>
<span data-ttu-id="6e319-187">Recorre los pasos de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="6e319-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="6e319-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="6e319-188">stepOut</span></span>
<span data-ttu-id="6e319-189">Recorre los pasos de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="6e319-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="6e319-190">pause</span><span class="sxs-lookup"><span data-stu-id="6e319-190">pause</span></span>
<span data-ttu-id="6e319-191">Se detiene en la siguiente instrucción de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6e319-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="6e319-192">resume</span><span class="sxs-lookup"><span data-stu-id="6e319-192">resume</span></span>
<span data-ttu-id="6e319-193">Reanuda la ejecución de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6e319-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="6e319-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="6e319-194">getScriptSource</span></span>
<span data-ttu-id="6e319-195">Devuelve el origen del script con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="6e319-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-196">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="6e319-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="6e319-198">Identificador del script para el que se va a obtener el origen.</span><span class="sxs-lookup"><span data-stu-id="6e319-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-199">Devuelve</span><span class="sxs-lookup"><span data-stu-id="6e319-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="6e319-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-201">Origen de script.</span><span class="sxs-lookup"><span data-stu-id="6e319-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="6e319-202">setPauseOnExceptions</span></span>
<span data-ttu-id="6e319-203">Define la pausa en el estado de las excepciones.</span><span class="sxs-lookup"><span data-stu-id="6e319-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="6e319-204">Puede establecerse en detener en todas las excepciones, excepciones no detectadas o sin excepciones.</span><span class="sxs-lookup"><span data-stu-id="6e319-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="6e319-205">El estado de pausa inicial en excepciones es de <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="6e319-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-207">situación</span><span class="sxs-lookup"><span data-stu-id="6e319-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="6e319-208">Valores permitidos: ninguno, no detectados, todos</span><span class="sxs-lookup"><span data-stu-id="6e319-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="6e319-209">Pausar en el modo de excepciones.</span><span class="sxs-lookup"><span data-stu-id="6e319-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="6e319-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="6e319-211">Evalúa Expression en un marco de llamada dado.</span><span class="sxs-lookup"><span data-stu-id="6e319-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="6e319-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="6e319-214">Identificador de marco de llamada que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="6e319-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-215">Expression</span><span class="sxs-lookup"><span data-stu-id="6e319-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-216">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="6e319-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-217">Devuelve</span><span class="sxs-lookup"><span data-stu-id="6e319-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-218">resultado</span><span class="sxs-lookup"><span data-stu-id="6e319-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="6e319-219">Contenedor de objetos para el resultado de evaluación.</span><span class="sxs-lookup"><span data-stu-id="6e319-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="6e319-220">setVariableValue</span></span>
<span data-ttu-id="6e319-221">Cambia el valor de la variable en un callframe.</span><span class="sxs-lookup"><span data-stu-id="6e319-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="6e319-222">Los ámbitos basados en objetos no son compatibles y se deben mutar manualmente.</span><span class="sxs-lookup"><span data-stu-id="6e319-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-223">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-225">número de base cero de ámbito que se mostraba en la cadena de ámbitos.</span><span class="sxs-lookup"><span data-stu-id="6e319-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="6e319-226">Solo se permiten los tipos de ámbito ' local ', ' cierre ' y ' Catch '.</span><span class="sxs-lookup"><span data-stu-id="6e319-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="6e319-227">Es posible manipular otros ámbitos de forma manual.</span><span class="sxs-lookup"><span data-stu-id="6e319-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-228">variableName</span><span class="sxs-lookup"><span data-stu-id="6e319-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-229">Nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6e319-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-230">Nuevovalor</span><span class="sxs-lookup"><span data-stu-id="6e319-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="6e319-231">Nuevo valor de variable.</span><span class="sxs-lookup"><span data-stu-id="6e319-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="6e319-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="6e319-233">Identificador de callframe que contiene la variable.</span><span class="sxs-lookup"><span data-stu-id="6e319-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="6e319-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="6e319-235">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-235">Experimental.</span></span> </b></span><span data-ttu-id="6e319-236">Reemplazar patrones de Blackbox anteriores por los que se hayan pasado.</span><span class="sxs-lookup"><span data-stu-id="6e319-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="6e319-237">Fuerza que el back-end omita la ejecución paso a paso en scripts con una dirección URL que coincide con uno de los patrones.</span><span class="sxs-lookup"><span data-stu-id="6e319-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="6e319-238">El depurador intentará dejar la secuencia de comandos de blackboxed realizando ' paso a paso ' varias veces, por último, recurriendo a ' paso hacia fuera ' si no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6e319-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-240">modos</span><span class="sxs-lookup"><span data-stu-id="6e319-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="6e319-241">Matriz de RegExpS que se usará para comprobar la dirección URL del script para el estado de Blackbox.</span><span class="sxs-lookup"><span data-stu-id="6e319-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="6e319-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="6e319-243">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-243">Experimental.</span></span> </b></span><span data-ttu-id="6e319-244">Microsoft: establece la propiedad de depurador especificada en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="6e319-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="6e319-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-247">Microsoft: el identificador de propiedad (es decir, msDebuggerPropertyId) que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="6e319-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-248">Nuevovalor</span><span class="sxs-lookup"><span data-stu-id="6e319-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="6e319-249">Eventos</span><span class="sxs-lookup"><span data-stu-id="6e319-249">Events</span></span>

### <span data-ttu-id="6e319-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="6e319-250">scriptParsed</span></span>
<span data-ttu-id="6e319-251">Se desencadena cuando se analiza el script.</span><span class="sxs-lookup"><span data-stu-id="6e319-251">Fired when the script is parsed.</span></span> <span data-ttu-id="6e319-252">Este evento también se desencadena para todos los scripts conocidos y no recopilados al habilitar el depurador.</span><span class="sxs-lookup"><span data-stu-id="6e319-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-253">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="6e319-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="6e319-255">Identificador de la secuencia de comandos analizada.</span><span class="sxs-lookup"><span data-stu-id="6e319-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-256">url</span><span class="sxs-lookup"><span data-stu-id="6e319-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-257">Dirección URL o nombre de la secuencia de comandos analizada (si hay alguna).</span><span class="sxs-lookup"><span data-stu-id="6e319-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-258">startLine</span><span class="sxs-lookup"><span data-stu-id="6e319-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-259">Desplazamiento de línea del script en el recurso con la dirección URL dada (para etiquetas de script).</span><span class="sxs-lookup"><span data-stu-id="6e319-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-260">Columnainicio</span><span class="sxs-lookup"><span data-stu-id="6e319-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-261">Desplazamiento de columna de la secuencia de comandos en el recurso con la dirección URL proporcionada.</span><span class="sxs-lookup"><span data-stu-id="6e319-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-262">Fin</span><span class="sxs-lookup"><span data-stu-id="6e319-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-263">Última línea de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="6e319-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-264">Columnafin</span><span class="sxs-lookup"><span data-stu-id="6e319-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-265">Longitud de la última línea de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="6e319-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="6e319-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="6e319-267">Especifica el contexto de creación de script.</span><span class="sxs-lookup"><span data-stu-id="6e319-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="6e319-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="6e319-269">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-270">Dirección URL de la asignación de origen asociada con el script (si existe).</span><span class="sxs-lookup"><span data-stu-id="6e319-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-271">longitud</span><span class="sxs-lookup"><span data-stu-id="6e319-271">length</span></span> <br/> <i><span data-ttu-id="6e319-272">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="6e319-273">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-273">Experimental.</span></span> </b></span><span data-ttu-id="6e319-274">Esta longitud de script.</span><span class="sxs-lookup"><span data-stu-id="6e319-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="6e319-275">msParentId</span></span> <br/> <i><span data-ttu-id="6e319-276">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="6e319-277">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-277">Experimental.</span></span> </b></span><span data-ttu-id="6e319-278">Este es el identificador de documento principal.</span><span class="sxs-lookup"><span data-stu-id="6e319-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="6e319-279">msMimeType</span></span> <br/> <i><span data-ttu-id="6e319-280">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="6e319-281">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-281">Experimental.</span></span> </b></span><span data-ttu-id="6e319-282">Este es el tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="6e319-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="6e319-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="6e319-284">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="6e319-285">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-285">Experimental.</span></span> </b></span><span data-ttu-id="6e319-286">Indica si se trata de código dinámico.</span><span class="sxs-lookup"><span data-stu-id="6e319-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="6e319-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="6e319-288">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="6e319-289">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-289">Experimental.</span></span> </b></span><span data-ttu-id="6e319-290">Este es el identificador de documento largo.</span><span class="sxs-lookup"><span data-stu-id="6e319-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="6e319-291">breakpointResolved</span></span>
<span data-ttu-id="6e319-292">Se desencadena cuando el punto de interrupción se resuelve como una secuencia de comandos y una ubicación reales.</span><span class="sxs-lookup"><span data-stu-id="6e319-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-293">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="6e319-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="6e319-295">Identificador único de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-296">Ubicación</span><span class="sxs-lookup"><span data-stu-id="6e319-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-297">Ubicación real del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-298">msLength</span><span class="sxs-lookup"><span data-stu-id="6e319-298">msLength</span></span> <br/> <i><span data-ttu-id="6e319-299">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="6e319-300">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-300">Experimental.</span></span> </b></span><span data-ttu-id="6e319-301">Microsoft: longitud del código (es decir, número de caracteres) en la ubicación del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-302">en pausa</span><span class="sxs-lookup"><span data-stu-id="6e319-302">paused</span></span>
<span data-ttu-id="6e319-303">Se desencadena cuando los depuradores se interrumpen por un punto de interrupción o una excepción.</span><span class="sxs-lookup"><span data-stu-id="6e319-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-304">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e319-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="6e319-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="6e319-306">Pila de llamadas: el depurador ha dejado de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6e319-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-307">tanto</span><span class="sxs-lookup"><span data-stu-id="6e319-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="6e319-308">Valores permitidos: punto de interrupción, paso, excepción, otro</span><span class="sxs-lookup"><span data-stu-id="6e319-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="6e319-309">Motivo de la pausa.</span><span class="sxs-lookup"><span data-stu-id="6e319-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-310">data</span><span class="sxs-lookup"><span data-stu-id="6e319-310">data</span></span> <br/> <i><span data-ttu-id="6e319-311">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="6e319-312">Objeto que contiene propiedades auxiliares específicas de ruptura.</span><span class="sxs-lookup"><span data-stu-id="6e319-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="6e319-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="6e319-314">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="6e319-315">Identificadores de puntos de interrupción del posicionamiento</span><span class="sxs-lookup"><span data-stu-id="6e319-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6e319-316">retomada</span><span class="sxs-lookup"><span data-stu-id="6e319-316">resumed</span></span>
<span data-ttu-id="6e319-317">Se desencadena cuando el depurador reanuda la ejecución.</span><span class="sxs-lookup"><span data-stu-id="6e319-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="6e319-318">Tipos</span><span class="sxs-lookup"><span data-stu-id="6e319-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="6e319-319">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="6e319-319">BreakpointId</span></span> `string`

<span data-ttu-id="6e319-320">Identificador de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="6e319-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="6e319-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="6e319-321">CallFrameId</span></span> `string`

<span data-ttu-id="6e319-322">Identificador del marco de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="6e319-323">Ubicación</span><span class="sxs-lookup"><span data-stu-id="6e319-323">Location</span></span> `object`

<span data-ttu-id="6e319-324">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="6e319-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-325">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e319-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-326">scriptId</span><span class="sxs-lookup"><span data-stu-id="6e319-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="6e319-327">Identificador de script tal y como se indica en el <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="6e319-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-328">lineNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-329">Número de línea en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="6e319-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-330">columnNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-330">columnNumber</span></span> <br/> <i><span data-ttu-id="6e319-331">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-332">Número de columna en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="6e319-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-333">msLength</span><span class="sxs-lookup"><span data-stu-id="6e319-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-334">Microsoft: longitud del código (es decir, número de caracteres) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="6e319-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="6e319-335">BreakLocation</span></span> `object`

<span data-ttu-id="6e319-336">Interrumpir la ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="6e319-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-337">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e319-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-338">scriptId</span><span class="sxs-lookup"><span data-stu-id="6e319-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="6e319-339">Identificador de script tal y como se indica en el <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="6e319-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-340">lineNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-341">Número de línea en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="6e319-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-342">columnNumber</span><span class="sxs-lookup"><span data-stu-id="6e319-342">columnNumber</span></span> <br/> <i><span data-ttu-id="6e319-343">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-344">Número de columna en el script (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="6e319-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-345">msLength</span><span class="sxs-lookup"><span data-stu-id="6e319-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6e319-346">Microsoft: longitud del código (es decir, número de caracteres) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-347">tipo</span><span class="sxs-lookup"><span data-stu-id="6e319-347">type</span></span> <br/> <i><span data-ttu-id="6e319-348">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-349">Valores permitidos: debuggerStatement, Call, Return.</span><span class="sxs-lookup"><span data-stu-id="6e319-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="6e319-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="6e319-350">CallFrame</span></span> `object`

<span data-ttu-id="6e319-351">Marco de llamada de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6e319-351">JavaScript call frame.</span></span> <span data-ttu-id="6e319-352">Matriz de marcos de llamadas que forman la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6e319-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-353">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e319-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="6e319-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="6e319-355">Identificador del marco de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-355">Call frame identifier.</span></span> <span data-ttu-id="6e319-356">Este identificador solo es válido cuando el depurador está en pausa.</span><span class="sxs-lookup"><span data-stu-id="6e319-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-357">functionName</span><span class="sxs-lookup"><span data-stu-id="6e319-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-358">Nombre de la función de JavaScript a la que se llama en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="6e319-359">functionLocation</span></span> <br/> <i><span data-ttu-id="6e319-360">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="6e319-361">Montaje.</span><span class="sxs-lookup"><span data-stu-id="6e319-361">Experimental.</span></span> </b></span><span data-ttu-id="6e319-362">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="6e319-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-363">Ubicación</span><span class="sxs-lookup"><span data-stu-id="6e319-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-364">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="6e319-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-365">url</span><span class="sxs-lookup"><span data-stu-id="6e319-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6e319-366">Nombre de script o URL de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6e319-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="6e319-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="6e319-368">Cadena de ámbitos para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-369">el</span><span class="sxs-lookup"><span data-stu-id="6e319-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="6e319-370">objeto para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e319-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-371">Vuelto</span><span class="sxs-lookup"><span data-stu-id="6e319-371">returnValue</span></span> <br/> <i><span data-ttu-id="6e319-372">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="6e319-373">Valor que se devuelve, si la función está en el punto devuelto.</span><span class="sxs-lookup"><span data-stu-id="6e319-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="6e319-374">Ámbito</span><span class="sxs-lookup"><span data-stu-id="6e319-374">Scope</span></span> `object`

<span data-ttu-id="6e319-375">Descripción del ámbito.</span><span class="sxs-lookup"><span data-stu-id="6e319-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6e319-376">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e319-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6e319-377">tipo</span><span class="sxs-lookup"><span data-stu-id="6e319-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="6e319-378">Valores permitidos: global, local, con, cierre, Catch, Block, script, eval, módulo</span><span class="sxs-lookup"><span data-stu-id="6e319-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="6e319-379">Tipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6e319-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-380">objeto</span><span class="sxs-lookup"><span data-stu-id="6e319-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="6e319-381">Objeto que representa el ámbito.</span><span class="sxs-lookup"><span data-stu-id="6e319-381">Object representing the scope.</span></span> <span data-ttu-id="6e319-382">Para <code>global</code> y <code>with</code> ámbitos, representa el objeto real; para el resto de los ámbitos, se trata de las variables de ámbito de la enumeración de objetos transitorias artificiales como sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e319-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-383">name</span><span class="sxs-lookup"><span data-stu-id="6e319-383">name</span></span> <br/> <i><span data-ttu-id="6e319-384">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-385">startLocation</span><span class="sxs-lookup"><span data-stu-id="6e319-385">startLocation</span></span> <br/> <i><span data-ttu-id="6e319-386">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-387">Ubicación en el código fuente donde comienza el ámbito</span><span class="sxs-lookup"><span data-stu-id="6e319-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6e319-388">endLocation</span><span class="sxs-lookup"><span data-stu-id="6e319-388">endLocation</span></span> <br/> <i><span data-ttu-id="6e319-389">opcional</span><span class="sxs-lookup"><span data-stu-id="6e319-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="6e319-390">Ubicación en el código fuente donde el ámbito finaliza</span><span class="sxs-lookup"><span data-stu-id="6e319-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="6e319-391">Dependencias</span><span class="sxs-lookup"><span data-stu-id="6e319-391">Dependencies</span></span>

[<span data-ttu-id="6e319-392">Motores</span><span class="sxs-lookup"><span data-stu-id="6e319-392">Runtime</span></span>](runtime.md)