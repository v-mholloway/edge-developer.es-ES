---
description: Obtiene la longitud de un valor de cadena.
title: Función JsGetStringLength | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b562b2dc58341523910db41fb8b748453b2a836
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573443"
---
# <span data-ttu-id="0e94e-103">Función JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="0e94e-103">JsGetStringLength Function</span></span>
<span data-ttu-id="0e94e-104">Obtiene la longitud de un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="0e94e-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="0e94e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e94e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="0e94e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e94e-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="0e94e-107">Valor de cadena para el que se va a obtener la longitud.</span><span class="sxs-lookup"><span data-stu-id="0e94e-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="0e94e-108">La longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="0e94e-108">The length of the string.</span></span>  
  
## <span data-ttu-id="0e94e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e94e-109">Return Value</span></span>  
 <span data-ttu-id="0e94e-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0e94e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0e94e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e94e-111">Remarks</span></span>  
 <span data-ttu-id="0e94e-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="0e94e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0e94e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e94e-113">Requirements</span></span>  
 <span data-ttu-id="0e94e-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0e94e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0e94e-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0e94e-115">See Also</span></span>  
 [<span data-ttu-id="0e94e-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0e94e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)