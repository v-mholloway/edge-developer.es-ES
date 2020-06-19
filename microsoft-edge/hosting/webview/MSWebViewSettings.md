---
description: Define las propiedades que habilitan o deshabilitan características de WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752181"
---
# Objeto MSWebViewSettings  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Define las propiedades que habilitan o deshabilitan características de [WebView](../webview.md) .  

## Propiedades  

### isIndexedDBEnabled  

Obtiene o establece un valor que indica si se permite el uso de IndexedDB en [WebView](../webview.md).  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

**Verdadero** si IndexedDB está permitido en la **vista de vista**de usuario; en caso contrario, **false**.  

### isJavaScriptEnabled  

Obtiene o establece un valor que indica si se permite el uso de JavaScript en [WebView](../webview.md).  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

**Verdadero** Se permite JavaScript en la [vista](../webview.md)de usuario; en caso contrario, **false**.  

### isScriptNotifyAllowed  

Obtiene o establece un valor que indica si se permite el uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) en [WebView](../webview.md).  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

Se permite **verdadero** [ScriptNotifyEvent](ScriptNotifyEvent.md) en la [vista](../webview.md)de usuario; en caso contrario, **false**.  
