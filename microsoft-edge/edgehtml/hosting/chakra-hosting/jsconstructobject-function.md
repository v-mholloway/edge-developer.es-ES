---
description: Invoca una función como un constructor.
title: Función JsConstructObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8dbb757456412e50efaf3a026d169e6b3612b6b1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236093"
---
# <span data-ttu-id="36dfd-103">Función JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="36dfd-103">JsConstructObject Function</span></span>

<span data-ttu-id="36dfd-104">Invoca una función como un constructor.</span><span class="sxs-lookup"><span data-stu-id="36dfd-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="36dfd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36dfd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="36dfd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36dfd-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="36dfd-107">Función que se va a invocar como constructor.</span><span class="sxs-lookup"><span data-stu-id="36dfd-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="36dfd-108">Los argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="36dfd-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="36dfd-109">Número de argumentos que se pasan a la función.</span><span class="sxs-lookup"><span data-stu-id="36dfd-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="36dfd-110">El valor devuelto de la invocación de la función.</span><span class="sxs-lookup"><span data-stu-id="36dfd-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="36dfd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36dfd-111">Return Value</span></span>  
 <span data-ttu-id="36dfd-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="36dfd-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="36dfd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36dfd-113">Remarks</span></span>  
 <span data-ttu-id="36dfd-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="36dfd-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="36dfd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36dfd-115">Requirements</span></span>  
 <span data-ttu-id="36dfd-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="36dfd-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="36dfd-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="36dfd-117">See Also</span></span>  
 [<span data-ttu-id="36dfd-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="36dfd-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
