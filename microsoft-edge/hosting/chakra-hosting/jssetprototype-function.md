---
description: Establece el prototipo de un objeto.
title: Función JsSetPrototype | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 625269c5f9f459a5c7eecb6cfc31cb85fc24214b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574422"
---
# Función JsSetPrototype
Establece el prototipo de un objeto.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### Parámetros  
 `object`  
 Objeto cuyo prototipo se va a cambiar.  
  
 `prototypeObject`  
 El nuevo prototipo del objeto.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)