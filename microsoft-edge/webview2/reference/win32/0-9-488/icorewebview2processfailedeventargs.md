---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4183f3a1c60bd9e2bdcff5227426db1f07c313cf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697521"
---
# interfaz ICoreWebView2ProcessFailedEventArgs 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

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

> [get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

