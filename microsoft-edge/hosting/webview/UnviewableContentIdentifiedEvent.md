---
description: Indica que la vista de la vista previa está intentando descargar un archivo no compatible.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572893"
---
# Objeto UnviewableContentIdentifiedEvent

Indica que [WebView](../webview.md) está intentando navegar a un archivo de un tipo de contenido no admitido. 

## Propiedades

### Medio

Obtiene el tipo de contenido del contenido que no se ve.

Esta propiedad es de solo lectura

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### Valor de propiedad
Escriba: **DOMString**

### Referer

Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.

Esta propiedad es de solo lectura.


```js
var referer = NavigationEventWithReferrer.referer;
```

#### Valor de propiedad
Escriba: **DOMString**

### uri

Identificador uniforme de recursos (URI) del destino de la navegación.

Esta propiedad es de solo lectura.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Valor de propiedad
Escriba: **DOMString**
