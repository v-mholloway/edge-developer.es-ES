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
ms.openlocfilehash: be8f475d4c1a886a92b46144f2bffde2d49dc9d4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655387"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Esto representa el entorno de WebView2.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.
[CreateAsync](#createasync) | Crea un entorno de WebView2 de perenne con la versión de Edge instalada.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Cree de forma asincrónica una nueva vista de vista previa.
[CreateWebResourceResponse](#createwebresourceresponse) | Crear un nuevo objeto de respuesta de recursos Web.

Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno. No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.

## Miembros

#### BrowserVersionString 

Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.

> cadena pública [BrowserVersionString](#browserversionstring)

Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString. Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.

#### NewBrowserVersionAvailable 

El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.

> evento público EventHandler< > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos. Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código. Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.

Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador. O simplemente pide al usuario que reinicie la aplicación.

#### CreateAsync 

Crea un entorno de WebView2 de perenne con la versión de Edge instalada.

> tarea asincrónica pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Options)

##### Parameters
* `browserExecutableFolder` La ruta de acceso relativa a la carpeta que contiene el borde incrustado. 

* `userDataFolder` userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2. 

* `options` Opciones usadas para crear un entorno WebView2.

#### CreateCoreWebView2ControllerAsync 

Cree de forma asincrónica una nueva vista de vista previa.

> tarea asincrónica pública< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada. La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView. El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.

Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación. Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.

#### CreateWebResourceResponse 

Crear un nuevo objeto de respuesta de recursos Web.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenido de Stream, int StatusCode, String ReasonPhrase, encabezados de cadena)

La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline. También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el CoreWebView2HttpResponseHeaders para construir los encabezados línea a línea. Para obtener información sobre otros parámetros, consulte CoreWebView2WebResourceResponse.

