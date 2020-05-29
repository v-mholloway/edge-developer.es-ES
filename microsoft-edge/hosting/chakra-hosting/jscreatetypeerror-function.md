---
description: Crea un nuevo objeto de error de JavaScript TypeError.
title: Función JsCreateTypeError | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 302bf75af3668dfdd0b40336e940e3eef3a74bce
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573480"
---
# <span data-ttu-id="26f5d-103">Función JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="26f5d-103">JsCreateTypeError Function</span></span>
<span data-ttu-id="26f5d-104">Crea un nuevo objeto de error de JavaScript TypeError.</span><span class="sxs-lookup"><span data-stu-id="26f5d-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="26f5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26f5d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="26f5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f5d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="26f5d-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="26f5d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="26f5d-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="26f5d-108">The new error object.</span></span>  
  
## <span data-ttu-id="26f5d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f5d-109">Return Value</span></span>  
 <span data-ttu-id="26f5d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="26f5d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="26f5d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26f5d-111">Remarks</span></span>  
 <span data-ttu-id="26f5d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="26f5d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="26f5d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f5d-113">Requirements</span></span>  
 <span data-ttu-id="26f5d-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="26f5d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="26f5d-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="26f5d-115">See Also</span></span>  
 [<span data-ttu-id="26f5d-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="26f5d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)