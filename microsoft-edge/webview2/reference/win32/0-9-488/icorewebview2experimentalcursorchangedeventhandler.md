---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 6fbcc82409791bc3d2da3bb2f7985732cb344a97
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880629"
---
# 0.9.515: ICoreWebView2ExperimentalCursorChangedEventHandler 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir eventos CursorChanged.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

Use la propiedad cursor para obtener el nuevo cursor.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

> invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * Sender, IUnknown * args)

No hay argumentos de evento y el parámetro args será null.

