---
description: Determina si un objeto tiene una propiedad.
title: Función JsHasProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c6cc195ae02c28500f0a018256d24278ad4b47d8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574561"
---
# <span data-ttu-id="b7d61-103">Función JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="b7d61-103">JsHasProperty Function</span></span>
<span data-ttu-id="b7d61-104">Determina si un objeto tiene una propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7d61-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="b7d61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7d61-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="b7d61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7d61-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b7d61-107">Objeto que puede contener la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7d61-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="b7d61-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7d61-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="b7d61-109">Si el objeto (o un prototipo) tiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7d61-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="b7d61-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7d61-110">Return Value</span></span>  
 <span data-ttu-id="b7d61-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b7d61-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b7d61-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7d61-112">Remarks</span></span>  
 <span data-ttu-id="b7d61-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b7d61-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b7d61-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7d61-114">Requirements</span></span>  
 <span data-ttu-id="b7d61-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b7d61-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b7d61-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b7d61-116">See Also</span></span>  
 [<span data-ttu-id="b7d61-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b7d61-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)