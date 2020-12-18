---
description: Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.
title: Función JsIdle | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236591"
---
# Función JsIdle

Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### Parámetros  
 `nextIdleTick`  
 La siguiente marca del sistema cuando haya más trabajo de inactividad para hacer. Puede ser null. Devuelve el número máximo de marcas si no hay nada de trabajo inactivo.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Si se ha habilitado el procesamiento en inactividad para el tiempo de ejecución actual, las llamadas `JsIdle` informarán al tiempo de ejecución actual de que el host está inactivo y que el tiempo de ejecución puede realizar tareas de limpieza de memoria.  
  
 `JsIdle` también puede devolver el número de marcas del sistema hasta que haya más trabajo de inactividad para que lo haga el motor en tiempo de ejecución. Las llamadas `JsIdle` antes de que se haya pasado este número de marcas no funcionarán.  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
