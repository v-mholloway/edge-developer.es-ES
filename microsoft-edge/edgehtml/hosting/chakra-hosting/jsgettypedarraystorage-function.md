---
description: Obtiene el almacenamiento de memoria subyacente utilizado por una matriz con tipo.
title: Función JsGetTypedArrayStorage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235942"
---
# Función JsGetTypedArrayStorage

Obtiene el almacenamiento de memoria subyacente utilizado por una matriz con tipo.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### Parámetros  
 `typedArray`  
 Instancia de matriz con tipo.  
  
 `buffer`  
 El búfer de la matriz. La vigencia del búfer devuelto es igual que la duración de la matriz. El puntero de búfer no se tiene en cuenta como una referencia a la matriz por el propósito de la recolección de elementos no utilizados.  
  
 `bufferLength`  
 El número de bytes del búfer.  
  
 `arrayType`  
 Tipo de la matriz.  
  
 `elementSize`  
 Tamaño de un elemento de la matriz.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
