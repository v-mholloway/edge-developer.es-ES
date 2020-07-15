---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 236dacec6db871fbc07c9f0067f3c8fa4fd6815d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880419"
---
# 0.9.515: ICoreWebView2PermissionRequestedEventHandler 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir el evento PermissionRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

> invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) * Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) * args)

