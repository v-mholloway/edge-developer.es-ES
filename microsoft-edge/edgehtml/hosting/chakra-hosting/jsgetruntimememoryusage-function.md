---
description: Obtiene el uso de memoria actual para un Runtime.
title: Función JsGetRuntimeMemoryUsage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a9c8d59e8cf73ad178f539f2f9f0ed191ceb47fd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236651"
---
# <span data-ttu-id="c1b09-103">Función JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="c1b09-103">JsGetRuntimeMemoryUsage Function</span></span>

<span data-ttu-id="c1b09-104">Obtiene el uso de memoria actual para un Runtime.</span><span class="sxs-lookup"><span data-stu-id="c1b09-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="c1b09-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1b09-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="c1b09-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1b09-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="c1b09-107">Motor en tiempo de ejecución cuyo uso de memoria se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c1b09-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="c1b09-108">Uso de memoria actual del motor en tiempo de ejecución, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c1b09-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="c1b09-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1b09-109">Return Value</span></span>  
 <span data-ttu-id="c1b09-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c1b09-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c1b09-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1b09-111">Remarks</span></span>  
 <span data-ttu-id="c1b09-112">El uso de memoria se puede recuperar siempre, independientemente de si el motor en tiempo de ejecución está activo o no en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="c1b09-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="c1b09-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b09-113">Requirements</span></span>  
 <span data-ttu-id="c1b09-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c1b09-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c1b09-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c1b09-115">See Also</span></span>  
 [<span data-ttu-id="c1b09-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c1b09-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
