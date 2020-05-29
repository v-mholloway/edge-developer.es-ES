---
description: Crea un nuevo objeto de error ReferenceError de JavaScript.
title: Función JsCreateReferenceError | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 958af7111a233077aa7a2c2391b26666f55c634b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573492"
---
# <span data-ttu-id="67424-103">Función JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="67424-103">JsCreateReferenceError Function</span></span>
<span data-ttu-id="67424-104">Crea un nuevo objeto de error ReferenceError de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="67424-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="67424-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67424-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="67424-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67424-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="67424-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="67424-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="67424-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="67424-108">The new error object.</span></span>  
  
## <span data-ttu-id="67424-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67424-109">Return Value</span></span>  
 <span data-ttu-id="67424-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="67424-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="67424-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67424-111">Remarks</span></span>  
 <span data-ttu-id="67424-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="67424-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="67424-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67424-113">Requirements</span></span>  
 <span data-ttu-id="67424-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="67424-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="67424-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="67424-115">See Also</span></span>  
 [<span data-ttu-id="67424-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="67424-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)