---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 39d52b1231e767739b63b3759cdd08e4c9b26be3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879992"
---
# interfaz ICoreWebView2ExperimentalNewWindowRequestedEventArgs 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NewWindowRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_WindowFeatures](#get_windowfeatures) | Características de la ventana especificadas por la llamada Window. Open.

El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).

## Miembros

#### get_WindowFeatures 

Características de la ventana especificadas por la llamada Window. Open.

> [get_WindowFeatures](#get_windowfeatures)(HRESULT) público ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) * * WindowFeatures)

Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.

