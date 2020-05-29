---
description: Obtiene el símbolo asociado al identificador de propiedad.
title: Función JsGetSymbolFromPropertyId | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6902384772f29f80751660ce2d4a295d2ea620ab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573439"
---
# <span data-ttu-id="859bc-103">Función JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="859bc-103">JsGetSymbolFromPropertyId Function</span></span>
<span data-ttu-id="859bc-104">Obtiene el símbolo asociado al identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="859bc-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="859bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="859bc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="859bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="859bc-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="859bc-107">IDENTIFICADOR de propiedad del que se va a obtener el símbolo.</span><span class="sxs-lookup"><span data-stu-id="859bc-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="859bc-108">Símbolo asociado al identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="859bc-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="859bc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="859bc-109">Return Value</span></span>  
 <span data-ttu-id="859bc-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="859bc-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="859bc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="859bc-111">Remarks</span></span>  
 <span data-ttu-id="859bc-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="859bc-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="859bc-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="859bc-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="859bc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="859bc-114">Requirements</span></span>  
 <span data-ttu-id="859bc-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="859bc-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="859bc-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="859bc-116">See Also</span></span>  
 [<span data-ttu-id="859bc-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="859bc-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)