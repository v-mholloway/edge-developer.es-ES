---
description: Crea un objeto de JavaScript `ArrayBuffer` .
title: Función JsCreateArrayBuffer | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7e81c50317de5243fbcdf761c09c084f97a8e1e0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573514"
---
# <span data-ttu-id="8153f-103">Función JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="8153f-103">JsCreateArrayBuffer Function</span></span>
<span data-ttu-id="8153f-104">Crea un objeto de JavaScript `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="8153f-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="8153f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8153f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="8153f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8153f-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="8153f-107">El número de bytes de la ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="8153f-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="8153f-108">El nuevo objeto ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="8153f-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="8153f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8153f-109">Return Value</span></span>  
 <span data-ttu-id="8153f-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="8153f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8153f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8153f-111">Remarks</span></span>  
 <span data-ttu-id="8153f-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="8153f-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="8153f-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8153f-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="8153f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8153f-114">Requirements</span></span>  
 <span data-ttu-id="8153f-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8153f-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8153f-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8153f-116">See Also</span></span>  
 [<span data-ttu-id="8153f-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8153f-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)