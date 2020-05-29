---
description: Establece el contexto de script actual en el hilo.
title: Función JsSetCurrentContext | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57620ad0e986034791ec07765d7cc115b958d661
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574518"
---
# <span data-ttu-id="26628-103">Función JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="26628-103">JsSetCurrentContext Function</span></span>
<span data-ttu-id="26628-104">Establece el contexto de script actual en el hilo.</span><span class="sxs-lookup"><span data-stu-id="26628-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="26628-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26628-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="26628-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26628-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="26628-107">Contexto de script que se va a convertir en actual.</span><span class="sxs-lookup"><span data-stu-id="26628-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="26628-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26628-108">Return Value</span></span>  
 <span data-ttu-id="26628-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="26628-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="26628-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26628-110">Example</span></span>

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

## <span data-ttu-id="26628-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26628-111">Requirements</span></span>  
 <span data-ttu-id="26628-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="26628-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="26628-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="26628-113">See Also</span></span>  
 [<span data-ttu-id="26628-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="26628-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)