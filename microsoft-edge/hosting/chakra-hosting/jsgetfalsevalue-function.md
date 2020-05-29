---
description: Obtiene el valor de `false` en el contexto de script actual.
title: Función JsGetFalseValue | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 52e54ad7eb34877c3cb83b06f5aba70edf285bca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573457"
---
# <span data-ttu-id="85968-103">Función JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="85968-103">JsGetFalseValue Function</span></span>
<span data-ttu-id="85968-104">Obtiene el valor de `false` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="85968-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="85968-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85968-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="85968-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85968-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="85968-107">El `false` valor.</span><span class="sxs-lookup"><span data-stu-id="85968-107">The `false` value.</span></span>  
  
## <span data-ttu-id="85968-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85968-108">Return Value</span></span>  
 <span data-ttu-id="85968-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="85968-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="85968-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85968-110">Remarks</span></span>  
 <span data-ttu-id="85968-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="85968-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="85968-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85968-112">Requirements</span></span>  
 <span data-ttu-id="85968-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="85968-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="85968-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="85968-114">See Also</span></span>  
 [<span data-ttu-id="85968-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="85968-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)