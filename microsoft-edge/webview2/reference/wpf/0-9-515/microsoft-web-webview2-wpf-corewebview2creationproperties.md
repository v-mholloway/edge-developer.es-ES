---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 04c80d3319c74d3461666b6f35fadd0481b45207
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885537"
---
# Clase Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Espacio de nombres: Microsoft. Web. WebView2. WPF \
Ensamblado: Microsoft.Web.WebView2.Wpf.dll

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

Esta clase es un paquete de los parámetros más comunes que se usan para crear un CoreWebView2Environment.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[BrowserExecutableFolder](#browserexecutablefolder) | Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.
[Idioma](#language) | Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.
[UserDataFolder](#userdatafolder) | Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.
[CoreWebView2CreationProperties](#corewebview2creationproperties) | Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.

Su propósito principal es establecer [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) para personalizar el entorno usado por una [WebView2](microsoft-web-webview2-wpf-webview2.md) durante la inicialización implícita. También es una buena utilidad de integración con WPF que permite que los parámetros de entorno usados comúnmente sean propiedades de dependencia y que se creen y usen en el marcado.

Esta clase no está pensada para contener todas las opciones de personalización del entorno. Si necesitas controlar completamente el entorno usado por un control WebView2, tendrás que inicializar el control de forma explícita creando tu propio entorno con CoreWebView2Environment. CreateAsync y pasándolo a [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de establecer la propiedad [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) en cualquier cosa. Consulta la documentación de la clase [WebView2](microsoft-web-webview2-wpf-webview2.md) para obtener información general sobre la inicialización.

## Miembros

#### BrowserExecutableFolder 

Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.

> cadena pública [BrowserExecutableFolder](#browserexecutablefolder)

#### Idioma 

Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.

> [lenguaje](#language) de cadenas pública

#### UserDataFolder 

Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.

> cadena pública [UserDataFolder](#userdatafolder)

#### CoreWebView2CreationProperties 

Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.

> [CoreWebView2CreationProperties](#corewebview2creationproperties)pública ()

