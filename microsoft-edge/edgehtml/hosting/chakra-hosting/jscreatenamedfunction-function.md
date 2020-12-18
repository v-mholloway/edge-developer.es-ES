---
description: Crea una nueva función de JavaScript con el nombre.
title: Función JsCreateNamedFunction | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236218"
---
# <span data-ttu-id="2be6f-103">Función JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="2be6f-103">JsCreateNamedFunction Function</span></span>

<span data-ttu-id="2be6f-104">Crea una nueva función de JavaScript con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2be6f-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="2be6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2be6f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="2be6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2be6f-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="2be6f-107">El nombre de esta función que se usará para propósitos de diagnóstico y stringification.</span><span class="sxs-lookup"><span data-stu-id="2be6f-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="2be6f-108">El método al que se llama cuando se invoca la función.</span><span class="sxs-lookup"><span data-stu-id="2be6f-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="2be6f-109">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2be6f-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="2be6f-110">El nuevo objeto de función.</span><span class="sxs-lookup"><span data-stu-id="2be6f-110">The new function object.</span></span>  
  
## <span data-ttu-id="2be6f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2be6f-111">Return Value</span></span>  
  
## <span data-ttu-id="2be6f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2be6f-112">Remarks</span></span>  
 <span data-ttu-id="2be6f-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="2be6f-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2be6f-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2be6f-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="2be6f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be6f-115">Requirements</span></span>  
 <span data-ttu-id="2be6f-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2be6f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2be6f-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2be6f-117">See Also</span></span>  
 [<span data-ttu-id="2be6f-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2be6f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
