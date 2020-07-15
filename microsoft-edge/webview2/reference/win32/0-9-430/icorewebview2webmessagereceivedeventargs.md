---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c619c066151941f1177d55c973569c89f03daa2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880167"
---
# 0.9.430: ICoreWebView2WebMessageReceivedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

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

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.

> [TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr * webMessageAsString)

Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG. Use esta para comunicarse a través de cadenas simples.

Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

