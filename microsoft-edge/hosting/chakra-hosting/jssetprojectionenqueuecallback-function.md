---
description: Establece la devolución de llamada que se va a usar para invocar una finalización de proyección a la persona que llama obligatoria.
title: Función JsSetProjectionEnqueueCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574503"
---
# <span data-ttu-id="d781e-103">Función JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="d781e-103">JsSetProjectionEnqueueCallback Function</span></span>
<span data-ttu-id="d781e-104">Establece la devolución de llamada que se va a usar para invocar una finalización de proyección a la persona que llama obligatoria.</span><span class="sxs-lookup"><span data-stu-id="d781e-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="d781e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d781e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="d781e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d781e-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="d781e-107">Devolución de llamada que se invocará cada vez que se complete una proyección en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d781e-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="d781e-108">El contexto de la aplicación proporcionado a `projectionEnqueueContext` .</span><span class="sxs-lookup"><span data-stu-id="d781e-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="d781e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d781e-109">Return Value</span></span>  
 <span data-ttu-id="d781e-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d781e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d781e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d781e-111">Remarks</span></span>  
 <span data-ttu-id="d781e-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="d781e-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d781e-113">La llamada debe proceder de un apartamento COM diferente o de un subproceso diferente en el mismo MTA.</span><span class="sxs-lookup"><span data-stu-id="d781e-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="d781e-114">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d781e-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="d781e-115">En este momento, PInvoke no es compatible con esta API.</span><span class="sxs-lookup"><span data-stu-id="d781e-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="d781e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d781e-116">Requirements</span></span>  
 <span data-ttu-id="d781e-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d781e-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d781e-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d781e-118">See Also</span></span>  
 [<span data-ttu-id="d781e-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d781e-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)