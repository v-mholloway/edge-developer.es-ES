---
description: Establece las propiedades indizadas de un objeto en datos externos. Los datos externos se usarán como almacén posterior para las propiedades indizadas del objeto y se puede obtener acceso a ellos como una matriz con tipo.
title: Función JsSetIndexedPropertiesToExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236064"
---
# Función JsSetIndexedPropertiesToExternalData

Establece las propiedades indizadas de un objeto en datos externos. Los datos externos se usarán como almacén posterior para las propiedades indizadas del objeto y se puede obtener acceso a ellos como una matriz con tipo.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### Parámetros  
 `object`  
 Objeto en el que se va a trabajar.  
  
 `data`  
 Datos externos que se usarán como almacén trasero para las propiedades indizadas del objeto.  
  
 `arrayType`  
 El tipo de elemento de matriz en datos externos.  
  
 `elementLength`  
 El número de elementos de matriz de datos externos.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
