---
description: Crea un nuevo objeto de error de JavaScript.
title: Función JsCreateError | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd2fd0172902cc6dc8a4dd169eef5947d0b25256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236079"
---
# <span data-ttu-id="ba19d-103">Función JsCreateError</span><span class="sxs-lookup"><span data-stu-id="ba19d-103">JsCreateError Function</span></span>

<span data-ttu-id="ba19d-104">Crea un nuevo objeto de error de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba19d-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="ba19d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba19d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="ba19d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba19d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="ba19d-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="ba19d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="ba19d-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="ba19d-108">The new error object.</span></span>  
  
## <span data-ttu-id="ba19d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba19d-109">Return Value</span></span>  
 <span data-ttu-id="ba19d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ba19d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ba19d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba19d-111">Remarks</span></span>  
 <span data-ttu-id="ba19d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="ba19d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ba19d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba19d-113">Requirements</span></span>  
 <span data-ttu-id="ba19d-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ba19d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ba19d-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ba19d-115">See Also</span></span>  
 [<span data-ttu-id="ba19d-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ba19d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
