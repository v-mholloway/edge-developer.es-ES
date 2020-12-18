---
description: Establece el motor en tiempo de ejecución del contexto actual en un estado de excepción.
title: Función JsSetException | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236277"
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
