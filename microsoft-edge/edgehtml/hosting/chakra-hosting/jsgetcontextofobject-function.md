---
description: Obtiene el contexto de script al que pertenece el objeto.
title: Función JsGetContextOfObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9085f9156e4e0ca9e952fe51447185239082f975
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236335"
---
# <span data-ttu-id="208a9-103">Función JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="208a9-103">JsGetContextOfObject Function</span></span>

<span data-ttu-id="208a9-104">Obtiene el contexto de script al que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="208a9-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="208a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="208a9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="208a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="208a9-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="208a9-107">Objeto del que se va a obtener el contexto.</span><span class="sxs-lookup"><span data-stu-id="208a9-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="208a9-108">El contexto al que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="208a9-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="208a9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="208a9-109">Return Value</span></span>  
 <span data-ttu-id="208a9-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="208a9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="208a9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="208a9-111">Remarks</span></span>  
 <span data-ttu-id="208a9-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="208a9-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="208a9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="208a9-113">Requirements</span></span>  
 <span data-ttu-id="208a9-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="208a9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="208a9-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="208a9-115">See Also</span></span>  
 [<span data-ttu-id="208a9-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="208a9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
