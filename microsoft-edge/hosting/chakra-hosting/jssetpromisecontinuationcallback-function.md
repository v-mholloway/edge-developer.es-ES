---
description: Establece una función de devolución de llamada de continuación de Promise a la que llama el contexto cuando una tarea se debe poner en cola para su ejecución futura.
title: Función JsSetPromiseContinuationCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9438bf05d879b0c2014c0a4d49d374d26eff3fb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574504"
---
# <span data-ttu-id="e50b6-103">Función JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="e50b6-103">JsSetPromiseContinuationCallback Function</span></span>
<span data-ttu-id="e50b6-104">Establece una función de devolución de llamada de continuación de Promise a la que llama el contexto cuando una tarea se debe poner en cola para su ejecución futura.</span><span class="sxs-lookup"><span data-stu-id="e50b6-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="e50b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e50b6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e50b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e50b6-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="e50b6-107">Función de devolución de llamada que se establece.</span><span class="sxs-lookup"><span data-stu-id="e50b6-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e50b6-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e50b6-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="e50b6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e50b6-109">Return Value</span></span>  
 <span data-ttu-id="e50b6-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e50b6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e50b6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e50b6-111">Remarks</span></span>  
 <span data-ttu-id="e50b6-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e50b6-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e50b6-113">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e50b6-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e50b6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e50b6-114">Requirements</span></span>  
 <span data-ttu-id="e50b6-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e50b6-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e50b6-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e50b6-116">See Also</span></span>  
 [<span data-ttu-id="e50b6-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e50b6-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)