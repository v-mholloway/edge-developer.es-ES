---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884592"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

