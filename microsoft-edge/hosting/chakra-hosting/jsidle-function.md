---
description: Indica al motor en tiempo de ejecución que realice cualquier procesamiento de inactividad que tenga que hacer.
title: Función JsIdle | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574559"
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