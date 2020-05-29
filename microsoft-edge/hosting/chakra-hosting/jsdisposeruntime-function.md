---
description: Se deshace de un tiempo de ejecución.
title: Función JsDisposeRuntime | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 89166249616c265ce75ebc43a01c838d607bdd08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574609"
---
# <span data-ttu-id="7235c-103">Función JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="7235c-103">JsDisposeRuntime Function</span></span>
<span data-ttu-id="7235c-104">Se deshace de un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7235c-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="7235c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7235c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="7235c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7235c-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="7235c-107">El Runtime que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="7235c-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="7235c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7235c-108">Return Value</span></span>  
 <span data-ttu-id="7235c-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7235c-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7235c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7235c-110">Remarks</span></span>  
 <span data-ttu-id="7235c-111">Una vez que se ha eliminado un Runtime, todos los recursos que es propiedad de él no son válidos y no se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="7235c-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="7235c-112">Si el motor en tiempo de ejecución está activo (es decir, está configurado para ser actual en un determinado subproceso), no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="7235c-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="7235c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7235c-113">Requirements</span></span>  
 <span data-ttu-id="7235c-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7235c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7235c-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7235c-115">See Also</span></span>  
 [<span data-ttu-id="7235c-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7235c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)