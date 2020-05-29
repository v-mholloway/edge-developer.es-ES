---
description: Establece una función de devolución de llamada de continuación de Promise a la que llama el contexto cuando una tarea se debe poner en cola para su ejecución futura.
title: Función JsSetPromiseContinuationCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9438bf05d879b0c2014c0a4d49d374d26eff3fb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574504"
---
# Función JsSetPromiseContinuationCallback
Establece una función de devolución de llamada de continuación de Promise a la que llama el contexto cuando una tarea se debe poner en cola para su ejecución futura.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### Parámetros  
 `promiseContinuationCallback`  
 Función de devolución de llamada que se establece.  
  
 `callbackState`  
 Estado proporcionado por el usuario que se devolverá a la devolución de llamada.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)