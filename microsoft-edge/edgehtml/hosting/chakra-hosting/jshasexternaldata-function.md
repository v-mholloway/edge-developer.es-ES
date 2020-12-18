---
description: Determina si un objeto es un objeto externo.
title: Función JsHasExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d73333215a33fc409190a0e33fa616b6350fb2a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235940"
---
# <span data-ttu-id="e1f32-103">Función JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="e1f32-103">JsHasExternalData Function</span></span>

<span data-ttu-id="e1f32-104">Determina si un objeto es un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e1f32-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="e1f32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1f32-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="e1f32-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1f32-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e1f32-107">El objeto.</span><span class="sxs-lookup"><span data-stu-id="e1f32-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="e1f32-108">Si el objeto es un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e1f32-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="e1f32-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1f32-109">Return Value</span></span>  
 <span data-ttu-id="e1f32-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e1f32-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e1f32-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1f32-111">Remarks</span></span>  
 <span data-ttu-id="e1f32-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e1f32-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e1f32-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1f32-113">Requirements</span></span>  
 <span data-ttu-id="e1f32-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1f32-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1f32-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e1f32-115">See Also</span></span>  
 [<span data-ttu-id="e1f32-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e1f32-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
