---
description: Obtiene el identificador de propiedad asociado al nombre.
title: Función JsGetPropertyIdFromName | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e1954b86937056523a30c15dbf350ac02fd63dde
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574580"
---
# <span data-ttu-id="89c76-103">Función JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="89c76-103">JsGetPropertyIdFromName Function</span></span>
<span data-ttu-id="89c76-104">Obtiene el identificador de propiedad asociado al nombre.</span><span class="sxs-lookup"><span data-stu-id="89c76-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="89c76-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89c76-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="89c76-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89c76-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="89c76-107">Nombre del identificador de propiedad que se va a obtener o crear.</span><span class="sxs-lookup"><span data-stu-id="89c76-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="89c76-108">El nombre puede constar solo de dígitos.</span><span class="sxs-lookup"><span data-stu-id="89c76-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="89c76-109">IDENTIFICADOR de propiedad en este Runtime para el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="89c76-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="89c76-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89c76-110">Return Value</span></span>  
 <span data-ttu-id="89c76-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="89c76-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="89c76-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89c76-112">Remarks</span></span>  
 <span data-ttu-id="89c76-113">Los identificadores de propiedad son específicos de un contexto y no se pueden usar en contextos.</span><span class="sxs-lookup"><span data-stu-id="89c76-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="89c76-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="89c76-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="89c76-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89c76-115">Requirements</span></span>  
 <span data-ttu-id="89c76-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="89c76-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="89c76-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="89c76-117">See Also</span></span>  
 [<span data-ttu-id="89c76-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="89c76-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)