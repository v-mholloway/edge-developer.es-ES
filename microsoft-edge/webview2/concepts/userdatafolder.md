---
description: Más información sobre cómo administrar carpetas de datos de usuario en aplicaciones de WebView2
title: Administrar la carpeta de datos de usuario en aplicaciones de WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control browser, HTML Edge, carpeta de datos de usuario
ms.openlocfilehash: ff11c4e83fa931a97ed1b5c8afa4a30b5c0b5d25
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118992"
---
# Administrar la carpeta de datos de usuario  

Las aplicaciones de WebView2 interactúan con las carpetas de datos de usuario para almacenar los datos del explorador, como cookies, permisos y recursos almacenados en la memoria caché.  Cada instancia de un control WebView2 está asociada a una carpeta de datos de usuario.  Cada carpeta de datos de usuario es única para un usuario.  

## Procedimientos recomendados  

Las carpetas de datos de usuario se crean automáticamente mediante WebView2.  Los programadores de WebView2 controlan la duración de la carpeta de datos de usuario.  Si su aplicación vuelve a usar los datos de usuario de las sesiones de la aplicación, considere la posibilidad de guardar las carpetas de datos de usuario; de lo contrario, puede eliminarlas.  Considere los escenarios siguientes al decidir cómo administrar las carpetas de datos de usuario:  

*   Si el mismo usuario usa la aplicación varias veces y el contenido Web de la aplicación depende de los datos del usuario, guarde la carpeta de datos de usuario.  Si varios usuarios usan la aplicación varias veces, cree una nueva carpeta de datos de usuario para cada nuevo usuario y guarde la carpeta de datos de usuario de cada usuario.
*   Si su aplicación no tiene usuarios repetidos, cree una nueva carpeta de datos de usuario para cada usuario y elimine la carpeta datos de usuario anterior.  

## Crear carpetas de datos de usuario  

Para especificar la ubicación de la carpeta de datos de usuario, incluya el `userDataFolder` parámetro al llamar a [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \ (Win32 \) o [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \ (.net \).  Después de la creación, los datos del explorador del control WebView2 se almacenan en una subcarpeta de `userDataFolder` .  Cuando `userDataFolder` no se especifica, WebView2 crea carpetas de datos de usuario en ubicaciones predeterminadas de la siguiente manera:  

*   Para las aplicaciones empaquetadas de la tienda Windows, la carpeta de usuario predeterminada es la subcarpeta `ApplicationData\LocalFolder` de la carpeta del paquete.  
*   Para las aplicaciones de escritorio existentes, la carpeta datos de usuario predeterminada es la ruta de acceso de archivo exe de la aplicación + `.WebView2` .  En lugar de usar el valor predeterminado, le recomendamos que especifique una carpeta de datos de usuario y que la cree en la misma carpeta en la que se almacenan todos los demás datos de la aplicación.  

## Eliminar carpetas de datos de usuario  

Es posible que su aplicación tenga que eliminar las carpetas de datos de usuario:  

*   Al desinstalar la aplicación.  Si está desinstalando aplicaciones de la tienda Windows empaquetadas, Windows elimina automáticamente las carpetas de datos de usuario.  
*   Para limpiar todo el historial de datos de exploración.  
*   Para recuperar datos dañados.  
*   Para quitar los datos de sesión anteriores.  

> [!NOTE]
> Es posible que los archivos de carpetas de datos de usuario aún estén en uso después de cerrar la aplicación WebView2.  En esta situación, espere a que el proceso del explorador y todos los procesos secundarios se cierren antes de eliminar la carpeta.  Puede recuperar el identificador de proceso del proceso del explorador mediante la `BrowserProcessId` propiedad de la WebView2.  

## Compartir carpetas de datos de usuario  

Es posible que los controles WebView2 compartan las mismas carpetas de datos de usuario en:  

*   [Optimizar los recursos del sistema](../concepts/process-model.md) al ejecutarse en un solo proceso del explorador.  
*   Compartir el historial del explorador y los recursos almacenados en caché.  

Tenga en cuenta lo siguiente al compartir carpetas de datos de usuario:  

1.  Al volver a crear los controles de WebView2 para actualizar las versiones del explorador con los eventos [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \ (Win32 \) o [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \ (.net \), asegúrese de que los procesos del explorador cierran y cierran WebView2 controles que comparten la misma carpeta de datos de usuario.  Para recuperar el identificador de proceso del proceso del explorador, use la `BrowserProcessId` propiedad del control WebView2.  

2.  Los controles de WebView2 que comparten la misma carpeta de datos de usuario deben usar las mismas opciones para [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \ (Win32 \) o [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \ (.net \).  De lo contrario, se producirá un error en la creación de WebView2 `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .  

Para aislar las distintas partes de la aplicación o cuando no es necesario compartir datos entre controles WebView2, puede optar por usar carpetas de datos de usuario diferentes.  Por ejemplo, una aplicación puede constar de dos controles WebView2, uno para mostrar un anuncio y el otro para mostrar el contenido de la aplicación.  En este caso, los desarrolladores pueden optar por usar distintas carpetas de datos de usuario para cada control de WebView2.  

> [!NOTE]
> Cada proceso de explorador WebView2 consume memoria y espacio en disco adicional.  Por lo tanto, le recomendamos que no ejecute WebView2s con demasiadas carpetas de datos de usuario diferentes al mismo tiempo.  
