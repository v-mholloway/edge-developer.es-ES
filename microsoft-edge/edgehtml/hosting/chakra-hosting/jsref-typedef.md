---
description: Una referencia a un objeto perteneciente al recolector de elementos no utilizados de Chakra.
title: JsRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235904"
---
# Definición de tipo JsRef

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
