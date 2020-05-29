---
description: Contiene información de referencia sobre la navegación
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573361"
---
# Objeto NavigationEventWithReferrer

Un objeto que representa un evento que se desencadena cuando se inicia la navegación y la navegación contiene una referencia.

## Propiedades

### Referer

Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.

Esta propiedad es de solo lectura.

#### Valor de propiedad
Escriba: **DOMString**


```js
var referer = NavigationEventWithReferrer.referer;
```

### uri

Identificador uniforme de recursos (URI) del destino de la navegación.

Esta propiedad es de solo lectura.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Valor de propiedad
Escriba: **DOMString**
