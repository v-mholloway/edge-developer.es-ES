---
description: Establece una función de devolución de llamada de continuación de Promise a la que llama el contexto cuando una tarea se debe poner en cola para su ejecución futura.
title: Función JsSetPromiseContinuationCallback | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236316"
---
# <span data-ttu-id="e545c-103">Función JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="e545c-103">JsSetPromiseContinuationCallback Function</span></span>

<span data-ttu-id="e545c-104">Establece una función de devolución de llamada de continuación de Promise a la que llama el contexto cuando una tarea se debe poner en cola para su ejecución futura.</span><span class="sxs-lookup"><span data-stu-id="e545c-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="e545c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e545c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e545c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e545c-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="e545c-107">Función de devolución de llamada que se establece.</span><span class="sxs-lookup"><span data-stu-id="e545c-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e545c-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e545c-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="e545c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e545c-109">Return Value</span></span>  
 <span data-ttu-id="e545c-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e545c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e545c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e545c-111">Remarks</span></span>  
 <span data-ttu-id="e545c-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e545c-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e545c-113">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e545c-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e545c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e545c-114">Requirements</span></span>  
 <span data-ttu-id="e545c-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e545c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e545c-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e545c-116">See Also</span></span>  
 [<span data-ttu-id="e545c-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e545c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
