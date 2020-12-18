---
description: Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.
title: Función JsValueToVariant | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236230"
---
# Función JsValueToVariant

Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### Parámetros  
 `object`  
 Un valor de JavaScript para proyectar como un `VARIANT` .  
  
 `variant`  
 Puntero a una `VARIANT` estructura que se inicializará como una proyección.  
  
## Valor devuelto  
  
## Observaciones  
 Los `VARIANT` clientes de automatización com pueden usar la proyección para llamar al objeto de JavaScript proyectado.  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
