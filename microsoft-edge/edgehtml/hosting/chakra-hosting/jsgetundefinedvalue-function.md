---
description: Obtiene el valor de `undefined` en el contexto de script actual.
title: Función JsGetUndefinedValue | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34bfaec4548ee2b77d6d98749c3049bb8f679134
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235941"
---
# <span data-ttu-id="45c49-103">Función JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="45c49-103">JsGetUndefinedValue Function</span></span>

<span data-ttu-id="45c49-104">Obtiene el valor de `undefined` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="45c49-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="45c49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45c49-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="45c49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45c49-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="45c49-107">El `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="45c49-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="45c49-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45c49-108">Return Value</span></span>  
 <span data-ttu-id="45c49-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="45c49-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="45c49-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45c49-110">Remarks</span></span>  
 <span data-ttu-id="45c49-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="45c49-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="45c49-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c49-112">Requirements</span></span>  
 <span data-ttu-id="45c49-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="45c49-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="45c49-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="45c49-114">See Also</span></span>  
 [<span data-ttu-id="45c49-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="45c49-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
