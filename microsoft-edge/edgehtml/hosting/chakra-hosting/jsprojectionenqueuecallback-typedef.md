---
description: Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236642"
---
# <span data-ttu-id="a4527-103">Definición de tipo JsProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="a4527-103">JsProjectionEnqueueCallback Typedef</span></span>

<span data-ttu-id="a4527-104">Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.</span><span class="sxs-lookup"><span data-stu-id="a4527-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="a4527-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4527-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="a4527-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4527-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="a4527-107">Devolución de llamada que se va a invocar en el subproceso original.</span><span class="sxs-lookup"><span data-stu-id="a4527-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="a4527-108">El contexto de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a4527-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="a4527-109">El contexto de JsRT que se debe pasar `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="a4527-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="a4527-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4527-110">Remarks</span></span>  
 <span data-ttu-id="a4527-111">Requiere la llamada a JsSetProjectionEnqueueCallback para recibir devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="a4527-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="a4527-112">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="a4527-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="a4527-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4527-113">Requirements</span></span>  
 <span data-ttu-id="a4527-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a4527-114">jsrt.h</span></span>  
  
## <span data-ttu-id="a4527-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a4527-115">See Also</span></span>  
 [<span data-ttu-id="a4527-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a4527-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
