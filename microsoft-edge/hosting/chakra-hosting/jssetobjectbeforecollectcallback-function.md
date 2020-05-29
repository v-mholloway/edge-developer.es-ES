---
description: Establece una función de devolución de llamada a la que llama el motor en tiempo de ejecución antes de la recolección de elementos no utilizados de un objeto.
title: Función JsSetObjectBeforeCollectCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574507"
---
# <span data-ttu-id="00cab-103">Función JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="00cab-103">JsSetObjectBeforeCollectCallback Function</span></span>
<span data-ttu-id="00cab-104">Establece una función de devolución de llamada a la que llama el motor en tiempo de ejecución antes de la recolección de elementos no utilizados de un objeto.</span><span class="sxs-lookup"><span data-stu-id="00cab-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="00cab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00cab-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="00cab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00cab-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="00cab-107">Objeto para el que se va a registrar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="00cab-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="00cab-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="00cab-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="00cab-109">Función de devolución de llamada que se establece.</span><span class="sxs-lookup"><span data-stu-id="00cab-109">The callback function being set.</span></span> <span data-ttu-id="00cab-110">Use null para borrar la devolución de llamada previamente registrada.</span><span class="sxs-lookup"><span data-stu-id="00cab-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="00cab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00cab-111">Return Value</span></span>  
 <span data-ttu-id="00cab-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="00cab-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="00cab-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00cab-113">Remarks</span></span>  
 <span data-ttu-id="00cab-114">La devolución de llamada se invoca en el actual subproceso de ejecución en tiempo de ejecución; por lo tanto, la ejecución se bloquea hasta que se completa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="00cab-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="00cab-115">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="00cab-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="00cab-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00cab-116">Requirements</span></span>  
 <span data-ttu-id="00cab-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="00cab-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="00cab-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="00cab-118">See Also</span></span>  
 [<span data-ttu-id="00cab-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="00cab-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)