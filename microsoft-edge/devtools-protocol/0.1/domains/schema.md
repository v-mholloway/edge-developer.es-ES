---
description: Referencia para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: Dominio de esquema-DevTools Protocol versión 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 83d7019d18ccce1c81b67aafdcafe1a8566694ea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573753"
---
# <span data-ttu-id="43f23-104">Esquema</span><span class="sxs-lookup"><span data-stu-id="43f23-104">Schema</span></span>
<span data-ttu-id="43f23-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="43f23-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="43f23-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="43f23-106">Methods</span></span>**](#methods) | [<span data-ttu-id="43f23-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="43f23-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="43f23-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="43f23-108">Types</span></span>**](#types) | [<span data-ttu-id="43f23-109">Dominio</span><span class="sxs-lookup"><span data-stu-id="43f23-109">Domain</span></span>](#domain) |
## <span data-ttu-id="43f23-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="43f23-110">Methods</span></span>

### <span data-ttu-id="43f23-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="43f23-111">getDomains</span></span>
<span data-ttu-id="43f23-112">Devuelve los dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="43f23-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="43f23-113">Devuelve</span><span class="sxs-lookup"><span data-stu-id="43f23-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="43f23-114">Confíe</span><span class="sxs-lookup"><span data-stu-id="43f23-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="43f23-115">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="43f23-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="43f23-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="43f23-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="43f23-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="43f23-117">Domain</span></span> `object`

<span data-ttu-id="43f23-118">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="43f23-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="43f23-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43f23-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="43f23-120">name</span><span class="sxs-lookup"><span data-stu-id="43f23-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="43f23-121">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="43f23-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="43f23-122">version</span><span class="sxs-lookup"><span data-stu-id="43f23-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="43f23-123">Versión del dominio.</span><span class="sxs-lookup"><span data-stu-id="43f23-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
