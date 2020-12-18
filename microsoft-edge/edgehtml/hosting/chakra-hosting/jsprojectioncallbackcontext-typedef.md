---
description: El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236403"
---
# <span data-ttu-id="92678-103">Definición de tipo JsProjectionCallbackContext</span><span class="sxs-lookup"><span data-stu-id="92678-103">JsProjectionCallbackContext Typedef</span></span>

<span data-ttu-id="92678-104">El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.</span><span class="sxs-lookup"><span data-stu-id="92678-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="92678-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92678-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="92678-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92678-106">Remarks</span></span>  
 <span data-ttu-id="92678-107">Requiere `JsSetProjectionEnqueueCallback` que se llame para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="92678-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="92678-108">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="92678-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="92678-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92678-109">Requirements</span></span>  
 <span data-ttu-id="92678-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="92678-110">jsrt.h</span></span>  
  
## <span data-ttu-id="92678-111">Consulta también</span><span class="sxs-lookup"><span data-stu-id="92678-111">See Also</span></span>  
 [<span data-ttu-id="92678-112">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="92678-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
