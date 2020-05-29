---
description: Establece la devolución de llamada que se va a usar para invocar una finalización de proyección a la persona que llama obligatoria.
title: Función JsSetProjectionEnqueueCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574503"
---
# Función JsSetProjectionEnqueueCallback
Establece la devolución de llamada que se va a usar para invocar una finalización de proyección a la persona que llama obligatoria.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### Parámetros  
 `projectionEnqueueContext`  
 Devolución de llamada que se invocará cada vez que se complete una proyección en un subproceso en segundo plano.  
  
 `callbackState`  
 El contexto de la aplicación proporcionado a `projectionEnqueueContext` .  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 La llamada debe proceder de un apartamento COM diferente o de un subproceso diferente en el mismo MTA.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
> [!CAUTION]
>  En este momento, PInvoke no es compatible con esta API.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)