---
description: Crea un nuevo objeto de error de JavaScript.
title: Función JsCreateError | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 33d70e3f077b085ccb4ab541d3246d777ea68978
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573505"
---
# <span data-ttu-id="b09a6-103">Función JsCreateError</span><span class="sxs-lookup"><span data-stu-id="b09a6-103">JsCreateError Function</span></span>
<span data-ttu-id="b09a6-104">Crea un nuevo objeto de error de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b09a6-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="b09a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b09a6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="b09a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b09a6-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="b09a6-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="b09a6-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="b09a6-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="b09a6-108">The new error object.</span></span>  
  
## <span data-ttu-id="b09a6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b09a6-109">Return Value</span></span>  
 <span data-ttu-id="b09a6-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b09a6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b09a6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b09a6-111">Remarks</span></span>  
 <span data-ttu-id="b09a6-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b09a6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b09a6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b09a6-113">Requirements</span></span>  
 <span data-ttu-id="b09a6-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b09a6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b09a6-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b09a6-115">See Also</span></span>  
 [<span data-ttu-id="b09a6-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b09a6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)