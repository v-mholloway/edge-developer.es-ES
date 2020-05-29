---
description: Obtiene el objeto global en el contexto de script actual.
title: Función JsGetGlobalObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9f8b540485e75ef80d42ba66f031b3e827b475fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573455"
---
# <span data-ttu-id="add98-103">Función JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="add98-103">JsGetGlobalObject Function</span></span>
<span data-ttu-id="add98-104">Obtiene el objeto global en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="add98-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="add98-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="add98-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="add98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="add98-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="add98-107">Objeto global.</span><span class="sxs-lookup"><span data-stu-id="add98-107">The global object.</span></span>  
  
## <span data-ttu-id="add98-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="add98-108">Return Value</span></span>  
 <span data-ttu-id="add98-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="add98-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="add98-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="add98-110">Remarks</span></span>  
 <span data-ttu-id="add98-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="add98-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="add98-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="add98-112">Requirements</span></span>  
 <span data-ttu-id="add98-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="add98-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="add98-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="add98-114">See Also</span></span>  
 [<span data-ttu-id="add98-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="add98-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)