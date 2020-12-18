---
description: Convierte el valor en Boolean con la semántica estándar de JavaScript.
title: Función JsConvertValueToBoolean | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d2e109690fc8a7a98a1ecb84d6f5abf6a646162b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236097"
---
# <span data-ttu-id="7e555-103">Función JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="7e555-103">JsConvertValueToBoolean Function</span></span>

<span data-ttu-id="7e555-104">Convierte el valor en Boolean con la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7e555-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="7e555-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e555-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="7e555-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e555-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="7e555-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="7e555-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="7e555-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="7e555-108">The converted value.</span></span>  
  
## <span data-ttu-id="7e555-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e555-109">Return Value</span></span>  
 <span data-ttu-id="7e555-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7e555-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7e555-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e555-111">Remarks</span></span>  
 <span data-ttu-id="7e555-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7e555-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7e555-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e555-113">Requirements</span></span>  
 <span data-ttu-id="7e555-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7e555-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7e555-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7e555-115">See Also</span></span>  
 [<span data-ttu-id="7e555-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7e555-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
