---
description: Crea un nuevo objeto de error RangeError de JavaScript.
title: Función JsCreateRangeError | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3759f1c04a2eb13488f756ae2c135373d9db1f74
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573494"
---
# <span data-ttu-id="91bb2-103">Función JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="91bb2-103">JsCreateRangeError Function</span></span>
<span data-ttu-id="91bb2-104">Crea un nuevo objeto de error RangeError de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="91bb2-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="91bb2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91bb2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="91bb2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91bb2-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="91bb2-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="91bb2-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="91bb2-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="91bb2-108">The new error object.</span></span>  
  
## <span data-ttu-id="91bb2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91bb2-109">Return Value</span></span>  
 <span data-ttu-id="91bb2-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="91bb2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="91bb2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91bb2-111">Remarks</span></span>  
 <span data-ttu-id="91bb2-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="91bb2-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="91bb2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91bb2-113">Requirements</span></span>  
 <span data-ttu-id="91bb2-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="91bb2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="91bb2-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="91bb2-115">See Also</span></span>  
 [<span data-ttu-id="91bb2-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="91bb2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)