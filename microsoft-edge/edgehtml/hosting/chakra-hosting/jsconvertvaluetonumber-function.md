---
description: Convierte el valor en número mediante la semántica estándar de JavaScript.
title: Función JsConvertValueToNumber | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8d00950ef3835c6d75f8f55ffe5002b32c6ee160
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236100"
---
# <span data-ttu-id="47792-103">Función JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="47792-103">JsConvertValueToNumber Function</span></span>

<span data-ttu-id="47792-104">Convierte el valor en número mediante la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="47792-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="47792-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47792-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="47792-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47792-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="47792-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="47792-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="47792-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="47792-108">The converted value.</span></span>  
  
## <span data-ttu-id="47792-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47792-109">Return Value</span></span>  
 <span data-ttu-id="47792-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="47792-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="47792-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47792-111">Remarks</span></span>  
 <span data-ttu-id="47792-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="47792-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="47792-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47792-113">Requirements</span></span>  
 <span data-ttu-id="47792-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="47792-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="47792-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="47792-115">See Also</span></span>  
 [<span data-ttu-id="47792-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="47792-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
