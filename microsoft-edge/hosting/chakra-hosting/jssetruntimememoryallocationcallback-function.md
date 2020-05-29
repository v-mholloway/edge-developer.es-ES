---
description: Establece una devolución de llamada de asignación de memoria para el tiempo de ejecución especificado.
title: Función JsSetRuntimeMemoryAllocationCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574409"
---
# Función JsSetRuntimeMemoryAllocationCallback
Establece una devolución de llamada de asignación de memoria para el tiempo de ejecución especificado.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### Parámetros  
 `runtime`  
 Motor en tiempo de ejecución para el que se va a registrar la devolución de llamada de asignación.  
  
 `callbackState`  
 Estado proporcionado por el usuario que se devolverá a la devolución de llamada.  
  
 `allocationCallback`  
 Devolución de llamada de asignación de memoria que se va a llamar para eventos de asignación de memoria.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 El registro de una devolución de llamada de asignación de memoria hará que el motor en tiempo de ejecución devuelva la llamada al host siempre que adquiera memoria o libere memoria para el sistema operativo. Se llama a la rutina de devolución de llamada antes de que el administrador de memoria en tiempo de ejecución asigne un bloque de memoria. La asignación se rechazará si la devolución de llamada devuelve false. El administrador de memoria en tiempo de ejecución también invocará la rutina de devolución de llamada después de liberar un bloque de memoria, así como después de que se produzcan errores de asignación.  
  
 La devolución de llamada se invoca en el actual subproceso de ejecución en tiempo de ejecución; por lo tanto, la ejecución se bloquea hasta que se completa la devolución de llamada.  
  
 El valor devuelto de la devolución de llamada no se almacena; las asignaciones rechazadas previamente no impiden que el motor en tiempo de ejecución invoque la devolución de llamada más adelante para nuevas asignaciones de memoria.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)