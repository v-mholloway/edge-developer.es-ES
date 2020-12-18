---
description: Una devolución de llamada de elemento de trabajo en segundo plano.
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236110"
---
# <span data-ttu-id="ad92e-103">Definición de tipo JsBackgroundWorkItemCallback</span><span class="sxs-lookup"><span data-stu-id="ad92e-103">JsBackgroundWorkItemCallback Typedef</span></span>

<span data-ttu-id="ad92e-104">Una devolución de llamada de elemento de trabajo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ad92e-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="ad92e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad92e-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="ad92e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad92e-106">Parameters</span></span>  
 <span data-ttu-id="ad92e-107">Devolución</span><span class="sxs-lookup"><span data-stu-id="ad92e-107">callbackData</span></span>  
 <span data-ttu-id="ad92e-108">Argumento de datos pasado al servicio de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ad92e-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="ad92e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad92e-109">Remarks</span></span>  
 <span data-ttu-id="ad92e-110">Este pasa al servicio de subprocesos del host (si se proporciona) para permitir que el host llame a la devolución de llamada del elemento de trabajo en el subproceso de fondo de su elección.</span><span class="sxs-lookup"><span data-stu-id="ad92e-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="ad92e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad92e-111">Requirements</span></span>  
 <span data-ttu-id="ad92e-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ad92e-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ad92e-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ad92e-113">See Also</span></span>  
 [<span data-ttu-id="ad92e-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ad92e-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
