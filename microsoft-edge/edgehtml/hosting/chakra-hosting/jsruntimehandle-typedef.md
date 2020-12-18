---
description: Identificador para un tiempo de ejecución de Chakra.
title: JsRuntimeHandle typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236063"
---
# Definición de tipo JsRuntimeHandle

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
