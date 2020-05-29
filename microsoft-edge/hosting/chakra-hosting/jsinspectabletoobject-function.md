---
description: Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .
title: Función JsInspectableToObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573434"
---
# Función JsInspectableToObject
Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### Parámetros  
 `inspectable`  
 `IInspectable`A para que se proyecte.  
  
 `value`  
 Un valor de JavaScript que es una proyección del `IInspectable` .  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 El script puede usar el valor previsto para llamar a un objeto de WinRT. Los hosts son responsables de exigir reglas de subprocesamiento COM.  
  
 Requiere un contexto de script activo.  
  
 Esta API solo se admite en el modo EdgeHTML.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)