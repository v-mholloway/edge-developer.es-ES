---
description: Crea un nuevo objeto de error de JavaScript SyntaxError.
title: Función JsCreateSyntaxError | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d6534bfa2b59cb2f6ab68c231d7a97c84876d62
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236433"
---
# <span data-ttu-id="efff2-103">Función JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="efff2-103">JsCreateSyntaxError Function</span></span>

<span data-ttu-id="efff2-104">Crea un nuevo objeto de error de JavaScript SyntaxError.</span><span class="sxs-lookup"><span data-stu-id="efff2-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="efff2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efff2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="efff2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efff2-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="efff2-107">Mensaje para el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="efff2-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="efff2-108">El nuevo objeto de error.</span><span class="sxs-lookup"><span data-stu-id="efff2-108">The new error object.</span></span>  
  
## <span data-ttu-id="efff2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efff2-109">Return Value</span></span>  
 <span data-ttu-id="efff2-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="efff2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="efff2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efff2-111">Remarks</span></span>  
 <span data-ttu-id="efff2-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="efff2-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="efff2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efff2-113">Requirements</span></span>  
 <span data-ttu-id="efff2-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="efff2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="efff2-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="efff2-115">See Also</span></span>  
 [<span data-ttu-id="efff2-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="efff2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
