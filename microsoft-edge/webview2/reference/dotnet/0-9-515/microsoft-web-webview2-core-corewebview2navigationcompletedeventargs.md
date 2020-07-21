---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885082"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

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

