---
description: Establece una función de devolución de llamada a la que llama el motor en tiempo de ejecución antes de la recolección de elementos no utilizados de un objeto.
title: Función JsSetObjectBeforeCollectCallback | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4689184dccaf6bc9f98eeacda5f5a4b91a927d40
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236065"
---
# <span data-ttu-id="3f3bc-103">Función JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="3f3bc-103">JsSetObjectBeforeCollectCallback Function</span></span>

<span data-ttu-id="3f3bc-104">Establece una función de devolución de llamada a la que llama el motor en tiempo de ejecución antes de la recolección de elementos no utilizados de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="3f3bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f3bc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="3f3bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f3bc-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="3f3bc-107">Objeto para el que se va a registrar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="3f3bc-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="3f3bc-109">Función de devolución de llamada que se establece.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-109">The callback function being set.</span></span> <span data-ttu-id="3f3bc-110">Use null para borrar la devolución de llamada previamente registrada.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="3f3bc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f3bc-111">Return Value</span></span>  
 <span data-ttu-id="3f3bc-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3f3bc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f3bc-113">Remarks</span></span>  
 <span data-ttu-id="3f3bc-114">La devolución de llamada se invoca en el actual subproceso de ejecución en tiempo de ejecución; por lo tanto, la ejecución se bloquea hasta que se completa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="3f3bc-115">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="3f3bc-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="3f3bc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f3bc-116">Requirements</span></span>  
 <span data-ttu-id="3f3bc-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3f3bc-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3f3bc-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3f3bc-118">See Also</span></span>  
 [<span data-ttu-id="3f3bc-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3f3bc-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
