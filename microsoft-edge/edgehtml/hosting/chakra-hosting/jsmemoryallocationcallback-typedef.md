---
description: Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236078"
---
# <span data-ttu-id="13cbb-103">Definición de tipo JsMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="13cbb-103">JsMemoryAllocationCallback Typedef</span></span>

<span data-ttu-id="13cbb-104">Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="13cbb-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="13cbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13cbb-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="13cbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13cbb-106">Parameters</span></span>  
 <span data-ttu-id="13cbb-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="13cbb-107">callbackState</span></span>  
 <span data-ttu-id="13cbb-108">El estado pasado a JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="13cbb-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="13cbb-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="13cbb-109">allocationEvent</span></span>  
 <span data-ttu-id="13cbb-110">Tipo de evento de asignación de tipo.</span><span class="sxs-lookup"><span data-stu-id="13cbb-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="13cbb-111">allocate</span><span class="sxs-lookup"><span data-stu-id="13cbb-111">allocationSize</span></span>  
 <span data-ttu-id="13cbb-112">El tamaño de la asignación.</span><span class="sxs-lookup"><span data-stu-id="13cbb-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="13cbb-113">Valor de propiedad y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13cbb-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="13cbb-114">Para el evento JsMemoryAllocate, devolver true permite que el motor en tiempo de ejecución continúe con la asignación.</span><span class="sxs-lookup"><span data-stu-id="13cbb-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="13cbb-115">Si devuelve falso, significa que se rechaza la solicitud de asignación.</span><span class="sxs-lookup"><span data-stu-id="13cbb-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="13cbb-116">El valor devuelto se omite para otros eventos de asignación.</span><span class="sxs-lookup"><span data-stu-id="13cbb-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="13cbb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13cbb-117">Remarks</span></span>  
 <span data-ttu-id="13cbb-118">Usa JsSetRuntimeMemoryAllocationCallback para registrar esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="13cbb-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="13cbb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13cbb-119">Requirements</span></span>  
 <span data-ttu-id="13cbb-120">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="13cbb-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="13cbb-121">Consulta también</span><span class="sxs-lookup"><span data-stu-id="13cbb-121">See Also</span></span>  
 [<span data-ttu-id="13cbb-122">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="13cbb-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
