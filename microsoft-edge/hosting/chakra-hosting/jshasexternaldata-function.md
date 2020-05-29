---
description: Determina si un objeto es un objeto externo.
title: Función JsHasExternalData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0ca86df09264eb82dac2e928874ca15edd2c8c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574568"
---
# <span data-ttu-id="78eae-103">Función JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="78eae-103">JsHasExternalData Function</span></span>
<span data-ttu-id="78eae-104">Determina si un objeto es un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="78eae-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="78eae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78eae-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="78eae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78eae-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="78eae-107">El objeto.</span><span class="sxs-lookup"><span data-stu-id="78eae-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="78eae-108">Si el objeto es un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="78eae-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="78eae-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78eae-109">Return Value</span></span>  
 <span data-ttu-id="78eae-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="78eae-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="78eae-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78eae-111">Remarks</span></span>  
 <span data-ttu-id="78eae-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="78eae-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="78eae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78eae-113">Requirements</span></span>  
 <span data-ttu-id="78eae-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="78eae-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="78eae-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="78eae-115">See Also</span></span>  
 [<span data-ttu-id="78eae-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="78eae-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)