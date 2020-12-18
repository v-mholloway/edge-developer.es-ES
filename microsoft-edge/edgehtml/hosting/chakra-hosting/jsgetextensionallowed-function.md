---
description: Devuelve un valor que indica si un objeto es extensible o no.
title: Función JsGetExtensionAllowed | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7bc9e3265b48a27d0da4bc4646b2b5e3b1765b86
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236325"
---
# <span data-ttu-id="75444-103">Función JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="75444-103">JsGetExtensionAllowed Function</span></span>

<span data-ttu-id="75444-104">Devuelve un valor que indica si un objeto es extensible o no.</span><span class="sxs-lookup"><span data-stu-id="75444-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="75444-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75444-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="75444-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75444-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="75444-107">Objeto que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="75444-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="75444-108">Si el objeto es extensible o no.</span><span class="sxs-lookup"><span data-stu-id="75444-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="75444-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75444-109">Return Value</span></span>  
 <span data-ttu-id="75444-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="75444-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="75444-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75444-111">Remarks</span></span>  
 <span data-ttu-id="75444-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="75444-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="75444-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75444-113">Requirements</span></span>  
 <span data-ttu-id="75444-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="75444-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="75444-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="75444-115">See Also</span></span>  
 [<span data-ttu-id="75444-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="75444-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
