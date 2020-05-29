---
description: Desenvuelve un objeto de JavaScript en un `IInspectable` puntero.
title: Función JsObjectToInspectable | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574556"
---
# Función JsObjectToInspectable
Desenvuelve un objeto de JavaScript en un `IInspectable` puntero.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### Parámetros  
 `value`  
 Un valor de JavaScript al que se debe proyectar `IInspectable` .  
  
 `inspectable`  
 Un `IInspectable` valor del objeto.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Los hosts son responsables de exigir reglas de subprocesamiento COM.  
  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)