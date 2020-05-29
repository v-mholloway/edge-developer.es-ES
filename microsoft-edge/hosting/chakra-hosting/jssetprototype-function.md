---
description: Establece el prototipo de un objeto.
title: Función JsSetPrototype | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 625269c5f9f459a5c7eecb6cfc31cb85fc24214b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574422"
---
# <span data-ttu-id="fb997-103">Función JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="fb997-103">JsSetPrototype Function</span></span>
<span data-ttu-id="fb997-104">Establece el prototipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="fb997-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="fb997-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb997-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="fb997-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb997-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="fb997-107">Objeto cuyo prototipo se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="fb997-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="fb997-108">El nuevo prototipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb997-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="fb997-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb997-109">Return Value</span></span>  
 <span data-ttu-id="fb997-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="fb997-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fb997-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb997-111">Remarks</span></span>  
 <span data-ttu-id="fb997-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="fb997-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fb997-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb997-113">Requirements</span></span>  
 <span data-ttu-id="fb997-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb997-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb997-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fb997-115">See Also</span></span>  
 [<span data-ttu-id="fb997-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fb997-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)