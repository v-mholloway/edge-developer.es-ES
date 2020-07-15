---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c13d0625669d6303c115c3d415d12278cfbe8320
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880503"
---
# 0.9.515: ICoreWebView2NavigationCompletedEventArgs 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

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

