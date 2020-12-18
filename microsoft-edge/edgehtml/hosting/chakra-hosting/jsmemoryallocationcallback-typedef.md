---
description: Rutina de devolución de llamada implementada por el usuario para eventos de asignación de memoria.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236078"
---
# Definición de tipo JsMemoryAllocationCallback

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
