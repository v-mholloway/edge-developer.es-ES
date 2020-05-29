---
description: Representa una cadena de notificación pasada desde el contenido de WebView a la aplicación.
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572894"
---
# Objeto ScriptNotifyEvent

Un objeto que representa un evento que se desencadena cuando el contenido incluido en la [vista en WebView](../webview.md) pasa una cadena a la aplicación mediante JavaScript.

## Propiedades
    
### callingUri

Obtiene el identificador uniforme de recursos (URI) de la página que contiene el script que ha provocado el **ScriptNotifyEvent**.

Esta propiedad es de solo lectura.

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### Valor de propiedad
Escriba: **DOMString**

### value

El nombre del método como se pasó a la aplicación.

Esta propiedad es de solo lectura.

```js
var value = ScriptNotifyEvent.value;
```

#### Valor de propiedad
Escriba: **DOMString**