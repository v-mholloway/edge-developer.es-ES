---
description: Obtiene el almacenamiento de memoria subyacente usado por un ArrayBuffer.
title: Función JsGetArrayBufferStorage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236205"
---
# <span data-ttu-id="1b520-103">Función JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="1b520-103">JsGetArrayBufferStorage Function</span></span>

<span data-ttu-id="1b520-104">Obtiene el almacenamiento de memoria subyacente usado por un `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="1b520-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="1b520-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b520-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="1b520-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b520-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="1b520-107">La instancia de ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="1b520-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="1b520-108">El búfer de ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="1b520-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="1b520-109">La duración del búfer devuelto es la misma que la del `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="1b520-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="1b520-110">El puntero de búfer no se cuenta como una referencia a la `ArrayBuffer` finalidad de la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="1b520-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="1b520-111">El número de bytes del búfer.</span><span class="sxs-lookup"><span data-stu-id="1b520-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="1b520-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b520-112">Return Value</span></span>  
 <span data-ttu-id="1b520-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="1b520-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1b520-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b520-114">Remarks</span></span>  
 <span data-ttu-id="1b520-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="1b520-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1b520-116">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b520-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="1b520-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b520-117">Requirements</span></span>  
 <span data-ttu-id="1b520-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1b520-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1b520-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="1b520-119">See Also</span></span>  
 [<span data-ttu-id="1b520-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1b520-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
