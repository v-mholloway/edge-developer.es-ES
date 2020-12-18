---
description: Devolución de llamada del servicio de subprocesos.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236232"
---
# Definición de tipo JsThreadServiceCallback

Devolución de llamada del servicio de subprocesos.  
  
## Sintaxis  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### Parámetros  
 devolución  
 Devolución de llamada para el elemento de trabajo en segundo plano.  
  
 Devolución  
 El argumento de datos que se va a pasar a la devolución de llamada.  
  
## Observaciones  
 El host puede especificar un servicio de subproceso en segundo plano al llamar a JsCreateRuntime. Si se especifica, los elementos de trabajo de fondo se pasarán al host mediante esta devolución de llamada. Se espera que el host empiece a ejecutar el elemento de trabajo de fondo inmediatamente y devuelva true o devuelva false, y el tiempo de ejecución controlará el elemento de trabajo de subproceso.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
