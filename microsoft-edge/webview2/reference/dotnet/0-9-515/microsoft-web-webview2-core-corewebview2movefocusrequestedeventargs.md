---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3c88108f0e1df89c62c8713ff37f35d0c759cf6c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655448"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

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

