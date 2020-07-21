---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 697a49bfe68f83085f6c961ee2cdd5ab21f3b59b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885824"
---
# 0.8.355: IWebView2ProcessFailedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento ProcessFailed.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_ProcessFailedKind](#get_processfailedkind) | El tipo de error de proceso que se ha producido.

## Miembros

#### get_ProcessFailedKind 

El tipo de error de proceso que se ha producido.

> [get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (WEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

