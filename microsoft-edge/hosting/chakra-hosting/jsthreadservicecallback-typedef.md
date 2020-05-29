---
description: Devolución de llamada del servicio de subprocesos.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573403"
---
# JsThreadServiceCallback typedef
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