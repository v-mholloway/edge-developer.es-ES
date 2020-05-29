---
description: Define las propiedades que habilitan o deshabilitan características de WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573368"
---
# Objeto MSWebViewSettings

Define las propiedades que habilitan o deshabilitan características de [WebView](../webview.md) .

## Propiedades

### isIndexedDBEnabled

Obtiene o establece un valor que indica si se permite el uso de IndexedDB en [WebView](../webview.md).

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### Valor de propiedad
Tipo: **Boolean**

**Verdadero** si IndexedDB está permitido en la **vista de vista**de usuario; en caso contrario, **false**. 

### isJavaScriptEnabled

Obtiene o establece un valor que indica si se permite el uso de JavaScript en [WebView](../webview.md).

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### Valor de propiedad
Tipo: **Boolean**

**Verdadero** Se permite JavaScript en la [vista](../webview.md)de usuario; en caso contrario, **false**. 

### isScriptNotifyAllowed

Obtiene o establece un valor que indica si se permite el uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) en [WebView](../webview.md).

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### Valor de propiedad
Tipo: **Boolean**

Se permite **verdadero** [ScriptNotifyEvent](ScriptNotifyEvent.md) en la [vista](../webview.md)de usuario; en caso contrario, **false**. 
