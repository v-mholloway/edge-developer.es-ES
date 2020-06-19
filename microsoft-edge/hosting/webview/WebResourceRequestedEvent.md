---
description: Un evento que se desencadena cuando se realiza una solicitud HTTP.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751985"
---
# Objeto WebResourceRequestedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Un evento que se desencadena cuando se realiza una solicitud HTTP.  

## Propiedades  

### EventArgs  

Información sobre la solicitud de recursos.  Este es un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).  

Esta propiedad es de solo lectura.  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### Valor de propiedad  

Escriba lo siguiente: **cualquiera**  
