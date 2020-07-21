---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: c021cfa866e55bfdf30185eeaf6015db1b523271
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886569"
---
# interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

Controlador de finalización de PopulateResponseContent Async.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.

Se invoca cuando la secuencia de contenido de la respuesta de un evento WebResourceResponseReceieved está disponible.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.

> invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)

