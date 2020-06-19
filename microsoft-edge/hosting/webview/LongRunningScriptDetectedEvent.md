---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752159"
---
# Objeto LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Proporciona información para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).  

## Propiedades  

### executionTime  

Obtiene el número de milisegundos que el elemento [WebView](../webview.md) ha estado ejecutando un script de ejecución prolongada.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### Valor de propiedad  

Tipo: **Long**  

### stopPageScriptExecution  

Detiene un script de ejecución larga que se ejecuta en el elemento [WebView](../webview.md) .  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### Valor de propiedad  

Tipo: **Boolean**  
