---
description: Representa un proceso de WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752160"
---
# Objeto MSWebViewProcess  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Representa un proceso de [WebView](../webview.md) .  

```javascript
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

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

Esta propiedad es de solo lectura.  

#### Valor de propiedad  

Tipo: **Boolean**  

## Métodos  

### CreateWebViewAsync  

Crea un [WebView](../webview.md) en un proceso específico.  

```javascript
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

```javascript
wvprocess.terminate();
```  

#### Valor devuelto  

Este método no devuelve un valor.  
