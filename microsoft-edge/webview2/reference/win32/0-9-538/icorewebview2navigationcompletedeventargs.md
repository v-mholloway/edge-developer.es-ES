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
ms.openlocfilehash: 11d7e5ffef11a445c55cd4a9d70fcbbb8087c024
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699410"
---
# interfaz ICoreWebView2NavigationCompletedEventArgs 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NavigationCompleted.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | Es verdadero cuando la navegación es correcta.
[get_NavigationId](#get_navigationid) | IDENTIFICADOR de la navegación.
[get_WebErrorStatus](#get_weberrorstatus) | El código de error si se produjo un error en la navegación.

## Miembros

#### get_IsSuccess 

Es verdadero cuando la navegación es correcta.

> [get_IsSuccess](#get_issuccess)de HRESULT público (bool * IsSuccess)

Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.

#### get_NavigationId 

IDENTIFICADOR de la navegación.

> [get_NavigationId](#get_navigationid)de HRESULT público (UINT64 * navigation_id)

#### get_WebErrorStatus 

El código de error si se produjo un error en la navegación.

> [get_WebErrorStatus](#get_weberrorstatus)de HRESULT público (COREWEBVIEW2_WEB_ERROR_STATUS * COREWEBVIEW2_WEB_ERROR_STATUS)

