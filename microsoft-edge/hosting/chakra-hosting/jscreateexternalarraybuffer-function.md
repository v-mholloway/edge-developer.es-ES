---
description: Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.
title: Función JsCreateExternalArrayBuffer | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573501"
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