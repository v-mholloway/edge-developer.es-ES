---
description: Contiene información de referencia sobre la navegación
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752132"
---
# Objeto NavigationEventWithReferrer  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Un objeto que representa un evento que se desencadena cuando se inicia la navegación y la navegación contiene una referencia.  

## Propiedades  

### Referer

Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.  

Esta propiedad es de solo lectura.  

#### Valor de propiedad  

Escriba: **DOMString**  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### uri  

Identificador uniforme de recursos (URI) del destino de la navegación.  

Esta propiedad es de solo lectura.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Valor de propiedad  

Escriba: **DOMString**  
