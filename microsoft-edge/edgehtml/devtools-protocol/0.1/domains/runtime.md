---
description: Referencia del protocolo DevTools versión 0.1 (EdgeHTML) para el dominio en tiempo de ejecución.  El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript mediante objetos reflejados y de evaluación remota.  Los resultados de la evaluación se devuelven como objeto reflejado que exponen el tipo de objeto, la representación de cadenas y el identificador único que se puede usar para más referencia de objeto.  Los objetos originales se mantienen en la memoria a menos que se liberan explícitamente.
title: 'Dominio en tiempo de ejecución: protocolo DevTools versión 0.1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397695"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="cf0b9-106">Dominio en tiempo de ejecución: protocolo DevTools versión 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="cf0b9-107">El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript mediante objetos reflejados y de evaluación remota.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span>  <span data-ttu-id="cf0b9-108">Los resultados de la evaluación se devuelven como objeto reflejado que exponen el tipo de objeto, la representación de cadenas y el identificador único que se puede usar para más referencia de objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span>  <span data-ttu-id="cf0b9-109">Los objetos originales se mantienen en la memoria a menos que se liberan explícitamente.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="cf0b9-110">Clasificación</span><span class="sxs-lookup"><span data-stu-id="cf0b9-110">Classification</span></span> | <span data-ttu-id="cf0b9-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf0b9-111">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="cf0b9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-112">Methods</span></span>](#methods) | <span data-ttu-id="cf0b9-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |  
| [<span data-ttu-id="cf0b9-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-114">Events</span></span>](#events) | <span data-ttu-id="cf0b9-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |  
| [<span data-ttu-id="cf0b9-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-116">Types</span></span>](#types) | <span data-ttu-id="cf0b9-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="cf0b9-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="cf0b9-119">habilitar</span><span class="sxs-lookup"><span data-stu-id="cf0b9-119">enable</span></span>  

<span data-ttu-id="cf0b9-120">Habilita la presentación de informes del `executionContextsCleared` evento.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-120">Enables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="cf0b9-121">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="cf0b9-121">disable</span></span>  

<span data-ttu-id="cf0b9-122">Deshabilita la presentación de informes del `executionContextsCleared` evento.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-122">Disables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="evaluate"></a><span data-ttu-id="cf0b9-123">evaluar</span><span class="sxs-lookup"><span data-stu-id="cf0b9-123">evaluate</span></span>  

<span data-ttu-id="cf0b9-124">Evalúa la expresión en el objeto global.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-124">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="cf0b9-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf0b9-125">Parameters</span></span> | <span data-ttu-id="cf0b9-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-126">Type</span></span> | <span data-ttu-id="cf0b9-127">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-127">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-128">expresión</span><span class="sxs-lookup"><span data-stu-id="cf0b9-128">expression</span></span> | `string` | <span data-ttu-id="cf0b9-129">Expresión que se debe evaluar.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-129">Expression to evaluate.</span></span> |  
| <span data-ttu-id="cf0b9-130">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-130">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-131">En modo silencioso, las excepciones que se inician durante la evaluación no se notifican y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-131">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="cf0b9-132">Invalida el `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-132">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="cf0b9-133">contextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-133">contextId \(optional\)</span></span> | [<span data-ttu-id="cf0b9-134">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-134">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="cf0b9-135">Especifica en qué contexto de ejecución se debe realizar la evaluación.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-135">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="cf0b9-136">Si se omite el parámetro, la evaluación se realizará en el contexto de la página inspeccionada.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-136">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="cf0b9-137">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-137">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-138">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-138">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="cf0b9-139">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-139">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-140">Si la ejecución debe `await` ser para el valor resultante y devolver una vez que se resuelva la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-140">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="cf0b9-141">Devuelve</span><span class="sxs-lookup"><span data-stu-id="cf0b9-141">Returns</span></span> | <span data-ttu-id="cf0b9-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-142">Type</span></span> | <span data-ttu-id="cf0b9-143">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-143">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-144">resultado</span><span class="sxs-lookup"><span data-stu-id="cf0b9-144">result</span></span> | [<span data-ttu-id="cf0b9-145">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-145">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-146">Resultado de la evaluación.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-146">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="cf0b9-147">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="cf0b9-147">callFunctionOn</span></span>  

<span data-ttu-id="cf0b9-148">Las llamadas funcionan con una declaración determinada en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-148">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="cf0b9-149">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-149">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="cf0b9-150">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf0b9-150">Parameters</span></span> | <span data-ttu-id="cf0b9-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-151">Type</span></span> | <span data-ttu-id="cf0b9-152">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-152">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-153">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="cf0b9-153">functionDeclaration</span></span> | `string` | <span data-ttu-id="cf0b9-154">Declaración de la función a la que se llamará.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-154">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="cf0b9-155">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-155">objectId \(optional\)</span></span> | [<span data-ttu-id="cf0b9-156">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-156">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="cf0b9-157">Identificador del objeto en el que se debe llamar.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-157">Identifier of the object to call function on.</span></span>  <span data-ttu-id="cf0b9-158">Se `objectId` debe especificar o `executionContextId` no.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-158">Either `objectId` or `executionContextId` should be specified.</span></span>  <span data-ttu-id="cf0b9-159">objectId debe ser de la función Runtime.evaluate().</span><span class="sxs-lookup"><span data-stu-id="cf0b9-159">objectId must be from the Runtime.evaluate() function.</span></span> |  
| <span data-ttu-id="cf0b9-160">argumentos \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-160">arguments \(optional\)</span></span> | [<span data-ttu-id="cf0b9-161">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="cf0b9-161">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="cf0b9-162">Argumentos de llamada.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-162">Call arguments.</span></span>  <span data-ttu-id="cf0b9-163">Todos los argumentos de llamada deben pertenecer al mismo mundo de JavaScript que el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-163">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="cf0b9-164">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-164">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-165">En modo silencioso, las excepciones que se inician durante la evaluación no se notifican y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-165">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="cf0b9-166">Invalida el `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-166">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="cf0b9-167">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-167">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-168">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-168">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="cf0b9-169">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-169">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-170">Si la ejecución debe `await` ser para el valor resultante y devolver una vez que se resuelva la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-170">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="cf0b9-171">Devuelve</span><span class="sxs-lookup"><span data-stu-id="cf0b9-171">Returns</span></span> | <span data-ttu-id="cf0b9-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-172">Type</span></span> | <span data-ttu-id="cf0b9-173">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-173">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-174">resultado</span><span class="sxs-lookup"><span data-stu-id="cf0b9-174">result</span></span> | [<span data-ttu-id="cf0b9-175">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-175">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-176">Resultado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-176">Call result.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="cf0b9-177">getProperties</span><span class="sxs-lookup"><span data-stu-id="cf0b9-177">getProperties</span></span>  

<span data-ttu-id="cf0b9-178">Devuelve las propiedades de un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-178">Returns properties of a given object.</span></span>  <span data-ttu-id="cf0b9-179">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-179">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="cf0b9-180">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf0b9-180">Parameters</span></span> | <span data-ttu-id="cf0b9-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-181">Type</span></span> | <span data-ttu-id="cf0b9-182">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-182">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-183">objectId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-183">objectId</span></span> | [<span data-ttu-id="cf0b9-184">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-184">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="cf0b9-185">Identificador del objeto para el que se devolverán las propiedades.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-185">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="cf0b9-186">debe ser de la `Debugger.evaluateOnCallFrame()` función.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-186">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="cf0b9-187">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-187">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-188">Si `true` , devuelve propiedades que pertenecen solo al elemento en sí, no a su cadena prototipo.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-188">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="cf0b9-189">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-189">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-190">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-190">**Experimental**.</span></span>  <span data-ttu-id="cf0b9-191">Si `true` , devuelve las propiedades del accessor \(with getter/setter\) solo; tampoco se devuelven las propiedades internas.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-191">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="cf0b9-192">Devuelve</span><span class="sxs-lookup"><span data-stu-id="cf0b9-192">Returns</span></span> | <span data-ttu-id="cf0b9-193">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-193">Type</span></span> | <span data-ttu-id="cf0b9-194">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-195">resultado</span><span class="sxs-lookup"><span data-stu-id="cf0b9-195">result</span></span> | [<span data-ttu-id="cf0b9-196">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="cf0b9-196">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="cf0b9-197">Propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-197">Object properties.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="cf0b9-198">Eventos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-198">Events</span></span>  

### <a name="executioncontextscleared"></a><span data-ttu-id="cf0b9-199">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="cf0b9-199">executionContextsCleared</span></span>  

<span data-ttu-id="cf0b9-200">Se emite cuando se borraron todos los executionContexts en el explorador.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-200">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="cf0b9-201">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="cf0b9-201">exceptionThrown</span></span>  

<span data-ttu-id="cf0b9-202">Se emitió cuando se produjo la excepción y no se controló.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-202">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="cf0b9-203">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf0b9-203">Parameters</span></span> | <span data-ttu-id="cf0b9-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-204">Type</span></span> | <span data-ttu-id="cf0b9-205">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-205">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-206">marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-206">timestamp</span></span> | [<span data-ttu-id="cf0b9-207">Timestamp</span><span class="sxs-lookup"><span data-stu-id="cf0b9-207">Timestamp</span></span>](#timestamp) | <span data-ttu-id="cf0b9-208">Marca de tiempo de la excepción.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-208">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="cf0b9-209">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="cf0b9-209">exceptionDetails</span></span> | [<span data-ttu-id="cf0b9-210">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="cf0b9-210">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a><span data-ttu-id="cf0b9-211">Tipos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-211">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="cf0b9-212">Cadena ScriptId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-212">ScriptId string</span></span>  

<a name="scriptid"></a>  

<span data-ttu-id="cf0b9-213">Identificador de script único.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-213">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="cf0b9-214">Cadena RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-214">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>  

<span data-ttu-id="cf0b9-215">Identificador de objeto único.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-215">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="cf0b9-216">Cadena UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="cf0b9-216">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="cf0b9-217">Valor primitivo que no puede ser cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-217">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="cf0b9-218">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="cf0b9-218">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="cf0b9-219">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="cf0b9-219">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="cf0b9-220">Objeto RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-220">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="cf0b9-221">Objeto Mirror que hace referencia al objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-221">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="cf0b9-222">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0b9-222">Properties</span></span> | <span data-ttu-id="cf0b9-223">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-223">Type</span></span> | <span data-ttu-id="cf0b9-224">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-224">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-225">tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-225">type</span></span> | `string` | <span data-ttu-id="cf0b9-226">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-226">Object type.</span></span>  <span data-ttu-id="cf0b9-227">Valores permitidos:  `object` , , , , , `function` `undefined` `string` `number` `boolean` y</span><span class="sxs-lookup"><span data-stu-id="cf0b9-227">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="cf0b9-228">subtipo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-228">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="cf0b9-229">Sugerencia de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-229">Object subtype hint.</span></span>  <span data-ttu-id="cf0b9-230">Se especifica solo `object` para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-230">Specified for `object` type values only.</span></span>  <span data-ttu-id="cf0b9-231">Valores permitidos:  `null` `error` , y</span><span class="sxs-lookup"><span data-stu-id="cf0b9-231">Allowed values:  `null`, `error`, and</span></span> `promise` |  
| <span data-ttu-id="cf0b9-232">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-232">className \(optional\)</span></span> | `string` | <span data-ttu-id="cf0b9-233">Nombre de clase de objeto \(constructor\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-233">Object class \(constructor\) name.</span></span>  <span data-ttu-id="cf0b9-234">Se especifica solo `object` para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-234">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="cf0b9-235">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-235">value \(optional\)</span></span> | `any` | <span data-ttu-id="cf0b9-236">Valor de objeto remoto en caso de valores primitivos o valores JSON \(si se solicitó\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-236">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="cf0b9-237">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-237">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="cf0b9-238">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="cf0b9-238">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="cf0b9-239">El valor primitivo que no puede tener cadena JSON no tiene `value` , pero obtiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-239">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="cf0b9-240">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-240">description \(optional\)</span></span> | `string` | <span data-ttu-id="cf0b9-241">Representación de cadena del objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-241">String representation of the object.</span></span> |  
| <span data-ttu-id="cf0b9-242">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-242">objectId \(optional\)</span></span> | [<span data-ttu-id="cf0b9-243">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-243">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="cf0b9-244">Identificador de objeto único \(para valores no primitivos\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-244">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="cf0b9-245">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-245">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="cf0b9-246">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-246">**Experimental**.</span></span>  <span data-ttu-id="cf0b9-247">Microsoft: el identificador de propiedad del depurador asociado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-247">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="cf0b9-248">PropertyDescriptor (objeto)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-248">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="cf0b9-249">Descriptor de la propiedad Object.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-249">Object property descriptor.</span></span>  

| <span data-ttu-id="cf0b9-250">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0b9-250">Properties</span></span> | <span data-ttu-id="cf0b9-251">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-251">Type</span></span> | <span data-ttu-id="cf0b9-252">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-252">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-253">name</span><span class="sxs-lookup"><span data-stu-id="cf0b9-253">name</span></span> | `string` | <span data-ttu-id="cf0b9-254">Nombre de la propiedad o descripción del símbolo.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-254">Property name or symbol description.</span></span> |  
| <span data-ttu-id="cf0b9-255">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-255">value \(optional\)</span></span> | [<span data-ttu-id="cf0b9-256">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-256">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-257">Valor asociado a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-257">The value associated with the property.</span></span> |  
| <span data-ttu-id="cf0b9-258">writable \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-258">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="cf0b9-259">si se puede cambiar el valor asociado a la propiedad \(data descriptors only\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-259">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="cf0b9-260">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-260">get \(optional\)</span></span> | [<span data-ttu-id="cf0b9-261">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-261">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-262">Función que sirve como getter para la propiedad, o si no hay ningún descriptor de acceso `undefined` \(descriptores de acceso\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-262">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="cf0b9-263">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-263">set \(optional\)</span></span> | [<span data-ttu-id="cf0b9-264">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-264">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-265">Función que sirve como setter para la propiedad, o si no hay ningún `undefined` setter \(descriptores de descriptores de acceso solamente\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-265">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="cf0b9-266">configurable</span><span class="sxs-lookup"><span data-stu-id="cf0b9-266">configurable</span></span> | `boolean` | `True` <span data-ttu-id="cf0b9-267">si se puede cambiar el tipo de descriptor de esta propiedad y si la propiedad se puede eliminar del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-267">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="cf0b9-268">enumerable</span><span class="sxs-lookup"><span data-stu-id="cf0b9-268">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="cf0b9-269">si esta propiedad se muestra durante la enumeración de las propiedades del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-269">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="cf0b9-270">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-270">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="cf0b9-271">si el resultado se ha arrojado durante la evaluación.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-271">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="cf0b9-272">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-272">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="cf0b9-273">si la propiedad es propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-273">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="cf0b9-274">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-274">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="cf0b9-275">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-275">**Experimental**.</span></span>  <span data-ttu-id="cf0b9-276">Microsoft:  `True` si la propiedad es un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-276">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="cf0b9-277">símbolo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-277">symbol \(optional\)</span></span> | [<span data-ttu-id="cf0b9-278">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-278">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-279">Objeto de símbolo de propiedad, si la propiedad es del `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-279">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="cf0b9-280">CallArgument (objeto)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-280">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="cf0b9-281">Representa el argumento de llamada de función.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-281">Represents function call argument.</span></span>  <span data-ttu-id="cf0b9-282">Debe especificarse el identificador de objeto remoto, el valor primitivo no extraíble o ninguno de `value` \(para undefined\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-282">Either remote object ID `value`, unserializable primitive value or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="cf0b9-283">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0b9-283">Properties</span></span> | <span data-ttu-id="cf0b9-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-284">Type</span></span> | <span data-ttu-id="cf0b9-285">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-285">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-286">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-286">value \(optional\)</span></span> | `any` | <span data-ttu-id="cf0b9-287">Valor primitivo o objeto javascript serializable.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-287">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="cf0b9-288">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-288">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="cf0b9-289">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="cf0b9-289">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="cf0b9-290">Valor primitivo que no puede estar en cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-290">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="cf0b9-291">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-291">objectId \(optional\)</span></span> | [<span data-ttu-id="cf0b9-292">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-292">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="cf0b9-293">Controlador de objetos remoto.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-293">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="cf0b9-294">Número entero ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-294">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="cf0b9-295">Id. de un contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-295">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="cf0b9-296">ExceptionDetails (objeto)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-296">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="cf0b9-297">Información detallada sobre la excepción \(o error\) que se produjo durante la compilación o ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-297">Detailed information about exception \(or error\) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="cf0b9-298">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0b9-298">Properties</span></span> | <span data-ttu-id="cf0b9-299">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-299">Type</span></span> | <span data-ttu-id="cf0b9-300">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-300">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-301">exceptionId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-301">exceptionId</span></span> | `integer` | <span data-ttu-id="cf0b9-302">Identificador de excepción.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-302">Exception ID.</span></span> |  
| <span data-ttu-id="cf0b9-303">texto</span><span class="sxs-lookup"><span data-stu-id="cf0b9-303">text</span></span> | `string` | <span data-ttu-id="cf0b9-304">Texto de excepción, que debe usarse junto con el objeto de excepción cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-304">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="cf0b9-305">lineNumber</span><span class="sxs-lookup"><span data-stu-id="cf0b9-305">lineNumber</span></span> | `integer` | <span data-ttu-id="cf0b9-306">Número de línea de la ubicación de excepción \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-306">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="cf0b9-307">columnNumber</span><span class="sxs-lookup"><span data-stu-id="cf0b9-307">columnNumber</span></span> | `integer` | <span data-ttu-id="cf0b9-308">Número de columna de la ubicación de excepción \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-308">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="cf0b9-309">scriptId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-309">scriptId \(optional\)</span></span> | [<span data-ttu-id="cf0b9-310">ScriptId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-310">ScriptId</span></span>](#scriptid) | <span data-ttu-id="cf0b9-311">Identificador de script de la ubicación de excepción.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-311">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="cf0b9-312">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-312">url \(optional\)</span></span> | `string` | <span data-ttu-id="cf0b9-313">Dirección URL de la ubicación de excepción, que se usará cuando no se haya notificado el script.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-313">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="cf0b9-314">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-314">stackTrace \(optional\)</span></span> | [<span data-ttu-id="cf0b9-315">StackTrace</span><span class="sxs-lookup"><span data-stu-id="cf0b9-315">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="cf0b9-316">Seguimiento de pila de JavaScript si está disponible.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-316">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="cf0b9-317">excepción \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-317">exception \(optional\)</span></span> | [<span data-ttu-id="cf0b9-318">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf0b9-318">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="cf0b9-319">Objeto Exception si está disponible.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-319">Exception object if available.</span></span> |  
| <span data-ttu-id="cf0b9-320">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-320">executionContextId \(optional\)</span></span> | [<span data-ttu-id="cf0b9-321">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-321">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="cf0b9-322">Identificador del contexto donde se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-322">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="cf0b9-323">Número entero de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-323">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="cf0b9-324">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-324">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="cf0b9-325">CallFrame (objeto)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-325">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="cf0b9-326">Entrada de pila para errores y aserciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-326">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="cf0b9-327">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0b9-327">Properties</span></span> | <span data-ttu-id="cf0b9-328">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-328">Type</span></span> | <span data-ttu-id="cf0b9-329">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-329">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-330">functionName</span><span class="sxs-lookup"><span data-stu-id="cf0b9-330">functionName</span></span> | `string` | <span data-ttu-id="cf0b9-331">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-331">JavaScript function name.</span></span> |  
| <span data-ttu-id="cf0b9-332">scriptId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-332">scriptId</span></span> | [<span data-ttu-id="cf0b9-333">ScriptId</span><span class="sxs-lookup"><span data-stu-id="cf0b9-333">ScriptId</span></span>](#scriptid) | <span data-ttu-id="cf0b9-334">Id. de script de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-334">JavaScript script ID.</span></span> |  
| <span data-ttu-id="cf0b9-335">url</span><span class="sxs-lookup"><span data-stu-id="cf0b9-335">url</span></span> | `string` | <span data-ttu-id="cf0b9-336">Dirección URL o nombre de script de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-336">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="cf0b9-337">lineNumber</span><span class="sxs-lookup"><span data-stu-id="cf0b9-337">lineNumber</span></span> | `integer` | <span data-ttu-id="cf0b9-338">Número de línea de script de JavaScript \(basado en 0\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-338">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="cf0b9-339">columnNumber</span><span class="sxs-lookup"><span data-stu-id="cf0b9-339">columnNumber</span></span> | `integer` | <span data-ttu-id="cf0b9-340">Número de columna de script de JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="cf0b9-340">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="cf0b9-341">StackTrace (objeto)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-341">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="cf0b9-342">Marcos de llamadas para aserciones o mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-342">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="cf0b9-343">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0b9-343">Properties</span></span> | <span data-ttu-id="cf0b9-344">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0b9-344">Type</span></span> | <span data-ttu-id="cf0b9-345">Detalles</span><span class="sxs-lookup"><span data-stu-id="cf0b9-345">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cf0b9-346">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-346">description \(optional\)</span></span> | `string` | <span data-ttu-id="cf0b9-347">Etiqueta de cadena de este seguimiento de pila.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-347">String label of this stack trace.</span></span>  <span data-ttu-id="cf0b9-348">Para los seguimientos asincrónicos, puede ser un nombre de la función que inició la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-348">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="cf0b9-349">callFrames</span><span class="sxs-lookup"><span data-stu-id="cf0b9-349">callFrames</span></span> | [<span data-ttu-id="cf0b9-350">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="cf0b9-350">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="cf0b9-351">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-351">JavaScript function name.</span></span> |  
| <span data-ttu-id="cf0b9-352">parent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="cf0b9-352">parent \(optional\)</span></span> | [<span data-ttu-id="cf0b9-353">StackTrace</span><span class="sxs-lookup"><span data-stu-id="cf0b9-353">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="cf0b9-354">Seguimiento de pila de JavaScript asincrónico que precedía a esta pila, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="cf0b9-354">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
