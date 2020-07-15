---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 898b76b1865cbda1909fa710707019582439db93
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879999"
---
# interfaz ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.

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

