---
description: Crea un objeto de error JavaScript URIError.
title: Función JsCreateURIError | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88e6c1fc04607b3be088e297d1fa86f9374bcb03
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236217"
---
# <span data-ttu-id="0aa9d-103">Función JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="0aa9d-103">JsCreateURIError Function</span></span>

<span data-ttu-id="0aa9d-104">Crea un objeto de error JavaScript URIError.</span><span class="sxs-lookup"><span data-stu-id="0aa9d-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="0aa9d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aa9d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="0aa9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aa9d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="0aa9d-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="0aa9d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="0aa9d-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="0aa9d-108">The new error object.</span></span>  
  
## <span data-ttu-id="0aa9d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aa9d-109">Return Value</span></span>  
 <span data-ttu-id="0aa9d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0aa9d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0aa9d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aa9d-111">Remarks</span></span>  
 <span data-ttu-id="0aa9d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="0aa9d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0aa9d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa9d-113">Requirements</span></span>  
 <span data-ttu-id="0aa9d-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0aa9d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0aa9d-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0aa9d-115">See Also</span></span>  
 [<span data-ttu-id="0aa9d-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0aa9d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
