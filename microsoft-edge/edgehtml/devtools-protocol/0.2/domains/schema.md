---
description: Referencia del protocolo DevTools versión 0.2 (EdgeHTML) para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: 'Dominio de esquema: protocolo DevTools versión 0.2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398150"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="a3512-104">Dominio de esquema: protocolo DevTools versión 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a3512-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="a3512-105">Proporciona información sobre el esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="a3512-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="a3512-106">Clasificación</span><span class="sxs-lookup"><span data-stu-id="a3512-106">Classification</span></span> | <span data-ttu-id="a3512-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3512-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="a3512-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a3512-108">Methods</span></span>](#methods) | [<span data-ttu-id="a3512-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="a3512-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="a3512-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="a3512-110">Types</span></span>](#types) | [<span data-ttu-id="a3512-111">Domain (objeto)</span><span class="sxs-lookup"><span data-stu-id="a3512-111">Domain object</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="a3512-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a3512-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="a3512-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="a3512-113">getDomains</span></span>  

<span data-ttu-id="a3512-114">Devuelve dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="a3512-114">Returns supported domains.</span></span>  

| <span data-ttu-id="a3512-115">Devuelve</span><span class="sxs-lookup"><span data-stu-id="a3512-115">Returns</span></span> | <span data-ttu-id="a3512-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3512-116">Type</span></span> | <span data-ttu-id="a3512-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="a3512-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a3512-118">dominios</span><span class="sxs-lookup"><span data-stu-id="a3512-118">domains</span></span> | [<span data-ttu-id="a3512-119">Dominio[]</span><span class="sxs-lookup"><span data-stu-id="a3512-119">Domain[]</span></span>](#domain) | <span data-ttu-id="a3512-120">Lista de dominios admitidos.</span><span class="sxs-lookup"><span data-stu-id="a3512-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="a3512-121">Tipos</span><span class="sxs-lookup"><span data-stu-id="a3512-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="a3512-122">Domain (objeto)</span><span class="sxs-lookup"><span data-stu-id="a3512-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="a3512-123">Descripción del dominio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="a3512-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="a3512-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3512-124">Properties</span></span> | <span data-ttu-id="a3512-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3512-125">Type</span></span> | <span data-ttu-id="a3512-126">Detalles</span><span class="sxs-lookup"><span data-stu-id="a3512-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a3512-127">name</span><span class="sxs-lookup"><span data-stu-id="a3512-127">name</span></span> | `string` | <span data-ttu-id="a3512-128">Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="a3512-128">Domain name.</span></span> |  
| <span data-ttu-id="a3512-129">version</span><span class="sxs-lookup"><span data-stu-id="a3512-129">version</span></span> | `string` | <span data-ttu-id="a3512-130">Versión de dominio.</span><span class="sxs-lookup"><span data-stu-id="a3512-130">Domain version.</span></span> |  

---  
