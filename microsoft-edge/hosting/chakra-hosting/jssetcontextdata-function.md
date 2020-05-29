---
description: Establece los datos internos de JsrtContext.
title: Función JsSetContextData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 00521bafdaf6125dd15746de8a1d403eaf03b4a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574519"
---
# <span data-ttu-id="0973e-103">Función JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="0973e-103">JsSetContextData Function</span></span>
<span data-ttu-id="0973e-104">Establece los datos internos de JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="0973e-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="0973e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0973e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="0973e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0973e-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="0973e-107">Contexto en el que se van a establecer los datos.</span><span class="sxs-lookup"><span data-stu-id="0973e-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="0973e-108">Puntero a los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="0973e-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="0973e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0973e-109">Return Value</span></span>  
 <span data-ttu-id="0973e-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0973e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0973e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0973e-111">Remarks</span></span>  
 <span data-ttu-id="0973e-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="0973e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0973e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0973e-113">Requirements</span></span>  
 <span data-ttu-id="0973e-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0973e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0973e-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0973e-115">See Also</span></span>  
 [<span data-ttu-id="0973e-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0973e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)