---
description: Las API de tiempo de ejecución de JavaScript (JsRT) le permiten agregar capacidades de scripting a aplicaciones de escritorio y de servidor que se ejecutan en Windows.
title: Referencia (tiempo de ejecución de JavaScript)
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 7166e6cd5d64060c2939d8404e1415dc34fce17b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752216"
---
# Referencia (tiempo de ejecución de JavaScript)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Las API de tiempo de ejecución de JavaScript (JsRT) le permiten agregar capacidades de scripting a aplicaciones de escritorio y de servidor que se ejecutan en Windows.  

Si deseas incrustar [ChakraCore](https://github.com/Microsoft/ChakraCore) en tu aplicación, consulta [ChakraCore wiki](https://aka.ms/corejsrtref) para obtener referencias de JSRT.  

## En esta sección  

Las typedefs, constantes y enumeraciones que admiten el hospedaje de JsRT se describen aquí:  
  
*   [Constantes, enumeraciones y definiciones de tipo en tiempo de ejecución de JavaScript](./javascript-runtime-typedefs-constants-and-enumerations.md)  

Las siguientes funciones permiten el hospedaje de JsRT:  

*   [Función JsAddRef](./jsaddref-function.md)  
*   [Función JsBooleanToBool](./jsbooleantobool-function.md)  
*   [Función JsBoolToBoolean](./jsbooltoboolean-function.md)  
*   [Función JsCallFunction](./jscallfunction-function.md)  
*   [Función JsCollectGarbage](./jscollectgarbage-function.md)  
*   [Función JsConstructObject](./jsconstructobject-function.md)  
*   [Función JsConvertValueToBoolean](./jsconvertvaluetoboolean-function.md)  
*   [Función JsConvertValueToNumber](./jsconvertvaluetonumber-function.md)  
*   [Función JsConvertValueToObject](./jsconvertvaluetoobject-function.md)  
*   [Función JsConvertValueToString](./jsconvertvaluetostring-function.md)  
*   [Función JsCreateArray](./jscreatearray-function.md)  
*   [Función JsCreateArrayBuffer](./jscreatearraybuffer-function.md)  
*   [Función JsCreateContext](./jscreatecontext-function.md)  
*   [Función JsCreateDataView](./jscreatedataview-function.md)  
*   [Función JsCreateError](./jscreateerror-function.md)  
*   [Función JsCreateExternalArrayBuffer](./jscreateexternalarraybuffer-function.md)  
*   [Función JsCreateExternalObject](./jscreateexternalobject-function.md)  
*   [Función JsCreateFunction](./jscreatefunction-function.md)  
*   [Función JsCreateNamedFunction](./jscreatenamedfunction-function.md)  
*   [Función JsCreateObject](./jscreateobject-function.md)  
*   [Función JsCreateRangeError](./jscreaterangeerror-function.md)  
*   [Función JsCreateReferenceError](./jscreatereferenceerror-function.md)  
*   [Función JsCreateRuntime](./jscreateruntime-function.md)  
*   [Función JsCreateSymbol](./jscreatesymbol-function.md)  
*   [Función JsCreateSyntaxError](./jscreatesyntaxerror-function.md)  
*   [Función JsCreateTypeError](./jscreatetypeerror-function.md)  
*   [Función JsCreateTypedArray](./jscreatetypedarray-function.md)  
*   [Función JsCreateURIError](./jscreateurierror-function.md)  
*   [Función JsDefineProperty](./jsdefineproperty-function.md)  
*   [Función JsDeleteIndexedProperty](./jsdeleteindexedproperty-function.md)  
*   [Función JsDeleteProperty](./jsdeleteproperty-function.md)  
*   [Función JsDisableRuntimeExecution](./jsdisableruntimeexecution-function.md)  
*   [Función JsDisposeRuntime](./jsdisposeruntime-function.md)  
*   [Función JsDoubleToNumber](./jsdoubletonumber-function.md)  
*   [Función JsEnableRuntimeExecution](./jsenableruntimeexecution-function.md)  
*   [Función JsEnumerateHeap](./jsenumerateheap-function.md)  
*   [Función JsEquals](./jsequals-function.md)  
*   [Función JsGetAndClearException](./jsgetandclearexception-function.md)  
*   [Función JsGetArrayBufferStorage](./jsgetarraybufferstorage-function.md)  
*   [Función JsGetContextData](./jsgetcontextdata-function.md)  
*   [Función JsGetContextOfObject](./jsgetcontextofobject-function.md)  
*   [Función JsGetCurrentContext](./jsgetcurrentcontext-function.md)  
*   [Función JsGetDataViewStorage](./jsgetdataviewstorage-function.md)  
*   [Función JsGetExtensionAllowed](./jsgetextensionallowed-function.md)  
*   [Función JsGetExternalData](./jsgetexternaldata-function.md)  
*   [Función JsGetFalseValue](./jsgetfalsevalue-function.md)  
*   [Función JsGetGlobalObject](./jsgetglobalobject-function.md)  
*   [Función JsGetIndexedPropertiesExternalData](./jsgetindexedpropertiesexternaldata-function.md)  
*   [Función JsGetIndexedProperty](./jsgetindexedproperty-function.md)  
*   [Función JsGetNullValue](./jsgetnullvalue-function.md)  
*   [Función JsGetOwnPropertyDescriptor](./jsgetownpropertydescriptor-function.md)  
*   [Función JsGetOwnPropertyNames](./jsgetownpropertynames-function.md)  
*   [Función JsGetOwnPropertySymbols](./jsgetownpropertysymbols-function.md)  
*   [Función JsGetProperty](./jsgetproperty-function.md)  
*   [Función JsGetPropertyIdFromName](./jsgetpropertyidfromname-function.md)  
*   [Función JsGetPropertyIdFromSymbol](./jsgetpropertyidfromsymbol-function.md)  
*   [Función JsGetPropertyIdType](./jsgetpropertyidtype-function.md)  
*   [Función JsGetPropertyNameFromId](./jsgetpropertynamefromid-function.md)  
*   [Función JsGetPrototype](./jsgetprototype-function.md)  
*   [Función JsGetRuntime](./jsgetruntime-function.md)  
*   [Función JsGetRuntimeMemoryLimit](./jsgetruntimememorylimit-function.md)  
*   [Función JsGetRuntimeMemoryUsage](./jsgetruntimememoryusage-function.md)  
*   [Función JsGetStringLength](./jsgetstringlength-function.md)  
*   [Función JsGetSymbolFromPropertyId](./jsgetsymbolfrompropertyid-function.md)  
*   [Función JsGetTrueValue](./jsgettruevalue-function.md)  
*   [Función JsGetTypedArrayInfo](./jsgettypedarrayinfo-function.md)  
*   [Función JsGetTypedArrayStorage](./jsgettypedarraystorage-function.md)  
*   [Función JsGetUndefinedValue](./jsgetundefinedvalue-function.md)  
*   [Función JsGetValueType](./jsgetvaluetype-function.md)  
*   [Función JsHasException](./jshasexception-function.md)  
*   [Función JsHasExternalData](./jshasexternaldata-function.md)  
*   [Función JsHasIndexedPropertiesExternalData](./jshasindexedpropertiesexternaldata-function.md)  
*   [Función JsHasIndexedProperty](./jshasindexedproperty-function.md)  
*   [Función JsHasProperty](./jshasproperty-function.md)  
*   [Función JsIdle](./jsidle-function.md)  
*   [Función JsInspectableToObject](./jsinspectabletoobject-function.md)  
*   [Función JsInstanceOf](./jsinstanceof-function.md)  
*   [Función JsIntToNumber](./jsinttonumber-function.md)  
*   [Función JsIsEnumeratingHeap](./jsisenumeratingheap-function.md)  
*   [Función JsIsRuntimeExecutionDisabled](./jsisruntimeexecutiondisabled-function.md)  
*   [Función JsNumberToDouble](./jsnumbertodouble-function.md)  
*   [Función JsNumberToInt](./jsnumbertoint-function.md)  
*   [Función JsObjectToInspectable](./jsobjecttoinspectable-function.md)  
*   [Función JsParseScript](./jsparsescript-function.md)  
*   [Función JsParseSerializedScript](./jsparseserializedscript-function.md)  
*   [Función JsParseSerializedScriptWithCallback](./jsparseserializedscriptwithcallback-function.md)  
*   [Función JsPointerToString](./jspointertostring-function.md)  
*   [Función JsPreventExtension](./jspreventextension-function.md)  
*   [Función JsProjectWinRTNamespace](./jsprojectwinrtnamespace-function.md)  
*   [Función JsRelease](./jsrelease-function.md)  
*   [Función JsRunScript](./jsrunscript-function.md)  
*   [Función JsRunSerializedScript](./jsrunserializedscript-function.md)  
*   [Función JsRunSerializedScriptWithCallback](./jsrunserializedscriptwithcallback-function.md)  
*   [Función JsSerializeScript](./jsserializescript-function.md)  
*   [Función JsSetContextData](./jssetcontextdata-function.md)  
*   [Función JsSetCurrentContext](./jssetcurrentcontext-function.md)  
*   [Función JsSetException](./jssetexception-function.md)  
*   [Función JsSetExternalData](./jssetexternaldata-function.md)  
*   [Función JsSetIndexedPropertiesToExternalData](./jssetindexedpropertiestoexternaldata-function.md)  
*   [Función JsSetIndexedProperty](./jssetindexedproperty-function.md)  
*   [Función JsSetObjectBeforeCollectCallback](./jssetobjectbeforecollectcallback-function.md)  
*   [Función JsSetProjectionEnqueueCallback](./jssetprojectionenqueuecallback-function.md)  
*   [Función JsSetPromiseContinuationCallback](./jssetpromisecontinuationcallback-function.md)  
*   [Función JsSetProperty](./jssetproperty-function.md)  
*   [Función JsSetPrototype](./jssetprototype-function.md)  
*   [Función JsSetRuntimeBeforeCollectCallback](./jssetruntimebeforecollectcallback-function.md)  
*   [Función JsSetRuntimeMemoryAllocationCallback](./jssetruntimememoryallocationcallback-function.md)  
*   [Función JsSetRuntimeMemoryLimit](./jssetruntimememorylimit-function.md)  
*   [Función JsStartDebugging](./jsstartdebugging-function.md)  
*   [Función JsStartProfiling](./jsstartprofiling-function.md)  
*   [Función JsStopProfiling](./jsstopprofiling-function.md)  
*   [Función JsStrictEquals](./jsstrictequals-function.md)  
*   [Función JsStringToPointer](./jsstringtopointer-function.md)  
*   [Función JsValueToVariant](./jsvaluetovariant-function.md)  
*   [Función JsVariantToValue](./jsvarianttovalue-function.md)  

## Consulte también  

*   [Hospedar el tiempo de ejecución de JavaScript](./hosting-the-javascript-runtime.md)  
*   [Hospedaje en tiempo de ejecución de JavaScript](../javascript-runtime-hosting.md)  
