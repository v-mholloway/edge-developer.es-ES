---
description: Obtiene el identificador de propiedad asociado al nombre.
title: Función JsGetPropertyIdFromName | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: adc8de4d55fa0c74ad191b4621ceb3a54026d02d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236430"
---
# <span data-ttu-id="55e15-103">Función JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="55e15-103">JsGetPropertyIdFromName Function</span></span>

<span data-ttu-id="55e15-104">Obtiene el identificador de propiedad asociado al nombre.</span><span class="sxs-lookup"><span data-stu-id="55e15-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="55e15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55e15-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="55e15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55e15-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="55e15-107">Nombre del identificador de propiedad que se va a obtener o crear.</span><span class="sxs-lookup"><span data-stu-id="55e15-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="55e15-108">El nombre puede constar solo de dígitos.</span><span class="sxs-lookup"><span data-stu-id="55e15-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="55e15-109">IDENTIFICADOR de propiedad en este Runtime para el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="55e15-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="55e15-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55e15-110">Return Value</span></span>  
 <span data-ttu-id="55e15-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="55e15-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="55e15-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55e15-112">Remarks</span></span>  
 <span data-ttu-id="55e15-113">Los identificadores de propiedad son específicos de un contexto y no se pueden usar en contextos.</span><span class="sxs-lookup"><span data-stu-id="55e15-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="55e15-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="55e15-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="55e15-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55e15-115">Requirements</span></span>  
 <span data-ttu-id="55e15-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="55e15-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="55e15-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="55e15-117">See Also</span></span>  
 [<span data-ttu-id="55e15-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="55e15-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
