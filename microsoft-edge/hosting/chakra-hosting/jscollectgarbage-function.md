---
description: Realiza una recolección completa de elementos no utilizados.
title: Función JsCollectGarbage | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1702ad960a0a2f366e97b8a994abd0700cec50e7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573527"
---
# <span data-ttu-id="46e52-103">Función JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="46e52-103">JsCollectGarbage Function</span></span>
<span data-ttu-id="46e52-104">Realiza una recolección completa de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="46e52-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="46e52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46e52-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="46e52-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46e52-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="46e52-107">El motor en tiempo de ejecución en el que se realizará la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="46e52-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="46e52-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46e52-108">Return Value</span></span>  
 <span data-ttu-id="46e52-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="46e52-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="46e52-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e52-110">Requirements</span></span>  
 <span data-ttu-id="46e52-111">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="46e52-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="46e52-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="46e52-112">See Also</span></span>  
 [<span data-ttu-id="46e52-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="46e52-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)