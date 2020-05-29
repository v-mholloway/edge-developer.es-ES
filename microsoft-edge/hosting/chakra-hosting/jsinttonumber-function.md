---
description: Crea un valor de número a partir de un `int` valor.
title: Función JsIntToNumber | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8f51638292346ec3058f9537d72b8fd21bebc6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573431"
---
# <span data-ttu-id="c2895-103">Función JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="c2895-103">JsIntToNumber Function</span></span>
<span data-ttu-id="c2895-104">Crea un valor de número a partir de un `int` valor.</span><span class="sxs-lookup"><span data-stu-id="c2895-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="c2895-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2895-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="c2895-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2895-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="c2895-107">`int`Para convertir en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="c2895-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="c2895-108">El nuevo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="c2895-108">The new number value.</span></span>  
  
## <span data-ttu-id="c2895-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2895-109">Return Value</span></span>  
 <span data-ttu-id="c2895-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c2895-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c2895-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2895-111">Remarks</span></span>  
 <span data-ttu-id="c2895-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="c2895-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c2895-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2895-113">Requirements</span></span>  
 <span data-ttu-id="c2895-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c2895-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c2895-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c2895-115">See Also</span></span>  
 [<span data-ttu-id="c2895-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c2895-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)