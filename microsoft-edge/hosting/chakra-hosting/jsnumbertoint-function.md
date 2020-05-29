---
description: Recupera el `int` valor de un valor numérico.
title: Función JsNumberToInt | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574557"
---
# <span data-ttu-id="622c3-103">Función JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="622c3-103">JsNumberToInt Function</span></span>
<span data-ttu-id="622c3-104">Recupera el `int` valor de un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="622c3-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="622c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="622c3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="622c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="622c3-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="622c3-107">Valor numérico que se va a convertir en un `int` valor.</span><span class="sxs-lookup"><span data-stu-id="622c3-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="622c3-108">El `int` valor.</span><span class="sxs-lookup"><span data-stu-id="622c3-108">The `int` value.</span></span>  
  
## <span data-ttu-id="622c3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="622c3-109">Return Value</span></span>  
  
## <span data-ttu-id="622c3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="622c3-110">Remarks</span></span>  
 <span data-ttu-id="622c3-111">Esta función recupera el valor de un valor de número y lo convierte en un `int` valor.</span><span class="sxs-lookup"><span data-stu-id="622c3-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="622c3-112">Se producirá un error `JsErrorInvalidArgument` si el tipo del valor no es número.</span><span class="sxs-lookup"><span data-stu-id="622c3-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="622c3-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="622c3-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="622c3-114">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="622c3-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="622c3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="622c3-115">Requirements</span></span>  
 <span data-ttu-id="622c3-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="622c3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="622c3-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="622c3-117">See Also</span></span>  
 [<span data-ttu-id="622c3-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="622c3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)