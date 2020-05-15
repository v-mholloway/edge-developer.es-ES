---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 529f4a444b3ad6d0d5831da6015831b077102354
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655106"
---
# interfaz ICoreWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento PermissionRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | El origen del contenido web que solicita el permiso.
[get_PermissionKind](#get_permissionkind) | Tipo del permiso solicitado.
[get_IsUserInitiated](#get_isuserinitiated) | True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.
[get_State](#get_state) | El estado de una solicitud de permiso, es decir,
[put_State](#put_state) | Establezca la propiedad State.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .

## Miembros

#### get_Uri 

El origen del contenido web que solicita el permiso.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### get_PermissionKind 

Tipo del permiso solicitado.

> [get_PermissionKind](#get_permissionkind)de HRESULT público (valor CORE_WEBVIEW2_PERMISSION_KIND *)

#### get_IsUserInitiated 

True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.

> [get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool * IsUserInitiated)

Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.

#### get_State 

El estado de una solicitud de permiso, es decir,

> [get_State](#get_state)de HRESULT público (valor CORE_WEBVIEW2_PERMISSION_STATE *)

Si se concede la solicitud. El valor predeterminado es CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Establezca la propiedad State.

> [put_State](#put_state)de HRESULT público (valor de CORE_WEBVIEW2_PERMISSION_STATE)

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * aplazamiento)

El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.

