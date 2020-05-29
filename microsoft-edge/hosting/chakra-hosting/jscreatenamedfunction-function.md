---
description: Crea una nueva función de JavaScript con el nombre.
title: Función JsCreateNamedFunction | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573497"
---
# Función JsCreateNamedFunction
Crea una nueva función de JavaScript con el nombre.
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Parámetros  
 `name`  
 El nombre de esta función que se usará para propósitos de diagnóstico y stringification.  
  
 `nativeFunction`  
 El método al que se llama cuando se invoca la función.  
  
 `callbackState`  
 Estado proporcionado por el usuario que se devolverá a la devolución de llamada.  
  
 `function`  
 El nuevo objeto de función.  
  
## Valor devuelto  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)