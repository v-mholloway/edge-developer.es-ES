---
description: Convierte el valor en cadena mediante la semántica estándar de JavaScript.
title: Función JsConvertValueToString | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 499f9555f6385b8458524fb4e14b92339c0aa478
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236082"
---
# <span data-ttu-id="baeb4-103">Función JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="baeb4-103">JsConvertValueToString Function</span></span>

<span data-ttu-id="baeb4-104">Convierte el valor en cadena mediante la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="baeb4-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="baeb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baeb4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="baeb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baeb4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="baeb4-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="baeb4-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="baeb4-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="baeb4-108">The converted value.</span></span>  
  
## <span data-ttu-id="baeb4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baeb4-109">Return Value</span></span>  
 <span data-ttu-id="baeb4-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="baeb4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="baeb4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baeb4-111">Remarks</span></span>  
 <span data-ttu-id="baeb4-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="baeb4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="baeb4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baeb4-113">Requirements</span></span>  
 <span data-ttu-id="baeb4-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="baeb4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="baeb4-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="baeb4-115">See Also</span></span>  
 [<span data-ttu-id="baeb4-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="baeb4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
