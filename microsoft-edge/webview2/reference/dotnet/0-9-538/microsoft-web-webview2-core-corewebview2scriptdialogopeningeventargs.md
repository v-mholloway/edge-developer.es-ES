---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 93e662088ae1561b5dcb33390f46a41c19ca0aaf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699311"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

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

