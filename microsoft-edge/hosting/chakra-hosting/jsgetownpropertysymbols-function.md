---
description: Obtiene la lista de todas las propiedades de símbolo en el objeto.
title: Función JsGetOwnPropertySymbols | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7a7f4e88986a45fbccfae0c53e92ff2e5313991
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574585"
---
# Función JsGetOwnPropertySymbols
Obtiene la lista de todas las propiedades de símbolo en el objeto.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### Parámetros  
 `object`  
 Objeto del que se van a obtener los símbolos de propiedad.  
  
 `propertySymbols`  
 Matriz de símbolos de propiedad.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)