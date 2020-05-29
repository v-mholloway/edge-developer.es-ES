---
description: Obtiene las propiedades de una matriz con tipo que se usan con frecuencia.
title: Función JsGetTypedArrayInfo | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b33b0c515733864c1849a08aa2f8dc6e884c22ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573435"
---
# <span data-ttu-id="8fabf-103">Función JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="8fabf-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="8fabf-104">Obtiene las propiedades de una matriz con tipo que se usan con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="8fabf-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="8fabf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fabf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="8fabf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fabf-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="8fabf-107">Instancia de matriz con tipo.</span><span class="sxs-lookup"><span data-stu-id="8fabf-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="8fabf-108">Tipo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8fabf-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="8fabf-109">El `ArrayBuffer` almacén de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8fabf-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="8fabf-110">Desplazamiento en bytes desde el inicio de arrayBuffer al que hace referencia la matriz.</span><span class="sxs-lookup"><span data-stu-id="8fabf-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="8fabf-111">El número de bytes de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8fabf-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="8fabf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fabf-112">Return Value</span></span>  
 <span data-ttu-id="8fabf-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="8fabf-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8fabf-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fabf-114">Remarks</span></span>  
 <span data-ttu-id="8fabf-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="8fabf-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8fabf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fabf-116">Requirements</span></span>  
 <span data-ttu-id="8fabf-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8fabf-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8fabf-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8fabf-118">See Also</span></span>  
 [<span data-ttu-id="8fabf-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8fabf-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)