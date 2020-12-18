---
description: Realiza una recolección completa de elementos no utilizados.
title: Función JsCollectGarbage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c551ddf119ec0aa349fcd756f6001d92dbbb0faa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236096"
---
# <span data-ttu-id="150c0-103">Función JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="150c0-103">JsCollectGarbage Function</span></span>

<span data-ttu-id="150c0-104">Realiza una recolección completa de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="150c0-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="150c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="150c0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="150c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="150c0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="150c0-107">El motor en tiempo de ejecución en el que se realizará la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="150c0-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="150c0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="150c0-108">Return Value</span></span>  
 <span data-ttu-id="150c0-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="150c0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="150c0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="150c0-110">Requirements</span></span>  
 <span data-ttu-id="150c0-111">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="150c0-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="150c0-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="150c0-112">See Also</span></span>  
 [<span data-ttu-id="150c0-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="150c0-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
