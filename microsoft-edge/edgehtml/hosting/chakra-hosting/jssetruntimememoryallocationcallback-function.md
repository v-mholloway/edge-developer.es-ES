---
description: Establece una devolución de llamada de asignación de memoria para el tiempo de ejecución especificado.
title: Función JsSetRuntimeMemoryAllocationCallback | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ee2abf36e14c26ac58b90d48a6115fd6502307c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236236"
---
# <span data-ttu-id="73728-103">Función JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="73728-103">JsSetRuntimeMemoryAllocationCallback Function</span></span>

<span data-ttu-id="73728-104">Establece una devolución de llamada de asignación de memoria para el tiempo de ejecución especificado.</span><span class="sxs-lookup"><span data-stu-id="73728-104">Sets a memory allocation callback for specified runtime.</span></span>  
  
## <span data-ttu-id="73728-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73728-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### <span data-ttu-id="73728-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73728-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="73728-107">Motor en tiempo de ejecución para el que se va a registrar la devolución de llamada de asignación.</span><span class="sxs-lookup"><span data-stu-id="73728-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="73728-108">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="73728-108">User provided state that will be passed back to the callback.</span></span>  
  
 `allocationCallback`  
 <span data-ttu-id="73728-109">Devolución de llamada de asignación de memoria que se va a llamar para eventos de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="73728-109">Memory allocation callback to be called for memory allocation events.</span></span>  
  
## <span data-ttu-id="73728-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73728-110">Return Value</span></span>  
 <span data-ttu-id="73728-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="73728-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="73728-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73728-112">Remarks</span></span>  
 <span data-ttu-id="73728-113">El registro de una devolución de llamada de asignación de memoria hará que el motor en tiempo de ejecución devuelva la llamada al host siempre que adquiera memoria o libere memoria para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73728-113">Registering a memory allocation callback will cause the runtime to call back to the host whenever it acquires memory from, or releases memory to, the OS.</span></span> <span data-ttu-id="73728-114">Se llama a la rutina de devolución de llamada antes de que el administrador de memoria en tiempo de ejecución asigne un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="73728-114">The callback routine is called before the runtime memory manager allocates a block of memory.</span></span> <span data-ttu-id="73728-115">La asignación se rechazará si la devolución de llamada devuelve false.</span><span class="sxs-lookup"><span data-stu-id="73728-115">The allocation will be rejected if the callback returns false.</span></span> <span data-ttu-id="73728-116">El administrador de memoria en tiempo de ejecución también invocará la rutina de devolución de llamada después de liberar un bloque de memoria, así como después de que se produzcan errores de asignación.</span><span class="sxs-lookup"><span data-stu-id="73728-116">The runtime memory manager will also invoke the callback routine after freeing a block of memory, as well as after allocation failures.</span></span>  
  
 <span data-ttu-id="73728-117">La devolución de llamada se invoca en el actual subproceso de ejecución en tiempo de ejecución; por lo tanto, la ejecución se bloquea hasta que se completa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="73728-117">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="73728-118">El valor devuelto de la devolución de llamada no se almacena; las asignaciones rechazadas previamente no impiden que el motor en tiempo de ejecución invoque la devolución de llamada más adelante para nuevas asignaciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="73728-118">The return value of the callback is not stored; previously rejected allocations will not prevent the runtime from invoking the callback again later for new memory allocations.</span></span>  
  
## <span data-ttu-id="73728-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73728-119">Requirements</span></span>  
 <span data-ttu-id="73728-120">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="73728-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="73728-121">Consulta también</span><span class="sxs-lookup"><span data-stu-id="73728-121">See Also</span></span>  
 [<span data-ttu-id="73728-122">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="73728-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
