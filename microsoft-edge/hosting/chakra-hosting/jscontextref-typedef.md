---
description: Una referencia a un contexto de script.
title: JsContextRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573524"
---
# JsContextRef typedef
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