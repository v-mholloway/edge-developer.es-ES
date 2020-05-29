---
description: Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.
title: Función JsSetException | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574516"
---
# Función JsSetException
Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Parámetros  
 `exception`  
 Excepción de JavaScript que se establece para el motor en tiempo de ejecución del contexto actual.  
  
## Valor devuelto  
 `JsNoError` Si el motor se ha configurado en un estado de excepción, de lo contrario, un código de error.  
  
## Observaciones  
 Si el tiempo de ejecución del contexto actual ya está en estado de excepción, esta API se devolverá `JsErrorInExceptionState` .  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)