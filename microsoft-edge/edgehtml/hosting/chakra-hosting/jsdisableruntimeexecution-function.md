---
description: Suspende la ejecución de scripts y finaliza cualquier script que se esté ejecutando en un tiempo de ejecución.
title: Función JsDisableRuntimeExecution | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236281"
---
# <span data-ttu-id="2652c-103">Función JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="2652c-103">JsDisableRuntimeExecution Function</span></span>

<span data-ttu-id="2652c-104">Suspende la ejecución de scripts y finaliza cualquier script que se esté ejecutando en un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2652c-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="2652c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2652c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="2652c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2652c-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="2652c-107">Tiempo de ejecución que se va a suspender.</span><span class="sxs-lookup"><span data-stu-id="2652c-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="2652c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2652c-108">Return Value</span></span>  
 <span data-ttu-id="2652c-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="2652c-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2652c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2652c-110">Remarks</span></span>  
 <span data-ttu-id="2652c-111">Las llamadas a un tiempo de ejecución suspendido fallarán hasta que `JsEnableRuntimeExecution` se llame.</span><span class="sxs-lookup"><span data-stu-id="2652c-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="2652c-112">No es necesario llamar a esta API en el subproceso en el que el motor en tiempo de ejecución está activo.</span><span class="sxs-lookup"><span data-stu-id="2652c-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="2652c-113">Aunque el motor en tiempo de ejecución se establecerá en un estado suspendido, un script en ejecución no se puede suspender inmediatamente; un script en ejecución se terminará con una excepción no interceptable lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="2652c-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="2652c-114">Suspender la ejecución en un tiempo de ejecución que ya está suspendido no es de op.</span><span class="sxs-lookup"><span data-stu-id="2652c-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="2652c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2652c-115">Requirements</span></span>  
 <span data-ttu-id="2652c-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2652c-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2652c-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2652c-117">See Also</span></span>  
 [<span data-ttu-id="2652c-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2652c-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
