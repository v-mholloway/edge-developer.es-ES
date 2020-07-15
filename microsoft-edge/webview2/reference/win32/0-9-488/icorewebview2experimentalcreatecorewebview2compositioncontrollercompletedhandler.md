---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9aa9a18701621ca78b74b12340ef5132953fbd2b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880671"
---
# 0.9.515: ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2CompositionController.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

> invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * WebView)

