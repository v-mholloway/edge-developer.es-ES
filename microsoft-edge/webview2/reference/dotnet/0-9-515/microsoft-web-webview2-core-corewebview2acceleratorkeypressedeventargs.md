---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 10694292c7943f87753ae87f6129655b27f425f3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885145"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

