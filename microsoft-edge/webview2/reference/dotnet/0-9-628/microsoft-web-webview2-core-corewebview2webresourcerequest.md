---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012627"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Una solicitud HTTP usada con el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Contenido](#content) | El cuerpo del mensaje de la solicitud HTTP como una secuencia.
[Encabezados](#headers) | Los encabezados de solicitud HTTP mutable.
[Método](#method) | El método de solicitud HTTP.
[URI](#uri) | Identificador URI de la solicitud.

## Miembros

#### Contenido 

El cuerpo del mensaje de la solicitud HTTP como una secuencia.

> [contenido](#content) de secuencia pública

Los datos de publicación estarán aquí. Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta. La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario. Null significa que no hay datos de contenido. Se aplican las semánticas de IStream (devuelva S_OK para leer las llamadas hasta que se agoten todos los datos).

#### Encabezados 

Los encabezados de solicitud HTTP mutable.

> [encabezados](#headers) de [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) pública

#### Método 

El método de solicitud HTTP.

> [método](#method) de cadena pública

#### URI 

Identificador URI de la solicitud.

> [URI](#uri) de cadena pública

