---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1d3cae59c0906a94414ff135ef8d84fac7cc89b4
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885075"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento MoveFocusRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Handled](#handled) | Indicar si la aplicación ha controlado el evento.
[Razón](#reason) | El motivo de la vista en WebView para activar el evento solicitado MoveFocus.

## Miembros

#### Handled 

Indicar si la aplicación ha controlado el evento.

> bool público [Handled](#handled)

Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE. Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada. La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana. Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.

#### Razón 

El motivo de la vista en WebView para activar el evento solicitado MoveFocus.

> [razón](#reason) de CoreWebView2MoveFocusReason pública

