---
description: Obtiene el contexto de script al que pertenece el objeto.
title: Función JsGetContextOfObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4f1b996954e877d9c98ac0caf06f255af629a386
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573467"
---
# Función JsGetContextOfObject
Obtiene el contexto de script al que pertenece el objeto.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### Parámetros  
 `object`  
 Objeto del que se va a obtener el contexto.  
  
 `context`  
 El contexto al que pertenece el objeto.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)