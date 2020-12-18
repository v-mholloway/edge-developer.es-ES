---
description: Crea un valor numérico a partir de un valor de tipo Double.
title: Función JsDoubleToNumber | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236280"
---
# <span data-ttu-id="9c791-103">Función JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="9c791-103">JsDoubleToNumber Function</span></span>

<span data-ttu-id="9c791-104">Crea un valor de número a partir de un `double` valor.</span><span class="sxs-lookup"><span data-stu-id="9c791-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="9c791-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c791-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="9c791-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c791-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="9c791-107">`double`Para convertir en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="9c791-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="9c791-108">El nuevo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="9c791-108">The new number value.</span></span>  
  
## <span data-ttu-id="9c791-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c791-109">Return Value</span></span>  
 <span data-ttu-id="9c791-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="9c791-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c791-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c791-111">Remarks</span></span>  
 <span data-ttu-id="9c791-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="9c791-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9c791-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c791-113">Requirements</span></span>  
 <span data-ttu-id="9c791-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9c791-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c791-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="9c791-115">See Also</span></span>  
 [<span data-ttu-id="9c791-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9c791-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
