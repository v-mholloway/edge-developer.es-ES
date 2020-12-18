---
description: Un código de error devuelto desde una API de hospedaje de Chakra.
title: JsErrorCode (enumeración) | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b0a4aa7b47070bd5c8c7fe48cdbecf0dbefa9aa5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236216"
---
# Enumeración JsErrorCode

Un código de error devuelto desde una API de hospedaje de Chakra.  
  
## Sintaxis  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## Miembros  
  
### Los  
  
|Nombre|Descripción|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|El contexto no puede ponerse en un estado de depuración porque ya se encuentra en estado de depuración.|  
|`JsErrorAlreadyProfilingContext`|El contexto no puede iniciar la generación de perfiles porque ya está generando perfiles.|  
|`JsErrorArgumentNotObject`|Se llamó a una API de hospedaje que opera en valores de objeto con un valor que no es un objeto.|  
|`JsErrorBadSerializedScript`|Se usó una secuencia de comandos en serie incorrecta o la secuencia de comandos serializada fue serializada por una versión diferente del motor de Chakra.|  
|`JsErrorCannotDisableExecution`|El motor en tiempo de ejecución no admite interrupciones de script confiables.|  
|`JsErrorCannotSerializeDebugScript`|Los scripts no se pueden serializar en contextos de depuración.|  
|`JsErrorCategoryEngine`|Categoría de errores relacionados con errores que se producen en el motor en sí.|  
|`JsErrorCategoryFatal`|Categoría de errores fatales y que significan un error del motor.|  
|`JsErrorCategoryScript`|Categoría de errores relacionados con errores en un script.|  
|`JsErrorCategoryUsage`|Categoría de errores que se relacionan con el uso incorrecto de la propia API.|  
|`JsErrorFatal`|Se ha producido un error grave en el motor.|  
|`JsErrorHeapEnumInProgress`|Actualmente se está realizando una enumeración de montones en el contexto de script.|  
|`JsErrorIdleNotEnabled`|Notificación de inactividad cuando el host no ha habilitado el procesamiento en inactividad.|  
|`JsErrorInDisabledState`|El tiempo de ejecución está en estado deshabilitado.|  
|`JsErrorInExceptionState`|El motor está en un estado de excepción y no se puede llamar a ninguna API hasta que se borre la excepción.|  
|`JsErrorInObjectBeforeCollectCallback`|La operación no se admite en un objeto antes de recopilar la devolución de llamada.<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsErrorInProfileCallback`|Un contexto de script está en medio de una devolución de llamada de perfil.|  
|`JsErrorInThreadServiceCallback`|Se está realizando una devolución de llamada del servicio de subprocesos.|  
|`JsErrorInvalidArgument`|Un argumento para una API de hospedaje no es válido.|  
|`JsErrorNoCurrentContext`|La API de hospedaje requiere que un contexto esté activo, pero no hay ningún contexto actual.|  
|`JsErrorNotImplemented`|Aún no se ha implementado una API de hospedaje.|  
|`JsErrorNullArgument`|Un argumento para una API de hospedaje es null en un contexto donde no está permitido el valor null.|  
|`JsErrorObjectNotInspectable`|El objeto no se puede desempaquetar como `IInspectable` puntero.<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsErrorOutOfMemory`|El motor de Chakra se ha quedado sin memoria.|  
|`JsErrorPropertyNotSymbol`|Una API de hospedaje que funciona en los identificadores de propiedad de símbolo pero se llamó con un identificador de propiedad sin símbolo. `JsGetSymbolFromPropertyId` Si se llama a la función con un identificador de propiedad sin símbolo, se devuelve el código de error.<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsErrorPropertyNotString`|Una API de hospedaje que funciona en identificadores de propiedad de cadena pero que se llamó con un identificador de propiedad no de cadena. Existing devuelve el código de error `JsGetPropertyNamefromId` si se llama a la función con el identificador de propiedad sin cadenas.<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsErrorRuntimeInUse`|Un Runtime que aún está en uso no se puede eliminar.|  
|`JsErrorScriptCompile`|Error al compilar JavaScript.|  
|`JsErrorScriptEvalDisabled`|Se terminó un script porque intentaste usar `eval` o `function` y eval se deshabilitó.|  
|`JsErrorScriptException`|Se produjo una excepción de JavaScript mientras se ejecutaba un script.|  
|`JsErrorScriptTerminated`|Se terminó un script a causa de una solicitud para suspender un tiempo de ejecución.|  
|`JsErrorWrongRuntime`|Se llamó a una API de hospedaje con un objeto creado en un tiempo de ejecución de JavaScript diferente.|  
|`JsErrorWrongThread`|Se llamó a una API de hospedaje en el subproceso equivocado.|  
|`JsNoError`|Código de error de éxito.|  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
