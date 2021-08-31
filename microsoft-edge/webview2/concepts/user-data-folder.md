---
description: Obtenga información sobre cómo administrar carpetas de datos de usuario en aplicaciones WebView2.
title: Administrar la carpeta de datos de usuario
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral, carpeta de datos de usuario
ms.openlocfilehash: 807c0cfa2a6a0ffa09aab7d369abc72ef2a390e4
ms.sourcegitcommit: 66a8e3db5b63b0532ca2f4003fa37bde6bd225b0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11933970"
---
# <a name="manage-the-user-data-folder"></a>Administrar la carpeta de datos de usuario  

Las aplicaciones WebView2 interactúan con carpetas de datos de usuario para almacenar datos del explorador, como cookies, permisos y recursos almacenados en caché.  Cada instancia de un control WebView2 está asociada a una carpeta de datos de usuario.  Cada carpeta de datos de usuario es única para un usuario.  

## <a name="best-practices"></a>Procedimientos recomendados  

WebView2 crea automáticamente las carpetas de datos de usuario.  Los programadores de WebView2 controlan la duración de la carpeta de datos de usuario.  Si la aplicación vuelve a usar datos de usuario de sesiones de aplicación, considere la posibilidad de guardar las carpetas de datos de usuario, de lo contrario, puede eliminarlos.  Tenga en cuenta los siguientes escenarios al decidir cómo administrar las carpetas de datos de usuario:  

*   Si el mismo usuario usa la aplicación repetidamente y el contenido web de la aplicación se basa en los datos del usuario, guarde la carpeta de datos del usuario.  Si varios usuarios usan la aplicación repetidamente, cree una nueva carpeta de datos de usuario para cada nuevo usuario y guarde la carpeta de datos de usuario de cada usuario.
*   Si la aplicación no tiene usuarios repetidos, cree una nueva carpeta de datos de usuario para cada usuario y elimine la carpeta de datos de usuario anterior.  
    
## <a name="create-user-data-folders"></a>Crear carpetas de datos de usuario  

Para especificar la ubicación de la carpeta de datos de usuario, incluya el parámetro al llamar a `userDataFolder` [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) o [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).  Después de la creación, los datos del explorador del control WebView2 se almacenan en una subcarpeta de `userDataFolder` .  Cuando `userDataFolder` no se especifica, WebView2 crea carpetas de datos de usuario en ubicaciones predeterminadas de la siguiente manera:  

*   Para las aplicaciones Windows store empaquetadas, la carpeta de usuario predeterminada es la `ApplicationData\LocalFolder` subcarpeta de la carpeta del paquete.  
*   Para las aplicaciones de escritorio existentes, la carpeta de datos de usuario predeterminada es la ruta de acceso exe de la aplicación + `.WebView2` .  En lugar de usar el valor predeterminado, se recomienda especificar una carpeta de datos de usuario y crearla en la misma carpeta donde se almacenan todos los demás datos de la aplicación.  
    
## <a name="delete-user-data-folders"></a>Eliminar carpetas de datos de usuario  

Es posible que la aplicación necesite eliminar carpetas de datos de usuario por los siguientes motivos:

*   Al desinstalar la aplicación.  Si desinstala aplicaciones empaquetadas Windows store, Windows las carpetas de datos de usuario automáticamente.  
*   Para limpiar todo el historial de datos de exploración.  
*   Para recuperarse de daños en los datos.  
*   Para quitar datos de sesión anteriores.  
    
> [!NOTE]
> Es posible que los archivos de las carpetas de datos de usuario aún se usen después de cerrar la aplicación WebView2.  En esta situación, espere a que el proceso del explorador y todos los procesos secundarios se cierren antes de eliminar la carpeta.  Puede recuperar el identificador de proceso del proceso del explorador mediante la `BrowserProcessId` propiedad webView2.  

## <a name="share-user-data-folders"></a>Compartir carpetas de datos de usuario  

Los controles WebView2 pueden compartir las mismas carpetas de datos de usuario para:  

*   [Optimice los recursos del](../concepts/process-model.md) sistema ejecutándose en un proceso de explorador.  
*   Compartir el historial del explorador y los recursos almacenados en caché.  
    
Tenga en cuenta lo siguiente al compartir carpetas de datos de usuario:  

1.  Al volver a crear controles WebView2 para actualizar las versiones del explorador mediante [eventos add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \(Win32\) o [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\), asegúrese de que los procesos del explorador salen y cierran los controles webView2 que comparten la misma carpeta de datos de usuario.  Para recuperar el identificador de proceso del proceso del explorador, use la `BrowserProcessId` propiedad del control WebView2.  
1.  Los controles WebView2 que comparten la misma carpeta de datos de usuario deben usar las mismas opciones para [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) o [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).  Si no es así, la creación de WebView2 producirá un error con `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .  
    
Para aislar diferentes partes de la aplicación, o cuando no es necesario compartir datos entre controles WebView2, puede usar diferentes carpetas de datos de usuario.  Por ejemplo, una aplicación puede estar formada por dos controles WebView2, uno para mostrar un anuncio y otro para mostrar contenido de la aplicación.  Puede usar diferentes carpetas de datos de usuario para cada control WebView2.

> [!NOTE]
> Cada proceso de explorador webView2 consume memoria adicional y espacio en disco.  Por lo tanto, se recomienda no ejecutar un control WebView2 con demasiadas carpetas de datos de usuario diferentes al mismo tiempo.  
