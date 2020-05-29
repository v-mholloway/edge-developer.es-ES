---
description: Referencia del dominio DOMDebugger. La depuración DOM permite establecer puntos de interrupción en determinadas operaciones de DOM y eventos. La ejecución de JavaScript se detendrá en estas operaciones como si se hubiera establecido un punto de interrupción común.
title: 'DOMDebugger Domain: DevTools Protocol versión 0,2'
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573734"
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
