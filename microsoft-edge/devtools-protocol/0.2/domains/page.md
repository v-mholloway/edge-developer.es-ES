---
description: Referencia del dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: Protocolo de DevTools versión 0,2'
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 688cc1fcfce0b81c5eed0c858a4a60b4754c49a4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573735"
---
# Página
Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.

| | |
|-|-|
| [**Métodos**](#methods) | [Habilitar](#enable), [deshabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree) |
| [**Eventos**](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |
| [**Tipos**](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |
## Métodos

### habilitar
Habilita las notificaciones de dominio de página.

</p>

---

### deshabilitar 
Deshabilita las notificaciones de dominio de página.

</p>

---

### navegar
Desplaza la página actual a la dirección URL dada.

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
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL para navegar por la página.</td>
        </tr>
        <tr>
            <td>frameId <br/> <i>opcional</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador de trama para navegar. Si no se especifica, se desplazará por la página superior.</td>
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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador del fotograma en el que se va a navegar.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getFrameTree
Devuelve la estructura de árbol de fotogramas actual.

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
            <td>frameTree</td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td>Presentar estructura de árbol de fotogramas.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### frameAttached
Se desencadena cuando el marco se ha adjuntado a su elemento primario.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador de la trama que se ha adjuntado.</td>
        </tr>
        <tr>
            <td>parentFrameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador de marco primario.</td>
        </tr>
        <tr>
            <td>apilable <br/> <i>opcional</i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td>Seguimiento de la pila de JavaScript del momento en que se asoció el marco, establecido solo si el marco se inició desde el script.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameDetached
Se desencadena cuando se ha desvinculado el marco de su elemento primario.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador de la trama que se ha desvinculado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameNavigated
Se activa una vez que se ha completado la navegación del marco.

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
            <td>bastidor</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Objeto Frame.</td>
        </tr>
    </tbody>
</table>
</p>

---

### loadEventFired
Corresponde al evento Window. onload.

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
            <td><code class="flyout">number</code></td>
            <td>Número de milisegundos desde la época.</td>
        </tr>
    </tbody>
</table>
</p>

---

### domContentEventFired
Corresponde al evento document. onDOMContentLoaded.

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
            <td><code class="flyout">number</code></td>
            <td>Número de milisegundos desde la época.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="frameid"></a> FrameId `string`

Identificador de trama único.

</p>

---

### <a name="frame"></a> Marco `object`

Información sobre el marco de la página.

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
            <td>id</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador único de marco.</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>opcional</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador único del marco primario.</td>
        </tr>
        <tr>
            <td>name <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nombre del marco según se especifica en la etiqueta.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL del documento de marco.</td>
        </tr>
        <tr>
            <td>securityOrigin</td>
            <td><code class="flyout">string</code></td>
            <td>Origen del documento de marco.</td>
        </tr>
        <tr>
            <td>mimeType</td>
            <td><code class="flyout">string</code></td>
            <td>MIME del marco según lo determine el explorador.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> FrameTree `object`

Información sobre la jerarquía de Marcos.

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
            <td>bastidor</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Información de fotograma para este elemento de árbol.</td>
        </tr>
        <tr>
            <td>childFrames <br/> <i>opcional</i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td>Marcos secundarios.</td>
        </tr>
    </tbody>
</table>
</p>

---
