---
description: Referencia del dominio en tiempo de ejecución. El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.
title: Dominio de tiempo de ejecución-protocolo de DevTools versión 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 710b3b3e0383f1f6feb7947e0468730d2e0b0e66
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882866"
---
# <span data-ttu-id="d9e32-106">Dominio de tiempo de ejecución-protocolo de DevTools versión 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="d9e32-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="d9e32-107">El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos.</span><span class="sxs-lookup"><span data-stu-id="d9e32-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="d9e32-108">Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="d9e32-109">Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d9e32-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="d9e32-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9e32-110">Methods</span></span>**](#methods) | <span data-ttu-id="d9e32-111">[enable](#enable), [Disable](#disable), [Evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="d9e32-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="d9e32-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="d9e32-112">Events</span></span>**](#events) | <span data-ttu-id="d9e32-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="d9e32-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="d9e32-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="d9e32-114">Types</span></span>**](#types) | <span data-ttu-id="d9e32-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="d9e32-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="d9e32-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9e32-116">Methods</span></span>

### <span data-ttu-id="d9e32-117">habilitar</span><span class="sxs-lookup"><span data-stu-id="d9e32-117">enable</span></span>
<span data-ttu-id="d9e32-118">Permite generar informes de <code>executionContextCreated</code> los <code>executionContextDestroyed</code> eventos y y <code>executionContextsCleared</code> .</span><span class="sxs-lookup"><span data-stu-id="d9e32-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="d9e32-119">Cuando los informes estén habilitados <code>executionContextCreated</code> , el evento se enviará inmediatamente por cada contexto de ejecución existente.</span><span class="sxs-lookup"><span data-stu-id="d9e32-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="d9e32-120">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="d9e32-120">disable</span></span>
<span data-ttu-id="d9e32-121">Deshabilita el informe de <code>executionContextCreated</code> los <code>executionContextDestroyed</code> <code>executionContextsCleared</code> eventos y.</span><span class="sxs-lookup"><span data-stu-id="d9e32-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="d9e32-122">considerar</span><span class="sxs-lookup"><span data-stu-id="d9e32-122">evaluate</span></span>
<span data-ttu-id="d9e32-123">Evalúa Expression en el objeto global.</span><span class="sxs-lookup"><span data-stu-id="d9e32-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-125">Expression</span><span class="sxs-lookup"><span data-stu-id="d9e32-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-126">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="d9e32-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="d9e32-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="d9e32-128">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-129">Determina si la API de la línea de comandos debe estar disponible durante la evaluación.</span><span class="sxs-lookup"><span data-stu-id="d9e32-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="d9e32-130">objectGroup</span></span> <br/> <i><span data-ttu-id="d9e32-131">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-132">Nombre de grupo simbólico que se puede usar para liberar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="d9e32-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-133">silent</span><span class="sxs-lookup"><span data-stu-id="d9e32-133">silent</span></span> <br/> <i><span data-ttu-id="d9e32-134">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-135">En modo silencioso, no se notifican las excepciones producidas durante la evaluación y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="d9e32-136">Estado de invalidaciones <code>setPauseOnException</code> .</span><span class="sxs-lookup"><span data-stu-id="d9e32-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-137">contextId</span><span class="sxs-lookup"><span data-stu-id="d9e32-137">contextId</span></span> <br/> <i><span data-ttu-id="d9e32-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="d9e32-139">Especifica el contexto de ejecución para realizar la evaluación.</span><span class="sxs-lookup"><span data-stu-id="d9e32-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="d9e32-140">Si se omite el parámetro, la evaluación se realizará en el contexto de la página inspeccionada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-141">returnByValue</span></span> <br/> <i><span data-ttu-id="d9e32-142">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-143">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="d9e32-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="d9e32-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="d9e32-145">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-146">Si la ejecución debe tener el <code>await</code> valor resultante y la devolución una vez que se resuelve la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-147">Devuelve</span><span class="sxs-lookup"><span data-stu-id="d9e32-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-148">resultado</span><span class="sxs-lookup"><span data-stu-id="d9e32-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-149">Resultado de evaluación.</span><span class="sxs-lookup"><span data-stu-id="d9e32-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="d9e32-150">callFunctionOn</span></span>
<span data-ttu-id="d9e32-151">Función calls con declaración dada en el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="d9e32-152">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="d9e32-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-153">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="d9e32-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-155">Declaración de la función que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="d9e32-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-156">ID</span><span class="sxs-lookup"><span data-stu-id="d9e32-156">objectId</span></span> <br/> <i><span data-ttu-id="d9e32-157">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="d9e32-158">Identificador del objeto en el que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="d9e32-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="d9e32-159">Debe especificar objectId o executionContextId.</span><span class="sxs-lookup"><span data-stu-id="d9e32-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="d9e32-160">objectId debe ser de la función Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="d9e32-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-161">arguments</span><span class="sxs-lookup"><span data-stu-id="d9e32-161">arguments</span></span> <br/> <i><span data-ttu-id="d9e32-162">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="d9e32-163">Argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-163">Call arguments.</span></span> <span data-ttu-id="d9e32-164">Todos los argumentos de la llamada deben pertenecer al mismo mundo de JavaScript que el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="d9e32-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-165">silent</span><span class="sxs-lookup"><span data-stu-id="d9e32-165">silent</span></span> <br/> <i><span data-ttu-id="d9e32-166">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-167">En modo silencioso, no se notifican las excepciones producidas durante la evaluación y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="d9e32-168">Estado de invalidaciones <code>setPauseOnException</code> .</span><span class="sxs-lookup"><span data-stu-id="d9e32-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-169">returnByValue</span></span> <br/> <i><span data-ttu-id="d9e32-170">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-171">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="d9e32-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="d9e32-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="d9e32-173">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-174">Si la ejecución debe tener el <code>await</code> valor resultante y la devolución una vez que se resuelve la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="d9e32-175">executionContextId</span></span> <br/> <i><span data-ttu-id="d9e32-176">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="d9e32-177">Especifica el contexto de ejecución en el que se usará el objeto global para llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="d9e32-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="d9e32-178">Debe especificarse executionContextId o objectId.</span><span class="sxs-lookup"><span data-stu-id="d9e32-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="d9e32-179">objectGroup</span></span> <br/> <i><span data-ttu-id="d9e32-180">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-181">Nombre de grupo simbólico que se puede usar para liberar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="d9e32-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="d9e32-182">Si no se especifica objectGroup y objectId es, objectGroup se heredará de Object.</span><span class="sxs-lookup"><span data-stu-id="d9e32-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-183">Devuelve</span><span class="sxs-lookup"><span data-stu-id="d9e32-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-184">resultado</span><span class="sxs-lookup"><span data-stu-id="d9e32-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-185">Resultado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="d9e32-186">awaitPromise</span></span>
<span data-ttu-id="d9e32-187">Agregar el controlador que se va a comprometer con el identificador de objeto Promise dado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-188">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="d9e32-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="d9e32-190">Identificador de la promesa.</span><span class="sxs-lookup"><span data-stu-id="d9e32-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-191">returnByValue</span></span> <br/> <i><span data-ttu-id="d9e32-192">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-193">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="d9e32-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-194">Devuelve</span><span class="sxs-lookup"><span data-stu-id="d9e32-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-195">resultado</span><span class="sxs-lookup"><span data-stu-id="d9e32-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-196">Resultado de la promesa.</span><span class="sxs-lookup"><span data-stu-id="d9e32-196">Promise result.</span></span>  <span data-ttu-id="d9e32-197">Contendrá un valor rechazado si la promesa ha sido rechazada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-198">getProperties</span><span class="sxs-lookup"><span data-stu-id="d9e32-198">getProperties</span></span>
<span data-ttu-id="d9e32-199">Devuelve las propiedades de un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-199">Returns properties of a given object.</span></span> <span data-ttu-id="d9e32-200">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="d9e32-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-202">ID</span><span class="sxs-lookup"><span data-stu-id="d9e32-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="d9e32-203">Identificador del objeto para el que se van a devolver las propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9e32-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="d9e32-204">objectId debe ser de la función Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="d9e32-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="d9e32-205">ownProperties</span></span> <br/> <i><span data-ttu-id="d9e32-206">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-207">Si es true, devuelve propiedades pertenecientes al propio elemento, no a su cadena de prototipo.</span><span class="sxs-lookup"><span data-stu-id="d9e32-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="d9e32-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="d9e32-209">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="d9e32-210">Montaje.</span><span class="sxs-lookup"><span data-stu-id="d9e32-210">Experimental.</span></span> </b></span><span data-ttu-id="d9e32-211">Si es verdadero, devuelve propiedades del descriptor de acceso (solo con el captador/establecedor); las propiedades internas no se devuelven.</span><span class="sxs-lookup"><span data-stu-id="d9e32-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-212">Devuelve</span><span class="sxs-lookup"><span data-stu-id="d9e32-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-213">resultado</span><span class="sxs-lookup"><span data-stu-id="d9e32-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="d9e32-214">Propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="d9e32-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="d9e32-216">Devuelve todas las variables Let, const y Class del ámbito global de la consola.</span><span class="sxs-lookup"><span data-stu-id="d9e32-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-217">Devuelve</span><span class="sxs-lookup"><span data-stu-id="d9e32-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-218">asigna</span><span class="sxs-lookup"><span data-stu-id="d9e32-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-219">releaseObject</span><span class="sxs-lookup"><span data-stu-id="d9e32-219">releaseObject</span></span>
<span data-ttu-id="d9e32-220">Libera el objeto remoto con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-221">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-222">ID</span><span class="sxs-lookup"><span data-stu-id="d9e32-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="d9e32-223">Identificador del objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="d9e32-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="d9e32-224">releaseObjectGroup</span></span>
<span data-ttu-id="d9e32-225">Libera todos los objetos remotos que pertenecen a un grupo determinado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-226">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="d9e32-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-228">Nombre del grupo de objetos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="d9e32-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="d9e32-229">discardConsoleEntries</span></span>
<span data-ttu-id="d9e32-230">Descarta las excepciones recopiladas y las llamadas API de consola.</span><span class="sxs-lookup"><span data-stu-id="d9e32-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="d9e32-231">Eventos</span><span class="sxs-lookup"><span data-stu-id="d9e32-231">Events</span></span>

### <span data-ttu-id="d9e32-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="d9e32-232">executionContextCreated</span></span>
<span data-ttu-id="d9e32-233">Se emite cuando se crea un nuevo contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-234">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-235">marco</span><span class="sxs-lookup"><span data-stu-id="d9e32-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="d9e32-236">Contexto de ejecución recién creado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="d9e32-237">executionContextDestroyed</span></span>
<span data-ttu-id="d9e32-238">Se emite cuando se destruye el contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="d9e32-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="d9e32-241">Identificador del contexto destruido</span><span class="sxs-lookup"><span data-stu-id="d9e32-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="d9e32-242">executionContextsCleared</span></span>
<span data-ttu-id="d9e32-243">Se emite cuando se han borrado todas las executionContexts en el explorador</span><span class="sxs-lookup"><span data-stu-id="d9e32-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="d9e32-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="d9e32-244">exceptionThrown</span></span>
<span data-ttu-id="d9e32-245">Se emite cuando se ha iniciado una excepción y no se ha controlado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-246">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-247">marca</span><span class="sxs-lookup"><span data-stu-id="d9e32-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="d9e32-248">Marca de fecha y hora de la excepción.</span><span class="sxs-lookup"><span data-stu-id="d9e32-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="d9e32-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9e32-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="d9e32-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-251">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9e32-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-252">tipo</span><span class="sxs-lookup"><span data-stu-id="d9e32-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="d9e32-253">Valores permitidos: log, info, warning, error, Debug, Assert, Table, trace, dir, dirxml, Clear, Select, Count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="d9e32-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="d9e32-254">Tipo de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-254">Type of the call.</span></span> <span data-ttu-id="d9e32-255">Esto incluye log, info, WARN, error, Debug, Assert, Table, trace, dir, dirxml, Clear, Select, Count, countReset, timeEnd, Exception, timeStamp, Group, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="d9e32-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-256">EventArgs</span><span class="sxs-lookup"><span data-stu-id="d9e32-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="d9e32-257">Argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="d9e32-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="d9e32-259">Identificador del contexto en el que se realizó la llamada de consola</span><span class="sxs-lookup"><span data-stu-id="d9e32-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-260">marca</span><span class="sxs-lookup"><span data-stu-id="d9e32-260">timestamp</span></span> <br/> <i><span data-ttu-id="d9e32-261">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="d9e32-262">Marca de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d9e32-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-263">stackTrace</span><span class="sxs-lookup"><span data-stu-id="d9e32-263">stackTrace</span></span> <br/> <i><span data-ttu-id="d9e32-264">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="d9e32-265">El seguimiento de la pila se capturó si está disponible</span><span class="sxs-lookup"><span data-stu-id="d9e32-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="d9e32-266">Tipos</span><span class="sxs-lookup"><span data-stu-id="d9e32-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="d9e32-267">ScriptId</span><span class="sxs-lookup"><span data-stu-id="d9e32-267">ScriptId</span></span> `string`

<span data-ttu-id="d9e32-268">Identificador de script único.</span><span class="sxs-lookup"><span data-stu-id="d9e32-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="d9e32-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="d9e32-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="d9e32-270">Identificador de objeto único.</span><span class="sxs-lookup"><span data-stu-id="d9e32-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="d9e32-271">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-271">UnserializableValue</span></span> `string`

<span data-ttu-id="d9e32-272">Valor primitivo que no puede ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="d9e32-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="d9e32-273">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="d9e32-273">Allowed Values</span></span>
<span data-ttu-id="d9e32-274">Infinity, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="d9e32-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="d9e32-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="d9e32-275">RemoteObject</span></span> `object`

<span data-ttu-id="d9e32-276">Objeto Mirror que hace referencia al objeto de JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="d9e32-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-277">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-278">tipo</span><span class="sxs-lookup"><span data-stu-id="d9e32-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="d9e32-279">Valores permitidos: objeto, función, sin definir, cadena, número, booleano, símbolo</span><span class="sxs-lookup"><span data-stu-id="d9e32-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="d9e32-280">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-281">subtipo</span><span class="sxs-lookup"><span data-stu-id="d9e32-281">subtype</span></span> <br/> <i><span data-ttu-id="d9e32-282">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="d9e32-283">Valores permitidos: null, error, Promise, nodo</span><span class="sxs-lookup"><span data-stu-id="d9e32-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="d9e32-284">Sugerencia de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-284">Object subtype hint.</span></span> <span data-ttu-id="d9e32-285">Especificado <code>object</code> solo para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="d9e32-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-286">className</span><span class="sxs-lookup"><span data-stu-id="d9e32-286">className</span></span> <br/> <i><span data-ttu-id="d9e32-287">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-288">Nombre de la clase de objeto (constructor).</span><span class="sxs-lookup"><span data-stu-id="d9e32-288">Object class (constructor) name.</span></span> <span data-ttu-id="d9e32-289">Especificado <code>object</code> solo para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="d9e32-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-290">value</span><span class="sxs-lookup"><span data-stu-id="d9e32-290">value</span></span> <br/> <i><span data-ttu-id="d9e32-291">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="d9e32-292">Valor del objeto remoto en caso de valores primitivos o valores de JSON (si se solicitó).</span><span class="sxs-lookup"><span data-stu-id="d9e32-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-293">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="d9e32-294">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="d9e32-295">El valor primitivo que no puede ser JSON-stringified no tiene</span><span class="sxs-lookup"><span data-stu-id="d9e32-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="d9e32-296">, pero obtiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d9e32-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-297">description</span><span class="sxs-lookup"><span data-stu-id="d9e32-297">description</span></span> <br/> <i><span data-ttu-id="d9e32-298">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-299">Representación de cadena del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-300">ID</span><span class="sxs-lookup"><span data-stu-id="d9e32-300">objectId</span></span> <br/> <i><span data-ttu-id="d9e32-301">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="d9e32-302">Identificador de objeto único (para valores no primitivos).</span><span class="sxs-lookup"><span data-stu-id="d9e32-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="d9e32-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="d9e32-304">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="d9e32-305">Montaje.</span><span class="sxs-lookup"><span data-stu-id="d9e32-305">Experimental.</span></span> </b></span><span data-ttu-id="d9e32-306">Microsoft: el identificador de propiedad de depurador asociado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="d9e32-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="d9e32-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="d9e32-308">Descriptor de propiedad de objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-309">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-310">name</span><span class="sxs-lookup"><span data-stu-id="d9e32-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-311">Nombre de propiedad o descripción de símbolo.</span><span class="sxs-lookup"><span data-stu-id="d9e32-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-312">value</span><span class="sxs-lookup"><span data-stu-id="d9e32-312">value</span></span> <br/> <i><span data-ttu-id="d9e32-313">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-314">El valor asociado a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d9e32-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-315">pueda</span><span class="sxs-lookup"><span data-stu-id="d9e32-315">writable</span></span> <br/> <i><span data-ttu-id="d9e32-316">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-317">True si el valor asociado a la propiedad puede cambiarse (solo para descriptores de datos).</span><span class="sxs-lookup"><span data-stu-id="d9e32-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-318">obtener</span><span class="sxs-lookup"><span data-stu-id="d9e32-318">get</span></span> <br/> <i><span data-ttu-id="d9e32-319">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-320">Una función que sirve como captador para la propiedad o si no hay <code>undefined</code> ningún captador (solo descriptores de acceso).</span><span class="sxs-lookup"><span data-stu-id="d9e32-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-321">set</span><span class="sxs-lookup"><span data-stu-id="d9e32-321">set</span></span> <br/> <i><span data-ttu-id="d9e32-322">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-323">Una función que sirve como un establecedor para la propiedad o <code>undefined</code> si no hay ningún establecedor (solo descriptores de acceso).</span><span class="sxs-lookup"><span data-stu-id="d9e32-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-324">puedan</span><span class="sxs-lookup"><span data-stu-id="d9e32-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-325">True si el tipo de este descriptor de propiedades se puede cambiar y si la propiedad se puede eliminar del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d9e32-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-326">enumera</span><span class="sxs-lookup"><span data-stu-id="d9e32-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-327">True si esta propiedad se muestra durante la enumeración de las propiedades del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d9e32-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="d9e32-328">wasThrown</span></span> <br/> <i><span data-ttu-id="d9e32-329">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-330">True si el resultado se produjo durante la evaluación.</span><span class="sxs-lookup"><span data-stu-id="d9e32-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="d9e32-331">isOwn</span></span> <br/> <i><span data-ttu-id="d9e32-332">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d9e32-333">True si la propiedad es propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="d9e32-335">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="d9e32-336">Montaje.</span><span class="sxs-lookup"><span data-stu-id="d9e32-336">Experimental.</span></span> </b></span><span data-ttu-id="d9e32-337">Microsoft: true si la propiedad es un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-338">símbolo</span><span class="sxs-lookup"><span data-stu-id="d9e32-338">symbol</span></span> <br/> <i><span data-ttu-id="d9e32-339">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-340">Objeto de símbolo de propiedad, si la propiedad es del `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="d9e32-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="d9e32-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="d9e32-341">CallArgument</span></span> `object`

<span data-ttu-id="d9e32-342">Representa el argumento de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="d9e32-342">Represents function call argument.</span></span> <span data-ttu-id="d9e32-343"><code>objectId</code>Se debe especificar el identificador de objeto remoto, el primitivo <code>value</code> , el valor primitivo inserializable o ninguno de los dos (no definidos).</span><span class="sxs-lookup"><span data-stu-id="d9e32-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-344">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-345">value</span><span class="sxs-lookup"><span data-stu-id="d9e32-345">value</span></span> <br/> <i><span data-ttu-id="d9e32-346">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="d9e32-347">Valor primitivo o objeto serializable de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9e32-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-348">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="d9e32-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="d9e32-349">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="d9e32-350">Valor primitivo que no puede ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="d9e32-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-351">ID</span><span class="sxs-lookup"><span data-stu-id="d9e32-351">objectId</span></span> <br/> <i><span data-ttu-id="d9e32-352">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="d9e32-353">Controlador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="d9e32-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="d9e32-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="d9e32-355">Identificador de un contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="d9e32-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="d9e32-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="d9e32-357">Descripción de un mundo aislado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-358">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-359">id</span><span class="sxs-lookup"><span data-stu-id="d9e32-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="d9e32-360">Identificador único del contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-360">Unique id of the execution context.</span></span> <span data-ttu-id="d9e32-361">Puede usarse para especificar qué evaluación de script de contexto de ejecución se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="d9e32-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-362">origen</span><span class="sxs-lookup"><span data-stu-id="d9e32-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-363">Origen de contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-364">name</span><span class="sxs-lookup"><span data-stu-id="d9e32-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-365">Nombre legible para la persona que describe el contexto determinado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="d9e32-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="d9e32-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="d9e32-367">Información detallada sobre la excepción (o error) que se produjo durante la compilación o ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="d9e32-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-368">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-369">exceptionId</span><span class="sxs-lookup"><span data-stu-id="d9e32-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d9e32-370">Identificador de excepción.</span><span class="sxs-lookup"><span data-stu-id="d9e32-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-371">texto</span><span class="sxs-lookup"><span data-stu-id="d9e32-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-372">Texto de excepción, que debe usarse junto con el objeto de excepción cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="d9e32-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="d9e32-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d9e32-374">Número de línea de la ubicación de excepción (basada en 0).</span><span class="sxs-lookup"><span data-stu-id="d9e32-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="d9e32-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d9e32-376">Número de columna de la ubicación de excepción (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="d9e32-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-377">scriptId</span><span class="sxs-lookup"><span data-stu-id="d9e32-377">scriptId</span></span> <br/> <i><span data-ttu-id="d9e32-378">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="d9e32-379">IDENTIFICADOR de script de la ubicación de excepción.</span><span class="sxs-lookup"><span data-stu-id="d9e32-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-380">url</span><span class="sxs-lookup"><span data-stu-id="d9e32-380">url</span></span> <br/> <i><span data-ttu-id="d9e32-381">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-382">Dirección URL de la ubicación de excepción que se usará cuando no se notificó el script.</span><span class="sxs-lookup"><span data-stu-id="d9e32-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-383">stackTrace</span><span class="sxs-lookup"><span data-stu-id="d9e32-383">stackTrace</span></span> <br/> <i><span data-ttu-id="d9e32-384">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="d9e32-385">Seguimiento de la pila de JavaScript si está disponible.</span><span class="sxs-lookup"><span data-stu-id="d9e32-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-386">excepción</span><span class="sxs-lookup"><span data-stu-id="d9e32-386">exception</span></span> <br/> <i><span data-ttu-id="d9e32-387">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="d9e32-388">Objeto de excepción si está disponible.</span><span class="sxs-lookup"><span data-stu-id="d9e32-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="d9e32-389">executionContextId</span></span> <br/> <i><span data-ttu-id="d9e32-390">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="d9e32-391">Identificador del contexto en el que se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="d9e32-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="d9e32-392">Timestamp</span><span class="sxs-lookup"><span data-stu-id="d9e32-392">Timestamp</span></span> `integer`

<span data-ttu-id="d9e32-393">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="d9e32-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="d9e32-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="d9e32-394">CallFrame</span></span> `object`

<span data-ttu-id="d9e32-395">Entrada de pila para errores y aserciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9e32-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-396">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-397">functionName</span><span class="sxs-lookup"><span data-stu-id="d9e32-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-398">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9e32-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-399">scriptId</span><span class="sxs-lookup"><span data-stu-id="d9e32-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="d9e32-400">ID. de script de JavaScript. ScriptId estará vacío si Debugger no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d9e32-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-401">url</span><span class="sxs-lookup"><span data-stu-id="d9e32-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-402">Nombre de script o URL de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9e32-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="d9e32-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d9e32-404">Número de línea de script de JavaScript (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="d9e32-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="d9e32-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d9e32-406">Número de columna de script de JavaScript (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="d9e32-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="d9e32-407">StackTrace</span><span class="sxs-lookup"><span data-stu-id="d9e32-407">StackTrace</span></span> `object`

<span data-ttu-id="d9e32-408">Llamar a marcos para las aserciones o los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="d9e32-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9e32-409">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9e32-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9e32-410">description</span><span class="sxs-lookup"><span data-stu-id="d9e32-410">description</span></span> <br/> <i><span data-ttu-id="d9e32-411">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9e32-412">Etiqueta de cadena de este seguimiento de pila.</span><span class="sxs-lookup"><span data-stu-id="d9e32-412">String label of this stack trace.</span></span> <span data-ttu-id="d9e32-413">Para las trazas asíncronas puede ser un nombre de la función que inició la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d9e32-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="d9e32-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="d9e32-415">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9e32-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d9e32-416">matriz</span><span class="sxs-lookup"><span data-stu-id="d9e32-416">parent</span></span> <br/> <i><span data-ttu-id="d9e32-417">opcional</span><span class="sxs-lookup"><span data-stu-id="d9e32-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="d9e32-418">Seguimiento asincrónico de la pila de JavaScript que precedía a esta pila, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="d9e32-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
