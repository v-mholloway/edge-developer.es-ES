---
description: Referencia para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: Dominio de esquema-DevTools Protocol versión 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: df86e6669956c14b7c905514fc44376f71eaa993
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573728"
---
# Esquema
Proporciona información sobre el esquema de protocolo.

| | |
|-|-|
| [**Métodos**](#methods) | [getDomains](#getdomains) |
| [**Tipos**](#types) | [Dominio](#domain) |
## Métodos

### getDomains
Devuelve los dominios admitidos.

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
            <td>Confíe</td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td>Lista de dominios admitidos.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="domain"></a> Dominio `object`

Descripción del dominio de protocolo.

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
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de dominio.</td>
        </tr>
        <tr>
            <td>version</td>
            <td><code class="flyout">string</code></td>
            <td>Versión del dominio.</td>
        </tr>
    </tbody>
</table>
</p>

---
