---
description: Crea un nuevo objeto de error RangeError de JavaScript.
title: Función JsCreateRangeError | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 72cf882d5f9517f0f05d9e3367283f5f531dbdb3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236244"
---
# <span data-ttu-id="5fcf2-103">Función JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="5fcf2-103">JsCreateRangeError Function</span></span>

<span data-ttu-id="5fcf2-104">Crea un nuevo objeto de error RangeError de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5fcf2-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="5fcf2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fcf2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="5fcf2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fcf2-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="5fcf2-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="5fcf2-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="5fcf2-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="5fcf2-108">The new error object.</span></span>  
  
## <span data-ttu-id="5fcf2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fcf2-109">Return Value</span></span>  
 <span data-ttu-id="5fcf2-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="5fcf2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5fcf2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fcf2-111">Remarks</span></span>  
 <span data-ttu-id="5fcf2-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="5fcf2-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5fcf2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fcf2-113">Requirements</span></span>  
 <span data-ttu-id="5fcf2-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5fcf2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5fcf2-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5fcf2-115">See Also</span></span>  
 [<span data-ttu-id="5fcf2-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5fcf2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
