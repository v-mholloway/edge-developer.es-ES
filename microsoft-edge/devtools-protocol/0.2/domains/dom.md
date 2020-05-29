---
description: Referencia del dominio DOM. Este dominio expone las operaciones de lectura y escritura de DOM. Cada nodo DOM se representa con su objeto reflejado que tiene una `id` . Esto `id` se puede usar para obtener información adicional sobre el nodo, resolverlo en el contenedor de objetos de JavaScript, etc. Es importante que el cliente reciba eventos DOM solo para los nodos que son conocidos para el cliente. El back-end realiza un seguimiento de los nodos que se enviaron al cliente y nunca envía dos veces el mismo nodo. Es responsabilidad del cliente recopilar información acerca de los nodos que se enviaron al cliente.<p>Tenga en cuenta que `iframe` los elementos propietarios devolverán los elementos del documento correspondientes como sus nodos secundarios.</p>
title: 'Dominio DOM: DevTools Protocol versión 0,2'
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 9ebe5ff709ac2981cb2359b7279c5d4e5d375426
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573740"
---
# DOM
Este dominio expone las operaciones de lectura y escritura de DOM. Cada nodo DOM se representa con su objeto reflejado que tiene una `id` . Esto `id` se puede usar para obtener información adicional sobre el nodo, resolverlo en el contenedor de objetos de JavaScript, etc. Es importante que el cliente reciba eventos DOM solo para los nodos que son conocidos para el cliente. El back-end realiza un seguimiento de los nodos que se enviaron al cliente y nunca envía dos veces el mismo nodo. Es responsabilidad del cliente recopilar información acerca de los nodos que se enviaron al cliente.<p>Tenga en cuenta que `iframe` los elementos propietarios devolverán los elementos del documento correspondientes como sus nodos secundarios.</p>

| | |
|-|-|
| [**Métodos**](#methods) | [enable](#enable), [Disable](#disable), [getdocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), requestNode, [setInspectedNode](#setinspectednode) [resolveNode](#requestnode) [, setInspectedNode](#resolvenode) |
| [**Eventos**](#events) | [setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated) |
| [**Tipos**](#types) | [RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype) |
| [**Dependencias**](#dependencies) | [Motores](runtime.md) |
## Métodos

### habilitar
Habilita el agente DOM para la página dada.

</p>

---

### deshabilitar 
Deshabilita el agente DOM para la página dada. Al deshabilitar el DOM, se invalidará cualquier nodeIds válido anteriormente.

</p>

---

### getDocument
Devuelve el nodo DOM raíz (y, opcionalmente, el subárbol) al autor de la llamada. `getDocument`Las llamadas invalidarán cualquier nodeIds válida anterior

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
            <td>Prof</td>
            <td><code class="flyout">integer</code></td>
            <td>La profundidad máxima a la que se deben recuperar los niños; el valor predeterminado es 2. Use-1 para todo el subárbol.</td>
        </tr>
        <tr>
            <td>atraviese</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si se debe atravesar iframes o no al devolver el subárbol (el valor predeterminado es false).</td>
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
            <td>carpeta</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Nodo resultante.</td>
        </tr>
    </tbody>
</table>
</p>

---

### highlightNode
Higlights un nodo DOM con identificador determinado o contenedor de objetos. se debe especificar nodeId, backendNodeId o objectId.

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
            <td>nodeId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que se va a resaltar.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>opcional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificador del nodo de back-end que se va a resaltar.</td>
        </tr>
        <tr>
            <td>ID <br/> <i>opcional</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>Identificador de objeto de JavaScript del nodo que se va a resaltar.</td>
        </tr>
        <tr>
            <td>higlightConfig</td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td>Descriptor de la apariencia del resaltado.</td>
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
            <td>carpeta</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Nodo resultante.</td>
        </tr>
    </tbody>
</table>
</p>

---

### hideHighlight
Oculta cualquier resaltado del nodo DOM actual.

</p>

---

### requestChildNodes
Solicitudes que los elementos secundarios del nodo con el identificador dado se devuelven a la persona que llama a GHE en forma de `setChildNodes` eventos. `setChildNodes` se desencadenará para cada nodo que no haya devuelto anteriormente a elementos secundarios, empezando desde el nodo solicitado hasta la profundidad especificada.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo del que se obtendrán los elementos secundarios.</td>
        </tr>
        <tr>
            <td>Prof</td>
            <td><code class="flyout">integer</code></td>
            <td>La profundidad máxima a la que se deben recuperar los niños; el valor predeterminado es 1. Use-1 para todo el subárbol.</td>
        </tr>
        <tr>
            <td>atraviese</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si se debe atravesar iframes o no al devolver el subárbol (el valor predeterminado es false).</td>
        </tr>
    </tbody>
</table>
</p>

---

### getAttributes
Devuelve los atributos del nodo especificado.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo para el que se va a recuperar el attibutes.</td>
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
            <td>atributos</td>
            <td><code class="flyout">string[]</code></td>
            <td>Matriz intercalada de nombres y valores de atributos de nodos.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getOuterHTML
Devuelve el formato HTML del nodo.

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
            <td>nodeId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>opcional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificador del nodo back-end.</td>
        </tr>
        <tr>
            <td>ID <br/> <i>opcional</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>Identificador de objeto de JavaScript del contenedor del nodo.</td>
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
            <td>outerHTML</td>
            <td><code class="flyout">string</code></td>
            <td>Formato HTML externo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pushNodesByBackendIdsToFrontend
Busca identificadores de nodo y resuelve todos los elementos primarios de los identificadores de nodo de back-end especificados

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
            <td>backendNodeIds</td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td>Identificadores de nodo back-end de los nodos que se van a resolver</td>
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
            <td>nodeIds</td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Identificadores de nodo de los nodos resueltos</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelector
Se ejecuta `querySelector` en un nodo determinado.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo sobre el que se realizará la consulta.</td>
        </tr>
        <tr>
            <td>lector</td>
            <td><code class="flyout">string</code></td>
            <td>La cadena de selector.</td>
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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Resultado del selector de consultas.</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelectorAll
Se ejecuta `querySelectorAll` en un nodo determinado.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo sobre el que se realizará la consulta.</td>
        </tr>
        <tr>
            <td>lector</td>
            <td><code class="flyout">string</code></td>
            <td>La cadena de selector.</td>
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
            <td>nodeIds</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Resultados del selector de consultas.</td>
        </tr>
    </tbody>
</table>
</p>

---

### requestNode
Solicita que se envíe al autor de la llamada el nodo con el identificador de objeto remoto dado. Todos los nodos que forman la ruta de acceso del nodo a la raíz también se envían al cliente como una serie de `setChildNodes` notificaciones. devuelve 0 si el cliente no ha solicitado previamente el documento que contiene el nodo solicitado.

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
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>Identificador de objeto de JavaScript para convertir en nodo.</td>
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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo para el objeto dado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### resolveNode
Resuelve el objeto de nodo de JavaScript para un NodeId o BackendNodeId determinado.

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
            <td>nodeId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que se va a resolver.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>opcional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificador del nodo back-end del nodo que se va a resolver.</td>
        </tr>
        <tr>
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de grupo simbólico que se puede usar para liberar varios objetos.</td>
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
            <td>objeto</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Contenedor de objeto de JavaScript para el nodo determinado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setInspectedNode
<span><b>Montaje. </b></span>Permite a la consola referirse al nodo inspeccionado anterior con el identificador dado a través de $0-$ 4.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador de nodo DOM al que se puede acceder mediante $0-$ 4 en la API de línea de comandos.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### setChildNodes
Se desencadena cuando el servidor desea proporcionar al cliente una estructura DOM que falta. Esto sucede en la mayoría de las llamadas que solicitan nodeIds

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
            <td>parentId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Nodo principal para poplate con elementos secundarios.</td>
        </tr>
        <tr>
            <td>node</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Matriz de nodos secundarios.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeModified
Se desencadena cuando el `Element` atributo de se modifica.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que ha cambiado.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre del atributo.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor de atributo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeRemoved
Se desencadena cuando `Element` se quita el atributo de.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que ha cambiado.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre del atributo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### characterDataModified
`DOMCharacterDataModified`Evento Mirror.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que ha cambiado.</td>
        </tr>
        <tr>
            <td>charcterData</td>
            <td><code class="flyout">string</code></td>
            <td>Nuevo valor de texto.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeInserted
`DOMNodeInserted`Evento Mirror.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que ha cambiado.</td>
        </tr>
        <tr>
            <td>previousNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del elemento anterior del mismo nivel del nodo insertado.</td>
        </tr>
        <tr>
            <td>nodo</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Datos de nodo insertados.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeRemoved
`DOMNodeRemoved`Evento Mirror.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que ha cambiado.</td>
        </tr>
        <tr>
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo que se ha quitado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### documentUpdated
Se activa cuando se `Document` ha actualizado totalmente. Los identificadores de nodo ya no son válidos.

</p>

---

## Tipos

### <a name="rgba"></a> RGBA `object`

Estructura que contiene un color RGBA.

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
            <td>d</td>
            <td><code class="flyout">integer</code></td>
            <td>El componente rojo, en el rango de [0-255].</td>
        </tr>
        <tr>
            <td>cuentas</td>
            <td><code class="flyout">integer</code></td>
            <td>El componente verde, en el rango de [0-255].</td>
        </tr>
        <tr>
            <td>letra</td>
            <td><code class="flyout">integer</code></td>
            <td>El componente azul, en el rango [0-255].</td>
        </tr>
        <tr>
            <td>a <br/> <i>opcional</i></td>
            <td><code class="flyout">number</code></td>
            <td>El componente alfa, en el rango de [0-1]. El valor predeterminado es 1.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> HighlightConfig `object`

Datos de configuración para resaltar los elementos de la página.

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
            <td>contentColor <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Color de relleno de resaltado del cuadro de contenido. El valor predeterminado es transparente.</td>
        </tr>
        <tr>
            <td>paddingColor <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Color de relleno resaltado de relleno. El valor predeterminado es transparente.</td>
        </tr>
        <tr>
            <td>ColorDeLosBordes <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Color de relleno de resaltado de borde. El valor predeterminado es transparente.</td>
        </tr>
        <tr>
            <td>marginColor <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Color de relleno de resaltado de margen. El valor predeterminado es transparente.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> NodeId `integer`

Identificador de nodo DOM único

</p>

---

### <a name="node"></a> Nodo `object`

Objeto Mirror que representa los nodos DOM reales.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador de nodo usado para hacer referencia a este nodo. El back-end desencadenará eventos de DOM para los nodos que tengan un nodeId conocido por el cliente.</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador de nodo del nodo principal, si existe.</td>
        </tr>
        <tr>
            <td>backendNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador del nodo back-end del nodo. BackendNodeIds los nodos de referencia que pueden ser conocidos para el cliente, pero no insertan eventos DOM sobre este nodo.</td>
        </tr>
        <tr>
            <td>Nodo</td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`nodeType de la.</td>
        </tr>
        <tr>
            <td>nombreDeNodo</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`nodeName de.</td>
        </tr>
        <tr>
            <td>Local</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`localName de</td>
        </tr>
        <tr>
            <td>nodeValue</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`nodeValue de la</td>
        </tr>
        <tr>
            <td>childNodeCount <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Recuento secundario de los `Container` nodos.</td>
        </tr>
        <tr>
            <td>niños <br/> <i>opcional</i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Nodos secundarios de este nodo cuando se solicitan con elementos secundarios.</td>
        </tr>
        <tr>
            <td>atributos <br/> <i>opcional</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Atributos de `Element` los nodos en el formulario de una matriz plana ' [nombre1, valor1, nombre2, valor2]</td>
        </tr>
        <tr>
            <td>documentURL <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL del documento a la que los `Document` nodos apuntan.</td>
        </tr>
        <tr>
            <td>baseURL <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL del documento que `Document` usan los nodos para la finalización de la dirección URL.</td>
        </tr>
        <tr>
            <td>publicId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` PublicId del nodo.</td>
        </tr>
        <tr>
            <td>systemId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` SystemId del nodo.</td>
        </tr>
        <tr>
            <td>internalSubset <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` InternalSubset del nodo.</td>
        </tr>
        <tr>
            <td>xmlVersion <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` Versión XML del nodo en el caso de documentos XML.</td>
        </tr>
        <tr>
            <td>name <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Nombre del nodo.</td>
        </tr>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Valor del nodo.</td>
        </tr>
        <tr>
            <td>frameId <br/> <i>opcional</i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td>IDENTIFICADOR del fotograma de los elementos de propietario del marco.</td>
        </tr>
        <tr>
            <td>contentDocument <br/> <i>opcional</i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Documento de contenido de los elementos de propietario del marco.</td>
        </tr>
        <tr>
            <td>isSVG <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si el nodo es SVG.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> BackendNodeId `integer`

Identificador de nodo DOM único que se usa para hacer referencia a un nodo que es posible que no se haya insertado en el front-end.

</p>

---

### <a name="pseudotype"></a> PseudoType `string`

Tipo de seudoelemento.

##### Valores permitidos
selección de la primera línea, primera letra, antes, después y selección
</p>

---

## Dependencias

[Motores](runtime.md)