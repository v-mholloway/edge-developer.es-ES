---
description: DevTools Protocol versión 0,2 (EdgeHTML) Reference para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: Dominio de esquema-DevTools Protocol versión 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 53038a02844fafc9550a6ac26303620a1a0183f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235958"
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
