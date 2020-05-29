---
description: Determina si el motor en tiempo de ejecución del contexto actual se encuentra en estado de excepción.
title: Función JsHasException | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574565"
---
# Función JsHasException
Determina si el motor en tiempo de ejecución del contexto actual se encuentra en estado de excepción.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### Parámetros  
 `hasException`  
 Si el tiempo de ejecución del contexto actual está en el estado de excepción.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Si una llamada al motor en tiempo de ejecución genera una excepción (ya sea como resultado de ejecutar un script o debido a un error de conversión), el motor en tiempo de ejecución se coloca en "estado de excepción". Se producirá un error en todas las llamadas creadas por el motor en tiempo de ejecución (excepto las API de excepción) `JsErrorInExceptionState` hasta que se borre la excepción.  
  
 Si el tiempo de ejecución del contexto actual está en el estado de excepción cuando se devuelve una devolución de llamada en el motor, el motor volverá a iniciar automáticamente la excepción.  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)