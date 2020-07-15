---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: aaaad1f622887ed1c941a9cf12ee4c753b352286
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878886"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

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

