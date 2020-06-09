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
ms.openlocfilehash: d3b3f4e78ef37ad2101a3a8f817279e999cea3e3
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697619"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Argumentos de evento para el evento NavigationCompleted.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[IsSuccess](#issuccess) | Es verdadero cuando la navegación es correcta.
[NavigationId](#navigationid) | IDENTIFICADOR de la navegación.
[WebErrorStatus](#weberrorstatus) | El código de error si se produjo un error en la navegación.

## Miembros

#### IsSuccess 

Es verdadero cuando la navegación es correcta.

> Public bool [IsSuccess](#issuccess)

Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.

#### NavigationId 

IDENTIFICADOR de la navegación.

> ulong [NavigationId](#navigationid)

#### WebErrorStatus 

El código de error si se produjo un error en la navegación.

> CoreWebView2WebErrorStatus pública [WebErrorStatus](#weberrorstatus)

