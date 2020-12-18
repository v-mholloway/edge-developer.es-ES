---
description: Devolución de llamada de función.
title: JsNativeFunction typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235901"
---
# Definición de tipo JsNativeFunction

Devolución de llamada de función.  
  
## Sintaxis  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### Parámetros  
 destinatario  
 `Function`Objeto que representa la función que se invoca.  
  
 isConstructCall  
 Indica si se trata de una llamada normal o de una llamada nueva.  
  
 arguments  
 Los argumentos de la llamada.  
  
 argumentCount  
 El número de argumentos.  
  
## Valor de propiedad y valor devuelto  
 El resultado de la llamada, si existe.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
