---
description: Establece el límite de memoria actual para un tiempo de ejecución.
title: Función JsSetRuntimeMemoryLimit | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1c31d8bbbec4be22fc1af09e546ad4c95f8ec2bd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235888"
---
# <span data-ttu-id="87ba0-103">Función JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="87ba0-103">JsSetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="87ba0-104">Establece el límite de memoria actual para un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="87ba0-104">Sets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="87ba0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87ba0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### <span data-ttu-id="87ba0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87ba0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="87ba0-107">Tiempo de ejecución cuyo límite de memoria se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="87ba0-107">The runtime whose memory limit is to be set.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="87ba0-108">El nuevo límite de memoria en tiempo de ejecución, en bytes, o-1 para sin límite de memoria.</span><span class="sxs-lookup"><span data-stu-id="87ba0-108">The new runtime memory limit, in bytes, or -1 for no memory limit.</span></span>  
  
## <span data-ttu-id="87ba0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87ba0-109">Return Value</span></span>  
 <span data-ttu-id="87ba0-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="87ba0-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="87ba0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87ba0-111">Remarks</span></span>  
 <span data-ttu-id="87ba0-112">Un límite de memoria hará que cualquier operación que supere el límite falle con un error de "memoria insuficiente".</span><span class="sxs-lookup"><span data-stu-id="87ba0-112">A memory limit will cause any operation which exceeds the limit to fail with an "out of memory" error.</span></span> <span data-ttu-id="87ba0-113">Establecer el límite de memoria de un tiempo de ejecución en-1 significa que el motor en tiempo de ejecución no tiene límite de memoria.</span><span class="sxs-lookup"><span data-stu-id="87ba0-113">Setting a runtime's memory limit to -1 means that the runtime has no memory limit.</span></span> <span data-ttu-id="87ba0-114">Los nuevos runtimes tienen como valor predeterminado un límite de memoria.</span><span class="sxs-lookup"><span data-stu-id="87ba0-114">New runtimes default to having no memory limit.</span></span> <span data-ttu-id="87ba0-115">Si el nuevo límite de memoria supera el uso actual, la llamada se realizará correctamente y cualquier asignación futura en este Runtime producirá un error hasta que el uso de memoria del Runtime descienda por debajo del límite.</span><span class="sxs-lookup"><span data-stu-id="87ba0-115">If the new memory limit exceeds current usage, the call will succeed and any future allocations in this runtime will fail until the runtime's memory usage drops below the limit.</span></span>  
  
 <span data-ttu-id="87ba0-116">El límite de memoria de un motor en tiempo de ejecución se puede establecer siempre, independientemente de si el motor en tiempo de ejecución está activo o no en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="87ba0-116">A runtime's memory limit can be always be set, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="87ba0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ba0-117">Requirements</span></span>  
 <span data-ttu-id="87ba0-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="87ba0-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="87ba0-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="87ba0-119">See Also</span></span>  
 [<span data-ttu-id="87ba0-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="87ba0-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
