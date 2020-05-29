---
description: Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.
title: Función JsIsRuntimeExecutionDisabled | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573424"
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