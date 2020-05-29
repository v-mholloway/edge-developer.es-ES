---
description: Devuelve la excepción que causó que el runtime del contexto actual esté en estado de excepción y restablece el estado de excepción de ese Runtime.
title: Función JsGetAndClearException | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: eb70b4b66b4bb270d9f26487708720efddc2effa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574599"
---
# Función JsGetAndClearException
Devuelve la excepción que causó que el runtime del contexto actual esté en estado de excepción y restablece el estado de excepción de ese Runtime.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### Parámetros  
 `exception`  
 Excepción para el motor en tiempo de ejecución del contexto actual.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Si el tiempo de ejecución del contexto actual no está en un estado de excepción, esta API devolverá `JsErrorInvalidArgument` . Si el motor en tiempo de ejecución está deshabilitado, devolverá una excepción que indica que el script ha finalizado, pero no borrará la excepción (la excepción se borrará si el motor en tiempo de ejecución se vuelve a habilitar con el `JsEnableRuntimeExecution` ).  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)