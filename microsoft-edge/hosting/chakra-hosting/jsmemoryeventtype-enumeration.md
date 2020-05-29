---
description: Tipo de evento de devolución de llamada de asignación.
title: JsMemoryEventType (enumeración) | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573420"
---
# <span data-ttu-id="fb529-103">Enumeración JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="fb529-103">JsMemoryEventType Enumeration</span></span>
<span data-ttu-id="fb529-104">Tipo de evento de devolución de llamada de asignación.</span><span class="sxs-lookup"><span data-stu-id="fb529-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="fb529-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb529-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="fb529-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb529-106">Members</span></span>  
  
### <span data-ttu-id="fb529-107">Los</span><span class="sxs-lookup"><span data-stu-id="fb529-107">Values</span></span>  
  
|<span data-ttu-id="fb529-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb529-108">Name</span></span>|<span data-ttu-id="fb529-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb529-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="fb529-110">Indica una solicitud de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="fb529-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="fb529-111">Indica un evento de asignación con error.</span><span class="sxs-lookup"><span data-stu-id="fb529-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="fb529-112">Indica un evento de liberación de memoria.</span><span class="sxs-lookup"><span data-stu-id="fb529-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="fb529-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb529-113">Requirements</span></span>  
 <span data-ttu-id="fb529-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb529-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb529-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fb529-115">See Also</span></span>  
 [<span data-ttu-id="fb529-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fb529-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)