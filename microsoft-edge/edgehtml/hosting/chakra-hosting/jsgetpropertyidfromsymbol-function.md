---
description: Obtiene el identificador de propiedad asociado al símbolo.
title: Función JsGetPropertyIdFromSymbol | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97f1fb517164d692cdd010f899dc40d2e3596ed
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236464"
---
# <span data-ttu-id="e1751-103">Función JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="e1751-103">JsGetPropertyIdFromSymbol Function</span></span>

<span data-ttu-id="e1751-104">Obtiene el identificador de propiedad asociado al símbolo.</span><span class="sxs-lookup"><span data-stu-id="e1751-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="e1751-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1751-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="e1751-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1751-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="e1751-107">Símbolo cuyo identificador de propiedad se está recuperando.</span><span class="sxs-lookup"><span data-stu-id="e1751-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="e1751-108">IDENTIFICADOR de propiedad del símbolo dado.</span><span class="sxs-lookup"><span data-stu-id="e1751-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="e1751-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1751-109">Return Value</span></span>  
 <span data-ttu-id="e1751-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e1751-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e1751-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1751-111">Remarks</span></span>  
 <span data-ttu-id="e1751-112">Los identificadores de propiedad son específicos de un contexto y no se pueden usar en contextos.</span><span class="sxs-lookup"><span data-stu-id="e1751-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="e1751-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e1751-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e1751-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1751-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="e1751-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1751-115">Requirements</span></span>  
 <span data-ttu-id="e1751-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1751-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1751-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e1751-117">See Also</span></span>  
 [<span data-ttu-id="e1751-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e1751-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
