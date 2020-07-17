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
# <span data-ttu-id="620f0-104">Dominio de esquema-DevTools Protocol versión 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="620f0-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="620f0-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="620f0-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="620f0-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="620f0-106">Methods</span></span>**](#methods) | [<span data-ttu-id="620f0-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="620f0-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="620f0-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="620f0-108">Types</span></span>**](#types) | [<span data-ttu-id="620f0-109">Dominio</span><span class="sxs-lookup"><span data-stu-id="620f0-109">Domain</span></span>](#domain) |
## <span data-ttu-id="620f0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="620f0-110">Methods</span></span>

### <span data-ttu-id="620f0-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="620f0-111">getDomains</span></span>
<span data-ttu-id="620f0-112">Devuelve los dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="620f0-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="620f0-113">Devuelve</span><span class="sxs-lookup"><span data-stu-id="620f0-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="620f0-114">Confíe</span><span class="sxs-lookup"><span data-stu-id="620f0-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="620f0-115">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="620f0-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="620f0-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="620f0-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="620f0-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="620f0-117">Domain</span></span> `object`

<span data-ttu-id="620f0-118">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="620f0-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="620f0-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="620f0-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="620f0-120">name</span><span class="sxs-lookup"><span data-stu-id="620f0-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="620f0-121">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="620f0-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="620f0-122">version</span><span class="sxs-lookup"><span data-stu-id="620f0-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="620f0-123">Versión del dominio.</span><span class="sxs-lookup"><span data-stu-id="620f0-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
