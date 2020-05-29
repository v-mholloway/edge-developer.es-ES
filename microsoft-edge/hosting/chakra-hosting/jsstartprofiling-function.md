---
description: Inicia la generación de perfiles en el contexto actual.
title: Función JsStartProfiling | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 891c39305e08d214a8f06b680c7022683a9d6fe4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574404"
---
# <span data-ttu-id="8792d-103">Función JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="8792d-103">JsStartProfiling Function</span></span>
<span data-ttu-id="8792d-104">Inicia la generación de perfiles en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="8792d-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="8792d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8792d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="8792d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8792d-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="8792d-107">Devolución de llamada de perfilado que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="8792d-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="8792d-108">Eventos de generación de perfiles con los que se va a devolver la llamada.</span><span class="sxs-lookup"><span data-stu-id="8792d-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="8792d-109">Contexto que se va a pasar a la devolución de llamada de perfilado.</span><span class="sxs-lookup"><span data-stu-id="8792d-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="8792d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8792d-110">Return Value</span></span>  
 <span data-ttu-id="8792d-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="8792d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8792d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8792d-112">Remarks</span></span>  
 <span data-ttu-id="8792d-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="8792d-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="8792d-114">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="8792d-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="8792d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8792d-115">Requirements</span></span>  
 <span data-ttu-id="8792d-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8792d-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8792d-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8792d-117">See Also</span></span>  
 [<span data-ttu-id="8792d-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8792d-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)