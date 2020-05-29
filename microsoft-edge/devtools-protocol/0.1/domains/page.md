---
description: Referencia del dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: Protocolo de DevTools versión 0,1'
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573759"
---
# Página
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
