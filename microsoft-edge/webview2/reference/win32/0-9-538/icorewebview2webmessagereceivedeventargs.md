---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c7d3d03fc1a0d53db403dab6c91dcdcf5ad6fd28
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699428"
---
# interfaz ICoreWebView2WebMessageReceivedEventArgs 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebMessageReceived.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Source](#get_source) | El URI del documento que envió este mensaje Web.
[get_WebMessageAsJson](#get_webmessageasjson) | Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

## Miembros

#### get_Source 

El URI del documento que envió este mensaje Web.

> [get_Source](#get_source)de HRESULT público (código LPWStr *)

#### get_WebMessageAsJson 

Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.

> [get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr * WebMessageAsJson)

Usa esta para comunicarte a través de objetos de JavaScript.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

> [TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr * webMessageAsString)

Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG. Use esta para comunicarse a través de cadenas simples.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

