---
description: Recupera el `int` valor de un valor numérico.
title: Función JsNumberToInt | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574557"
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