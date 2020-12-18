---
description: Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.
title: Función JsSetException | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236277"
---
# <span data-ttu-id="5c6c0-103">Función JsSetException</span><span class="sxs-lookup"><span data-stu-id="5c6c0-103">JsSetException Function</span></span>

<span data-ttu-id="5c6c0-104">Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="5c6c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c6c0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="5c6c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c6c0-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="5c6c0-107">Excepción de JavaScript que se establece para el motor en tiempo de ejecución del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="5c6c0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c6c0-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="5c6c0-109">Si el motor se ha configurado en un estado de excepción, de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5c6c0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c6c0-110">Remarks</span></span>  
 <span data-ttu-id="5c6c0-111">Si el tiempo de ejecución del contexto actual ya está en estado de excepción, esta API se devolverá `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="5c6c0-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="5c6c0-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5c6c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c6c0-113">Requirements</span></span>  
 <span data-ttu-id="5c6c0-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5c6c0-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5c6c0-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5c6c0-115">See Also</span></span>  
 [<span data-ttu-id="5c6c0-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5c6c0-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
