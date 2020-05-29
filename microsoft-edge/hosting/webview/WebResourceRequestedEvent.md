---
description: Un evento que se desencadena cuando se realiza una solicitud HTTP.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572890"
---
# Objeto WebResourceRequestedEvent

Un evento que se desencadena cuando se realiza una solicitud HTTP.

## Propiedades

### EventArgs

Información sobre la solicitud de recursos. Este es un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).

Esta propiedad es de solo lectura.

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### Valor de propiedad
Escriba lo siguiente: **cualquiera**

