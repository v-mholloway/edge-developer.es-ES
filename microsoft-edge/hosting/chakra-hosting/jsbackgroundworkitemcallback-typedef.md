---
description: Una devolución de llamada de elemento de trabajo en segundo plano.
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573537"
---
# <span data-ttu-id="dd9ed-103">JsBackgroundWorkItemCallback typedef</span><span class="sxs-lookup"><span data-stu-id="dd9ed-103">JsBackgroundWorkItemCallback Typedef</span></span>
<span data-ttu-id="dd9ed-104">Una devolución de llamada de elemento de trabajo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="dd9ed-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="dd9ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd9ed-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="dd9ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd9ed-106">Parameters</span></span>  
 <span data-ttu-id="dd9ed-107">Devolución</span><span class="sxs-lookup"><span data-stu-id="dd9ed-107">callbackData</span></span>  
 <span data-ttu-id="dd9ed-108">Argumento de datos pasado al servicio de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dd9ed-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="dd9ed-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd9ed-109">Remarks</span></span>  
 <span data-ttu-id="dd9ed-110">Este pasa al servicio de subprocesos del host (si se proporciona) para permitir que el host llame a la devolución de llamada del elemento de trabajo en el subproceso de fondo de su elección.</span><span class="sxs-lookup"><span data-stu-id="dd9ed-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="dd9ed-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd9ed-111">Requirements</span></span>  
 <span data-ttu-id="dd9ed-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dd9ed-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dd9ed-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dd9ed-113">See Also</span></span>  
 [<span data-ttu-id="dd9ed-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dd9ed-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)