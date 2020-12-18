---
description: Establece el contexto de script actual en el hilo.
title: Función JsSetCurrentContext | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60ec1760c582f1f6771a5af64f59c4a77b1a43f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236238"
---
# <span data-ttu-id="593c9-103">Función JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="593c9-103">JsSetCurrentContext Function</span></span>

<span data-ttu-id="593c9-104">Establece el contexto de script actual en el hilo.</span><span class="sxs-lookup"><span data-stu-id="593c9-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="593c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="593c9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="593c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="593c9-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="593c9-107">Contexto de script que se va a convertir en actual.</span><span class="sxs-lookup"><span data-stu-id="593c9-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="593c9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="593c9-108">Return Value</span></span>  
 <span data-ttu-id="593c9-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="593c9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="593c9-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="593c9-110">Example</span></span>

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## <span data-ttu-id="593c9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="593c9-111">Requirements</span></span>  
 <span data-ttu-id="593c9-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="593c9-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="593c9-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="593c9-113">See Also</span></span>  
 [<span data-ttu-id="593c9-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="593c9-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
