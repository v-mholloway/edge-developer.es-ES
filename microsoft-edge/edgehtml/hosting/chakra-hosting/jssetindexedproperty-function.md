---
description: Establecer el valor en el índice especificado de un objeto.
title: Función JsSetIndexedProperty | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1fa961750fa5db262e1512d8d26572280d5e726c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236059"
---
# <span data-ttu-id="06e68-103">Función JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="06e68-103">JsSetIndexedProperty Function</span></span>

<span data-ttu-id="06e68-104">Establecer el valor en el índice especificado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="06e68-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="06e68-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06e68-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="06e68-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06e68-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="06e68-107">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="06e68-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="06e68-108">Índice que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="06e68-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="06e68-109">Valor que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="06e68-109">The value to set.</span></span>  
  
## <span data-ttu-id="06e68-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06e68-110">Return Value</span></span>  
 <span data-ttu-id="06e68-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="06e68-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="06e68-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06e68-112">Remarks</span></span>  
 <span data-ttu-id="06e68-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="06e68-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="06e68-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06e68-114">Requirements</span></span>  
 <span data-ttu-id="06e68-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="06e68-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="06e68-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="06e68-116">See Also</span></span>  
 [<span data-ttu-id="06e68-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="06e68-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
