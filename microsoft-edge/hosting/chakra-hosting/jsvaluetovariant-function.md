---
description: Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.
title: Función JsValueToVariant | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573396"
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