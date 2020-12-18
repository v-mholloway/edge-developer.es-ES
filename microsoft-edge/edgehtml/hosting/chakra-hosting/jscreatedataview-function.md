---
description: Crea un objeto de JavaScript `DataView` .
title: Función JsCreateDataView | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236076"
---
# Función JsCreateDataView

Crea un objeto de JavaScript `DataView` .  
  
## Sintaxis  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parámetros  
 `arrayBuffer`  
 Objeto existente `ArrayBuffer` para usar como almacenamiento para el objeto de resultado `DataView` .  
  
 `byteOffset`  
 Desplazamiento en bytes desde el inicio de `arrayBuffer` para el resultado `DataView` a la referencia.  
  
 `byteLength`  
 El número de bytes en el ArrayBuffer de resultado de DataView al que hacer referencia.  
  
 `result`  
 Nuevo objeto DataView.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
