---
description: Los scripts de tiempo de ejecución de JavaScript (JsRT) typedefs, constantes y enumeraciones admiten la incorporación de capacidades de scripting en aplicaciones de escritorio y de servidor que se ejecutan en Windows.
title: Constantes, enumeraciones y definiciones de tipo en tiempo de ejecución de JavaScript
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 1aa107ed-e144-4947-b5bb-90284a537174
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 20c52c3a958f6ba14fbfbdcdad794747a9c34949
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752265"
---
# <span data-ttu-id="bd5a4-103">Constantes, enumeraciones y definiciones de tipo en tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="bd5a4-103">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="bd5a4-104">Los scripts de tiempo de ejecución de JavaScript (JsRT) typedefs, constantes y enumeraciones admiten la incorporación de capacidades de scripting en aplicaciones de escritorio y de servidor que se ejecutan en Windows.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-104">JavaScript Runtime (JsRT) typedefs, constants, and enumerations support adding scripting capabilities to desktop and server-side applications running on Windows.</span></span>  

## <span data-ttu-id="bd5a4-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bd5a4-105">In this section</span></span>  

<span data-ttu-id="bd5a4-106">Las siguientes typedefs globales admiten hospedaje de JsRT:</span><span class="sxs-lookup"><span data-stu-id="bd5a4-106">The following global typedefs support JsRT hosting:</span></span>  

*   [<span data-ttu-id="bd5a4-107">Definición de tipo JsBackgroundWorkItemCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-107">JsBackgroundWorkItemCallback Typedef</span></span>](./jsbackgroundworkitemcallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-108">Definición de tipo JsBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-108">JsBeforeCollectCallback Typedef</span></span>](./jsbeforecollectcallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-109">Definición de tipo JsContextRef</span><span class="sxs-lookup"><span data-stu-id="bd5a4-109">JsContextRef Typedef</span></span>](./jscontextref-typedef.md)  
*   [<span data-ttu-id="bd5a4-110">Definición de tipo JsFinalizeCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-110">JsFinalizeCallback Typedef</span></span>](./jsfinalizecallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-111">Definición de tipo JsMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-111">JsMemoryAllocationCallback Typedef</span></span>](./jsmemoryallocationcallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-112">Definición de tipo JsNativeFunction</span><span class="sxs-lookup"><span data-stu-id="bd5a4-112">JsNativeFunction Typedef</span></span>](./jsnativefunction-typedef.md)  
*   [<span data-ttu-id="bd5a4-113">Definición de tipo JsObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-113">JsObjectBeforeCollectCallback Typedef</span></span>](./jsobjectbeforecollectcallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-114">Definición de tipo JsProjectionCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-114">JsProjectionCallback Typedef</span></span>](./jsprojectioncallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-115">Definición de tipo JsProjectionCallbackContext</span><span class="sxs-lookup"><span data-stu-id="bd5a4-115">JsProjectionCallbackContext Typedef</span></span>](./jsprojectioncallbackcontext-typedef.md)  
*   [<span data-ttu-id="bd5a4-116">Definición de tipo JsProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-116">JsProjectionEnqueueCallback Typedef</span></span>](./jsprojectionenqueuecallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-117">Definición de tipo JsPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-117">JsPromiseContinuationCallback Typedef</span></span>](./jspromisecontinuationcallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-118">Definición de tipo JsPropertyIdRef </span><span class="sxs-lookup"><span data-stu-id="bd5a4-118">JsPropertyIdRef Typedef</span></span>](./jspropertyidref-typedef.md)  
*   [<span data-ttu-id="bd5a4-119">Definición de tipo JsRef</span><span class="sxs-lookup"><span data-stu-id="bd5a4-119">JsRef Typedef</span></span>](./jsref-typedef.md)  
*   [<span data-ttu-id="bd5a4-120">Definición de tipo JsRuntimeHandle</span><span class="sxs-lookup"><span data-stu-id="bd5a4-120">JsRuntimeHandle Typedef</span></span>](./jsruntimehandle-typedef.md)  
*   [<span data-ttu-id="bd5a4-121">Definición de tipo JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-121">JsSerializedScriptLoadSourceCallback Typedef</span></span>](./jsserializedscriptloadsourcecallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-122">Definición de tipo JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-122">JsSerializedScriptUnloadCallback typedef</span></span>](./jsserializedscriptunloadcallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-123">Definición de tipo JsSourceContext</span><span class="sxs-lookup"><span data-stu-id="bd5a4-123">JsSourceContext Typedef</span></span>](./jssourcecontext-typedef.md)  
*   [<span data-ttu-id="bd5a4-124">Definición de tipo JsThreadServiceCallback</span><span class="sxs-lookup"><span data-stu-id="bd5a4-124">JsThreadServiceCallback Typedef</span></span>](./jsthreadservicecallback-typedef.md)  
*   [<span data-ttu-id="bd5a4-125">Definición de tipo JsValueRef</span><span class="sxs-lookup"><span data-stu-id="bd5a4-125">JsValueRef Typedef</span></span>](./jsvalueref-typedef.md)  

<span data-ttu-id="bd5a4-126">Las siguientes constantes son compatibles con hospedaje de JsRT:</span><span class="sxs-lookup"><span data-stu-id="bd5a4-126">The following constants support JsRT hosting:</span></span>  

*   [<span data-ttu-id="bd5a4-127">Constante JS_INVALID_PROPERTYID</span><span class="sxs-lookup"><span data-stu-id="bd5a4-127">JS_INVALID_PROPERTYID Constant</span></span>](./js-invalid-propertyid-constant.md)  
*   [<span data-ttu-id="bd5a4-128">Constante JS_INVALID_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="bd5a4-128">JS_INVALID_REFERENCE Constant</span></span>](./js-invalid-reference-constant.md)  
*   [<span data-ttu-id="bd5a4-129">Constante JS_INVALID_RUNTIME_HANDLE</span><span class="sxs-lookup"><span data-stu-id="bd5a4-129">JS_INVALID_RUNTIME_HANDLE Constant</span></span>](./js-invalid-runtime-handle-constant.md)  
*   [<span data-ttu-id="bd5a4-130">Constante JS_SOURCE_CONTEXT_NONE</span><span class="sxs-lookup"><span data-stu-id="bd5a4-130">JS_SOURCE_CONTEXT_NONE Constant</span></span>](./js-source-context-none-constant.md)  

<span data-ttu-id="bd5a4-131">Las siguientes enumeraciones admiten hospedaje de JsRT:</span><span class="sxs-lookup"><span data-stu-id="bd5a4-131">The following enumerations support JsRT hosting:</span></span>  

*   [<span data-ttu-id="bd5a4-132">Enumeración JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="bd5a4-132">JsErrorCode Enumeration</span></span>](./jserrorcode-enumeration.md)  
*   [<span data-ttu-id="bd5a4-133">Enumeración JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="bd5a4-133">JsMemoryEventType Enumeration</span></span>](./jsmemoryeventtype-enumeration.md)  
*   [<span data-ttu-id="bd5a4-134">Enumeración JsPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="bd5a4-134">JsPropertyIdType Enumeration</span></span>](./jspropertyidtype-enumeration.md)  
*   [<span data-ttu-id="bd5a4-135">Enumeración JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="bd5a4-135">JsRuntimeAttributes Enumeration</span></span>](./jsruntimeattributes-enumeration.md)  
*   [<span data-ttu-id="bd5a4-136">Enumeración JsRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="bd5a4-136">JsRuntimeVersion Enumeration</span></span>](./jsruntimeversion-enumeration.md)  
*   [<span data-ttu-id="bd5a4-137">Enumeración JsTypedArrayType</span><span class="sxs-lookup"><span data-stu-id="bd5a4-137">JsTypedArrayType Enumeration</span></span>](./jstypedarraytype-enumeration.md)  
*   [<span data-ttu-id="bd5a4-138">Enumeración de JsValueType</span><span class="sxs-lookup"><span data-stu-id="bd5a4-138">JsValueType Enumeration</span></span>](./jsvaluetype-enumeration.md)  

## <span data-ttu-id="bd5a4-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd5a4-139">See also</span></span>  

*   [<span data-ttu-id="bd5a4-140">Hospedar el tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="bd5a4-140">Hosting the JavaScript Runtime</span></span>](./hosting-the-javascript-runtime.md)  
*   [<span data-ttu-id="bd5a4-141">Hospedaje en tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="bd5a4-141">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)  
