---
description: Obtiene la longitud de un valor de cadena.
title: Función JsGetStringLength | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10fd6be4bb839ccb9eb64c99931cdb474e3aa7a2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236648"
---
# <span data-ttu-id="b25fb-103">Función JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="b25fb-103">JsGetStringLength Function</span></span>

<span data-ttu-id="b25fb-104">Obtiene la longitud de un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="b25fb-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="b25fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b25fb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="b25fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b25fb-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="b25fb-107">Valor de cadena para el que se va a obtener la longitud.</span><span class="sxs-lookup"><span data-stu-id="b25fb-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="b25fb-108">La longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b25fb-108">The length of the string.</span></span>  
  
## <span data-ttu-id="b25fb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b25fb-109">Return Value</span></span>  
 <span data-ttu-id="b25fb-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b25fb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b25fb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b25fb-111">Remarks</span></span>  
 <span data-ttu-id="b25fb-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b25fb-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b25fb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b25fb-113">Requirements</span></span>  
 <span data-ttu-id="b25fb-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b25fb-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b25fb-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b25fb-115">See Also</span></span>  
 [<span data-ttu-id="b25fb-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b25fb-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
