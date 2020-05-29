---
description: Crea un valor de JavaScript que es una proyección del valor que se ha pasado `VARIANT` .
title: Función JsVariantToValue | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573392"
---
# Función JsVariantToValue
Crea un valor de JavaScript que es una proyección del valor que se ha pasado `VARIANT` .  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parámetros  
 `variant`  
 `VARIANT`A para que se proyecte.  
  
 `value`  
 Un valor de JavaScript que es una proyección del `VARIANT` .  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 El script puede utilizar el valor proyectado para llamar a un objeto de automatización COM desde un script. Los hosts son responsables de exigir reglas de subprocesamiento COM.  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)