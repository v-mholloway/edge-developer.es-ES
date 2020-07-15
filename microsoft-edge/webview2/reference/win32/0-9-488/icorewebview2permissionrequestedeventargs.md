---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 88f5008dbc9a4ebfccfe96299899a2474ecc6d95
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880412"
---
# 0.9.515: ICoreWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento PermissionRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsUserInitiated](#get_isuserinitiated) | True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.
[get_PermissionKind](#get_permissionkind) | Tipo del permiso solicitado.
[get_State](#get_state) | El estado de una solicitud de permiso, es decir,
[get_Uri](#get_uri) | El origen del contenido web que solicita el permiso.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .
[put_State](#put_state) | Establezca la propiedad State.

## Miembros

#### get_IsUserInitiated 

True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.

> [get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool * IsUserInitiated)

Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.

#### get_PermissionKind 

Tipo del permiso solicitado.

> [get_PermissionKind](#get_permissionkind)de HRESULT público (valor COREWEBVIEW2_PERMISSION_KIND *)

#### get_State 

El estado de una solicitud de permiso, es decir,

> [get_State](#get_state)de HRESULT público (valor COREWEBVIEW2_PERMISSION_STATE *)

Si se concede la solicitud. El valor predeterminado es COREWEBVIEW2_PERMISSION_STATE_DEFAULT.

#### get_Uri 

El origen del contenido web que solicita el permiso.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) * * aplazamiento)

El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.

#### put_State 

Establezca la propiedad State.

> [put_State](#put_state)de HRESULT público (valor de COREWEBVIEW2_PERMISSION_STATE)

