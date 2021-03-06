---
description: Referencia del protocolo DevTools versión 0.2 (EdgeHTML) para el dominio depurador. El dominio del depurador expone las capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, recorrer la ejecución, explorar seguimientos de pila, etc.
title: 'Dominio del depurador: protocolo DevTools versión 0.2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 00c410812edd4d11e9904a489955e7fd218a7e5d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398178"
---
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="e4359-105">Dominio del depurador: protocolo DevTools versión 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e4359-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="e4359-106">El dominio del depurador expone las capacidades de depuración de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="e4359-107">Permite establecer y quitar puntos de interrupción, recorrer la ejecución, explorar seguimientos de pila, etc.</span><span class="sxs-lookup"><span data-stu-id="e4359-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="e4359-108">Clasificación</span><span class="sxs-lookup"><span data-stu-id="e4359-108">Classification</span></span> | <span data-ttu-id="e4359-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4359-109">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="e4359-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4359-110">Methods</span></span>**](#methods) | <span data-ttu-id="e4359-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepout), [stepOut](#stepinto), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="e4359-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [**<span data-ttu-id="e4359-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="e4359-112">Events</span></span>**](#events) | <span data-ttu-id="e4359-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="e4359-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [**<span data-ttu-id="e4359-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="e4359-114">Types</span></span>**](#types) | <span data-ttu-id="e4359-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="e4359-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [**<span data-ttu-id="e4359-116">Dependencias</span><span class="sxs-lookup"><span data-stu-id="e4359-116">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="e4359-117">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e4359-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="e4359-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4359-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="e4359-119">habilitar</span><span class="sxs-lookup"><span data-stu-id="e4359-119">enable</span></span>  

<span data-ttu-id="e4359-120">Habilita el depurador para la página determinada.</span><span class="sxs-lookup"><span data-stu-id="e4359-120">Enables debugger for the given page.</span></span> <span data-ttu-id="e4359-121">Los clientes no deben asumir que la depuración se ha habilitado hasta que se reciba el resultado de este comando.</span><span class="sxs-lookup"><span data-stu-id="e4359-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="e4359-122">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="e4359-122">disable</span></span>  

<span data-ttu-id="e4359-123">Deshabilita el depurador para una página determinada.</span><span class="sxs-lookup"><span data-stu-id="e4359-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="e4359-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="e4359-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="e4359-125">Devuelve posibles ubicaciones para el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-125">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="e4359-126">scriptId en las ubicaciones de intervalo inicial y final debe ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="e4359-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="e4359-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-127">Parameters</span></span> | <span data-ttu-id="e4359-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-128">Type</span></span> | <span data-ttu-id="e4359-129">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-130">start</span><span class="sxs-lookup"><span data-stu-id="e4359-130">start</span></span> | [<span data-ttu-id="e4359-131">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-131">Location</span></span>](#location) | <span data-ttu-id="e4359-132">Inicio del intervalo en el que buscar posibles ubicaciones de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="e4359-133">terminar</span><span class="sxs-lookup"><span data-stu-id="e4359-133">end</span></span> | [<span data-ttu-id="e4359-134">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-134">Location</span></span>](#location) | <span data-ttu-id="e4359-135">Fin del intervalo para buscar posibles ubicaciones de punto de interrupción en \(excluding\).</span><span class="sxs-lookup"><span data-stu-id="e4359-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="e4359-136">Cuando no se especifica, el final de los scripts se usa como fin del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e4359-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="e4359-137">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e4359-137">Returns</span></span> | <span data-ttu-id="e4359-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-138">Type</span></span> | <span data-ttu-id="e4359-139">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-140">ubicaciones</span><span class="sxs-lookup"><span data-stu-id="e4359-140">locations</span></span> | [<span data-ttu-id="e4359-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="e4359-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="e4359-142">Lista de las posibles ubicaciones de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="e4359-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="e4359-143">setBreakpointsActive</span></span>  

<span data-ttu-id="e4359-144">Activa/desactiva todos los puntos de interrupción de la página.</span><span class="sxs-lookup"><span data-stu-id="e4359-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="e4359-145">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-145">Parameters</span></span> | <span data-ttu-id="e4359-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-146">Type</span></span> | <span data-ttu-id="e4359-147">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-148">activa</span><span class="sxs-lookup"><span data-stu-id="e4359-148">active</span></span> | `boolean` | <span data-ttu-id="e4359-149">Nuevo valor para el estado activo de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-149">New value for breakpoints active state.</span></span> | 

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="e4359-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="e4359-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="e4359-151">Establece el punto de interrupción de JavaScript en una ubicación determinada especificada por dirección URL o url regex.</span><span class="sxs-lookup"><span data-stu-id="e4359-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="e4359-152">Una vez emitido este comando, todos los scripts de análisis existentes tendrán puntos de interrupción resueltos y devueltos en la `locations` propiedad.</span><span class="sxs-lookup"><span data-stu-id="e4359-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="e4359-153">El análisis de scripts de coincidencia adicional dará como resultado la emisión `breakpointResolved` de eventos posteriores.</span><span class="sxs-lookup"><span data-stu-id="e4359-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="e4359-154">Este punto de interrupción lógico sobrevivirá a las recargas de página.</span><span class="sxs-lookup"><span data-stu-id="e4359-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="e4359-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-155">Parameters</span></span> | <span data-ttu-id="e4359-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-156">Type</span></span> | <span data-ttu-id="e4359-157">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e4359-158">lineNumber</span></span> | `integer` | <span data-ttu-id="e4359-159">Número de línea en el que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-159">Line number to set breakpoint at.</span></span> | 
| <span data-ttu-id="e4359-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-160">url \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-161">Dirección URL de los recursos en los que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="e4359-162">urlRegex \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-162">urlRegex \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-163">Patrón Regex para las direcciones URL de los recursos en las que se establecen los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="e4359-164">O `url` `urlRegex` debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="e4359-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="e4359-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-165">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="e4359-166">Desplazamiento en la línea en la que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="e4359-167">condición \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-167">condition \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-168">Expresión que se usará como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-168">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="e4359-169">Cuando se especifica, el depurador solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="e4359-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="e4359-170">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e4359-170">Returns</span></span> | <span data-ttu-id="e4359-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-171">Type</span></span> | <span data-ttu-id="e4359-172">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-173">breakpointId</span></span> | [<span data-ttu-id="e4359-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="e4359-175">Identificador del punto de interrupción creado para obtener más referencia.</span><span class="sxs-lookup"><span data-stu-id="e4359-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="e4359-176">ubicaciones</span><span class="sxs-lookup"><span data-stu-id="e4359-176">locations</span></span> | [<span data-ttu-id="e4359-177">Location[]</span><span class="sxs-lookup"><span data-stu-id="e4359-177">Location[]</span></span>](#location) | <span data-ttu-id="e4359-178">Lista de las ubicaciones en las que se resolvió este punto de interrupción tras su adición.</span><span class="sxs-lookup"><span data-stu-id="e4359-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="e4359-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e4359-179">setBreakpoint</span></span>  

<span data-ttu-id="e4359-180">Establece el punto de interrupción de JavaScript en una ubicación determinada.</span><span class="sxs-lookup"><span data-stu-id="e4359-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="e4359-181">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-181">Parameters</span></span> | <span data-ttu-id="e4359-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-182">Type</span></span> | <span data-ttu-id="e4359-183">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-184">ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-184">location</span></span> | [<span data-ttu-id="e4359-185">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-185">Location</span></span>](#location) | <span data-ttu-id="e4359-186">Ubicación en la que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="e4359-187">condición \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-187">condition \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-188">Expresión que se usará como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="e4359-189">Cuando se especifica, el depurador solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="e4359-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="e4359-190">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e4359-190">Returns</span></span> | <span data-ttu-id="e4359-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-191">Type</span></span> | <span data-ttu-id="e4359-192">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-193">breakpointId</span></span> | [<span data-ttu-id="e4359-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="e4359-195">Identificador del punto de interrupción creado para obtener más referencia.</span><span class="sxs-lookup"><span data-stu-id="e4359-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="e4359-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="e4359-196">actualLocation</span></span> | [<span data-ttu-id="e4359-197">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-197">Location</span></span>](#location) | <span data-ttu-id="e4359-198">Ubicación en la que se resolvió este punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="e4359-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e4359-199">removeBreakpoint</span></span>  

<span data-ttu-id="e4359-200">Quita el punto de interrupción de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="e4359-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-201">Parameters</span></span> | <span data-ttu-id="e4359-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-202">Type</span></span> | <span data-ttu-id="e4359-203">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-204">breakpointId</span></span> | [<span data-ttu-id="e4359-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="e4359-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="e4359-206">stepOver</span></span>  

<span data-ttu-id="e4359-207">Pasos sobre la instrucción.</span><span class="sxs-lookup"><span data-stu-id="e4359-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="e4359-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="e4359-208">stepInto</span></span>  

<span data-ttu-id="e4359-209">Pasos en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="e4359-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="e4359-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="e4359-210">stepOut</span></span>  

<span data-ttu-id="e4359-211">Sale de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="e4359-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="e4359-212">pause</span><span class="sxs-lookup"><span data-stu-id="e4359-212">pause</span></span>  

<span data-ttu-id="e4359-213">Se detiene en la siguiente instrucción JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="e4359-214">resume</span><span class="sxs-lookup"><span data-stu-id="e4359-214">resume</span></span>  

<span data-ttu-id="e4359-215">Reanuda la ejecución de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="e4359-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="e4359-216">getScriptSource</span></span>  

<span data-ttu-id="e4359-217">Devuelve el origen del script con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="e4359-217">Returns source for the script with given id.</span></span>  

| <span data-ttu-id="e4359-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-218">Parameters</span></span> | <span data-ttu-id="e4359-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-219">Type</span></span> | <span data-ttu-id="e4359-220">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-221">scriptId</span></span> | [<span data-ttu-id="e4359-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e4359-223">Id. del script para obtener el origen.</span><span class="sxs-lookup"><span data-stu-id="e4359-223">ID of the script to get source for.</span></span> |  

| <span data-ttu-id="e4359-224">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e4359-224">Returns</span></span> | <span data-ttu-id="e4359-225">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-225">Type</span></span> | <span data-ttu-id="e4359-226">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-226">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-227">scriptSource</span><span class="sxs-lookup"><span data-stu-id="e4359-227">scriptSource</span></span> | `string` | <span data-ttu-id="e4359-228">Origen de script.</span><span class="sxs-lookup"><span data-stu-id="e4359-228">Script source.</span></span> | 

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="e4359-229">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="e4359-229">setPauseOnExceptions</span></span>  

<span data-ttu-id="e4359-230">Define la pausa en el estado de excepciones.</span><span class="sxs-lookup"><span data-stu-id="e4359-230">Defines pause on exceptions state.</span></span>  <span data-ttu-id="e4359-231">Se puede establecer para detener todas las excepciones, excepciones no detectadas o ninguna excepción.</span><span class="sxs-lookup"><span data-stu-id="e4359-231">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="e4359-232">La pausa inicial en el estado de excepciones es `none` .</span><span class="sxs-lookup"><span data-stu-id="e4359-232">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="e4359-233">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-233">Parameters</span></span> | <span data-ttu-id="e4359-234">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-234">Type</span></span> | <span data-ttu-id="e4359-235">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-235">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-236">state</span><span class="sxs-lookup"><span data-stu-id="e4359-236">state</span></span> | `string` | <span data-ttu-id="e4359-237">Pausa en el modo de excepciones.</span><span class="sxs-lookup"><span data-stu-id="e4359-237">Pause on exceptions mode.</span></span>  <span data-ttu-id="e4359-238">Valores permitidos:  `none` , `uncaught` ,</span><span class="sxs-lookup"><span data-stu-id="e4359-238">Allowed values:  `none`, `uncaught`,</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="e4359-239">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="e4359-239">evaluateOnCallFrame</span></span>  

<span data-ttu-id="e4359-240">Evalúa la expresión en un marco de llamada determinado.</span><span class="sxs-lookup"><span data-stu-id="e4359-240">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="e4359-241">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-241">Parameters</span></span> | <span data-ttu-id="e4359-242">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-242">Type</span></span> | <span data-ttu-id="e4359-243">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-243">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-244">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-244">callFrameId</span></span> | [<span data-ttu-id="e4359-245">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-245">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="e4359-246">Identificador de marco de llamada para evaluar.</span><span class="sxs-lookup"><span data-stu-id="e4359-246">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="e4359-247">expresión</span><span class="sxs-lookup"><span data-stu-id="e4359-247">expression</span></span> | `string` | <span data-ttu-id="e4359-248">Expresión que se debe evaluar.</span><span class="sxs-lookup"><span data-stu-id="e4359-248">Expression to evaluate.</span></span> | 

| <span data-ttu-id="e4359-249">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e4359-249">Returns</span></span> | <span data-ttu-id="e4359-250">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-250">Type</span></span> | <span data-ttu-id="e4359-251">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-251">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-252">resultado</span><span class="sxs-lookup"><span data-stu-id="e4359-252">result</span></span> | [<span data-ttu-id="e4359-253">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e4359-253">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="e4359-254">Contenedor de objetos para el resultado de evaluación.</span><span class="sxs-lookup"><span data-stu-id="e4359-254">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="e4359-255">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="e4359-255">setVariableValue</span></span>  

<span data-ttu-id="e4359-256">Cambia el valor de variable en un fotograma de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-256">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="e4359-257">Los ámbitos basados en objetos no son compatibles y deben mutarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="e4359-257">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="e4359-258">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-258">Parameters</span></span> | <span data-ttu-id="e4359-259">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-259">Type</span></span> | <span data-ttu-id="e4359-260">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-260">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-261">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="e4359-261">scopeNumber</span></span> | `integer` | <span data-ttu-id="e4359-262">Número de ámbito basado en 0 tal como se insumía en la cadena de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-262">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="e4359-263">Solo `local` se permiten , y los tipos de `closure` `catch` ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-263">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="e4359-264">Otros ámbitos se pueden manipular manualmente.</span><span class="sxs-lookup"><span data-stu-id="e4359-264">Other scopes could be manipulated manually.</span></span> | 
| <span data-ttu-id="e4359-265">variableName</span><span class="sxs-lookup"><span data-stu-id="e4359-265">variableName</span></span> | `string` | <span data-ttu-id="e4359-266">Nombre de variable.</span><span class="sxs-lookup"><span data-stu-id="e4359-266">Variable name.</span></span> | 
| <span data-ttu-id="e4359-267">newValue</span><span class="sxs-lookup"><span data-stu-id="e4359-267">newValue</span></span> | [<span data-ttu-id="e4359-268">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="e4359-268">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="e4359-269">Nuevo valor de variable.</span><span class="sxs-lookup"><span data-stu-id="e4359-269">New variable value.</span></span> |  
| <span data-ttu-id="e4359-270">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-270">callFrameId</span></span> | [<span data-ttu-id="e4359-271">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-271">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="e4359-272">Id. de trama de llamada que contiene variable.</span><span class="sxs-lookup"><span data-stu-id="e4359-272">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="e4359-273">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="e4359-273">setBlackboxPatterns</span></span>  

<span data-ttu-id="e4359-274">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-274">**Experimental**.</span></span>  <span data-ttu-id="e4359-275">Reemplace los patrones de la caja negra anteriores por los pasados.</span><span class="sxs-lookup"><span data-stu-id="e4359-275">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="e4359-276">Fuerza al back-end a omitir el paso a paso o la pausa en scripts con una dirección URL que coincida con uno de los patrones.</span><span class="sxs-lookup"><span data-stu-id="e4359-276">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="e4359-277">El depurador intentará dejar el script en caja negra realizando el "step in" varias veces y, por último, recurrirá a "step out" si no se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4359-277">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>  


| <span data-ttu-id="e4359-278">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-278">Parameters</span></span> | <span data-ttu-id="e4359-279">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-279">Type</span></span> | <span data-ttu-id="e4359-280">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-280">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-281">patrones</span><span class="sxs-lookup"><span data-stu-id="e4359-281">patterns</span></span> | `string[]` | <span data-ttu-id="e4359-282">Matriz de regexps que se usará para comprobar la dirección URL del script para el estado de la caja negra.</span><span class="sxs-lookup"><span data-stu-id="e4359-282">Array of regexps that will be used to check script url for blackbox state.</span></span> | 

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="e4359-283">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="e4359-283">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="e4359-284">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-284">**Experimental**.</span></span>  <span data-ttu-id="e4359-285">Microsoft: establece la propiedad depurador especificada en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e4359-285">Microsoft: Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="e4359-286">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-286">Parameters</span></span> | <span data-ttu-id="e4359-287">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-287">Type</span></span> | <span data-ttu-id="e4359-288">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-288">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-289">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="e4359-289">debuggerPropertyId</span></span> | <span data-ttu-id="e4359-290">string</span><span class="sxs-lookup"><span data-stu-id="e4359-290">string</span></span> | <span data-ttu-id="e4359-291">Microsoft: el identificador de propiedad \(es decir, `msDebuggerPropertyId` \) que se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="e4359-291">Microsoft:  The property id \(i.e. `msDebuggerPropertyId`\) to set.</span></span> | 
| <span data-ttu-id="e4359-292">newValue</span><span class="sxs-lookup"><span data-stu-id="e4359-292">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="e4359-293">Eventos</span><span class="sxs-lookup"><span data-stu-id="e4359-293">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="e4359-294">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="e4359-294">scriptParsed</span></span>  

<span data-ttu-id="e4359-295">Se desencadena cuando se analiza el script.</span><span class="sxs-lookup"><span data-stu-id="e4359-295">Fired when the script is parsed.</span></span> <span data-ttu-id="e4359-296">Este evento también se desencadena para todos los scripts conocidos y no reconocidos al habilitar el depurador.</span><span class="sxs-lookup"><span data-stu-id="e4359-296">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="e4359-297">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-297">Parameters</span></span> | <span data-ttu-id="e4359-298">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-298">Type</span></span> | <span data-ttu-id="e4359-299">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-299">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-300">scriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-300">scriptId</span></span> | [<span data-ttu-id="e4359-301">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-301">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e4359-302">Identificador del script analizado.</span><span class="sxs-lookup"><span data-stu-id="e4359-302">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="e4359-303">url</span><span class="sxs-lookup"><span data-stu-id="e4359-303">url</span></span> | `string` | <span data-ttu-id="e4359-304">Dirección URL o nombre del script analizada \(si la hay\).</span><span class="sxs-lookup"><span data-stu-id="e4359-304">URL or name of the script parsed \(if any\).</span></span> | 
| <span data-ttu-id="e4359-305">startLine</span><span class="sxs-lookup"><span data-stu-id="e4359-305">startLine</span></span> | `integer` | <span data-ttu-id="e4359-306">Desplazamiento de línea del script dentro del recurso con la dirección URL especificada \(para etiquetas de script\).</span><span class="sxs-lookup"><span data-stu-id="e4359-306">Line offset of the script within the resource with given URL \(for script tags\).</span></span> | 
| <span data-ttu-id="e4359-307">startColumn</span><span class="sxs-lookup"><span data-stu-id="e4359-307">startColumn</span></span> | `integer` | <span data-ttu-id="e4359-308">Desplazamiento de columna del script dentro del recurso con una dirección URL determinada.</span><span class="sxs-lookup"><span data-stu-id="e4359-308">Column offset of the script within the resource with given URL.</span></span> | 
| <span data-ttu-id="e4359-309">endLine</span><span class="sxs-lookup"><span data-stu-id="e4359-309">endLine</span></span> | `integer` | <span data-ttu-id="e4359-310">Última línea del script.</span><span class="sxs-lookup"><span data-stu-id="e4359-310">Last line of the script.</span></span> | 
| <span data-ttu-id="e4359-311">endColumn</span><span class="sxs-lookup"><span data-stu-id="e4359-311">endColumn</span></span> | `integer` | <span data-ttu-id="e4359-312">Longitud de la última línea del script.</span><span class="sxs-lookup"><span data-stu-id="e4359-312">Length of the last line of the script.</span></span> | 
| <span data-ttu-id="e4359-313">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e4359-313">executionContextId</span></span> | [<span data-ttu-id="e4359-314">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="e4359-314">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="e4359-315">Especifica el contexto de creación de scripts.</span><span class="sxs-lookup"><span data-stu-id="e4359-315">Specifies script creation context.</span></span> |  
| <span data-ttu-id="e4359-316">sourceMapURL \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-316">sourceMapURL \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-317">Dirección URL del mapa de origen asociado con script (si lo hubiera).</span><span class="sxs-lookup"><span data-stu-id="e4359-317">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="e4359-318">length \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-318">length \(optional\)</span></span> | `integer` | <span data-ttu-id="e4359-319">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-319">**Experimental**.</span></span>  <span data-ttu-id="e4359-320">Esta longitud de script.</span><span class="sxs-lookup"><span data-stu-id="e4359-320">This script length.</span></span> |  
| <span data-ttu-id="e4359-321">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-321">msParentId \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-322">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-322">**Experimental**.</span></span>  <span data-ttu-id="e4359-323">Este es el identificador del documento primario.</span><span class="sxs-lookup"><span data-stu-id="e4359-323">This is the parent document ID.</span></span> |  
| <span data-ttu-id="e4359-324">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-324">msMimeType \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-325">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-325">**Experimental**.</span></span>  <span data-ttu-id="e4359-326">Este es el tipo mime.</span><span class="sxs-lookup"><span data-stu-id="e4359-326">This is the mime type.</span></span> |  
| <span data-ttu-id="e4359-327">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-327">msIsDynamicCode \(optional\)</span></span> | `boolean` | <span data-ttu-id="e4359-328">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-328">**Experimental**.</span></span>  <span data-ttu-id="e4359-329">Esto indica si se trata de código dinámico.</span><span class="sxs-lookup"><span data-stu-id="e4359-329">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="e4359-330">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-330">msLongDocumentId \(optional\)</span></span> | `integer` | <span data-ttu-id="e4359-331">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-331">**Experimental**.</span></span>  <span data-ttu-id="e4359-332">Este es el identificador de documento largo.</span><span class="sxs-lookup"><span data-stu-id="e4359-332">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="e4359-333">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="e4359-333">breakpointResolved</span></span>  

<span data-ttu-id="e4359-334">Se desencadena cuando el punto de interrupción se resuelve en un script y una ubicación reales.</span><span class="sxs-lookup"><span data-stu-id="e4359-334">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="e4359-335">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-335">Parameters</span></span> | <span data-ttu-id="e4359-336">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-336">Type</span></span> | <span data-ttu-id="e4359-337">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-337">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-338">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-338">breakpointId</span></span> | [<span data-ttu-id="e4359-339">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-339">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="e4359-340">Identificador único de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-340">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="e4359-341">ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-341">location</span></span> | [<span data-ttu-id="e4359-342">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-342">Location</span></span>](#location) | <span data-ttu-id="e4359-343">Ubicación real del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-343">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="e4359-344">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-344">msLength \(optional\)</span></span> | `integer` | <span data-ttu-id="e4359-345">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-345">**Experimental**.</span></span>  <span data-ttu-id="e4359-346">Microsoft: longitud del código \(es decir, número de caracteres\) en la ubicación del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-346">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="e4359-347">en pausa</span><span class="sxs-lookup"><span data-stu-id="e4359-347">paused</span></span>  

<span data-ttu-id="e4359-348">Se desencadena cuando los depuradores se interrumpen para un punto de interrupción o una excepción.</span><span class="sxs-lookup"><span data-stu-id="e4359-348">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="e4359-349">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4359-349">Parameters</span></span> | <span data-ttu-id="e4359-350">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-350">Type</span></span> | <span data-ttu-id="e4359-351">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-351">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-352">callFrames</span><span class="sxs-lookup"><span data-stu-id="e4359-352">callFrames</span></span> | [<span data-ttu-id="e4359-353">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="e4359-353">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="e4359-354">Pila de llamadas en la que se detuvo el depurador.</span><span class="sxs-lookup"><span data-stu-id="e4359-354">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="e4359-355">motivo</span><span class="sxs-lookup"><span data-stu-id="e4359-355">reason</span></span> | `string` |  <span data-ttu-id="e4359-356">Motivo de pausa.</span><span class="sxs-lookup"><span data-stu-id="e4359-356">Pause reason.</span></span>  <span data-ttu-id="e4359-357">Valores permitidos:  `breakpoint` `step` , , , `exception` `other` y</span><span class="sxs-lookup"><span data-stu-id="e4359-357">Allowed values:  `breakpoint`, `step`, `exception`, `other`, and</span></span> `EventListener` |  
| <span data-ttu-id="e4359-358">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-358">data \(optional\)</span></span> | `object` | <span data-ttu-id="e4359-359">Objeto que contiene propiedades auxiliares específicas de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-359">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="e4359-360">hitBreakpoints \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-360">hitBreakpoints \(optional\)</span></span> | `string[]` | <span data-ttu-id="e4359-361">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="e4359-361">Hit breakpoints IDs</span></span> |  
| <span data-ttu-id="e4359-362">asyncStackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-362">asyncStackTrace \(optional\)</span></span> | `StackTrace` | <span data-ttu-id="e4359-363">Seguimiento de pila asincrónica de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-363">JavaScript async stack trace.</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="e4359-364">reanudado</span><span class="sxs-lookup"><span data-stu-id="e4359-364">resumed</span></span>  

<span data-ttu-id="e4359-365">Se desencadena cuando el depurador reanuda la ejecución.</span><span class="sxs-lookup"><span data-stu-id="e4359-365">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="e4359-366">Tipos</span><span class="sxs-lookup"><span data-stu-id="e4359-366">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="e4359-367">Cadena BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e4359-367">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="e4359-368">Identificador de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e4359-368">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="e4359-369">Cadena CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-369">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="e4359-370">Identificador de marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-370">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="e4359-371">Location (objeto)</span><span class="sxs-lookup"><span data-stu-id="e4359-371">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="e4359-372">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="e4359-372">Location in the source code.</span></span>  

| <span data-ttu-id="e4359-373">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4359-373">Properties</span></span> | <span data-ttu-id="e4359-374">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-374">Type</span></span> | <span data-ttu-id="e4359-375">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-375">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-376">scriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-376">scriptId</span></span> | [<span data-ttu-id="e4359-377">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-377">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e4359-378">Identificador de script como se ha notificado en `Debugger.scriptParsed` el archivo .</span><span class="sxs-lookup"><span data-stu-id="e4359-378">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="e4359-379">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e4359-379">lineNumber</span></span> | `integer` | <span data-ttu-id="e4359-380">Número de línea en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e4359-380">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e4359-381">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-381">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="e4359-382">Número de columna en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e4359-382">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e4359-383">msLength</span><span class="sxs-lookup"><span data-stu-id="e4359-383">msLength</span></span> | `integer` | <span data-ttu-id="e4359-384">Microsoft: longitud del código \(es decir, número de caracteres\) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-384">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="e4359-385">BreakLocation (objeto)</span><span class="sxs-lookup"><span data-stu-id="e4359-385">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="e4359-386">Ubicación de interrupción en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="e4359-386">Break location in the source code.</span></span>  

| <span data-ttu-id="e4359-387">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4359-387">Properties</span></span> | <span data-ttu-id="e4359-388">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-388">Type</span></span> | <span data-ttu-id="e4359-389">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-390">scriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-390">scriptId</span></span> | [<span data-ttu-id="e4359-391">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e4359-391">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e4359-392">Identificador de script como se ha notificado en `Debugger.scriptParsed` el archivo .</span><span class="sxs-lookup"><span data-stu-id="e4359-392">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="e4359-393">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e4359-393">lineNumber</span></span> | `integer` | <span data-ttu-id="e4359-394">Número de línea en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e4359-394">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e4359-395">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-395">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="e4359-396">Número de columna en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e4359-396">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e4359-397">msLength</span><span class="sxs-lookup"><span data-stu-id="e4359-397">msLength</span></span> | `integer` | <span data-ttu-id="e4359-398">Microsoft: longitud del código \(es decir, número de caracteres\) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-398">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="e4359-399">tipo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-399">type \(optional\)</span></span> | `string` | <span data-ttu-id="e4359-400">Valores permitidos: debuggerStatement, call, return.</span><span class="sxs-lookup"><span data-stu-id="e4359-400">Allowed values: debuggerStatement, call, return.</span></span> |  

---  

### <a name="callframe-object"></a><span data-ttu-id="e4359-401">CallFrame (objeto)</span><span class="sxs-lookup"><span data-stu-id="e4359-401">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="e4359-402">Marco de llamada de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-402">JavaScript call frame.</span></span> <span data-ttu-id="e4359-403">La matriz de marcos de llamadas forma la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e4359-403">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="e4359-404">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4359-404">Properties</span></span> | <span data-ttu-id="e4359-405">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-405">Type</span></span> | <span data-ttu-id="e4359-406">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-406">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-407">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-407">callFrameId</span></span> | [<span data-ttu-id="e4359-408">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e4359-408">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="e4359-409">Identificador de marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-409">Call frame identifier.</span></span>  <span data-ttu-id="e4359-410">Este identificador solo es válido mientras el depurador está en pausa.</span><span class="sxs-lookup"><span data-stu-id="e4359-410">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="e4359-411">functionName</span><span class="sxs-lookup"><span data-stu-id="e4359-411">functionName</span></span> | `string` | <span data-ttu-id="e4359-412">Nombre de la función JavaScript llamada en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-412">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="e4359-413">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-413">functionLocation \(optional\)</span></span> | [<span data-ttu-id="e4359-414">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-414">Location</span></span>](#location) | <span data-ttu-id="e4359-415">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="e4359-415">**Experimental**.</span></span>  <span data-ttu-id="e4359-416">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="e4359-416">Location in the source code.</span></span> |  
| <span data-ttu-id="e4359-417">ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-417">location</span></span> | [<span data-ttu-id="e4359-418">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-418">Location</span></span>](#location) | <span data-ttu-id="e4359-419">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="e4359-419">Location in the source code.</span></span> |  
| <span data-ttu-id="e4359-420">url</span><span class="sxs-lookup"><span data-stu-id="e4359-420">url</span></span> | `string` | <span data-ttu-id="e4359-421">Dirección URL o nombre de script de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4359-421">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="e4359-422">scopeChain</span><span class="sxs-lookup"><span data-stu-id="e4359-422">scopeChain</span></span> | [<span data-ttu-id="e4359-423">Scope[]</span><span class="sxs-lookup"><span data-stu-id="e4359-423">Scope[]</span></span>](#scope) | <span data-ttu-id="e4359-424">Cadena de ámbito para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-424">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="e4359-425">this</span><span class="sxs-lookup"><span data-stu-id="e4359-425">this</span></span> | [<span data-ttu-id="e4359-426">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e4359-426">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="e4359-427">para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4359-427">object for this call frame.</span></span> |  
| <span data-ttu-id="e4359-428">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-428">returnValue \(optional\)</span></span> | [<span data-ttu-id="e4359-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e4359-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="e4359-430">Valor que se devuelve, si la función está en el punto de devolución.</span><span class="sxs-lookup"><span data-stu-id="e4359-430">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="e4359-431">Scope (objeto)</span><span class="sxs-lookup"><span data-stu-id="e4359-431">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="e4359-432">Descripción del ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-432">Scope description.</span></span>  

| <span data-ttu-id="e4359-433">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4359-433">Properties</span></span> | <span data-ttu-id="e4359-434">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-434">Type</span></span> | <span data-ttu-id="e4359-435">Detalles</span><span class="sxs-lookup"><span data-stu-id="e4359-435">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e4359-436">tipo</span><span class="sxs-lookup"><span data-stu-id="e4359-436">type</span></span> | `string` | <span data-ttu-id="e4359-437">Tipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-437">Scope type.</span></span>  <span data-ttu-id="e4359-438">Valores permitidos:  `global` , , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` `module` y</span><span class="sxs-lookup"><span data-stu-id="e4359-438">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, `module`, and</span></span> `return` |  
| <span data-ttu-id="e4359-439">objeto</span><span class="sxs-lookup"><span data-stu-id="e4359-439">object</span></span> | [<span data-ttu-id="e4359-440">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e4359-440">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="e4359-441">Objeto que representa el ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-441">Object representing the scope.</span></span>  <span data-ttu-id="e4359-442">For y scopes representa el objeto real; para el resto de ámbitos, es un objeto transitorio artificial que enumera las variables de `global` `with` ámbito como sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="e4359-442">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="e4359-443">nombre \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-443">name \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="e4359-444">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-444">startLocation \(optional\)</span></span> | [<span data-ttu-id="e4359-445">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-445">Location</span></span>](#location) | <span data-ttu-id="e4359-446">Ubicación en el código fuente donde se inicia el ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-446">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="e4359-447">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="e4359-447">endLocation \(optional\)</span></span> | [<span data-ttu-id="e4359-448">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4359-448">Location</span></span>](#location) | <span data-ttu-id="e4359-449">Ubicación en el código fuente donde finaliza el ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4359-449">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="e4359-450">Dependencias</span><span class="sxs-lookup"><span data-stu-id="e4359-450">Dependencies</span></span>  

[<span data-ttu-id="e4359-451">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e4359-451">Runtime</span></span>](./runtime.md)  
