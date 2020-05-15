---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655368"
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

