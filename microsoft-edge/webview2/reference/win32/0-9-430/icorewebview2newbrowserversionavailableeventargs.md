---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884865"
---
# 0.9.430: ICoreWebView2NewBrowserVersionAvailableEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

