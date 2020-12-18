---
description: Obtiene el objeto global en el contexto de script actual.
title: Función JsGetGlobalObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cda960710180c135b99abd359d0cc76776ff0225
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236322"
---
# <span data-ttu-id="bfb17-103">Función JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="bfb17-103">JsGetGlobalObject Function</span></span>

<span data-ttu-id="bfb17-104">Obtiene el objeto global en el contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="bfb17-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="bfb17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfb17-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="bfb17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfb17-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="bfb17-107">Objeto global.</span><span class="sxs-lookup"><span data-stu-id="bfb17-107">The global object.</span></span>  
  
## <span data-ttu-id="bfb17-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfb17-108">Return Value</span></span>  
 <span data-ttu-id="bfb17-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="bfb17-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bfb17-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfb17-110">Remarks</span></span>  
 <span data-ttu-id="bfb17-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="bfb17-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bfb17-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb17-112">Requirements</span></span>  
 <span data-ttu-id="bfb17-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bfb17-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bfb17-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bfb17-114">See Also</span></span>  
 [<span data-ttu-id="bfb17-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bfb17-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
