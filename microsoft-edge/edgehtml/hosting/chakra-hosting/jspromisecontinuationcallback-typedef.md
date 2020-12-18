---
description: Una devolución de llamada de continuación de Promise.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236640"
---
# Definición de tipo JsPromiseContinuationCallback

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
