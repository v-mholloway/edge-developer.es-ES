---
description: Convierte el valor en objeto usando la semántica estándar de JavaScript.
title: Función JsConvertValueToObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6a8b1a8933cdcaaf250a2e28ed8fc758ea66cc0e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573517"
---
# <span data-ttu-id="91fcd-103">Función JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="91fcd-103">JsConvertValueToObject Function</span></span>
<span data-ttu-id="91fcd-104">Convierte el valor en objeto usando la semántica estándar de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="91fcd-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="91fcd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91fcd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="91fcd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91fcd-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="91fcd-107">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="91fcd-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="91fcd-108">El valor convertido.</span><span class="sxs-lookup"><span data-stu-id="91fcd-108">The converted value.</span></span>  
  
## <span data-ttu-id="91fcd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91fcd-109">Return Value</span></span>  
 <span data-ttu-id="91fcd-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="91fcd-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="91fcd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91fcd-111">Remarks</span></span>  
 <span data-ttu-id="91fcd-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="91fcd-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="91fcd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91fcd-113">Requirements</span></span>  
 <span data-ttu-id="91fcd-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="91fcd-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="91fcd-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="91fcd-115">See Also</span></span>  
 [<span data-ttu-id="91fcd-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="91fcd-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)