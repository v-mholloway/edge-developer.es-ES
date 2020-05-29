---
description: El contexto pasado a la devolución de llamada de la aplicación, JsProjectionEnqueueCallback, de JsRT y, a continuación, se devolvió a JsRT en la devolución de llamada proporcionada, `JsProjectionCallback` por la aplicación en el hilo correcto.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573413"
---
# JsProjectionCallbackContext typedef
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