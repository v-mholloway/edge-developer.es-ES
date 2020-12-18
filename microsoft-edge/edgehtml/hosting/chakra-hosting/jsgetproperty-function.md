---
description: Obtiene la propiedad de un objeto.
title: Función JsGetProperty | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e5731fa3f889fc1b182f88e37ae90c96d3825402
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235884"
---
# <span data-ttu-id="bd57b-103">Función JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="bd57b-103">JsGetProperty Function</span></span>

<span data-ttu-id="bd57b-104">Obtiene la propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="bd57b-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="bd57b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd57b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="bd57b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd57b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bd57b-107">Objeto que contiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bd57b-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="bd57b-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bd57b-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="bd57b-109">El valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bd57b-109">The value of the property.</span></span>  
  
## <span data-ttu-id="bd57b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd57b-110">Return Value</span></span>  
 <span data-ttu-id="bd57b-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="bd57b-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bd57b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd57b-112">Remarks</span></span>  
 <span data-ttu-id="bd57b-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="bd57b-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bd57b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd57b-114">Requirements</span></span>  
 <span data-ttu-id="bd57b-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bd57b-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bd57b-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bd57b-116">See Also</span></span>  
 [<span data-ttu-id="bd57b-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bd57b-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
