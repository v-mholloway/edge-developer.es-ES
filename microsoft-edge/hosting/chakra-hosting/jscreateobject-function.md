---
description: Crea un objeto nuevo.
title: Función JsCreateObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ed988aae0921978819d379562d4a966e4a082a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573495"
---
# <span data-ttu-id="6499d-103">Función JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="6499d-103">JsCreateObject Function</span></span>
<span data-ttu-id="6499d-104">Crea un objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="6499d-104">Creates a new object.</span></span>
  
## <span data-ttu-id="6499d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6499d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="6499d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6499d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6499d-107">El objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="6499d-107">The new object.</span></span>  
  
## <span data-ttu-id="6499d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6499d-108">Return Value</span></span>  
 <span data-ttu-id="6499d-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6499d-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6499d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6499d-110">Remarks</span></span>  
 <span data-ttu-id="6499d-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="6499d-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6499d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6499d-112">Requirements</span></span>  
 <span data-ttu-id="6499d-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6499d-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6499d-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6499d-114">See Also</span></span>  
 [<span data-ttu-id="6499d-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6499d-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)