---
description: Libera una referencia a un objeto recolectado de basura.
title: Función JsRelease | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 134ba16509b6c2f0c232214d7efba4d8c8915d43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574540"
---
# <span data-ttu-id="f34d1-103">Función JsRelease</span><span class="sxs-lookup"><span data-stu-id="f34d1-103">JsRelease Function</span></span>
<span data-ttu-id="f34d1-104">Libera una referencia a un objeto recolectado de basura.</span><span class="sxs-lookup"><span data-stu-id="f34d1-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="f34d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f34d1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="f34d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f34d1-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="f34d1-107">Objeto al que se va a agregar una referencia.</span><span class="sxs-lookup"><span data-stu-id="f34d1-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="f34d1-108">El nuevo recuento de referencia del objeto (puede pasar el valor null).</span><span class="sxs-lookup"><span data-stu-id="f34d1-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="f34d1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f34d1-109">Return Value</span></span>  
 <span data-ttu-id="f34d1-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="f34d1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f34d1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f34d1-111">Remarks</span></span>  
 <span data-ttu-id="f34d1-112">Quita una referencia a un `JsRef` controlador creado por `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="f34d1-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="f34d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f34d1-113">Requirements</span></span>  
 <span data-ttu-id="f34d1-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f34d1-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f34d1-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="f34d1-115">See Also</span></span>  
 [<span data-ttu-id="f34d1-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f34d1-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)