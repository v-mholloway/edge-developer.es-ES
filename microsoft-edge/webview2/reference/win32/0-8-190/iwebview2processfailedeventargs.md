---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5ceb24d0d20f580e14e0d5af7ec09881c9ab0eb2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878249"
---
# 0.8.355: IWebView2ProcessFailedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

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

