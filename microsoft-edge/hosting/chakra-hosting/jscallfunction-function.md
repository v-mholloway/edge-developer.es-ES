---
description: Invoca una función.
title: Función JsCallFunction | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f242ccef71d8a2b361dbe2d1a299728f5551f5d3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573530"
---
# Función JsCallFunction
Invoca una función.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### Parámetros  
 `function`  
 Función que se va a invocar.  
  
 `arguments`  
 Los argumentos de la llamada.  
  
 `argumentCount`  
 Número de argumentos que se pasan a la función.  
  
 `result`  
 El valor devuelto de la invocación de la función, si existe.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)