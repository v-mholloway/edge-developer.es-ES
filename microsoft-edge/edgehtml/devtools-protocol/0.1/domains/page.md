---
description: DevTools Protocol versión 0,1 (EdgeHTML) Reference para el dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: DevTools Protocol versión 0,1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236353"
---
# <span data-ttu-id="b523d-104">Dominio de la página: DevTools Protocol versión 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="b523d-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="b523d-105">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.</span><span class="sxs-lookup"><span data-stu-id="b523d-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="b523d-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="b523d-106">Methods</span></span>**](#methods) | <span data-ttu-id="b523d-107">[Habilitar](#enable), [deshabilitar](#disable), [navegar](#navigate)</span><span class="sxs-lookup"><span data-stu-id="b523d-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="b523d-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="b523d-108">Types</span></span>**](#types) | [<span data-ttu-id="b523d-109">FrameId</span><span class="sxs-lookup"><span data-stu-id="b523d-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="b523d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b523d-110">Methods</span></span>

### <span data-ttu-id="b523d-111">habilitar</span><span class="sxs-lookup"><span data-stu-id="b523d-111">enable</span></span>
<span data-ttu-id="b523d-112">Habilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="b523d-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="b523d-113">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="b523d-113">disable</span></span>
<span data-ttu-id="b523d-114">Deshabilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="b523d-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="b523d-115">navegar</span><span class="sxs-lookup"><span data-stu-id="b523d-115">navigate</span></span>
<span data-ttu-id="b523d-116">Desplaza la página actual a la dirección URL dada.</span><span class="sxs-lookup"><span data-stu-id="b523d-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b523d-117">Parameters</span><span class="sxs-lookup"><span data-stu-id="b523d-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b523d-118">url</span><span class="sxs-lookup"><span data-stu-id="b523d-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b523d-119">Dirección URL para navegar por la página.</span><span class="sxs-lookup"><span data-stu-id="b523d-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b523d-120">Devuelve</span><span class="sxs-lookup"><span data-stu-id="b523d-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b523d-121">frameId</span><span class="sxs-lookup"><span data-stu-id="b523d-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="b523d-122">Montaje.</span><span class="sxs-lookup"><span data-stu-id="b523d-122">Experimental.</span></span> </b></span><span data-ttu-id="b523d-123">Identificador del fotograma en el que se va a navegar.</span><span class="sxs-lookup"><span data-stu-id="b523d-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="b523d-124">Tipos</span><span class="sxs-lookup"><span data-stu-id="b523d-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="b523d-125">FrameId</span><span class="sxs-lookup"><span data-stu-id="b523d-125">FrameId</span></span> `string`

<span data-ttu-id="b523d-126">Identificador de trama único.</span><span class="sxs-lookup"><span data-stu-id="b523d-126">Unique frame identifier.</span></span>


---
