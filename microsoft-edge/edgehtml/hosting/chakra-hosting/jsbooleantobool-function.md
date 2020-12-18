---
description: Recupera el `bool` valor de un valor booleano.
title: Función JsBooleanToBool | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 36bf2dc32b94466d8cdea37886e86a42c4ec01d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236094"
---
# <span data-ttu-id="cb7a0-103">Función JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="cb7a0-103">JsBooleanToBool Function</span></span>

<span data-ttu-id="cb7a0-104">Recupera el `bool` valor de un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="cb7a0-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="cb7a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb7a0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="cb7a0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb7a0-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="cb7a0-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="cb7a0-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="cb7a0-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="cb7a0-108">The converted value.</span></span>  
  
## <span data-ttu-id="cb7a0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb7a0-109">Return Value</span></span>  
 <span data-ttu-id="cb7a0-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="cb7a0-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cb7a0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb7a0-111">Remarks</span></span>  
 <span data-ttu-id="cb7a0-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="cb7a0-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cb7a0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb7a0-113">Requirements</span></span>  
 <span data-ttu-id="cb7a0-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cb7a0-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cb7a0-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="cb7a0-115">See Also</span></span>  
 [<span data-ttu-id="cb7a0-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cb7a0-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
