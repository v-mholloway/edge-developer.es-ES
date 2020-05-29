---
description: Crea un valor numérico a partir de un valor de tipo Double.
title: Función JsDoubleToNumber | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c33adbe217f27f77e348fc56e87c4587c6a6ec4c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574606"
---
# <span data-ttu-id="181cd-103">Función JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="181cd-103">JsDoubleToNumber Function</span></span>
<span data-ttu-id="181cd-104">Crea un valor de número a partir de un `double` valor.</span><span class="sxs-lookup"><span data-stu-id="181cd-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="181cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="181cd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="181cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="181cd-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="181cd-107">`double`Para convertir en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="181cd-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="181cd-108">El nuevo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="181cd-108">The new number value.</span></span>  
  
## <span data-ttu-id="181cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="181cd-109">Return Value</span></span>  
 <span data-ttu-id="181cd-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="181cd-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="181cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="181cd-111">Remarks</span></span>  
 <span data-ttu-id="181cd-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="181cd-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="181cd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="181cd-113">Requirements</span></span>  
 <span data-ttu-id="181cd-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="181cd-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="181cd-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="181cd-115">See Also</span></span>  
 [<span data-ttu-id="181cd-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="181cd-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)