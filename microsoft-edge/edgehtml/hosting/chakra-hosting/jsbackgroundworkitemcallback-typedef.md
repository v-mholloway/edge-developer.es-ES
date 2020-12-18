---
description: Una devolución de llamada de elemento de trabajo en segundo plano.
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236110"
---
# Definición de tipo JsBackgroundWorkItemCallback

Una devolución de llamada de elemento de trabajo en segundo plano.  
  
## Sintaxis  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### Parámetros  
 Devolución  
 Argumento de datos pasado al servicio de subprocesos.  
  
## Observaciones  
 Este pasa al servicio de subprocesos del host (si se proporciona) para permitir que el host llame a la devolución de llamada del elemento de trabajo en el subproceso de fondo de su elección.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
