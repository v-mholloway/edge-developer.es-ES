---
description: Referencia del dominio en tiempo de ejecución. El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.
title: Dominio de tiempo de ejecución-protocolo de DevTools versión 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 33bc98b272aaa8831e908207b97ea7d3d0842976
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573756"
---
# <span data-ttu-id="e978d-106">Motores</span><span class="sxs-lookup"><span data-stu-id="e978d-106">Runtime</span></span>
<span data-ttu-id="e978d-107">El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos.</span><span class="sxs-lookup"><span data-stu-id="e978d-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="e978d-108">Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="e978d-109">Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e978d-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e978d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e978d-110">Methods</span></span>**](#methods) | <span data-ttu-id="e978d-111">[enable](#enable), [Disable](#disable), [Evaluate](#evaluate), [callFunctionOn](#callfunctionon), [GetProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="e978d-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="e978d-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="e978d-112">Events</span></span>**](#events) | <span data-ttu-id="e978d-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="e978d-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="e978d-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="e978d-114">Types</span></span>**](#types) | <span data-ttu-id="e978d-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="e978d-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="e978d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="e978d-116">Methods</span></span>

### <span data-ttu-id="e978d-117">habilitar</span><span class="sxs-lookup"><span data-stu-id="e978d-117">enable</span></span>
<span data-ttu-id="e978d-118">Permite informar del <code>executionContextsCleared</code> evento.</span><span class="sxs-lookup"><span data-stu-id="e978d-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="e978d-119">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="e978d-119">disable</span></span>
<span data-ttu-id="e978d-120">Deshabilita los informes del <code>executionContextsCleared</code> evento.</span><span class="sxs-lookup"><span data-stu-id="e978d-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="e978d-121">considerar</span><span class="sxs-lookup"><span data-stu-id="e978d-121">evaluate</span></span>
<span data-ttu-id="e978d-122">Evalúa Expression en el objeto global.</span><span class="sxs-lookup"><span data-stu-id="e978d-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-123">Parameters</span><span class="sxs-lookup"><span data-stu-id="e978d-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-124">Expression</span><span class="sxs-lookup"><span data-stu-id="e978d-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-125">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="e978d-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-126">silent</span><span class="sxs-lookup"><span data-stu-id="e978d-126">silent</span></span> <br/> <i><span data-ttu-id="e978d-127">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-128">En modo silencioso, no se notifican las excepciones producidas durante la evaluación y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="e978d-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="e978d-129">Estado de invalidaciones <code>setPauseOnException</code> .</span><span class="sxs-lookup"><span data-stu-id="e978d-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-130">contextId</span><span class="sxs-lookup"><span data-stu-id="e978d-130">contextId</span></span> <br/> <i><span data-ttu-id="e978d-131">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e978d-132">Especifica el contexto de ejecución para realizar la evaluación.</span><span class="sxs-lookup"><span data-stu-id="e978d-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="e978d-133">Si se omite el parámetro, la evaluación se realizará en el contexto de la página inspeccionada.</span><span class="sxs-lookup"><span data-stu-id="e978d-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e978d-134">returnByValue</span></span> <br/> <i><span data-ttu-id="e978d-135">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-136">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="e978d-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e978d-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="e978d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-139">Si la ejecución debe tener el <code>await</code> valor resultante y la devolución una vez que se resuelve la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="e978d-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-140">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e978d-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-141">resultado</span><span class="sxs-lookup"><span data-stu-id="e978d-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-142">Resultado de evaluación.</span><span class="sxs-lookup"><span data-stu-id="e978d-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="e978d-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="e978d-143">callFunctionOn</span></span>
<span data-ttu-id="e978d-144">Función calls con declaración dada en el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="e978d-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="e978d-145">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="e978d-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-146">Parameters</span><span class="sxs-lookup"><span data-stu-id="e978d-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="e978d-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-148">Declaración de la función que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="e978d-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-149">ID</span><span class="sxs-lookup"><span data-stu-id="e978d-149">objectId</span></span> <br/> <i><span data-ttu-id="e978d-150">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e978d-151">Identificador del objeto en el que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="e978d-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="e978d-152">Debe especificar objectId o executionContextId.</span><span class="sxs-lookup"><span data-stu-id="e978d-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="e978d-153">objectId debe ser de la función Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="e978d-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-154">arguments</span><span class="sxs-lookup"><span data-stu-id="e978d-154">arguments</span></span> <br/> <i><span data-ttu-id="e978d-155">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="e978d-156">Argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e978d-156">Call arguments.</span></span> <span data-ttu-id="e978d-157">Todos los argumentos de la llamada deben pertenecer al mismo mundo de JavaScript que el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="e978d-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-158">silent</span><span class="sxs-lookup"><span data-stu-id="e978d-158">silent</span></span> <br/> <i><span data-ttu-id="e978d-159">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-160">En modo silencioso, no se notifican las excepciones producidas durante la evaluación y no pausan la ejecución.</span><span class="sxs-lookup"><span data-stu-id="e978d-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="e978d-161">Estado de invalidaciones <code>setPauseOnException</code> .</span><span class="sxs-lookup"><span data-stu-id="e978d-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e978d-162">returnByValue</span></span> <br/> <i><span data-ttu-id="e978d-163">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-164">Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</span><span class="sxs-lookup"><span data-stu-id="e978d-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e978d-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="e978d-166">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-167">Si la ejecución debe tener el <code>await</code> valor resultante y la devolución una vez que se resuelve la promesa esperada.</span><span class="sxs-lookup"><span data-stu-id="e978d-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-168">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e978d-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-169">resultado</span><span class="sxs-lookup"><span data-stu-id="e978d-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-170">Resultado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e978d-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="e978d-171">getProperties</span><span class="sxs-lookup"><span data-stu-id="e978d-171">getProperties</span></span>
<span data-ttu-id="e978d-172">Devuelve las propiedades de un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="e978d-172">Returns properties of a given object.</span></span> <span data-ttu-id="e978d-173">El grupo de objetos del resultado se hereda del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="e978d-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-174">Parameters</span><span class="sxs-lookup"><span data-stu-id="e978d-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-175">ID</span><span class="sxs-lookup"><span data-stu-id="e978d-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e978d-176">Identificador del objeto para el que se van a devolver las propiedades.</span><span class="sxs-lookup"><span data-stu-id="e978d-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="e978d-177">objectId debe ser de la función Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="e978d-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="e978d-178">ownProperties</span></span> <br/> <i><span data-ttu-id="e978d-179">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-180">Si es true, devuelve propiedades pertenecientes al propio elemento, no a su cadena de prototipo.</span><span class="sxs-lookup"><span data-stu-id="e978d-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="e978d-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="e978d-182">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e978d-183">Montaje.</span><span class="sxs-lookup"><span data-stu-id="e978d-183">Experimental.</span></span> </b></span><span data-ttu-id="e978d-184">Si es verdadero, devuelve propiedades del descriptor de acceso (solo con el captador/establecedor); las propiedades internas no se devuelven.</span><span class="sxs-lookup"><span data-stu-id="e978d-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-185">Devuelve</span><span class="sxs-lookup"><span data-stu-id="e978d-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-186">resultado</span><span class="sxs-lookup"><span data-stu-id="e978d-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="e978d-187">Propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="e978d-188">Eventos</span><span class="sxs-lookup"><span data-stu-id="e978d-188">Events</span></span>

### <span data-ttu-id="e978d-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="e978d-189">executionContextsCleared</span></span>
<span data-ttu-id="e978d-190">Se emite cuando se han borrado todas las executionContexts en el explorador</span><span class="sxs-lookup"><span data-stu-id="e978d-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="e978d-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="e978d-191">exceptionThrown</span></span>
<span data-ttu-id="e978d-192">Se emite cuando se ha iniciado una excepción y no se ha controlado.</span><span class="sxs-lookup"><span data-stu-id="e978d-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-193">Parameters</span><span class="sxs-lookup"><span data-stu-id="e978d-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-194">marca</span><span class="sxs-lookup"><span data-stu-id="e978d-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="e978d-195">Marca de fecha y hora de la excepción.</span><span class="sxs-lookup"><span data-stu-id="e978d-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="e978d-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="e978d-197">Tipos</span><span class="sxs-lookup"><span data-stu-id="e978d-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="e978d-198">ScriptId</span><span class="sxs-lookup"><span data-stu-id="e978d-198">ScriptId</span></span> `string`

<span data-ttu-id="e978d-199">Identificador de script único.</span><span class="sxs-lookup"><span data-stu-id="e978d-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="e978d-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="e978d-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="e978d-201">Identificador de objeto único.</span><span class="sxs-lookup"><span data-stu-id="e978d-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="e978d-202">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="e978d-202">UnserializableValue</span></span> `string`

<span data-ttu-id="e978d-203">Valor primitivo que no puede ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="e978d-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="e978d-204">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="e978d-204">Allowed Values</span></span>
<span data-ttu-id="e978d-205">Infinity, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="e978d-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="e978d-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e978d-206">RemoteObject</span></span> `object`

<span data-ttu-id="e978d-207">Objeto Mirror que hace referencia al objeto de JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="e978d-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-208">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e978d-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-209">tipo</span><span class="sxs-lookup"><span data-stu-id="e978d-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e978d-210">Valores permitidos: objeto, función, sin definir, cadena, número, booleano, símbolo</span><span class="sxs-lookup"><span data-stu-id="e978d-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="e978d-211">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-212">subtipo</span><span class="sxs-lookup"><span data-stu-id="e978d-212">subtype</span></span> <br/> <i><span data-ttu-id="e978d-213">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e978d-214">Valores permitidos: null, error, Promise</span><span class="sxs-lookup"><span data-stu-id="e978d-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="e978d-215">Sugerencia de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-215">Object subtype hint.</span></span> <span data-ttu-id="e978d-216">Especificado <code>object</code> solo para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="e978d-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-217">className</span><span class="sxs-lookup"><span data-stu-id="e978d-217">className</span></span> <br/> <i><span data-ttu-id="e978d-218">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-219">Nombre de la clase de objeto (constructor).</span><span class="sxs-lookup"><span data-stu-id="e978d-219">Object class (constructor) name.</span></span> <span data-ttu-id="e978d-220">Especificado <code>object</code> solo para los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="e978d-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-221">value</span><span class="sxs-lookup"><span data-stu-id="e978d-221">value</span></span> <br/> <i><span data-ttu-id="e978d-222">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="e978d-223">Valor del objeto remoto en caso de valores primitivos o valores de JSON (si se solicitó).</span><span class="sxs-lookup"><span data-stu-id="e978d-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-224">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="e978d-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="e978d-225">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="e978d-226">El valor primitivo que no puede ser JSON-stringified no tiene</span><span class="sxs-lookup"><span data-stu-id="e978d-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="e978d-227">, pero obtiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e978d-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-228">description</span><span class="sxs-lookup"><span data-stu-id="e978d-228">description</span></span> <br/> <i><span data-ttu-id="e978d-229">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-230">Representación de cadena del objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-231">ID</span><span class="sxs-lookup"><span data-stu-id="e978d-231">objectId</span></span> <br/> <i><span data-ttu-id="e978d-232">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e978d-233">Identificador de objeto único (para valores no primitivos).</span><span class="sxs-lookup"><span data-stu-id="e978d-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="e978d-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="e978d-235">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="e978d-236">Montaje.</span><span class="sxs-lookup"><span data-stu-id="e978d-236">Experimental.</span></span> </b></span><span data-ttu-id="e978d-237">Microsoft: el identificador de propiedad de depurador asociado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="e978d-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="e978d-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="e978d-239">Descriptor de propiedad de objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-240">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e978d-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-241">name</span><span class="sxs-lookup"><span data-stu-id="e978d-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-242">Nombre de propiedad o descripción de símbolo.</span><span class="sxs-lookup"><span data-stu-id="e978d-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-243">value</span><span class="sxs-lookup"><span data-stu-id="e978d-243">value</span></span> <br/> <i><span data-ttu-id="e978d-244">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-245">El valor asociado a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e978d-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-246">pueda</span><span class="sxs-lookup"><span data-stu-id="e978d-246">writable</span></span> <br/> <i><span data-ttu-id="e978d-247">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-248">True si el valor asociado a la propiedad puede cambiarse (solo para descriptores de datos).</span><span class="sxs-lookup"><span data-stu-id="e978d-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-249">obtener</span><span class="sxs-lookup"><span data-stu-id="e978d-249">get</span></span> <br/> <i><span data-ttu-id="e978d-250">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-251">Una función que sirve como captador para la propiedad o si no hay <code>undefined</code> ningún captador (solo descriptores de acceso).</span><span class="sxs-lookup"><span data-stu-id="e978d-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-252">set</span><span class="sxs-lookup"><span data-stu-id="e978d-252">set</span></span> <br/> <i><span data-ttu-id="e978d-253">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-254">Una función que sirve como un establecedor para la propiedad o <code>undefined</code> si no hay ningún establecedor (solo descriptores de acceso).</span><span class="sxs-lookup"><span data-stu-id="e978d-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-255">puedan</span><span class="sxs-lookup"><span data-stu-id="e978d-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-256">True si el tipo de este descriptor de propiedades se puede cambiar y si la propiedad se puede eliminar del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e978d-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-257">enumera</span><span class="sxs-lookup"><span data-stu-id="e978d-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-258">True si esta propiedad se muestra durante la enumeración de las propiedades del objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e978d-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="e978d-259">wasThrown</span></span> <br/> <i><span data-ttu-id="e978d-260">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-261">True si el resultado se produjo durante la evaluación.</span><span class="sxs-lookup"><span data-stu-id="e978d-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="e978d-262">isOwn</span></span> <br/> <i><span data-ttu-id="e978d-263">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e978d-264">True si la propiedad es propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="e978d-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="e978d-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="e978d-266">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e978d-267">Montaje.</span><span class="sxs-lookup"><span data-stu-id="e978d-267">Experimental.</span></span> </b></span><span data-ttu-id="e978d-268">Microsoft: true si la propiedad es un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e978d-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-269">símbolo</span><span class="sxs-lookup"><span data-stu-id="e978d-269">symbol</span></span> <br/> <i><span data-ttu-id="e978d-270">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-271">Objeto de símbolo de propiedad, si la propiedad es del `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="e978d-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="e978d-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="e978d-272">CallArgument</span></span> `object`

<span data-ttu-id="e978d-273">Representa el argumento de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="e978d-273">Represents function call argument.</span></span> <span data-ttu-id="e978d-274"><code>objectId</code>Se debe especificar el identificador de objeto remoto, el primitivo <code>value</code> , el valor primitivo inserializable o ninguno de los dos (no definidos).</span><span class="sxs-lookup"><span data-stu-id="e978d-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-275">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e978d-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-276">value</span><span class="sxs-lookup"><span data-stu-id="e978d-276">value</span></span> <br/> <i><span data-ttu-id="e978d-277">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="e978d-278">Valor primitivo o objeto serializable de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e978d-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-279">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="e978d-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="e978d-280">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="e978d-281">Valor primitivo que no puede ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="e978d-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-282">ID</span><span class="sxs-lookup"><span data-stu-id="e978d-282">objectId</span></span> <br/> <i><span data-ttu-id="e978d-283">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e978d-284">Controlador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="e978d-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="e978d-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="e978d-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="e978d-286">Identificador de un contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e978d-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="e978d-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="e978d-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="e978d-288">Información detallada sobre la excepción (o error) que se produjo durante la compilación o ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="e978d-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-289">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e978d-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-290">exceptionId</span><span class="sxs-lookup"><span data-stu-id="e978d-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e978d-291">Identificador de excepción.</span><span class="sxs-lookup"><span data-stu-id="e978d-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-292">texto</span><span class="sxs-lookup"><span data-stu-id="e978d-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-293">Texto de excepción, que debe usarse junto con el objeto de excepción cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="e978d-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e978d-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e978d-295">Número de línea de la ubicación de excepción (basada en 0).</span><span class="sxs-lookup"><span data-stu-id="e978d-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e978d-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e978d-297">Número de columna de la ubicación de excepción (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="e978d-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-298">scriptId</span><span class="sxs-lookup"><span data-stu-id="e978d-298">scriptId</span></span> <br/> <i><span data-ttu-id="e978d-299">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="e978d-300">IDENTIFICADOR de script de la ubicación de excepción.</span><span class="sxs-lookup"><span data-stu-id="e978d-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-301">url</span><span class="sxs-lookup"><span data-stu-id="e978d-301">url</span></span> <br/> <i><span data-ttu-id="e978d-302">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-303">Dirección URL de la ubicación de excepción que se usará cuando no se notificó el script.</span><span class="sxs-lookup"><span data-stu-id="e978d-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-304">stackTrace</span><span class="sxs-lookup"><span data-stu-id="e978d-304">stackTrace</span></span> <br/> <i><span data-ttu-id="e978d-305">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e978d-306">Seguimiento de la pila de JavaScript si está disponible.</span><span class="sxs-lookup"><span data-stu-id="e978d-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-307">excepción</span><span class="sxs-lookup"><span data-stu-id="e978d-307">exception</span></span> <br/> <i><span data-ttu-id="e978d-308">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e978d-309">Objeto de excepción si está disponible.</span><span class="sxs-lookup"><span data-stu-id="e978d-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e978d-310">executionContextId</span></span> <br/> <i><span data-ttu-id="e978d-311">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e978d-312">Identificador del contexto en el que se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="e978d-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="e978d-313">Timestamp</span><span class="sxs-lookup"><span data-stu-id="e978d-313">Timestamp</span></span> `integer`

<span data-ttu-id="e978d-314">Número de milisegundos desde la época.</span><span class="sxs-lookup"><span data-stu-id="e978d-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="e978d-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="e978d-315">CallFrame</span></span> `object`

<span data-ttu-id="e978d-316">Entrada de pila para errores y aserciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e978d-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-317">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e978d-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-318">functionName</span><span class="sxs-lookup"><span data-stu-id="e978d-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-319">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e978d-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-320">scriptId</span><span class="sxs-lookup"><span data-stu-id="e978d-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="e978d-321">ID. de script de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e978d-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-322">url</span><span class="sxs-lookup"><span data-stu-id="e978d-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-323">Nombre de script o URL de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e978d-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e978d-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e978d-325">Número de línea de script de JavaScript (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="e978d-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e978d-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e978d-327">Número de columna de script de JavaScript (basado en 0).</span><span class="sxs-lookup"><span data-stu-id="e978d-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="e978d-328">StackTrace</span><span class="sxs-lookup"><span data-stu-id="e978d-328">StackTrace</span></span> `object`

<span data-ttu-id="e978d-329">Llamar a marcos para las aserciones o los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="e978d-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e978d-330">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e978d-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e978d-331">description</span><span class="sxs-lookup"><span data-stu-id="e978d-331">description</span></span> <br/> <i><span data-ttu-id="e978d-332">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e978d-333">Etiqueta de cadena de este seguimiento de pila.</span><span class="sxs-lookup"><span data-stu-id="e978d-333">String label of this stack trace.</span></span> <span data-ttu-id="e978d-334">Para las trazas asíncronas puede ser un nombre de la función que inició la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e978d-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="e978d-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="e978d-336">Nombre de la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e978d-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e978d-337">matriz</span><span class="sxs-lookup"><span data-stu-id="e978d-337">parent</span></span> <br/> <i><span data-ttu-id="e978d-338">opcional</span><span class="sxs-lookup"><span data-stu-id="e978d-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e978d-339">Seguimiento asincrónico de la pila de JavaScript que precedía a esta pila, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="e978d-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---
