---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 2e3afec26b0e09a80182118f74b6f50733b0c71a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655263"
---
# interfaz IWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

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
