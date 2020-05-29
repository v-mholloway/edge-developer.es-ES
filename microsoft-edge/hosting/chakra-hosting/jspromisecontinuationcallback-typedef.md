---
description: Una devolución de llamada de continuación de Promise.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573405"
---
# JsPromiseContinuationCallback typedef
Una devolución de llamada de continuación de Promise.  
  
## Sintaxis  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parámetros  
 `task`  
  `callbackState`  
  
## Observaciones  
 El host puede especificar una devolución de llamada de continuación de Promise `JsSetPromiseContinuationCallback` . Si un script crea una tarea que se va a ejecutar más adelante, se llamará a la devolución de llamada de continuación de Promise con la tarea y la tarea debe ponerse en una cola FIFO, que se ejecutará cuando el script actual termine de ejecutarse.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)