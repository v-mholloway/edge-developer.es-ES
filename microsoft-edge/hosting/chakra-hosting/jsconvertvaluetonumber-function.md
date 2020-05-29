---
description: Convierte el valor en número mediante la semántica estándar de JavaScript.
title: Función JsConvertValueToNumber | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3b3f450a58aaf1c434e1d34cd51577e3a5a9ee31
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573518"
---
# <span data-ttu-id="2226b-103">Función JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="2226b-103">JsConvertValueToNumber Function</span></span>
<span data-ttu-id="2226b-104">Convierte el valor en número mediante la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2226b-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="2226b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2226b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="2226b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2226b-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="2226b-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="2226b-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="2226b-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="2226b-108">The converted value.</span></span>  
  
## <span data-ttu-id="2226b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2226b-109">Return Value</span></span>  
 <span data-ttu-id="2226b-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="2226b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2226b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2226b-111">Remarks</span></span>  
 <span data-ttu-id="2226b-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="2226b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2226b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2226b-113">Requirements</span></span>  
 <span data-ttu-id="2226b-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2226b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2226b-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2226b-115">See Also</span></span>  
 [<span data-ttu-id="2226b-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2226b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)