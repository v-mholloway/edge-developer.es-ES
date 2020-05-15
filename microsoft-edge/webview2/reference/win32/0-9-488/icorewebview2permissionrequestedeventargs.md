---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 018d986ac0941406a62786bfb6e3666cf33dc09f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655284"
---
# interfaz ICoreWebView2PermissionRequestedEventArgs 

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

