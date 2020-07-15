---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: ef1ca9707bba15fdaf8f37a306b56fdfc2c34588
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878984"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento AcceleratorKeyPressed.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Handled](#handled) | Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.
[KeyEventKind](#keyeventkind) | El tipo de evento de clave que causó el evento que se va a desencadenar.
[KeyEventLParam](#keyeventlparam) | El valor LPARAM que acompañaba al mensaje de ventana.
[PhysicalKeyStatus](#physicalkeystatus) | Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.
[VirtualKey](#virtualkey) | El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.

## Miembros

#### Handled 

Durante la invocación del controlador AcceleratorKeyPressedEvent, la vista en WebView está bloqueada esperando la decisión de si el host va a controlar el acelerador o no.

> bool público [Handled](#handled)

Si la propiedad Handled se establece en TRUE, esto evitará que la vista previa realice la acción predeterminada para esta tecla de aceleración. De lo contrario, la vista de WebView realizará la acción predeterminada para la tecla de aceleración.

#### KeyEventKind 

El tipo de evento de clave que causó el evento que se va a desencadenar.

> [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) pública [KeyEventKind](#keyeventkind)

#### KeyEventLParam 

El valor LPARAM que acompañaba al mensaje de ventana.

> public int [KeyEventLParam](#keyeventlparam)

Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.

#### PhysicalKeyStatus 

Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.

> [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) pública [PhysicalKeyStatus](#physicalkeystatus)

#### VirtualKey 

El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.

> uint pública [VirtualKey](#virtualkey)

Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A". Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).

