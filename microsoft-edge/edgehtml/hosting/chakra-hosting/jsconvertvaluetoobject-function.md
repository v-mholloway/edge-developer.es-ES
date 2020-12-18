---
description: Convierte el valor en objeto usando la semántica estándar de JavaScript.
title: Función JsConvertValueToObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6f3676b512585b0750c994bcfcdf9d2e6e4e1cc3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236083"
---
# <span data-ttu-id="dd4ef-103">Función JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="dd4ef-103">JsConvertValueToObject Function</span></span>

<span data-ttu-id="dd4ef-104">Convierte el valor en objeto usando la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dd4ef-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="dd4ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd4ef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="dd4ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd4ef-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="dd4ef-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="dd4ef-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="dd4ef-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="dd4ef-108">The converted value.</span></span>  
  
## <span data-ttu-id="dd4ef-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd4ef-109">Return Value</span></span>  
 <span data-ttu-id="dd4ef-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="dd4ef-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dd4ef-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd4ef-111">Remarks</span></span>  
 <span data-ttu-id="dd4ef-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="dd4ef-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dd4ef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd4ef-113">Requirements</span></span>  
 <span data-ttu-id="dd4ef-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dd4ef-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dd4ef-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dd4ef-115">See Also</span></span>  
 [<span data-ttu-id="dd4ef-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dd4ef-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
