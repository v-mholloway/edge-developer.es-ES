---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878802"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento PermissionRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.
[PermissionKind](#permissionkind) | Tipo del permiso solicitado.
[Estado](#state) | El estado de una solicitud de permiso, es decir,
[URI](#uri) | El origen del contenido web que solicita el permiso.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.

## Miembros

#### IsUserInitiated 

True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.

> Public bool [IsUserInitiated](#isuserinitiated)

Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.

#### PermissionKind 

Tipo del permiso solicitado.

> CoreWebView2PermissionKind pública [PermissionKind](#permissionkind)

#### Estado 

El estado de una solicitud de permiso, es decir,

> [Estado](#state) de CoreWebView2PermissionState público

Si se concede la solicitud.

El valor predeterminado es CoreWebView2PermissionState. default.

#### URI 

El origen del contenido web que solicita el permiso.

> [URI](#uri) de cadena pública

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.

> Public CoreWebView2Deferral [GetDeferral](#getdeferral)()

El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.

