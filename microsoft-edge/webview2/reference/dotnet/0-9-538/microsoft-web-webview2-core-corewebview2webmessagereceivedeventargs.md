---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 01c6a22ec84b85437920dceb66072089fd6d0d93
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879663"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento WebMessageReceived.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Source](#source) | El URI del documento que envió este mensaje Web.
[WebMessageAsJson](#webmessageasjson) | Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

## Miembros

#### Source 

El URI del documento que envió este mensaje Web.

> [origen](#source) de cadena público

#### WebMessageAsJson 

Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.

> cadena pública [WebMessageAsJson](#webmessageasjson)

Usa esta para comunicarte a través de objetos de JavaScript.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

> cadena pública [TryGetWebMessageAsString](#trygetwebmessageasstring)()

Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG. Use esta para comunicarse a través de cadenas simples.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

