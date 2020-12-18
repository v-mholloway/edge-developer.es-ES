---
description: La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.
title: JsProjectionCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236407"
---
# Definición de tipo JsProjectionCallback

La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.  
  
## Sintaxis  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### Parámetros  
 `jsContext`  
 Requiere `JsSetProjectionEnqueueCallback` que se llame para recibir devoluciones de llamada.  
  
## Observaciones  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
