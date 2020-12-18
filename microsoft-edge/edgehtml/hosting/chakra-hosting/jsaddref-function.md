---
description: Agrega una referencia a un objeto recolectado recolectado.
title: Función JsAddRef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236112"
---
# <span data-ttu-id="5f2ff-103">Función JsAddRef</span><span class="sxs-lookup"><span data-stu-id="5f2ff-103">JsAddRef Function</span></span>

<span data-ttu-id="5f2ff-104">Agrega una referencia a un objeto recolectado recolectado.</span><span class="sxs-lookup"><span data-stu-id="5f2ff-104">Adds a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="5f2ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f2ff-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="5f2ff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f2ff-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="5f2ff-107">Objeto al que se va a agregar una referencia.</span><span class="sxs-lookup"><span data-stu-id="5f2ff-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="5f2ff-108">El nuevo recuento de referencia del objeto (puede pasar el valor null).</span><span class="sxs-lookup"><span data-stu-id="5f2ff-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="5f2ff-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f2ff-109">Return Value</span></span>  
 <span data-ttu-id="5f2ff-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="5f2ff-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5f2ff-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f2ff-111">Remarks</span></span>  
 <span data-ttu-id="5f2ff-112">Esto solo debe llamarse en `JsRef` los identificadores que no se van a almacenar en algún lugar de la pila.</span><span class="sxs-lookup"><span data-stu-id="5f2ff-112">This only needs to be called on `JsRef` handles that are not going to be stored somewhere on the stack.</span></span> <span data-ttu-id="5f2ff-113">`JsAddRef`Las llamadas garantizan que el objeto al que `JsRef` hace referencia no se liberará hasta que `JsRelease` se llame.</span><span class="sxs-lookup"><span data-stu-id="5f2ff-113">Calling `JsAddRef` ensures that the object the `JsRef` refers to will not be freed until `JsRelease` is called.</span></span>  
  
## <span data-ttu-id="5f2ff-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f2ff-114">Requirements</span></span>  
 <span data-ttu-id="5f2ff-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5f2ff-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5f2ff-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5f2ff-116">See Also</span></span>  
 [<span data-ttu-id="5f2ff-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5f2ff-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
