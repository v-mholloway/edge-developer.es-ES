---
description: Referencia del dominio de la página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.
title: 'Dominio de la página: Protocolo de DevTools versión 0,1'
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573759"
---
# <span data-ttu-id="eff06-104">Página</span><span class="sxs-lookup"><span data-stu-id="eff06-104">Page</span></span>
<span data-ttu-id="eff06-105">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de la página.</span><span class="sxs-lookup"><span data-stu-id="eff06-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="eff06-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="eff06-106">Methods</span></span>**](#methods) | <span data-ttu-id="eff06-107">[Habilitar](#enable), [deshabilitar](#disable), [navegar](#navigate)</span><span class="sxs-lookup"><span data-stu-id="eff06-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="eff06-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="eff06-108">Types</span></span>**](#types) | [<span data-ttu-id="eff06-109">FrameId</span><span class="sxs-lookup"><span data-stu-id="eff06-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="eff06-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="eff06-110">Methods</span></span>

### <span data-ttu-id="eff06-111">habilitar</span><span class="sxs-lookup"><span data-stu-id="eff06-111">enable</span></span>
<span data-ttu-id="eff06-112">Habilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="eff06-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="eff06-113">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="eff06-113">disable</span></span>
<span data-ttu-id="eff06-114">Deshabilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="eff06-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="eff06-115">navegar</span><span class="sxs-lookup"><span data-stu-id="eff06-115">navigate</span></span>
<span data-ttu-id="eff06-116">Desplaza la página actual a la dirección URL dada.</span><span class="sxs-lookup"><span data-stu-id="eff06-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="eff06-117">Parameters</span><span class="sxs-lookup"><span data-stu-id="eff06-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="eff06-118">url</span><span class="sxs-lookup"><span data-stu-id="eff06-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="eff06-119">Dirección URL para navegar por la página.</span><span class="sxs-lookup"><span data-stu-id="eff06-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="eff06-120">Devuelve</span><span class="sxs-lookup"><span data-stu-id="eff06-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="eff06-121">frameId</span><span class="sxs-lookup"><span data-stu-id="eff06-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="eff06-122">Montaje.</span><span class="sxs-lookup"><span data-stu-id="eff06-122">Experimental.</span></span> </b></span><span data-ttu-id="eff06-123">Identificador del fotograma en el que se va a navegar.</span><span class="sxs-lookup"><span data-stu-id="eff06-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="eff06-124">Tipos</span><span class="sxs-lookup"><span data-stu-id="eff06-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="eff06-125">FrameId</span><span class="sxs-lookup"><span data-stu-id="eff06-125">FrameId</span></span> `string`

<span data-ttu-id="eff06-126">Identificador de trama único.</span><span class="sxs-lookup"><span data-stu-id="eff06-126">Unique frame identifier.</span></span>


---
