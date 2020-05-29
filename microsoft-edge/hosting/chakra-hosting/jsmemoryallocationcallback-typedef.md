---
description: Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573423"
---
# <span data-ttu-id="d34d8-103">JsMemoryAllocationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="d34d8-103">JsMemoryAllocationCallback Typedef</span></span>
<span data-ttu-id="d34d8-104">Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="d34d8-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="d34d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d34d8-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="d34d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d34d8-106">Parameters</span></span>  
 <span data-ttu-id="d34d8-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="d34d8-107">callbackState</span></span>  
 <span data-ttu-id="d34d8-108">El estado pasado a JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="d34d8-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="d34d8-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="d34d8-109">allocationEvent</span></span>  
 <span data-ttu-id="d34d8-110">Tipo de evento de asignación de tipo.</span><span class="sxs-lookup"><span data-stu-id="d34d8-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="d34d8-111">allocate</span><span class="sxs-lookup"><span data-stu-id="d34d8-111">allocationSize</span></span>  
 <span data-ttu-id="d34d8-112">El tamaño de la asignación.</span><span class="sxs-lookup"><span data-stu-id="d34d8-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="d34d8-113">Valor de propiedad y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d34d8-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="d34d8-114">Para el evento JsMemoryAllocate, devolver true permite que el motor en tiempo de ejecución continúe con la asignación.</span><span class="sxs-lookup"><span data-stu-id="d34d8-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="d34d8-115">Si devuelve falso, significa que se rechaza la solicitud de asignación.</span><span class="sxs-lookup"><span data-stu-id="d34d8-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="d34d8-116">El valor devuelto se omite para otros eventos de asignación.</span><span class="sxs-lookup"><span data-stu-id="d34d8-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="d34d8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d34d8-117">Remarks</span></span>  
 <span data-ttu-id="d34d8-118">Usa JsSetRuntimeMemoryAllocationCallback para registrar esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d34d8-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="d34d8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d34d8-119">Requirements</span></span>  
 <span data-ttu-id="d34d8-120">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d34d8-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d34d8-121">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d34d8-121">See Also</span></span>  
 [<span data-ttu-id="d34d8-122">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d34d8-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)