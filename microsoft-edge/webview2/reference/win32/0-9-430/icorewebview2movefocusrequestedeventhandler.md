---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8a826b5693bce0970c4360fb40c7e13ccacc1f01
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880979"
---
# 0.9.430: ICoreWebView2MoveFocusRequestedEventHandler 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

La persona que llama implementa este método para recibir el evento MoveFocusRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

> invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) * Sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) * args)

