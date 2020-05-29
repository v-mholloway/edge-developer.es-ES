---
description: Una devolución de llamada de elemento de trabajo en segundo plano.
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573537"
---
# JsBackgroundWorkItemCallback typedef
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