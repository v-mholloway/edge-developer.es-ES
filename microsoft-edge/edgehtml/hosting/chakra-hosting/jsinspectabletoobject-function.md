---
description: Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .
title: Función JsInspectableToObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236462"
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
