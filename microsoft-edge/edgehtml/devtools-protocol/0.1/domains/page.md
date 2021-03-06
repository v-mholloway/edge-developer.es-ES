---
description: Referencia del protocolo DevTools versión 0.1 (EdgeHTML) para el dominio de página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.
title: 'Dominio de página: protocolo DevTools versión 0.1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399151"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="3fa9f-104">Dominio de página: protocolo DevTools versión 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="3fa9f-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="3fa9f-105">Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="3fa9f-106">Clasificación</span><span class="sxs-lookup"><span data-stu-id="3fa9f-106">Classification</span></span> | <span data-ttu-id="3fa9f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fa9f-107">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="3fa9f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fa9f-108">Methods</span></span>**](#methods) | <span data-ttu-id="3fa9f-109">[enable](#enable), [disable](#disable), [navigate](#navigate)</span><span class="sxs-lookup"><span data-stu-id="3fa9f-109">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |  
| [**<span data-ttu-id="3fa9f-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="3fa9f-110">Types</span></span>**](#types) | [<span data-ttu-id="3fa9f-111">FrameId</span><span class="sxs-lookup"><span data-stu-id="3fa9f-111">FrameId</span></span>](#frameid) |  

## <a name="methods"></a><span data-ttu-id="3fa9f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fa9f-112">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="3fa9f-113">habilitar</span><span class="sxs-lookup"><span data-stu-id="3fa9f-113">enable</span></span>  

<span data-ttu-id="3fa9f-114">Habilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-114">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="3fa9f-115">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="3fa9f-115">disable</span></span>  

<span data-ttu-id="3fa9f-116">Deshabilita las notificaciones de dominio de página.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-116">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="3fa9f-117">navegar</span><span class="sxs-lookup"><span data-stu-id="3fa9f-117">navigate</span></span>  

<span data-ttu-id="3fa9f-118">Navega a la página actual a la dirección URL determinada.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-118">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="3fa9f-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="3fa9f-119">Parameters</span></span> | <span data-ttu-id="3fa9f-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fa9f-120">Type</span></span> | <span data-ttu-id="3fa9f-121">Detalles</span><span class="sxs-lookup"><span data-stu-id="3fa9f-121">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="3fa9f-122">url</span><span class="sxs-lookup"><span data-stu-id="3fa9f-122">url</span></span> | `string` | <span data-ttu-id="3fa9f-123">DIRECCIÓN URL para navegar por la página.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-123">URL to navigate the page to.</span></span> |  

| <span data-ttu-id="3fa9f-124">Devuelve</span><span class="sxs-lookup"><span data-stu-id="3fa9f-124">Returns</span></span> | <span data-ttu-id="3fa9f-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fa9f-125">Type</span></span> | <span data-ttu-id="3fa9f-126">Detalles</span><span class="sxs-lookup"><span data-stu-id="3fa9f-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="3fa9f-127">frameId</span><span class="sxs-lookup"><span data-stu-id="3fa9f-127">frameId</span></span> | [<span data-ttu-id="3fa9f-128">FrameId</span><span class="sxs-lookup"><span data-stu-id="3fa9f-128">FrameId</span></span>](#frameid) | <span data-ttu-id="3fa9f-129">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-129">**Experimental**.</span></span>  <span data-ttu-id="3fa9f-130">Identificador de fotograma que se navegará.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-130">Frame ID that will be navigated.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="3fa9f-131">Tipos</span><span class="sxs-lookup"><span data-stu-id="3fa9f-131">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="3fa9f-132">Cadena FrameId</span><span class="sxs-lookup"><span data-stu-id="3fa9f-132">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="3fa9f-133">Identificador de fotograma único.</span><span class="sxs-lookup"><span data-stu-id="3fa9f-133">Unique frame identifier.</span></span>  

&nbsp;  

---  
