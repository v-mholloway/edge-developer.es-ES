---
description: Obtiene las propiedades de una matriz con tipo que se usan con frecuencia.
title: Función JsGetTypedArrayInfo | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236445"
---
# Función JsGetTypedArrayInfo

Obtiene las propiedades de una matriz con tipo que se usan con frecuencia.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### Parámetros  
 `typedArray`  
 Instancia de matriz con tipo.  
  
 `arrayType`  
 Tipo de la matriz.  
  
 `arrayBuffer`  
 El `ArrayBuffer` almacén de la matriz.  
  
 `byteOffset`  
 Desplazamiento en bytes desde el inicio de arrayBuffer al que hace referencia la matriz.  
  
 `byteLength`  
 El número de bytes de la matriz.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
