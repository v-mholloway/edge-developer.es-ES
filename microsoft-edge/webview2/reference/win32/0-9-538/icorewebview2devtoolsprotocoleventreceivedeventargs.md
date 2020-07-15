---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880132"
---
# interfaz ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

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

