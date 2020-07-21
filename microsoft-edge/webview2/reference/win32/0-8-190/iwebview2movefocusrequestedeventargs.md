---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5d8d447bced6bbbb51ae33220e74ebcf47f11ce5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885930"
---
# 0.8.355: IWebView2MoveFocusRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento MoveFocusRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Reason](#get_reason) | El motivo de la vista en WebView para activar el evento solicitado MoveFocus.
[get_Handled](#get_handled) | Indicar si la aplicación ha controlado el evento.
[put_Handled](#put_handled) | Establecer la propiedad Handled.

## Miembros

#### get_Reason 

El motivo de la vista en WebView para activar el evento solicitado MoveFocus.

> [get_Reason](#get_reason)de HRESULT público (valor WEBVIEW2_MOVE_FOCUS_REASON *)

#### get_Handled 

Indicar si la aplicación ha controlado el evento.

> [get_Handled](#get_handled)de HRESULT público (bool * Value)

Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE. Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada. La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana. Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.

#### put_Handled 

Establecer la propiedad Handled.

> [put_Handled](#put_handled)de HRESULT público (valor bool)

