---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: d2c3b3ee179dec217418241031142549d170e440
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655065"
---
# Clase Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Espacio de nombres: Microsoft. Web. WebView2. WPF \
Ensamblado: Microsoft. Web. WebView2. WPF. dll

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

