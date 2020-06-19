---
description: Establece los datos internos de JsrtContext.
title: Función JsSetContextData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e874f500ca82328dddeaaa03a0b78a188b8fd241
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751936"
---
# Función JsSetContextData
Establece los datos internos de JsrtContext.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### Parámetros  
 `context`  
 Contexto en el que se van a establecer los datos.  
  
 `data`  
 Puntero a los datos que se van a establecer.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)