---
description: Obtiene un descriptor de propiedad para la propiedad de un objeto.
title: Función JsGetOwnPropertyDescriptor | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 05c7a58fa12d7ca8013c512f40031963ebc8ac18
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236275"
---
# <span data-ttu-id="07b9d-103">Función JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="07b9d-103">JsGetOwnPropertyDescriptor Function</span></span>

<span data-ttu-id="07b9d-104">Obtiene un descriptor de propiedad para la propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="07b9d-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="07b9d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07b9d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="07b9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07b9d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="07b9d-107">Objeto que tiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="07b9d-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="07b9d-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="07b9d-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="07b9d-109">Descriptor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="07b9d-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="07b9d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07b9d-110">Return Value</span></span>  
 <span data-ttu-id="07b9d-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="07b9d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="07b9d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07b9d-112">Remarks</span></span>  
 <span data-ttu-id="07b9d-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="07b9d-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="07b9d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b9d-114">Requirements</span></span>  
 <span data-ttu-id="07b9d-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="07b9d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="07b9d-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="07b9d-116">See Also</span></span>  
 [<span data-ttu-id="07b9d-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="07b9d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
