---
description: Las API de tiempo de ejecución de JavaScript (JsRT) le permiten agregar capacidades de scripting a aplicaciones de escritorio y de servidor que se ejecutan en Windows.
title: Referencia (tiempo de ejecución de JavaScript) | Microsoft docs
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d1215d84daa31f2338b8c7e237625d0129026bea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573390"
---
# <span data-ttu-id="02e36-103">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="02e36-103">Reference (JavaScript Runtime)</span></span>
<span data-ttu-id="02e36-104">Las API de tiempo de ejecución de JavaScript (JsRT) le permiten agregar capacidades de scripting a aplicaciones de escritorio y de servidor que se ejecutan en Windows.</span><span class="sxs-lookup"><span data-stu-id="02e36-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  
  
 <span data-ttu-id="02e36-105">Si deseas incrustar [ChakraCore](https://github.com/Microsoft/ChakraCore) en tu aplicación, consulta [ChakraCore wiki](https://aka.ms/corejsrtref) para obtener referencias de JSRT.</span><span class="sxs-lookup"><span data-stu-id="02e36-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  
  
## <span data-ttu-id="02e36-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="02e36-106">In This Section</span></span>  
 <span data-ttu-id="02e36-107">Las typedefs, constantes y enumeraciones que admiten el hospedaje de JsRT se describen aquí:</span><span class="sxs-lookup"><span data-stu-id="02e36-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
-   [<span data-ttu-id="02e36-108">Typedefs, constantes y enumeraciones en tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="02e36-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](../chakra-hosting/javascript-runtime-typedefs-constants-and-enumerations.md)  
  
 <span data-ttu-id="02e36-109">Las siguientes funciones permiten el hospedaje de JsRT:</span><span class="sxs-lookup"><span data-stu-id="02e36-109">The following functions enable JsRT hosting:</span></span>  
  
-   [<span data-ttu-id="02e36-110">Función JsAddRef</span><span class="sxs-lookup"><span data-stu-id="02e36-110">JsAddRef Function</span></span>](../chakra-hosting/jsaddref-function.md)  
  
-   [<span data-ttu-id="02e36-111">Función JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="02e36-111">JsBooleanToBool Function</span></span>](../chakra-hosting/jsbooleantobool-function.md)  
  
-   [<span data-ttu-id="02e36-112">Función JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="02e36-112">JsBoolToBoolean Function</span></span>](../chakra-hosting/jsbooltoboolean-function.md)  
  
-   [<span data-ttu-id="02e36-113">Función JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="02e36-113">JsCallFunction Function</span></span>](../chakra-hosting/jscallfunction-function.md)  
  
-   [<span data-ttu-id="02e36-114">Función JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="02e36-114">JsCollectGarbage Function</span></span>](../chakra-hosting/jscollectgarbage-function.md)  
  
-   [<span data-ttu-id="02e36-115">Función JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="02e36-115">JsConstructObject Function</span></span>](../chakra-hosting/jsconstructobject-function.md)  
  
-   [<span data-ttu-id="02e36-116">Función JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="02e36-116">JsConvertValueToBoolean Function</span></span>](../chakra-hosting/jsconvertvaluetoboolean-function.md)  
  
-   [<span data-ttu-id="02e36-117">Función JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="02e36-117">JsConvertValueToNumber Function</span></span>](../chakra-hosting/jsconvertvaluetonumber-function.md)  
  
-   [<span data-ttu-id="02e36-118">Función JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="02e36-118">JsConvertValueToObject Function</span></span>](../chakra-hosting/jsconvertvaluetoobject-function.md)  
  
-   [<span data-ttu-id="02e36-119">Función JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="02e36-119">JsConvertValueToString Function</span></span>](../chakra-hosting/jsconvertvaluetostring-function.md)  
  
-   [<span data-ttu-id="02e36-120">Función JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="02e36-120">JsCreateArray Function</span></span>](../chakra-hosting/jscreatearray-function.md)  
  
-   [<span data-ttu-id="02e36-121">Función JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="02e36-121">JsCreateArrayBuffer Function</span></span>](../chakra-hosting/jscreatearraybuffer-function.md)  
  
-   [<span data-ttu-id="02e36-122">Función JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="02e36-122">JsCreateContext Function</span></span>](../chakra-hosting/jscreatecontext-function.md)  
  
-   [<span data-ttu-id="02e36-123">Función JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="02e36-123">JsCreateDataView Function</span></span>](../chakra-hosting/jscreatedataview-function.md)  
  
-   [<span data-ttu-id="02e36-124">Función JsCreateError</span><span class="sxs-lookup"><span data-stu-id="02e36-124">JsCreateError Function</span></span>](../chakra-hosting/jscreateerror-function.md)  
  
-   [<span data-ttu-id="02e36-125">Función JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="02e36-125">JsCreateExternalArrayBuffer Function</span></span>](../chakra-hosting/jscreateexternalarraybuffer-function.md)  
  
-   [<span data-ttu-id="02e36-126">Función JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="02e36-126">JsCreateExternalObject Function</span></span>](../chakra-hosting/jscreateexternalobject-function.md)  
  
-   [<span data-ttu-id="02e36-127">Función JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="02e36-127">JsCreateFunction Function</span></span>](../chakra-hosting/jscreatefunction-function.md)  
  
-   [<span data-ttu-id="02e36-128">Función JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="02e36-128">JsCreateNamedFunction Function</span></span>](../chakra-hosting/jscreatenamedfunction-function.md)  
  
-   [<span data-ttu-id="02e36-129">Función JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="02e36-129">JsCreateObject Function</span></span>](../chakra-hosting/jscreateobject-function.md)  
  
-   [<span data-ttu-id="02e36-130">Función JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="02e36-130">JsCreateRangeError Function</span></span>](../chakra-hosting/jscreaterangeerror-function.md)  
  
-   [<span data-ttu-id="02e36-131">Función JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="02e36-131">JsCreateReferenceError Function</span></span>](../chakra-hosting/jscreatereferenceerror-function.md)  
  
-   [<span data-ttu-id="02e36-132">Función JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="02e36-132">JsCreateRuntime Function</span></span>](../chakra-hosting/jscreateruntime-function.md)  
  
-   [<span data-ttu-id="02e36-133">Función JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="02e36-133">JsCreateSymbol Function</span></span>](../chakra-hosting/jscreatesymbol-function.md)  
  
-   [<span data-ttu-id="02e36-134">Función JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="02e36-134">JsCreateSyntaxError Function</span></span>](../chakra-hosting/jscreatesyntaxerror-function.md)  
  
-   [<span data-ttu-id="02e36-135">Función JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="02e36-135">JsCreateTypeError Function</span></span>](../chakra-hosting/jscreatetypeerror-function.md)  
  
-   [<span data-ttu-id="02e36-136">Función JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="02e36-136">JsCreateTypedArray Function</span></span>](../chakra-hosting/jscreatetypedarray-function.md)  
  
-   [<span data-ttu-id="02e36-137">Función JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="02e36-137">JsCreateURIError Function</span></span>](../chakra-hosting/jscreateurierror-function.md)  
  
-   [<span data-ttu-id="02e36-138">Función JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-138">JsDefineProperty Function</span></span>](../chakra-hosting/jsdefineproperty-function.md)  
  
-   [<span data-ttu-id="02e36-139">Función JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-139">JsDeleteIndexedProperty Function</span></span>](../chakra-hosting/jsdeleteindexedproperty-function.md)  
  
-   [<span data-ttu-id="02e36-140">Función JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-140">JsDeleteProperty Function</span></span>](../chakra-hosting/jsdeleteproperty-function.md)  
  
-   [<span data-ttu-id="02e36-141">Función JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="02e36-141">JsDisableRuntimeExecution Function</span></span>](../chakra-hosting/jsdisableruntimeexecution-function.md)  
  
-   [<span data-ttu-id="02e36-142">Función JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="02e36-142">JsDisposeRuntime Function</span></span>](../chakra-hosting/jsdisposeruntime-function.md)  
  
-   [<span data-ttu-id="02e36-143">Función JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="02e36-143">JsDoubleToNumber Function</span></span>](../chakra-hosting/jsdoubletonumber-function.md)  
  
-   [<span data-ttu-id="02e36-144">Función JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="02e36-144">JsEnableRuntimeExecution Function</span></span>](../chakra-hosting/jsenableruntimeexecution-function.md)  
  
-   [<span data-ttu-id="02e36-145">Función JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="02e36-145">JsEnumerateHeap Function</span></span>](../chakra-hosting/jsenumerateheap-function.md)  
  
-   [<span data-ttu-id="02e36-146">Función JsEquals</span><span class="sxs-lookup"><span data-stu-id="02e36-146">JsEquals Function</span></span>](../chakra-hosting/jsequals-function.md)  
  
-   [<span data-ttu-id="02e36-147">Función JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="02e36-147">JsGetAndClearException Function</span></span>](../chakra-hosting/jsgetandclearexception-function.md)  
  
-   [<span data-ttu-id="02e36-148">Función JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="02e36-148">JsGetArrayBufferStorage Function</span></span>](../chakra-hosting/jsgetarraybufferstorage-function.md)  
  
-   [<span data-ttu-id="02e36-149">Función JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="02e36-149">JsGetContextData Function</span></span>](../chakra-hosting/jsgetcontextdata-function.md)  
  
-   [<span data-ttu-id="02e36-150">Función JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="02e36-150">JsGetContextOfObject Function</span></span>](../chakra-hosting/jsgetcontextofobject-function.md)  
  
-   [<span data-ttu-id="02e36-151">Función JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="02e36-151">JsGetCurrentContext Function</span></span>](../chakra-hosting/jsgetcurrentcontext-function.md)  
  
-   [<span data-ttu-id="02e36-152">Función JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="02e36-152">JsGetDataViewStorage Function</span></span>](../chakra-hosting/jsgetdataviewstorage-function.md)  
  
-   [<span data-ttu-id="02e36-153">Función JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="02e36-153">JsGetExtensionAllowed Function</span></span>](../chakra-hosting/jsgetextensionallowed-function.md)  
  
-   [<span data-ttu-id="02e36-154">Función JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="02e36-154">JsGetExternalData Function</span></span>](../chakra-hosting/jsgetexternaldata-function.md)  
  
-   [<span data-ttu-id="02e36-155">Función JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="02e36-155">JsGetFalseValue Function</span></span>](../chakra-hosting/jsgetfalsevalue-function.md)  
  
-   [<span data-ttu-id="02e36-156">Función JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="02e36-156">JsGetGlobalObject Function</span></span>](../chakra-hosting/jsgetglobalobject-function.md)  
  
-   [<span data-ttu-id="02e36-157">Función JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="02e36-157">JsGetIndexedPropertiesExternalData Function</span></span>](../chakra-hosting/jsgetindexedpropertiesexternaldata-function.md)  
  
-   [<span data-ttu-id="02e36-158">Función JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-158">JsGetIndexedProperty Function</span></span>](../chakra-hosting/jsgetindexedproperty-function.md)  
  
-   [<span data-ttu-id="02e36-159">Función JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="02e36-159">JsGetNullValue Function</span></span>](../chakra-hosting/jsgetnullvalue-function.md)  
  
-   [<span data-ttu-id="02e36-160">Función JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="02e36-160">JsGetOwnPropertyDescriptor Function</span></span>](../chakra-hosting/jsgetownpropertydescriptor-function.md)  
  
-   [<span data-ttu-id="02e36-161">Función JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="02e36-161">JsGetOwnPropertyNames Function</span></span>](../chakra-hosting/jsgetownpropertynames-function.md)  
  
-   [<span data-ttu-id="02e36-162">Función JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="02e36-162">JsGetOwnPropertySymbols Function</span></span>](../chakra-hosting/jsgetownpropertysymbols-function.md)  
  
-   [<span data-ttu-id="02e36-163">Función JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-163">JsGetProperty Function</span></span>](../chakra-hosting/jsgetproperty-function.md)  
  
-   [<span data-ttu-id="02e36-164">Función JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="02e36-164">JsGetPropertyIdFromName Function</span></span>](../chakra-hosting/jsgetpropertyidfromname-function.md)  
  
-   [<span data-ttu-id="02e36-165">Función JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="02e36-165">JsGetPropertyIdFromSymbol Function</span></span>](../chakra-hosting/jsgetpropertyidfromsymbol-function.md)  
  
-   [<span data-ttu-id="02e36-166">Función JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="02e36-166">JsGetPropertyIdType Function</span></span>](../chakra-hosting/jsgetpropertyidtype-function.md)  
  
-   [<span data-ttu-id="02e36-167">Función JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="02e36-167">JsGetPropertyNameFromId Function</span></span>](../chakra-hosting/jsgetpropertynamefromid-function.md)  
  
-   [<span data-ttu-id="02e36-168">Función JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="02e36-168">JsGetPrototype Function</span></span>](../chakra-hosting/jsgetprototype-function.md)  
  
-   [<span data-ttu-id="02e36-169">Función JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="02e36-169">JsGetRuntime Function</span></span>](../chakra-hosting/jsgetruntime-function.md)  
  
-   [<span data-ttu-id="02e36-170">Función JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="02e36-170">JsGetRuntimeMemoryLimit Function</span></span>](../chakra-hosting/jsgetruntimememorylimit-function.md)  
  
-   [<span data-ttu-id="02e36-171">Función JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="02e36-171">JsGetRuntimeMemoryUsage Function</span></span>](../chakra-hosting/jsgetruntimememoryusage-function.md)  
  
-   [<span data-ttu-id="02e36-172">Función JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="02e36-172">JsGetStringLength Function</span></span>](../chakra-hosting/jsgetstringlength-function.md)  
  
-   [<span data-ttu-id="02e36-173">Función JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="02e36-173">JsGetSymbolFromPropertyId Function</span></span>](../chakra-hosting/jsgetsymbolfrompropertyid-function.md)  
  
-   [<span data-ttu-id="02e36-174">Función JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="02e36-174">JsGetTrueValue Function</span></span>](../chakra-hosting/jsgettruevalue-function.md)  
  
-   [<span data-ttu-id="02e36-175">Función JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="02e36-175">JsGetTypedArrayInfo Function</span></span>](../chakra-hosting/jsgettypedarrayinfo-function.md)  
  
-   [<span data-ttu-id="02e36-176">Función JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="02e36-176">JsGetTypedArrayStorage Function</span></span>](../chakra-hosting/jsgettypedarraystorage-function.md)  
  
-   [<span data-ttu-id="02e36-177">Función JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="02e36-177">JsGetUndefinedValue Function</span></span>](../chakra-hosting/jsgetundefinedvalue-function.md)  
  
-   [<span data-ttu-id="02e36-178">Función JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="02e36-178">JsGetValueType Function</span></span>](../chakra-hosting/jsgetvaluetype-function.md)  
  
-   [<span data-ttu-id="02e36-179">Función JsHasException</span><span class="sxs-lookup"><span data-stu-id="02e36-179">JsHasException Function</span></span>](../chakra-hosting/jshasexception-function.md)  
  
-   [<span data-ttu-id="02e36-180">Función JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="02e36-180">JsHasExternalData Function</span></span>](../chakra-hosting/jshasexternaldata-function.md)  
  
-   [<span data-ttu-id="02e36-181">Función JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="02e36-181">JsHasIndexedPropertiesExternalData Function</span></span>](../chakra-hosting/jshasindexedpropertiesexternaldata-function.md)  
  
-   [<span data-ttu-id="02e36-182">Función JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-182">JsHasIndexedProperty Function</span></span>](../chakra-hosting/jshasindexedproperty-function.md)  
  
-   [<span data-ttu-id="02e36-183">Función JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-183">JsHasProperty Function</span></span>](../chakra-hosting/jshasproperty-function.md)  
  
-   [<span data-ttu-id="02e36-184">Función JsIdle</span><span class="sxs-lookup"><span data-stu-id="02e36-184">JsIdle Function</span></span>](../chakra-hosting/jsidle-function.md)  
  
-   [<span data-ttu-id="02e36-185">Función JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="02e36-185">JsInspectableToObject Function</span></span>](../chakra-hosting/jsinspectabletoobject-function.md)  
  
-   [<span data-ttu-id="02e36-186">Función JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="02e36-186">JsInstanceOf Function</span></span>](../chakra-hosting/jsinstanceof-function.md)  
  
-   [<span data-ttu-id="02e36-187">Función JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="02e36-187">JsIntToNumber Function</span></span>](../chakra-hosting/jsinttonumber-function.md)  
  
-   [<span data-ttu-id="02e36-188">Función JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="02e36-188">JsIsEnumeratingHeap Function</span></span>](../chakra-hosting/jsisenumeratingheap-function.md)  
  
-   [<span data-ttu-id="02e36-189">Función JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="02e36-189">JsIsRuntimeExecutionDisabled Function</span></span>](../chakra-hosting/jsisruntimeexecutiondisabled-function.md)  
  
-   [<span data-ttu-id="02e36-190">Función JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="02e36-190">JsNumberToDouble Function</span></span>](../chakra-hosting/jsnumbertodouble-function.md)  
  
-   [<span data-ttu-id="02e36-191">Función JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="02e36-191">JsNumberToInt Function</span></span>](../chakra-hosting/jsnumbertoint-function.md)  
  
-   [<span data-ttu-id="02e36-192">Función JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="02e36-192">JsObjectToInspectable Function</span></span>](../chakra-hosting/jsobjecttoinspectable-function.md)  
  
-   [<span data-ttu-id="02e36-193">Función JsParseScript</span><span class="sxs-lookup"><span data-stu-id="02e36-193">JsParseScript Function</span></span>](../chakra-hosting/jsparsescript-function.md)  
  
-   [<span data-ttu-id="02e36-194">Función JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="02e36-194">JsParseSerializedScript Function</span></span>](../chakra-hosting/jsparseserializedscript-function.md)  
  
-   [<span data-ttu-id="02e36-195">Función JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-195">JsParseSerializedScriptWithCallback Function</span></span>](../chakra-hosting/jsparseserializedscriptwithcallback-function.md)  
  
-   [<span data-ttu-id="02e36-196">Función JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="02e36-196">JsPointerToString Function</span></span>](../chakra-hosting/jspointertostring-function.md)  
  
-   [<span data-ttu-id="02e36-197">Función JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="02e36-197">JsPreventExtension Function</span></span>](../chakra-hosting/jspreventextension-function.md)  
  
-   [<span data-ttu-id="02e36-198">Función JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="02e36-198">JsProjectWinRTNamespace Function</span></span>](../chakra-hosting/jsprojectwinrtnamespace-function.md)  
  
-   [<span data-ttu-id="02e36-199">Función JsRelease</span><span class="sxs-lookup"><span data-stu-id="02e36-199">JsRelease Function</span></span>](../chakra-hosting/jsrelease-function.md)  
  
-   [<span data-ttu-id="02e36-200">Función JsRunScript</span><span class="sxs-lookup"><span data-stu-id="02e36-200">JsRunScript Function</span></span>](../chakra-hosting/jsrunscript-function.md)  
  
-   [<span data-ttu-id="02e36-201">Función JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="02e36-201">JsRunSerializedScript Function</span></span>](../chakra-hosting/jsrunserializedscript-function.md)  
  
-   [<span data-ttu-id="02e36-202">Función JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-202">JsRunSerializedScriptWithCallback Function</span></span>](../chakra-hosting/jsrunserializedscriptwithcallback-function.md)  
  
-   [<span data-ttu-id="02e36-203">Función JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="02e36-203">JsSerializeScript Function</span></span>](../chakra-hosting/jsserializescript-function.md)  
  
-   [<span data-ttu-id="02e36-204">Función JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="02e36-204">JsSetContextData Function</span></span>](../chakra-hosting/jssetcontextdata-function.md)  
  
-   [<span data-ttu-id="02e36-205">Función JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="02e36-205">JsSetCurrentContext Function</span></span>](../chakra-hosting/jssetcurrentcontext-function.md)  
  
-   [<span data-ttu-id="02e36-206">Función JsSetException</span><span class="sxs-lookup"><span data-stu-id="02e36-206">JsSetException Function</span></span>](../chakra-hosting/jssetexception-function.md)  
  
-   [<span data-ttu-id="02e36-207">Función JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="02e36-207">JsSetExternalData Function</span></span>](../chakra-hosting/jssetexternaldata-function.md)  
  
-   [<span data-ttu-id="02e36-208">Función JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="02e36-208">JsSetIndexedPropertiesToExternalData Function</span></span>](../chakra-hosting/jssetindexedpropertiestoexternaldata-function.md)  
  
-   [<span data-ttu-id="02e36-209">Función JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-209">JsSetIndexedProperty Function</span></span>](../chakra-hosting/jssetindexedproperty-function.md)  
  
-   [<span data-ttu-id="02e36-210">Función JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-210">JsSetObjectBeforeCollectCallback Function</span></span>](../chakra-hosting/jssetobjectbeforecollectcallback-function.md)  
  
-   [<span data-ttu-id="02e36-211">Función JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-211">JsSetProjectionEnqueueCallback Function</span></span>](../chakra-hosting/jssetprojectionenqueuecallback-function.md)  
  
-   [<span data-ttu-id="02e36-212">Función JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-212">JsSetPromiseContinuationCallback Function</span></span>](../chakra-hosting/jssetpromisecontinuationcallback-function.md)  
  
-   [<span data-ttu-id="02e36-213">Función JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="02e36-213">JsSetProperty Function</span></span>](../chakra-hosting/jssetproperty-function.md)  
  
-   [<span data-ttu-id="02e36-214">Función JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="02e36-214">JsSetPrototype Function</span></span>](../chakra-hosting/jssetprototype-function.md)  
  
-   [<span data-ttu-id="02e36-215">Función JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](../chakra-hosting/jssetruntimebeforecollectcallback-function.md)  
  
-   [<span data-ttu-id="02e36-216">Función JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="02e36-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](../chakra-hosting/jssetruntimememoryallocationcallback-function.md)  
  
-   [<span data-ttu-id="02e36-217">Función JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="02e36-217">JsSetRuntimeMemoryLimit Function</span></span>](../chakra-hosting/jssetruntimememorylimit-function.md)  
  
-   [<span data-ttu-id="02e36-218">Función JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="02e36-218">JsStartDebugging Function</span></span>](../chakra-hosting/jsstartdebugging-function.md)  
  
-   [<span data-ttu-id="02e36-219">Función JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="02e36-219">JsStartProfiling Function</span></span>](../chakra-hosting/jsstartprofiling-function.md)  
  
-   [<span data-ttu-id="02e36-220">Función JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="02e36-220">JsStopProfiling Function</span></span>](../chakra-hosting/jsstopprofiling-function.md)  
  
-   [<span data-ttu-id="02e36-221">Función JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="02e36-221">JsStrictEquals Function</span></span>](../chakra-hosting/jsstrictequals-function.md)  
  
-   [<span data-ttu-id="02e36-222">Función JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="02e36-222">JsStringToPointer Function</span></span>](../chakra-hosting/jsstringtopointer-function.md)  
  
-   [<span data-ttu-id="02e36-223">Función JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="02e36-223">JsValueToVariant Function</span></span>](../chakra-hosting/jsvaluetovariant-function.md)  
  
-   [<span data-ttu-id="02e36-224">Función JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="02e36-224">JsVariantToValue Function</span></span>](../chakra-hosting/jsvarianttovalue-function.md)  
  
## <span data-ttu-id="02e36-225">Consulta también</span><span class="sxs-lookup"><span data-stu-id="02e36-225">See Also</span></span>  
 [<span data-ttu-id="02e36-226">Hospedaje de JavaScript en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="02e36-226">Hosting the JavaScript Runtime</span></span>](../chakra-hosting/hosting-the-javascript-runtime.md)   
 [<span data-ttu-id="02e36-227">Hospedaje en tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="02e36-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)