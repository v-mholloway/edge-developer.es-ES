---
description: Determina si el motor en tiempo de ejecución del contexto actual se encuentra en estado de excepción.
title: Función JsHasException | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574565"
---
# <span data-ttu-id="929e4-103">Función JsHasException</span><span class="sxs-lookup"><span data-stu-id="929e4-103">JsHasException Function</span></span>
<span data-ttu-id="929e4-104">Determina si el motor en tiempo de ejecución del contexto actual se encuentra en estado de excepción.</span><span class="sxs-lookup"><span data-stu-id="929e4-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="929e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="929e4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="929e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="929e4-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="929e4-107">Si el tiempo de ejecución del contexto actual está en el estado de excepción.</span><span class="sxs-lookup"><span data-stu-id="929e4-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="929e4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="929e4-108">Return Value</span></span>  
 <span data-ttu-id="929e4-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="929e4-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="929e4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="929e4-110">Remarks</span></span>  
 <span data-ttu-id="929e4-111">Si una llamada al motor en tiempo de ejecución genera una excepción (ya sea como resultado de ejecutar un script o debido a un error de conversión), el motor en tiempo de ejecución se coloca en "estado de excepción".</span><span class="sxs-lookup"><span data-stu-id="929e4-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="929e4-112">Se producirá un error en todas las llamadas creadas por el motor en tiempo de ejecución (excepto las API de excepción) `JsErrorInExceptionState` hasta que se borre la excepción.</span><span class="sxs-lookup"><span data-stu-id="929e4-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="929e4-113">Si el tiempo de ejecución del contexto actual está en el estado de excepción cuando se devuelve una devolución de llamada en el motor, el motor volverá a iniciar automáticamente la excepción.</span><span class="sxs-lookup"><span data-stu-id="929e4-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="929e4-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="929e4-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="929e4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="929e4-115">Requirements</span></span>  
 <span data-ttu-id="929e4-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="929e4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="929e4-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="929e4-117">See Also</span></span>  
 [<span data-ttu-id="929e4-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="929e4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)