---
description: Recupera el `bool` valor de un valor booleano.
title: Función JsBooleanToBool | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 55b0ef1278cbc73652fc8427e004cab002d76e5b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573535"
---
# <span data-ttu-id="7d6cf-103">Función JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="7d6cf-103">JsBooleanToBool Function</span></span>
<span data-ttu-id="7d6cf-104">Recupera el `bool` valor de un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="7d6cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d6cf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="7d6cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d6cf-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="7d6cf-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="7d6cf-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-108">The converted value.</span></span>  
  
## <span data-ttu-id="7d6cf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d6cf-109">Return Value</span></span>  
 <span data-ttu-id="7d6cf-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7d6cf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d6cf-111">Remarks</span></span>  
 <span data-ttu-id="7d6cf-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7d6cf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6cf-113">Requirements</span></span>  
 <span data-ttu-id="7d6cf-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7d6cf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7d6cf-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7d6cf-115">See Also</span></span>  
 [<span data-ttu-id="7d6cf-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7d6cf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)