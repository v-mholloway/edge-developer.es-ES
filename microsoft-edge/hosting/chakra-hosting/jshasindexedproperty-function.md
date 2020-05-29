---
description: Prueba si un objeto tiene un valor en el índice especificado.
title: Función JsHasIndexedProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85d9fa12c44bd1d961ec2a7ba494484873635586
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574562"
---
# <span data-ttu-id="69ae1-103">Función JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="69ae1-103">JsHasIndexedProperty Function</span></span>
<span data-ttu-id="69ae1-104">Prueba si un objeto tiene un valor en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="69ae1-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="69ae1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69ae1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="69ae1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69ae1-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="69ae1-107">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="69ae1-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="69ae1-108">Índice que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="69ae1-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="69ae1-109">Si el objeto tiene un valor en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="69ae1-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="69ae1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69ae1-110">Return Value</span></span>  
 <span data-ttu-id="69ae1-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="69ae1-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="69ae1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69ae1-112">Remarks</span></span>  
 <span data-ttu-id="69ae1-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="69ae1-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="69ae1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ae1-114">Requirements</span></span>  
 <span data-ttu-id="69ae1-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="69ae1-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="69ae1-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="69ae1-116">See Also</span></span>  
 [<span data-ttu-id="69ae1-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="69ae1-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)