---
description: Crea un objeto de JavaScript `ArrayBuffer` .
title: Función JsCreateArrayBuffer | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bee44d77f78bd35705211c598db78ab09000c71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236077"
---
# <span data-ttu-id="d84df-103">Función JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="d84df-103">JsCreateArrayBuffer Function</span></span>

<span data-ttu-id="d84df-104">Crea un objeto de JavaScript `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="d84df-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="d84df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d84df-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="d84df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d84df-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="d84df-107">El número de bytes de la ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="d84df-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="d84df-108">El nuevo objeto ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="d84df-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="d84df-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d84df-109">Return Value</span></span>  
 <span data-ttu-id="d84df-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d84df-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d84df-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d84df-111">Remarks</span></span>  
 <span data-ttu-id="d84df-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="d84df-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d84df-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d84df-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="d84df-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d84df-114">Requirements</span></span>  
 <span data-ttu-id="d84df-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d84df-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d84df-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d84df-116">See Also</span></span>  
 [<span data-ttu-id="d84df-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d84df-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
