---
description: Obtiene el contexto de script al que pertenece el objeto.
title: Función JsGetContextOfObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4f1b996954e877d9c98ac0caf06f255af629a386
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573467"
---
# <span data-ttu-id="60150-103">Función JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="60150-103">JsGetContextOfObject Function</span></span>
<span data-ttu-id="60150-104">Obtiene el contexto de script al que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="60150-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="60150-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60150-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="60150-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60150-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="60150-107">Objeto del que se va a obtener el contexto.</span><span class="sxs-lookup"><span data-stu-id="60150-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="60150-108">El contexto al que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="60150-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="60150-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60150-109">Return Value</span></span>  
 <span data-ttu-id="60150-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="60150-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="60150-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60150-111">Remarks</span></span>  
 <span data-ttu-id="60150-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="60150-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="60150-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60150-113">Requirements</span></span>  
 <span data-ttu-id="60150-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="60150-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="60150-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="60150-115">See Also</span></span>  
 [<span data-ttu-id="60150-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="60150-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)