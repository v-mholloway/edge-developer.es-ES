---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a6c7acf933192bfe96ac863620d3348eeca41ec7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880797"
---
# 0.9.515: ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

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

