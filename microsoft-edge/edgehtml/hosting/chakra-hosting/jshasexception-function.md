---
description: Determina si el motor en tiempo de ejecución del contexto actual se encuentra en estado de excepción.
title: Función JsHasException | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235945"
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
