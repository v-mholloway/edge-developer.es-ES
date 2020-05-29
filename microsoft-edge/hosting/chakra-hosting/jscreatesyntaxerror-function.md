---
description: Crea un nuevo objeto de error de JavaScript SyntaxError.
title: Función JsCreateSyntaxError | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 8f7459e8300df56aa8ccfaa78ef97ce2b6ec6fa0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573483"
---
# <span data-ttu-id="049ef-103">Función JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="049ef-103">JsCreateSyntaxError Function</span></span>
<span data-ttu-id="049ef-104">Crea un nuevo objeto de error de JavaScript SyntaxError.</span><span class="sxs-lookup"><span data-stu-id="049ef-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="049ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="049ef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="049ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="049ef-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="049ef-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="049ef-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="049ef-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="049ef-108">The new error object.</span></span>  
  
## <span data-ttu-id="049ef-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="049ef-109">Return Value</span></span>  
 <span data-ttu-id="049ef-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="049ef-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="049ef-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="049ef-111">Remarks</span></span>  
 <span data-ttu-id="049ef-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="049ef-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="049ef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="049ef-113">Requirements</span></span>  
 <span data-ttu-id="049ef-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="049ef-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="049ef-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="049ef-115">See Also</span></span>  
 [<span data-ttu-id="049ef-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="049ef-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)