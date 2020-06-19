---
description: Ejecuta una secuencia de comandos serializada. Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.
title: Función JsRunSerializedScriptWithCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84a74d3c1aa68469dfe2fe42fdee685faa4c358c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752223"
---
# Función JsRunSerializedScriptWithCallback
Ejecuta una secuencia de comandos serializada. Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
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
 El resultado de ejecutar el script, si existe. Este parámetro puede ser null.  
  
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