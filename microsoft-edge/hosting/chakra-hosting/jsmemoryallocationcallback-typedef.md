---
description: Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573423"
---
# JsMemoryAllocationCallback typedef
Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.  
  
## Sintaxis  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### Parámetros  
 callbackState  
 El estado pasado a JsSetRuntimeMemoryAllocationCallback.  
  
 allocationEvent  
 Tipo de evento de asignación de tipo.  
  
 allocate  
 El tamaño de la asignación.  
  
## Valor de propiedad y valor devuelto  
 Para el evento JsMemoryAllocate, devolver true permite que el motor en tiempo de ejecución continúe con la asignación. Si devuelve falso, significa que se rechaza la solicitud de asignación. El valor devuelto se omite para otros eventos de asignación.  
  
## Observaciones  
 Usa JsSetRuntimeMemoryAllocationCallback para registrar esta devolución de llamada.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)