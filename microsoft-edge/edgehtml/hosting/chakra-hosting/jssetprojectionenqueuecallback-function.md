---
description: Establece la devolución de llamada que se va a usar para invocar una finalización de proyección a la persona que llama obligatoria.
title: Función JsSetProjectionEnqueueCallback | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236061"
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
