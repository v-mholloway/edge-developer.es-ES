---
description: Analiza una secuencia de comandos serializada y devuelve una función que representa el script. Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.
title: Función JsParseSerializedScriptWithCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ad6d635722f0b3fea8b19f8d16679b402d1fd56e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574548"
---
# Función JsParseSerializedScriptWithCallback
Analiza una secuencia de comandos serializada y devuelve una función que representa el script. Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### Parámetros  
 `scriptLoadCallback`  
 Devolución de llamada llamada cuando es necesario cargar el código fuente del script.  
  
 `scriptUnloadCallback`  
 Devolución de llamada llamada cuando ya no se necesita el script y el código de origen serializados.  
  
 `buffer`  
 El script serializado.  
  
 `sourceContext`  
 Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.     Este contexto se transmitirá a scriptLoadCallback y scriptUnloadCallback.  
  
 `sourceUrl`  
 La ubicación de la que procede la secuencia de comandos.  
  
 `result`  
 Una función que representa el código de la secuencia de comandos.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
  
> [!NOTE]
>  Esta API aún no está disponible para las aplicaciones de la tienda.  
  
 Requiere un contexto de script activo.  
  
 El motor en tiempo de ejecución retendrá el búfer hasta que se hayan recolectado como no utilizados todas las instancias de las funciones creadas desde el búfer.  A continuación, llamará a scriptUnloadCallback para informar al autor de la llamada de que es seguro liberarlo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)