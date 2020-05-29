---
description: Devuelve un valor que indica si se está enumerando el montón del contexto actual.
title: Función JsIsEnumeratingHeap | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 79f263547ef5812d905103d09ede7499d56c5dfb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573427"
---
# <span data-ttu-id="913c9-103">Función JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="913c9-103">JsIsEnumeratingHeap Function</span></span>
<span data-ttu-id="913c9-104">Devuelve un valor que indica si se está enumerando el montón del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="913c9-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="913c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="913c9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="913c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="913c9-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="913c9-107">Si se está enumerando el montón.</span><span class="sxs-lookup"><span data-stu-id="913c9-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="913c9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="913c9-108">Return Value</span></span>  
 <span data-ttu-id="913c9-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="913c9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="913c9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="913c9-110">Remarks</span></span>  
 <span data-ttu-id="913c9-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="913c9-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="913c9-112">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="913c9-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="913c9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913c9-113">Requirements</span></span>  
 <span data-ttu-id="913c9-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="913c9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="913c9-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="913c9-115">See Also</span></span>  
 [<span data-ttu-id="913c9-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="913c9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)