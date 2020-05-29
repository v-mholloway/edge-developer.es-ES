---
description: Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573411"
---
# JsProjectionEnqueueCallback typedef
Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.  
  
## Sintaxis  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parámetros  
 `jsCallback`  
 Devolución de llamada que se va a invocar en el subproceso original.  
  
 `jsContext`  
 El contexto de las aplicaciones.  
  
 `callbackState`  
 El contexto de JsRT que se debe pasar `jsCallback` .  
  
## Observaciones  
 Requiere la llamada a JsSetProjectionEnqueueCallback para recibir devoluciones de llamada.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)