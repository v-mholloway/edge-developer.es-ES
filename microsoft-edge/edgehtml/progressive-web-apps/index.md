---
description: Las aplicaciones web progresivas se ejecutan de forma nativa en Windows 10.  Aquí encontrarás todo lo que necesitas saber como desarrollador web.
title: Aplicaciones web progresivas (EdgeHTML) en Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 87996f6be7c1963c01a476b307a31e689e3880d4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236272"
---
# Aplicaciones web progresivas (EdgeHTML) en Windows  

Con las [aplicaciones web progresivas][MDNApps] \(o simplemente PWAs \), no es necesario que decida entre usar tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionar a los usuarios una experiencia nativa de tipo aplicación personalizada para su dispositivo.  Esto se debe a que PWAs son solo sitios web que se han [mejorado progresivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicaciones nativas en plataformas compatibles.  Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.  

:::row:::
    :::column:::
        ![Icono de descubrimiento][ImageISearch]
        ### [Reconocible][MDNPwaAdvantagesDiscoverable]
        Desde los resultados de la búsqueda web y los almacenes de aplicaciones auxiliares
    :::column-end:::
    :::column:::
        ![Icono de instalación][ImageIPackage]
        ### [Instalables][MDNPwaAdvantagesInstallable]
        Anclar e iniciar desde la pantalla de inicio  
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
        Escala \(subir o bajar \) con capacidades de dispositivo  
    :::column-end:::
    :::column:::
        ![Icono de seguridad][ImageISecurity]
        ### [Seguros][MDNPwaAdvantagesSafe]
        Proporciona un punto de conexión HTTPS seguro y otras medidas de seguridad para el usuario  
    :::column-end:::
    :::column:::
        ![Icono de respuesta][ImageIResponsive]
        ### [Dinámica][MDNPwaAdvantagesResponsive]
        Se adapta al tamaño y la orientación de la pantalla del usuario y al método de entrada  
    :::column-end:::
    :::column:::
        ![Icono de vínculo][ImageILink]
        ### [Linkable][MDNPwaAdvantagesLinkable]
        Compartir e iniciar desde un hipervínculo estándar  
    :::column-end:::
:::row-end:::

Al crear o convertir el sitio existente en un PWA, puede integrar mejor el público existente con las notificaciones Push y con el soporte técnico sin conexión.  Al mismo tiempo, puede continuar con la creación de la audiencia en la web abierta, ya que los usuarios pueden descubrir su PWA mediante la búsqueda y el uso compartido de vínculos.  

## PWAs en Windows 10 (EdgeHTML)  

> [!NOTE]
> Con el movimiento a Microsoft Edge (cromo) desde EdgeHTML, las plataformas web subyacentes usadas por PWAs no son iguales.  Edge (cromo) PWAs se instalan desde el explorador y se ejecutan en él.  Edge (EdgeHTML) PWAs se ejecutan como aplicaciones para la plataforma universal de Windows (UWP) y usan la plataforma web de EdgeHTML anterior.  Si necesita acceso a la API de Windows 10 para su PWA, esta documentación de EdgeHTML es para usted.  Si su objetivo es la compatibilidad entre plataformas sin acceso específico a la API de Windows, visite la [documentación de PWA de Microsoft Edge (cromo)][PwaChromiumIndex].  

Al crear una aplicación web progresiva para aprovechar las ventajas de Windows 10, puede distribuir su PWA a través de [Microsoft Store][MicrosoftDeveloperStore], la base de instalación completa de Windows 10 de más de 600 millones de usuarios activos mensuales es la posible audiencia de la aplicación.  Las aplicaciones desarrolladas de esta manera se ejecutan como aplicaciones de la [plataforma universal de Windows][WindowsUWPGetStartedGuide] y tienen un nativo como acceso a las API de WinRT.  Ten en cuenta que la plataforma web que representa tu código es EdgeHTML al usar las API de WinRT, así que asegúrate de usar la detección de características antes de llamar a cualquier API específica de Windows para asegurarte de que tu PWA pueda ejecutarse a través de plataformas en las que esté disponible la PWAs de Microsoft Edge \(cromo \).  

[Aquí le mostramos cómo empezar][PwaEdgehtmlGetStarted] a convertir su aplicación web a un PWA \(EdgeHTML \), probarla en Windows 10 y distribuirlo en Microsoft Store.  

## Requisitos  

Para ejecutar como PWA, la aplicación web hospedada en el servidor requiere como mínimo:  

*   [Https][WikiHttps].  Proteja a los usuarios proporcionando una conexión segura para la comunicación entre servidores y aplicaciones.  Los trabajadores del servicio y otras tecnologías de PWA solo funcionan con recursos Web servidos a través de una conexión segura \(o de `localhost` para fines de depuración \).  
  
*   [Trabajadores del servicio][MDNServiceWorkerApi].  Use los subprocesos de trabajo de servicio para actuar como proxies de red entre su servidor y la aplicación cliente a fin de proporcionar compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones push, sincronización de datos en segundo plano y optimizaciones del rendimiento de carga de la página.  

*   [Manifiesto de la aplicación web][MDNWebAppManifest].  Proporcione un archivo de metadatos basado en JSON que describa la información clave de la aplicación web \(como iconos, idioma y punto de entrada de dirección URL \) para que Windows 10 y otras plataformas de hospedaje puedan proporcionar a los usuarios de PWA una experiencia de aplicación nativa y de instalación.  Asociar el sitio con un manifiesto de la aplicación web hace que sea apto para [la inclusión automática en Microsoft Store][PwaEdgehtmlMicrosoftStoreImportingBing] a través del servicio de indización de Bing.  

Para ser un fantástico PWA, tu aplicación también necesita:  

*   [Compatibilidad entre exploradores][MDNCrossBrowserTesting].  Asegúrese de que su PWA funciona [probando][MicrosoftDeveloperEdgeToolsRemote] en exploradores y entornos diferentes.  En Windows 10, asegúrese de probar la aplicación en el explorador Microsoft Edge y también en la experiencia de PWA completa, como una aplicación independiente instalada de Windows 10 \(con el motor de EdgeHTML \).  
  
*   [Diseño eficaz][WikiResponsiveWebDesign].  Use diseños fluidos y imágenes flexibles con CSS [Grid][MDNCssGridLayout] y/o [Flexbox][MDNCssFlexibleBoxLayout], [consultas de medios][MDNMediaQueries]y [imágenes receptivas[MDNResponsiveImages] para adaptar su UX al dispositivo del usuario.  Use [las herramientas de emulación][DevToolsGuideEmulation] de dispositivos de su explorador para probar de forma local o configure una [sesión de depuración remota][DevToolsProtocolClientsEdgeDevToolsPreview] para probar directamente en un dispositivo de destino.  En Windows 10, PWAs \(EdgeHTML \) también pueden adaptarse a los [factores de forma][WindowsUWPDesignDevicesIndex] más allá de los equipos de escritorio, teléfonos y tabletas, entre los que se incluyen: [Xbox y TV][WindowsUWPDesignDevicesDesigningTv], [Surface Hub][MicrosoftDeveloperWindowsSurfaceHub]y dispositivos [Windows Mixed Reality][MicrosoftDeveloperWindowsMixedReality] .  
  
*   [Vínculo en profundidad][WikiDeepLinking].  Enrute cada página de su sitio a una dirección URL única de modo que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia mediante el uso compartido de los medios sociales.  

*   [Procedimientos recomendados][Webhint].  Usa herramientas de calidad de código como [webhint][Webhint] pelusa para optimizar la eficacia, solidez, seguridad y accesibilidad de tu aplicación.  

Para enviar la aplicación web progresiva a [Microsoft Store][MicrosoftDeveloperStore], debe tener:  

*   Una [cuenta de Microsoft Developer][WindowsUWPPublishDeveloperAccount]  
*   Pasos completados [para publicar una aplicación de Windows][WindowsUWPPublishIndex]  

En los próximos meses, los PWAs de los [criterios específicos][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] de las reuniones Web se indexan automáticamente por el motor de búsqueda de Bing en Microsoft Store \(donde los desarrolladores pueden administrarlos directamente para la audiencia de Windows 10 \).  

Para obtener más información [, consulta PWAs (EdgeHTML) en Microsoft Store][PwaEdgehtmlMicrosoftStore] .  

## Disponibilidad actual  

Compatibilidad del motor de explorador para las llamadas de aplicaciones web progresivas para una serie de componentes de arquitectura, la más importante es la infraestructura de redes subyacente a la [API de Fetch][MDNFetchApi].  La compatibilidad de PWA en el motor de EdgeHTML se completó en la versión de Windows 10 1809.  Mejoras adicionales en los estándares web desde ese momento, no se incorporará al motor de EdgeHTML, por lo que debe asegurarse de ejecutar pruebas de compatibilidad y de usar la detección de características para realizar una reserva correcta si la característica que necesita no es compatible con PWA en la plataforma EdgeHTML.  

Para la próxima versión de Microsoft Edge \(cromo \) en 2020, la plataforma del explorador es totalmente compatible con estas características que funcionan en todos los dispositivos en los que se admite el explorador de cromo.  

Para EdgeHTML y Windows, este es el estado actual de las tecnologías PWA basadas en estándares:  

| Tecnología | Propósito | Disponibilidad | Notas de uso |  
|:--- |:--- |:--- |:--- |  
| [Manifiesto de la aplicación Web][MDNWebAppManifest] | Proporciona los metadatos de la aplicación al sistema operativo host para habilitar la instalación y promoción de la tienda de aplicaciones.  Necesario para PWAs en Microsoft Store.  | [En desarrollo][MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest] | Por ahora, puedes usar el creador de [PWA][|::ref1::|] para generar un manifiesto JSON compatible con el W3C y empaquetar tu aplicación para varias plataformas de sistemas operativos.  Para Windows, PWA Builder traduce el manifiesto de JSON en el `.appxmanifest` formato \(XML \) necesario para las aplicaciones de Windows 10.  |  
| [API de captura][MDNFetchApi] | Proporciona redes asincrónicas \(solicitudes, respuestas \) para los recursos de página |[EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /compilación 14393 + | La sintaxis de la [API de trabajo del servicio][MDNServiceWorkerApi] se basa en las API de red basadas en Fetch.  También puede usar [Fetch API][MDNFetchApi] más generalmente como una moderna alternativa a `XMLHttpRequest` .  |  
| [API de trabajo de servicio][MDNServiceWorkerApi] | Proporciona un modelo de aplicación web o proxy de red con funciones sin conexión, donde se ejecutan independientemente de las páginas Web.  | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /compilación 17133 + | Soporte experimental \(detrás `Enable Service Workers` de Flag \) enviado en EdgeHTML 16.  De forma predeterminada, en las compilaciones de 17 EdgeHTML.  |  
| [API de caché][MDNCache] | Proporciona un mecanismo de almacenamiento para pares de solicitud y respuesta de red | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /compilación 17133 + | Consulte la nota anterior [API de trabajo del servicio][MDNServiceWorkerApi] .  |  
| [API de inserción][MDNPushApi] | Permite a un trabajador de servicios suscribirse a las notificaciones push |[EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /compilación 17133 +| Consulte la nota anterior [API de trabajo del servicio][MDNServiceWorkerApi] .  Las aplicaciones de Windows 10 \(incluido PWAs \) requieren el [servicio de notificaciones de inserción de Windows \(WNS \)][WindowsUWPControlsPatternTilesNotificationsWns] para entregar notificaciones push, que admite la [API Push][MDNPushApi]de W3C.  |  
| [API de notificaciones][MDNNotificationsApi] | Permite a un trabajador de servicio mostrar una notificación del sistema al usuario tras el mensaje PUSH | [EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /compilación 14393 + | Las notificaciones Web de EdgeHTML están completamente integradas en el [centro de actividades][MicrosoftSupportWindowsNotificationSettings]de Windows 10, en el que los usuarios pueden administrar notificaciones de aplicaciones y establecer [horas de silencio][MicrosoftSupportWindowsFocusAssist].  |  
| [API de sincronización en segundo plano][MDNSyncManager] | Proporciona una API para notificar a un trabajador de servicio que el usuario ha vuelto a conectarse y programar eventos periódicos para sincronizar los datos locales con el servidor. | [En desarrollo][MicrosoftDeveloperEdgePlatformStatusBackgroundSync] | Por el momento, podrás usar la API de [WinRT BackgroundTask][WindowsUWPLaunchResumeBackgroundTasks] nativa para implementar tareas en segundo plano para tu PWA cuando se ejecute como una aplicación de Windows 10.  |  

Este es el estado actual del soporte técnico de Microsoft Store para PWAs en Windows 10:  

| Método de envío de la tienda | Estado | Detalles |  
|:--- |:--- |:--- |  
| Manual \(se inició el desarrollador \) | Disponible | Visite [PWAs (EdgeHTML) en la tienda de Microsoft][PwaEdgehtmlMicrosoftStore] para comenzar.  |  
| Automático \(indexado automáticamente con Bing \) | Próximamente | [Actualmente][WindowsBlogsWelcomingPWAsEdgeWindows] estamos intentando el proceso de incorporación de PWA con un subconjunto limitado de socios de aplicaciones.  En los próximos meses, Microsoft te agradece PWAs en la web estándar de Microsoft Store.  Consulte la [importación automática de PWA con Bing][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] para obtener más información sobre los requisitos de Microsoft Store para las listas de PWA generadas automáticamente.  |  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview-clientes de protocolo DevTools | Microsoft docs"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Emulación | Microsoft docs"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Novedades de EdgeHTML 17 | Microsoft docs"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Novedades de EdgeHTML 14 Microsoft docs"  
[PwaChromiumIndex]: ../../progressive-web-apps-chromium/index.md "Aplicaciones web progresivas (cromo) en Windows | Microsoft docs"  
[PwaEdgehtmlGetStarted]: ../progressive-web-apps/get-started.md "Introducción a las aplicaciones web progresivas (EdgeHTML) | Microsoft docs"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Aplicaciones web progresivas en Microsoft Store | Microsoft docs"
[PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Criterios para el envío automático: aplicaciones web progresivas en Microsoft Store | Microsoft docs"  
[PwaEdgehtmlMicrosoftStoreImportingBing]: ./microsoft-store.md#automatic-pwa-importing-with-bing "Importación automática de PWA con Bing-aplicaciones web progresivas (EdgeHTML) en Microsoft Store | Microsoft docs"  


[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Introducción a los servicios de notificaciones de inserción de Windows \(WNS \)"  
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
[]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imágenes de respuesta MDNResponsiveImages | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de la aplicación Web | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculación profunda: Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Diseño web con respuesta: Wikipedia"  
