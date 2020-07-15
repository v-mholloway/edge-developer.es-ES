---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878774"
---
# Estructura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

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

