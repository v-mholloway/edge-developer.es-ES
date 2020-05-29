---
description: Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos. La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574522"
---
# JsSerializedScriptUnloadCallback typedef
Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos. La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.  
  
## Sintaxis  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### Parámetros  
 `sourceContext`  
 El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .  
  
## Observaciones  
  
> [!WARNING]
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)