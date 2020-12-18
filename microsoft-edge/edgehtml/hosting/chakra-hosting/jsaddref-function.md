---
description: Agrega una referencia a un objeto recolectado recolectado.
title: Función JsAddRef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236112"
---
# Función JsAddRef

Agrega una referencia a un objeto recolectado recolectado.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### Parámetros  
 `ref`  
 Objeto al que se va a agregar una referencia.  
  
 `count`  
 El nuevo recuento de referencia del objeto (puede pasar el valor null).  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Esto solo debe llamarse en `JsRef` los identificadores que no se van a almacenar en algún lugar de la pila. `JsAddRef`Las llamadas garantizan que el objeto al que `JsRef` hace referencia no se liberará hasta que `JsRelease` se llame.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
