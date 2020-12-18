---
description: Obtiene el almacenamiento de memoria subyacente utilizado por DataView.
title: Función JsGetDataViewStorage | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236326"
---
# Función JsGetDataViewStorage

Obtiene el almacenamiento de memoria subyacente usado por un `DataView` .  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Parámetros  
 `dataView`  
 La instancia de DataView.  
  
 `buffer`  
 El búfer de DataView. La duración del búfer devuelto es la misma que la del `DataView` . El puntero de búfer no se cuenta como una referencia a la `DataView` finalidad de la recolección de elementos no utilizados.  
  
 `bufferLength`  
 El número de bytes del búfer.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo Microsoft Edge.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
