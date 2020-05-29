---
description: Suspende la ejecución de scripts y finaliza cualquier script que se esté ejecutando en un tiempo de ejecución.
title: Función JsDisableRuntimeExecution | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573473"
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