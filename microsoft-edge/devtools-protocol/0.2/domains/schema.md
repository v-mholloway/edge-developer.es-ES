---
description: Referencia para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: Dominio de esquema-DevTools Protocol versión 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: d0fbe9cde742d255797a2460b940732ffa5b8f27
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882880"
---
# Dominio de esquema-DevTools Protocol versión 0,2 (EdgeHTML)  

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
