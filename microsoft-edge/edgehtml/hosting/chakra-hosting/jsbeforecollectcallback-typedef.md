---
description: Una devolución de llamada llamada antes de la colección.
title: JsBeforeCollectCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236101"
---
# <span data-ttu-id="bb7c9-103">Definición de tipo JsBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="bb7c9-103">JsBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="bb7c9-104">Una devolución de llamada llamada antes de la colección.</span><span class="sxs-lookup"><span data-stu-id="bb7c9-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="bb7c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb7c9-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="bb7c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb7c9-106">Parameters</span></span>  
 <span data-ttu-id="bb7c9-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="bb7c9-107">callbackState</span></span>  
 <span data-ttu-id="bb7c9-108">El estado pasado a JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="bb7c9-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="bb7c9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb7c9-109">Remarks</span></span>  
 <span data-ttu-id="bb7c9-110">Usa JsSetBeforeCollectCallback para registrar esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bb7c9-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="bb7c9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb7c9-111">Requirements</span></span>  
 <span data-ttu-id="bb7c9-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bb7c9-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bb7c9-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bb7c9-113">See Also</span></span>  
 [<span data-ttu-id="bb7c9-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bb7c9-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
