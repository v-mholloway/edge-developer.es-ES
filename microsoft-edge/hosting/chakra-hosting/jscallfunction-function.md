---
description: Invoca una función.
title: Función JsCallFunction | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f242ccef71d8a2b361dbe2d1a299728f5551f5d3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573530"
---
# <span data-ttu-id="14871-103">Función JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="14871-103">JsCallFunction Function</span></span>
<span data-ttu-id="14871-104">Invoca una función.</span><span class="sxs-lookup"><span data-stu-id="14871-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="14871-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14871-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="14871-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14871-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="14871-107">Función que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="14871-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="14871-108">Los argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="14871-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="14871-109">Número de argumentos que se pasan a la función.</span><span class="sxs-lookup"><span data-stu-id="14871-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="14871-110">El valor devuelto de la invocación de la función, si existe.</span><span class="sxs-lookup"><span data-stu-id="14871-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="14871-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14871-111">Return Value</span></span>  
 <span data-ttu-id="14871-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="14871-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="14871-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14871-113">Remarks</span></span>  
 <span data-ttu-id="14871-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="14871-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="14871-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14871-115">Requirements</span></span>  
 <span data-ttu-id="14871-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="14871-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="14871-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="14871-117">See Also</span></span>  
 [<span data-ttu-id="14871-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="14871-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)