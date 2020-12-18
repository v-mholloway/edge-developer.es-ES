---
description: Obtiene el símbolo asociado al identificador de propiedad.
title: Función JsGetSymbolFromPropertyId | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472253aea228ca0374c42d99710a7a7ab528184c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236647"
---
# <span data-ttu-id="5e622-103">Función JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="5e622-103">JsGetSymbolFromPropertyId Function</span></span>

<span data-ttu-id="5e622-104">Obtiene el símbolo asociado al identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5e622-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="5e622-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e622-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="5e622-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e622-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="5e622-107">IDENTIFICADOR de propiedad del que se va a obtener el símbolo.</span><span class="sxs-lookup"><span data-stu-id="5e622-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="5e622-108">Símbolo asociado al identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5e622-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="5e622-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e622-109">Return Value</span></span>  
 <span data-ttu-id="5e622-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="5e622-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5e622-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e622-111">Remarks</span></span>  
 <span data-ttu-id="5e622-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="5e622-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5e622-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e622-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="5e622-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e622-114">Requirements</span></span>  
 <span data-ttu-id="5e622-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5e622-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5e622-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5e622-116">See Also</span></span>  
 [<span data-ttu-id="5e622-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5e622-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
