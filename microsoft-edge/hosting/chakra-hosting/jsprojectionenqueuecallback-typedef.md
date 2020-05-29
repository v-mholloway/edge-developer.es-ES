---
description: Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573411"
---
# <span data-ttu-id="5c36b-103">JsProjectionEnqueueCallback typedef</span><span class="sxs-lookup"><span data-stu-id="5c36b-103">JsProjectionEnqueueCallback Typedef</span></span>
<span data-ttu-id="5c36b-104">Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.</span><span class="sxs-lookup"><span data-stu-id="5c36b-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="5c36b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c36b-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="5c36b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c36b-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="5c36b-107">Devolución de llamada que se va a invocar en el subproceso original.</span><span class="sxs-lookup"><span data-stu-id="5c36b-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="5c36b-108">El contexto de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5c36b-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="5c36b-109">El contexto de JsRT que se debe pasar `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="5c36b-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="5c36b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c36b-110">Remarks</span></span>  
 <span data-ttu-id="5c36b-111">Requiere la llamada a JsSetProjectionEnqueueCallback para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="5c36b-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="5c36b-112">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="5c36b-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="5c36b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c36b-113">Requirements</span></span>  
 <span data-ttu-id="5c36b-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5c36b-114">jsrt.h</span></span>  
  
## <span data-ttu-id="5c36b-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5c36b-115">See Also</span></span>  
 [<span data-ttu-id="5c36b-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5c36b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)