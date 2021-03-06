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
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a>Dominio en tiempo de ejecución: protocolo DevTools versión 0.1 (EdgeHTML)  

El dominio en tiempo de ejecución expone el tiempo de ejecución de JavaScript mediante objetos reflejados y de evaluación remota.  Los resultados de la evaluación se devuelven como objeto reflejado que exponen el tipo de objeto, la representación de cadenas y el identificador único que se puede usar para más referencia de objeto.  Los objetos originales se mantienen en la memoria a menos que se liberan explícitamente.  

| Clasificación | Miembros |  
|:--- |:--- |  
| [Métodos](#methods) | [enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties) |  
| [Eventos](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |  
| [Tipos](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Métodos  

### <a name="enable"></a>habilitar  

Habilita la presentación de informes del `executionContextsCleared` evento.  

&nbsp;  

---  

### <a name="disable"></a>deshabilitar   

Deshabilita la presentación de informes del `executionContextsCleared` evento.  

&nbsp;  

---  

### <a name="evaluate"></a>evaluar  

Evalúa la expresión en el objeto global.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| expresión | `string` | Expresión que se debe evaluar. |  
| silent \(optional\) | `boolean` | En modo silencioso, las excepciones que se inician durante la evaluación no se notifican y no pausan la ejecución.  Invalida el `setPauseOnException` estado. |  
| contextId \(optional\) | [ExecutionContextId](#executioncontextid) | Especifica en qué contexto de ejecución se debe realizar la evaluación.  Si se omite el parámetro, la evaluación se realizará en el contexto de la página inspeccionada. |  
| returnByValue \(optional\) | `boolean` | Si se espera que el resultado sea un objeto JSON que se debe enviar por valor. |  
| awaitPromise \(optional\) | `boolean` | Si la ejecución debe `await` ser para el valor resultante y devolver una vez que se resuelva la promesa esperada. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| resultado | [RemoteObject](#remoteobject) | Resultado de la evaluación. |  

---  

### <a name="callfunctionon"></a>callFunctionOn  

Las llamadas funcionan con una declaración determinada en el objeto especificado.  El grupo de objetos del resultado se hereda del objeto de destino.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| functionDeclaration | `string` | Declaración de la función a la que se llamará. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificador del objeto en el que se debe llamar.  Se `objectId` debe especificar o `executionContextId` no.  objectId debe ser de la función Runtime.evaluate(). |  
| argumentos \(optional\) | [CallArgument[]](#callargument) | Argumentos de llamada.  Todos los argumentos de llamada deben pertenecer al mismo mundo de JavaScript que el objeto de destino. |  
| silent \(optional\) | `boolean` | En modo silencioso, las excepciones que se inician durante la evaluación no se notifican y no pausan la ejecución.  Invalida el `setPauseOnException` estado. |  
| returnByValue \(optional\) | `boolean` | Si se espera que el resultado sea un objeto JSON que se debe enviar por valor. |  
| awaitPromise \(optional\) | `boolean` | Si la ejecución debe `await` ser para el valor resultante y devolver una vez que se resuelva la promesa esperada. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| resultado | [RemoteObject](#remoteobject) | Resultado de la llamada. |  

---  

### <a name="getproperties"></a>getProperties  

Devuelve las propiedades de un objeto determinado.  El grupo de objetos del resultado se hereda del objeto de destino.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Identificador del objeto para el que se devolverán las propiedades.  `objectId` debe ser de la `Debugger.evaluateOnCallFrame()` función. |  
| ownProperties \(optional\) | `boolean` | Si `true` , devuelve propiedades que pertenecen solo al elemento en sí, no a su cadena prototipo. |  
| accessorPropertiesOnly \(optional\) | `boolean` | **Experimental**.  Si `true` , devuelve las propiedades del accessor \(with getter/setter\) solo; tampoco se devuelven las propiedades internas. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| resultado | [PropertyDescriptor[]](#propertydescriptor) | Propiedades del objeto. |  

---  

## <a name="events"></a>Eventos  

### <a name="executioncontextscleared"></a>executionContextsCleared  

Se emite cuando se borraron todos los executionContexts en el explorador.  

&nbsp;  

---  

### <a name="exceptionthrown"></a>exceptionThrown  

Se emitió cuando se produjo la excepción y no se controló.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| marca de tiempo | [Timestamp](#timestamp) | Marca de tiempo de la excepción. |  
| exceptionDetails | [ExceptionDetails](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a>Tipos  

### <a name="scriptid-string"></a>Cadena ScriptId  

<a name="scriptid"></a>  

Identificador de script único.  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a>Cadena RemoteObjectId  

<a name="remoteobjectid"></a>  

Identificador de objeto único.  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a>Cadena UnserializableValue  

<a name="unserializablevalue"></a>  

Valor primitivo que no puede ser cadena JSON.  

##### <a name="allowed-values"></a>Valores permitidos  

`Infinity`, `NaN`, `-Infinity`, `-0`  

---  

### <a name="remoteobject-object"></a>Objeto RemoteObject  

<a name="remoteobject"></a>  

Objeto Mirror que hace referencia al objeto JavaScript original.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| tipo | `string` | Tipo de objeto.  Valores permitidos:  `object` , , , , , `function` `undefined` `string` `number` `boolean` y `symbol` |  
| subtipo \(optional\) | `string` | Sugerencia de subtipo de objeto.  Se especifica solo `object` para los valores de tipo.  Valores permitidos:  `null` `error` , y `promise` |  
| className \(optional\) | `string` | Nombre de clase de objeto \(constructor\).  Se especifica solo `object` para los valores de tipo. |  
| value \(optional\) | `any` | Valor de objeto remoto en caso de valores primitivos o valores JSON \(si se solicitó\). |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | El valor primitivo que no puede tener cadena JSON no tiene `value` , pero obtiene esta propiedad. |  
| description \(optional\) | `string` | Representación de cadena del objeto. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificador de objeto único \(para valores no primitivos\). |  
| msDebuggerPropertyId \(optional\) | `string` | **Experimental**.  Microsoft: el identificador de propiedad del depurador asociado para este objeto. |  

---  

### <a name="propertydescriptor-object"></a>PropertyDescriptor (objeto)  

<a name="propertydescriptor"></a>  

Descriptor de la propiedad Object.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| name | `string` | Nombre de la propiedad o descripción del símbolo. |  
| value \(optional\) | [RemoteObject](#remoteobject) | Valor asociado a la propiedad. |  
| writable \(optional\) | `boolean` | `True` si se puede cambiar el valor asociado a la propiedad \(data descriptors only\). |  
| get \(optional\) | [RemoteObject](#remoteobject) | Función que sirve como getter para la propiedad, o si no hay ningún descriptor de acceso `undefined` \(descriptores de acceso\). |  
| set \(optional\) | [RemoteObject](#remoteobject) | Función que sirve como setter para la propiedad, o si no hay ningún `undefined` setter \(descriptores de descriptores de acceso solamente\). |  
| configurable | `boolean` | `True` si se puede cambiar el tipo de descriptor de esta propiedad y si la propiedad se puede eliminar del objeto correspondiente. |  
| enumerable | `boolean` | `True` si esta propiedad se muestra durante la enumeración de las propiedades del objeto correspondiente. |  
| wasThrown \(optional\) | `boolean` | `True` si el resultado se ha arrojado durante la evaluación. |  
| isOwn \(optional\) | `boolean` | `True` si la propiedad es propiedad del objeto. |  
| msReturnValue \(optional\) | `boolean` | **Experimental**.  Microsoft:  `True` si la propiedad es un valor devuelto. |  
| símbolo \(optional\) | [RemoteObject](#remoteobject) | Objeto de símbolo de propiedad, si la propiedad es del `symbol` tipo. |  

---  

### <a name="callargument-object"></a>CallArgument (objeto)  

<a name="callargument"></a>  

Representa el argumento de llamada de función.  Debe especificarse el identificador de objeto remoto, el valor primitivo no extraíble o ninguno de `value` \(para undefined\).  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| value \(optional\) | `any` | Valor primitivo o objeto javascript serializable. |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Valor primitivo que no puede estar en cadena JSON. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Controlador de objetos remoto. |  

---  

### <a name="executioncontextid-integer"></a>Número entero ExecutionContextId  

<a name="executioncontextid"></a>  

Id. de un contexto de ejecución.  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a>ExceptionDetails (objeto)  

<a name="exceptiondetails"></a>  

Información detallada sobre la excepción \(o error\) que se produjo durante la compilación o ejecución de scripts.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| exceptionId | `integer` | Identificador de excepción. |  
| texto | `string` | Texto de excepción, que debe usarse junto con el objeto de excepción cuando esté disponible. |  
| lineNumber | `integer` | Número de línea de la ubicación de excepción \(0-based\). |  
| columnNumber | `integer` | Número de columna de la ubicación de excepción \(0-based\). |  
| scriptId \(optional\) | [ScriptId](#scriptid) | Identificador de script de la ubicación de excepción. |  
| url \(optional\) | `string` | Dirección URL de la ubicación de excepción, que se usará cuando no se haya notificado el script. |  
| stackTrace \(optional\) | [StackTrace](#stacktrace) | Seguimiento de pila de JavaScript si está disponible. |  
| excepción \(optional\) | [RemoteObject](#remoteobject) | Objeto Exception si está disponible. |  
| executionContextId \(optional\) | [ExecutionContextId](#executioncontextid) | Identificador del contexto donde se produjo la excepción. |  

---  

### <a name="timestamp-integer"></a>Número entero de marca de tiempo  

<a name="timestamp"></a>  

Número de milisegundos desde la época.  

&nbsp;  

---  

### <a name="callframe-object"></a>CallFrame (objeto)  

<a name="callframe"></a>  

Entrada de pila para errores y aserciones en tiempo de ejecución.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| functionName | `string` | Nombre de la función JavaScript. |  
| scriptId | [ScriptId](#scriptid) | Id. de script de JavaScript. |  
| url | `string` | Dirección URL o nombre de script de JavaScript. |  
| lineNumber | `integer` | Número de línea de script de JavaScript \(basado en 0\). |  
| columnNumber | `integer` | Número de columna de script de JavaScript \(0-based\). |  

---  

### <a name="stacktrace-object"></a>StackTrace (objeto)  

<a name="stacktrace"></a>  

Marcos de llamadas para aserciones o mensajes de error.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| description \(optional\) | `string` | Etiqueta de cadena de este seguimiento de pila.  Para los seguimientos asincrónicos, puede ser un nombre de la función que inició la llamada asincrónica. |  
| callFrames | [CallFrame[]](#callframe) | Nombre de la función JavaScript. |  
| parent \(optional\) | [StackTrace](#stacktrace) | Seguimiento de pila de JavaScript asincrónico que precedía a esta pila, si está disponible. |  

---  
