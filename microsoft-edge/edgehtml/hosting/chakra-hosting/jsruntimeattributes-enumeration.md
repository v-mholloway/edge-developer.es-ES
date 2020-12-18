---
description: 'Atributos de un Runtime. '
title: JsRuntimeAttributes (enumeración) | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbc5341c3214d9796278d334507e284989ff45dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236202"
---
# <span data-ttu-id="d65b3-103">Enumeración JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="d65b3-103">JsRuntimeAttributes Enumeration</span></span>

<span data-ttu-id="d65b3-104">Atributos de un Runtime.</span><span class="sxs-lookup"><span data-stu-id="d65b3-104">Attributes of a runtime.</span></span>  
  
## <span data-ttu-id="d65b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d65b3-105">Syntax</span></span>  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## <span data-ttu-id="d65b3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d65b3-106">Members</span></span>  
  
### <span data-ttu-id="d65b3-107">Los</span><span class="sxs-lookup"><span data-stu-id="d65b3-107">Values</span></span>  
  
|<span data-ttu-id="d65b3-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="d65b3-108">Name</span></span>|<span data-ttu-id="d65b3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d65b3-109">Description</span></span>|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|<span data-ttu-id="d65b3-110">El motor en tiempo de ejecución debe admitir una interrupción de script confiable.</span><span class="sxs-lookup"><span data-stu-id="d65b3-110">The runtime should support reliable script interruption.</span></span> <span data-ttu-id="d65b3-111">Esto aumenta el número de lugares en los que el motor en tiempo de ejecución buscará una solicitud de interrupción de script a costa de una pequeña cantidad de rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d65b3-111">This increases the number of places where the runtime will check for a script interrupt request at the cost of a small amount of runtime performance.</span></span>|  
|`JsRuntimeAttributeDisableBackgroundWork`|<span data-ttu-id="d65b3-112">El motor en tiempo de ejecución no realizará ningún trabajo (como la recolección de elementos no utilizados) en subprocesos en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d65b3-112">The runtime will not do any work (such as garbage collection) on background threads.</span></span>|  
|`JsRuntimeAttributeDisableEval`|<span data-ttu-id="d65b3-113">El uso del `eval` `function` constructor or inicia una excepción.</span><span class="sxs-lookup"><span data-stu-id="d65b3-113">Using `eval` or `function` constructor will throw an exception.</span></span>|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|<span data-ttu-id="d65b3-114">El motor en tiempo de ejecución no generará código nativo.</span><span class="sxs-lookup"><span data-stu-id="d65b3-114">Runtime will not generate native code.</span></span>|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|<span data-ttu-id="d65b3-115">El motor en tiempo de ejecución habilitará todas las características experimentales.</span><span class="sxs-lookup"><span data-stu-id="d65b3-115">Runtime will enable all experimental features.</span></span>|  
|`JsRuntimeAttributeEnableIdleProcessing`|<span data-ttu-id="d65b3-116">El anfitrión llama `JsIdle` , así que habilita el procesamiento de inactividad.</span><span class="sxs-lookup"><span data-stu-id="d65b3-116">Host will call `JsIdle`, so enable idle processing.</span></span> <span data-ttu-id="d65b3-117">De lo contrario, el motor en tiempo de ejecución administrará la memoria de forma ligeramente más agresiva.</span><span class="sxs-lookup"><span data-stu-id="d65b3-117">Otherwise, the runtime will manage memory slightly more aggressively.</span></span>|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|<span data-ttu-id="d65b3-118">Las llamadas `JsSetException` también enviarán la excepción al depurador de script (si existe), lo que proporciona al depurador una oportunidad de interrumpir la excepción.</span><span class="sxs-lookup"><span data-stu-id="d65b3-118">Calling `JsSetException` will also dispatch the exception to the script debugger (if any) giving the debugger a chance to break on the exception.</span></span>|  
|`JsRuntimeAttributeNone`|<span data-ttu-id="d65b3-119">Sin atributos especiales.</span><span class="sxs-lookup"><span data-stu-id="d65b3-119">No special attributes.</span></span>|  
  
## <span data-ttu-id="d65b3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d65b3-120">Requirements</span></span>  
 <span data-ttu-id="d65b3-121">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d65b3-121">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d65b3-122">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d65b3-122">See Also</span></span>  
 [<span data-ttu-id="d65b3-123">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d65b3-123">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
