---
description: Crea una nueva función de JavaScript con el nombre.
title: Función JsCreateNamedFunction | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573497"
---
# <span data-ttu-id="1ef83-103">Función JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="1ef83-103">JsCreateNamedFunction Function</span></span>
<span data-ttu-id="1ef83-104">Crea una nueva función de JavaScript con el nombre.</span><span class="sxs-lookup"><span data-stu-id="1ef83-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="1ef83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ef83-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="1ef83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ef83-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="1ef83-107">El nombre de esta función que se usará para propósitos de diagnóstico y stringification.</span><span class="sxs-lookup"><span data-stu-id="1ef83-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="1ef83-108">El método al que se llama cuando se invoca la función.</span><span class="sxs-lookup"><span data-stu-id="1ef83-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="1ef83-109">Estado proporcionado por el usuario que se devolverá a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1ef83-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="1ef83-110">El nuevo objeto de función.</span><span class="sxs-lookup"><span data-stu-id="1ef83-110">The new function object.</span></span>  
  
## <span data-ttu-id="1ef83-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ef83-111">Return Value</span></span>  
  
## <span data-ttu-id="1ef83-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ef83-112">Remarks</span></span>  
 <span data-ttu-id="1ef83-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="1ef83-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1ef83-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ef83-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="1ef83-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ef83-115">Requirements</span></span>  
 <span data-ttu-id="1ef83-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ef83-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ef83-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="1ef83-117">See Also</span></span>  
 [<span data-ttu-id="1ef83-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1ef83-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)