---
description: Suspende la ejecución de scripts y finaliza cualquier script que se esté ejecutando en un tiempo de ejecución.
title: Función JsDisableRuntimeExecution | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236281"
---
# Función JsDisableRuntimeExecution

Suspende la ejecución de scripts y finaliza cualquier script que se esté ejecutando en un tiempo de ejecución.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Parámetros  
 `runtime`  
 Tiempo de ejecución que se va a suspender.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Las llamadas a un tiempo de ejecución suspendido fallarán hasta que `JsEnableRuntimeExecution` se llame.  
  
 No es necesario llamar a esta API en el subproceso en el que el motor en tiempo de ejecución está activo. Aunque el motor en tiempo de ejecución se establecerá en un estado suspendido, un script en ejecución no se puede suspender inmediatamente; un script en ejecución se terminará con una excepción no interceptable lo antes posible.  
  
 Suspender la ejecución en un tiempo de ejecución que ya está suspendido no es de op.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
