---
description: El tipo de JavaScript de un JsValueRef.
title: JsValueType (enumeración) | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236228"
---
# Enumeración de JsValueType

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
