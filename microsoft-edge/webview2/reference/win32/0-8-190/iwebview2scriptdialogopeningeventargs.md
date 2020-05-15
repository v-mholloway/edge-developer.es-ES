---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 867a8f3656b04a566708fc6fc1a24e80b967c1e2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655092"
---
# interfaz IWebView2ScriptDialogOpeningEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Argumentos de evento para el evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Identificador URI de la página que solicitó el cuadro de diálogo.
[get_Kind](#get_kind) | El cuadro de diálogo tipo de JavaScript.
[get_Message](#get_message) | Mensaje del cuadro de diálogo.
[Aceptar](#accept) | El anfitrión puede llamarlo para responder con aceptar para confirmar y pedir diálogos, o no llamar a este método para indicar que es cancelado.
[get_DefaultText](#get_defaulttext) | El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.
[get_ResultText](#get_resulttext) | El valor devuelto por la función prompt de JavaScript, si se llama a Accept.
[put_ResultText](#put_resulttext) | Establezca la propiedad ResultText.
[GetDeferral](#getdeferral) | Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .

## Miembros

#### get_Uri 

Identificador URI de la página que solicitó el cuadro de diálogo.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### get_Kind 

El cuadro de diálogo tipo de JavaScript.

> [get_Kind](#get_kind)de HRESULT público (WEBVIEW2_SCRIPT_DIALOG_KIND * tipo)

#### get_Message 

Mensaje del cuadro de diálogo.

> [get_Message](#get_message)de HRESULT público (mensaje LPWStr *)

Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt.

#### Aceptar 

El anfitrión puede llamarlo para responder con aceptar para confirmar y pedir diálogos, o no llamar a este método para indicar que es cancelado.

> [aceptación](#accept)pública de HRESULT ()

Desde JavaScript esto significa que la función CONFIRM devuelve true si se llama a Accept. Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.

#### get_DefaultText 

El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.

> [get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr * DefaultText)

Este es el valor predeterminado para usar en el resultado de la función pregunta.

#### get_ResultText 

El valor devuelto por la función prompt de JavaScript, si se llama a Accept.

> [get_ResultText](#get_resulttext)de HRESULT público (LPWStr * ResultText)

Esto se omite en los tipos de diálogo que no sean preguntar. Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.

#### put_ResultText 

Establezca la propiedad ResultText.

> [put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)

#### GetDeferral 

Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .

> [GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) * * aplazamiento)

Puedes usarlo para completar el evento en un momento posterior.

