---
description: Devuelve la excepción que causó que el runtime del contexto actual esté en estado de excepción y restablece el estado de excepción de ese Runtime.
title: Función JsGetAndClearException | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: eb70b4b66b4bb270d9f26487708720efddc2effa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574599"
---
# <span data-ttu-id="81d84-103">Función JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="81d84-103">JsGetAndClearException Function</span></span>
<span data-ttu-id="81d84-104">Devuelve la excepción que causó que el runtime del contexto actual esté en estado de excepción y restablece el estado de excepción de ese Runtime.</span><span class="sxs-lookup"><span data-stu-id="81d84-104">Returns the exception that caused the runtime of the current context to be in the exception state and resets the exception state for that runtime.</span></span>  
  
## <span data-ttu-id="81d84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81d84-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### <span data-ttu-id="81d84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81d84-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="81d84-107">Excepción para el motor en tiempo de ejecución del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="81d84-107">The exception for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="81d84-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81d84-108">Return Value</span></span>  
 <span data-ttu-id="81d84-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="81d84-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="81d84-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81d84-110">Remarks</span></span>  
 <span data-ttu-id="81d84-111">Si el tiempo de ejecución del contexto actual no está en un estado de excepción, esta API devolverá `JsErrorInvalidArgument` .</span><span class="sxs-lookup"><span data-stu-id="81d84-111">If the runtime of the current context is not in an exception state, this API will return `JsErrorInvalidArgument`.</span></span> <span data-ttu-id="81d84-112">Si el motor en tiempo de ejecución está deshabilitado, devolverá una excepción que indica que el script ha finalizado, pero no borrará la excepción (la excepción se borrará si el motor en tiempo de ejecución se vuelve a habilitar con el `JsEnableRuntimeExecution` ).</span><span class="sxs-lookup"><span data-stu-id="81d84-112">If the runtime is disabled, this will return an exception indicating that the script was terminated, but it will not clear the exception (the exception will be cleared if the runtime is re-enabled using `JsEnableRuntimeExecution`).</span></span>  
  
 <span data-ttu-id="81d84-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="81d84-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="81d84-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81d84-114">Requirements</span></span>  
 <span data-ttu-id="81d84-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="81d84-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="81d84-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="81d84-116">See Also</span></span>  
 [<span data-ttu-id="81d84-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="81d84-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)