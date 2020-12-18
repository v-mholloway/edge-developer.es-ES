---
description: Una devolución de llamada de continuación de Promise.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236640"
---
# <span data-ttu-id="ea3a2-103">Definición de tipo JsPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="ea3a2-103">JsPromiseContinuationCallback Typedef</span></span>

<span data-ttu-id="ea3a2-104">Una devolución de llamada de continuación de Promise.</span><span class="sxs-lookup"><span data-stu-id="ea3a2-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="ea3a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea3a2-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="ea3a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea3a2-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="ea3a2-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea3a2-107">Remarks</span></span>  
 <span data-ttu-id="ea3a2-108">El host puede especificar una devolución de llamada de continuación de Promise `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="ea3a2-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="ea3a2-109">Si un script crea una tarea que se va a ejecutar más adelante, se llamará a la devolución de llamada de continuación de Promise con la tarea y la tarea debe ponerse en una cola FIFO, que se ejecutará cuando el script actual termine de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="ea3a2-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="ea3a2-110">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="ea3a2-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="ea3a2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea3a2-111">Requirements</span></span>  
 <span data-ttu-id="ea3a2-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ea3a2-112">jsrt.h</span></span>  
  
## <span data-ttu-id="ea3a2-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ea3a2-113">See Also</span></span>  
 [<span data-ttu-id="ea3a2-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ea3a2-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
