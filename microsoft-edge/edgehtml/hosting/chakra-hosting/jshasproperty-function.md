---
description: Determina si un objeto tiene una propiedad.
title: Función JsHasProperty | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e45ecfaafb06c49a6a3773eb798ee93a19fd6d6e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236289"
---
# <span data-ttu-id="a4ebc-103">Función JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="a4ebc-103">JsHasProperty Function</span></span>

<span data-ttu-id="a4ebc-104">Determina si un objeto tiene una propiedad.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="a4ebc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4ebc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="a4ebc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4ebc-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a4ebc-107">Objeto que puede contener la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="a4ebc-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="a4ebc-109">Si el objeto (o un prototipo) tiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="a4ebc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4ebc-110">Return Value</span></span>  
 <span data-ttu-id="a4ebc-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a4ebc-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4ebc-112">Remarks</span></span>  
 <span data-ttu-id="a4ebc-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a4ebc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4ebc-114">Requirements</span></span>  
 <span data-ttu-id="a4ebc-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a4ebc-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a4ebc-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a4ebc-116">See Also</span></span>  
 [<span data-ttu-id="a4ebc-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a4ebc-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
