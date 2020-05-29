---
description: Contiene información sobre la navegación de WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573367"
---
# Objeto NavigationCompletedEvent

Un objeto que representa un evento que se desencadena cuando [WebView](../webview.md) ha terminado de cargar el contenido actual o si se ha producido un error en la navegación.

## Propiedades
    
### uri

Identificador uniforme de recursos (URI) de la navegación.

Esta propiedad es de solo lectura.

```js
var uri = NavigationCompletedEvent.uri;
```

#### Valor de propiedad
Escriba: **DOMString**

### isSuccess

Obtiene un valor que indica si la navegación se completó correctamente.

Esta propiedad es de solo lectura

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### Valor de propiedad
Tipo: **Boolean**

### webErrorStatus

Si la navegación no se realizó correctamente, obtiene un valor que indica por qué.

Esta propiedad es de solo lectura

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### Valor de propiedad
Tipo: **largo sin signo**
