---
description: Establece los datos internos de JsrtContext.
title: Función JsSetContextData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e874f500ca82328dddeaaa03a0b78a188b8fd241
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751936"
---
# <span data-ttu-id="59bc7-103">Función JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="59bc7-103">JsSetContextData Function</span></span>
<span data-ttu-id="59bc7-104">Establece los datos internos de JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="59bc7-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="59bc7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59bc7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="59bc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59bc7-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="59bc7-107">Contexto en el que se van a establecer los datos.</span><span class="sxs-lookup"><span data-stu-id="59bc7-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="59bc7-108">Puntero a los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="59bc7-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="59bc7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59bc7-109">Return Value</span></span>  
 <span data-ttu-id="59bc7-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="59bc7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="59bc7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59bc7-111">Remarks</span></span>  
 <span data-ttu-id="59bc7-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="59bc7-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="59bc7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59bc7-113">Requirements</span></span>  
 <span data-ttu-id="59bc7-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="59bc7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="59bc7-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="59bc7-115">See Also</span></span>  
 [<span data-ttu-id="59bc7-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="59bc7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)