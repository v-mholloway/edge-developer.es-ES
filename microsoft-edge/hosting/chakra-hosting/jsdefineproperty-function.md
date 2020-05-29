---
description: Define la propiedad de un nuevo objeto desde un descriptor de propiedades.
title: Función JsDefineProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c9641b4d00540670b44d1718a6aa2aca3b02de
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573477"
---
# <span data-ttu-id="6800f-103">Función JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="6800f-103">JsDefineProperty Function</span></span>
<span data-ttu-id="6800f-104">Define la propiedad de un nuevo objeto desde un descriptor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6800f-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="6800f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6800f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="6800f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6800f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6800f-107">Objeto que tiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6800f-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="6800f-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6800f-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="6800f-109">Descriptor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6800f-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="6800f-110">Si se definió la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6800f-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="6800f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6800f-111">Return Value</span></span>  
 <span data-ttu-id="6800f-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6800f-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6800f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6800f-113">Remarks</span></span>  
 <span data-ttu-id="6800f-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="6800f-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6800f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6800f-115">Requirements</span></span>  
 <span data-ttu-id="6800f-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6800f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6800f-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6800f-117">See Also</span></span>  
 [<span data-ttu-id="6800f-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6800f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)