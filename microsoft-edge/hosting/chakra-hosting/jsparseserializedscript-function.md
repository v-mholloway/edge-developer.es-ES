---
description: Analiza una secuencia de comandos serializada y devuelve una función que representa el script.
title: Función JsParseSerializedScript | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a778a007e69f15063d23cc55f999144ab55a306c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574551"
---
# Función JsParseSerializedScript
Analiza una secuencia de comandos serializada y devuelve una función que representa el script.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parámetros  
 `script`  
 Script que se va a analizar.  
  
 `buffer`  
 El script serializado.  
  
 `sourceContext`  
 Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.  
  
 `sourceUrl`  
 La ubicación de la que procede la secuencia de comandos.  
  
 `result`  
 Una función que representa el código de la secuencia de comandos.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 Requiere un contexto de script activo.  
  
 El motor de scripting no conserva el búfer en la memoria, por lo que el código debe mantenerlo activo durante el tiempo que pueda usarse para ejecutar scripts.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)