---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: ebfb4aaf3f0c2b5531aaab3783572cf550bebf83
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012731"
---
# interfaz ICoreWebView2NavigationStartingEventArgs 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NavigationStarting.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Cancel](#get_cancel) | El anfitrión puede establecer esta marca para cancelar la navegación.
[get_IsRedirected](#get_isredirected) | True cuando se redirige la navegación.
[get_IsUserInitiated](#get_isuserinitiated) | True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.
[get_NavigationId](#get_navigationid) | IDENTIFICADOR de la navegación.
[get_RequestHeaders](#get_requestheaders) | Los encabezados de la solicitud HTTP para la navegación.
[get_Uri](#get_uri) | Identificador URI de la navegación solicitada.
[put_Cancel](#put_cancel) | Establezca la propiedad cancelar.

## Miembros

#### get_Cancel 

El anfitrión puede establecer esta marca para cancelar la navegación.

> [get_Cancel](#get_cancel)de HRESULT público (bool * CANCEL)

Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto. Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde. Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación. Cancelación de la navegación a: no se admite la navegación en blanco o en el marco a srcdoc. Dichos intentos serán ignorados.

#### get_IsRedirected 

True cuando se redirige la navegación.

> [get_IsRedirected](#get_isredirected)de HRESULT público (bool * IsRedirected)

#### get_IsUserInitiated 

True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.

> [get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool * IsUserInitiated)

#### get_NavigationId 

IDENTIFICADOR de la navegación.

> [get_NavigationId](#get_navigationid)(HRESULT) público (UINT64 * NavigationId)

#### get_RequestHeaders 

Los encabezados de la solicitud HTTP para la navegación.

> [get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * * RequestHeaders)

Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.

#### get_Uri 

Identificador URI de la navegación solicitada.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### put_Cancel 

Establezca la propiedad cancelar.

> [put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)

