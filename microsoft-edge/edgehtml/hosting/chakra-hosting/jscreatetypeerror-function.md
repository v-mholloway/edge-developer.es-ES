---
description: Crea un nuevo objeto de error de JavaScript TypeError.
title: Función JsCreateTypeError | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627dfdc6f01f0708366720a957b3784fc7bb59a4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236429"
---
# <span data-ttu-id="0511d-103">Función JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="0511d-103">JsCreateTypeError Function</span></span>

<span data-ttu-id="0511d-104">Crea un nuevo objeto de error de JavaScript TypeError.</span><span class="sxs-lookup"><span data-stu-id="0511d-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="0511d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0511d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="0511d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0511d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="0511d-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="0511d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="0511d-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="0511d-108">The new error object.</span></span>  
  
## <span data-ttu-id="0511d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0511d-109">Return Value</span></span>  
 <span data-ttu-id="0511d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0511d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0511d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0511d-111">Remarks</span></span>  
 <span data-ttu-id="0511d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="0511d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0511d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0511d-113">Requirements</span></span>  
 <span data-ttu-id="0511d-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0511d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0511d-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0511d-115">See Also</span></span>  
 [<span data-ttu-id="0511d-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0511d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
