---
description: Obtiene la lista de todas las propiedades del objeto.
title: Función JsGetOwnPropertyNames | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5355caab864724d72fdb2c7abb3dc70e39662b55
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574584"
---
# <span data-ttu-id="e422d-103">Función JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="e422d-103">JsGetOwnPropertyNames Function</span></span>
<span data-ttu-id="e422d-104">Obtiene la lista de todas las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="e422d-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="e422d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e422d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="e422d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e422d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e422d-107">Objeto del que se obtienen los nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e422d-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="e422d-108">Una matriz de nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e422d-108">An array of property names.</span></span>  
  
## <span data-ttu-id="e422d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e422d-109">Return Value</span></span>  
 <span data-ttu-id="e422d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e422d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e422d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e422d-111">Remarks</span></span>  
 <span data-ttu-id="e422d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e422d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e422d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e422d-113">Requirements</span></span>  
 <span data-ttu-id="e422d-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e422d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e422d-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e422d-115">See Also</span></span>  
 [<span data-ttu-id="e422d-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e422d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)