---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: 05b8a10c723ae57b2c95551f4d5043f3336eba3b
ms.sourcegitcommit: 65db518273b3cd69f1b3c528809600719b9b70aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016329"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Esto representa el entorno de WebView2.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para su uso a través de WebView2.
[CompareBrowserVersions](#comparebrowserversions) | Compare las versiones del explorador para determinar si coinciden o son diferentes.
[CreateAsync](#createasync) | Crea un entorno de WebView2 de perenne con la versión instalada de Microsoft Edge.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Cree de forma asincrónica una nueva vista de vista previa.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Cree un CoreWebView2PointerInfo vacío.
[CreateWebResourceResponse](#createwebresourceresponse) | Crear un nuevo objeto de respuesta de recursos Web.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Obtener la información de versión del explorador.
[GetProviderForHwnd](#getproviderforhwnd) | Devuelve el proveedor de automatización de la interfaz de usuario de la CoreWebView2CompositionController que se corresponde con el HWND dado.

Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno. No se garantiza que su uso en diferentes entornos sea compatible y podría fallar. 

## Miembros

#### BrowserVersionString 

Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.

> cadena pública [BrowserVersionString](#browserversionstring)

Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString. Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.

#### NewBrowserVersionAvailable 

NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para su uso a través de WebView2.

> evento público EventHandler< > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos. Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código. Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.

Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador. O simplemente pide al usuario que reinicie la aplicación.

#### CompareBrowserVersions 

Compare las versiones del explorador para determinar si coinciden o son diferentes.

> public static int [CompareBrowserVersions](#comparebrowserversions)(cadena version1, String version2)

Devuelve-1, 0 o 1 dependiendo de si la primera versión es menor, igual o superior a la que se compara con la segunda versión.

La entrada puede usar directamente el versionInfo Obtenido de GetAvailableCoreWebView2BrowserVersionString, la información de canal se pasará por alto.

##### Parameters
* `version1` Primera versión que se va a comparar. 

* `version2` La segunda versión que se compara.

#### CreateAsync 

Crea un entorno de WebView2 de perenne con la versión instalada de Microsoft Edge.

> tarea pública estática asincrónica< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Options)

##### Parameters
* `browserExecutableFolder` La ruta de acceso relativa a la carpeta que contiene la versión fija del motor en tiempo de ejecución de WebView2. 

* `userDataFolder` userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2. 

* `options` Opciones usadas para crear un entorno WebView2.

#### CreateCoreWebView2CompositionControllerAsync 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.

> tarea asincrónica pública< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)

parentWindow es el HWND en el que la aplicación se conectará al árbol visual de la vista de ventana. Este es el HWND que la aplicación recibirá una entrada de puntero o de mouse para la vista de ventana (y deberá usar SendMouseInput/SendPointerInput para reenviar). Si la aplicación mueve el árbol visual WebView a una ventana distinta de otra, debe establecer CoreWebView2CompositionController. ParentWindow para actualizar el nuevo HWND primario del árbol visual.

Establezca la propiedad RootVisualTarget en el CoreWebView2CompositionController creado para proporcionar un objeto visual que hospede el árbol visual del explorador.

Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación. Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.

#### CreateCoreWebView2ControllerAsync 

Cree de forma asincrónica una nueva vista de vista previa.

> tarea asincrónica pública< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada. La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView. El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.

Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación. Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.

#### CreateCoreWebView2PointerInfo 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Cree un CoreWebView2PointerInfo vacío.

> Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()

La CoreWebView2PointerInfo devuelta debe rellenarse con toda la información relevante antes de llamar a SendPointerInput.

#### CreateWebResourceResponse 

Crear un nuevo objeto de respuesta de recursos Web.

> Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(contenido de Stream, int StatusCode, String ReasonPhrase, encabezados de cadena)

La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline. También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el CoreWebView2HttpResponseHeaders para construir los encabezados línea a línea. Para obtener información sobre otros parámetros, consulte CoreWebView2WebResourceResponse.

#### GetAvailableBrowserVersionString 

Obtener la información de versión del explorador.

> cadena estática pública [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(cadena browserExecutableFolder)

También puede obtener el nombre del canal si el canal no es estable. Si usas el tiempo de ejecución de WebView2, no se devuelve ningún nombre de canal.

##### Parameters
* `browserExecutableFolder` La ruta de acceso relativa a la carpeta que contiene la versión fija del motor en tiempo de ejecución de WebView2.

#### GetProviderForHwnd 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Devuelve el proveedor de automatización de la interfaz de usuario de la CoreWebView2CompositionController que se corresponde con el HWND dado.

> [GetProviderForHwnd](#getproviderforhwnd)de objeto público (HWND HWND)
