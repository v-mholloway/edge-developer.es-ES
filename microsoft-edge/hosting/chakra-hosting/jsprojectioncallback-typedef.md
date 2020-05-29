---
description: La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.
title: JsProjectionCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573412"
---
# <span data-ttu-id="32605-103">JsProjectionCallback typedef</span><span class="sxs-lookup"><span data-stu-id="32605-103">JsProjectionCallback Typedef</span></span>
<span data-ttu-id="32605-104">La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.</span><span class="sxs-lookup"><span data-stu-id="32605-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="32605-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32605-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="32605-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32605-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="32605-107">Requiere `JsSetProjectionEnqueueCallback` que se llame para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="32605-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="32605-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32605-108">Remarks</span></span>  
 <span data-ttu-id="32605-109">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="32605-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="32605-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32605-110">Requirements</span></span>  
 <span data-ttu-id="32605-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="32605-111">jsrt.h</span></span>  
  
## <span data-ttu-id="32605-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="32605-112">See Also</span></span>  
 [<span data-ttu-id="32605-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="32605-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)