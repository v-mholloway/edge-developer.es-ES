---
description: Obtiene el nombre asociado al identificador de propiedad.
title: Función JsGetPropertyNameFromId | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e76c69c1d746302bb95cd7229872845c4fbcc88
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573451"
---
# <span data-ttu-id="c9589-103">Función JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="c9589-103">JsGetPropertyNameFromId Function</span></span>
<span data-ttu-id="c9589-104">Obtiene el nombre asociado al identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9589-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="c9589-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9589-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="c9589-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9589-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="c9589-107">IDENTIFICADOR de propiedad para obtener el nombre.</span><span class="sxs-lookup"><span data-stu-id="c9589-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="c9589-108">Nombre asociado al identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9589-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="c9589-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9589-109">Return Value</span></span>  
 <span data-ttu-id="c9589-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c9589-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c9589-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9589-111">Remarks</span></span>  
 <span data-ttu-id="c9589-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="c9589-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c9589-113">El búfer devuelto es válido siempre que el Runtime esté activo y no se pueda usar una vez que el Runtime se haya eliminado.</span><span class="sxs-lookup"><span data-stu-id="c9589-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="c9589-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9589-114">Requirements</span></span>  
 <span data-ttu-id="c9589-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c9589-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c9589-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c9589-116">See Also</span></span>  
 [<span data-ttu-id="c9589-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c9589-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)