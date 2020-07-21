---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885055"
---
# 0.8.355: IWebView2AcceleratorKeyPressedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento AcceleratorKeyPressed.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_KeyEventType](#get_keyeventtype) | El tipo de evento de clave que causó el evento que se va a desencadenar.
[get_VirtualKey](#get_virtualkey) | El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.
[get_KeyEventLParam](#get_keyeventlparam) | El valor LPARAM que acompañaba al mensaje de ventana.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.
[Indicador](#handle) | Al llamar, se permitirá que continúe el proceso del explorador.

## Miembros

#### get_KeyEventType 

El tipo de evento de clave que causó el evento que se va a desencadenar.

> [get_KeyEventType](#get_keyeventtype)de HRESULT público (WEBVIEW2_KEY_EVENT_TYPE * KeyEventType)

Esta es una de WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN o WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.

#### get_VirtualKey 

El código de tecla virtual Win32 de la tecla que se ha presionado o soltado.

> [get_VirtualKey](#get_virtualkey)pública HRESULT (uint * VirtualKey)

Será una de las constantes de la clave virtual de Win32, como VK_RETURN o un valor ASCII (en mayúsculas), como "A". Puede comprobar si las teclas Ctrl o Alt se presionan llamando a GetKeyState (VK_CONTROL) o GetKeyState (VK_MENU).

#### get_KeyEventLParam 

El valor LPARAM que acompañaba al mensaje de ventana.

> [get_KeyEventLParam](#get_keyeventlparam)de HRESULT público (int * lParam)

Consulte la documentación de los mensajes de WM_KEYDOWN y WM_KEYUP.

#### get_PhysicalKeyStatus 

Estructura que representa la información que se pasa en el LPARAM del mensaje de la ventana.

> [get_PhysicalKeyStatus](#get_physicalkeystatus)de HRESULT público (WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### Indicador 

Al llamar, se permitirá que continúe el proceso del explorador.

> [identificador](#handle)de HRESULT público (bool Handled)

Si se pasa TRUE, el explorador no podrá realizar la acción predeterminada para esta tecla de aceleración. Si el controlador de eventos vuelve sin llamar al [controlador ()](#handle), es equivalente a llamar a handle (false). Llamar a [HANDLE ()](#handle) después de que ya se ha llamado o el controlador de eventos se ha devuelto no hará nada.

