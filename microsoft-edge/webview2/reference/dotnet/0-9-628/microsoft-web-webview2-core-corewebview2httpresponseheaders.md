---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012670"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Encabezados de respuesta HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Anexa la línea de encabezado con el nombre y el valor.
[Contains](#contains) | Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.
[GetHeader](#getheader) | Obtiene el primer valor de encabezado de la colección que coincide con el nombre.
[GetHeaders](#getheaders) | Obtiene los valores de encabezado que coinciden con el nombre.
[GetIterator](#getiterator) | Obtiene un iterador sobre la colección de encabezados de respuesta completos.

Se usa para construir un WebResourceResponse para el evento WebResourceRequested.

## Miembros

#### AppendHeader 

Anexa la línea de encabezado con el nombre y el valor.

> public void [AppendHeader](#appendheader)(string name, valor de cadena)

#### Contains 

Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.

> Public bool [contiene](#contains)(cadena nombre)

#### GetHeader 

Obtiene el primer valor de encabezado de la colección que coincide con el nombre.

> cadena pública [GetHeader](#getheader)(cadena nombre)

#### GetHeaders 

Obtiene los valores de encabezado que coinciden con el nombre.

> Public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(cadena nombre)

#### GetIterator 

Obtiene un iterador sobre la colección de encabezados de respuesta completos.

> Public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()

