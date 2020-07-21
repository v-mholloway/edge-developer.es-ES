---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e2a9486011d5ef3ef480271ed32a7c8b586cf9bd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885831"
---
# 0.8.355: IWebView2PermissionRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento PermissionRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | El origen del contenido web que solicita el permiso.
[get_PermissionType](#get_permissiontype) | Tipo del permiso solicitado.
[get_IsUserInitiated](#get_isuserinitiated) | True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.
[get_State](#get_state) | El estado de una solicitud de permiso, es decir,
[put_State](#put_state) | Establezca la propiedad State.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .

## Miembros

#### get_Uri 

El origen del contenido web que solicita el permiso.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### get_PermissionType 

Tipo del permiso solicitado.

> [get_PermissionType](#get_permissiontype)de HRESULT público (valor WEBVIEW2_PERMISSION_TYPE *)

#### get_IsUserInitiated 

True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.

> [get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool * IsUserInitiated)

Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.

#### get_State 

El estado de una solicitud de permiso, es decir,

> [get_State](#get_state)de HRESULT público (valor WEBVIEW2_PERMISSION_STATE *)

Si se concede la solicitud. El valor predeterminado es WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Establezca la propiedad State.

> [put_State](#put_state)de HRESULT público (valor de WEBVIEW2_PERMISSION_STATE)

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .

> [GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) * * aplazamiento)

El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.

