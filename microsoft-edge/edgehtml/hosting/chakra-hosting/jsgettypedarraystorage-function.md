---
description: Obtiene el almacenamiento de memoria subyacente utilizado por una matriz con tipo.
title: Función JsGetTypedArrayStorage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235942"
---
# <span data-ttu-id="28deb-103">Función JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="28deb-103">JsGetTypedArrayStorage Function</span></span>

<span data-ttu-id="28deb-104">Obtiene el almacenamiento de memoria subyacente utilizado por una matriz con tipo.</span><span class="sxs-lookup"><span data-stu-id="28deb-104">Obtains the underlying memory storage used by a typed array.</span></span>  
  
## <span data-ttu-id="28deb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28deb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### <span data-ttu-id="28deb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28deb-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="28deb-107">Instancia de matriz con tipo.</span><span class="sxs-lookup"><span data-stu-id="28deb-107">The typed array instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="28deb-108">El búfer de la matriz.</span><span class="sxs-lookup"><span data-stu-id="28deb-108">The array's buffer.</span></span> <span data-ttu-id="28deb-109">La vigencia del búfer devuelto es igual que la duración de la matriz.</span><span class="sxs-lookup"><span data-stu-id="28deb-109">The lifetime of the buffer returned is the same as the lifetime of the array.</span></span> <span data-ttu-id="28deb-110">El puntero de búfer no se tiene en cuenta como una referencia a la matriz por el propósito de la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="28deb-110">The buffer pointer does not count as a reference to the array for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="28deb-111">El número de bytes del búfer.</span><span class="sxs-lookup"><span data-stu-id="28deb-111">The number of bytes in the buffer.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="28deb-112">Tipo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="28deb-112">The type of the array.</span></span>  
  
 `elementSize`  
 <span data-ttu-id="28deb-113">Tamaño de un elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="28deb-113">The size of an element of the array.</span></span>  
  
## <span data-ttu-id="28deb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28deb-114">Return Value</span></span>  
 <span data-ttu-id="28deb-115">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="28deb-115">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="28deb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28deb-116">Remarks</span></span>  
 <span data-ttu-id="28deb-117">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="28deb-117">Requires an active script context.</span></span>  
  
 <span data-ttu-id="28deb-118">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="28deb-118">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="28deb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28deb-119">Requirements</span></span>  
 <span data-ttu-id="28deb-120">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="28deb-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="28deb-121">Consulta también</span><span class="sxs-lookup"><span data-stu-id="28deb-121">See Also</span></span>  
 [<span data-ttu-id="28deb-122">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="28deb-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
