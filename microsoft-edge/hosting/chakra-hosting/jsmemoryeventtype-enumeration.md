---
description: Tipo de evento de devolución de llamada de asignación.
title: JsMemoryEventType (enumeración) | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573420"
---
# Enumeración JsMemoryEventType
Tipo de evento de devolución de llamada de asignación.  
  
## Sintaxis  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## Miembros  
  
### Los  
  
|Nombre|Descripción|  
|----------|-----------------|  
|`JsMemoryAllocate`|Indica una solicitud de asignación de memoria.|  
|`JsMemoryFailure`|Indica un evento de asignación con error.|  
|`JsMemoryFree`|Indica un evento de liberación de memoria.|  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)