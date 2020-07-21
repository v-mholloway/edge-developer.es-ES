---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c42e353c80335b6dccdad49b470e68fa5ae2f559
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884256"
---
# 0.9.430: ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento DevToolsProtocolEventReceived.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_ParameterObjectAsJson](#get_parameterobjectasjson) | El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.

## Miembros

#### get_ParameterObjectAsJson 

El objeto de parámetro del evento DevToolsProtocol correspondiente representado como una cadena JSON.

> [get_ParameterObjectAsJson](#get_parameterobjectasjson)de HRESULT público (LPWStr * ParameterObjectAsJson)

