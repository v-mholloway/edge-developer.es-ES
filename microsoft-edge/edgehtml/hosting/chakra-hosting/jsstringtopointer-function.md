---
description: Recupera el puntero de cadena de un valor de cadena.
title: Función JsStringToPointer | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236234"
---
# <span data-ttu-id="6da2c-103">Función JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="6da2c-103">JsStringToPointer Function</span></span>

<span data-ttu-id="6da2c-104">Recupera el puntero de cadena de un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="6da2c-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="6da2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6da2c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="6da2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6da2c-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="6da2c-107">Valor de cadena que se va a convertir en un puntero de cadena.</span><span class="sxs-lookup"><span data-stu-id="6da2c-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="6da2c-108">Puntero de cadena.</span><span class="sxs-lookup"><span data-stu-id="6da2c-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="6da2c-109">La longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="6da2c-109">The length of the string.</span></span>  
  
## <span data-ttu-id="6da2c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6da2c-110">Return Value</span></span>  
 <span data-ttu-id="6da2c-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6da2c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6da2c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6da2c-112">Remarks</span></span>  
 <span data-ttu-id="6da2c-113">Esta función recupera el puntero de cadena de un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="6da2c-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="6da2c-114">Se producirá un error `JsErrorInvalidArgument` si el tipo del valor no es una cadena.</span><span class="sxs-lookup"><span data-stu-id="6da2c-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="6da2c-115">La duración de la cadena devuelta será la misma que la del valor que viene de lo procede, pero el puntero de cadena no se considera una referencia al valor (y, por lo tanto, no se conservará).</span><span class="sxs-lookup"><span data-stu-id="6da2c-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="6da2c-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="6da2c-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6da2c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6da2c-117">Requirements</span></span>  
 <span data-ttu-id="6da2c-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6da2c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6da2c-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6da2c-119">See Also</span></span>  
 [<span data-ttu-id="6da2c-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6da2c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
