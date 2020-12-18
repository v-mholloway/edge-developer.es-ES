---
description: Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.
title: Función JsIdle | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236591"
---
# <span data-ttu-id="9c5ca-103">Función JsIdle</span><span class="sxs-lookup"><span data-stu-id="9c5ca-103">JsIdle Function</span></span>

<span data-ttu-id="9c5ca-104">Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="9c5ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c5ca-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="9c5ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c5ca-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="9c5ca-107">La siguiente marca del sistema cuando haya más trabajo de inactividad para hacer.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="9c5ca-108">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-108">Can be null.</span></span> <span data-ttu-id="9c5ca-109">Devuelve el número máximo de marcas si no hay nada de trabajo inactivo.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="9c5ca-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c5ca-110">Return Value</span></span>  
 <span data-ttu-id="9c5ca-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c5ca-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c5ca-112">Remarks</span></span>  
 <span data-ttu-id="9c5ca-113">Si se ha habilitado el procesamiento en inactividad para el tiempo de ejecución actual, las llamadas `JsIdle` informarán al tiempo de ejecución actual de que el host está inactivo y que el tiempo de ejecución puede realizar tareas de limpieza de memoria.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="9c5ca-114">también puede devolver el número de marcas del sistema hasta que haya más trabajo de inactividad para que lo haga el motor en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="9c5ca-115">Las llamadas `JsIdle` antes de que se haya pasado este número de marcas no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="9c5ca-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="9c5ca-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9c5ca-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c5ca-117">Requirements</span></span>  
 <span data-ttu-id="9c5ca-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9c5ca-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c5ca-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="9c5ca-119">See Also</span></span>  
 [<span data-ttu-id="9c5ca-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9c5ca-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
