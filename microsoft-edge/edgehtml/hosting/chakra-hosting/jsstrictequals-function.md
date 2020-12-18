---
description: Compara dos valores de JavaScript para una igualdad estricta.
title: Función JsStrictEquals | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 98af1629129986cc21cafe5660d3155e031919dc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236237"
---
# <span data-ttu-id="ebb75-103">Función JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="ebb75-103">JsStrictEquals Function</span></span>

<span data-ttu-id="ebb75-104">Compara dos valores de JavaScript para una igualdad estricta.</span><span class="sxs-lookup"><span data-stu-id="ebb75-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="ebb75-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebb75-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="ebb75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebb75-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="ebb75-107">Primer objeto que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="ebb75-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="ebb75-108">El segundo objeto que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="ebb75-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="ebb75-109">Si los valores son estrictamente iguales.</span><span class="sxs-lookup"><span data-stu-id="ebb75-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="ebb75-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebb75-110">Return Value</span></span>  
 <span data-ttu-id="ebb75-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ebb75-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ebb75-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebb75-112">Remarks</span></span>  
 <span data-ttu-id="ebb75-113">Esta función es equivalente al `===` operador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ebb75-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="ebb75-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="ebb75-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ebb75-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb75-115">Requirements</span></span>  
 <span data-ttu-id="ebb75-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ebb75-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ebb75-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ebb75-117">See Also</span></span>  
 [<span data-ttu-id="ebb75-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ebb75-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
