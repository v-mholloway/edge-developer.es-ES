---
description: Identificador para un tiempo de ejecución de Chakra.
title: JsRuntimeHandle typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574524"
---
# JsRuntimeHandle typedef
Identificador para un tiempo de ejecución de Chakra.  
  
## Sintaxis  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## Observaciones  
 Cada tiempo de ejecución de Chakra tiene su propio motor de ejecución independiente, compilador JIT y montón recolectado de basura. Como tal, cada Runtime está completamente aislado de otros runtimes.  
  
 Los Runtimes se pueden usar en cualquier subproceso, pero solo un subproceso puede llamar a tiempo de ejecución en cualquier momento.  
  
> [!WARNING]
>  Un JsRuntimeHandle, a diferencia de otras referencias de objeto de la API de hospedaje de Chakra, no se ha recolectado como no utilizado porque contiene el montón recolectado de elementos no utilizados. Un tiempo de ejecución continuará existiendo hasta que se llame a JsDisposeRuntime.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)