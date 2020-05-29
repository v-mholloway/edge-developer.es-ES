---
description: Detiene la generación de perfiles en el contexto actual.
title: Función JsStopProfiling | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574403"
---
# <span data-ttu-id="7836c-103">Función JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="7836c-103">JsStopProfiling Function</span></span>
<span data-ttu-id="7836c-104">Detiene la generación de perfiles en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="7836c-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="7836c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7836c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="7836c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7836c-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="7836c-107">El motivo de detener la generación de perfiles para pasar a la devolución de llamada del generador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="7836c-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="7836c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7836c-108">Return Value</span></span>  
 <span data-ttu-id="7836c-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7836c-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7836c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7836c-110">Remarks</span></span>  
 <span data-ttu-id="7836c-111">No devolverá un error si la generación de perfiles no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="7836c-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="7836c-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7836c-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="7836c-113">Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="7836c-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="7836c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7836c-114">Requirements</span></span>  
 <span data-ttu-id="7836c-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7836c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7836c-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7836c-116">See Also</span></span>  
 [<span data-ttu-id="7836c-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7836c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)