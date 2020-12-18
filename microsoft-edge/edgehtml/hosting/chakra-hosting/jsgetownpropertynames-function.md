---
description: Obtiene la lista de todas las propiedades del objeto.
title: Función JsGetOwnPropertyNames | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d00788b6ef581b923413e5c71a63bb27398a326
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235885"
---
# <span data-ttu-id="2511f-103">Función JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="2511f-103">JsGetOwnPropertyNames Function</span></span>

<span data-ttu-id="2511f-104">Obtiene la lista de todas las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="2511f-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="2511f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2511f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="2511f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2511f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2511f-107">Objeto del que se obtienen los nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2511f-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="2511f-108">Una matriz de nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2511f-108">An array of property names.</span></span>  
  
## <span data-ttu-id="2511f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2511f-109">Return Value</span></span>  
 <span data-ttu-id="2511f-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="2511f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2511f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2511f-111">Remarks</span></span>  
 <span data-ttu-id="2511f-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="2511f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2511f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2511f-113">Requirements</span></span>  
 <span data-ttu-id="2511f-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2511f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2511f-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2511f-115">See Also</span></span>  
 [<span data-ttu-id="2511f-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2511f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
