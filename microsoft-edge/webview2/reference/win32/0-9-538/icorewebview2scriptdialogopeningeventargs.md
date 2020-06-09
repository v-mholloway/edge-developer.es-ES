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
ms.openlocfilehash: 94a008af5a66109add56cec7fd0969d4e20d8ca8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699459"
---
# interfaz ICoreWebView2ScriptDialogOpeningEventArgs 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Argumentos de evento para el evento ScriptDialogOpening.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Aceptar](#accept) | El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.
[get_DefaultText](#get_defaulttext) | El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.
[get_Kind](#get_kind) | El cuadro de diálogo tipo de JavaScript.
[get_Message](#get_message) | Mensaje del cuadro de diálogo.
[get_ResultText](#get_resulttext) | El valor devuelto por la función prompt de JavaScript, si se llama a Accept.
[get_Uri](#get_uri) | Identificador URI de la página que solicitó el cuadro de diálogo.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .
[put_ResultText](#put_resulttext) | Establezca la propiedad ResultText.

## Miembros

#### Aceptar 

El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.

> [aceptación](#accept)pública de HRESULT ()

Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept. Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.

#### get_DefaultText 

El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.

> [get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr * DefaultText)

Este es el valor predeterminado para usar en el resultado de la función pregunta.

#### get_Kind 

El cuadro de diálogo tipo de JavaScript.

> [get_Kind](#get_kind)de HRESULT público (COREWEBVIEW2_SCRIPT_DIALOG_KIND * tipo)

Aceptar, confirmar, solicitar o beforeunload.

#### get_Message 

Mensaje del cuadro de diálogo.

> [get_Message](#get_message)de HRESULT público (mensaje LPWStr *)

Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.

#### get_ResultText 

El valor devuelto por la función prompt de JavaScript, si se llama a Accept.

> [get_ResultText](#get_resulttext)de HRESULT público (LPWStr * ResultText)

Esto se omite en los tipos de diálogo que no sean preguntar. Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.

#### get_Uri 

Identificador URI de la página que solicitó el cuadro de diálogo.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) * * aplazamiento)

Puedes usarlo para completar el evento en un momento posterior.

#### put_ResultText 

Establezca la propiedad ResultText.

> [put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)

