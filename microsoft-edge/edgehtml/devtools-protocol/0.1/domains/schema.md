---
description: DevTools Protocol versión 0,1 (EdgeHTML) Reference para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: Dominio de esquema-DevTools Protocol versión 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7b4ec71b7799ae099c673bd81fa5b15a8ddd5d27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236346"
---
# <span data-ttu-id="3c9ab-104">Dominio de esquema-DevTools Protocol versión 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="3c9ab-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="3c9ab-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3c9ab-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="3c9ab-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c9ab-106">Methods</span></span>**](#methods) | [<span data-ttu-id="3c9ab-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="3c9ab-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="3c9ab-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="3c9ab-108">Types</span></span>**](#types) | [<span data-ttu-id="3c9ab-109">Dominio</span><span class="sxs-lookup"><span data-stu-id="3c9ab-109">Domain</span></span>](#domain) |
## <span data-ttu-id="3c9ab-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c9ab-110">Methods</span></span>

### <span data-ttu-id="3c9ab-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="3c9ab-111">getDomains</span></span>
<span data-ttu-id="3c9ab-112">Devuelve los dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="3c9ab-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="3c9ab-113">Devuelve</span><span class="sxs-lookup"><span data-stu-id="3c9ab-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="3c9ab-114">Confíe</span><span class="sxs-lookup"><span data-stu-id="3c9ab-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="3c9ab-115">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="3c9ab-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="3c9ab-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="3c9ab-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="3c9ab-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="3c9ab-117">Domain</span></span> `object`

<span data-ttu-id="3c9ab-118">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3c9ab-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="3c9ab-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c9ab-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="3c9ab-120">name</span><span class="sxs-lookup"><span data-stu-id="3c9ab-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="3c9ab-121">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="3c9ab-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="3c9ab-122">version</span><span class="sxs-lookup"><span data-stu-id="3c9ab-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="3c9ab-123">Versión del dominio.</span><span class="sxs-lookup"><span data-stu-id="3c9ab-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
