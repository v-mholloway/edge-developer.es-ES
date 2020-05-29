---
description: Devuelve el prototipo de un objeto.
title: Función JsGetPrototype | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 12708634fea9e8f9fd1205514845b1cb9760ee9e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573450"
---
# <span data-ttu-id="072b9-103">Función JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="072b9-103">JsGetPrototype Function</span></span>
<span data-ttu-id="072b9-104">Devuelve el prototipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="072b9-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="072b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="072b9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="072b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="072b9-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="072b9-107">Objeto cuyo prototipo se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="072b9-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="072b9-108">Prototipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="072b9-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="072b9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="072b9-109">Return Value</span></span>  
 <span data-ttu-id="072b9-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="072b9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="072b9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="072b9-111">Remarks</span></span>  
 <span data-ttu-id="072b9-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="072b9-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="072b9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="072b9-113">Requirements</span></span>  
 <span data-ttu-id="072b9-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="072b9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="072b9-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="072b9-115">See Also</span></span>  
 [<span data-ttu-id="072b9-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="072b9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)