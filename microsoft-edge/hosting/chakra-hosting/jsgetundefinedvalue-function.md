---
description: Obtiene el valor de `undefined` en el contexto de script actual.
title: Función JsGetUndefinedValue | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5edd536a29f5003591de476cb5d21ddb64f48c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574571"
---
# <span data-ttu-id="3869e-103">Función JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="3869e-103">JsGetUndefinedValue Function</span></span>
<span data-ttu-id="3869e-104">Obtiene el valor de `undefined` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="3869e-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="3869e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3869e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="3869e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3869e-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="3869e-107">El `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="3869e-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="3869e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3869e-108">Return Value</span></span>  
 <span data-ttu-id="3869e-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="3869e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3869e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3869e-110">Remarks</span></span>  
 <span data-ttu-id="3869e-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="3869e-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3869e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3869e-112">Requirements</span></span>  
 <span data-ttu-id="3869e-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3869e-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3869e-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3869e-114">See Also</span></span>  
 [<span data-ttu-id="3869e-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3869e-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)