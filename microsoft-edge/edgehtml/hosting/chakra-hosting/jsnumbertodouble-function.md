---
description: Recupera el `double` valor de un valor numérico.
title: Función JsNumberToDouble | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e4ae744f091045116a639aff619c475c7c7025f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236421"
---
# <span data-ttu-id="70397-103">Función JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="70397-103">JsNumberToDouble Function</span></span>

<span data-ttu-id="70397-104">Recupera el `double` valor de un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="70397-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="70397-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70397-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="70397-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70397-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="70397-107">Valor de número que se va a convertir en un `double` valor.</span><span class="sxs-lookup"><span data-stu-id="70397-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="70397-108">El `double` valor.</span><span class="sxs-lookup"><span data-stu-id="70397-108">The `double` value.</span></span>  
  
## <span data-ttu-id="70397-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70397-109">Return Value</span></span>  
 <span data-ttu-id="70397-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="70397-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="70397-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70397-111">Remarks</span></span>  
 <span data-ttu-id="70397-112">Esta función recupera el valor de un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="70397-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="70397-113">Se producirá un error `JsErrorInvalidArgument` si el tipo del valor no es número.</span><span class="sxs-lookup"><span data-stu-id="70397-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="70397-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="70397-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="70397-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70397-115">Requirements</span></span>  
 <span data-ttu-id="70397-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="70397-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="70397-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="70397-117">See Also</span></span>  
 [<span data-ttu-id="70397-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="70397-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
