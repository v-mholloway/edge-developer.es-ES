---
description: Obtiene el almacenamiento de memoria subyacente utilizado por DataView.
title: Función JsGetDataViewStorage | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573462"
---
# <span data-ttu-id="6c135-103">Función JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="6c135-103">JsGetDataViewStorage Function</span></span>
<span data-ttu-id="6c135-104">Obtiene el almacenamiento de memoria subyacente usado por un `DataView` .</span><span class="sxs-lookup"><span data-stu-id="6c135-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="6c135-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c135-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="6c135-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c135-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="6c135-107">La instancia de DataView.</span><span class="sxs-lookup"><span data-stu-id="6c135-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="6c135-108">El búfer de DataView.</span><span class="sxs-lookup"><span data-stu-id="6c135-108">The DataView's buffer.</span></span> <span data-ttu-id="6c135-109">La duración del búfer devuelto es la misma que la del `DataView` .</span><span class="sxs-lookup"><span data-stu-id="6c135-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="6c135-110">El puntero de búfer no se cuenta como una referencia a la `DataView` finalidad de la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="6c135-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="6c135-111">El número de bytes del búfer.</span><span class="sxs-lookup"><span data-stu-id="6c135-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="6c135-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c135-112">Return Value</span></span>  
 <span data-ttu-id="6c135-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6c135-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6c135-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c135-114">Remarks</span></span>  
 <span data-ttu-id="6c135-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="6c135-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6c135-116">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6c135-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="6c135-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c135-117">Requirements</span></span>  
 <span data-ttu-id="6c135-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6c135-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6c135-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6c135-119">See Also</span></span>  
 [<span data-ttu-id="6c135-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6c135-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)