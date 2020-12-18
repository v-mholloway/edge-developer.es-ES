---
description: Establece los datos internos de JsrtContext.
title: Función JsSetContextData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cac404b9e79bafb5a8eafb47e893dbdf38a02405
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236399"
---
# <span data-ttu-id="19376-103">Función JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="19376-103">JsSetContextData Function</span></span>

<span data-ttu-id="19376-104">Establece los datos internos de JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="19376-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="19376-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19376-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="19376-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19376-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="19376-107">Contexto en el que se van a establecer los datos.</span><span class="sxs-lookup"><span data-stu-id="19376-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="19376-108">Puntero a los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="19376-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="19376-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19376-109">Return Value</span></span>  
 <span data-ttu-id="19376-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="19376-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="19376-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19376-111">Remarks</span></span>  
 <span data-ttu-id="19376-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="19376-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="19376-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19376-113">Requirements</span></span>  
 <span data-ttu-id="19376-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="19376-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="19376-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="19376-115">See Also</span></span>  
 [<span data-ttu-id="19376-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="19376-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
