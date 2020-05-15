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
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655419"
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

