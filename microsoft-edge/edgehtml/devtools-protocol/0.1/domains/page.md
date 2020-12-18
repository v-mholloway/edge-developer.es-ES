---
description: DevTools Protocol versión 0,1 (EdgeHTML) Reference para el dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: DevTools Protocol versión 0,1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236353"
---
# Dominio de la página: DevTools Protocol versión 0,1 (EdgeHTML)  

Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.

| | |
|-|-|
| [**Métodos**](#methods) | [Habilitar](#enable), [deshabilitar](#disable), [navegar](#navigate) |
| [**Tipos**](#types) | [FrameId](#frameid) |
## Métodos

### habilitar
Habilita las notificaciones de dominio de página.


---

### deshabilitar 
Deshabilita las notificaciones de dominio de página.


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
            <td><span><b>Montaje. </b></span>Identificador del fotograma en el que se va a navegar.</td>
        </tr>
    </tbody>
</table>

---

## Tipos

### <a name="frameid"></a> FrameId `string`

Identificador de trama único.


---
