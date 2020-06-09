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
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699314"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Argumentos de evento para el evento NewWindowRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Handled](#handled) | Si el NewWindowRequestedEvent es manejado por el hospedador.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.
[NewWindow](#newwindow) | Obtiene la nueva ventana.
[URI](#uri) | El URI de destino de la NewWindowRequest.
[WindowFeatures](#windowfeatures) | Características de la ventana especificadas por la llamada Window. Open.
[GetDeferral](#getdeferral) | Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.

El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).

## Miembros

#### Handled 

Si el NewWindowRequestedEvent es manejado por el hospedador.

> bool público [Handled](#handled)

Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto. Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana. El valor predeterminado es false.

#### IsUserInitiated 

IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.

> Public bool [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Obtiene la nueva ventana.

> CoreWebView2 pública [NewWindow](#newwindow)

#### URI 

El URI de destino de la NewWindowRequest.

> [URI](#uri) de cadena pública

No se debe navegar por la WebView de destino. Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.

#### WindowFeatures 

> [!NOTE]
> Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).

Características de la ventana especificadas por la llamada Window. Open.

> CoreWebView2WindowFeatures pública [WindowFeatures](#windowfeatures)

Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.

#### GetDeferral 

Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.

> Public CoreWebView2Deferral [GetDeferral](#getdeferral)()

Puedes usar el objeto CoreWebView2Deferral para completar la solicitud de apertura de ventana más adelante. Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.

