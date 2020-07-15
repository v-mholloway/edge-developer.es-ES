---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: cbff39e9393026f51471bdfb3189600e2d7bf109
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879698"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento ScriptDialogOpening.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[DefaultText](#defaulttext) | El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.
[Tipos](#kind) | El cuadro de diálogo tipo de JavaScript.
[Mensaje](#message) | Mensaje del cuadro de diálogo.
[ResultText](#resulttext) | El valor devuelto por la función prompt de JavaScript, si se llama a Accept.
[URI](#uri) | Identificador URI de la página que solicitó el cuadro de diálogo.
[Aceptar](#accept) | El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.

## Miembros

#### DefaultText 

El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.

> cadena pública [DefaultText](#defaulttext)

Este es el valor predeterminado para usar en el resultado de la función pregunta.

#### Tipos 

El cuadro de diálogo tipo de JavaScript.

> [tipo](#kind) de CoreWebView2ScriptDialogKind público

Aceptar, confirmar, solicitar o beforeunload.

#### Mensaje 

Mensaje del cuadro de diálogo.

> [mensaje](#message) de cadena pública

Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.

#### ResultText 

El valor devuelto por la función prompt de JavaScript, si se llama a Accept.

> cadena pública [ResultText](#resulttext)

Esto se omite en los tipos de diálogo que no sean preguntar. Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.

#### URI 

Identificador URI de la página que solicitó el cuadro de diálogo.

> [URI](#uri) de cadena pública

#### Aceptar 

El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.

> [Accept](#accept)public void ()

Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept. Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.

> Public CoreWebView2Deferral [GetDeferral](#getdeferral)()

Puedes usarlo para completar el evento en un momento posterior.

