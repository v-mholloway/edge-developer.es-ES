---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9a98e2afa5b15452d7521183abebc019d51e3a3c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885460"
---
# 0.9.515: ICoreWebView2SourceChangedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

