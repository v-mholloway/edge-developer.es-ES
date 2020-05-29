---
description: Serializa una secuencia de comandos analizada en un búfer del que se puede volver a usar.
title: Función JsSerializeScript | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1b45067fddb7ea4dff02e527e460db1270011c61
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574520"
---
# Función JsSerializeScript
Serializa una secuencia de comandos analizada en un búfer del que se puede volver a usar.  
  
## Sintaxis  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### Parámetros  
 `script`  
 Script que se va a serializar.  
  
 `buffer`  
 El búfer en el que se coloca el script serializado. Puede ser null.  
  
 `bufferSize`  
 En la entrada, el tamaño del búfer, en bytes; al salir, el tamaño del búfer, en bytes, necesario para mantener el script serializado.  
  
## Valor devuelto  
 El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.  
  
## Observaciones  
 `JsSerializeScript` analiza un script y, a continuación, almacena el formulario analizado de la secuencia de comandos en un formato independiente del tiempo de ejecución. El script serializado se puede deserializar en cualquier Runtime sin necesidad de volver a analizar el script.  
  
 Requiere un contexto de script activo.  
  
## Requisitos  
 **Encabezado:** jsrt. h  
  
## Consulta también  
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)