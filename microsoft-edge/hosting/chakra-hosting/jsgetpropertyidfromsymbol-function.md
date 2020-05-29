---
description: Obtiene el identificador de propiedad asociado al símbolo.
title: Función JsGetPropertyIdFromSymbol | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0d11dbaf25b85e2bcd85a0cf2bac1b499fd4fa3e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574581"
---
# <span data-ttu-id="4b45d-103">Función JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="4b45d-103">JsGetPropertyIdFromSymbol Function</span></span>
<span data-ttu-id="4b45d-104">Obtiene el identificador de propiedad asociado al símbolo.</span><span class="sxs-lookup"><span data-stu-id="4b45d-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="4b45d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b45d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="4b45d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b45d-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="4b45d-107">Símbolo cuyo identificador de propiedad se está recuperando.</span><span class="sxs-lookup"><span data-stu-id="4b45d-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="4b45d-108">IDENTIFICADOR de propiedad del símbolo dado.</span><span class="sxs-lookup"><span data-stu-id="4b45d-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="4b45d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b45d-109">Return Value</span></span>  
 <span data-ttu-id="4b45d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4b45d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4b45d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b45d-111">Remarks</span></span>  
 <span data-ttu-id="4b45d-112">Los identificadores de propiedad son específicos de un contexto y no se pueden usar en contextos.</span><span class="sxs-lookup"><span data-stu-id="4b45d-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="4b45d-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="4b45d-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4b45d-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4b45d-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4b45d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b45d-115">Requirements</span></span>  
 <span data-ttu-id="4b45d-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4b45d-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4b45d-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="4b45d-117">See Also</span></span>  
 [<span data-ttu-id="4b45d-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4b45d-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)