---
description: Crea un objeto de matriz de JavaScript.
title: Función JsCreateArray | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fb6a65df1484eb308224a42bb5a65443855c6215
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573513"
---
# <span data-ttu-id="eccb4-103">Función JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="eccb4-103">JsCreateArray Function</span></span>
<span data-ttu-id="eccb4-104">Crea un objeto de matriz de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eccb4-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="eccb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eccb4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="eccb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eccb4-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="eccb4-107">La longitud inicial de la matriz.</span><span class="sxs-lookup"><span data-stu-id="eccb4-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="eccb4-108">El nuevo objeto de matriz.</span><span class="sxs-lookup"><span data-stu-id="eccb4-108">The new array object.</span></span>  
  
## <span data-ttu-id="eccb4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eccb4-109">Return Value</span></span>  
 <span data-ttu-id="eccb4-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="eccb4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="eccb4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eccb4-111">Remarks</span></span>  
 <span data-ttu-id="eccb4-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="eccb4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="eccb4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eccb4-113">Requirements</span></span>  
 <span data-ttu-id="eccb4-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="eccb4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eccb4-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="eccb4-115">See Also</span></span>  
 [<span data-ttu-id="eccb4-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="eccb4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)