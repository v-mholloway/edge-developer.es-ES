---
description: Tipo de evento de devolución de llamada de asignación.
title: JsMemoryEventType (enumeración) | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a28010f908285098cf652b497b6d6c272bc763fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235887"
---
# <span data-ttu-id="083ba-103">Enumeración JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="083ba-103">JsMemoryEventType Enumeration</span></span>

<span data-ttu-id="083ba-104">Tipo de evento de devolución de llamada de asignación.</span><span class="sxs-lookup"><span data-stu-id="083ba-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="083ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="083ba-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="083ba-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="083ba-106">Members</span></span>  
  
### <span data-ttu-id="083ba-107">Los</span><span class="sxs-lookup"><span data-stu-id="083ba-107">Values</span></span>  
  
|<span data-ttu-id="083ba-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="083ba-108">Name</span></span>|<span data-ttu-id="083ba-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="083ba-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="083ba-110">Indica una solicitud de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="083ba-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="083ba-111">Indica un evento de asignación con error.</span><span class="sxs-lookup"><span data-stu-id="083ba-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="083ba-112">Indica un evento de liberación de memoria.</span><span class="sxs-lookup"><span data-stu-id="083ba-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="083ba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="083ba-113">Requirements</span></span>  
 <span data-ttu-id="083ba-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="083ba-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="083ba-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="083ba-115">See Also</span></span>  
 [<span data-ttu-id="083ba-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="083ba-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
