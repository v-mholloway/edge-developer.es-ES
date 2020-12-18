---
description: Detiene la generación de perfiles en el contexto actual.
title: Función JsStopProfiling | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236271"
---
# <span data-ttu-id="6cc5a-103">Función JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="6cc5a-103">JsStopProfiling Function</span></span>

<span data-ttu-id="6cc5a-104">Detiene la generación de perfiles en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="6cc5a-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="6cc5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cc5a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="6cc5a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cc5a-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="6cc5a-107">El motivo de detener la generación de perfiles para pasar a la devolución de llamada del generador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="6cc5a-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="6cc5a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cc5a-108">Return Value</span></span>  
 <span data-ttu-id="6cc5a-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6cc5a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6cc5a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cc5a-110">Remarks</span></span>  
 <span data-ttu-id="6cc5a-111">No devolverá un error si la generación de perfiles no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="6cc5a-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="6cc5a-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="6cc5a-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6cc5a-113">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="6cc5a-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="6cc5a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cc5a-114">Requirements</span></span>  
 <span data-ttu-id="6cc5a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6cc5a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6cc5a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6cc5a-116">See Also</span></span>  
 [<span data-ttu-id="6cc5a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6cc5a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
