---
description: Crea un objeto de matriz con tipo de JavaScript.
title: Función JsCreateTypedArray | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573482"
---
# <span data-ttu-id="53fa2-103">Función JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="53fa2-103">JsCreateTypedArray Function</span></span>
<span data-ttu-id="53fa2-104">Crea un objeto de matriz con tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="53fa2-104">Creates a JavaScript typed array object.</span></span>  
  
## <span data-ttu-id="53fa2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53fa2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="53fa2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53fa2-106">Parameters</span></span>  
 `arrayType`  
 <span data-ttu-id="53fa2-107">Tipo de matriz que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="53fa2-107">The type of the array to create.</span></span>  
  
 `baseArray`  
 <span data-ttu-id="53fa2-108">Matriz base de la nueva matriz.</span><span class="sxs-lookup"><span data-stu-id="53fa2-108">The base array of the new array.</span></span> <span data-ttu-id="53fa2-109">Usar `JS_INVALID_REFERENCE` si no hay ninguna matriz base.</span><span class="sxs-lookup"><span data-stu-id="53fa2-109">Use `JS_INVALID_REFERENCE` if no base array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="53fa2-110">Desplazamiento en bytes desde el principio de `baseArray` ( `ArrayBuffer` ) para la matriz con tipo de resultado a la que se hará referencia.</span><span class="sxs-lookup"><span data-stu-id="53fa2-110">The offset in bytes from the start of `baseArray` (`ArrayBuffer`) for result typed array to reference.</span></span> <span data-ttu-id="53fa2-111">Solo es aplicable cuando `baseArray` es un `ArrayBuffer` objeto.</span><span class="sxs-lookup"><span data-stu-id="53fa2-111">Only applicable when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="53fa2-112">En caso contrario, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="53fa2-112">Must be 0 otherwise.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="53fa2-113">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53fa2-113">The number of elements in the array.</span></span> <span data-ttu-id="53fa2-114">Solo es aplicable al crear una matriz con tipo nueva sin `baseArray` ( `baseArray` es `JS_INVALID_REFERENCE` ) o cuando `baseArray` es un `ArrayBuffer` objeto.</span><span class="sxs-lookup"><span data-stu-id="53fa2-114">Only applicable when creating a new typed array without `baseArray` (`baseArray` is `JS_INVALID_REFERENCE`) or when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="53fa2-115">En caso contrario, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="53fa2-115">Must be 0 otherwise.</span></span>  
  
 `result`  
 <span data-ttu-id="53fa2-116">El nuevo objeto de matriz con tipo.</span><span class="sxs-lookup"><span data-stu-id="53fa2-116">The new typed array object.</span></span>  
  
## <span data-ttu-id="53fa2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53fa2-117">Return Value</span></span>  
 <span data-ttu-id="53fa2-118">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="53fa2-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="53fa2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53fa2-119">Remarks</span></span>  
 <span data-ttu-id="53fa2-120">`baseArray`Puede ser una `ArrayBuffer` , otra matriz con tipo o un JavaScript `Array` .</span><span class="sxs-lookup"><span data-stu-id="53fa2-120">The `baseArray` can be an `ArrayBuffer`, another typed array, or a JavaScript `Array`.</span></span> <span data-ttu-id="53fa2-121">La matriz con tipo devuelta usará `baseArray` si es una `ArrayBuffer` o, de lo contrario, crear y usar una copia de la matriz de origen subyacente.</span><span class="sxs-lookup"><span data-stu-id="53fa2-121">The returned typed array will use the `baseArray` if it is an `ArrayBuffer`, or otherwise create and use a copy of the underlying source array.</span></span>  
  
 <span data-ttu-id="53fa2-122">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="53fa2-122">Requires an active script context.</span></span>  
  
 <span data-ttu-id="53fa2-123">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="53fa2-123">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="53fa2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53fa2-124">Requirements</span></span>  
 <span data-ttu-id="53fa2-125">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="53fa2-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="53fa2-126">Consulta también</span><span class="sxs-lookup"><span data-stu-id="53fa2-126">See Also</span></span>  
 [<span data-ttu-id="53fa2-127">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="53fa2-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)