---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4dfe2296312ac3ff3e9c67667c660aafcea38211
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885761"
---
# 0.8.355: IWebView2WebMessageReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebMessageReceived.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Source](#get_source) | El URI del documento que envió este mensaje Web.
[get_WebMessageAsJson](#get_webmessageasjson) | Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.
[get_WebMessageAsString](#get_webmessageasstring) | Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

## Miembros

#### get_Source 

El URI del documento que envió este mensaje Web.

> [get_Source](#get_source)de HRESULT público (código LPWStr *)

#### get_WebMessageAsJson 

Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.

> [get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr * WebMessageAsJson)

Usa esta para comunicarte a través de objetos de JavaScript.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### get_WebMessageAsString 

Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

> [get_WebMessageAsString](#get_webmessageasstring)de HRESULT público (LPWStr * WebMessageAsString)

Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG. Use esta para comunicarse a través de cadenas simples.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

