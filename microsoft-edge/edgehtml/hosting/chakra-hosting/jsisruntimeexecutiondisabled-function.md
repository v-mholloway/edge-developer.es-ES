---
description: Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.
title: Función JsIsRuntimeExecutionDisabled | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235902"
---
# Función JsIsRuntimeExecutionDisabled

Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### Parámetros  
 `runtime`  
 Especifica el motor en tiempo de ejecución para comprobar si la ejecución está deshabilitada.  
  
 `isDisabled`  
 `true` Si la ejecución está deshabilitada, de `false` lo contrario.  
  
## Valor devuelto  
 `JsNoError` Si la operación se realizó correctamente, un código de error en caso contrario.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
