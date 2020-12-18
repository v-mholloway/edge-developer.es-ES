---
description: El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236403"
---
# Definición de tipo JsProjectionCallbackContext

El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.  
  
## Sintaxis  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Observaciones  
 Requiere `JsSetProjectionEnqueueCallback` que se llame para recibir devoluciones de llamada.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
