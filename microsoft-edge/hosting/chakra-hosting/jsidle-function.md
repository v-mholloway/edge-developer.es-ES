---
description: Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.
title: Función JsIdle | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574559"
---
# <span data-ttu-id="00afd-103">Función JsIdle</span><span class="sxs-lookup"><span data-stu-id="00afd-103">JsIdle Function</span></span>
<span data-ttu-id="00afd-104">Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.</span><span class="sxs-lookup"><span data-stu-id="00afd-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="00afd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00afd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="00afd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00afd-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="00afd-107">La siguiente marca del sistema cuando haya más trabajo de inactividad para hacer.</span><span class="sxs-lookup"><span data-stu-id="00afd-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="00afd-108">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="00afd-108">Can be null.</span></span> <span data-ttu-id="00afd-109">Devuelve el número máximo de marcas si no hay nada de trabajo inactivo.</span><span class="sxs-lookup"><span data-stu-id="00afd-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="00afd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00afd-110">Return Value</span></span>  
 <span data-ttu-id="00afd-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="00afd-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="00afd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00afd-112">Remarks</span></span>  
 <span data-ttu-id="00afd-113">Si se ha habilitado el procesamiento en inactividad para el tiempo de ejecución actual, las llamadas `JsIdle` informarán al tiempo de ejecución actual de que el host está inactivo y que el tiempo de ejecución puede realizar tareas de limpieza de memoria.</span><span class="sxs-lookup"><span data-stu-id="00afd-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="00afd-114">también puede devolver el número de marcas del sistema hasta que haya más trabajo de inactividad para que lo haga el motor en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="00afd-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="00afd-115">Las llamadas `JsIdle` antes de que se haya pasado este número de marcas no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="00afd-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="00afd-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="00afd-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="00afd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00afd-117">Requirements</span></span>  
 <span data-ttu-id="00afd-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="00afd-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="00afd-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="00afd-119">See Also</span></span>  
 [<span data-ttu-id="00afd-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="00afd-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)