---
description: Establece el prototipo de un objeto.
title: Función JsSetPrototype | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 860a7b8d85e043c87d554e09de50d0cb642b273a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236062"
---
# <span data-ttu-id="37362-103">Función JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="37362-103">JsSetPrototype Function</span></span>

<span data-ttu-id="37362-104">Establece el prototipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="37362-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="37362-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37362-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="37362-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37362-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="37362-107">Objeto cuyo prototipo se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="37362-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="37362-108">El nuevo prototipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="37362-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="37362-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37362-109">Return Value</span></span>  
 <span data-ttu-id="37362-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="37362-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="37362-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37362-111">Remarks</span></span>  
 <span data-ttu-id="37362-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="37362-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="37362-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37362-113">Requirements</span></span>  
 <span data-ttu-id="37362-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="37362-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="37362-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="37362-115">See Also</span></span>  
 [<span data-ttu-id="37362-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="37362-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
