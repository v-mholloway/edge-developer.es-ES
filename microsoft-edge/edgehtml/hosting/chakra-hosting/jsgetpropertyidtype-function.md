---
description: Obtiene el tipo de propiedad.
title: Función JsGetPropertyIdType | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 93ee11bf74014361c89aa93bbb58361b426f573f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236463"
---
# <span data-ttu-id="dec15-103">Función JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="dec15-103">JsGetPropertyIdType Function</span></span>

<span data-ttu-id="dec15-104">Obtiene el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dec15-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="dec15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dec15-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="dec15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dec15-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="dec15-107">IDENTIFICADOR de propiedad del que se va a obtener el tipo.</span><span class="sxs-lookup"><span data-stu-id="dec15-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="dec15-108">El `JsPropertyIdType` del identificador de propiedad proporcionado.</span><span class="sxs-lookup"><span data-stu-id="dec15-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="dec15-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dec15-109">Return Value</span></span>  
 <span data-ttu-id="dec15-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="dec15-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dec15-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dec15-111">Remarks</span></span>  
 <span data-ttu-id="dec15-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="dec15-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="dec15-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dec15-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="dec15-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec15-114">Requirements</span></span>  
 <span data-ttu-id="dec15-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dec15-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dec15-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dec15-116">See Also</span></span>  
 [<span data-ttu-id="dec15-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dec15-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
