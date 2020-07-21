---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: bd9d10d5f281b2e8f0a5d0687235560c44edc170
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886440"
---
# 0.9.430: ICoreWebView2NavigationStartingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NavigationStarting.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Identificador URI de la navegación solicitada.
[get_IsUserInitiated](#get_isuserinitiated) | True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.
[get_IsRedirected](#get_isredirected) | True cuando se redirige la navegación.
[get_RequestHeaders](#get_requestheaders) | Los encabezados de la solicitud HTTP para la navegación.
[get_Cancel](#get_cancel) | El anfitrión puede establecer esta marca para cancelar la navegación.
[put_Cancel](#put_cancel) | Establezca la propiedad cancelar.
[get_NavigationId](#get_navigationid) | IDENTIFICADOR de la navegación.

## Miembros

#### get_Uri 

Identificador URI de la navegación solicitada.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### get_IsUserInitiated 

True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.

> [get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool * IsUserInitiated)

#### get_IsRedirected 

True cuando se redirige la navegación.

> [get_IsRedirected](#get_isredirected)de HRESULT público (bool * IsRedirected)

#### get_RequestHeaders 

Los encabezados de la solicitud HTTP para la navegación.

> [get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) * * RequestHeaders)

Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.

#### get_Cancel 

El anfitrión puede establecer esta marca para cancelar la navegación.

> [get_Cancel](#get_cancel)de HRESULT público (bool * CANCEL)

Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto. Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde. Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.

#### put_Cancel 

Establezca la propiedad cancelar.

> [put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)

#### get_NavigationId 

IDENTIFICADOR de la navegación.

> [get_NavigationId](#get_navigationid)de HRESULT público (UINT64 * navigation_id)

