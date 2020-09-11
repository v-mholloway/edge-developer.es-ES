---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012623"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Una respuesta HTTP usada con el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Contenido](#content) | Contenido de la respuesta HTTP como una secuencia.
[Encabezados](#headers) | Encabezados de respuesta HTTP invalidados.
[ReasonPhrase](#reasonphrase) | La frase de razón de respuesta HTTP.
[StatusCode](#statuscode) | El código de estado de respuesta HTTP.

## Miembros

#### Contenido 

Contenido de la respuesta HTTP como una secuencia.

> [contenido](#content) de secuencia pública

La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta. La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario. Null significa que no hay datos de contenido. Se aplican las semánticas de IStream (devuelva S_OK para leer las llamadas hasta que se agoten todos los datos).

#### Encabezados 

Encabezados de respuesta HTTP invalidados.

> [encabezados](#headers) de [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) pública

#### ReasonPhrase 

La frase de razón de respuesta HTTP.

> cadena pública [ReasonPhrase](#reasonphrase)

#### StatusCode 

El código de estado de respuesta HTTP.

> public int [StatusCode](#statuscode)

