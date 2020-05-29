---
description: Crea una nueva función de JavaScript.
title: Función JsCreateFunction | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 22585afcb379c281eda621c3b233ccf4bc278ad1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573499"
---
# <span data-ttu-id="a065a-103">Función JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="a065a-103">JsCreateFunction Function</span></span>
<span data-ttu-id="a065a-104">Crea una nueva función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a065a-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="a065a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a065a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="a065a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a065a-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="a065a-107">El método al que se llama cuando se invoca la función.</span><span class="sxs-lookup"><span data-stu-id="a065a-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="a065a-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a065a-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="a065a-109">El nuevo objeto de función.</span><span class="sxs-lookup"><span data-stu-id="a065a-109">The new function object.</span></span>  
  
## <span data-ttu-id="a065a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a065a-110">Return Value</span></span>  
 <span data-ttu-id="a065a-111">El resultado de la llamada, si existe.</span><span class="sxs-lookup"><span data-stu-id="a065a-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="a065a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a065a-112">Remarks</span></span>  
 <span data-ttu-id="a065a-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="a065a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a065a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a065a-114">Requirements</span></span>  
 <span data-ttu-id="a065a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a065a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a065a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a065a-116">See Also</span></span>  
 [<span data-ttu-id="a065a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a065a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)