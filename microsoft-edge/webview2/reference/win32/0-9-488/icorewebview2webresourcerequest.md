---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4b76cf998f8e2fd8982f7e51f1d9167e3862ec02
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655125"
---
# interfaz ICoreWebView2WebResourceRequest 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

Una solicitud HTTP usada con el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Content](#get_content) | El cuerpo del mensaje de la solicitud HTTP como una secuencia.
[get_Headers](#get_headers) | Los encabezados de solicitud HTTP mutable.
[get_Method](#get_method) | El método de solicitud HTTP.
[get_Uri](#get_uri) | Identificador URI de la solicitud.
[put_Content](#put_content) | Establezca la propiedad de contenido.
[put_Method](#put_method) | Establezca la propiedad Method.
[put_Uri](#put_uri) | Establezca la propiedad URI.

## Miembros

#### get_Content 

El cuerpo del mensaje de la solicitud HTTP como una secuencia.

> [get_Content](#get_content)(HRESULT) público (contenido de IStream * *)

Los datos de publicación estarán aquí. Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta. La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario. Null significa que no hay datos de contenido. Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)

#### get_Headers 

Los encabezados de solicitud HTTP mutable.

> [get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * *)

#### get_Method 

El método de solicitud HTTP.

> [get_Method](#get_method)de HRESULT público (método LPWStr *)

#### get_Uri 

Identificador URI de la solicitud.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### put_Content 

Establezca la propiedad de contenido.

> [put_Content](#put_content)(HRESULT) público (contenido de IStream *)

#### put_Method 

Establezca la propiedad Method.

> [put_Method](#put_method)de HRESULT público (método LPCWSTR)

#### put_Uri 

Establezca la propiedad URI.

> [put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)

