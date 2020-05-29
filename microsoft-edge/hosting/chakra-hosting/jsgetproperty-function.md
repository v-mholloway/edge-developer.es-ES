---
description: Obtiene la propiedad de un objeto.
title: Función JsGetProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ea0e5a3bad9363800d2b4a3a18ab932ecc384486
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574582"
---
# <span data-ttu-id="bbe4a-103">Función JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="bbe4a-103">JsGetProperty Function</span></span>
<span data-ttu-id="bbe4a-104">Obtiene la propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="bbe4a-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="bbe4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbe4a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="bbe4a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbe4a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bbe4a-107">Objeto que contiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bbe4a-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="bbe4a-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bbe4a-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="bbe4a-109">El valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bbe4a-109">The value of the property.</span></span>  
  
## <span data-ttu-id="bbe4a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbe4a-110">Return Value</span></span>  
 <span data-ttu-id="bbe4a-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="bbe4a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bbe4a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbe4a-112">Remarks</span></span>  
 <span data-ttu-id="bbe4a-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="bbe4a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bbe4a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbe4a-114">Requirements</span></span>  
 <span data-ttu-id="bbe4a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bbe4a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bbe4a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bbe4a-116">See Also</span></span>  
 [<span data-ttu-id="bbe4a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bbe4a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)