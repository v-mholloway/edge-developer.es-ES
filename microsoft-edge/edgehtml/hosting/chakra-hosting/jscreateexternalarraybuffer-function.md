---
description: Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.
title: Función JsCreateExternalArrayBuffer | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236469"
---
# Función JsCreateExternalArrayBuffer

Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### Parámetros  
 `data`  
 Puntero a la memoria externa.  
  
 `byteLength`  
 El número de bytes de la memoria externa.  
  
 `finalizeCallback`  
 Una devolución de llamada para cuando el objeto está finalizado. Puede ser null.  
  
 `callbackState`  
 El estado proporcionado por el usuario que se devolverá a finalizeCallback.  
  
 `result`  
 El `ArrayBuffer` objeto nuevo.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
