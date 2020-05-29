---
description: Obtiene el contexto de script actual en el hilo.
title: Función JsGetCurrentContext | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 78f04674aab8783c43f22516903669e0f9b7543b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573463"
---
# <span data-ttu-id="e69e1-103">Función JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="e69e1-103">JsGetCurrentContext Function</span></span>
<span data-ttu-id="e69e1-104">Obtiene el contexto de script actual en el hilo.</span><span class="sxs-lookup"><span data-stu-id="e69e1-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="e69e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e69e1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="e69e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e69e1-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="e69e1-107">El contexto de script actual en el hilo, NULL si no hay ningún contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="e69e1-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="e69e1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e69e1-108">Return Value</span></span>  
 <span data-ttu-id="e69e1-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e69e1-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e69e1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e69e1-110">Requirements</span></span>  
 <span data-ttu-id="e69e1-111">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e69e1-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e69e1-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e69e1-112">See Also</span></span>  
 [<span data-ttu-id="e69e1-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e69e1-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)