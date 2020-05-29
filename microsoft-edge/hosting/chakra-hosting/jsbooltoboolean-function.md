---
description: Crea un valor booleano a partir de un `bool` valor.
title: Función JsBoolToBoolean | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f795bdd02a2a21dc4a0c8948a76ef817d6e0fac6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573533"
---
# <span data-ttu-id="b795b-103">Función JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="b795b-103">JsBoolToBoolean Function</span></span>
<span data-ttu-id="b795b-104">Crea un valor booleano a partir de un `bool` valor.</span><span class="sxs-lookup"><span data-stu-id="b795b-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="b795b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b795b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="b795b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b795b-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="b795b-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="b795b-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="b795b-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="b795b-108">The converted value.</span></span>  
  
## <span data-ttu-id="b795b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b795b-109">Return Value</span></span>  
 <span data-ttu-id="b795b-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b795b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b795b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b795b-111">Remarks</span></span>  
 <span data-ttu-id="b795b-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b795b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b795b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b795b-113">Requirements</span></span>  
 <span data-ttu-id="b795b-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b795b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b795b-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b795b-115">See Also</span></span>  
 [<span data-ttu-id="b795b-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b795b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)