---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 5cc3ca23dcababc35a73b44a81c54439d0dbe1a3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884312"
---
# 0.9.430: ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateCoreWebView2Environment.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

> invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) * created_environment)

