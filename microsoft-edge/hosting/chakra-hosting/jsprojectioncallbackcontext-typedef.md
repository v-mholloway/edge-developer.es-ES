---
description: El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573413"
---
# <span data-ttu-id="c60b5-103">JsProjectionCallbackContext typedef</span><span class="sxs-lookup"><span data-stu-id="c60b5-103">JsProjectionCallbackContext Typedef</span></span>
<span data-ttu-id="c60b5-104">El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.</span><span class="sxs-lookup"><span data-stu-id="c60b5-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="c60b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c60b5-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="c60b5-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c60b5-106">Remarks</span></span>  
 <span data-ttu-id="c60b5-107">Requiere `JsSetProjectionEnqueueCallback` que se llame para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="c60b5-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="c60b5-108">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="c60b5-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="c60b5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c60b5-109">Requirements</span></span>  
 <span data-ttu-id="c60b5-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c60b5-110">jsrt.h</span></span>  
  
## <span data-ttu-id="c60b5-111">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c60b5-111">See Also</span></span>  
 [<span data-ttu-id="c60b5-112">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c60b5-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)