---
description: Obtiene el valor de `null` en el contexto de script actual.
title: Función JsGetNullValue | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84164aa9ce5d522b0933d928d85b26c652be066f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574590"
---
# <span data-ttu-id="b2da7-103">Función JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="b2da7-103">JsGetNullValue Function</span></span>
<span data-ttu-id="b2da7-104">Obtiene el valor de `null` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="b2da7-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="b2da7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2da7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="b2da7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2da7-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="b2da7-107">El `null` valor.</span><span class="sxs-lookup"><span data-stu-id="b2da7-107">The `null` value.</span></span>  
  
## <span data-ttu-id="b2da7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2da7-108">Return Value</span></span>  
 <span data-ttu-id="b2da7-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b2da7-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b2da7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2da7-110">Remarks</span></span>  
 <span data-ttu-id="b2da7-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b2da7-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b2da7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2da7-112">Requirements</span></span>  
 <span data-ttu-id="b2da7-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b2da7-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b2da7-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b2da7-114">See Also</span></span>  
 [<span data-ttu-id="b2da7-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b2da7-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)