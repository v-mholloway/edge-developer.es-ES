---
description: Un código de error devuelto desde una API de hospedaje de Chakra.
title: JsErrorCode (enumeración) | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3d1a319872ac69b2acaf19997f3c38f9c04597b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574601"
---
# <span data-ttu-id="7df18-103">Enumeración JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="7df18-103">JsErrorCode Enumeration</span></span>
<span data-ttu-id="7df18-104">Un código de error devuelto desde una API de hospedaje de Chakra.</span><span class="sxs-lookup"><span data-stu-id="7df18-104">An error code returned from a Chakra hosting API.</span></span>  
  
## <span data-ttu-id="7df18-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7df18-105">Syntax</span></span>  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## <span data-ttu-id="7df18-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7df18-106">Members</span></span>  
  
### <span data-ttu-id="7df18-107">Los</span><span class="sxs-lookup"><span data-stu-id="7df18-107">Values</span></span>  
  
|<span data-ttu-id="7df18-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="7df18-108">Name</span></span>|<span data-ttu-id="7df18-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7df18-109">Description</span></span>|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|<span data-ttu-id="7df18-110">El contexto no puede ponerse en un estado de depuración porque ya se encuentra en estado de depuración.</span><span class="sxs-lookup"><span data-stu-id="7df18-110">The context cannot be put into a debug state because it is already in a debug state.</span></span>|  
|`JsErrorAlreadyProfilingContext`|<span data-ttu-id="7df18-111">El contexto no puede iniciar la generación de perfiles porque ya está generando perfiles.</span><span class="sxs-lookup"><span data-stu-id="7df18-111">The context cannot start profiling because it is already profiling.</span></span>|  
|`JsErrorArgumentNotObject`|<span data-ttu-id="7df18-112">Se llamó a una API de hospedaje que opera en valores de objeto con un valor que no es un objeto.</span><span class="sxs-lookup"><span data-stu-id="7df18-112">A hosting API that operates on object values was called with a non-object value.</span></span>|  
|`JsErrorBadSerializedScript`|<span data-ttu-id="7df18-113">Se usó una secuencia de comandos en serie incorrecta o la secuencia de comandos serializada fue serializada por una versión diferente del motor de Chakra.</span><span class="sxs-lookup"><span data-stu-id="7df18-113">A bad serialized script was used, or the serialized script was serialized by a different version of the Chakra engine.</span></span>|  
|`JsErrorCannotDisableExecution`|<span data-ttu-id="7df18-114">El motor en tiempo de ejecución no admite interrupciones de script confiables.</span><span class="sxs-lookup"><span data-stu-id="7df18-114">Runtime does not support reliable script interruption.</span></span>|  
|`JsErrorCannotSerializeDebugScript`|<span data-ttu-id="7df18-115">Los scripts no se pueden serializar en contextos de depuración.</span><span class="sxs-lookup"><span data-stu-id="7df18-115">Scripts cannot be serialized in debug contexts.</span></span>|  
|`JsErrorCategoryEngine`|<span data-ttu-id="7df18-116">Categoría de errores relacionados con errores que se producen en el motor en sí.</span><span class="sxs-lookup"><span data-stu-id="7df18-116">Category of errors that relates to errors occurring within the engine itself.</span></span>|  
|`JsErrorCategoryFatal`|<span data-ttu-id="7df18-117">Categoría de errores fatales y que significan un error del motor.</span><span class="sxs-lookup"><span data-stu-id="7df18-117">Category of errors that are fatal and signify failure of the engine.</span></span>|  
|`JsErrorCategoryScript`|<span data-ttu-id="7df18-118">Categoría de errores relacionados con errores en un script.</span><span class="sxs-lookup"><span data-stu-id="7df18-118">Category of errors that relates to errors in a script.</span></span>|  
|`JsErrorCategoryUsage`|<span data-ttu-id="7df18-119">Categoría de errores que se relacionan con el uso incorrecto de la propia API.</span><span class="sxs-lookup"><span data-stu-id="7df18-119">Category of errors that relates to incorrect usage of the API itself.</span></span>|  
|`JsErrorFatal`|<span data-ttu-id="7df18-120">Se ha producido un error grave en el motor.</span><span class="sxs-lookup"><span data-stu-id="7df18-120">A fatal error in the engine has occurred.</span></span>|  
|`JsErrorHeapEnumInProgress`|<span data-ttu-id="7df18-121">Actualmente se está realizando una enumeración de montones en el contexto de script.</span><span class="sxs-lookup"><span data-stu-id="7df18-121">A heap enumeration is currently underway in the script context.</span></span>|  
|`JsErrorIdleNotEnabled`|<span data-ttu-id="7df18-122">Notificación de inactividad cuando el host no ha habilitado el procesamiento en inactividad.</span><span class="sxs-lookup"><span data-stu-id="7df18-122">Idle notification given when the host did not enable idle processing.</span></span>|  
|`JsErrorInDisabledState`|<span data-ttu-id="7df18-123">El tiempo de ejecución está en estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7df18-123">The runtime is in a disabled state.</span></span>|  
|`JsErrorInExceptionState`|<span data-ttu-id="7df18-124">El motor está en un estado de excepción y no se puede llamar a ninguna API hasta que se borre la excepción.</span><span class="sxs-lookup"><span data-stu-id="7df18-124">The engine is in an exception state and no APIs can be called until the exception is cleared.</span></span>|  
|`JsErrorInObjectBeforeCollectCallback`|<span data-ttu-id="7df18-125">La operación no se admite en un objeto antes de recopilar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="7df18-125">The operation is not supported in an object before collect callback.</span></span><br /><br /> <span data-ttu-id="7df18-126">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7df18-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorInProfileCallback`|<span data-ttu-id="7df18-127">Un contexto de script está en medio de una devolución de llamada de perfil.</span><span class="sxs-lookup"><span data-stu-id="7df18-127">A script context is in the middle of a profile callback.</span></span>|  
|`JsErrorInThreadServiceCallback`|<span data-ttu-id="7df18-128">Se está realizando una devolución de llamada del servicio de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="7df18-128">A thread service callback is currently underway.</span></span>|  
|`JsErrorInvalidArgument`|<span data-ttu-id="7df18-129">Un argumento para una API de hospedaje no es válido.</span><span class="sxs-lookup"><span data-stu-id="7df18-129">An argument to a hosting API was invalid.</span></span>|  
|`JsErrorNoCurrentContext`|<span data-ttu-id="7df18-130">La API de hospedaje requiere que un contexto esté activo, pero no hay ningún contexto actual.</span><span class="sxs-lookup"><span data-stu-id="7df18-130">The hosting API requires that a context be current, but there is no current context.</span></span>|  
|`JsErrorNotImplemented`|<span data-ttu-id="7df18-131">Aún no se ha implementado una API de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7df18-131">A hosting API is not yet implemented.</span></span>|  
|`JsErrorNullArgument`|<span data-ttu-id="7df18-132">Un argumento para una API de hospedaje es null en un contexto donde no está permitido el valor null.</span><span class="sxs-lookup"><span data-stu-id="7df18-132">An argument to a hosting API was null in a context where null is not allowed.</span></span>|  
|`JsErrorObjectNotInspectable`|<span data-ttu-id="7df18-133">El objeto no se puede desempaquetar como `IInspectable` puntero.</span><span class="sxs-lookup"><span data-stu-id="7df18-133">Object cannot be unwrapped to `IInspectable` pointer.</span></span><br /><br /> <span data-ttu-id="7df18-134">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7df18-134">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorOutOfMemory`|<span data-ttu-id="7df18-135">El motor de Chakra se ha quedado sin memoria.</span><span class="sxs-lookup"><span data-stu-id="7df18-135">The Chakra engine has run out of memory.</span></span>|  
|`JsErrorPropertyNotSymbol`|<span data-ttu-id="7df18-136">Una API de hospedaje que funciona en los identificadores de propiedad de símbolo pero se llamó con un identificador de propiedad sin símbolo. `JsGetSymbolFromPropertyId`Si se llama a la función con un identificador de propiedad sin símbolo, se devuelve el código de error.</span><span class="sxs-lookup"><span data-stu-id="7df18-136">A hosting API that operates on symbol property ids but was called with a non-symbol property id. The error code is returned by `JsGetSymbolFromPropertyId` if the function is called with non-symbol property id.</span></span><br /><br /> <span data-ttu-id="7df18-137">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7df18-137">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorPropertyNotString`|<span data-ttu-id="7df18-138">Una API de hospedaje que funciona en identificadores de propiedad de cadena pero que se llamó con un identificador de propiedad no de cadena. Existing devuelve el código de error `JsGetPropertyNamefromId` si se llama a la función con el identificador de propiedad sin cadenas.</span><span class="sxs-lookup"><span data-stu-id="7df18-138">A hosting API that operates on string property ids but was called with a non-string property id. The error code is returned by existing `JsGetPropertyNamefromId` if the function is called with non-string property id.</span></span><br /><br /> <span data-ttu-id="7df18-139">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7df18-139">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorRuntimeInUse`|<span data-ttu-id="7df18-140">Un Runtime que aún está en uso no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="7df18-140">A runtime that is still in use cannot be disposed.</span></span>|  
|`JsErrorScriptCompile`|<span data-ttu-id="7df18-141">Error al compilar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7df18-141">JavaScript failed to compile.</span></span>|  
|`JsErrorScriptEvalDisabled`|<span data-ttu-id="7df18-142">Se terminó un script porque intentaste usar `eval` o `function` y eval se deshabilitó.</span><span class="sxs-lookup"><span data-stu-id="7df18-142">A script was terminated because it tried to use `eval` or `function` and eval was disabled.</span></span>|  
|`JsErrorScriptException`|<span data-ttu-id="7df18-143">Se produjo una excepción de JavaScript mientras se ejecutaba un script.</span><span class="sxs-lookup"><span data-stu-id="7df18-143">A JavaScript exception occurred while running a script.</span></span>|  
|`JsErrorScriptTerminated`|<span data-ttu-id="7df18-144">Se terminó un script a causa de una solicitud para suspender un tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7df18-144">A script was terminated due to a request to suspend a runtime.</span></span>|  
|`JsErrorWrongRuntime`|<span data-ttu-id="7df18-145">Se llamó a una API de hospedaje con un objeto creado en un tiempo de ejecución de JavaScript diferente.</span><span class="sxs-lookup"><span data-stu-id="7df18-145">A hosting API was called with object created on different JavaScript runtime.</span></span>|  
|`JsErrorWrongThread`|<span data-ttu-id="7df18-146">Se llamó a una API de hospedaje en el subproceso equivocado.</span><span class="sxs-lookup"><span data-stu-id="7df18-146">A hosting API was called on the wrong thread.</span></span>|  
|`JsNoError`|<span data-ttu-id="7df18-147">Código de error de éxito.</span><span class="sxs-lookup"><span data-stu-id="7df18-147">Success error code.</span></span>|  
  
## <span data-ttu-id="7df18-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df18-148">Requirements</span></span>  
 <span data-ttu-id="7df18-149">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7df18-149">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7df18-150">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7df18-150">See Also</span></span>  
 [<span data-ttu-id="7df18-151">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7df18-151">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)