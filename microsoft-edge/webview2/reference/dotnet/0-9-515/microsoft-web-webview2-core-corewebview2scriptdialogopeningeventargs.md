---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b7071a312ce1fa3ca006a6805a1f712a51d0dab0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879117"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs (clase) 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

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

