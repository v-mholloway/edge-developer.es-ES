---
description: Obtiene el tipo de JavaScript de un JsValueRef.
title: Función JsGetValueType | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574566"
---
# Función JsGetValueType
Obtiene el tipo de JavaScript de un JsValueRef.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### Parámetros  
 `value`  
 El valor cuyo tipo se va a devolver.  
  
 `type`  
 Tipo del valor.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)