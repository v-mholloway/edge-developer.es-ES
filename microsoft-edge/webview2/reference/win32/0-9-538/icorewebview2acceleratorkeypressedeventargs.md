---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: bf6ed3234a575637da7104c4d033ce82b18d039c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880118"
---
# interfaz ICoreWebView2AcceleratorKeyPressedEventArgs 

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento AcceleratorKeyPressed.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.
[get_KeyEventKind](#get_keyeventkind) | El tipo de evento de clave que causó el evento que se va a desencadenar.
[get_KeyEventLParam](#get_keyeventlparam) | El valor LPARAM que acompañaba al mensaje de ventana.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.
[get_VirtualKey](#get_virtualkey) | El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.
[put_Handled](#put_handled) | Establece la propiedad Handled.

## Miembros

#### get_Handled 

Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.

> [get_Handled](#get_handled)de HRESULT público (bool * Handled)

Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración. De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.

#### get_KeyEventKind 

El tipo de evento de clave que causó el evento que se va a desencadenar.

> [get_KeyEventKind](#get_keyeventkind)de HRESULT público (COREWEBVIEW2_KEY_EVENT_KIND * KeyEventKind)

#### get_KeyEventLParam 

El valor LPARAM que acompañaba al mensaje de ventana.

> [get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int * lParam)

Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.

#### get_PhysicalKeyStatus 

Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.

> [get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (COREWEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### get_VirtualKey 

El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.

> [get_VirtualKey](#get_virtualkey)pública HRESULT (uint * VirtualKey)

Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A". Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).

#### put_Handled 

Establece la propiedad Handled.

> [put_Handled](#put_handled)de HRESULT público (bool controlado)

