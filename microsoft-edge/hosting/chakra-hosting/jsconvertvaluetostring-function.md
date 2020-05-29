---
description: Convierte el valor en cadena mediante la semántica estándar de JavaScript.
title: Función JsConvertValueToString | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 21c77ca3050773c07572665c6d58e0ebc05d8ee9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573515"
---
# <span data-ttu-id="e95d8-103">Función JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="e95d8-103">JsConvertValueToString Function</span></span>
<span data-ttu-id="e95d8-104">Convierte el valor en cadena mediante la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e95d8-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="e95d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e95d8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="e95d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e95d8-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="e95d8-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e95d8-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="e95d8-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="e95d8-108">The converted value.</span></span>  
  
## <span data-ttu-id="e95d8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e95d8-109">Return Value</span></span>  
 <span data-ttu-id="e95d8-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e95d8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e95d8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e95d8-111">Remarks</span></span>  
 <span data-ttu-id="e95d8-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e95d8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e95d8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e95d8-113">Requirements</span></span>  
 <span data-ttu-id="e95d8-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e95d8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e95d8-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e95d8-115">See Also</span></span>  
 [<span data-ttu-id="e95d8-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e95d8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)