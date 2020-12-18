---
description: Enumera el montón del contexto actual.
title: Función JsEnumerateHeap | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236427"
---
# <span data-ttu-id="72fd5-103">Función JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="72fd5-103">JsEnumerateHeap Function</span></span>

<span data-ttu-id="72fd5-104">Enumera el montón del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="72fd5-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="72fd5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72fd5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="72fd5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72fd5-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="72fd5-107">Enumerador de montones.</span><span class="sxs-lookup"><span data-stu-id="72fd5-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="72fd5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72fd5-108">Return Value</span></span>  
 <span data-ttu-id="72fd5-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="72fd5-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="72fd5-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72fd5-110">Remarks</span></span>  
 <span data-ttu-id="72fd5-111">Mientras se está enumerando el montón, no se puede quitar el contexto actual y se producirá un error en todas las llamadas para modificar el estado del contexto hasta que se libere el enumerador heap.</span><span class="sxs-lookup"><span data-stu-id="72fd5-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="72fd5-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="72fd5-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="72fd5-113">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="72fd5-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="72fd5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72fd5-114">Requirements</span></span>  
 <span data-ttu-id="72fd5-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="72fd5-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72fd5-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="72fd5-116">See Also</span></span>  
 [<span data-ttu-id="72fd5-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="72fd5-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
