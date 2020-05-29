---
description: Una devolución de llamada de continuación de Promise.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573405"
---
# <span data-ttu-id="e15e1-103">JsPromiseContinuationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="e15e1-103">JsPromiseContinuationCallback Typedef</span></span>
<span data-ttu-id="e15e1-104">Una devolución de llamada de continuación de Promise.</span><span class="sxs-lookup"><span data-stu-id="e15e1-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="e15e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e15e1-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e15e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e15e1-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="e15e1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e15e1-107">Remarks</span></span>  
 <span data-ttu-id="e15e1-108">El host puede especificar una devolución de llamada de continuación de Promise `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="e15e1-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="e15e1-109">Si un script crea una tarea que se va a ejecutar más adelante, se llamará a la devolución de llamada de continuación de Promise con la tarea y la tarea debe ponerse en una cola FIFO, que se ejecutará cuando el script actual termine de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e15e1-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="e15e1-110">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e15e1-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e15e1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e15e1-111">Requirements</span></span>  
 <span data-ttu-id="e15e1-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e15e1-112">jsrt.h</span></span>  
  
## <span data-ttu-id="e15e1-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e15e1-113">See Also</span></span>  
 [<span data-ttu-id="e15e1-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e15e1-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)