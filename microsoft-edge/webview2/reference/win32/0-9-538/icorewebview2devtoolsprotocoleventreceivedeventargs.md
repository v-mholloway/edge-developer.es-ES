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
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699368"
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

