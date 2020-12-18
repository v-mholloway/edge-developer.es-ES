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
# <span data-ttu-id="f7e0b-104">Dominio de esquema-DevTools Protocol versión 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f7e0b-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="f7e0b-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f7e0b-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f7e0b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7e0b-106">Methods</span></span>**](#methods) | [<span data-ttu-id="f7e0b-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="f7e0b-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="f7e0b-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="f7e0b-108">Types</span></span>**](#types) | [<span data-ttu-id="f7e0b-109">Dominio</span><span class="sxs-lookup"><span data-stu-id="f7e0b-109">Domain</span></span>](#domain) |
## <span data-ttu-id="f7e0b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7e0b-110">Methods</span></span>

### <span data-ttu-id="f7e0b-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="f7e0b-111">getDomains</span></span>
<span data-ttu-id="f7e0b-112">Devuelve los dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="f7e0b-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f7e0b-113">Devuelve</span><span class="sxs-lookup"><span data-stu-id="f7e0b-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f7e0b-114">Confíe</span><span class="sxs-lookup"><span data-stu-id="f7e0b-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="f7e0b-115">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="f7e0b-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f7e0b-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="f7e0b-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="f7e0b-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="f7e0b-117">Domain</span></span> `object`

<span data-ttu-id="f7e0b-118">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f7e0b-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f7e0b-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f7e0b-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f7e0b-120">name</span><span class="sxs-lookup"><span data-stu-id="f7e0b-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f7e0b-121">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="f7e0b-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f7e0b-122">version</span><span class="sxs-lookup"><span data-stu-id="f7e0b-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f7e0b-123">Versión del dominio.</span><span class="sxs-lookup"><span data-stu-id="f7e0b-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
