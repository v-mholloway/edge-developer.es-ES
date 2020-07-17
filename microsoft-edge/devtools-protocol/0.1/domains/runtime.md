---
description: Referencia del dominio en tiempo de ejecución. El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.
title: Dominio de tiempo de ejecución-protocolo de DevTools versión 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 15d6cd254ddbe2337e3db850620dc3eb20a5ea67
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882936"
---
# Dominio de tiempo de ejecución-protocolo de DevTools versión 0,1 (EdgeHTML)  

El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript por medio de objetos de evaluación y reflejo remotos. Los resultados de la evaluación se devuelven como un objeto de espejo que expone el tipo de objeto, la representación de cadena y el identificador único que se puede usar para más referencias de objeto. Los objetos originales se mantienen en la memoria, a menos que se hayan liberado explícitamente.

| | |
|-|-|
| [**Métodos**](#methods) | [enable](#enable), [Disable](#disable), [Evaluate](#evaluate), [callFunctionOn](#callfunctionon), [GetProperties](#getproperties) |
| [**Eventos**](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |
| [**Tipos**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |
## Métodos

### habilitar
Permite informar del <code>executionContextsCleared</code> evento.


---

### deshabilitar 
Deshabilita los informes del <code>executionContextsCleared</code> evento.


---

### considerar
Evalúa Expression en el objeto global.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Expression</td>
            <td><code class="flyout">string</code></td>
            <td>Expresión que se va a evaluar.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>En modo silencioso, no se notifican las excepciones producidas durante la evaluación y no pausan la ejecución. Estado de invalidaciones <code>setPauseOnException</code> .</td>
        </tr>
        <tr>
            <td>contextId <br/> <i>opcional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Especifica el contexto de ejecución para realizar la evaluación. Si se omite el parámetro, la evaluación se realizará en el contexto de la página inspeccionada.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la ejecución debe tener el <code>await</code> valor resultante y la devolución una vez que se resuelve la promesa esperada.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>resultado</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Resultado de evaluación.</td>
        </tr>
    </tbody>
</table>

---

### callFunctionOn
Función calls con declaración dada en el objeto dado. El grupo de objetos del resultado se hereda del objeto de destino.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>functionDeclaration</td>
            <td><code class="flyout">string</code></td>
            <td>Declaración de la función que se va a llamar.</td>
        </tr>
        <tr>
            <td>ID <br/> <i>opcional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador del objeto en el que se va a llamar. Debe especificar objectId o executionContextId.  objectId debe ser de la función Runtime. Evaluate ().</td>
        </tr>
        <tr>
            <td>arguments <br/> <i>opcional</i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td>Argumentos de la llamada. Todos los argumentos de la llamada deben pertenecer al mismo mundo de JavaScript que el objeto de destino.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>En modo silencioso, no se notifican las excepciones producidas durante la evaluación y no pausan la ejecución. Estado de invalidaciones <code>setPauseOnException</code> .</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si se espera que el resultado sea un objeto JSON que se debe enviar por valor.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la ejecución debe tener el <code>await</code> valor resultante y la devolución una vez que se resuelve la promesa esperada.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>resultado</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Resultado de la llamada.</td>
        </tr>
    </tbody>
</table>

---

### getProperties
Devuelve las propiedades de un objeto determinado. El grupo de objetos del resultado se hereda del objeto de destino.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ID</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador del objeto para el que se van a devolver las propiedades.  objectId debe ser de la función Debugger. evaluateOnCallFrame ().</td>
        </tr>
        <tr>
            <td>ownProperties <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si es true, devuelve propiedades pertenecientes al propio elemento, no a su cadena de prototipo.</td>
        </tr>
        <tr>
            <td>accessorPropertiesOnly <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Montaje. </b></span>Si es verdadero, devuelve propiedades del descriptor de acceso (solo con el captador/establecedor); las propiedades internas no se devuelven.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>resultado</td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td>Propiedades del objeto.</td>
        </tr>
    </tbody>
</table>

---

## Eventos

### executionContextsCleared
Se emite cuando se han borrado todas las executionContexts en el explorador


---

### exceptionThrown
Se emite cuando se ha iniciado una excepción y no se ha controlado.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>marca</td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Marca de fecha y hora de la excepción.</td>
        </tr>
        <tr>
            <td>exceptionDetails</td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## Tipos

### <a name="scriptid"></a> ScriptId `string`

Identificador de script único.


---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Identificador de objeto único.


---

### <a name="unserializablevalue"></a> UnserializableValue `string`

Valor primitivo que no puede ser JSON-stringified.

##### Valores permitidos
Infinity, NaN,-Infinity,-0

---

### <a name="remoteobject"></a> RemoteObject `object`

Objeto Mirror que hace referencia al objeto de JavaScript original.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>tipo</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: objeto, función, sin definir, cadena, número, booleano, símbolo</i></td>
            <td>Tipo de objeto.</td>
        </tr>
        <tr>
            <td>subtipo <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: null, error, Promise</i></td>
            <td>Sugerencia de subtipo de objeto. Especificado <code>object</code> solo para los valores de tipo.</td>
        </tr>
        <tr>
            <td>className <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la clase de objeto (constructor). Especificado <code>object</code> solo para los valores de tipo.</td>
        </tr>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><code class="flyout">any</code></td>
            <td>Valor del objeto remoto en caso de valores primitivos o valores de JSON (si se solicitó).</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>opcional</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>El valor primitivo que no puede ser JSON-stringified no tiene <code>value</code>, pero obtiene esta propiedad.</td>
        </tr>
        <tr>
            <td>description <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Representación de cadena del objeto.</td>
        </tr>
        <tr>
            <td>ID <br/> <i>opcional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador de objeto único (para valores no primitivos).</td>
        </tr>
        <tr>
            <td>msDebuggerPropertyId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Montaje. </b></span>Microsoft: el identificador de propiedad de depurador asociado para este objeto.</td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> PropertyDescriptor `object`

Descriptor de propiedad de objeto.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de propiedad o descripción de símbolo.</td>
        </tr>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>El valor asociado a la propiedad.</td>
        </tr>
        <tr>
            <td>pueda <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si el valor asociado a la propiedad puede cambiarse (solo para descriptores de datos).</td>
        </tr>
        <tr>
            <td>obtener <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Una función que sirve como captador para la propiedad o si no hay <code>undefined</code> ningún captador (solo descriptores de acceso).</td>
        </tr>
        <tr>
            <td>set <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Una función que sirve como un establecedor para la propiedad o <code>undefined</code> si no hay ningún establecedor (solo descriptores de acceso).</td>
        </tr>
        <tr>
            <td>puedan</td>
            <td><code class="flyout">boolean</code></td>
            <td>True si el tipo de este descriptor de propiedades se puede cambiar y si la propiedad se puede eliminar del objeto correspondiente.</td>
        </tr>
        <tr>
            <td>enumera</td>
            <td><code class="flyout">boolean</code></td>
            <td>True si esta propiedad se muestra durante la enumeración de las propiedades del objeto correspondiente.</td>
        </tr>
        <tr>
            <td>wasThrown <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si el resultado se produjo durante la evaluación.</td>
        </tr>
        <tr>
            <td>isOwn <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si la propiedad es propiedad del objeto.</td>
        </tr>
        <tr>
            <td>msReturnValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Montaje. </b></span>Microsoft: true si la propiedad es un valor devuelto.</td>
        </tr>
        <tr>
            <td>símbolo <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Objeto de símbolo de propiedad, si la propiedad es del `symbol` tipo. </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> CallArgument `object`

Representa el argumento de la llamada de función. <code>objectId</code>Se debe especificar el identificador de objeto remoto, el primitivo <code>value</code> , el valor primitivo inserializable o ninguno de los dos (no definidos).

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><code class="flyout">any</code></td>
            <td>Valor primitivo o objeto serializable de JavaScript.</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>opcional</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Valor primitivo que no puede ser JSON-stringified.</td>
        </tr>
        <tr>
            <td>ID <br/> <i>opcional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Controlador de objeto remoto.</td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> ExecutionContextId `integer`

Identificador de un contexto de ejecución.


---

### <a name="exceptiondetails"></a> ExceptionDetails `object`

Información detallada sobre la excepción (o error) que se produjo durante la compilación o ejecución de scripts.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>exceptionId</td>
            <td><code class="flyout">integer</code></td>
            <td>Identificador de excepción.</td>
        </tr>
        <tr>
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto de excepción, que debe usarse junto con el objeto de excepción cuando esté disponible.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de línea de la ubicación de excepción (basada en 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de columna de la ubicación de excepción (basado en 0).</td>
        </tr>
        <tr>
            <td>scriptId <br/> <i>opcional</i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>IDENTIFICADOR de script de la ubicación de excepción.</td>
        </tr>
        <tr>
            <td>url <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL de la ubicación de excepción que se usará cuando no se notificó el script.</td>
        </tr>
        <tr>
            <td>stackTrace <br/> <i>opcional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Seguimiento de la pila de JavaScript si está disponible.</td>
        </tr>
        <tr>
            <td>excepción <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Objeto de excepción si está disponible.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>opcional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Identificador del contexto en el que se produjo la excepción.</td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> Timestamp `integer`

Número de milisegundos desde la época.


---

### <a name="callframe"></a> CallFrame `object`

Entrada de pila para errores y aserciones en tiempo de ejecución.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>functionName</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la función JavaScript.</td>
        </tr>
        <tr>
            <td>scriptId</td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>ID. de script de JavaScript.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de script o URL de JavaScript.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de línea de script de JavaScript (basado en 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de columna de script de JavaScript (basado en 0).</td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> StackTrace `object`

Llamar a marcos para las aserciones o los mensajes de error.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>description <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Etiqueta de cadena de este seguimiento de pila. Para las trazas asíncronas puede ser un nombre de la función que inició la llamada asincrónica.</td>
        </tr>
        <tr>
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Nombre de la función JavaScript.</td>
        </tr>
        <tr>
            <td>matriz <br/> <i>opcional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Seguimiento asincrónico de la pila de JavaScript que precedía a esta pila, si está disponible.</td>
        </tr>
    </tbody>
</table>

---
