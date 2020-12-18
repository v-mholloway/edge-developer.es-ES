---
description: Devuelve el prototipo de un objeto.
title: Función JsGetPrototype | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d64e8b090753e5d0627f0d40ee8745eeadd65227
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236577"
---
# <span data-ttu-id="5426f-103">Función JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="5426f-103">JsGetPrototype Function</span></span>

<span data-ttu-id="5426f-104">Devuelve el prototipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="5426f-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="5426f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5426f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="5426f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5426f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="5426f-107">Objeto cuyo prototipo se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="5426f-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="5426f-108">Prototipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="5426f-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="5426f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5426f-109">Return Value</span></span>  
 <span data-ttu-id="5426f-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="5426f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5426f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5426f-111">Remarks</span></span>  
 <span data-ttu-id="5426f-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="5426f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5426f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5426f-113">Requirements</span></span>  
 <span data-ttu-id="5426f-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5426f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5426f-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5426f-115">See Also</span></span>  
 [<span data-ttu-id="5426f-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5426f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
