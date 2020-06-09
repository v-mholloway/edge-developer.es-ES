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
ms.openlocfilehash: 58ca180e73c3e4644e466e13c4059f32102f1896
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699315"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

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

