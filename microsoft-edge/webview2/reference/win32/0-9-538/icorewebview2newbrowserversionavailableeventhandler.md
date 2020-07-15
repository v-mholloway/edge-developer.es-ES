---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 82a5e73b8b928897e5c0af1610631c9e7d636337
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879747"
---
# interfaz ICoreWebView2NewBrowserVersionAvailableEventHandler 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

> invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) * webviewEnvironment, IUnknown * args)

