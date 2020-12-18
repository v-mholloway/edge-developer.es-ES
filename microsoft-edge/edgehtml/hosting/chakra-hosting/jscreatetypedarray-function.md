---
description: Crea un objeto de matriz con tipo de JavaScript.
title: Función JsCreateTypedArray | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62f62296d81dafe6515f69a990e33ff5c00730e1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236432"
---
# Función JsCreateTypedArray

Crea un objeto de matriz con tipo de JavaScript.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parámetros  
 `arrayType`  
 Tipo de matriz que se va a crear.  
  
 `baseArray`  
 Matriz base de la nueva matriz. Usar `JS_INVALID_REFERENCE` si no hay ninguna matriz base.  
  
 `byteOffset`  
 Desplazamiento en bytes desde el principio de `baseArray` ( `ArrayBuffer` ) para la matriz con tipo de resultado a la que se hará referencia. Solo es aplicable cuando `baseArray` es un `ArrayBuffer` objeto. En caso contrario, debe ser 0.  
  
 `elementLength`  
 Número de elementos de la matriz. Solo es aplicable al crear una matriz con tipo nueva sin `baseArray` ( `baseArray` es `JS_INVALID_REFERENCE` ) o cuando `baseArray` es un `ArrayBuffer` objeto. En caso contrario, debe ser 0.  
  
 `result`  
 El nuevo objeto de matriz con tipo.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 `baseArray`Puede ser una `ArrayBuffer` , otra matriz con tipo o un JavaScript `Array` . La matriz con tipo devuelta usará `baseArray` si es una `ArrayBuffer` o, de lo contrario, crear y usar una copia de la matriz de origen subyacente.  
  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
