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
ms.openlocfilehash: 290d82666e5b9c5062132e1eb7515e39e2deb978
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699381"
---
# interfaz ICoreWebView2CapturePreviewCompletedHandler 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

La persona que llama implementa este método para recibir el resultado del método CapturePreview.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.

El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.

> invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)

