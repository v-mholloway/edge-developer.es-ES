---
description: Obtiene el almacenamiento de memoria subyacente utilizado por DataView.
title: Función JsGetDataViewStorage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236326"
---
# <span data-ttu-id="7e0b8-103">Función JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="7e0b8-103">JsGetDataViewStorage Function</span></span>

<span data-ttu-id="7e0b8-104">Obtiene el almacenamiento de memoria subyacente usado por un `DataView` .</span><span class="sxs-lookup"><span data-stu-id="7e0b8-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="7e0b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e0b8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="7e0b8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e0b8-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="7e0b8-107">La instancia de DataView.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="7e0b8-108">El búfer de DataView.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-108">The DataView's buffer.</span></span> <span data-ttu-id="7e0b8-109">La duración del búfer devuelto es la misma que la del `DataView` .</span><span class="sxs-lookup"><span data-stu-id="7e0b8-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="7e0b8-110">El puntero de búfer no se cuenta como una referencia a la `DataView` finalidad de la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="7e0b8-111">El número de bytes del búfer.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="7e0b8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e0b8-112">Return Value</span></span>  
 <span data-ttu-id="7e0b8-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7e0b8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e0b8-114">Remarks</span></span>  
 <span data-ttu-id="7e0b8-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="7e0b8-116">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7e0b8-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="7e0b8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e0b8-117">Requirements</span></span>  
 <span data-ttu-id="7e0b8-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7e0b8-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7e0b8-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7e0b8-119">See Also</span></span>  
 [<span data-ttu-id="7e0b8-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7e0b8-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
