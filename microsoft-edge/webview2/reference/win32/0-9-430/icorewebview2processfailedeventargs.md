---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: f4238f0d75f39727260296703e84740ca77b30d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877740"
---
# 0.9.430: ICoreWebView2ProcessFailedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2ProcessFailedEventArgs
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

> [get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (CORE_WEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

