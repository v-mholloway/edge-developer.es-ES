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
ms.openlocfilehash: cc64e805b0d929d71340d5a012e7848860c35f5c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655327"
---
# interfaz ICoreWebView2NewWindowRequestedEventArgs 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NewWindowRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.
[get_NewWindow](#get_newwindow) | Obtiene la nueva ventana.
[get_Uri](#get_uri) | El URI de destino de la NewWindowRequest.
[GetDeferral](#getdeferral) | Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.
[put_Handled](#put_handled) | Establece si el NewWindowRequestedEvent es manejado por el hospedador.
[put_NewWindow](#put_newwindow) | Establece una vista previa como resultado de la NewWindowRequest.

El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).

## Miembros

#### get_Handled 

Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.

> [get_Handled](#get_handled)de HRESULT público (bool * Handled)

#### get_IsUserInitiated 

IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.

> [get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool * IsUserInitiated)

#### get_NewWindow 

Obtiene la nueva ventana.

> [get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](icorewebview2.md) * * NewWindow)

#### get_Uri 

El URI de destino de la NewWindowRequest.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### GetDeferral 

Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) * * aplazamiento)

Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de apertura de ventana más adelante. Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.

#### put_Handled 

Establece si el NewWindowRequestedEvent es manejado por el hospedador.

> [put_Handled](#put_handled)de HRESULT público (bool controlado)

Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto. Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana. El valor predeterminado es false.

#### put_NewWindow 

Establece una vista previa como resultado de la NewWindowRequest.

> [put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](icorewebview2.md) * NewWindow)

No se debe navegar por la WebView de destino. Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.

