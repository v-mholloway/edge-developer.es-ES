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
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699382"
---
# interfaz ICoreWebView2ContentLoadingEventArgs 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Argumentos de evento para el evento ContentLoading.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | True si el contenido cargado es una página de error.
[get_NavigationId](#get_navigationid) | IDENTIFICADOR de la navegación.

## Miembros

#### get_IsErrorPage 

True si el contenido cargado es una página de error.

> [get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool * IsErrorPage)

#### get_NavigationId 

IDENTIFICADOR de la navegación.

> [get_NavigationId](#get_navigationid)de HRESULT público (UINT64 * navigation_id)

