---
description: Crea un nuevo objeto que almacena algunos datos externos.
title: Función JsCreateExternalObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d402c3d379a16186daaba601c7f830c53a9a953
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236592"
---
# <span data-ttu-id="79f0a-103">Función JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="79f0a-103">JsCreateExternalObject Function</span></span>

<span data-ttu-id="79f0a-104">Crea un nuevo objeto que almacena algunos datos externos.</span><span class="sxs-lookup"><span data-stu-id="79f0a-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="79f0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79f0a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="79f0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79f0a-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="79f0a-107">Datos externos que representará el objeto.</span><span class="sxs-lookup"><span data-stu-id="79f0a-107">External data that the object will represent.</span></span> <span data-ttu-id="79f0a-108">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="79f0a-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="79f0a-109">Una devolución de llamada para cuando el objeto está finalizado.</span><span class="sxs-lookup"><span data-stu-id="79f0a-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="79f0a-110">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="79f0a-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="79f0a-111">El objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="79f0a-111">The new object.</span></span>  
  
## <span data-ttu-id="79f0a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79f0a-112">Return Value</span></span>  
 <span data-ttu-id="79f0a-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="79f0a-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="79f0a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79f0a-114">Remarks</span></span>  
 <span data-ttu-id="79f0a-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="79f0a-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="79f0a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79f0a-116">Requirements</span></span>  
 <span data-ttu-id="79f0a-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="79f0a-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="79f0a-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="79f0a-118">See Also</span></span>  
 [<span data-ttu-id="79f0a-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="79f0a-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
