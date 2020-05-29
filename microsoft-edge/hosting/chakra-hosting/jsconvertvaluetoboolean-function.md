---
description: Convierte el valor en Boolean con la semántica estándar de JavaScript.
title: Función JsConvertValueToBoolean | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 861871a030d5a47621ccaf40b6cd332f42a06583
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573520"
---
# <span data-ttu-id="c0ba4-103">Función JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="c0ba4-103">JsConvertValueToBoolean Function</span></span>
<span data-ttu-id="c0ba4-104">Convierte el valor en Boolean con la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0ba4-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="c0ba4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0ba4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="c0ba4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0ba4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="c0ba4-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="c0ba4-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="c0ba4-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="c0ba4-108">The converted value.</span></span>  
  
## <span data-ttu-id="c0ba4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0ba4-109">Return Value</span></span>  
 <span data-ttu-id="c0ba4-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c0ba4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c0ba4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0ba4-111">Remarks</span></span>  
 <span data-ttu-id="c0ba4-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="c0ba4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c0ba4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0ba4-113">Requirements</span></span>  
 <span data-ttu-id="c0ba4-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c0ba4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c0ba4-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c0ba4-115">See Also</span></span>  
 [<span data-ttu-id="c0ba4-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c0ba4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)