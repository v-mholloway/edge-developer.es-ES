---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573377"
---
# Objeto LongRunningScriptDetectedEvent

Proporciona información para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).

## Propiedades

### executionTime

Obtiene el número de milisegundos que el elemento [WebView](../webview.md) ha estado ejecutando un script de ejecución prolongada.

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### Valor de propiedad
Tipo: **Long**

### stopPageScriptExecution
Detiene un script de ejecución larga que se ejecuta en el elemento [WebView](../webview.md) .

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### Valor de propiedad
Tipo: **Boolean**