---
description: Obtiene el valor de `true` en el contexto de script actual.
title: Función JsGetTrueValue | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58798e1e8aab57d626be0c8c878f9be39d0af942
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236643"
---
# <span data-ttu-id="aa435-103">Función JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="aa435-103">JsGetTrueValue Function</span></span>

<span data-ttu-id="aa435-104">Obtiene el valor de `true` en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="aa435-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="aa435-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa435-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="aa435-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa435-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="aa435-107">El `true` valor.</span><span class="sxs-lookup"><span data-stu-id="aa435-107">The `true` value.</span></span>  
  
## <span data-ttu-id="aa435-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa435-108">Return Value</span></span>  
 <span data-ttu-id="aa435-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="aa435-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aa435-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa435-110">Remarks</span></span>  
 <span data-ttu-id="aa435-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="aa435-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="aa435-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa435-112">Requirements</span></span>  
 <span data-ttu-id="aa435-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aa435-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aa435-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="aa435-114">See Also</span></span>  
 [<span data-ttu-id="aa435-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aa435-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
