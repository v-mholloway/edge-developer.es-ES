---
description: Devolución de llamada de la aplicación a la que llama JsRT cuando se completa una API de proyección en un subproceso diferente del original.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236642"
---
# Definición de tipo JsProjectionEnqueueCallback

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
