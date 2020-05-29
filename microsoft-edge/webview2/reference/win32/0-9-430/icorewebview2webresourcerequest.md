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
ms.openlocfilehash: 201b9af4a5838c9537014864c31cd2121f9dfe76
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655103"
---
# interfaz ICoreWebView2WebResourceRequest 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

Una solicitud HTTP usada con el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Identificador URI de la solicitud.
[put_Uri](#put_uri) | Establezca la propiedad URI.
[get_Method](#get_method) | El método de solicitud HTTP.
[put_Method](#put_method) | Establezca la propiedad Method.
[get_Content](#get_content) | El cuerpo del mensaje de la solicitud HTTP como una secuencia.
[put_Content](#put_content) | Establezca la propiedad de contenido.
[get_Headers](#get_headers) | Los encabezados de solicitud HTTP mutable.

## Miembros

#### get_Uri 

Identificador URI de la solicitud.

> [get_Uri](#get_uri)de HRESULT público (URI LPWStr *)

#### put_Uri 

Establezca la propiedad URI.

> [put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)

#### get_Method 

El método de solicitud HTTP.

> [get_Method](#get_method)de HRESULT público (método LPWStr *)

#### put_Method 

Establezca la propiedad Method.

> [put_Method](#put_method)de HRESULT público (método LPCWSTR)

#### get_Content 

El cuerpo del mensaje de la solicitud HTTP como una secuencia.

> [get_Content](#get_content)(HRESULT) público (contenido de IStream * *)

Los datos de publicación estarán aquí. Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta. La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario. Null significa que no hay datos de contenido. Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)

#### put_Content 

Establezca la propiedad de contenido.

> [put_Content](#put_content)(HRESULT) público (contenido de IStream *)

#### get_Headers 

Los encabezados de solicitud HTTP mutable.

> [get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) * *)
