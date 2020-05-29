---
description: Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.
title: Función JsSetException | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574516"
---
# <span data-ttu-id="b8bef-103">Función JsSetException</span><span class="sxs-lookup"><span data-stu-id="b8bef-103">JsSetException Function</span></span>
<span data-ttu-id="b8bef-104">Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.</span><span class="sxs-lookup"><span data-stu-id="b8bef-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="b8bef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8bef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="b8bef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8bef-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="b8bef-107">Excepción de JavaScript que se establece para el motor en tiempo de ejecución del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="b8bef-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="b8bef-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8bef-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="b8bef-109">Si el motor se ha configurado en un estado de excepción, de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b8bef-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b8bef-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8bef-110">Remarks</span></span>  
 <span data-ttu-id="b8bef-111">Si el tiempo de ejecución del contexto actual ya está en estado de excepción, esta API se devolverá `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="b8bef-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="b8bef-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b8bef-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b8bef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bef-113">Requirements</span></span>  
 <span data-ttu-id="b8bef-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b8bef-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b8bef-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b8bef-115">See Also</span></span>  
 [<span data-ttu-id="b8bef-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b8bef-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)