---
description: Obtiene el motor en tiempo de ejecución al que pertenece el contexto.
title: Función JsGetRuntime | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573447"
---
# <span data-ttu-id="8bd7a-103">Función JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="8bd7a-103">JsGetRuntime Function</span></span>
<span data-ttu-id="8bd7a-104">Obtiene el motor en tiempo de ejecución al que pertenece el contexto.</span><span class="sxs-lookup"><span data-stu-id="8bd7a-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="8bd7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bd7a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="8bd7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bd7a-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="8bd7a-107">Contexto desde el que se va a obtener el motor en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="8bd7a-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="8bd7a-108">El motor en tiempo de ejecución al que pertenece el contexto.</span><span class="sxs-lookup"><span data-stu-id="8bd7a-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="8bd7a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bd7a-109">Return Value</span></span>  
 <span data-ttu-id="8bd7a-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="8bd7a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8bd7a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bd7a-111">Requirements</span></span>  
 <span data-ttu-id="8bd7a-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8bd7a-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8bd7a-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8bd7a-113">See Also</span></span>  
 [<span data-ttu-id="8bd7a-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8bd7a-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)