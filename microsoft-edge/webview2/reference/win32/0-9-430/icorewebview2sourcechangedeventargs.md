---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8a9f1b1e44353796c6d3b57d3f4c6f3d4997aad5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880202"
---
# 0.9.430: ICoreWebView2SourceChangedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento SourceChanged.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | True si la página a la que se navega es un documento nuevo.

## Miembros

#### get_IsNewDocument 

True si la página a la que se navega es un documento nuevo.

> [get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool * IsNewDocument)

