---
description: Detiene la generación de perfiles en el contexto actual.
title: Función JsStopProfiling | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574403"
---
# Función JsStopProfiling
Detiene la generación de perfiles en el contexto actual.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### Parámetros  
 `reason`  
 El motivo de detener la generación de perfiles para pasar a la devolución de llamada del generador de perfiles.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 No devolverá un error si la generación de perfiles no se ha iniciado.  
  
 Requiere un contexto de script activo.  
  
 Esta API es compatible con las aplicaciones de escritorio, pero no es compatible con las aplicaciones de la tienda.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)