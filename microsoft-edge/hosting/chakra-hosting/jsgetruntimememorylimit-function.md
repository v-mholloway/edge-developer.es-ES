---
description: Obtiene el límite de memoria actual para un tiempo de ejecución.
title: Función JsGetRuntimeMemoryLimit | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e6b44bb1dc8ad5fb8c07248a225c10682f96c86a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573444"
---
# <span data-ttu-id="46baa-103">Función JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="46baa-103">JsGetRuntimeMemoryLimit Function</span></span>
<span data-ttu-id="46baa-104">Obtiene el límite de memoria actual para un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="46baa-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="46baa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46baa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="46baa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46baa-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="46baa-107">Tiempo de ejecución cuyo límite de memoria se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="46baa-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="46baa-108">Límite de memoria actual del motor en tiempo de ejecución, en bytes, o-1 si no se ha establecido ningún límite.</span><span class="sxs-lookup"><span data-stu-id="46baa-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="46baa-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46baa-109">Return Value</span></span>  
 <span data-ttu-id="46baa-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="46baa-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="46baa-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46baa-111">Remarks</span></span>  
 <span data-ttu-id="46baa-112">El límite de memoria de un motor en tiempo de ejecución se puede recuperar siempre, independientemente de si el motor en tiempo de ejecución está activo o no en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="46baa-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="46baa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46baa-113">Requirements</span></span>  
 <span data-ttu-id="46baa-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="46baa-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="46baa-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="46baa-115">See Also</span></span>  
 [<span data-ttu-id="46baa-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="46baa-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)