---
description: Obtiene el almacenamiento de memoria subyacente usado por un ArrayBuffer.
title: Función JsGetArrayBufferStorage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236205"
---
# Función JsGetArrayBufferStorage

Obtiene el almacenamiento de memoria subyacente usado por un `ArrayBuffer` .  
  
## Sintaxis  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Parámetros  
 `arrayBuffer`  
 La instancia de ArrayBuffer.  
  
 `buffer`  
 El búfer de ArrayBuffer. La duración del búfer devuelto es la misma que la del `ArrayBuffer` . El puntero de búfer no se cuenta como una referencia a la `ArrayBuffer` finalidad de la recolección de elementos no utilizados.  
  
 `bufferLength`  
 El número de bytes del búfer.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
