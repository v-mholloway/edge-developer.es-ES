---
description: Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos. La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751943"
---
# Definición de tipo JsSerializedScriptUnloadCallback
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