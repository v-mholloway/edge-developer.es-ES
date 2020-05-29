---
description: La devolución de llamada de JsRT a la que se debe llamar con el contexto pasado al `JsProjectionEnqueueCallback` subproceso correcto.
title: JsProjectionCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573412"
---
# JsProjectionCallback typedef
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