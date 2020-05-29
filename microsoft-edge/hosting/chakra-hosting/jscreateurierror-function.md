---
description: Crea un objeto de error JavaScript URIError.
title: Función JsCreateURIError | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5188827cd0b89b1dd6b54af005f6e118c4ae4c94
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573479"
---
# <span data-ttu-id="ab731-103">Función JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="ab731-103">JsCreateURIError Function</span></span>
<span data-ttu-id="ab731-104">Crea un objeto de error JavaScript URIError.</span><span class="sxs-lookup"><span data-stu-id="ab731-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="ab731-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab731-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="ab731-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab731-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="ab731-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="ab731-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="ab731-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="ab731-108">The new error object.</span></span>  
  
## <span data-ttu-id="ab731-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab731-109">Return Value</span></span>  
 <span data-ttu-id="ab731-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ab731-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ab731-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab731-111">Remarks</span></span>  
 <span data-ttu-id="ab731-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="ab731-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ab731-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab731-113">Requirements</span></span>  
 <span data-ttu-id="ab731-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ab731-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ab731-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ab731-115">See Also</span></span>  
 [<span data-ttu-id="ab731-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ab731-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)