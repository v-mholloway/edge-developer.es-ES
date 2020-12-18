---
description: 'Establece una función de devolución de llamada que el motor en tiempo de ejecución llama antes de la recolección de elementos no utilizados. '
title: Función JsSetRuntimeBeforeCollectCallback | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236066"
---
# <span data-ttu-id="fd5c0-103">Función JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="fd5c0-103">JsSetRuntimeBeforeCollectCallback Function</span></span>

<span data-ttu-id="fd5c0-104">Establece una función de devolución de llamada que el motor en tiempo de ejecución llama antes de la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="fd5c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd5c0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="fd5c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd5c0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="fd5c0-107">Motor en tiempo de ejecución para el que se va a registrar la devolución de llamada de asignación.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="fd5c0-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="fd5c0-109">Función de devolución de llamada que se establece.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="fd5c0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd5c0-110">Return Value</span></span>  
 <span data-ttu-id="fd5c0-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fd5c0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd5c0-112">Remarks</span></span>  
 <span data-ttu-id="fd5c0-113">La devolución de llamada se invoca en el actual subproceso de ejecución en tiempo de ejecución; por lo tanto, la ejecución se bloquea hasta que se completa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="fd5c0-114">Los hosts pueden usar la devolución de llamada para prepararse para la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="fd5c0-115">Por ejemplo, al liberar referencias innecesarias en objetos Chakra.</span><span class="sxs-lookup"><span data-stu-id="fd5c0-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="fd5c0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd5c0-116">Requirements</span></span>  
 <span data-ttu-id="fd5c0-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fd5c0-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fd5c0-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fd5c0-118">See Also</span></span>  
 [<span data-ttu-id="fd5c0-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fd5c0-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
