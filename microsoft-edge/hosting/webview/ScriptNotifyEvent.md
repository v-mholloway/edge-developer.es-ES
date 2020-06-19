---
description: Representa una cadena de notificación pasada desde el contenido de WebView a la aplicación.
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752027"
---
# Objeto ScriptNotifyEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Un objeto que representa un evento que se desencadena cuando el contenido incluido en la [vista en WebView](../webview.md) pasa una cadena a la aplicación mediante JavaScript.  

## Propiedades  

### callingUri  

Obtiene el identificador uniforme de recursos (URI) de la página que contiene el script que ha provocado el **ScriptNotifyEvent**.  

Esta propiedad es de solo lectura.  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### Valor de propiedad  

Escriba: **DOMString**  

### value  

El nombre del método como se pasó a la aplicación.  

Esta propiedad es de solo lectura.  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### Valor de propiedad  

Escriba: **DOMString**  
