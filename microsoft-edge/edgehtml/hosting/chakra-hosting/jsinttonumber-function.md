---
description: Crea un valor de número a partir de un `int` valor.
title: Función JsIntToNumber | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24e861d1535ae79843fb35de8a047031a479fe16
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236461"
---
# <span data-ttu-id="b0feb-103">Función JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="b0feb-103">JsIntToNumber Function</span></span>

<span data-ttu-id="b0feb-104">Crea un valor de número a partir de un `int` valor.</span><span class="sxs-lookup"><span data-stu-id="b0feb-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="b0feb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0feb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="b0feb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0feb-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="b0feb-107">`int`Para convertir en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="b0feb-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="b0feb-108">El nuevo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="b0feb-108">The new number value.</span></span>  
  
## <span data-ttu-id="b0feb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0feb-109">Return Value</span></span>  
 <span data-ttu-id="b0feb-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b0feb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b0feb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0feb-111">Remarks</span></span>  
 <span data-ttu-id="b0feb-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b0feb-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b0feb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0feb-113">Requirements</span></span>  
 <span data-ttu-id="b0feb-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b0feb-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b0feb-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b0feb-115">See Also</span></span>  
 [<span data-ttu-id="b0feb-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b0feb-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
