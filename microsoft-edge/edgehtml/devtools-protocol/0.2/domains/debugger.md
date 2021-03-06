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
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a>Dominio del depurador: protocolo DevTools versión 0.2 (EdgeHTML)  

El dominio del depurador expone las capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, recorrer la ejecución, explorar seguimientos de pila, etc.

| Clasificación | Miembros |  
|:--- |:--- |  
| [**Métodos**](#methods) | [enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepout), [stepOut](#stepinto), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |  
| [**Eventos**](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed) |  
| [**Tipos**](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope) |  
| [**Dependencias**](#dependencies) | [Tiempo de ejecución](./runtime.md) |  

## <a name="methods"></a>Métodos  

### <a name="enable"></a>habilitar  

Habilita el depurador para la página determinada. Los clientes no deben asumir que la depuración se ha habilitado hasta que se reciba el resultado de este comando.  

&nbsp;  

---  

### <a name="disable"></a>deshabilitar   

Deshabilita el depurador para una página determinada.  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a>getPossibleBreakpoints  

Devuelve posibles ubicaciones para el punto de interrupción. scriptId en las ubicaciones de intervalo inicial y final debe ser el mismo.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| start | [Ubicación](#location) | Inicio del intervalo en el que buscar posibles ubicaciones de punto de interrupción. |  
| terminar | [Ubicación](#location) | Fin del intervalo para buscar posibles ubicaciones de punto de interrupción en \(excluding\).  Cuando no se especifica, el final de los scripts se usa como fin del intervalo. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| ubicaciones | [BreakLocation](#breaklocation) | Lista de las posibles ubicaciones de punto de interrupción. |  

---  

### <a name="setbreakpointsactive"></a>setBreakpointsActive  

Activa/desactiva todos los puntos de interrupción de la página.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| activa | `boolean` | Nuevo valor para el estado activo de puntos de interrupción. | 

---  

### <a name="setbreakpointbyurl"></a>setBreakpointByUrl  

Establece el punto de interrupción de JavaScript en una ubicación determinada especificada por dirección URL o url regex.  Una vez emitido este comando, todos los scripts de análisis existentes tendrán puntos de interrupción resueltos y devueltos en la `locations` propiedad.  El análisis de scripts de coincidencia adicional dará como resultado la emisión `breakpointResolved` de eventos posteriores.  Este punto de interrupción lógico sobrevivirá a las recargas de página.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| lineNumber | `integer` | Número de línea en el que se establece el punto de interrupción. | 
| url \(optional\) | `string` | Dirección URL de los recursos en los que se establece el punto de interrupción. |  
| urlRegex \(optional\) | `string` | Patrón Regex para las direcciones URL de los recursos en las que se establecen los puntos de interrupción.  O `url` `urlRegex` debe especificarse. |  
| columnNumber \(optional\) | `integer` | Desplazamiento en la línea en la que se establece el punto de interrupción. |  
| condición \(optional\) | `string` | Expresión que se usará como condición de punto de interrupción. Cuando se especifica, el depurador solo se detendrá en el punto de interrupción si esta expresión se evalúa como true. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Identificador del punto de interrupción creado para obtener más referencia. |  
| ubicaciones | [Location[]](#location) | Lista de las ubicaciones en las que se resolvió este punto de interrupción tras su adición. |  

---  

### <a name="setbreakpoint"></a>setBreakpoint  

Establece el punto de interrupción de JavaScript en una ubicación determinada.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| ubicación | [Ubicación](#location) | Ubicación en la que se establece el punto de interrupción. |  
| condición \(optional\) | `string` | Expresión que se usará como condición de punto de interrupción.  Cuando se especifica, el depurador solo se detendrá en el punto de interrupción si esta expresión se evalúa como true. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Identificador del punto de interrupción creado para obtener más referencia. |  
| actualLocation | [Ubicación](#location) | Ubicación en la que se resolvió este punto de interrupción. |  

---  

### <a name="removebreakpoint"></a>removeBreakpoint  

Quita el punto de interrupción de JavaScript.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a>stepOver  

Pasos sobre la instrucción.  

&nbsp;  

---  

### <a name="stepinto"></a>stepInto  

Pasos en la llamada de función.  

&nbsp;  

---  

### <a name="stepout"></a>stepOut  

Sale de la llamada de función.  

&nbsp;  

---  

### <a name="pause"></a>pause  

Se detiene en la siguiente instrucción JavaScript.  

&nbsp;  

---  

### <a name="resume"></a>resume  

Reanuda la ejecución de JavaScript.  

&nbsp;  

---  

### <a name="getscriptsource"></a>getScriptSource  

Devuelve el origen del script con el identificador especificado.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Id. del script para obtener el origen. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| scriptSource | `string` | Origen de script. | 

---  

### <a name="setpauseonexceptions"></a>setPauseOnExceptions  

Define la pausa en el estado de excepciones.  Se puede establecer para detener todas las excepciones, excepciones no detectadas o ninguna excepción.  La pausa inicial en el estado de excepciones es `none` .  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| state | `string` | Pausa en el modo de excepciones.  Valores permitidos:  `none` , `uncaught` , `all` |  

---  

### <a name="evaluateoncallframe"></a>evaluateOnCallFrame  

Evalúa la expresión en un marco de llamada determinado.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Identificador de marco de llamada para evaluar. |  
| expresión | `string` | Expresión que se debe evaluar. | 

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| resultado | [Runtime.RemoteObject](./runtime.md#remoteobject) | Contenedor de objetos para el resultado de evaluación. |  

---  

### <a name="setvariablevalue"></a>setVariableValue  

Cambia el valor de variable en un fotograma de llamada.  Los ámbitos basados en objetos no son compatibles y deben mutarse manualmente.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| scopeNumber | `integer` | Número de ámbito basado en 0 tal como se insumía en la cadena de ámbito.  Solo `local` se permiten , y los tipos de `closure` `catch` ámbito.  Otros ámbitos se pueden manipular manualmente. | 
| variableName | `string` | Nombre de variable. | 
| newValue | [Runtime.CallArgument](./runtime.md#callargument) | Nuevo valor de variable. |  
| callFrameId | [CallFrameId](#callframeid) | Id. de trama de llamada que contiene variable. |  

---  

### <a name="setblackboxpatterns"></a>setBlackboxPatterns  

**Experimental**.  Reemplace los patrones de la caja negra anteriores por los pasados.  Fuerza al back-end a omitir el paso a paso o la pausa en scripts con una dirección URL que coincida con uno de los patrones.  El depurador intentará dejar el script en caja negra realizando el "step in" varias veces y, por último, recurrirá a "step out" si no se ejecuta correctamente.  


| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| patrones | `string[]` | Matriz de regexps que se usará para comprobar la dirección URL del script para el estado de la caja negra. | 

---  

### <a name="mssetdebuggerpropertyvalue"></a>msSetDebuggerPropertyValue  

**Experimental**.  Microsoft: establece la propiedad depurador especificada en el valor especificado.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| debuggerPropertyId | string | Microsoft: el identificador de propiedad \(es decir, `msDebuggerPropertyId` \) que se debe establecer. | 
| newValue | `string` | &nbsp; |  

---  

## <a name="events"></a>Eventos  

### <a name="scriptparsed"></a>scriptParsed  

Se desencadena cuando se analiza el script. Este evento también se desencadena para todos los scripts conocidos y no reconocidos al habilitar el depurador.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificador del script analizado. |  
| url | `string` | Dirección URL o nombre del script analizada \(si la hay\). | 
| startLine | `integer` | Desplazamiento de línea del script dentro del recurso con la dirección URL especificada \(para etiquetas de script\). | 
| startColumn | `integer` | Desplazamiento de columna del script dentro del recurso con una dirección URL determinada. | 
| endLine | `integer` | Última línea del script. | 
| endColumn | `integer` | Longitud de la última línea del script. | 
| executionContextId | [Runtime.ExecutionContextId](./runtime.md#executioncontextid) | Especifica el contexto de creación de scripts. |  
| sourceMapURL \(optional\) | `string` | Dirección URL del mapa de origen asociado con script (si lo hubiera). |  
| length \(optional\) | `integer` | **Experimental**.  Esta longitud de script. |  
| msParentId \(optional\) | `string` | **Experimental**.  Este es el identificador del documento primario. |  
| msMimeType \(optional\) | `string` | **Experimental**.  Este es el tipo mime. |  
| msIsDynamicCode \(optional\) | `boolean` | **Experimental**.  Esto indica si se trata de código dinámico. |  
| msLongDocumentId \(optional\) | `integer` | **Experimental**.  Este es el identificador de documento largo. |  

---  

### <a name="breakpointresolved"></a>breakpointResolved  

Se desencadena cuando el punto de interrupción se resuelve en un script y una ubicación reales.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Identificador único de punto de interrupción. |  
| ubicación | [Ubicación](#location) | Ubicación real del punto de interrupción. |  
| msLength \(optional\) | `integer` | **Experimental**.  Microsoft: longitud del código \(es decir, número de caracteres\) en la ubicación del punto de interrupción. |  

---  

### <a name="paused"></a>en pausa  

Se desencadena cuando los depuradores se interrumpen para un punto de interrupción o una excepción.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| callFrames | [CallFrame[]](#callframe) | Pila de llamadas en la que se detuvo el depurador. |  
| motivo | `string` |  Motivo de pausa.  Valores permitidos:  `breakpoint` `step` , , , `exception` `other` y `EventListener` |  
| data \(optional\) | `object` | Objeto que contiene propiedades auxiliares específicas de interrupción. |  
| hitBreakpoints \(optional\) | `string[]` | Hit breakpoints IDs |  
| asyncStackTrace \(optional\) | `StackTrace` | Seguimiento de pila asincrónica de JavaScript. |  

---  

### <a name="resumed"></a>reanudado  

Se desencadena cuando el depurador reanuda la ejecución.  

&nbsp;  

---  

## <a name="types"></a>Tipos  

### <a name="breakpointid-string"></a>Cadena BreakpointId  

<a name="breakpointid"></a>  

Identificador de punto de interrupción.  

&nbsp;  

---  

### <a name="callframeid-string"></a>Cadena CallFrameId  

<a name="callframeid"></a>  

Identificador de marco de llamada.  

&nbsp;  

---  

### <a name="location-object"></a>Location (objeto)  

<a name="location"></a>  

Ubicación en el código fuente.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificador de script como se ha notificado en `Debugger.scriptParsed` el archivo . |  
| lineNumber | `integer` | Número de línea en el script \(0-based\). |  
| columnNumber \(optional\) | `integer` | Número de columna en el script \(0-based\). |  
| msLength | `integer` | Microsoft: longitud del código \(es decir, número de caracteres\) en este marco de llamada. |  

---  

### <a name="breaklocation-object"></a>BreakLocation (objeto)  

<a name="breaklocation"></a>  

Ubicación de interrupción en el código fuente.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificador de script como se ha notificado en `Debugger.scriptParsed` el archivo . |  
| lineNumber | `integer` | Número de línea en el script \(0-based\). |  
| columnNumber \(optional\) | `integer` | Número de columna en el script \(0-based\). |  
| msLength | `integer` | Microsoft: longitud del código \(es decir, número de caracteres\) en este marco de llamada. |  
| tipo \(optional\) | `string` | Valores permitidos: debuggerStatement, call, return. |  

---  

### <a name="callframe-object"></a>CallFrame (objeto)  

<a name="callframe"></a>  

Marco de llamada de JavaScript. La matriz de marcos de llamadas forma la pila de llamadas.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Identificador de marco de llamada.  Este identificador solo es válido mientras el depurador está en pausa. |  
| functionName | `string` | Nombre de la función JavaScript llamada en este marco de llamada. |  
| functionLocation \(optional\) | [Ubicación](#location) | **Experimental**.  Ubicación en el código fuente. |  
| ubicación | [Ubicación](#location) | Ubicación en el código fuente. |  
| url | `string` | Dirección URL o nombre de script de JavaScript. |  
| scopeChain | [Scope[]](#scope) | Cadena de ámbito para este marco de llamada. |  
| this | [Runtime.RemoteObject](./runtime.md#remoteobject) | `this` para este marco de llamada. |  
| returnValue \(optional\) | [Runtime.RemoteObject](./runtime.md#remoteobject) | Valor que se devuelve, si la función está en el punto de devolución. |  

---  

### <a name="scope-object"></a>Scope (objeto)  

<a name="scope"></a>  

Descripción del ámbito.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| tipo | `string` | Tipo de ámbito.  Valores permitidos:  `global` , , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` `module` y `return` |  
| objeto | [Runtime.RemoteObject](./runtime.md#remoteobject) | Objeto que representa el ámbito.  For y scopes representa el objeto real; para el resto de ámbitos, es un objeto transitorio artificial que enumera las variables de `global` `with` ámbito como sus propiedades. |  
| nombre \(optional\) | `string` | &nbsp; |  
| startLocation \(optional\) | [Ubicación](#location) | Ubicación en el código fuente donde se inicia el ámbito. |  
| endLocation \(optional\) | [Ubicación](#location) | Ubicación en el código fuente donde finaliza el ámbito. |  

---  

## <a name="dependencies"></a>Dependencias  

[Tiempo de ejecución](./runtime.md)  
