---
description: Las aplicaciones web progresivas (cromo) se ejecutan de forma nativa en Windows 10.  Aquí encontrarás todo lo que necesitas saber como desarrollador web.
title: Aplicaciones web progresivas en Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: a13f39dc3b3e0d47ad07b0e447556dc14093e71b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231219"
---
# Descripción general de las aplicaciones web progresivas en Windows  

[Aplicaciones web progresivas][MDNApps] \ (PWAs \) proporcionan acceso a las tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionan a los usuarios una experiencia nativa, como la aplicación personalizada para sus dispositivos.  PWAs son sitios web que se han [mejorado progresivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicaciones nativas en plataformas compatibles.  Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [Reconocible][MDNPwaAdvantagesDiscoverable]
        Desde los resultados de la búsqueda web y los almacenes de aplicaciones auxiliares
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [Instalables][MDNPwaAdvantagesInstallable]
        Anclar e iniciar desde la pantalla principal, el menú Inicio, la barra de tareas, etc.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [Reactivable][MDNPwaAdvantagesReEngageable]
        Enviar notificaciones push, incluso cuando la aplicación no está activa
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [Independiente de la red][MDNPwaAdvantagesNetworkIndependent]
        Trabaja sin conexión y en condiciones de redes bajas
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [Reduci][MDNPwaAdvantagesProgressive]
        Experiencia de ampliación (o de baja) con capacidades de dispositivo
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [Seguros][MDNPwaAdvantagesSafe]
        Proporciona un punto de conexión HTTPS seguro y otras medidas de seguridad para el usuario
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [Dinámica][MDNPwaAdvantagesResponsive]
        Se adapta al tamaño de la pantalla o a la orientación y el método de entrada del usuario
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [Linkable][MDNPwaAdvantagesLinkable]
        Compartir e iniciar desde un hipervínculo estándar
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Cree \ (o convierta \) su sitio web existente en un PWA para mejorar su compromiso con los usuarios.  Las mejoras incluyen las notificaciones push, la integración como la aplicación y el soporte técnico sin conexión.  Continúe con la creación de la audiencia en la web abierta para que los usuarios puedan descubrir su PWA mediante la búsqueda y el uso compartido de vínculos.  Y lo mejor de todo es que la aplicación se actualiza con el código de servidor Web.  

## PWAs en Microsoft Edge (cromo)  

Cuando se crea una aplicación Web de acceso público orientada a las API estándar Web, la aplicación puede implementarse en todas las plataformas y dispositivos, y aprovechar las capacidades específicas del dispositivo según esté disponible.  PWAs en Microsoft Edge \ (cromo \) agrega las siguientes ventajas a tu sitio Web.  

*   Tu aplicación se ha creado en una plataforma web basada en estándares.  
*   Permite a los usuarios instalar la aplicación directamente desde el explorador.  
*   Permite a los usuarios instalar la aplicación sin un registro o implementación basado en la tienda.  
    
Los PWAs de escritorio se admiten en cualquiera de las plataformas disponibles Microsoft Edge \ (cromo \). Microsoft Edge \ (cromo \) está disponible en Windows 7, Windows 10 y macOS.  Se incluyen los siguientes beneficios:  

*   Las aplicaciones se pueden instalar directamente desde el explorador mediante el icono de **instalación** de la barra de navegación.  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Instalar el control flotante y el icono de la aplicación" lightbox="./media/install_pwa_icon.png":::
       Instalar el control flotante y el icono de la aplicación  
    :::image-end:::  
    
*   Las aplicaciones también pueden instalarse, ejecutarse y administrarse **** desde el menú de  >  **aplicaciones** de configuración  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Elementos de menú de la aplicación en configuración" lightbox="./media/app_menus.png":::
       Elementos de menú de la aplicación en configuración  
    :::image-end:::  
    
*   Las notificaciones web están integradas en el sistema de notificaciones de Windows  
*   Almacén de cookies compartido con el perfil de explorador que instaló la aplicación  
*   Acceso a otras características del explorador con la **configuración y más** el `...` menú \ (\), incluidos la validación de certificados, los permisos de sitio, la protección de rastreo y las extensiones de explorador  
*   Acceso total a [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para la depuración de la aplicación  
    
> [!IMPORTANT]
> Para personalizar PWAs específicamente para Windows 10 que realicen solicitudes de API de WinRT con JavaScript, vaya a [documentación específica para las características de EdgeHTML PWA] [PwaEdgehtmlIndex].  Obtenga más información sobre cómo probar su PWA en Windows 10 y cómo distribuirlo en Microsoft Store.  

> [!NOTE]
> Para obtener más información sobre los beneficios de PWA, las próximas características y las demostraciones breves, vaya a la sesión de la [compilación 2020 PWA][BuildVideo]. 

## Requisitos  

Para ejecutar como PWA, la aplicación web hospedada por el servidor debe incluir los siguientes requisitos mínimos.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Protege a los usuarios proporcionando una conexión segura para la comunicación entre servidores o aplicaciones.  Los trabajadores del servicio y otras tecnologías de PWA solo funcionan con recursos Web servidos a través de una conexión segura \ (o de `localhost` para fines de depuración \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Trabajos de servicio][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Usa subprocesos de trabajo de servicio para actuar como servidores proxy de red entre la aplicación de servidor y la de cliente.  Los subprocesos de trabajo del servicio proporcionan compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones push, sincronización de datos en segundo plano y optimizaciones de rendimiento de carga de página.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Manifiesto de la aplicación Web][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Proporciona un archivo de metadatos basado en JSON que describe información clave sobre su aplicación web para que Windows 10 y otras plataformas de hospedaje ofrezcan a los usuarios de PWA una experiencia de aplicaciones nativas instalables.  La información de clave incluye iconos, idiomas y el punto de entrada de la dirección URL. 
   :::column-end:::
:::row-end:::  

Para ser un fantástico PWA, tu aplicación también debe cumplir con los siguientes requisitos.  

:::row:::
   :::column span="1":::
      [Compatibilidad entre exploradores][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Asegúrese de que su PWA funciona [probando][MicrosoftDeveloperEdgeToolsRemote] en exploradores y entornos diferentes.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Diseño adaptativo][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Emplea diseños fluidos y imágenes flexibles.  El diseño dinámico incluye los siguientes elementos que adaptan su UX al dispositivo del usuario.  
      
      *   [Cuadrícula][MDNCssGridLayout] CSS  
      *   [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [Cuadrícula][MDNCssGridLayout] CSS y [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [consultas de medios][MDNMediaQueries]  
      *   [imágenes con capacidad de respuesta][MDNResponsiveImages]  
      
      Usa [herramientas de emulación de dispositivos][DevToolsGuideDeviceModeTestingOtherBrowsers] de su explorador para probar localmente o crear una sesión de depuración remota en [Windows][DevtoolsRemoteDebuggingWindows] o [Android][DevtoolsRemoteDebuggingIndex] para probar directamente en un dispositivo de destino.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Vinculación profunda][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Dirige cada página del sitio a una dirección URL única de modo que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia mediante el uso compartido de los medios sociales.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Prácticas de validación y pruebas][Webhint]  
   :::column-end:::
   :::column span="2":::
      Usa herramientas de calidad de código como [webhint][Webhint] pelusa para optimizar la eficacia, solidez, seguridad y accesibilidad de tu aplicación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Lista de comprobación de cromo PWA][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Verifica su PWA con la lista de comprobación de la referencia de PWA de Google.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Para convertir su PWA en una aplicación de [Microsoft Store][MicrosoftDeveloperStore] , vaya a [aplicaciones web progresivas (EdgeHTML) en Microsoft Store] [PwaEdgehtmlMicrosoftStore].  
  
## Consulte también  

*   [PWAs de mitos][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Una guía básica para la aplicación web progresiva][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Publicaciones sin conexión con aplicaciones web progresivas][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [Q&A DE PWA][AaronGustafsonNotebookPwaQa]  
*   [Apuestas en la web][JoretegBlogBettingWeb]  
*   [Asignar nombres a aplicaciones web progresivas][Fberriman20170626NamingProgressiveWebApps]  
*   [Diseñar y crear una aplicación web progresiva sin un marco (parte 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Diseñar y crear una aplicación web progresiva sin un marco (parte 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Diseñar y crear una aplicación web progresiva sin un marco (parte 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introducción a la depuración remota dispositivos con Windows 10 | Microsoft docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emular y probar otros exploradores | Microsoft docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Depurar aplicaciones web progresivas | Microsoft docs"  
<!--[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "What's new in EdgeHTML 17 | Microsoft Docs"  -->  
<!--[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "What's New in EdgeHTML 14 | Microsoft Docs"  -->  
[PwaEdgehtmlIndex]: .. /edgehtml/Progressive-Web-Apps/index.MD "aplicaciones web progresivas (EdgeHTML) en Windows | Microsoft docs "  
[PwaEdgehtmlMicrosoftStore]: .. /edgehtml/Progressive-Web-Apps/Microsoft-Store.MD "aplicaciones web progresivas en Microsoft Store | Microsoft docs "
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Información general de los servicios de notificaciones de inserción de Windows (WNS) | Microsoft docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Diseño para Xbox y TV | Microsoft docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Consideraciones sobre la interfaz de usuario para dispositivos para UWP | Microsoft docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "¿Qué es una aplicación para la plataforma universal de Windows (UWP)? | Microsoft docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Admitir la aplicación con tareas en segundo plano | Microsoft docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publicar aplicaciones y juegos de Windows | Microsoft docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Abrir una cuenta de desarrollador | Microsoft docs"  

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

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "Q&A DE PWA"  

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

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Una guía básica para la aplicación web progresiva"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs de mitos: la nueva edición de Edge"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Asignar nombres a aplicaciones web progresivas"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Apuestas en la web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Publicaciones sin conexión con aplicaciones web progresivas"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Diseñar y crear una aplicación web progresiva sin un marco (parte 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Diseñar y crear una aplicación web progresiva sin un marco (parte 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Diseñar y crear una aplicación web progresiva sin un marco (parte 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "¿Qué es una buena aplicación web progresiva? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculación profunda: Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Diseño web con respuesta: Wikipedia"  
