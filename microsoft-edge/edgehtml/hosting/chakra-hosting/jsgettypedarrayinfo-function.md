---
description: Obtiene las propiedades de una matriz con tipo que se usan con frecuencia.
title: Función JsGetTypedArrayInfo | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236445"
---
# <span data-ttu-id="1ed11-103">Función JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="1ed11-103">JsGetTypedArrayInfo Function</span></span>

<span data-ttu-id="1ed11-104">Obtiene las propiedades de una matriz con tipo que se usan con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1ed11-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="1ed11-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ed11-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="1ed11-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ed11-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="1ed11-107">Instancia de matriz con tipo.</span><span class="sxs-lookup"><span data-stu-id="1ed11-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="1ed11-108">Tipo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="1ed11-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="1ed11-109">El `ArrayBuffer` almacén de la matriz.</span><span class="sxs-lookup"><span data-stu-id="1ed11-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="1ed11-110">Desplazamiento en bytes desde el inicio de arrayBuffer al que hace referencia la matriz.</span><span class="sxs-lookup"><span data-stu-id="1ed11-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="1ed11-111">El número de bytes de la matriz.</span><span class="sxs-lookup"><span data-stu-id="1ed11-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="1ed11-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ed11-112">Return Value</span></span>  
 <span data-ttu-id="1ed11-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="1ed11-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1ed11-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ed11-114">Remarks</span></span>  
 <span data-ttu-id="1ed11-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="1ed11-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1ed11-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed11-116">Requirements</span></span>  
 <span data-ttu-id="1ed11-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ed11-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ed11-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="1ed11-118">See Also</span></span>  
 [<span data-ttu-id="1ed11-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1ed11-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
