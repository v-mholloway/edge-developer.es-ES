---
description: Enumera el montón del contexto actual.
title: Función JsEnumerateHeap | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f1c2590388fcc09b641e3908d45eef7271bcb1ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574607"
---
# <span data-ttu-id="fe909-103">Función JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="fe909-103">JsEnumerateHeap Function</span></span>
<span data-ttu-id="fe909-104">Enumera el montón del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="fe909-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="fe909-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe909-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="fe909-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe909-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="fe909-107">Enumerador de montones.</span><span class="sxs-lookup"><span data-stu-id="fe909-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="fe909-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe909-108">Return Value</span></span>  
 <span data-ttu-id="fe909-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="fe909-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fe909-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe909-110">Remarks</span></span>  
 <span data-ttu-id="fe909-111">Mientras se está enumerando el montón, no se puede quitar el contexto actual y se producirá un error en todas las llamadas para modificar el estado del contexto hasta que se libere el enumerador heap.</span><span class="sxs-lookup"><span data-stu-id="fe909-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="fe909-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="fe909-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="fe909-113">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="fe909-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="fe909-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe909-114">Requirements</span></span>  
 <span data-ttu-id="fe909-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fe909-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fe909-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fe909-116">See Also</span></span>  
 [<span data-ttu-id="fe909-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fe909-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)