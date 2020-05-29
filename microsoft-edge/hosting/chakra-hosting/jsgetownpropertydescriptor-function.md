---
description: Obtiene un descriptor de propiedad para la propiedad de un objeto.
title: Función JsGetOwnPropertyDescriptor | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6f500aec8b892cb2ad437bd7159ab14165a8bfb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574591"
---
# <span data-ttu-id="d223a-103">Función JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="d223a-103">JsGetOwnPropertyDescriptor Function</span></span>
<span data-ttu-id="d223a-104">Obtiene un descriptor de propiedad para la propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d223a-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="d223a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d223a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="d223a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d223a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="d223a-107">Objeto que tiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d223a-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="d223a-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d223a-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="d223a-109">Descriptor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d223a-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="d223a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d223a-110">Return Value</span></span>  
 <span data-ttu-id="d223a-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d223a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d223a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d223a-112">Remarks</span></span>  
 <span data-ttu-id="d223a-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="d223a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d223a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d223a-114">Requirements</span></span>  
 <span data-ttu-id="d223a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d223a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d223a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d223a-116">See Also</span></span>  
 [<span data-ttu-id="d223a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d223a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)