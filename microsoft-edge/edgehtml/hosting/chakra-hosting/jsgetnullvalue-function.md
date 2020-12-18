---
description: Obtiene el valor de `null` en el contexto de script actual.
title: Función JsGetNullValue | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235907"
---
# <span data-ttu-id="0fe9a-103">Función JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="0fe9a-103">JsGetNullValue Function</span></span>

<span data-ttu-id="0fe9a-104">Obtiene el valor de `null` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="0fe9a-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="0fe9a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fe9a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="0fe9a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fe9a-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="0fe9a-107">El `null` valor.</span><span class="sxs-lookup"><span data-stu-id="0fe9a-107">The `null` value.</span></span>  
  
## <span data-ttu-id="0fe9a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fe9a-108">Return Value</span></span>  
 <span data-ttu-id="0fe9a-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0fe9a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0fe9a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fe9a-110">Remarks</span></span>  
 <span data-ttu-id="0fe9a-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="0fe9a-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0fe9a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fe9a-112">Requirements</span></span>  
 <span data-ttu-id="0fe9a-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0fe9a-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0fe9a-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0fe9a-114">See Also</span></span>  
 [<span data-ttu-id="0fe9a-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0fe9a-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
