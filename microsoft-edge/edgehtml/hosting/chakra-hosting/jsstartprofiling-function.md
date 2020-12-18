---
description: Inicia la generación de perfiles en el contexto actual.
title: Función JsStartProfiling | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 332ff04a987e6e7ae5030983af96dd48249e58e2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236270"
---
# <span data-ttu-id="d84f8-103">Función JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="d84f8-103">JsStartProfiling Function</span></span>

<span data-ttu-id="d84f8-104">Inicia la generación de perfiles en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="d84f8-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="d84f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d84f8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="d84f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d84f8-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="d84f8-107">Devolución de llamada de perfilado que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d84f8-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="d84f8-108">Eventos de generación de perfiles con los que se va a devolver la llamada.</span><span class="sxs-lookup"><span data-stu-id="d84f8-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="d84f8-109">Contexto que se va a pasar a la devolución de llamada de perfilado.</span><span class="sxs-lookup"><span data-stu-id="d84f8-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="d84f8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d84f8-110">Return Value</span></span>  
 <span data-ttu-id="d84f8-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d84f8-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d84f8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d84f8-112">Remarks</span></span>  
 <span data-ttu-id="d84f8-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="d84f8-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d84f8-114">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="d84f8-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="d84f8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d84f8-115">Requirements</span></span>  
 <span data-ttu-id="d84f8-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d84f8-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d84f8-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d84f8-117">See Also</span></span>  
 [<span data-ttu-id="d84f8-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d84f8-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
