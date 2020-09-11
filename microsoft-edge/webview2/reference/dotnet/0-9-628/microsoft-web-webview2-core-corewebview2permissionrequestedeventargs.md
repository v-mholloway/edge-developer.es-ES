---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012641"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento PermissionRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | True cuando se inició la solicitud de nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con target.
[PermissionKind](#permissionkind) | Tipo del permiso solicitado.
[Estado](#state) | El estado de una solicitud de permiso, es decir,
[URI](#uri) | El origen del contenido web que solicita el permiso.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.

## Miembros

#### IsUserInitiated 

True cuando se inició la solicitud de nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con target.

> Public bool [IsUserInitiated](#isuserinitiated)

El bloqueador de ventanas emergentes de Edge está deshabilitado para WebView, por lo que la aplicación puede usar esta marca para bloquear los mensajes emergentes no iniciados por el usuario.

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

