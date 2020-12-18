---
description: Una referencia a un contexto de script.
title: JsContextRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236099"
---
# Definición de tipo JsContextRef

Una referencia a un contexto de script.  
  
## Sintaxis  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Observaciones  
 Cada contexto de script contiene su propio objeto global, distinto del objeto global en otros contextos de script.  
  
 Muchas API de hospedaje de Chakra requieren un contexto de script "activo", que se puede establecer mediante `JsSetCurrentContext` . Las API de hospedaje de Chakra que requieren un contexto actual se encontrarán en la documentación de forma explícita.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
