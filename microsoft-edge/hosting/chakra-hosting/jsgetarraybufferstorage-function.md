---
description: Obtiene el almacenamiento de memoria subyacente usado por un ArrayBuffer.
title: Función JsGetArrayBufferStorage | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574598"
---
# <span data-ttu-id="4559f-103">Función JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="4559f-103">JsGetArrayBufferStorage Function</span></span>
<span data-ttu-id="4559f-104">Obtiene el almacenamiento de memoria subyacente usado por un `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="4559f-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="4559f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4559f-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="4559f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4559f-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="4559f-107">La instancia de ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="4559f-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="4559f-108">El búfer de ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="4559f-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="4559f-109">La duración del búfer devuelto es la misma que la del `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="4559f-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="4559f-110">El puntero de búfer no se cuenta como una referencia a la `ArrayBuffer` finalidad de la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="4559f-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="4559f-111">El número de bytes del búfer.</span><span class="sxs-lookup"><span data-stu-id="4559f-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="4559f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4559f-112">Return Value</span></span>  
 <span data-ttu-id="4559f-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4559f-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4559f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4559f-114">Remarks</span></span>  
 <span data-ttu-id="4559f-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="4559f-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4559f-116">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4559f-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4559f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4559f-117">Requirements</span></span>  
 <span data-ttu-id="4559f-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4559f-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4559f-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="4559f-119">See Also</span></span>  
 [<span data-ttu-id="4559f-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4559f-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)