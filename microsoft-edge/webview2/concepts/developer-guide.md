---
description: Obtenga información sobre los procedimientos recomendados de desarrollo que se deben usar al desarrollar la aplicación WebView2.
title: Procedimientos recomendados de desarrollo de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, edge, procedimientos recomendados
ms.openlocfilehash: 7e8c6746e864b474c2987817c521224499a95e1f
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627981"
---
# <a name="webview2-development-best-practices"></a>Procedimientos recomendados de desarrollo de WebView2  

Cada equipo de desarrollo sigue diferentes prácticas al compilar su aplicación. Al crear aplicaciones webView2, hay prácticas que se recomienda seguir. En este artículo se describen las recomendaciones y los procedimientos recomendados para usted al crear aplicaciones WebView2 basadas en producción.

## <a name="use-evergreen-webview2-runtime-recommended"></a>Usar Evergreen WebView2 Runtime (recomendado)  

Aunque La versión fija tiene sus casos de uso para aplicaciones que tienen requisitos de compatibilidad estrictos, se recomienda usar Evergreen WebView2 Runtime.  Evergreen WebView2 Runtime se actualiza automáticamente e incluye las últimas características y revisiones de seguridad disponibles para la aplicación WebView2. Evergreen WebView2 Runtime también requiere menos espacio de almacenamiento en el disco.

Asegúrese de que Evergreen WebView2 Runtime está instalado antes de usar la aplicación WebView2.  Para obtener más información, vaya [a Deploying the Evergreen WebView2 Runtime][Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime].  

## <a name="run-compatibility-tests-regularly-when-using-the-evergreen-webview2-runtime"></a>Ejecutar pruebas de compatibilidad con regularidad al usar Evergreen WebView2 Runtime

Al usar Evergreen WebView2 Runtime, el tiempo de ejecución se actualiza automáticamente, por lo que debe ejecutar periódicamente pruebas de compatibilidad. Pruebe el contenido web del control WebView2 con las versiones no estables de Microsoft Edge, para asegurarse de que la aplicación WebView2 funciona según lo esperado.

Esta guía es similar a la que ofrecemos a los desarrolladores web. Para obtener más información, vaya a [Permanecer compatible en modo Evergreen][Webview2ConceptsDistributionStayCompatibleEvergreenMode].

## <a name="ensure-apis-are-supported-by-the-installed-webview2-runtime"></a>Asegúrese de que las API son compatibles con el tiempo de ejecución de WebView2 instalado

Las aplicaciones webView2 necesitan un SDK de Webview2 y un Tiempo de ejecución de WebView2 instalado en el equipo para ejecutarse. Tanto el SDK como el tiempo de ejecución tienen versiones. Dado que las API se agregan continuamente a WebView2, también se lanzan nuevas versiones del tiempo de ejecución para admitir las nuevas API. Asegúrese de que las API que usa la aplicación WebView2 son compatibles con El tiempo de ejecución de WebView2 que está instalado en el equipo. 

Si usa Evergreen WebView2 Runtime, hay algunos escenarios en los que es posible que el tiempo de ejecución no se actualice para usar la versión más reciente. Por ejemplo, cuando los usuarios no tienen acceso a Internet, el tiempo de ejecución no se actualiza automáticamente en ese entorno. Además, el uso de algunas directivas de grupo pausa las actualizaciones de WebView2. Al insertar una actualización en la aplicación WebView2, la aplicación puede interrumpirse porque usa API más recientes que no están disponibles en el tiempo de ejecución instalado.   
 
Para solucionar esta situación, puede probar la disponibilidad de las API en el tiempo de ejecución instalado, antes de que el código llame a la API. Esta prueba de funcionalidad más reciente es similar a otros procedimientos recomendados de desarrollo web que detectan características compatibles antes de usar nuevas API web. Para probar la disponibilidad de la API en el tiempo de ejecución instalado, use:  

*   El `queryinterface` de C/C++. 
*   Un bloque try/catch en .NET o WinUI. 
    
Para obtener más información, vaya a [Determine WebView2 Runtime requirement][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement].  

## <a name="update-the-fixed-version-runtime"></a>Actualizar el tiempo de ejecución de la versión fija  

Si usa el tiempo de ejecución de versión fija, asegúrese de actualizar el tiempo de ejecución con regularidad para reducir cualquier riesgo de seguridad potencial. Al usar contenido de terceros en aplicaciones webview2, tenga en cuenta siempre que el contenido no es de confianza.  Para obtener más información, vaya al [modo de distribución de versión fija][Webview2ConceptsDistributionFixedVersionDistributionMode].  

## <a name="manage-new-versions-of-the-runtime"></a>Administrar nuevas versiones del tiempo de ejecución  

Cuando se descarga una nueva versión de Evergreen WebView2 Runtime en el dispositivo, las aplicaciones webView2 que se ejecutan siguen usando el tiempo de ejecución anterior, hasta que se libera el proceso del explorador.  Este comportamiento permite que las aplicaciones se ejecuten continuamente e impide que se elimine el tiempo de ejecución anterior.  Para usar la nueva versión del tiempo de ejecución, deberá liberar todas las referencias a los objetos de entorno webView2 anteriores o reiniciar la aplicación.  La próxima vez que cree un nuevo entorno WebView2, usará la nueva versión.

Cuando hay una nueva versión disponible, puede realizar acciones automáticamente, como notificar al usuario que reinicie la aplicación.  Para detectar que hay disponible una nueva versión, puede usar el evento [add_NewBrowserVersionAvailable(Win32)][Webview2ReferenceaddNewBrowserVersionAvailable] o [CoreWebView2Environment.NewBrowserVersionAvailable(.NET)][Webview2ReferenceNewBrowserVersionAvailable] en el código. Si el código controla el reinicio de la aplicación, considere la posibilidad de guardar el estado de usuario antes de que salga la aplicación WebView2.  

## <a name="manage-the-lifetime-of-the-user-data-folder"></a>Administrar la duración de la carpeta de datos de usuario 
Las aplicaciones webView2 crean una carpeta de datos de usuario para almacenar datos como cookies, credenciales y permisos.  Después de crear la carpeta, la aplicación es responsable de administrar la duración de la carpeta de datos de usuario.  Por ejemplo, la aplicación debe realizar la limpieza cuando se desinstala la aplicación.  Para obtener más información, vaya a [Administrar la carpeta de datos de usuario][Webview2ConceptsUserDataFolder].  

## <a name="handle-runtime-process-failures"></a>Controlar errores de proceso en tiempo de ejecución
La aplicación WebView2 debe escuchar y controlar el evento, por lo que la aplicación puede recuperarse de errores de procesos en tiempo de ejecución compatibles con el proceso `ProcessFailed` de aplicación webView2.

Las aplicaciones webView2 son compatibles con una colección de procesos en tiempo de ejecución que se ejecutan junto con el proceso de la aplicación. Estos procesos de tiempo de ejecución compatibles pueden producir errores por diversos motivos, como que el usuario se esté quedando sin memoria o que el usuario termine. Cuando se produce un error en un proceso de tiempo de ejecución compatible, WebView2 notifica a la aplicación generando el [evento ProcessFailed][WebView2ProcessFailedEvent].

## <a name="follow-recommended-webview2-security-best-practices"></a>Seguir los procedimientos recomendados de seguridad de WebView2 
Para cualquier aplicación WebView2, asegúrese de seguir nuestros procedimientos recomendados de seguridad de WebView2.  Para obtener más información, vaya a [Procedimientos recomendados para desarrollar aplicaciones webView2 seguras.][Webview2ConceptsSecurity]  

<!-- links -->  

[Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]: ../concepts/distribution.md#deploying-the-evergreen-webview2-runtime "Implementación de Evergreen WebView2 Runtime: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ../concepts/distribution.md#fixed-version-distribution-mode "Modo de distribución de versiones fijas: distribución de aplicaciones mediante WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionStayCompatibleEvergreenMode]: ../concepts/distribution.md#stay-compatible-in-evergreen-mode "Mantener la compatibilidad en modo Evergreen: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ../concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones webView2 seguras | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ../concepts/user-data-folder.md "Administrar la carpeta de datos de usuario | Microsoft Docs"  
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#determine-webview2-runtime-requirement "Determinar el requisito de Tiempo de ejecución de WebView2: comprender las versiones del SDK de WebView2 | Microsoft Docs"  
[Webview2GetStartedWin32]: ../get-started/win32.md "Introducción a WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ../get-started/winforms.md "Introducción a WebView2 en Windows Forms | Microsoft Docs"  
[Webview2GetStartedWinui]: ../get-started/winui.md "Introducción a WebView2 en WinUI 3 (versión preliminar) | Microsoft Docs"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Introducción a WebView2 en WPF | Microsoft Docs"  

[Webview2ReferenceaddNewBrowserVersionAvailable]: /microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable "add_NewBrowserVersionAvailable | Microsoft Docs"  

[Webview2ReferenceNewBrowserVersionAvailable]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable "Evento CoreWebView2Environment.NewBrowserVersionAvailable | Microsoft Docs"  
[WebView2ProcessFailedEvent]: /microsoft-edge/webview2/reference/win32/icorewebview2processfailedeventargs "ICoreWebView2ProcessFailedEventArgs | Microsoft Docs"  

