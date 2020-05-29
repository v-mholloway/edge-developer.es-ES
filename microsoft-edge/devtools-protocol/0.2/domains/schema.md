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
# <span data-ttu-id="b1884-104">Esquema</span><span class="sxs-lookup"><span data-stu-id="b1884-104">Schema</span></span>
<span data-ttu-id="b1884-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="b1884-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="b1884-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1884-106">Methods</span></span>**](#methods) | [<span data-ttu-id="b1884-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="b1884-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="b1884-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="b1884-108">Types</span></span>**](#types) | [<span data-ttu-id="b1884-109">Dominio</span><span class="sxs-lookup"><span data-stu-id="b1884-109">Domain</span></span>](#domain) |
## <span data-ttu-id="b1884-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1884-110">Methods</span></span>

### <span data-ttu-id="b1884-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="b1884-111">getDomains</span></span>
<span data-ttu-id="b1884-112">Devuelve los dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="b1884-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b1884-113">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b1884-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b1884-114">Confíe</span><span class="sxs-lookup"><span data-stu-id="b1884-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="b1884-115">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="b1884-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="b1884-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="b1884-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="b1884-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="b1884-117">Domain</span></span> `object`

<span data-ttu-id="b1884-118">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="b1884-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b1884-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1884-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b1884-120">name</span><span class="sxs-lookup"><span data-stu-id="b1884-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b1884-121">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="b1884-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b1884-122">version</span><span class="sxs-lookup"><span data-stu-id="b1884-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b1884-123">Versión del dominio.</span><span class="sxs-lookup"><span data-stu-id="b1884-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
