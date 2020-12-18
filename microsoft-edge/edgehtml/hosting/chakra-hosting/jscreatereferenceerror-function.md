---
description: Crea un nuevo objeto de error ReferenceError de JavaScript.
title: Función JsCreateReferenceError | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fc8f10c443d6ca019c1460c84344bf04513e44b9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236300"
---
# <span data-ttu-id="f1ed8-103">Función JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="f1ed8-103">JsCreateReferenceError Function</span></span>

<span data-ttu-id="f1ed8-104">Crea un nuevo objeto de error ReferenceError de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f1ed8-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="f1ed8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1ed8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="f1ed8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1ed8-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="f1ed8-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="f1ed8-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="f1ed8-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="f1ed8-108">The new error object.</span></span>  
  
## <span data-ttu-id="f1ed8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1ed8-109">Return Value</span></span>  
 <span data-ttu-id="f1ed8-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="f1ed8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f1ed8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1ed8-111">Remarks</span></span>  
 <span data-ttu-id="f1ed8-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="f1ed8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f1ed8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ed8-113">Requirements</span></span>  
 <span data-ttu-id="f1ed8-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f1ed8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f1ed8-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="f1ed8-115">See Also</span></span>  
 [<span data-ttu-id="f1ed8-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f1ed8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
