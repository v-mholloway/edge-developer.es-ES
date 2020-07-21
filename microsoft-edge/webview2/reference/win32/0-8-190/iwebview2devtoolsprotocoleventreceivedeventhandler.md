---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: a26a2c18c402bffe11353b2f53f0559acde3663b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886167"
---
# 0.8.355: IWebView2DevToolsProtocolEventReceivedEventHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived desde el [IWebView2WebView](IWebView2WebView.md).

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

> invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) * WebView,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) * args)

