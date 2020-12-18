---
description: Se deshace de un tiempo de ejecución.
title: Función JsDisposeRuntime | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236282"
---
# <span data-ttu-id="46ed3-103">Función JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="46ed3-103">JsDisposeRuntime Function</span></span>

<span data-ttu-id="46ed3-104">Se deshace de un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="46ed3-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="46ed3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46ed3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="46ed3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46ed3-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="46ed3-107">El Runtime que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="46ed3-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="46ed3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46ed3-108">Return Value</span></span>  
 <span data-ttu-id="46ed3-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="46ed3-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="46ed3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46ed3-110">Remarks</span></span>  
 <span data-ttu-id="46ed3-111">Una vez que se ha eliminado un Runtime, todos los recursos que es propiedad de él no son válidos y no se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="46ed3-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="46ed3-112">Si el motor en tiempo de ejecución está activo (es decir, está configurado para ser actual en un determinado subproceso), no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="46ed3-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="46ed3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46ed3-113">Requirements</span></span>  
 <span data-ttu-id="46ed3-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="46ed3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="46ed3-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="46ed3-115">See Also</span></span>  
 [<span data-ttu-id="46ed3-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="46ed3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
