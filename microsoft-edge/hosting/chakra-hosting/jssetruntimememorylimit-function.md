---
description: Establece el límite de memoria actual para un tiempo de ejecución.
title: Función JsSetRuntimeMemoryLimit | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ec8d098c528ac813926797280541aa2c9c4fee79
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574408"
---
# Función JsSetRuntimeMemoryLimit
Establece el límite de memoria actual para un tiempo de ejecución.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### Parámetros  
 `runtime`  
 Tiempo de ejecución cuyo límite de memoria se va a establecer.  
  
 `memoryLimit`  
 El nuevo límite de memoria en tiempo de ejecución, en bytes, o-1 para sin límite de memoria.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Un límite de memoria hará que cualquier operación que supere el límite falle con un error de "memoria insuficiente". Establecer el límite de memoria de un tiempo de ejecución en-1 significa que el motor en tiempo de ejecución no tiene límite de memoria. Los nuevos runtimes tienen como valor predeterminado un límite de memoria. Si el nuevo límite de memoria supera el uso actual, la llamada se realizará correctamente y cualquier asignación futura en este Runtime producirá un error hasta que el uso de memoria del Runtime descienda por debajo del límite.  
  
 El límite de memoria de un motor en tiempo de ejecución se puede establecer siempre, independientemente de si el motor en tiempo de ejecución está activo o no en otro subproceso.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)