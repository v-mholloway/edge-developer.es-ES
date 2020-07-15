---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 22fc8ec74c8da0a0ff072cacf91a792b9246900f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879803"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs (clase) 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

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

