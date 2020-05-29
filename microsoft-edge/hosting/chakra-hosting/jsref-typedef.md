---
description: Una referencia a un objeto perteneciente al recolector de elementos no utilizados de Chakra.
title: JsRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574541"
---
# JsRef typedef
Una referencia a un objeto perteneciente al recolector de elementos no utilizados de Chakra.  
  
## Sintaxis  
  
```cpp  
typedef void *JsRef;  
```  
  
## Observaciones  
 Un tiempo de ejecución de Chakra realizará un seguimiento automático de las referencias de JsRef siempre que estén almacenadas en variables locales o en parámetros (es decir, en la pila). Almacenar un JsRef en cualquier lugar que no sea en la pila requiere llamar a JsAddRef y JsRelease para administrar la duración del objeto; de lo contrario, el recolector de elementos no utilizados puede liberar el objeto mientras aún está en uso.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)