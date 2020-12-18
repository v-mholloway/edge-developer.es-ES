---
description: Crea un objeto de JavaScript `DataView` .
title: Función JsCreateDataView | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236076"
---
# <span data-ttu-id="28802-103">Función JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="28802-103">JsCreateDataView Function</span></span>

<span data-ttu-id="28802-104">Crea un objeto de JavaScript `DataView` .</span><span class="sxs-lookup"><span data-stu-id="28802-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="28802-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28802-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="28802-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28802-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="28802-107">Objeto existente `ArrayBuffer` para usar como almacenamiento para el objeto de resultado `DataView` .</span><span class="sxs-lookup"><span data-stu-id="28802-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="28802-108">Desplazamiento en bytes desde el inicio de `arrayBuffer` para el resultado `DataView` a la referencia.</span><span class="sxs-lookup"><span data-stu-id="28802-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="28802-109">El número de bytes en el ArrayBuffer de resultado de DataView al que hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="28802-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="28802-110">Nuevo objeto DataView.</span><span class="sxs-lookup"><span data-stu-id="28802-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="28802-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28802-111">Return Value</span></span>  
 <span data-ttu-id="28802-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="28802-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="28802-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28802-113">Remarks</span></span>  
 <span data-ttu-id="28802-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="28802-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="28802-115">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="28802-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="28802-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28802-116">Requirements</span></span>  
 <span data-ttu-id="28802-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="28802-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="28802-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="28802-118">See Also</span></span>  
 [<span data-ttu-id="28802-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="28802-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
