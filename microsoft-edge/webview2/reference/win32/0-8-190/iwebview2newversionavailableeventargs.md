---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885873"
---
# 0.8.355: IWebView2NewVersionAvailableEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NewVersionAvailable.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.

## Miembros

#### get_NewVersion 

Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.

> [get_NewVersion](#get_newversion)de HRESULT público (LPWStr * NewVersion)

