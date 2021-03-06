---
description: Referencia del protocolo DevTools versión 0.1 (EdgeHTML) para el dominio depurador.  El dominio del depurador expone las capacidades de depuración de JavaScript.  Permite establecer y quitar puntos de interrupción, recorrer la ejecución, explorar seguimientos de pila, etc.
title: 'Dominio del depurador: protocolo DevTools versión 0.1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397681"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="73adb-105">Dominio del depurador: protocolo DevTools versión 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="73adb-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="73adb-106">El dominio del depurador expone las capacidades de depuración de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73adb-106">Debugger domain exposes JavaScript debugging capabilities.</span></span>  <span data-ttu-id="73adb-107">Permite establecer y quitar puntos de interrupción, recorrer la ejecución, explorar seguimientos de pila, etc.</span><span class="sxs-lookup"><span data-stu-id="73adb-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="73adb-108">Clasificación</span><span class="sxs-lookup"><span data-stu-id="73adb-108">Classification</span></span> | <span data-ttu-id="73adb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="73adb-109">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="73adb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="73adb-110">Methods</span></span>](#methods) | <span data-ttu-id="73adb-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepout), [stepOut](#stepinto), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="73adb-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [<span data-ttu-id="73adb-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="73adb-112">Events</span></span>](#events) | <span data-ttu-id="73adb-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="73adb-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [<span data-ttu-id="73adb-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="73adb-114">Types</span></span>](#types) | <span data-ttu-id="73adb-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="73adb-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [<span data-ttu-id="73adb-116">Dependencias</span><span class="sxs-lookup"><span data-stu-id="73adb-116">Dependencies</span></span>](#dependencies) | [<span data-ttu-id="73adb-117">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="73adb-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="73adb-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="73adb-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="73adb-119">habilitar</span><span class="sxs-lookup"><span data-stu-id="73adb-119">enable</span></span>  

<span data-ttu-id="73adb-120">Habilita el depurador para la página determinada.</span><span class="sxs-lookup"><span data-stu-id="73adb-120">Enables debugger for the given page.</span></span>  <span data-ttu-id="73adb-121">Los clientes no deben asumir que la depuración se ha habilitado hasta que se reciba el resultado de este comando.</span><span class="sxs-lookup"><span data-stu-id="73adb-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="73adb-122">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="73adb-122">disable</span></span>  

<span data-ttu-id="73adb-123">Deshabilita el depurador para una página determinada.</span><span class="sxs-lookup"><span data-stu-id="73adb-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="73adb-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="73adb-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="73adb-125">Devuelve posibles ubicaciones para el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-125">Returns possible locations for breakpoint.</span></span>  <span data-ttu-id="73adb-126">scriptId en las ubicaciones de intervalo inicial y final debe ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="73adb-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="73adb-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-127">Parameters</span></span> | <span data-ttu-id="73adb-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-128">Type</span></span> | <span data-ttu-id="73adb-129">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-130">start</span><span class="sxs-lookup"><span data-stu-id="73adb-130">start</span></span> | [<span data-ttu-id="73adb-131">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-131">Location</span></span>](#location) | <span data-ttu-id="73adb-132">Inicio del intervalo en el que buscar posibles ubicaciones de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="73adb-133">terminar</span><span class="sxs-lookup"><span data-stu-id="73adb-133">end</span></span> | [<span data-ttu-id="73adb-134">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-134">Location</span></span>](#location) | <span data-ttu-id="73adb-135">Fin del intervalo para buscar posibles ubicaciones de punto de interrupción en \(excluding\).</span><span class="sxs-lookup"><span data-stu-id="73adb-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="73adb-136">Cuando no se especifica, el final de los scripts se usa como fin del intervalo.</span><span class="sxs-lookup"><span data-stu-id="73adb-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="73adb-137">Devuelve</span><span class="sxs-lookup"><span data-stu-id="73adb-137">Returns</span></span> | <span data-ttu-id="73adb-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-138">Type</span></span> | <span data-ttu-id="73adb-139">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-140">ubicaciones</span><span class="sxs-lookup"><span data-stu-id="73adb-140">locations</span></span> | [<span data-ttu-id="73adb-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="73adb-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="73adb-142">Lista de las posibles ubicaciones de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="73adb-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="73adb-143">setBreakpointsActive</span></span>  

<span data-ttu-id="73adb-144">Activa/desactiva todos los puntos de interrupción de la página.</span><span class="sxs-lookup"><span data-stu-id="73adb-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="73adb-145">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-145">Parameters</span></span> | <span data-ttu-id="73adb-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-146">Type</span></span> | <span data-ttu-id="73adb-147">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-148">activa</span><span class="sxs-lookup"><span data-stu-id="73adb-148">active</span></span> | `boolean` | <span data-ttu-id="73adb-149">Nuevo valor para el estado activo de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-149">New value for breakpoints active state.</span></span> |  

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="73adb-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="73adb-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="73adb-151">Establece el punto de interrupción de JavaScript en una ubicación determinada especificada por dirección URL o url regex.</span><span class="sxs-lookup"><span data-stu-id="73adb-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="73adb-152">Una vez emitido este comando, todos los scripts de análisis existentes tendrán puntos de interrupción resueltos y devueltos en la `locations` propiedad.</span><span class="sxs-lookup"><span data-stu-id="73adb-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="73adb-153">El análisis de scripts de coincidencia adicional dará como resultado la emisión `breakpointResolved` de eventos posteriores.</span><span class="sxs-lookup"><span data-stu-id="73adb-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="73adb-154">Este punto de interrupción lógico sobrevivirá a las recargas de página.</span><span class="sxs-lookup"><span data-stu-id="73adb-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="73adb-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-155">Parameters</span></span> | <span data-ttu-id="73adb-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-156">Type</span></span> | <span data-ttu-id="73adb-157">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="73adb-158">lineNumber</span></span> | `integer` | <span data-ttu-id="73adb-159">Número de línea en el que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-159">Line number to set breakpoint at.</span></span> |  
| <span data-ttu-id="73adb-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-160">url  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-161">Dirección URL de los recursos en los que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="73adb-162">urlRegex \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-162">urlRegex  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-163">Patrón Regex para las direcciones URL de los recursos en las que se establecen los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="73adb-164">O `url` `urlRegex` debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="73adb-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="73adb-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-165">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="73adb-166">Desplazamiento en la línea en la que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="73adb-167">condición \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-167">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-168">Expresión que se usará como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-168">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="73adb-169">Cuando se especifica, el depurador solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="73adb-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="73adb-170">Devuelve</span><span class="sxs-lookup"><span data-stu-id="73adb-170">Returns</span></span> | <span data-ttu-id="73adb-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-171">Type</span></span> | <span data-ttu-id="73adb-172">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-173">breakpointId</span></span> | [<span data-ttu-id="73adb-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="73adb-175">Identificador del punto de interrupción creado para obtener más referencia.</span><span class="sxs-lookup"><span data-stu-id="73adb-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="73adb-176">ubicaciones</span><span class="sxs-lookup"><span data-stu-id="73adb-176">locations</span></span> | [<span data-ttu-id="73adb-177">Location[]</span><span class="sxs-lookup"><span data-stu-id="73adb-177">Location[]</span></span>](#location) | <span data-ttu-id="73adb-178">Lista de las ubicaciones en las que se resolvió este punto de interrupción tras su adición.</span><span class="sxs-lookup"><span data-stu-id="73adb-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="73adb-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="73adb-179">setBreakpoint</span></span>  

<span data-ttu-id="73adb-180">Establece el punto de interrupción de JavaScript en una ubicación determinada.</span><span class="sxs-lookup"><span data-stu-id="73adb-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="73adb-181">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-181">Parameters</span></span> | <span data-ttu-id="73adb-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-182">Type</span></span> | <span data-ttu-id="73adb-183">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-184">ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-184">location</span></span> | [<span data-ttu-id="73adb-185">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-185">Location</span></span>](#location) | <span data-ttu-id="73adb-186">Ubicación en la que se establece el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="73adb-187">condición \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-187">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-188">Expresión que se usará como condición de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="73adb-189">Cuando se especifica, el depurador solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="73adb-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="73adb-190">Devuelve</span><span class="sxs-lookup"><span data-stu-id="73adb-190">Returns</span></span> | <span data-ttu-id="73adb-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-191">Type</span></span> | <span data-ttu-id="73adb-192">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-193">breakpointId</span></span> | [<span data-ttu-id="73adb-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="73adb-195">Identificador del punto de interrupción creado para obtener más referencia.</span><span class="sxs-lookup"><span data-stu-id="73adb-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="73adb-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="73adb-196">actualLocation</span></span> | [<span data-ttu-id="73adb-197">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-197">Location</span></span>](#location) | <span data-ttu-id="73adb-198">Ubicación en la que se resolvió este punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="73adb-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="73adb-199">removeBreakpoint</span></span>  

<span data-ttu-id="73adb-200">Quita el punto de interrupción de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73adb-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="73adb-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-201">Parameters</span></span> | <span data-ttu-id="73adb-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-202">Type</span></span> | <span data-ttu-id="73adb-203">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-204">breakpointId</span></span> | [<span data-ttu-id="73adb-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="73adb-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="73adb-206">stepOver</span></span>  

<span data-ttu-id="73adb-207">Pasos sobre la instrucción.</span><span class="sxs-lookup"><span data-stu-id="73adb-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="73adb-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="73adb-208">stepInto</span></span>  

<span data-ttu-id="73adb-209">Pasos en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="73adb-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="73adb-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="73adb-210">stepOut</span></span>  

<span data-ttu-id="73adb-211">Sale de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="73adb-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="73adb-212">pause</span><span class="sxs-lookup"><span data-stu-id="73adb-212">pause</span></span>  

<span data-ttu-id="73adb-213">Se detiene en la siguiente instrucción JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73adb-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="73adb-214">resume</span><span class="sxs-lookup"><span data-stu-id="73adb-214">resume</span></span>  

<span data-ttu-id="73adb-215">Reanuda la ejecución de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73adb-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="73adb-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="73adb-216">getScriptSource</span></span>  

<span data-ttu-id="73adb-217">Devuelve el origen del script con un identificador determinado.</span><span class="sxs-lookup"><span data-stu-id="73adb-217">Returns source for the script with given ID.</span></span>  

| <span data-ttu-id="73adb-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-218">Parameters</span></span> | <span data-ttu-id="73adb-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-219">Type</span></span> | <span data-ttu-id="73adb-220">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-221">scriptId</span></span> | [<span data-ttu-id="73adb-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="73adb-223">Id. del script para obtener el origen.</span><span class="sxs-lookup"><span data-stu-id="73adb-223">ID of the script to get source for.</span></span> |  
| <span data-ttu-id="73adb-224">Devuelve</span><span class="sxs-lookup"><span data-stu-id="73adb-224">Returns</span></span> | <span data-ttu-id="73adb-225">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-225">Type</span></span> | <span data-ttu-id="73adb-226">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-226">Details</span></span> |  
|<span data-ttu-id="73adb-227">:---</span><span class="sxs-lookup"><span data-stu-id="73adb-227">:---</span></span> |<span data-ttu-id="73adb-228">:---</span><span class="sxs-lookup"><span data-stu-id="73adb-228">:---</span></span> |<span data-ttu-id="73adb-229">:---</span><span class="sxs-lookup"><span data-stu-id="73adb-229">:---</span></span> |  
| <span data-ttu-id="73adb-230">scriptSource</span><span class="sxs-lookup"><span data-stu-id="73adb-230">scriptSource</span></span> | `string` | <span data-ttu-id="73adb-231">Origen de script.</span><span class="sxs-lookup"><span data-stu-id="73adb-231">Script source.</span></span> |  

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="73adb-232">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="73adb-232">setPauseOnExceptions</span></span>  

<span data-ttu-id="73adb-233">Define la pausa en el estado de excepciones.</span><span class="sxs-lookup"><span data-stu-id="73adb-233">Defines pause on exceptions state.</span></span>  <span data-ttu-id="73adb-234">Se puede establecer para detener todas las excepciones, excepciones no detectadas o ninguna excepción.</span><span class="sxs-lookup"><span data-stu-id="73adb-234">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="73adb-235">La pausa inicial en el estado de excepciones es `none` .</span><span class="sxs-lookup"><span data-stu-id="73adb-235">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="73adb-236">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-236">Parameters</span></span> | <span data-ttu-id="73adb-237">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-237">Type</span></span> | <span data-ttu-id="73adb-238">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-239">state</span><span class="sxs-lookup"><span data-stu-id="73adb-239">state</span></span> | `string` | <span data-ttu-id="73adb-240">Pausa en el modo de excepciones.</span><span class="sxs-lookup"><span data-stu-id="73adb-240">Pause on exceptions mode.</span></span>  <span data-ttu-id="73adb-241">Valores permitidos:  `none` `uncaught` , y</span><span class="sxs-lookup"><span data-stu-id="73adb-241">Allowed values:  `none`, `uncaught`, and</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="73adb-242">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="73adb-242">evaluateOnCallFrame</span></span>  

<span data-ttu-id="73adb-243">Evalúa la expresión en un marco de llamada determinado.</span><span class="sxs-lookup"><span data-stu-id="73adb-243">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="73adb-244">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-244">Parameters</span></span> | <span data-ttu-id="73adb-245">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-245">Type</span></span> | <span data-ttu-id="73adb-246">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-246">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-247">callFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-247">callFrameId</span></span> | [<span data-ttu-id="73adb-248">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-248">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="73adb-249">Identificador de marco de llamada para evaluar.</span><span class="sxs-lookup"><span data-stu-id="73adb-249">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="73adb-250">expresión</span><span class="sxs-lookup"><span data-stu-id="73adb-250">expression</span></span> | `string` | <span data-ttu-id="73adb-251">Expresión que se debe evaluar.</span><span class="sxs-lookup"><span data-stu-id="73adb-251">Expression to evaluate.</span></span> |  
| <span data-ttu-id="73adb-252">Devuelve</span><span class="sxs-lookup"><span data-stu-id="73adb-252">Returns</span></span> | <span data-ttu-id="73adb-253">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-253">Type</span></span> | <span data-ttu-id="73adb-254">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-254">Details</span></span> |  
|<span data-ttu-id="73adb-255">:---</span><span class="sxs-lookup"><span data-stu-id="73adb-255">:---</span></span> |<span data-ttu-id="73adb-256">:---</span><span class="sxs-lookup"><span data-stu-id="73adb-256">:---</span></span> |<span data-ttu-id="73adb-257">:---</span><span class="sxs-lookup"><span data-stu-id="73adb-257">:---</span></span> |  
| <span data-ttu-id="73adb-258">resultado</span><span class="sxs-lookup"><span data-stu-id="73adb-258">result</span></span> | [<span data-ttu-id="73adb-259">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="73adb-259">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="73adb-260">Contenedor de objetos para el resultado de evaluación.</span><span class="sxs-lookup"><span data-stu-id="73adb-260">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="73adb-261">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="73adb-261">setVariableValue</span></span>  

<span data-ttu-id="73adb-262">Cambia el valor de variable en un fotograma de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-262">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="73adb-263">Los ámbitos basados en objetos no son compatibles y deben mutarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="73adb-263">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="73adb-264">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-264">Parameters</span></span> | <span data-ttu-id="73adb-265">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-265">Type</span></span> | <span data-ttu-id="73adb-266">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-266">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-267">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="73adb-267">scopeNumber</span></span> | `integer` | <span data-ttu-id="73adb-268">Número de ámbito basado en 0 tal como se insumía en la cadena de ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-268">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="73adb-269">Solo `local` se permiten , y los tipos de `closure` `catch` ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-269">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="73adb-270">Otros ámbitos se pueden manipular manualmente.</span><span class="sxs-lookup"><span data-stu-id="73adb-270">Other scopes could be manipulated manually.</span></span> |  
| <span data-ttu-id="73adb-271">variableName</span><span class="sxs-lookup"><span data-stu-id="73adb-271">variableName</span></span> | `string` | <span data-ttu-id="73adb-272">Nombre de variable.</span><span class="sxs-lookup"><span data-stu-id="73adb-272">Variable name.</span></span> |  
| <span data-ttu-id="73adb-273">newValue</span><span class="sxs-lookup"><span data-stu-id="73adb-273">newValue</span></span> | [<span data-ttu-id="73adb-274">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="73adb-274">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="73adb-275">Nuevo valor de variable.</span><span class="sxs-lookup"><span data-stu-id="73adb-275">New variable value.</span></span> |  
| <span data-ttu-id="73adb-276">callFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-276">callFrameId</span></span> | [<span data-ttu-id="73adb-277">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-277">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="73adb-278">Id. de trama de llamada que contiene variable.</span><span class="sxs-lookup"><span data-stu-id="73adb-278">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="73adb-279">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="73adb-279">setBlackboxPatterns</span></span>  

<span data-ttu-id="73adb-280">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-280">**Experimental**.</span></span>  <span data-ttu-id="73adb-281">Reemplace los patrones de la caja negra anteriores por los pasados.</span><span class="sxs-lookup"><span data-stu-id="73adb-281">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="73adb-282">Fuerza al back-end a omitir el paso a paso o la pausa en scripts con una dirección URL que coincida con uno de los patrones.</span><span class="sxs-lookup"><span data-stu-id="73adb-282">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="73adb-283">El depurador intentará dejar el script en caja negra realizando varias veces, finalmente recurriendo `step in` a si no se ejecuta `step out` correctamente.</span><span class="sxs-lookup"><span data-stu-id="73adb-283">The debugger will try to leave blackboxed script by performing `step in` several times, finally resorting to `step out` if unsuccessful.</span></span>  

| <span data-ttu-id="73adb-284">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-284">Parameters</span></span> | <span data-ttu-id="73adb-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-285">Type</span></span> | <span data-ttu-id="73adb-286">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-286">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-287">patrones</span><span class="sxs-lookup"><span data-stu-id="73adb-287">patterns</span></span> | `string[]` | <span data-ttu-id="73adb-288">Matriz de regexps que se usará para comprobar la dirección URL del script para el estado de la caja negra.</span><span class="sxs-lookup"><span data-stu-id="73adb-288">Array of regexps that will be used to check script url for blackbox state.</span></span> |  

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="73adb-289">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="73adb-289">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="73adb-290">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-290">**Experimental**.</span></span>  <span data-ttu-id="73adb-291">Microsoft: establece la propiedad depurador especificada en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="73adb-291">Microsoft:  Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="73adb-292">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-292">Parameters</span></span> | <span data-ttu-id="73adb-293">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-293">Type</span></span> | <span data-ttu-id="73adb-294">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-294">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-295">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="73adb-295">debuggerPropertyId</span></span> | `string` | <span data-ttu-id="73adb-296">Microsoft: el identificador de propiedad \(es decir, msDebuggerPropertyId\) que se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="73adb-296">Microsoft: The property ID \(i.e. msDebuggerPropertyId\) to set.</span></span> |  
| <span data-ttu-id="73adb-297">newValue</span><span class="sxs-lookup"><span data-stu-id="73adb-297">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="73adb-298">Eventos</span><span class="sxs-lookup"><span data-stu-id="73adb-298">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="73adb-299">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="73adb-299">scriptParsed</span></span>  

<span data-ttu-id="73adb-300">Se desencadena cuando se analiza el script.</span><span class="sxs-lookup"><span data-stu-id="73adb-300">Fired when the script is parsed.</span></span>  <span data-ttu-id="73adb-301">Este evento también se desencadena para todos los scripts conocidos y no reconocidos al habilitar el depurador.</span><span class="sxs-lookup"><span data-stu-id="73adb-301">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="73adb-302">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-302">Parameters</span></span> | <span data-ttu-id="73adb-303">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-303">Type</span></span> | <span data-ttu-id="73adb-304">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-304">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-305">scriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-305">scriptId</span></span> | [<span data-ttu-id="73adb-306">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-306">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="73adb-307">Identificador del script analizado.</span><span class="sxs-lookup"><span data-stu-id="73adb-307">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="73adb-308">url</span><span class="sxs-lookup"><span data-stu-id="73adb-308">url</span></span> | `string` | <span data-ttu-id="73adb-309">Dirección URL o nombre del script analizada \(si la hay\).</span><span class="sxs-lookup"><span data-stu-id="73adb-309">URL or name of the script parsed \(if any\).</span></span> |  
| <span data-ttu-id="73adb-310">startLine</span><span class="sxs-lookup"><span data-stu-id="73adb-310">startLine</span></span> | `integer` | <span data-ttu-id="73adb-311">Desplazamiento de línea del script dentro del recurso con la dirección URL especificada \(para etiquetas de script\).</span><span class="sxs-lookup"><span data-stu-id="73adb-311">Line offset of the script within the resource with given URL \(for script tags\).</span></span> |  
| <span data-ttu-id="73adb-312">startColumn</span><span class="sxs-lookup"><span data-stu-id="73adb-312">startColumn</span></span> | `integer` | <span data-ttu-id="73adb-313">Desplazamiento de columna del script dentro del recurso con una dirección URL determinada.</span><span class="sxs-lookup"><span data-stu-id="73adb-313">Column offset of the script within the resource with given URL.</span></span> |  
| <span data-ttu-id="73adb-314">endLine</span><span class="sxs-lookup"><span data-stu-id="73adb-314">endLine</span></span> | `integer` | <span data-ttu-id="73adb-315">Última línea del script.</span><span class="sxs-lookup"><span data-stu-id="73adb-315">Last line of the script.</span></span> |  
| <span data-ttu-id="73adb-316">endColumn</span><span class="sxs-lookup"><span data-stu-id="73adb-316">endColumn</span></span> | `integer` | <span data-ttu-id="73adb-317">Longitud de la última línea del script.</span><span class="sxs-lookup"><span data-stu-id="73adb-317">Length of the last line of the script.</span></span> |  
| <span data-ttu-id="73adb-318">executionContextId</span><span class="sxs-lookup"><span data-stu-id="73adb-318">executionContextId</span></span> | [<span data-ttu-id="73adb-319">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="73adb-319">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="73adb-320">Especifica el contexto de creación de scripts.</span><span class="sxs-lookup"><span data-stu-id="73adb-320">Specifies script creation context.</span></span> |  
| <span data-ttu-id="73adb-321">sourceMapURL \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-321">sourceMapURL  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-322">Dirección URL del mapa de origen asociado con script (si lo hubiera).</span><span class="sxs-lookup"><span data-stu-id="73adb-322">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="73adb-323">length \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-323">length  \(optional\)</span></span> | `integer` | <span data-ttu-id="73adb-324">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-324">**Experimental**.</span></span>  <span data-ttu-id="73adb-325">Esta longitud de script.</span><span class="sxs-lookup"><span data-stu-id="73adb-325">This script length.</span></span> |  
| <span data-ttu-id="73adb-326">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-326">msParentId  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-327">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-327">**Experimental**.</span></span>  <span data-ttu-id="73adb-328">Este es el identificador del documento primario.</span><span class="sxs-lookup"><span data-stu-id="73adb-328">This is the parent document ID.</span></span> |  
| <span data-ttu-id="73adb-329">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-329">msMimeType  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-330">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-330">**Experimental**.</span></span>  <span data-ttu-id="73adb-331">Este es el tipo mime.</span><span class="sxs-lookup"><span data-stu-id="73adb-331">This is the mime type.</span></span> |  
| <span data-ttu-id="73adb-332">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-332">msIsDynamicCode  \(optional\)</span></span> | `boolean` | <span data-ttu-id="73adb-333">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-333">**Experimental**.</span></span>  <span data-ttu-id="73adb-334">Esto indica si se trata de código dinámico.</span><span class="sxs-lookup"><span data-stu-id="73adb-334">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="73adb-335">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-335">msLongDocumentId  \(optional\)</span></span> | `integer` | <span data-ttu-id="73adb-336">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-336">**Experimental**.</span></span>  <span data-ttu-id="73adb-337">Este es el identificador de documento largo.</span><span class="sxs-lookup"><span data-stu-id="73adb-337">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="73adb-338">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="73adb-338">breakpointResolved</span></span>  

<span data-ttu-id="73adb-339">Se desencadena cuando el punto de interrupción se resuelve en un script y una ubicación reales.</span><span class="sxs-lookup"><span data-stu-id="73adb-339">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="73adb-340">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-340">Parameters</span></span> | <span data-ttu-id="73adb-341">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-341">Type</span></span> | <span data-ttu-id="73adb-342">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-342">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-343">breakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-343">breakpointId</span></span> | [<span data-ttu-id="73adb-344">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-344">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="73adb-345">Identificador único de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-345">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="73adb-346">ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-346">location</span></span> | [<span data-ttu-id="73adb-347">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-347">Location</span></span>](#location) | <span data-ttu-id="73adb-348">Ubicación real del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-348">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="73adb-349">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-349">msLength  \(optional\)</span></span> | `integer` | <span data-ttu-id="73adb-350">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-350">**Experimental**.</span></span>  <span data-ttu-id="73adb-351">Microsoft: longitud del código \(es decir, número de caracteres\) en la ubicación del punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-351">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="73adb-352">en pausa</span><span class="sxs-lookup"><span data-stu-id="73adb-352">paused</span></span>  

<span data-ttu-id="73adb-353">Se desencadena cuando los depuradores se interrumpen para un punto de interrupción o una excepción.</span><span class="sxs-lookup"><span data-stu-id="73adb-353">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="73adb-354">Parameters</span><span class="sxs-lookup"><span data-stu-id="73adb-354">Parameters</span></span> | <span data-ttu-id="73adb-355">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-355">Type</span></span> | <span data-ttu-id="73adb-356">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-356">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-357">callFrames</span><span class="sxs-lookup"><span data-stu-id="73adb-357">callFrames</span></span> | [<span data-ttu-id="73adb-358">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="73adb-358">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="73adb-359">Pila de llamadas en la que se detuvo el depurador.</span><span class="sxs-lookup"><span data-stu-id="73adb-359">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="73adb-360">motivo</span><span class="sxs-lookup"><span data-stu-id="73adb-360">reason</span></span> | `string` | <span data-ttu-id="73adb-361">Motivo de pausa.</span><span class="sxs-lookup"><span data-stu-id="73adb-361">Pause reason.</span></span>  <span data-ttu-id="73adb-362">Valores permitidos:  `breakpoint` `step` , , `exception` y</span><span class="sxs-lookup"><span data-stu-id="73adb-362">Allowed values:  `breakpoint`, `step`, `exception`, and</span></span> `other` |  
| <span data-ttu-id="73adb-363">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-363">data  \(optional\)</span></span> | `object` | <span data-ttu-id="73adb-364">Objeto que contiene propiedades auxiliares específicas de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-364">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="73adb-365">hitBreakpoints \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-365">hitBreakpoints  \(optional\)</span></span> | `string[]` | <span data-ttu-id="73adb-366">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="73adb-366">Hit breakpoints IDs</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="73adb-367">reanudado</span><span class="sxs-lookup"><span data-stu-id="73adb-367">resumed</span></span>  

<span data-ttu-id="73adb-368">Se desencadena cuando el depurador reanuda la ejecución.</span><span class="sxs-lookup"><span data-stu-id="73adb-368">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="73adb-369">Tipos</span><span class="sxs-lookup"><span data-stu-id="73adb-369">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="73adb-370">Cadena BreakpointId</span><span class="sxs-lookup"><span data-stu-id="73adb-370">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="73adb-371">Identificador de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="73adb-371">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="73adb-372">Cadena CallFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-372">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="73adb-373">Identificador de marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-373">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="73adb-374">Location (objeto)</span><span class="sxs-lookup"><span data-stu-id="73adb-374">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="73adb-375">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="73adb-375">Location in the source code.</span></span>  

| <span data-ttu-id="73adb-376">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73adb-376">Properties</span></span> | <span data-ttu-id="73adb-377">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-377">Type</span></span> | <span data-ttu-id="73adb-378">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-378">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-379">scriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-379">scriptId</span></span> | [<span data-ttu-id="73adb-380">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-380">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="73adb-381">Identificador de script como se ha notificado en `Debugger.scriptParsed` el archivo .</span><span class="sxs-lookup"><span data-stu-id="73adb-381">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="73adb-382">lineNumber</span><span class="sxs-lookup"><span data-stu-id="73adb-382">lineNumber</span></span> | `integer` | <span data-ttu-id="73adb-383">Número de línea en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="73adb-383">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="73adb-384">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-384">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="73adb-385">Número de columna en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="73adb-385">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="73adb-386">msLength</span><span class="sxs-lookup"><span data-stu-id="73adb-386">msLength</span></span> | `integer` | <span data-ttu-id="73adb-387">Microsoft: longitud del código \(es decir, número de caracteres\) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-387">Microsoft: Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="73adb-388">BreakLocation (objeto)</span><span class="sxs-lookup"><span data-stu-id="73adb-388">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="73adb-389">Ubicación de interrupción en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="73adb-389">Break location in the source code.</span></span>  

| <span data-ttu-id="73adb-390">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73adb-390">Properties</span></span> | <span data-ttu-id="73adb-391">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-391">Type</span></span> | <span data-ttu-id="73adb-392">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-392">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-393">scriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-393">scriptId</span></span> | [<span data-ttu-id="73adb-394">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="73adb-394">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="73adb-395">Identificador de script como se ha notificado en `Debugger.scriptParsed` el archivo .</span><span class="sxs-lookup"><span data-stu-id="73adb-395">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="73adb-396">lineNumber</span><span class="sxs-lookup"><span data-stu-id="73adb-396">lineNumber</span></span> | `integer` | <span data-ttu-id="73adb-397">Número de línea en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="73adb-397">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="73adb-398">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-398">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="73adb-399">Número de columna en el script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="73adb-399">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="73adb-400">msLength</span><span class="sxs-lookup"><span data-stu-id="73adb-400">msLength</span></span> | `integer` | <span data-ttu-id="73adb-401">Microsoft: longitud del código \(es decir, número de caracteres\) en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-401">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="73adb-402">tipo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-402">type  \(optional\)</span></span> | `string` | <span data-ttu-id="73adb-403">Valores permitidos:  `debuggerStatement` `call` , y</span><span class="sxs-lookup"><span data-stu-id="73adb-403">Allowed values:  `debuggerStatement`, `call`, and</span></span> `return` |  

---  

### <a name="callframe-object"></a><span data-ttu-id="73adb-404">CallFrame (objeto)</span><span class="sxs-lookup"><span data-stu-id="73adb-404">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="73adb-405">Marco de llamada de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73adb-405">JavaScript call frame.</span></span>  <span data-ttu-id="73adb-406">La matriz de marcos de llamadas forma la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="73adb-406">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="73adb-407">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73adb-407">Properties</span></span> | <span data-ttu-id="73adb-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-408">Type</span></span> | <span data-ttu-id="73adb-409">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-409">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-410">callFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-410">callFrameId</span></span> | [<span data-ttu-id="73adb-411">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="73adb-411">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="73adb-412">Identificador de marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-412">Call frame identifier.</span></span>  <span data-ttu-id="73adb-413">Este identificador solo es válido mientras el depurador está en pausa.</span><span class="sxs-lookup"><span data-stu-id="73adb-413">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="73adb-414">functionName</span><span class="sxs-lookup"><span data-stu-id="73adb-414">functionName</span></span> | `string` | <span data-ttu-id="73adb-415">Nombre de la función JavaScript llamada en este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-415">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="73adb-416">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-416">functionLocation  \(optional\)</span></span> | [<span data-ttu-id="73adb-417">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-417">Location</span></span>](#location) | <span data-ttu-id="73adb-418">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="73adb-418">**Experimental**.</span></span>  <span data-ttu-id="73adb-419">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="73adb-419">Location in the source code.</span></span> |  
| <span data-ttu-id="73adb-420">ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-420">location</span></span> | [<span data-ttu-id="73adb-421">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-421">Location</span></span>](#location) | <span data-ttu-id="73adb-422">Ubicación en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="73adb-422">Location in the source code.</span></span> |  
| <span data-ttu-id="73adb-423">url</span><span class="sxs-lookup"><span data-stu-id="73adb-423">url</span></span> | `string` | <span data-ttu-id="73adb-424">Dirección URL o nombre de script de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73adb-424">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="73adb-425">scopeChain</span><span class="sxs-lookup"><span data-stu-id="73adb-425">scopeChain</span></span> | [<span data-ttu-id="73adb-426">Scope[]</span><span class="sxs-lookup"><span data-stu-id="73adb-426">Scope[]</span></span>](#scope) | <span data-ttu-id="73adb-427">Cadena de ámbito para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-427">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="73adb-428">this</span><span class="sxs-lookup"><span data-stu-id="73adb-428">this</span></span> | [<span data-ttu-id="73adb-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="73adb-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="73adb-430">para este marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="73adb-430">object for this call frame.</span></span> |  
| <span data-ttu-id="73adb-431">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-431">returnValue  \(optional\)</span></span> | [<span data-ttu-id="73adb-432">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="73adb-432">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="73adb-433">Valor que se devuelve, si la función está en el punto de devolución.</span><span class="sxs-lookup"><span data-stu-id="73adb-433">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="73adb-434">Scope (objeto)</span><span class="sxs-lookup"><span data-stu-id="73adb-434">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="73adb-435">Descripción del ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-435">Scope description.</span></span>  

| <span data-ttu-id="73adb-436">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73adb-436">Properties</span></span> | <span data-ttu-id="73adb-437">Tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-437">Type</span></span> | <span data-ttu-id="73adb-438">Detalles</span><span class="sxs-lookup"><span data-stu-id="73adb-438">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="73adb-439">tipo</span><span class="sxs-lookup"><span data-stu-id="73adb-439">type</span></span> | `string` | <span data-ttu-id="73adb-440">Tipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-440">Scope type.</span></span>  <span data-ttu-id="73adb-441">Valores permitidos:  `global` , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` y</span><span class="sxs-lookup"><span data-stu-id="73adb-441">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, and</span></span> `module` |  
| <span data-ttu-id="73adb-442">objeto</span><span class="sxs-lookup"><span data-stu-id="73adb-442">object</span></span> | [<span data-ttu-id="73adb-443">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="73adb-443">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="73adb-444">Objeto que representa el ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-444">Object representing the scope.</span></span>  <span data-ttu-id="73adb-445">For y scopes representa el objeto real; para el resto de ámbitos, es un objeto transitorio artificial que enumera las variables de `global` `with` ámbito como sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="73adb-445">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="73adb-446">nombre \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-446">name  \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="73adb-447">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-447">startLocation  \(optional\)</span></span> | [<span data-ttu-id="73adb-448">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-448">Location</span></span>](#location) | <span data-ttu-id="73adb-449">Ubicación en el código fuente donde se inicia el ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-449">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="73adb-450">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="73adb-450">endLocation  \(optional\)</span></span> | [<span data-ttu-id="73adb-451">Ubicación</span><span class="sxs-lookup"><span data-stu-id="73adb-451">Location</span></span>](#location) | <span data-ttu-id="73adb-452">Ubicación en el código fuente donde finaliza el ámbito.</span><span class="sxs-lookup"><span data-stu-id="73adb-452">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="73adb-453">Dependencias</span><span class="sxs-lookup"><span data-stu-id="73adb-453">Dependencies</span></span>  

[<span data-ttu-id="73adb-454">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="73adb-454">Runtime</span></span>](./runtime.md)  
