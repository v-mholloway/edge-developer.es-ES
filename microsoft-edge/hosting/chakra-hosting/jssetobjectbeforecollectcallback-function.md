---
description: Establece una función de devolución de llamada a la que llama el motor en tiempo de ejecución antes de la recolección de elementos no utilizados de un objeto.
title: Función JsSetObjectBeforeCollectCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574507"
---
# Función JsSetObjectBeforeCollectCallback
Establece una función de devolución de llamada a la que llama el motor en tiempo de ejecución antes de la recolección de elementos no utilizados de un objeto.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### Parámetros  
 `ref`  
 Objeto para el que se va a registrar la devolución de llamada.  
  
 `callbackState`  
 Estado proporcionado por el usuario que se devolverá a la devolución de llamada.  
  
 `objectBeforeCollectCallback`  
 Función de devolución de llamada que se establece. Use null para borrar la devolución de llamada previamente registrada.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 La devolución de llamada se invoca en el actual subproceso de ejecución en tiempo de ejecución; por lo tanto, la ejecución se bloquea hasta que se completa la devolución de llamada.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)