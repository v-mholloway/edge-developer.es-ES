---
description: Una referencia a un contexto de script.
title: JsContextRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236099"
---
# <span data-ttu-id="b8d8d-103">Definición de tipo JsContextRef</span><span class="sxs-lookup"><span data-stu-id="b8d8d-103">JsContextRef Typedef</span></span>

<span data-ttu-id="b8d8d-104">Una referencia a un contexto de script.</span><span class="sxs-lookup"><span data-stu-id="b8d8d-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="b8d8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8d8d-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="b8d8d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8d8d-106">Remarks</span></span>  
 <span data-ttu-id="b8d8d-107">Cada contexto de script contiene su propio objeto global, distinto del objeto global en otros contextos de script.</span><span class="sxs-lookup"><span data-stu-id="b8d8d-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="b8d8d-108">Muchas API de hospedaje de Chakra requieren un contexto de script "activo", que se puede establecer mediante `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="b8d8d-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="b8d8d-109">Las API de hospedaje de Chakra que requieren un contexto actual se encontrarán en la documentación de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="b8d8d-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="b8d8d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d8d-110">Requirements</span></span>  
 <span data-ttu-id="b8d8d-111">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b8d8d-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b8d8d-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b8d8d-112">See Also</span></span>  
 [<span data-ttu-id="b8d8d-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b8d8d-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
