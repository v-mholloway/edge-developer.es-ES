---
description: Obtiene el valor de `false` en el contexto de script actual.
title: Función JsGetFalseValue | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c87ad969fc7547f4d650148005327fb93dce805d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236323"
---
# <span data-ttu-id="fd492-103">Función JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="fd492-103">JsGetFalseValue Function</span></span>

<span data-ttu-id="fd492-104">Obtiene el valor de `false` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="fd492-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="fd492-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd492-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="fd492-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd492-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="fd492-107">El `false` valor.</span><span class="sxs-lookup"><span data-stu-id="fd492-107">The `false` value.</span></span>  
  
## <span data-ttu-id="fd492-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd492-108">Return Value</span></span>  
 <span data-ttu-id="fd492-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="fd492-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fd492-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd492-110">Remarks</span></span>  
 <span data-ttu-id="fd492-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="fd492-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fd492-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd492-112">Requirements</span></span>  
 <span data-ttu-id="fd492-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fd492-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fd492-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fd492-114">See Also</span></span>  
 [<span data-ttu-id="fd492-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fd492-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
