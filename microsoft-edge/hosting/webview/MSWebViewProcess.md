---
description: Representa un proceso de WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573370"
---
# Objeto MSWebViewProcess

Representa un proceso de [WebView](../webview.md) .

```js
var wvprocess = new MSWebViewProcess();
```

## Propiedades

### enterpriseId

IDENTIFICADOR de empresa del proceso.

```js
var enterpriseId = wvprocess.enterpriseId;
```

Esta propiedad es de solo lectura.

#### Valor de propiedad
Escriba: **DOMString**

### isPrivateNetworkClientServerCapabilityEnabled

Obtiene un valor que indica si el proceso de [WebView](../webview.md) tiene la [declaración de funcionalidades](/windows/uwp/packaging/app-capability-declarations) de la aplicación universal de Windows *(cliente & servidor)* habilitada en el manifiesto de la aplicación.

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

Esta propiedad es de solo lectura.

#### Valor de propiedad
Tipo: **Boolean**

## Métodos

### CreateWebViewAsync

Crea un [WebView](../webview.md) en un proceso específico.

```js
wvprocess.createWebviewAsync();
```

#### Valor devuelto

Escrita**`Promise<MSHTMLWebViewElement>`**

### GetWebViews

Devuelve una secuencia de objetos **MSWebViewProcess** hospedados en el proceso.

#### Valor devuelto

Escrita**`sequence<MSHTMLWebViewElement>`**

### Detiene

Finaliza el proceso.

```js
wvprocess.terminate();
```

#### Valor devuelto

Este método no devuelve un valor.
