---
description: Contiene información sobre la navegación de WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752145"
---
# Objeto NavigationCompletedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Un objeto que representa un evento que se desencadena cuando [WebView](../webview.md) ha terminado de cargar el contenido actual o si se ha producido un error en la navegación.  

## Propiedades  

### uri  

Identificador uniforme de recursos (URI) de la navegación.  

Esta propiedad es de solo lectura.  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### Valor de propiedad  

Escriba: **DOMString**  

### isSuccess  

Obtiene un valor que indica si la navegación se completó correctamente.  

Esta propiedad es de solo lectura.  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

### webErrorStatus  

Si la navegación no se realizó correctamente, obtiene un valor que indica por qué.  

Esta propiedad es de solo lectura.  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### Valor de propiedad  

Tipo: **largo sin signo**  
