---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877857"
---
# 0.9.430: ICoreWebView2NewBrowserVersionAvailableEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NewBrowserVersionAvailable.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.

## Miembros

#### get_NewVersion 

Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.

> [get_NewVersion](#get_newversion)de HRESULT público (LPWStr * NewVersion)

