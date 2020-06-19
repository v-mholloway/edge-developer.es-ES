---
description: Indica que la vista de la vista previa está intentando descargar un archivo no compatible.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752016"
---
# Objeto UnviewableContentIdentifiedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Indica que [WebView](../webview.md) está intentando navegar a un archivo de un tipo de contenido no admitido.  

## Propiedades  

### Medio  

Obtiene el tipo de contenido del contenido que no se ve.  

Esta propiedad es de solo lectura  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### Valor de propiedad  

Escriba: **DOMString**  

### Referer  

Identificador uniforme de recursos (URI) de la página de la [vista](../webview.md) web que solicita la navegación.  

Esta propiedad es de solo lectura.  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### Valor de propiedad  

Escriba: **DOMString**  

### uri  

Identificador uniforme de recursos (URI) del destino de la navegación.  

Esta propiedad es de solo lectura.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Valor de propiedad  

Escriba: **DOMString**  
