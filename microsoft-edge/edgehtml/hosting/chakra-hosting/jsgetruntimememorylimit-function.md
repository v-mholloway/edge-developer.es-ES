---
description: Obtiene el límite de memoria actual para un tiempo de ejecución.
title: Función JsGetRuntimeMemoryLimit | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236590"
---
# <span data-ttu-id="36fe1-103">Función JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="36fe1-103">JsGetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="36fe1-104">Obtiene el límite de memoria actual para un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="36fe1-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="36fe1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36fe1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="36fe1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36fe1-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="36fe1-107">Tiempo de ejecución cuyo límite de memoria se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="36fe1-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="36fe1-108">Límite de memoria actual del motor en tiempo de ejecución, en bytes, o-1 si no se ha establecido ningún límite.</span><span class="sxs-lookup"><span data-stu-id="36fe1-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="36fe1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36fe1-109">Return Value</span></span>  
 <span data-ttu-id="36fe1-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="36fe1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="36fe1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36fe1-111">Remarks</span></span>  
 <span data-ttu-id="36fe1-112">El límite de memoria de un motor en tiempo de ejecución se puede recuperar siempre, independientemente de si el motor en tiempo de ejecución está activo o no en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="36fe1-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="36fe1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36fe1-113">Requirements</span></span>  
 <span data-ttu-id="36fe1-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="36fe1-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="36fe1-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="36fe1-115">See Also</span></span>  
 [<span data-ttu-id="36fe1-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="36fe1-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
