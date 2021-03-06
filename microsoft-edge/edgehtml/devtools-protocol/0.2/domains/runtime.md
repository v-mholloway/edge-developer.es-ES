---
description: Referencia del protocolo DevTools versión 0.2 (EdgeHTML) para el dominio en tiempo de ejecución. El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript mediante objetos reflejados y de evaluación remota. Los resultados de la evaluación se devuelven como objeto reflejado que exponen el tipo de objeto, la representación de cadenas y el identificador único que se puede usar para más referencia de objeto. Los objetos originales se mantienen en la memoria a menos que se liberan explícitamente.
title: 'Dominio en tiempo de ejecución: protocolo DevTools versión 0.2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: afc79a17c5002f60806872a9add57f518ff6cb45
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398143"
---
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="88bbd-106">Dominio en tiempo de ejecución: protocolo DevTools versión 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="88bbd-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="88bbd-107">El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript mediante objetos reflejados y de evaluación remota.</span><span class="sxs-lookup"><span data-stu-id="88bbd-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="88bbd-108">Los resultados de la evaluación se devuelven como objeto reflejado que exponen el tipo de objeto, la representación de cadenas y el identificador único que se puede usar para más referencia de objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="88bbd-109">Los objetos originales se mantienen en la memoria a menos que se liberan explícitamente.</span><span class="sxs-lookup"><span data-stu-id="88bbd-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="88bbd-110">Clasificación</span><span class="sxs-lookup"><span data-stu-id="88bbd-110">Classification</span></span> | <span data-ttu-id="88bbd-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="88bbd-111">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="88bbd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="88bbd-112">Methods</span></span>**](#methods) | <span data-ttu-id="88bbd-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="88bbd-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |  
| [**<span data-ttu-id="88bbd-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="88bbd-114">Events</span></span>**](#events) | <span data-ttu-id="88bbd-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="88bbd-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |  
| [**<span data-ttu-id="88bbd-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="88bbd-116">Types</span></span>**](#types) | <span data-ttu-id="88bbd-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="88bbd-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="88bbd-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="88bbd-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="88bbd-119">habilitar</span><span class="sxs-lookup"><span data-stu-id="88bbd-119">enable</span></span>  

<span data-ttu-id="88bbd-120">Habilita la presentación de informes `executionContextCreated` de los eventos , `executionContextDestroyed` `executionContextsCleared` y.</span><span class="sxs-lookup"><span data-stu-id="88bbd-120">Enables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  <span data-ttu-id="88bbd-121">Cuando se habilita el informe, `executionContextCreated` el evento se enviará inmediatamente para cada contexto de ejecución existente.</span><span class="sxs-lookup"><span data-stu-id="88bbd-121">When the reporting gets enabled the `executionContextCreated` event will be sent immediately for each existing execution context.</span></span>  

---  

### <a name="disable"></a><span data-ttu-id="88bbd-122">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="88bbd-122">disable</span></span>  

<span data-ttu-id="88bbd-123">Deshabilita los informes de `executionContextCreated` los `executionContextDestroyed` eventos , `executionContextsCleared` y.</span><span class="sxs-lookup"><span data-stu-id="88bbd-123">Disables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  

---  

### <a name="evaluate"></a><span data-ttu-id="88bbd-124">evaluar</span><span class="sxs-lookup"><span data-stu-id="88bbd-124">evaluate</span></span>  

<span data-ttu-id="88bbd-125">Evalúa la expresión en el objeto global.</span><span class="sxs-lookup"><span data-stu-id="88bbd-125">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="88bbd-126">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-126">Parameters</span></span> | <span data-ttu-id="88bbd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-127">Type</span></span> | <span data-ttu-id="88bbd-128">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-128">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-129">expresión</span><span class="sxs-lookup"><span data-stu-id="88bbd-129">expression</span></span> | `string` | <span data-ttu-id="88bbd-130">Expresión que se debe evaluar.</span><span class="sxs-lookup"><span data-stu-id="88bbd-130">Expression to evaluate.</span></span> |  
| <span data-ttu-id="88bbd-131">includeCommandLineAPI \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-131">includeCommandLineAPI \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-132">Determina si la API de línea de comandos debe estar disponible durante la evaluación.</span><span class="sxs-lookup"><span data-stu-id="88bbd-132">Determines whether Command Line API should be available during the evaluation.</span></span> |  
| <span data-ttu-id="88bbd-133">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-133">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-134">Nombre de grupo simbólico que se puede usar para liberar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="88bbd-134">Symbolic group name that can be used to release multiple objects.</span></span> |  
| <span data-ttu-id="88bbd-135">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-135">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-136">En modo silencioso, las excepciones que se inician durante la evaluación no se notifican y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-136">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="88bbd-137">Invalida el `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-137">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="88bbd-138">contextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-138">contextId \(optional\)</span></span> | [<span data-ttu-id="88bbd-139">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-139">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="88bbd-140">Especifica en qué contexto de ejecución se debe realizar la evaluación.</span><span class="sxs-lookup"><span data-stu-id="88bbd-140">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="88bbd-141">Si se omite el parámetro, la evaluación se realizará en el contexto de la página inspeccionada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-141">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="88bbd-142">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-142">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-143">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="88bbd-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="88bbd-144">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-144">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-145">Si la ejecución debe `await` ser para el valor resultante y devolver una vez que se resuelva la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-145">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="88bbd-146">Devuelve</span><span class="sxs-lookup"><span data-stu-id="88bbd-146">Returns</span></span> | <span data-ttu-id="88bbd-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-147">Type</span></span> | <span data-ttu-id="88bbd-148">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-148">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-149">resultado</span><span class="sxs-lookup"><span data-stu-id="88bbd-149">result</span></span> | [<span data-ttu-id="88bbd-150">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-150">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-151">Resultado de la evaluación.</span><span class="sxs-lookup"><span data-stu-id="88bbd-151">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="88bbd-152">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="88bbd-152">callFunctionOn</span></span>  

<span data-ttu-id="88bbd-153">Las llamadas funcionan con una declaración determinada en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-153">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="88bbd-154">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="88bbd-154">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="88bbd-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-155">Parameters</span></span> | <span data-ttu-id="88bbd-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-156">Type</span></span> | <span data-ttu-id="88bbd-157">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-158">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="88bbd-158">functionDeclaration</span></span> | `string` | <span data-ttu-id="88bbd-159">Declaración de la función a la que se llamará.</span><span class="sxs-lookup"><span data-stu-id="88bbd-159">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="88bbd-160">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-160">objectId \(optional\)</span></span> | [<span data-ttu-id="88bbd-161">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-161">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="88bbd-162">Identificador del objeto en el que se debe llamar.</span><span class="sxs-lookup"><span data-stu-id="88bbd-162">Identifier of the object to call function on.</span></span>  <span data-ttu-id="88bbd-163">Se `objectId` debe especificar o `executionContextId` no.</span><span class="sxs-lookup"><span data-stu-id="88bbd-163">Either `objectId` or `executionContextId` should be specified.</span></span>  `objectId` <span data-ttu-id="88bbd-164">debe ser de la `Runtime.evaluate()` función.</span><span class="sxs-lookup"><span data-stu-id="88bbd-164">must be from the `Runtime.evaluate()` function.</span></span> |  
| <span data-ttu-id="88bbd-165">argumentos \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-165">arguments \(optional\)</span></span> | [<span data-ttu-id="88bbd-166">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="88bbd-166">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="88bbd-167">Argumentos de llamada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-167">Call arguments.</span></span>  <span data-ttu-id="88bbd-168">Todos los argumentos de llamada deben pertenecer al mismo mundo de JavaScript que el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="88bbd-168">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="88bbd-169">boolean \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-169">boolean \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-170">En modo silencioso, las excepciones que se inician durante la evaluación no se notifican y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-170">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="88bbd-171">Invalida el `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-171">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="88bbd-172">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-172">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-173">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="88bbd-173">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="88bbd-174">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-174">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-175">Si la ejecución debe `await` ser para el valor resultante y devolver una vez que se resuelva la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-175">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  
| <span data-ttu-id="88bbd-176">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-176">executionContextId \(optional\)</span></span> | [<span data-ttu-id="88bbd-177">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-177">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="88bbd-178">Especifica el contexto de ejecución en el que se usará el objeto global para llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="88bbd-178">Specifies execution context which global object will be used to call function on.</span></span>  <span data-ttu-id="88bbd-179">Cualquiera de los dos</span><span class="sxs-lookup"><span data-stu-id="88bbd-179">Either</span></span>
`executionContextId` <span data-ttu-id="88bbd-180">o `objectId` debe especificarse</span><span class="sxs-lookup"><span data-stu-id="88bbd-180">or `objectId` should be specified</span></span> |  
| <span data-ttu-id="88bbd-181">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-181">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-182">Nombre de grupo simbólico que se puede usar para liberar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="88bbd-182">Symbolic group name that can be used to release multiple objects.</span></span>  <span data-ttu-id="88bbd-183">Si `objectGroup` no se especifica y `objectId` es, se `objectGroup` heredará del objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-183">If `objectGroup` is not specified and `objectId` is, `objectGroup` will be inherited from object.</span></span> |  

| <span data-ttu-id="88bbd-184">Devuelve</span><span class="sxs-lookup"><span data-stu-id="88bbd-184">Returns</span></span> | <span data-ttu-id="88bbd-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-185">Type</span></span> | <span data-ttu-id="88bbd-186">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-187">resultado</span><span class="sxs-lookup"><span data-stu-id="88bbd-187">result</span></span> | [<span data-ttu-id="88bbd-188">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-188">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-189">Resultado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-189">Call result.</span></span> |  

---  

### <a name="awaitpromise"></a><span data-ttu-id="88bbd-190">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="88bbd-190">awaitPromise</span></span>  

<span data-ttu-id="88bbd-191">Agregar controlador para prometer con un identificador de objeto de promesa determinado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-191">Add handler to promise with given promise object id.</span></span>  

| <span data-ttu-id="88bbd-192">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-192">Parameters</span></span> | <span data-ttu-id="88bbd-193">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-193">Type</span></span> | <span data-ttu-id="88bbd-194">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-195">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-195">promiseObjectId</span></span> | [<span data-ttu-id="88bbd-196">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-196">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="88bbd-197">Identificador de la promesa.</span><span class="sxs-lookup"><span data-stu-id="88bbd-197">Identifier of the promise.</span></span> |  
| <span data-ttu-id="88bbd-198">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-198">returnByValue \(optional\)</span></span> | <span data-ttu-id="88bbd-199">booleano</span><span class="sxs-lookup"><span data-stu-id="88bbd-199">boolean</span></span> | <span data-ttu-id="88bbd-200">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="88bbd-200">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  

| <span data-ttu-id="88bbd-201">Devuelve</span><span class="sxs-lookup"><span data-stu-id="88bbd-201">Returns</span></span> | <span data-ttu-id="88bbd-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-202">Type</span></span> | <span data-ttu-id="88bbd-203">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-204">resultado</span><span class="sxs-lookup"><span data-stu-id="88bbd-204">result</span></span> | [<span data-ttu-id="88bbd-205">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-205">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-206">Resultado de la promesa.</span><span class="sxs-lookup"><span data-stu-id="88bbd-206">Promise result.</span></span>  <span data-ttu-id="88bbd-207">Contendrá el valor rechazado si se rechazó la promesa.</span><span class="sxs-lookup"><span data-stu-id="88bbd-207">Will contain rejected value if promise was rejected.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="88bbd-208">getProperties</span><span class="sxs-lookup"><span data-stu-id="88bbd-208">getProperties</span></span>  

<span data-ttu-id="88bbd-209">Devuelve las propiedades de un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-209">Returns properties of a given object.</span></span> <span data-ttu-id="88bbd-210">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="88bbd-210">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="88bbd-211">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-211">Parameters</span></span> | <span data-ttu-id="88bbd-212">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-212">Type</span></span> | <span data-ttu-id="88bbd-213">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-213">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-214">objectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-214">objectId</span></span> | [<span data-ttu-id="88bbd-215">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-215">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="88bbd-216">Identificador del objeto para el que se devolverán las propiedades.</span><span class="sxs-lookup"><span data-stu-id="88bbd-216">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="88bbd-217">debe ser de la `Debugger.evaluateOnCallFrame()` función.</span><span class="sxs-lookup"><span data-stu-id="88bbd-217">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="88bbd-218">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-218">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-219">Si `true` , devuelve propiedades que pertenecen solo al elemento en sí, no a su cadena prototipo.</span><span class="sxs-lookup"><span data-stu-id="88bbd-219">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="88bbd-220">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-220">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-221">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="88bbd-221">**Experimental**.</span></span>  <span data-ttu-id="88bbd-222">Si `true` , devuelve las propiedades del accessor \(with getter/setter\) solo; tampoco se devuelven las propiedades internas.</span><span class="sxs-lookup"><span data-stu-id="88bbd-222">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="88bbd-223">Devuelve</span><span class="sxs-lookup"><span data-stu-id="88bbd-223">Returns</span></span> | <span data-ttu-id="88bbd-224">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-224">Type</span></span> | <span data-ttu-id="88bbd-225">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-225">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-226">resultado</span><span class="sxs-lookup"><span data-stu-id="88bbd-226">result</span></span> | [<span data-ttu-id="88bbd-227">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="88bbd-227">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="88bbd-228">Propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-228">Object properties.</span></span> |  

---  

### <a name="globallexicalscopenames"></a><span data-ttu-id="88bbd-229">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="88bbd-229">globalLexicalScopeNames</span></span>  

<span data-ttu-id="88bbd-230">Devuelve todas las variables let, const y class del ámbito global de la consola.</span><span class="sxs-lookup"><span data-stu-id="88bbd-230">Returns all let, const, and class variables from the console global scope.</span></span>  

| <span data-ttu-id="88bbd-231">Devuelve</span><span class="sxs-lookup"><span data-stu-id="88bbd-231">Returns</span></span> | <span data-ttu-id="88bbd-232">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-232">Type</span></span> | <span data-ttu-id="88bbd-233">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-233">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-234">nombres</span><span class="sxs-lookup"><span data-stu-id="88bbd-234">names</span></span> | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a><span data-ttu-id="88bbd-235">releaseObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-235">releaseObject</span></span>  

<span data-ttu-id="88bbd-236">Libera el objeto remoto con un identificador determinado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-236">Releases remote object with given ID.</span></span>  

| <span data-ttu-id="88bbd-237">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-237">Parameters</span></span> | <span data-ttu-id="88bbd-238">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-238">Type</span></span> | <span data-ttu-id="88bbd-239">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-239">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-240">objectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-240">objectId</span></span> | [<span data-ttu-id="88bbd-241">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-241">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="88bbd-242">Identificador del objeto que se liberará.</span><span class="sxs-lookup"><span data-stu-id="88bbd-242">Identifier of the object to release.</span></span> |  

---  

### <a name="releaseobjectgroup"></a><span data-ttu-id="88bbd-243">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="88bbd-243">releaseObjectGroup</span></span>  

<span data-ttu-id="88bbd-244">Libera todos los objetos remotos que pertenecen a un grupo determinado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-244">Releases all remote objects that belong to a given group.</span></span>  

| <span data-ttu-id="88bbd-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-245">Parameters</span></span> | <span data-ttu-id="88bbd-246">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-246">Type</span></span> | <span data-ttu-id="88bbd-247">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-247">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-248">objectGroup</span><span class="sxs-lookup"><span data-stu-id="88bbd-248">objectGroup</span></span> | `string` | <span data-ttu-id="88bbd-249">Nombre del grupo de objetos simbólico.</span><span class="sxs-lookup"><span data-stu-id="88bbd-249">Symbolic object group name.</span></span> |  

---  

### <a name="discardconsoleentries"></a><span data-ttu-id="88bbd-250">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="88bbd-250">discardConsoleEntries</span></span>  

<span data-ttu-id="88bbd-251">Descarta las excepciones recopiladas y las llamadas a la API de consola.</span><span class="sxs-lookup"><span data-stu-id="88bbd-251">Discards collected exceptions and console API calls.</span></span>  

---  

## <a name="events"></a><span data-ttu-id="88bbd-252">Eventos</span><span class="sxs-lookup"><span data-stu-id="88bbd-252">Events</span></span>  

### <a name="executioncontextcreated"></a><span data-ttu-id="88bbd-253">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="88bbd-253">executionContextCreated</span></span>  

<span data-ttu-id="88bbd-254">Se emite cuando se crea un nuevo contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-254">Issued when new execution context is created.</span></span>  

| <span data-ttu-id="88bbd-255">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-255">Parameters</span></span> | <span data-ttu-id="88bbd-256">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-256">Type</span></span> | <span data-ttu-id="88bbd-257">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-257">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-258">contexto</span><span class="sxs-lookup"><span data-stu-id="88bbd-258">context</span></span> | [<span data-ttu-id="88bbd-259">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="88bbd-259">ExecutionContextDescription</span></span>](#executioncontextdescription) | <span data-ttu-id="88bbd-260">Contexto de ejecución recién creado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-260">A newly created execution context.</span></span> |  

---  

### <a name="executioncontextdestroyed"></a><span data-ttu-id="88bbd-261">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="88bbd-261">executionContextDestroyed</span></span>  

<span data-ttu-id="88bbd-262">Se emite cuando se destruye el contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-262">Issued when execution context is destroyed.</span></span>  

| <span data-ttu-id="88bbd-263">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-263">Parameters</span></span> | <span data-ttu-id="88bbd-264">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-264">Type</span></span> | <span data-ttu-id="88bbd-265">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-265">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-266">executionContextId</span></span> | [<span data-ttu-id="88bbd-267">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-267">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="88bbd-268">Id. del contexto destruido.</span><span class="sxs-lookup"><span data-stu-id="88bbd-268">ID of the destroyed context.</span></span> |  

---  

### <a name="executioncontextscleared"></a><span data-ttu-id="88bbd-269">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="88bbd-269">executionContextsCleared</span></span>  

<span data-ttu-id="88bbd-270">Se emite cuando se borraron todos los executionContexts en el explorador.</span><span class="sxs-lookup"><span data-stu-id="88bbd-270">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="88bbd-271">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="88bbd-271">exceptionThrown</span></span>  

<span data-ttu-id="88bbd-272">Se emitió cuando se produjo la excepción y no se controló.</span><span class="sxs-lookup"><span data-stu-id="88bbd-272">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="88bbd-273">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-273">Parameters</span></span> | <span data-ttu-id="88bbd-274">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-274">Type</span></span> | <span data-ttu-id="88bbd-275">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-275">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-276">marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="88bbd-276">timestamp</span></span> | [<span data-ttu-id="88bbd-277">Timestamp</span><span class="sxs-lookup"><span data-stu-id="88bbd-277">Timestamp</span></span>](#timestamp) | <span data-ttu-id="88bbd-278">Marca de tiempo de la excepción.</span><span class="sxs-lookup"><span data-stu-id="88bbd-278">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="88bbd-279">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="88bbd-279">exceptionDetails</span></span> | [<span data-ttu-id="88bbd-280">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="88bbd-280">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

### <a name="consoleapicalled"></a><span data-ttu-id="88bbd-281">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="88bbd-281">consoleAPICalled</span></span>  

| <span data-ttu-id="88bbd-282">Parameters</span><span class="sxs-lookup"><span data-stu-id="88bbd-282">Parameters</span></span> | <span data-ttu-id="88bbd-283">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-283">Type</span></span> | <span data-ttu-id="88bbd-284">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-284">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-285">tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-285">type</span></span> | `string` | <span data-ttu-id="88bbd-286">Tipo de llamada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-286">Type of the call.</span></span>  <span data-ttu-id="88bbd-287">Valores permitidos:  `log` , , , , , , , , `info` , , `warning` , , , `error` , , `debug` `assert` `table` `trace` `dir` , `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` `startGroupCollapsed` y</span><span class="sxs-lookup"><span data-stu-id="88bbd-287">Allowed values:  `log`, `info`, `warning`, `error`, `debug`, `assert`, `table`, `trace`, `dir`, `dirxml`, `clear`, `select`, `count`, `countReset`, `timeEnd`, `timeStamp`, `startGroup`, `startGroupCollapsed`, and</span></span> `endGroup` |  
| <span data-ttu-id="88bbd-288">args</span><span class="sxs-lookup"><span data-stu-id="88bbd-288">args</span></span> | <span data-ttu-id="88bbd-289">[RemoteObject[]] (#remoteobject</span><span class="sxs-lookup"><span data-stu-id="88bbd-289">[RemoteObject[]](#remoteobject</span></span> | <span data-ttu-id="88bbd-290">Argumentos de llamada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-290">Call arguments.</span></span> |  
| <span data-ttu-id="88bbd-291">executionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-291">executionContextId</span></span> | [<span data-ttu-id="88bbd-292">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-292">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="88bbd-293">Identificador del contexto donde se realizó la llamada de consola.</span><span class="sxs-lookup"><span data-stu-id="88bbd-293">Identifier of the context where console call was made.</span></span> |  
| <span data-ttu-id="88bbd-294">timestamp \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-294">timestamp \(optional\)</span></span> | [<span data-ttu-id="88bbd-295">Timestamp</span><span class="sxs-lookup"><span data-stu-id="88bbd-295">Timestamp</span></span>](#timestamp) | <span data-ttu-id="88bbd-296">Marca de tiempo de llamada.</span><span class="sxs-lookup"><span data-stu-id="88bbd-296">Call timestamp.</span></span> |  
| <span data-ttu-id="88bbd-297">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-297">stackTrace \(optional\)</span></span> | [<span data-ttu-id="88bbd-298">StackTrace</span><span class="sxs-lookup"><span data-stu-id="88bbd-298">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="88bbd-299">Seguimiento de pila capturado si está disponible.</span><span class="sxs-lookup"><span data-stu-id="88bbd-299">Stack trace captured if available.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="88bbd-300">Tipos</span><span class="sxs-lookup"><span data-stu-id="88bbd-300">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="88bbd-301">Cadena ScriptId</span><span class="sxs-lookup"><span data-stu-id="88bbd-301">ScriptId string</span></span>  

<a name="scriptid"></a>

<span data-ttu-id="88bbd-302">Identificador de script único.</span><span class="sxs-lookup"><span data-stu-id="88bbd-302">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="88bbd-303">Cadena RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-303">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>

<span data-ttu-id="88bbd-304">Identificador de objeto único.</span><span class="sxs-lookup"><span data-stu-id="88bbd-304">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="88bbd-305">Cadena UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="88bbd-305">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="88bbd-306">Valor primitivo que no puede ser cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="88bbd-306">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="88bbd-307">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="88bbd-307">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="88bbd-308">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="88bbd-308">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="88bbd-309">Objeto RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-309">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="88bbd-310">Objeto Mirror que hace referencia al objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="88bbd-310">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="88bbd-311">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-311">Properties</span></span> | <span data-ttu-id="88bbd-312">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-312">Type</span></span> | <span data-ttu-id="88bbd-313">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-313">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-314">tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-314">type</span></span> | `string` | <span data-ttu-id="88bbd-315">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-315">Object type.</span></span>  <span data-ttu-id="88bbd-316">Valores permitidos:  `object` , , , , , `function` `undefined` `string` `number` `boolean` y</span><span class="sxs-lookup"><span data-stu-id="88bbd-316">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="88bbd-317">subtipo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-317">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-318">Sugerencia de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-318">Object subtype hint.</span></span>  <span data-ttu-id="88bbd-319">Se especifica solo `object` para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="88bbd-319">Specified for `object` type values only.</span></span>  <span data-ttu-id="88bbd-320">Valores permitidos:  `null` `error` , , `promise` y</span><span class="sxs-lookup"><span data-stu-id="88bbd-320">Allowed values:  `null`, `error`, `promise`, and</span></span> `node` |  
| <span data-ttu-id="88bbd-321">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-321">className \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-322">Nombre de clase de objeto \(constructor\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-322">Object class \(constructor\) name.</span></span>  <span data-ttu-id="88bbd-323">Se especifica solo `object` para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="88bbd-323">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="88bbd-324">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-324">value \(optional\)</span></span> | `any` | <span data-ttu-id="88bbd-325">Valor de objeto remoto en caso de valores primitivos o valores JSON \(si se solicitó\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-325">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="88bbd-326">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-326">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="88bbd-327">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="88bbd-327">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="88bbd-328">El valor primitivo que no puede tener cadena JSON no tiene `value` , pero obtiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="88bbd-328">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="88bbd-329">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-329">description \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-330">Representación de cadena del objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-330">String representation of the object.</span></span> |  
| <span data-ttu-id="88bbd-331">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-331">objectId \(optional\)</span></span> | [<span data-ttu-id="88bbd-332">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="88bbd-332">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="88bbd-333">Identificador de objeto único \(para valores no primitivos\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-333">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="88bbd-334">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-334">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-335">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="88bbd-335">**Experimental**.</span></span>  <span data-ttu-id="88bbd-336">Microsoft: el identificador de propiedad del depurador asociado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-336">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="88bbd-337">PropertyDescriptor (objeto)</span><span class="sxs-lookup"><span data-stu-id="88bbd-337">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="88bbd-338">Descriptor de la propiedad Object.</span><span class="sxs-lookup"><span data-stu-id="88bbd-338">Object property descriptor.</span></span>  

| <span data-ttu-id="88bbd-339">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-339">Properties</span></span> | <span data-ttu-id="88bbd-340">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-340">Type</span></span> | <span data-ttu-id="88bbd-341">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-341">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-342">name</span><span class="sxs-lookup"><span data-stu-id="88bbd-342">name</span></span> | `string` | <span data-ttu-id="88bbd-343">Nombre de la propiedad o descripción del símbolo.</span><span class="sxs-lookup"><span data-stu-id="88bbd-343">Property name or symbol description.</span></span> |  
| <span data-ttu-id="88bbd-344">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-344">value \(optional\)</span></span> | [<span data-ttu-id="88bbd-345">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-345">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-346">Valor asociado a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="88bbd-346">The value associated with the property.</span></span> |  
| <span data-ttu-id="88bbd-347">writable \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-347">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="88bbd-348">si se puede cambiar el valor asociado a la propiedad \(data descriptors only\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-348">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="88bbd-349">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-349">get \(optional\)</span></span> | [<span data-ttu-id="88bbd-350">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-350">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-351">Función que sirve como getter para la propiedad, o si no hay ningún descriptor de acceso `undefined` \(descriptores de acceso\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-351">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="88bbd-352">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-352">set \(optional\)</span></span> | [<span data-ttu-id="88bbd-353">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-353">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-354">Función que sirve como setter para la propiedad, o si no hay ningún `undefined` setter \(descriptores de descriptores de acceso solamente\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-354">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="88bbd-355">configurable</span><span class="sxs-lookup"><span data-stu-id="88bbd-355">configurable</span></span> | `boolean` | `True` <span data-ttu-id="88bbd-356">si se puede cambiar el tipo de descriptor de esta propiedad y si la propiedad se puede eliminar del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="88bbd-356">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="88bbd-357">enumerable</span><span class="sxs-lookup"><span data-stu-id="88bbd-357">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="88bbd-358">si esta propiedad se muestra durante la enumeración de las propiedades del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="88bbd-358">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="88bbd-359">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-359">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="88bbd-360">si el resultado se ha arrojado durante la evaluación.</span><span class="sxs-lookup"><span data-stu-id="88bbd-360">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="88bbd-361">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-361">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="88bbd-362">si la propiedad es propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-362">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="88bbd-363">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-363">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="88bbd-364">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="88bbd-364">**Experimental**.</span></span>  <span data-ttu-id="88bbd-365">Microsoft:  `True` si la propiedad es un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-365">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="88bbd-366">símbolo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-366">symbol \(optional\)</span></span> | [<span data-ttu-id="88bbd-367">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-367">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-368">Objeto de símbolo de propiedad, si la propiedad es del `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="88bbd-368">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="88bbd-369">CallArgument (objeto)</span><span class="sxs-lookup"><span data-stu-id="88bbd-369">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="88bbd-370">Representa el argumento de llamada de función.</span><span class="sxs-lookup"><span data-stu-id="88bbd-370">Represents function call argument.</span></span>  <span data-ttu-id="88bbd-371">Debe especificarse el identificador de objeto remoto , el valor primitivo primitivo , el valor primitivo `objectId` `value` inserializable o ninguno de \(para undefined\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-371">Either remote object ID `objectId`, primitive `value`, unserializable primitive value, or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="88bbd-372">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-372">Properties</span></span> | <span data-ttu-id="88bbd-373">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-373">Type</span></span> | <span data-ttu-id="88bbd-374">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-374">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-375">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-375">value \(optional\)</span></span> | `any` | <span data-ttu-id="88bbd-376">Valor primitivo o objeto javascript serializable.</span><span class="sxs-lookup"><span data-stu-id="88bbd-376">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="88bbd-377">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-377">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="88bbd-378">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="88bbd-378">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="88bbd-379">Valor primitivo que no puede estar en cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="88bbd-379">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="88bbd-380">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-380">objectId \(optional\)</span></span> | <span data-ttu-id="88bbd-381">[RemoteObjectId](#remoteobjectid)]</span><span class="sxs-lookup"><span data-stu-id="88bbd-381">[RemoteObjectId](#remoteobjectid)]</span></span> | <span data-ttu-id="88bbd-382">Controlador de objetos remoto.</span><span class="sxs-lookup"><span data-stu-id="88bbd-382">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="88bbd-383">Número entero ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-383">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="88bbd-384">Id. de un contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-384">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a><span data-ttu-id="88bbd-385">ExecutionContextDescription (objeto)</span><span class="sxs-lookup"><span data-stu-id="88bbd-385">ExecutionContextDescription object</span></span>  

<a name="executioncontextdescription"></a>  

<span data-ttu-id="88bbd-386">Descripción de un mundo aislado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-386">Description of an isolated world.</span></span>  

| <span data-ttu-id="88bbd-387">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-387">Properties</span></span> | <span data-ttu-id="88bbd-388">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-388">Type</span></span> | <span data-ttu-id="88bbd-389">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-390">id</span><span class="sxs-lookup"><span data-stu-id="88bbd-390">id</span></span> | [<span data-ttu-id="88bbd-391">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-391">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="88bbd-392">Identificador único del contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-392">Unique ID of the execution context.</span></span>  <span data-ttu-id="88bbd-393">Se puede usar para especificar en qué contexto de ejecución</span><span class="sxs-lookup"><span data-stu-id="88bbd-393">It can be used to specify in which execution context</span></span>
<span data-ttu-id="88bbd-394">debe realizarse la evaluación de scripts.</span><span class="sxs-lookup"><span data-stu-id="88bbd-394">script evaluation should be performed.</span></span> |  
| <span data-ttu-id="88bbd-395">origin</span><span class="sxs-lookup"><span data-stu-id="88bbd-395">origin</span></span> | `string` | <span data-ttu-id="88bbd-396">Origen del contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-396">Execution context origin.</span></span> |  
| <span data-ttu-id="88bbd-397">name</span><span class="sxs-lookup"><span data-stu-id="88bbd-397">name</span></span> | `string` | <span data-ttu-id="88bbd-398">Nombre legible que describe un contexto determinado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-398">Human readable name describing given context.</span></span> |  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="88bbd-399">ExceptionDetails (objeto)</span><span class="sxs-lookup"><span data-stu-id="88bbd-399">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="88bbd-400">Información detallada sobre la excepción (o error) que se produjo durante la compilación o ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="88bbd-400">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="88bbd-401">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-401">Properties</span></span> | <span data-ttu-id="88bbd-402">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-402">Type</span></span> | <span data-ttu-id="88bbd-403">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-403">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-404">exceptionId</span><span class="sxs-lookup"><span data-stu-id="88bbd-404">exceptionId</span></span> | `integer` | <span data-ttu-id="88bbd-405">Identificador de excepción.</span><span class="sxs-lookup"><span data-stu-id="88bbd-405">Exception ID.</span></span> |  
| <span data-ttu-id="88bbd-406">texto</span><span class="sxs-lookup"><span data-stu-id="88bbd-406">text</span></span> | `string` | <span data-ttu-id="88bbd-407">Texto de excepción, que debe usarse junto con el objeto de excepción cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="88bbd-407">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="88bbd-408">lineNumber</span><span class="sxs-lookup"><span data-stu-id="88bbd-408">lineNumber</span></span> | `integer` | <span data-ttu-id="88bbd-409">Número de línea de la ubicación de excepción \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-409">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="88bbd-410">columnNumber</span><span class="sxs-lookup"><span data-stu-id="88bbd-410">columnNumber</span></span> | `integer` | <span data-ttu-id="88bbd-411">Número de columna de la ubicación de excepción \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-411">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="88bbd-412">scriptId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-412">scriptId \(optional\)</span></span> | [<span data-ttu-id="88bbd-413">ScriptId</span><span class="sxs-lookup"><span data-stu-id="88bbd-413">ScriptId</span></span>](#scriptid) | <span data-ttu-id="88bbd-414">Identificador de script de la ubicación de excepción.</span><span class="sxs-lookup"><span data-stu-id="88bbd-414">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="88bbd-415">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-415">url \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-416">Dirección URL de la ubicación de excepción, que se usará cuando no se haya notificado el script.</span><span class="sxs-lookup"><span data-stu-id="88bbd-416">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="88bbd-417">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-417">stackTrace \(optional\)</span></span> | [<span data-ttu-id="88bbd-418">StackTrace</span><span class="sxs-lookup"><span data-stu-id="88bbd-418">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="88bbd-419">Seguimiento de pila de JavaScript si está disponible.</span><span class="sxs-lookup"><span data-stu-id="88bbd-419">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="88bbd-420">excepción \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-420">exception \(optional\)</span></span> | [<span data-ttu-id="88bbd-421">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="88bbd-421">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="88bbd-422">Objeto Exception si está disponible.</span><span class="sxs-lookup"><span data-stu-id="88bbd-422">Exception object if available.</span></span> |  
| <span data-ttu-id="88bbd-423">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-423">executionContextId \(optional\)</span></span> | [<span data-ttu-id="88bbd-424">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="88bbd-424">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="88bbd-425">Identificador del contexto donde se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="88bbd-425">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="88bbd-426">Número entero de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="88bbd-426">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="88bbd-427">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="88bbd-427">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="88bbd-428">CallFrame (objeto)</span><span class="sxs-lookup"><span data-stu-id="88bbd-428">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="88bbd-429">Entrada de pila para errores y aserciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="88bbd-429">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="88bbd-430">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-430">Properties</span></span> | <span data-ttu-id="88bbd-431">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-431">Type</span></span> | <span data-ttu-id="88bbd-432">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-432">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-433">functionName</span><span class="sxs-lookup"><span data-stu-id="88bbd-433">functionName</span></span> | `string` | <span data-ttu-id="88bbd-434">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="88bbd-434">JavaScript function name.</span></span> |  
| <span data-ttu-id="88bbd-435">scriptId</span><span class="sxs-lookup"><span data-stu-id="88bbd-435">scriptId</span></span> | [<span data-ttu-id="88bbd-436">ScriptId</span><span class="sxs-lookup"><span data-stu-id="88bbd-436">ScriptId</span></span>](#scriptid) | <span data-ttu-id="88bbd-437">Identificador de script de JavaScript. ScriptId estará vacío si el depurador no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="88bbd-437">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span> |  
| <span data-ttu-id="88bbd-438">url</span><span class="sxs-lookup"><span data-stu-id="88bbd-438">url</span></span> | `string` | <span data-ttu-id="88bbd-439">Dirección URL o nombre de script de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="88bbd-439">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="88bbd-440">lineNumber</span><span class="sxs-lookup"><span data-stu-id="88bbd-440">lineNumber</span></span> | `integer` | <span data-ttu-id="88bbd-441">Número de línea de script de JavaScript \(basado en 0\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-441">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="88bbd-442">columnNumber</span><span class="sxs-lookup"><span data-stu-id="88bbd-442">columnNumber</span></span> | <span data-ttu-id="88bbd-443">entero</span><span class="sxs-lookup"><span data-stu-id="88bbd-443">integer</span></span> | <span data-ttu-id="88bbd-444">Número de columna de script de JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="88bbd-444">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="88bbd-445">StackTrace (objeto)</span><span class="sxs-lookup"><span data-stu-id="88bbd-445">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="88bbd-446">Marcos de llamadas para aserciones o mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="88bbd-446">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="88bbd-447">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88bbd-447">Properties</span></span> | <span data-ttu-id="88bbd-448">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bbd-448">Type</span></span> | <span data-ttu-id="88bbd-449">Detalles</span><span class="sxs-lookup"><span data-stu-id="88bbd-449">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="88bbd-450">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-450">description \(optional\)</span></span> | `string` | <span data-ttu-id="88bbd-451">Etiqueta de cadena de este seguimiento de pila.</span><span class="sxs-lookup"><span data-stu-id="88bbd-451">String label of this stack trace.</span></span>  <span data-ttu-id="88bbd-452">Para los seguimientos asincrónicos, puede ser un nombre de la función que inició la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="88bbd-452">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="88bbd-453">callFrames</span><span class="sxs-lookup"><span data-stu-id="88bbd-453">callFrames</span></span> | [<span data-ttu-id="88bbd-454">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="88bbd-454">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="88bbd-455">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="88bbd-455">JavaScript function name.</span></span> |  
| <span data-ttu-id="88bbd-456">parent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="88bbd-456">parent \(optional\)</span></span> | [<span data-ttu-id="88bbd-457">StackTrace</span><span class="sxs-lookup"><span data-stu-id="88bbd-457">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="88bbd-458">Seguimiento de pila de JavaScript asincrónico que precedía a esta pila, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="88bbd-458">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
