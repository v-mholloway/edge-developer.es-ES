---
description: Referencia del protocolo DevTools versión 0.1 (EdgeHTML) para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: 'Dominio de esquema: protocolo DevTools versión 0.1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398864"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="3be2a-104">Dominio de esquema: protocolo DevTools versión 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="3be2a-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="3be2a-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3be2a-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="3be2a-106">Clasificación</span><span class="sxs-lookup"><span data-stu-id="3be2a-106">Classification</span></span> | <span data-ttu-id="3be2a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3be2a-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="3be2a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3be2a-108">Methods</span></span>](#methods) | [<span data-ttu-id="3be2a-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="3be2a-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="3be2a-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="3be2a-110">Types</span></span>](#types) | [<span data-ttu-id="3be2a-111">Dominio</span><span class="sxs-lookup"><span data-stu-id="3be2a-111">Domain</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="3be2a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3be2a-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="3be2a-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="3be2a-113">getDomains</span></span>  

<span data-ttu-id="3be2a-114">Devuelve dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="3be2a-114">Returns supported domains.</span></span>  

| <span data-ttu-id="3be2a-115">Devuelve</span><span class="sxs-lookup"><span data-stu-id="3be2a-115">Returns</span></span> | <span data-ttu-id="3be2a-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="3be2a-116">Type</span></span> | <span data-ttu-id="3be2a-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="3be2a-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="3be2a-118">dominios</span><span class="sxs-lookup"><span data-stu-id="3be2a-118">domains</span></span> | [<span data-ttu-id="3be2a-119">Dominio[]</span><span class="sxs-lookup"><span data-stu-id="3be2a-119">Domain[]</span></span>](#domain) | <span data-ttu-id="3be2a-120">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="3be2a-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="3be2a-121">Tipos</span><span class="sxs-lookup"><span data-stu-id="3be2a-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="3be2a-122">Domain (objeto)</span><span class="sxs-lookup"><span data-stu-id="3be2a-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="3be2a-123">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3be2a-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="3be2a-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3be2a-124">Properties</span></span> | <span data-ttu-id="3be2a-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="3be2a-125">Type</span></span> | <span data-ttu-id="3be2a-126">Detalles</span><span class="sxs-lookup"><span data-stu-id="3be2a-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="3be2a-127">name</span><span class="sxs-lookup"><span data-stu-id="3be2a-127">name</span></span> | `string` | <span data-ttu-id="3be2a-128">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="3be2a-128">Domain name.</span></span> |  
| <span data-ttu-id="3be2a-129">version</span><span class="sxs-lookup"><span data-stu-id="3be2a-129">version</span></span> | `string` | <span data-ttu-id="3be2a-130">Versión de dominio.</span><span class="sxs-lookup"><span data-stu-id="3be2a-130">Domain version.</span></span> |  

---  
