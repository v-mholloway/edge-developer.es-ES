---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: cd692de6aaa3dc694fb2fe149411e5fd64de1ee2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878872"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

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

