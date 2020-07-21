---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886377"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento NavigationStarting.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Cancelar](#cancel) | El anfitrión puede establecer esta marca para cancelar la navegación.
[IsRedirected](#isredirected) | True cuando se redirige la navegación.
[IsUserInitiated](#isuserinitiated) | True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.
[NavigationId](#navigationid) | IDENTIFICADOR de la navegación.
[RequestHeaders](#requestheaders) | Los encabezados de la solicitud HTTP para la navegación.
[URI](#uri) | Identificador URI de la navegación solicitada.

## Miembros

#### Cancelar 

El anfitrión puede establecer esta marca para cancelar la navegación.

> [cancelación](#cancel) pública de bool

Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto. Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde. Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.

#### IsRedirected 

True cuando se redirige la navegación.

> Public bool [IsRedirected](#isredirected)

#### IsUserInitiated 

True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.

> Public bool [IsUserInitiated](#isuserinitiated)

#### NavigationId 

IDENTIFICADOR de la navegación.

> ulong [NavigationId](#navigationid)

#### RequestHeaders 

Los encabezados de la solicitud HTTP para la navegación.

> HttpRequestHeaders pública [RequestHeaders](#requestheaders)

Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.

#### URI 

Identificador URI de la navegación solicitada.

> [URI](#uri) de cadena pública

