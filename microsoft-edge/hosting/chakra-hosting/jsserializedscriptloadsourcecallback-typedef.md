---
description: Lo llama el motor en tiempo de ejecución para cargar el código fuente de la secuencia de comandos serializada. El autor de la llamada debe mantener el búfer de script válido hasta el `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752202"
---
# Definición de tipo JsSerializedScriptLoadSourceCallback
Lo llama el motor en tiempo de ejecución para cargar el código fuente de la secuencia de comandos serializada. El autor de la llamada debe mantener el búfer de script válido hasta el `JsSerializedScriptUnloadCallback` .  
  
## Sintaxis  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### Parámetros  
 `sourceContext`  
 El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .  
  
 `scriptBuffer`  
 El script devuelto.  
  
## Observaciones  
  
> [!WARNING]
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)