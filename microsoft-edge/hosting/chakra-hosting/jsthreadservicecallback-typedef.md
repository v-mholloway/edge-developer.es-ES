---
description: Devolución de llamada del servicio de subprocesos.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573403"
---
# <span data-ttu-id="0f76a-103">JsThreadServiceCallback typedef</span><span class="sxs-lookup"><span data-stu-id="0f76a-103">JsThreadServiceCallback Typedef</span></span>
<span data-ttu-id="0f76a-104">Devolución de llamada del servicio de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0f76a-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="0f76a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f76a-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="0f76a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f76a-106">Parameters</span></span>  
 <span data-ttu-id="0f76a-107">devolución</span><span class="sxs-lookup"><span data-stu-id="0f76a-107">callback</span></span>  
 <span data-ttu-id="0f76a-108">Devolución de llamada para el elemento de trabajo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0f76a-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="0f76a-109">Devolución</span><span class="sxs-lookup"><span data-stu-id="0f76a-109">callbackData</span></span>  
 <span data-ttu-id="0f76a-110">El argumento de datos que se va a pasar a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0f76a-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="0f76a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f76a-111">Remarks</span></span>  
 <span data-ttu-id="0f76a-112">El host puede especificar un servicio de subproceso en segundo plano al llamar a JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="0f76a-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="0f76a-113">Si se especifica, los elementos de trabajo de fondo se pasarán al host mediante esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0f76a-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="0f76a-114">Se espera que el host empiece a ejecutar el elemento de trabajo de fondo inmediatamente y devuelva true o devuelva false, y el tiempo de ejecución controlará el elemento de trabajo de subproceso.</span><span class="sxs-lookup"><span data-stu-id="0f76a-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="0f76a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f76a-115">Requirements</span></span>  
 <span data-ttu-id="0f76a-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f76a-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f76a-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0f76a-117">See Also</span></span>  
 [<span data-ttu-id="0f76a-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f76a-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)