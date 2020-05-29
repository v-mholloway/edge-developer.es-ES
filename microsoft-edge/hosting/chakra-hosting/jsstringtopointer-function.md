---
description: Recupera el puntero de cadena de un valor de cadena.
title: Función JsStringToPointer | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574405"
---
# Función JsStringToPointer
Recupera el puntero de cadena de un valor de cadena.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### Parámetros  
 `value`  
 Valor de cadena que se va a convertir en un puntero de cadena.  
  
 `stringValue`  
 Puntero de cadena.  
  
 `stringLength`  
 La longitud de la cadena.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Esta función recupera el puntero de cadena de un valor de cadena. Se producirá un error `JsErrorInvalidArgument` si el tipo del valor no es una cadena. La duración de la cadena devuelta será la misma que la del valor que viene de lo procede, pero el puntero de cadena no se considera una referencia al valor (y, por lo tanto, no se conservará).  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)