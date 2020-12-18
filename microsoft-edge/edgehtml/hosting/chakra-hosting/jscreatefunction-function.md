---
description: Crea una nueva función de JavaScript.
title: Función JsCreateFunction | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f7e67e86e6d8055664bfb1b58e6d5653f6d75d1b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236437"
---
# <span data-ttu-id="1464b-103">Función JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="1464b-103">JsCreateFunction Function</span></span>

<span data-ttu-id="1464b-104">Crea una nueva función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1464b-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="1464b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1464b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="1464b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1464b-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="1464b-107">El método al que se llama cuando se invoca la función.</span><span class="sxs-lookup"><span data-stu-id="1464b-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="1464b-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1464b-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="1464b-109">El nuevo objeto de función.</span><span class="sxs-lookup"><span data-stu-id="1464b-109">The new function object.</span></span>  
  
## <span data-ttu-id="1464b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1464b-110">Return Value</span></span>  
 <span data-ttu-id="1464b-111">El resultado de la llamada, si existe.</span><span class="sxs-lookup"><span data-stu-id="1464b-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="1464b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1464b-112">Remarks</span></span>  
 <span data-ttu-id="1464b-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="1464b-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1464b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1464b-114">Requirements</span></span>  
 <span data-ttu-id="1464b-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1464b-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1464b-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="1464b-116">See Also</span></span>  
 [<span data-ttu-id="1464b-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1464b-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
