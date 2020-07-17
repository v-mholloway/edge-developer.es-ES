---
description: Referencia del dominio de depuración. El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.
title: Dominio de depuración-DevTools Protocol versión 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1e76d17e5dfbe39ba61c7cb45a4e88b9fd223068
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882957"
---
# Dominio de depuración-DevTools Protocol versión 0,1 (EdgeHTML)  
  
El dominio del depurador expone capacidades de depuración de JavaScript. Permite establecer y quitar puntos de interrupción, avanzar por la ejecución, explorar los seguimientos de la pila, etc.

| | |
|-|-|
| [**Métodos**](#methods) | [enable](#enable), [Disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [ancho](#stepover) [de es, stepInto](#stepinto) [, stepOut](#stepout), [PAUSE](#pause), [resume](#resume) [, getScriptSource, setPauseOnExceptions](#getscriptsource) [, evaluateOnCallFrame](#setpauseonexceptions) [,](#evaluateoncallframe) [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns) [, msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |
| [**Eventos**](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [reanudado](#resumed) |
| [**Tipos**](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Ubicación](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [ámbito](#scope) |
| [**Dependencias**](#dependencies) | [Tiempo de ejecución](runtime.md) |
## Métodos

### habilitar
Habilita el depurador para la página dada. Los clientes no deben suponer que la depuración se ha habilitado hasta que se reciba el resultado de este comando.


---

### deshabilitar 
Deshabilita el depurador para la página dada.


---

### getPossibleBreakpoints
Devuelve posibles ubicaciones para el punto de interrupción. scriptId en las ubicaciones de intervalo de inicio y de finalización deben ser iguales.

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
            <td>start</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Inicio del rango para buscar posibles ubicaciones de puntos de interrupción en.</td>
        </tr>
        <tr>
            <td>terminar</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Fin del rango para buscar posibles ubicaciones de puntos de interrupción en (excepto). Cuando no se especifica, el final de las secuencias de comandos se usa como fin del rango.</td>
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
            <td>sitios</td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td>Lista de posibles ubicaciones de los puntos de interrupción.</td>
        </tr>
    </tbody>
</table>

---

### setBreakpointsActive
Activa o desactiva todos los puntos de interrupción de la página.

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
            <td>activa</td>
            <td><code class="flyout">boolean</code></td>
            <td>Nuevo valor para puntos de interrupción activo estado.</td>
        </tr>
    </tbody>
</table>

---

### setBreakpointByUrl
Establece un punto de interrupción de JavaScript en la ubicación especificada, por dirección URL o dirección URL Regex. Una vez que se haya emitido este comando, todos los scripts analizados existentes tendrán los puntos de interrupción resueltos y devueltos en la <code>locations</code> propiedad. Además, el análisis de scripts más parecido dará como resultado <code>breakpointResolved</code> eventos posteriores. Este punto de interrupción lógico afectará a las recargas de páginas.

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
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de línea para establecer el punto de interrupción en.</td>
        </tr>
        <tr>
            <td>url <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL de los recursos para establecer el punto de interrupción.</td>
        </tr>
        <tr>
            <td>urlRegex <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Patrón de Regex para las direcciones URL de los recursos para establecer puntos de interrupción. <code>url</code>O <code>urlRegex</code> debe especificarse.</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Desplazamiento en la línea para establecer el punto de interrupción en.</td>
        </tr>
        <tr>
            <td>requisito <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Expresión que se va a usar como condición de punto de interrupción. Cuando se especifica, Debugger solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Identificador del punto de interrupción creado para referencia adicional.</td>
        </tr>
        <tr>
            <td>sitios</td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td>Lista de las ubicaciones en las que se ha resuelto este punto de interrupción.</td>
        </tr>
    </tbody>
</table>

---

### setBreakpoint
Establece un punto de interrupción de JavaScript en una ubicación determinada.

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
            <td>Ubicación</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ubicación en la que se establecerá el punto de interrupción.</td>
        </tr>
        <tr>
            <td>requisito <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Expresión que se va a usar como condición de punto de interrupción. Cuando se especifica, Debugger solo se detendrá en el punto de interrupción si esta expresión se evalúa como true.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Identificador del punto de interrupción creado para referencia adicional.</td>
        </tr>
        <tr>
            <td>actualLocation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ubicación en la que se resuelve este punto de interrupción.</td>
        </tr>
    </tbody>
</table>

---

### removeBreakpoint
Quita el punto de interrupción de JavaScript.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### Pasadas
Pasos sobre la instrucción.


---

### stepInto
Recorre los pasos de la llamada de función.


---

### stepOut
Recorre los pasos de la llamada de función.


---

### pause
Se detiene en la siguiente instrucción de JavaScript.


---

### resume
Reanuda la ejecución de JavaScript.


---

### getScriptSource
Devuelve el origen del script con el identificador especificado.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador del script para el que se va a obtener el origen.</td>
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
            <td>scriptSource</td>
            <td><code class="flyout">string</code></td>
            <td>Origen de script.</td>
        </tr>
    </tbody>
</table>

---

### setPauseOnExceptions
Define la pausa en el estado de las excepciones. Puede establecerse en detener en todas las excepciones, excepciones no detectadas o sin excepciones. El estado de pausa inicial en excepciones es de <code>none</code> .

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
            <td>situación</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: ninguno, no detectados, todos</i></td>
            <td>Pausar en el modo de excepciones.</td>
        </tr>
    </tbody>
</table>

---

### evaluateOnCallFrame
Evalúa Expression en un marco de llamada dado.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identificador de marco de llamada que se va a evaluar.</td>
        </tr>
        <tr>
            <td>Expression</td>
            <td><code class="flyout">string</code></td>
            <td>Expresión que se va a evaluar.</td>
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
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Contenedor de objetos para el resultado de evaluación.</td>
        </tr>
    </tbody>
</table>

---

### setVariableValue
Cambia el valor de la variable en un callframe. Los ámbitos basados en objetos no son compatibles y se deben mutar manualmente.

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
            <td>scopeNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>número de base cero de ámbito que se mostraba en la cadena de ámbitos. Solo se permiten los tipos de ámbito ' local ', ' cierre ' y ' Catch '. Es posible manipular otros ámbitos de forma manual.</td>
        </tr>
        <tr>
            <td>variableName</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la variable.</td>
        </tr>
        <tr>
            <td>Nuevovalor</td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td>Nuevo valor de variable.</td>
        </tr>
        <tr>
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identificador de callframe que contiene la variable.</td>
        </tr>
    </tbody>
</table>

---

### setBlackboxPatterns
<span><b>Montaje. </b></span>Reemplazar patrones de Blackbox anteriores por los que se hayan pasado. Fuerza que el back-end omita la ejecución paso a paso en scripts con una dirección URL que coincide con uno de los patrones. El depurador intentará dejar la secuencia de comandos de blackboxed realizando ' paso a paso ' varias veces, por último, recurriendo a ' paso hacia fuera ' si no se ha realizado correctamente.

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
            <td>modos</td>
            <td><code class="flyout">string[]</code></td>
            <td>Matriz de RegExpS que se usará para comprobar la dirección URL del script para el estado de Blackbox.</td>
        </tr>
    </tbody>
</table>

---

### msSetDebuggerPropertyValue
<span><b>Montaje. </b></span>Microsoft: establece la propiedad de depurador especificada en el valor especificado.

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
            <td>debuggerPropertyId</td>
            <td><code class="flyout">string</code></td>
            <td>Microsoft: el identificador de propiedad (es decir, msDebuggerPropertyId) que se va a establecer.</td>
        </tr>
        <tr>
            <td>Nuevovalor</td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## Eventos

### scriptParsed
Se desencadena cuando se analiza el script. Este evento también se desencadena para todos los scripts conocidos y no recopilados al habilitar el depurador.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador de la secuencia de comandos analizada.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL o nombre de la secuencia de comandos analizada (si hay alguna).</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Desplazamiento de línea del script en el recurso con la dirección URL dada (para etiquetas de script).</td>
        </tr>
        <tr>
            <td>Columnainicio</td>
            <td><code class="flyout">integer</code></td>
            <td>Desplazamiento de columna de la secuencia de comandos en el recurso con la dirección URL proporcionada.</td>
        </tr>
        <tr>
            <td>Fin</td>
            <td><code class="flyout">integer</code></td>
            <td>Última línea de la secuencia de comandos.</td>
        </tr>
        <tr>
            <td>Columnafin</td>
            <td><code class="flyout">integer</code></td>
            <td>Longitud de la última línea de la secuencia de comandos.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td>Especifica el contexto de creación de script.</td>
        </tr>
        <tr>
            <td>sourceMapURL <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL de la asignación de origen asociada con el script (si existe).</td>
        </tr>
        <tr>
            <td>longitud <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Montaje. </b></span>Esta longitud de script.</td>
        </tr>
        <tr>
            <td>msParentId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Montaje. </b></span>Este es el identificador de documento principal.</td>
        </tr>
        <tr>
            <td>msMimeType <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Montaje. </b></span>Este es el tipo MIME.</td>
        </tr>
        <tr>
            <td>msIsDynamicCode <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Montaje. </b></span>Indica si se trata de código dinámico.</td>
        </tr>
        <tr>
            <td>msLongDocumentId <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Montaje. </b></span>Este es el identificador de documento largo.</td>
        </tr>
    </tbody>
</table>

---

### breakpointResolved
Se desencadena cuando el punto de interrupción se resuelve como una secuencia de comandos y una ubicación reales.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Identificador único de punto de interrupción.</td>
        </tr>
        <tr>
            <td>Ubicación</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ubicación real del punto de interrupción.</td>
        </tr>
        <tr>
            <td>msLength <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Montaje. </b></span>Microsoft: longitud del código (es decir, número de caracteres) en la ubicación del punto de interrupción.</td>
        </tr>
    </tbody>
</table>

---

### en pausa
Se desencadena cuando los depuradores se interrumpen por un punto de interrupción o una excepción.

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
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Pila de llamadas: el depurador ha dejado de hacerlo.</td>
        </tr>
        <tr>
            <td>tanto</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: punto de interrupción, paso, excepción, otro</i></td>
            <td>Motivo de la pausa.</td>
        </tr>
        <tr>
            <td>data <br/> <i>opcional</i></td>
            <td><code class="flyout">object</code></td>
            <td>Objeto que contiene propiedades auxiliares específicas de ruptura.</td>
        </tr>
        <tr>
            <td>hitBreakpoints <br/> <i>opcional</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Identificadores de puntos de interrupción del posicionamiento</td>
        </tr>
    </tbody>
</table>

---

### retomada
Se desencadena cuando el depurador reanuda la ejecución.


---

## Tipos

### <a name="breakpointid"></a> BreakpointId `string`

Identificador de punto de interrupción.


---

### <a name="callframeid"></a> CallFrameId `string`

Identificador del marco de la llamada.


---

### <a name="location"></a> Ubicación `object`

Ubicación en el código fuente.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador de script tal y como se indica en el <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de línea en el script (basado en 0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Número de columna en el script (basado en 0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: longitud del código (es decir, número de caracteres) en este marco de llamada.</td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> BreakLocation `object`

Interrumpir la ubicación en el código fuente.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador de script tal y como se indica en el <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número de línea en el script (basado en 0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Número de columna en el script (basado en 0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: longitud del código (es decir, número de caracteres) en este marco de llamada.</td>
        </tr>
        <tr>
            <td>tipo <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Valores permitidos: debuggerStatement, Call, Return.</td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> CallFrame `object`

Marco de llamada de JavaScript. Matriz de marcos de llamadas que forman la pila de llamadas.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identificador del marco de la llamada. Este identificador solo es válido cuando el depurador está en pausa.</td>
        </tr>
        <tr>
            <td>functionName</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la función de JavaScript a la que se llama en este marco de llamada.</td>
        </tr>
        <tr>
            <td>functionLocation <br/> <i>opcional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b>Montaje. </b></span>Ubicación en el código fuente.</td>
        </tr>
        <tr>
            <td>Ubicación</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ubicación en el código fuente.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de script o URL de JavaScript.</td>
        </tr>
        <tr>
            <td>scopeChain</td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td>Cadena de ámbitos para este marco de llamada.</td>
        </tr>
        <tr>
            <td>el</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> objeto para este marco de llamada.</td>
        </tr>
        <tr>
            <td>Vuelto <br/> <i>opcional</i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Valor que se devuelve, si la función está en el punto devuelto.</td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> Ámbito `object`

Descripción del ámbito.

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
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: global, local, con, cierre, Catch, Block, script, eval, módulo</i></td>
            <td>Tipo de ámbito.</td>
        </tr>
        <tr>
            <td>objeto</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Objeto que representa el ámbito. Para <code>global</code> y <code>with</code> ámbitos, representa el objeto real; para el resto de los ámbitos, se trata de las variables de ámbito de la enumeración de objetos transitorias artificiales como sus propiedades.</td>
        </tr>
        <tr>
            <td>name <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td>startLocation <br/> <i>opcional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ubicación en el código fuente donde comienza el ámbito</td>
        </tr>
        <tr>
            <td>endLocation <br/> <i>opcional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ubicación en el código fuente donde el ámbito finaliza</td>
        </tr>
    </tbody>
</table>

---

## Dependencias

[Tiempo de ejecución](runtime.md)