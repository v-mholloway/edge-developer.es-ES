---
description: Referencia para el dominio de superposición. El dominio de superposición expone elementos visuales y la interacción de selección de nodos
title: Dominio de superposición-protocolo de DevTools versión 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235962"
---
# Overlay

El dominio de superposición expone elementos visuales y la interacción de selección de nodos

| | |
|-|-|
| [**Métodos**](#methods) | [Habilitar](#enable), [deshabilitar](#disable), [setInspectMode](#setinspectmode) |
| [**Eventos**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
| [**Dependencias**](#dependencies) | [DOM](dom.md) |
## Métodos

### habilitar
Permite la creación de informes <code>nodeHighlightRequested</code> y <code>inspectElementRequested</code> eventos

</p>

---

### deshabilitar 
Deshabilita los informes de eventos de dominio de superposición

</p>

---

### setInspectMode
Establece el modo de selección de elementos para el cliente.

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
            <td>mode</td>
            <td><code class="flyout">string</code></td>
            <td>El modo de inspección.  Los valores válidos son ' searchForNode ' y ' none '.</td>
        </tr>
        <tr>
            <td>highlightConfig <br/> <i>opcional</i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td>La configuración de resaltado que se usará durante la inspección</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### inspectNodeRequested
Notifica al cliente que el usuario ha solicitado inspeccionar un nodo determinado

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
            <td>backendNodeId</td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td>El identificador del nodo back-end del nodo solicitado</td>
        </tr>
    </tbody>
</table>
</p>

---

### nodeHighlightRequested
Indica que el usuario ha activado el nodo y puede inspeccionar el nodo

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
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td>El identificador de nodo del nodo que se está considerando</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dependencias

[DOM](dom.md)
