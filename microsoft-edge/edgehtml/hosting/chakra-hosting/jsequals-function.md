---
description: Compara dos valores de JavaScript para determinar si son iguales.
title: Función JsEquals | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88f906419e73ed0de6ddde0a872becbd18908997
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236654"
---
# <span data-ttu-id="b7594-103">Función JsEquals</span><span class="sxs-lookup"><span data-stu-id="b7594-103">JsEquals Function</span></span>

<span data-ttu-id="b7594-104">Compara dos valores de JavaScript para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="b7594-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="b7594-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7594-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="b7594-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7594-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="b7594-107">Primer objeto que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b7594-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="b7594-108">El segundo objeto que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b7594-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="b7594-109">Si los valores son iguales.</span><span class="sxs-lookup"><span data-stu-id="b7594-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="b7594-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7594-110">Return Value</span></span>  
 <span data-ttu-id="b7594-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b7594-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b7594-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7594-112">Remarks</span></span>  
 <span data-ttu-id="b7594-113">Esta función es equivalente al `==` operador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b7594-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="b7594-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b7594-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b7594-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7594-115">Requirements</span></span>  
 <span data-ttu-id="b7594-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b7594-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b7594-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b7594-117">See Also</span></span>  
 [<span data-ttu-id="b7594-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b7594-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
