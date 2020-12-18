---
description: Obtiene el contexto de script actual en el hilo.
title: Función JsGetCurrentContext | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236330"
---
# <span data-ttu-id="31a29-103">Función JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="31a29-103">JsGetCurrentContext Function</span></span>

<span data-ttu-id="31a29-104">Obtiene el contexto de script actual en el hilo.</span><span class="sxs-lookup"><span data-stu-id="31a29-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="31a29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31a29-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="31a29-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31a29-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="31a29-107">El contexto de script actual en el hilo, NULL si no hay ningún contexto de script actual.</span><span class="sxs-lookup"><span data-stu-id="31a29-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="31a29-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31a29-108">Return Value</span></span>  
 <span data-ttu-id="31a29-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="31a29-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="31a29-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31a29-110">Requirements</span></span>  
 <span data-ttu-id="31a29-111">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="31a29-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="31a29-112">Consulta también</span><span class="sxs-lookup"><span data-stu-id="31a29-112">See Also</span></span>  
 [<span data-ttu-id="31a29-113">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="31a29-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
