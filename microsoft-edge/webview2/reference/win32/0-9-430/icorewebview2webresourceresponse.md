---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 6d28a5e0b08406cdf83b7e0a60428463e9647d45
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655267"
---
# interfaz ICoreWebView2WebResourceResponse 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

Una respuesta HTTP usada con el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Contenido de la respuesta HTTP como una secuencia.
[put_Content](#put_content) | Establezca la propiedad de contenido.
[get_Headers](#get_headers) | Encabezados de respuesta HTTP invalidados.
[get_StatusCode](#get_statuscode) | El código de estado de respuesta HTTP.
[put_StatusCode](#put_statuscode) | Establezca la propiedad StatusCode.
[get_ReasonPhrase](#get_reasonphrase) | La frase de razón de respuesta HTTP.
[put_ReasonPhrase](#put_reasonphrase) | Establezca la propiedad ReasonPhrase.

## Miembros

#### get_Content 

Contenido de la respuesta HTTP como una secuencia.

> [get_Content](#get_content)(HRESULT) público (contenido de IStream * *)

La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta. La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario. Null significa que no hay datos de contenido. Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)

#### put_Content 

Establezca la propiedad de contenido.

> [put_Content](#put_content)(HRESULT) público (contenido de IStream *)

#### get_Headers 

Encabezados de respuesta HTTP invalidados.

> [get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) * *)

#### get_StatusCode 

El código de estado de respuesta HTTP.

> [get_StatusCode](#get_statuscode)de HRESULT público (int * StatusCode)

#### put_StatusCode 

Establezca la propiedad StatusCode.

> [put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)

#### get_ReasonPhrase 

La frase de razón de respuesta HTTP.

> [get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr * ReasonPhrase)

#### put_ReasonPhrase 

Establezca la propiedad ReasonPhrase.

> [put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)

