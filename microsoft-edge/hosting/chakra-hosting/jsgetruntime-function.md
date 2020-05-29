---
description: Obtiene el motor en tiempo de ejecución al que pertenece el contexto.
title: Función JsGetRuntime | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573447"
---
# Función JsGetRuntime
Obtiene el motor en tiempo de ejecución al que pertenece el contexto.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### Parámetros  
 `context`  
 Contexto desde el que se va a obtener el motor en tiempo de ejecución.  
  
 `runtime`  
 El motor en tiempo de ejecución al que pertenece el contexto.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)