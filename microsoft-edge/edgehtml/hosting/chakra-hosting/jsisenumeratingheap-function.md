---
description: Devuelve un valor que indica si se está enumerando el montón del contexto actual.
title: Función JsIsEnumeratingHeap | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5b66fc70ea79d78029f6bc0c900ade1aae38e604
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236453"
---
# <span data-ttu-id="bdae6-103">Función JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="bdae6-103">JsIsEnumeratingHeap Function</span></span>

<span data-ttu-id="bdae6-104">Devuelve un valor que indica si se está enumerando el montón del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="bdae6-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="bdae6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdae6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="bdae6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdae6-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="bdae6-107">Si se está enumerando el montón.</span><span class="sxs-lookup"><span data-stu-id="bdae6-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="bdae6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdae6-108">Return Value</span></span>  
 <span data-ttu-id="bdae6-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="bdae6-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bdae6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdae6-110">Remarks</span></span>  
 <span data-ttu-id="bdae6-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="bdae6-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="bdae6-112">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="bdae6-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="bdae6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdae6-113">Requirements</span></span>  
 <span data-ttu-id="bdae6-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bdae6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bdae6-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bdae6-115">See Also</span></span>  
 [<span data-ttu-id="bdae6-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bdae6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
