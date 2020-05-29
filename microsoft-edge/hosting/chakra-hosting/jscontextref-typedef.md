---
description: Una referencia a un contexto de script.
title: JsContextRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573524"
---
# <span data-ttu-id="8c9a2-103">JsContextRef typedef</span><span class="sxs-lookup"><span data-stu-id="8c9a2-103">JsContextRef Typedef</span></span>
<span data-ttu-id="8c9a2-104">Una referencia a un contexto de script.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="8c9a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c9a2-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="8c9a2-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c9a2-106">Remarks</span></span>  
 <span data-ttu-id="8c9a2-107">Cada contexto de script contiene su propio objeto global, distinto del objeto global en otros contextos de script.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="8c9a2-108">Muchas API de hospedaje de Chakra requieren un contexto de script "activo", que se puede establecer mediante `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="8c9a2-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="8c9a2-109">Las API de hospedaje de Chakra que requieren un contexto actual se encontrarán en la documentación de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="8c9a2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c9a2-110">Requirements</span></span>  
 <span data-ttu-id="8c9a2-111">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8c9a2-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8c9a2-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8c9a2-112">See Also</span></span>  
 [<span data-ttu-id="8c9a2-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8c9a2-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)