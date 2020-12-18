---
description: Crea un valor booleano a partir de un `bool` valor.
title: Función JsBoolToBoolean | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3d6ec9f85d53e0d78c6bbe1c7d3282971831717b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236098"
---
# <span data-ttu-id="b1fb5-103">Función JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="b1fb5-103">JsBoolToBoolean Function</span></span>

<span data-ttu-id="b1fb5-104">Crea un valor booleano a partir de un `bool` valor.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="b1fb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1fb5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="b1fb5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1fb5-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="b1fb5-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="b1fb5-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-108">The converted value.</span></span>  
  
## <span data-ttu-id="b1fb5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1fb5-109">Return Value</span></span>  
 <span data-ttu-id="b1fb5-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b1fb5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1fb5-111">Remarks</span></span>  
 <span data-ttu-id="b1fb5-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b1fb5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1fb5-113">Requirements</span></span>  
 <span data-ttu-id="b1fb5-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b1fb5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b1fb5-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b1fb5-115">See Also</span></span>  
 [<span data-ttu-id="b1fb5-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b1fb5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
