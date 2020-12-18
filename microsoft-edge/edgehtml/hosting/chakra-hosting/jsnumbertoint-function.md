---
description: Recupera el `int` valor de un valor numérico.
title: Función JsNumberToInt | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236419"
---
# Función JsNumberToInt

Recupera el `int` valor de un valor numérico.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### Parámetros  
 `value`  
 Valor numérico que se va a convertir en un `int` valor.  
  
 `intValue`  
 El `int` valor.  
  
## Valor devuelto  
  
## Observaciones  
 Esta función recupera el valor de un valor de número y lo convierte en un `int` valor. Se producirá un error `JsErrorInvalidArgument` si el tipo del valor no es número.  
  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
