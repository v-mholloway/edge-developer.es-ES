---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a3d1f899cb270f9a44d92d647ab2f5a4d5c3b02a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886370"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

