---
description: Compara dos valores de JavaScript para determinar si son iguales.
title: Función JsEquals | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84416584a048512ab20754a3b59eb8ec255901c4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574602"
---
# <span data-ttu-id="b3401-103">Función JsEquals</span><span class="sxs-lookup"><span data-stu-id="b3401-103">JsEquals Function</span></span>
<span data-ttu-id="b3401-104">Compara dos valores de JavaScript para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="b3401-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="b3401-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3401-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="b3401-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3401-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="b3401-107">Primer objeto que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b3401-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="b3401-108">El segundo objeto que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b3401-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="b3401-109">Si los valores son iguales.</span><span class="sxs-lookup"><span data-stu-id="b3401-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="b3401-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3401-110">Return Value</span></span>  
 <span data-ttu-id="b3401-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b3401-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b3401-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3401-112">Remarks</span></span>  
 <span data-ttu-id="b3401-113">Esta función es equivalente al `==` operador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b3401-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="b3401-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b3401-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b3401-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3401-115">Requirements</span></span>  
 <span data-ttu-id="b3401-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b3401-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b3401-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b3401-117">See Also</span></span>  
 [<span data-ttu-id="b3401-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b3401-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)