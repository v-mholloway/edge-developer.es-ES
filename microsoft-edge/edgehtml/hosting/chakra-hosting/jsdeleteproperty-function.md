---
description: Elimina la propiedad de un objeto.
title: Función JsDeleteProperty | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55089bd4cff7ef4d58bcce1d7531d4ca1c7381ae
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235911"
---
# <span data-ttu-id="e134c-103">Función JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="e134c-103">JsDeleteProperty Function</span></span>

<span data-ttu-id="e134c-104">Elimina la propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="e134c-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="e134c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e134c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="e134c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e134c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e134c-107">Objeto que contiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e134c-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="e134c-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e134c-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="e134c-109">El conjunto de propiedades debe seguir las reglas de modo estricto.</span><span class="sxs-lookup"><span data-stu-id="e134c-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="e134c-110">Si se eliminó la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e134c-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="e134c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e134c-111">Return Value</span></span>  
 <span data-ttu-id="e134c-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e134c-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e134c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e134c-113">Remarks</span></span>  
 <span data-ttu-id="e134c-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e134c-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e134c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e134c-115">Requirements</span></span>  
 <span data-ttu-id="e134c-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e134c-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e134c-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e134c-117">See Also</span></span>  
 [<span data-ttu-id="e134c-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e134c-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
