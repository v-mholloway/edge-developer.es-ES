---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4ae58375f0158a3876b284e16a579149dc6db9a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699432"
---
# interfaz ICoreWebView2SourceChangedEventArgs 

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

