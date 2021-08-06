---
description: Obtenga información sobre los procedimientos recomendados de desarrollo que se deben usar al desarrollar la aplicación WebView2.
title: Procedimientos recomendados de desarrollo de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, edge, procedimientos recomendados
ms.openlocfilehash: d4b7544a991fb9dda80d969afc8e7da2bc83d711d9a2002fb205271f87960f2f
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11800146"
---
# <a name="webview2-development-best-practices"></a>Procedimientos recomendados de desarrollo de WebView2

Cada equipo de desarrollo sigue diferentes prácticas al compilar su aplicación.  Al crear aplicaciones de producción de WebView2, se recomienda seguir estas recomendaciones y procedimientos recomendados.


## <a name="use-the-evergreen-runtime-recommended"></a>Usar el tiempo de ejecución de Evergreen (recomendado)

Por lo general, se recomienda usar Evergreen WebView2 Runtime.  La distribución de tiempo de ejecución de versiones fijas solo se recomienda para aplicaciones que tienen requisitos de compatibilidad estrictos.  El tiempo de ejecución de Evergreen se actualiza automáticamente en el cliente, de modo que las últimas características y revisiones de seguridad estén disponibles para la aplicación WebView2.  El tiempo de ejecución de Evergreen también requiere menos espacio de almacenamiento en el disco que el tiempo de ejecución de la versión fija.

Si usas el tiempo de ejecución de Evergreen, antes de ejecutar la aplicación WebView2, prueba si Evergreen WebView2 Runtime está instalado en el cliente.  Para obtener más información, vaya [a Deploying the Evergreen WebView2 Runtime][Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime].


## <a name="run-compatibility-tests-regularly-when-using-the-evergreen-runtime"></a>Ejecutar pruebas de compatibilidad con regularidad al usar Evergreen Runtime

Al usar Evergreen WebView2 Runtime, el tiempo de ejecución se actualiza automáticamente, por lo que debe ejecutar periódicamente pruebas de compatibilidad.  Para asegurarse de que la aplicación WebView2 seguirá funcionando como se esperaba, pruebe el contenido web en el control WebView2 con los canales [de Insider (versión preliminar)][MicrosoftedgeinsiderDownload] de Microsoft Edge (Beta, Desarrollo o Canary).

Esta guía es similar a la que ofrecemos a los desarrolladores web.  Para obtener más información, vaya [a Probar la aplicación para la compatibilidad con avances.][Webview2ConceptsDistributionStayCompatibleEvergreenMode]


## <a name="test-whether-newer-apis-are-supported-by-the-installed-webview2-runtime"></a>Probar si las API más recientes son compatibles con el tiempo de ejecución de WebView2 instalado

<!-- the main section about QueryInterface is in versioning.md; this section should be only a couple paragraphs -->

Para ejecutar una aplicación WebView2 desarrollada con una versión determinada del SDK de Webview2, el cliente debe tener instalada una versión compatible de WebView2 Runtime.  Dado que las API se agregan continuamente a WebView2, también se lanzan nuevas versiones del tiempo de ejecución para admitir las nuevas API.  Usa la detección de características para asegurarte de que las API más recientes que usa la aplicación WebView2 son compatibles con El tiempo de ejecución de WebView2 instalado en el cliente.

Si usa Evergreen WebView2 Runtime, hay algunos escenarios en los que el tiempo de ejecución de un cliente no se ha actualizado automáticamente a la versión más reciente.  Por ejemplo, si un cliente no tiene acceso a Internet, el tiempo de ejecución no se actualiza automáticamente.  Además, algunas directivas de grupo pausan la actualización del tiempo de ejecución.  Al insertar una actualización en la aplicación WebView2, es posible que la aplicación no funcione si intenta llamar a API más recientes que no están disponibles en el tiempo de ejecución instalado del cliente.

Para solucionar esta situación, antes de que el código llame a una API de WebView2 agregada recientemente, compruebe si esa API está disponible en el tiempo de ejecución instalado del cliente.  Esta prueba de funcionalidad más reciente es similar a otros procedimientos recomendados de desarrollo web que detectan características compatibles antes de usar nuevas API web.  Para probar la disponibilidad de la API en el tiempo de ejecución instalado, use:

*   `QueryInterface` en C/C++.
*   Un `try/catch` bloque en .NET o WinUI.

Para obtener más información, vaya a Detección de características para comprobar si el tiempo de ejecución instalado [admite API agregadas recientemente.][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]


## <a name="update-the-fixed-version-runtime"></a>Actualizar el tiempo de ejecución de la versión fija

Si usas El tiempo de ejecución de WebView2 de versión fija, asegúrate de actualizar regularmente el tiempo de ejecución de WebView2 que está empaquetado con la aplicación, para reducir los riesgos de seguridad.  Al usar contenido de terceros en aplicaciones webview2, considere siempre que el contenido no es de confianza.  Para obtener más información, vaya al [modo de distribución de versión fija][Webview2ConceptsDistributionFixedVersionDistributionMode].


## <a name="manage-new-versions-of-the-evergreen-runtime"></a>Administrar nuevas versiones de Evergreen Runtime

Cuando se descarga una nueva versión de Evergreen WebView2 Runtime en el cliente, las aplicaciones webView2 que se ejecutan siguen usando la versión anterior del tiempo de ejecución, hasta que se libera el proceso del explorador.  Este comportamiento permite que las aplicaciones se ejecuten continuamente e impide que se elimine el tiempo de ejecución anterior.  Para usar la nueva versión del tiempo de ejecución, debes liberar todas las referencias a los objetos de entorno webView2 anteriores o reiniciar la aplicación.  La próxima vez que la aplicación cree un nuevo entorno WebView2, la aplicación usará la nueva versión del tiempo de ejecución.

Cuando hay disponible una nueva versión del tiempo de ejecución, la aplicación puede tomar medidas automáticamente, como notificar al usuario que reinicie la aplicación.  Para detectar que hay disponible una nueva versión del tiempo de ejecución, puede usar el evento [add_NewBrowserVersionAvailable (Win32)][Webview2ReferenceaddNewBrowserVersionAvailable] o [CoreWebView2Environment.NewBrowserVersionAvailable (.NET)][Webview2ReferenceNewBrowserVersionAvailable] en el código.  Si el código controla el reinicio de la aplicación, considera la posibilidad de guardar el estado del usuario antes de que salga la aplicación WebView2.

<!-- are the Ref links enough, or link to a regular article or article subsection? -->


## <a name="manage-the-lifetime-of-the-user-data-folder"></a>Administrar la duración de la carpeta de datos de usuario

Las aplicaciones webView2 crean una carpeta de datos de usuario para almacenar datos como cookies, credenciales y permisos.  Después de crear la carpeta, la aplicación es responsable de administrar la duración de la carpeta de datos de usuario.  Por ejemplo, la aplicación debe realizar la limpieza cuando se desinstala la aplicación.  Para obtener más información, vaya a [Administrar la carpeta de datos de usuario][Webview2ConceptsUserDataFolder].


## <a name="handle-runtime-process-failures"></a>Controlar errores de proceso en tiempo de ejecución

La aplicación WebView2 debe escuchar y controlar el evento, por lo que la aplicación puede recuperarse de errores de procesos en tiempo de ejecución compatibles con el proceso `ProcessFailed` de aplicación webView2.

Las aplicaciones webView2 son compatibles con una colección de procesos en tiempo de ejecución que se ejecutan junto con el proceso de la aplicación.  Estos procesos de tiempo de ejecución compatibles pueden producir errores por diversos motivos, como que el usuario se esté quedando sin memoria o que el usuario termine.  Cuando se produce un error en un proceso de tiempo de ejecución compatible, WebView2 notifica a la aplicación generando el [evento ProcessFailed][WebView2ProcessFailedEvent].

<!-- is the Ref link enough, or link to a long section in regular docs? -->


## <a name="follow-recommended-webview2-security-best-practices"></a>Seguir los procedimientos recomendados de seguridad de WebView2

Para cualquier aplicación WebView2, asegúrate de seguir nuestros procedimientos recomendados de seguridad de WebView2.  Para obtener más información, vaya a [Procedimientos recomendados para desarrollar aplicaciones webView2 seguras.][Webview2ConceptsSecurity]


<!-- links -->
[Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]: ../concepts/distribution.md#deploying-the-evergreen-webview2-runtime "Implementación de Evergreen WebView2 Runtime: distribuir una aplicación WebView2 y la aplicación WebView2 Runtime | Microsoft Docs"
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ../concepts/distribution.md#details-about-the-fixed-version-runtime-distribution-mode "Detalles sobre el modo de distribución de Tiempo de ejecución de versión fija: distribuir una aplicación WebView2 y webView2 Runtime | Microsoft Docs"
[Webview2ConceptsDistributionStayCompatibleEvergreenMode]: ../concepts/distribution.md#test-your-app-for-forward-compatibility "Probar la compatibilidad de la aplicación con avances: distribuir una aplicación WebView2 y el entorno de tiempo de ejecución de WebView2 | Microsoft Docs"
[Webview2ConceptsSecurity]: ../concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones webView2 seguras | Microsoft Docs"
[Webview2ConceptsUserDataFolder]: ../concepts/user-data-folder.md "Administrar la carpeta de datos de usuario | Microsoft Docs"
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#feature-detecting-to-test-whether-the-installed-runtime-supports-recently-added-apis "Detección de características para comprobar si el tiempo de ejecución instalado admite API agregadas recientemente: comprender las versiones del SDK de WebView2 | Microsoft Docs"
[Webview2GetStartedWin32]: ../get-started/win32.md "Introducción a WebView2 | Microsoft Docs"
[Webview2GetStartedWinforms]: ../get-started/winforms.md "Introducción a WebView2 en Windows Forms | Microsoft Docs"
[Webview2GetStartedWinui]: ../get-started/winui.md "Introducción a WebView2 en WinUI 3 (versión preliminar) | Microsoft Docs"
[Webview2GetStartedWpf]: ../get-started/wpf.md "Introducción a WebView2 en WPF | Microsoft Docs"
<!-- external links -->
[Webview2ReferenceaddNewBrowserVersionAvailable]: /microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable "add_NewBrowserVersionAvailable | Microsoft Docs"

[Webview2ReferenceNewBrowserVersionAvailable]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable "Evento CoreWebView2Environment.NewBrowserVersionAvailable | Microsoft Docs"
[WebView2ProcessFailedEvent]: /microsoft-edge/webview2/reference/win32/icorewebview2processfailedeventargs "ICoreWebView2ProcessFailedEventArgs | Microsoft Docs"

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"
