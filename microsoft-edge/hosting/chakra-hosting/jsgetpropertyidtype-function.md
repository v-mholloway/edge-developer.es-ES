---
description: Obtiene el tipo de propiedad.
title: Función JsGetPropertyIdType | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a43cfc2efd69cc14813ad88850afbf602d477d71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574579"
---
# <span data-ttu-id="9ae4c-103">Función JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="9ae4c-103">JsGetPropertyIdType Function</span></span>
<span data-ttu-id="9ae4c-104">Obtiene el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="9ae4c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ae4c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="9ae4c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ae4c-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="9ae4c-107">IDENTIFICADOR de propiedad del que se va a obtener el tipo.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="9ae4c-108">El `JsPropertyIdType` del identificador de propiedad proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="9ae4c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ae4c-109">Return Value</span></span>  
 <span data-ttu-id="9ae4c-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9ae4c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ae4c-111">Remarks</span></span>  
 <span data-ttu-id="9ae4c-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9ae4c-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="9ae4c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ae4c-114">Requirements</span></span>  
 <span data-ttu-id="9ae4c-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9ae4c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9ae4c-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="9ae4c-116">See Also</span></span>  
 [<span data-ttu-id="9ae4c-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)