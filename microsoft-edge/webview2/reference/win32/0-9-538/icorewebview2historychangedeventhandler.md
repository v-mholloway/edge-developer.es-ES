---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879915"
---
# interfaz ICoreWebView2HistoryChangedEventHandler 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | No hay argumentos de evento y el parámetro args será null.

## Miembros

#### Invoke 

No hay argumentos de evento y el parámetro args será null.

> invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) * WebView, IUnknown * args)

