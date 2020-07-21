---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e17e12759bef051a33e99999f0e938da5bd16939
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883787"
---
# 0.9.515: ICoreWebView2WebResourceResponse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

Una respuesta HTTP usada con el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Contenido de la respuesta HTTP como una secuencia.
[get_Headers](#get_headers) | Encabezados de respuesta HTTP invalidados.
[get_ReasonPhrase](#get_reasonphrase) | La frase de razón de respuesta HTTP.
[get_StatusCode](#get_statuscode) | El código de estado de respuesta HTTP.
[put_Content](#put_content) | Establezca la propiedad de contenido.
[put_ReasonPhrase](#put_reasonphrase) | Establezca la propiedad ReasonPhrase.
[put_StatusCode](#put_statuscode) | Establezca la propiedad StatusCode.

## Miembros

#### get_Content 

Contenido de la respuesta HTTP como una secuencia.

> [get_Content](#get_content)(HRESULT) público (contenido de IStream * *)

La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta. La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario. Null significa que no hay datos de contenido. Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)

#### get_Headers 

Encabezados de respuesta HTTP invalidados.

> [get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) * *)

#### get_ReasonPhrase 

La frase de razón de respuesta HTTP.

> [get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr * ReasonPhrase)

#### get_StatusCode 

El código de estado de respuesta HTTP.

> [get_StatusCode](#get_statuscode)de HRESULT público (int * StatusCode)

#### put_Content 

Establezca la propiedad de contenido.

> [put_Content](#put_content)(HRESULT) público (contenido de IStream *)

#### put_ReasonPhrase 

Establezca la propiedad ReasonPhrase.

> [put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)

#### put_StatusCode 

Establezca la propiedad StatusCode.

> [put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)

