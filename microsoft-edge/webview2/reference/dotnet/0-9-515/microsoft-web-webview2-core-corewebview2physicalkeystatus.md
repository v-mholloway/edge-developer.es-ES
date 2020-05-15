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
ms.openlocfilehash: 28ed6db251095e2baf6474950c6839dc4a5a8633
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655508"
---
# Estructura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[IsExtendedKey](#isextendedkey) | Indica si la tecla es una tecla extendida.
[IsKeyReleased](#iskeyreleased) | Estado de transición.
[IsMenuKeyDown](#ismenukeydown) | El código de contexto.
[RepeatCount](#repeatcount) | El número de repeticiones del mensaje actual.
[ScanCode](#scancode) | El código de análisis.
[WasKeyDown](#waskeydown) | El estado de clave anterior.

Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .

## Miembros

#### IsExtendedKey 

Indica si la tecla es una tecla extendida.

> public int [IsExtendedKey](#isextendedkey)

#### IsKeyReleased 

Estado de transición.

> public int [IsKeyReleased](#iskeyreleased)

#### IsMenuKeyDown 

El código de contexto.

> public int [IsMenuKeyDown](#ismenukeydown)

#### RepeatCount 

El número de repeticiones del mensaje actual.

> Public uint [RepeatCount](#repeatcount)

#### ScanCode 

El código de análisis.

> uint pública [Scancode](#scancode)

#### WasKeyDown 

El estado de clave anterior.

> public int [WasKeyDown](#waskeydown)

