---
description: Obtiene la lista de todas las propiedades de símbolo en el objeto.
title: Función JsGetOwnPropertySymbols | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7a7f4e88986a45fbccfae0c53e92ff2e5313991
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574585"
---
# <span data-ttu-id="7546a-103">Función JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="7546a-103">JsGetOwnPropertySymbols Function</span></span>
<span data-ttu-id="7546a-104">Obtiene la lista de todas las propiedades de símbolo en el objeto.</span><span class="sxs-lookup"><span data-stu-id="7546a-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="7546a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7546a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="7546a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7546a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7546a-107">Objeto del que se van a obtener los símbolos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7546a-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="7546a-108">Matriz de símbolos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7546a-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="7546a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7546a-109">Return Value</span></span>  
 <span data-ttu-id="7546a-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7546a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7546a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7546a-111">Remarks</span></span>  
 <span data-ttu-id="7546a-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7546a-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="7546a-113">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7546a-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="7546a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7546a-114">Requirements</span></span>  
 <span data-ttu-id="7546a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7546a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7546a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7546a-116">See Also</span></span>  
 [<span data-ttu-id="7546a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7546a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)