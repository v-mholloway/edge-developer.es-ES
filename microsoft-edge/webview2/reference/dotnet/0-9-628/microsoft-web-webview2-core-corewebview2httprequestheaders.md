---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012606"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Encabezados de solicitud HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Contains](#contains) | Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.
[GetHeader](#getheader) | Obtiene el valor de encabezado que coincide con el nombre.
[GetHeaders](#getheaders) | Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.
[GetIterator](#getiterator) | Obtiene un iterador en la colección de encabezados de solicitud.
[RemoveHeader](#removeheader) | Quita el encabezado que coincide con el nombre.
[SetHeader](#setheader) | Agrega o actualiza el encabezado que coincide con el nombre.

Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting. Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.

## Miembros

#### Contains 

Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.

> Public bool [contiene](#contains)(cadena nombre)

#### GetHeader 

Obtiene el valor de encabezado que coincide con el nombre.

> cadena pública [GetHeader](#getheader)(cadena nombre)

#### GetHeaders 

Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.

> Public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(cadena nombre)

#### GetIterator 

Obtiene un iterador en la colección de encabezados de solicitud.

> Public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()

#### RemoveHeader 

Quita el encabezado que coincide con el nombre.

> public void [RemoveHeader](#removeheader)(string name)

#### SetHeader 

Agrega o actualiza el encabezado que coincide con el nombre.

> public void [SetHeader](#setheader)(string name, valor de cadena)

