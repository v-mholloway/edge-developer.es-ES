---
description: Devolución de llamada del servicio de subprocesos.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236232"
---
# <span data-ttu-id="a1849-103">Definición de tipo JsThreadServiceCallback</span><span class="sxs-lookup"><span data-stu-id="a1849-103">JsThreadServiceCallback Typedef</span></span>

<span data-ttu-id="a1849-104">Devolución de llamada del servicio de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a1849-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="a1849-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1849-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="a1849-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1849-106">Parameters</span></span>  
 <span data-ttu-id="a1849-107">devolución</span><span class="sxs-lookup"><span data-stu-id="a1849-107">callback</span></span>  
 <span data-ttu-id="a1849-108">Devolución de llamada para el elemento de trabajo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a1849-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="a1849-109">Devolución</span><span class="sxs-lookup"><span data-stu-id="a1849-109">callbackData</span></span>  
 <span data-ttu-id="a1849-110">El argumento de datos que se va a pasar a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a1849-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="a1849-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1849-111">Remarks</span></span>  
 <span data-ttu-id="a1849-112">El host puede especificar un servicio de subproceso en segundo plano al llamar a JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="a1849-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="a1849-113">Si se especifica, los elementos de trabajo de fondo se pasarán al host mediante esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a1849-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="a1849-114">Se espera que el host empiece a ejecutar el elemento de trabajo de fondo inmediatamente y devuelva true o devuelva false, y el tiempo de ejecución controlará el elemento de trabajo de subproceso.</span><span class="sxs-lookup"><span data-stu-id="a1849-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="a1849-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1849-115">Requirements</span></span>  
 <span data-ttu-id="a1849-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a1849-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a1849-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a1849-117">See Also</span></span>  
 [<span data-ttu-id="a1849-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a1849-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
