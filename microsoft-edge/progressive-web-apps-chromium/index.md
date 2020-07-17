---
description: Las aplicaciones web progresivas se ejecutan de forma nativa en Windows 10.  Aquí encontrarás todo lo que necesitas saber como desarrollador web.
title: Aplicaciones web progresivas en Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 90740bac07ebfd74f89e2524e6955621e1b09b05
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882810"
---
# Aplicaciones web progresivas en Windows  

Con las [aplicaciones web progresivas][MDNApps] \ (o simplemente PWAs \), no tiene que decidir entre usar las tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionar a los usuarios una experiencia nativa de tipo aplicación personalizada para sus dispositivos.  PWAs son solo sitios web que se han [mejorado progresivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicaciones nativas en plataformas compatibles.  Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.  

:::row:::
    :::column:::
        ![Icono de descubrimiento][ImageISearch]
        ### [Reconocible][MDNPwaAdvantagesDiscoverable]
        Desde los resultados de la búsqueda web y los almacenes de aplicaciones auxiliares
    :::column-end:::
    :::column:::
        ![Icono de instalación][ImageIPackage]
        ### [Instalables][MDNPwaAdvantagesInstallable]
        Anclar e iniciar desde la pantalla principal, el menú Inicio, la barra de tareas, etc.
    :::column-end:::
    :::column:::
        ![Icono volver a participar][ImageIPushNotification]
        ### [Reactivable][MDNPwaAdvantagesReEngageable]
        Enviar notificaciones push, incluso cuando la aplicación no está activa
    :::column-end:::
    :::column:::
        ![Icono independiente de red][ImageIOffline]
        ### [Independiente de la red][MDNPwaAdvantagesNetworkIndependent]
        Trabaja sin conexión y en condiciones de redes bajas
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Icono de progresivo][ImageIProgressive]
        ### [Reduci][MDNPwaAdvantagesProgressive]
        Experiencia de ampliación (o de baja) con capacidades de dispositivo
    :::column-end:::
    :::column:::
        ![Icono de seguridad][ImageISecurity]
        ### [Seguros][MDNPwaAdvantagesSafe]
        Proporciona un punto de conexión HTTPS seguro y otras medidas de seguridad para el usuario
    :::column-end:::
    :::column:::
        ![Icono de respuesta][ImageIResponsive]
        ### [Dinámica][MDNPwaAdvantagesResponsive]
        Se adapta al tamaño de la pantalla o a la orientación y el método de entrada del usuario
    :::column-end:::
    :::column:::
        ![Icono de vínculo][ImageILink]
        ### [Linkable][MDNPwaAdvantagesLinkable]
        Compartir e iniciar desde un hipervínculo estándar
    :::column-end:::
:::row-end:::

Al crear o convertir el sitio existente en un PWA, usted se compromete mejor con su audiencia existente mediante notificaciones push, integración de tipo aplicación y soporte técnico sin conexión.  Al mismo tiempo, debe continuar con la creación de la audiencia en la web abierta, ya que los usuarios pueden descubrir su PWA mediante la búsqueda y el uso compartido de vínculos.  Lo mejor de todo es que puedes actualizar tu aplicación actualizando el código de tu servidor Web.  

## PWAs en Microsoft Edge (cromo)  

Al crear una aplicación web progresiva dirigida a las API de Web Standard, la aplicación puede implementarse en varias plataformas y dispositivos, y aprovechar las capacidades específicas del dispositivo según esté disponible.  PWAs en Microsoft Edge \ (cromo \) se basa completamente en estándares desde una perspectiva de plataforma web y permite a los usuarios instalar la aplicación directamente desde el explorador sin necesidad de un registro o implementación basado en la tienda.  Los PWAs de escritorio son compatibles con cualquiera de las plataformas Microsoft Edge \ (cromo \) está disponible, incluidos Windows 7, Windows 10 y macOS.  Otros beneficios son:  

*   Las aplicaciones se pueden instalar directamente desde el explorador mediante el icono de **instalación** de la barra de navegación.  
    
    ![Instalar el control flotante y el icono de la aplicación][ImageInstallPwa]  
    
*   Las aplicaciones también pueden instalarse, ejecutarse y administrarse desde el menú de **Settings**  >  **aplicaciones** de configuración  
    
    ![Elementos de menú de la aplicación en configuración][ImageAppMenus]  

*   Las notificaciones web están integradas en el sistema de notificaciones de Windows
*   Almacén de cookies compartido con el perfil de explorador que instaló la aplicación
*   Acceso a otras características del explorador mediante el `...` menú, como la validación de certificados, los permisos de sitio, la protección de rastreo y las extensiones de explorador
*   Acceso total a [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para la depuración de la aplicación  

> [!IMPORTANT]
> Para personalizar PWAs específicamente para Windows 10 que realizan solicitudes de API de WinRT con JavaScript, consulta la [documentación específica de las características de EDGEHTML PWA][PwaEdgehtmlIndex].  Obtenga más información sobre cómo probar su PWA en Windows 10 y cómo distribuirlo en Microsoft Store.  

> [!NOTE]
> Consulte la [sesión de compilación 2020 PWA][BuildVideo] para obtener información general sobre los beneficios de PWA, las próximas características y las demostraciones breves. 

## Requisitos  

Para ejecutar como PWA, la aplicación web hospedada por el servidor debe incluir los siguientes requisitos mínimos.  

| Requisitos | Detalles | 
|:--- |:--- |  
| [HTTPS][WikiHttps] | Proteger a los usuarios proporcionando una conexión segura para la comunicación entre servidores o aplicaciones.  Los trabajadores del servicio y otras tecnologías de PWA solo funcionan con recursos Web servidos a través de una conexión segura \ (o de `localhost` para fines de depuración \).  |  
| [Trabajos de servicio][MDNServiceWorkerApi] | Use los subprocesos de trabajo de servicio para actuar como proxies de red entre su servidor y la aplicación cliente a fin de proporcionar compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones push, sincronización de datos en segundo plano y optimizaciones del rendimiento de carga de la página.  |  
| [Manifiesto de la aplicación Web][MDNWebAppManifest] | Proporcione un archivo de metadatos basado en JSON que describa la información clave de la aplicación web \ (como iconos, idioma y punto de entrada de dirección URL \), para que Windows 10 y otras plataformas de hospedaje puedan proporcionar a los usuarios de PWA una experiencia de aplicación nativa, instalable y de aplicación.  |  

Para ser un fantástico PWA, tu aplicación también debe cumplir con los siguientes requisitos.  

| Requisitos | Detalles | 
|:--- |:--- |  
| [Compatibilidad entre exploradores][MDNCrossBrowserTesting] | Asegúrese de que su PWA funciona [probando][MicrosoftDeveloperEdgeToolsRemote] en exploradores y entornos diferentes.  |  
| [Diseño adaptativo][WikiResponsiveWebDesign] | Use diseños fluidos y imágenes flexibles con CSS [Grid][MDNCssGridLayout], [Flexbox][MDNCssFlexibleBoxLayout], CSS [Grid][MDNCssGridLayout] y [Flexbox][MDNCssFlexibleBoxLayout] , [consultas de medios][MDNMediaQueries]e [imágenes de respuesta][MDNResponsiveImages] para adaptar su UX al dispositivo del usuario.  Use [las herramientas de emulación de dispositivos][DevToolsGuide|::ref1::|] de su explorador para probar de forma local o configure una [sesión de depuración remota][DevToolsProtocolClientsEdgeDevToolsPreview] para probar directamente en un dispositivo de destino.  |  
| [Vinculación profunda][WikiDeepLinking] | Enrute cada página de su sitio a una dirección URL única de modo que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia mediante el uso compartido de los medios sociales.  |  
| [Procedimientos recomendados][Webhint] | Usa herramientas de calidad de código como [webhint][Webhint] pelusa para optimizar la eficacia, solidez, seguridad y accesibilidad de tu aplicación.  |  
| [Lista de comprobación de cromo PWA][WebDevGoodPwaChecklist] | Consulte su PWA con la lista de comprobación de Google Baseline PWA.  |  

Si quiere convertir su PWA en una aplicación de [Microsoft Store][MicrosoftDeveloperStore] , vaya a la documentación de las [aplicaciones web progresivas (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .  
  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

[ImageInstallPwa]: ./media/Install_PWA.png  
[ImageAppMenus]: ./media/App_menus.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Vista previa de Microsoft Edge DevTools - Clientes de protocolo de DevTools"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Emulación"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps.md "Depurar aplicaciones web progresivas"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Novedades de EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Novedades de EdgeHTML 14"  
[PwaEdgehtmlIndex]: ../progressive-web-apps-edgehtml/index.md "Aplicaciones web progresivas (EdgeHTML) en Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Aplicaciones web progresivas en Microsoft Store"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Introducción a los servicios de notificaciones de inserción de Windows \ (WNS \)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Diseño para Xbox y TV"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Consideraciones sobre la interfaz de usuario para dispositivos UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "¿Qué es una aplicación para la plataforma universal de Windows (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Admitir la aplicación con tareas en segundo plano"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publicar aplicaciones y juegos de Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Abrir una cuenta de desarrollador"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Bienvenida a aplicaciones web progresivas a Microsoft Edge y Windows 10: blogs de Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de sincronización en segundo plano-estado de la plataforma de Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifiesto de la aplicación web: estado de la plataforma de Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Pruebas instantáneas"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Realidad mixta para desarrolladores"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Tienda de Microsoft Developer"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Activar o desactivar el centro de atención de foco en Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Cambiar la configuración de notificaciones en Windows 10"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Descripción de la mejora progresiva: una lista separada"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "aplicaciones | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Pruebas entre exploradores | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Diseño de cuadro flexible CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Diseño de cuadrícula CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Fetch API | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Consultas de medios | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Reconocible: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Instalable: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Linkable: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Red independiente: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Ventajas progresivas de las aplicaciones Web"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Reactivable: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Ventajas de la aplicación web progresiva de respuesta"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Ventajas de la aplicación web con seguridad progresiva"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imágenes de respuesta | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de la aplicación Web | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Vídeo de PWA"

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "¿Qué es una buena aplicación web progresiva? | Web. dev"  

[Webhint]: https://webhint.io "sugerencia"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculación profunda: Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Diseño web con respuesta: Wikipedia"  
