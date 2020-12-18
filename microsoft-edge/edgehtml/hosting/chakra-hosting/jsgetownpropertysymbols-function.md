---
description: Obtiene la lista de todas las propiedades de símbolo en el objeto.
title: Función JsGetOwnPropertySymbols | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236446"
---
# <span data-ttu-id="e388d-103">Función JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="e388d-103">JsGetOwnPropertySymbols Function</span></span>

<span data-ttu-id="e388d-104">Obtiene la lista de todas las propiedades de símbolo en el objeto.</span><span class="sxs-lookup"><span data-stu-id="e388d-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="e388d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e388d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="e388d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e388d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e388d-107">Objeto del que se van a obtener los símbolos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e388d-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="e388d-108">Matriz de símbolos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e388d-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="e388d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e388d-109">Return Value</span></span>  
 <span data-ttu-id="e388d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e388d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e388d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e388d-111">Remarks</span></span>  
 <span data-ttu-id="e388d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e388d-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e388d-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e388d-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="e388d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e388d-114">Requirements</span></span>  
 <span data-ttu-id="e388d-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e388d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e388d-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e388d-116">See Also</span></span>  
 [<span data-ttu-id="e388d-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e388d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
