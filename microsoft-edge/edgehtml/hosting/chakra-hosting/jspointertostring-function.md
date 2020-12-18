---
description: Crea un valor de cadena a partir de un puntero de cadena.
title: Función JsPointerToString | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c00a060098f0b021afca27b300f3e0578e992cb9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236410"
---
# <span data-ttu-id="5283a-103">Función JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="5283a-103">JsPointerToString Function</span></span>

<span data-ttu-id="5283a-104">Crea un valor de cadena a partir de un puntero de cadena.</span><span class="sxs-lookup"><span data-stu-id="5283a-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="5283a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5283a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="5283a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5283a-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="5283a-107">El puntero de cadena que se va a convertir en un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="5283a-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="5283a-108">Longitud de la cadena que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="5283a-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="5283a-109">El nuevo valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="5283a-109">The new string value.</span></span>  
  
## <span data-ttu-id="5283a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5283a-110">Return Value</span></span>  
 <span data-ttu-id="5283a-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="5283a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5283a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5283a-112">Remarks</span></span>  
 <span data-ttu-id="5283a-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="5283a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5283a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5283a-114">Requirements</span></span>  
 <span data-ttu-id="5283a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5283a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5283a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5283a-116">See Also</span></span>  
 [<span data-ttu-id="5283a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5283a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
