---
description: La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.
title: JsProjectionCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236407"
---
# <span data-ttu-id="d1f23-103">Definición de tipo JsProjectionCallback</span><span class="sxs-lookup"><span data-stu-id="d1f23-103">JsProjectionCallback Typedef</span></span>

<span data-ttu-id="d1f23-104">La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.</span><span class="sxs-lookup"><span data-stu-id="d1f23-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="d1f23-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1f23-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="d1f23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1f23-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="d1f23-107">Requiere `JsSetProjectionEnqueueCallback` que se llame para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="d1f23-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="d1f23-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1f23-108">Remarks</span></span>  
 <span data-ttu-id="d1f23-109">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d1f23-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d1f23-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1f23-110">Requirements</span></span>  
 <span data-ttu-id="d1f23-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d1f23-111">jsrt.h</span></span>  
  
## <span data-ttu-id="d1f23-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d1f23-112">See Also</span></span>  
 [<span data-ttu-id="d1f23-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d1f23-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
