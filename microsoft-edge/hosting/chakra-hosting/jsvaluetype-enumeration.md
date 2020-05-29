---
description: El tipo de JavaScript de un JsValueRef.
title: JsValueType (enumeración) | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c42231525b55b49f0931a2ace33b373e0d4ae441
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573395"
---
# Enumeración JsValueType
El tipo de JavaScript de un JsValueRef.  
  
## Sintaxis  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## Miembros  
  
### Los  
  
|Nombre|Descripción|  
|----------|-----------------|  
|`JsUndefined`|El valor es el `undefined` valor.|  
|`JsNull`|El valor es el `null` valor.|  
|`JsNumber`|El valor es un valor de número de JavaScript.|  
|`JsString`|El valor es un valor de cadena de JavaScript.|  
|`JsBoolean`|El valor es un valor booleano de JavaScript.|  
|`JsObject`|El valor es un valor de objeto de JavaScript.|  
|`JsFunction`|El valor es un valor de objeto de función de JavaScript.|  
|`JsError`|El valor es un valor de objeto de error de JavaScript.|  
|`JsArray`|El valor es un valor de objeto de matriz de JavaScript.|  
|`JsSymbol`|El valor es un valor de símbolo de JavaScript.<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsArrayBuffer`|El valor es un valor de objeto de JavaScript `ArrayBuffer` .<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsTypedArray`|El valor es un valor de objeto de matriz con tipo de JavaScript.<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
|`JsDataView`|El valor es un valor de objeto de JavaScript `DataView` .<br /><br /> Este valor de enumeración solo se admite en el modo Microsoft Edge.|  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)