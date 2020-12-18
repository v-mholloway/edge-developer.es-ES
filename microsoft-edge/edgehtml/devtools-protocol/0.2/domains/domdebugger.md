---
description: Referencia del dominio DOMDebugger. La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos. La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.
title: 'DOMDebugger Domain: DevTools Protocol versión 0,2'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235964"
---
# DOMDebugger

La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos. La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.

| | |
|-|-|
| [**Métodos**](#methods) | [setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint) |
## Métodos

### setInstrumentationBreakpoint
<span><b>Montaje. </b></span>Establece un punto de interrupción en un evento nativo determinado.

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
            <td>nombreDeEvento</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la instrumentación que se va a detener. Valores válidos: ' scriptFirstStatement '.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeInstrumentationBreakpoint
<span><b>Montaje. </b></span>Quita un punto de interrupción de un evento nativo en particular.

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
            <td>nombreDeEvento</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la instrumentación que se va a detener. Valores válidos: ' scriptFirstStatement '.</td>
        </tr>
    </tbody>
</table>
</p>

---
