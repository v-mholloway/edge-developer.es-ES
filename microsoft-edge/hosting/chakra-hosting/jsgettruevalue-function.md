---
description: Obtiene el valor de `true` en el contexto de script actual.
title: Función JsGetTrueValue | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 620ed775947db9d7156d61df1cfdf974a46baec2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573437"
---
# <span data-ttu-id="15dd0-103">Función JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="15dd0-103">JsGetTrueValue Function</span></span>
<span data-ttu-id="15dd0-104">Obtiene el valor de `true` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="15dd0-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="15dd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15dd0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="15dd0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15dd0-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="15dd0-107">El `true` valor.</span><span class="sxs-lookup"><span data-stu-id="15dd0-107">The `true` value.</span></span>  
  
## <span data-ttu-id="15dd0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15dd0-108">Return Value</span></span>  
 <span data-ttu-id="15dd0-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="15dd0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="15dd0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15dd0-110">Remarks</span></span>  
 <span data-ttu-id="15dd0-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="15dd0-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="15dd0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15dd0-112">Requirements</span></span>  
 <span data-ttu-id="15dd0-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="15dd0-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="15dd0-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="15dd0-114">See Also</span></span>  
 [<span data-ttu-id="15dd0-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="15dd0-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)