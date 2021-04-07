---
description: Las aplicaciones web progresivas (Chromium) se ejecutan de forma nativa en Windows 10.  Este es todo lo que necesita saber como desarrollador web.
title: Aplicaciones web progresivas en Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: be832ee5c0ad395dae7b4946c41da157ab5cd9ba
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480191"
---
# <a name="progressive-web-apps-on-windows-overview"></a>Introducción a Las aplicaciones web progresivas en Windows  

[Las aplicaciones web][MDNApps] progresivas \(PWAs\) proporcionan acceso a tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionan a los usuarios una experiencia nativa y parecida a una aplicación personalizada para sus dispositivos.  Las PWA son sitios web que se [mejoran progresivamente][AListApartUnderstandingProgressiveEnhancement] para que funcionen como aplicaciones nativas en plataformas de soporte técnico.  Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a>[Detectable][MDNPwaAdvantagesDiscoverable]
        Desde resultados de búsqueda web y almacenes de aplicaciones compatibles
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::
        ### <a name="installablemdnpwaadvantagesinstallable"></a>[Instalable][MDNPwaAdvantagesInstallable]
        Anclar e iniciar desde la pantalla principal, menú Inicio, barra de tareas, y así sucesivamente
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a>[Reenganable][MDNPwaAdvantagesReEngageable]
        Enviar notificaciones de inserción, incluso cuando la aplicación no está activa
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a>[Independiente de red][MDNPwaAdvantagesNetworkIndependent]
        Funciona sin conexión y en condiciones de red baja
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a>[Progresivo][MDNPwaAdvantagesProgressive]
        La experiencia escala hacia arriba (o hacia abajo) con funcionalidades de dispositivo
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::
        ### <a name="safemdnpwaadvantagessafe"></a>[Seguro][MDNPwaAdvantagesSafe]
        Proporciona un punto de conexión HTTPS seguro y otras protecciones de usuario
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a>[Dinámica][MDNPwaAdvantagesResponsive]
        Se adapta al tamaño de pantalla u orientación del usuario y al método de entrada
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::
        ### <a name="linkablemdnpwaadvantageslinkable"></a>[Vinculable][MDNPwaAdvantagesLinkable]
        Compartir e iniciar desde un hipervínculo estándar
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Cree \(o convert\) su sitio web existente en una PWA para mejorar su interacción con los usuarios.  Las mejoras incluyen notificaciones de inserción, integración como aplicaciones y compatibilidad sin conexión.  Siga construyendo su audiencia en la web abierta para que los usuarios descubran su PWA a través de la búsqueda y el uso compartido de vínculos.  Lo mejor de todo es que la aplicación se actualiza con el código del servidor web.  

## <a name="pwas-on-microsoft-edge-chromium"></a>PWAs en Microsoft Edge (Chromium)  

Al crear una API estándar web de aplicación web progresiva, es posible que la aplicación se implemente en plataformas y dispositivos y aproveche las capacidades específicas del dispositivo según esté disponible.  Las PWA de Microsoft Edge \(Chromium\) agregan las siguientes ventajas a su sitio web.  

*   La aplicación se basa en una plataforma web basada en estándares.  
*   Permite a los usuarios instalar la aplicación directamente desde el explorador.  
*   Permite a los usuarios instalar la aplicación sin una implementación o registro basado en la Tienda.  
    
Las PWA de escritorio se admiten en cualquiera de las plataformas que Microsoft Edge \(Chromium\) está disponible. Microsoft Edge \(Chromium\) está disponible en Windows 7, Windows 10 y macOS.  Se incluyen las siguientes ventajas.  

*   Las aplicaciones se pueden instalar directamente desde el explorador mediante el **icono Instalar** en la barra de navegación.  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Instalar el icono y el menú desplegable de la aplicación" lightbox="./media/install-progressive-web-app-icon.png":::
       Instalar el icono y el menú desplegable de la aplicación  
    :::image-end:::  
    
*   Las aplicaciones también pueden instalarse, ejecutarse y administrarse desde el **menú Aplicaciones**  >  **de** configuración  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="Elementos de menú de la aplicación en configuración" lightbox="./media/app-menus.png":::
       Elementos de menú de la aplicación en configuración  
    :::image-end:::  
    
*   Las notificaciones web están integradas en el sistema de notificaciones de Windows  
*   Almacén de cookies compartido con el perfil del explorador que instaló la aplicación  
*   Acceso a otras características del explorador mediante el menú **Configuración** y más \( \) que incluye validación de certificados, permisos de sitio, protección de seguimiento y extensiones `...` de explorador  
*   Acceso total a [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para depurar la aplicación  
    
> [!NOTE]
> Para obtener más información sobre las ventajas de PWA, las próximas características y las demostraciones breves, vaya a [La compilación 2020 sesión de PWA][BuildVideo]. 

## <a name="requirements"></a>Requisitos  

Para ejecutarse como PWA, la aplicación web hospedada en el servidor debe incluir los siguientes requisitos mínimos.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Protege a los usuarios proporcionando una conexión segura para la comunicación de aplicaciones o servidores.  Los trabajadores de servicio y otras tecnologías de PWA solo funcionan con recursos web que se sirven a través de una conexión segura \(o desde `localhost` para fines de depuración\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Trabajos de servicio][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Usa subprocesos de trabajo de servicio para actuar como servidores proxy de red entre el servidor y la aplicación cliente.  Los subprocesos de trabajo de servicio proporcionan compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones de inserción, sincronización de datos en segundo plano y optimizaciones de rendimiento de carga de página.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Manifiesto de aplicación web][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Proporciona un archivo de metadatos basado en JSON que describe información clave sobre la aplicación web, de modo que Windows 10 y otras plataformas host proporcionan a los usuarios de PWA una experiencia de aplicación nativa instalable.  La información clave incluye iconos, idioma y punto de entrada de dirección URL. 
   :::column-end:::
:::row-end:::  

Para ser un gran PWA, la aplicación también debe cumplir los siguientes requisitos.  

:::row:::
   :::column span="1":::
      [Compatibilidad entre exploradores][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Asegúrese de que su PWA funciona [mediante pruebas][MicrosoftDeveloperEdgeToolsRemote] en diferentes exploradores y entornos.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Diseño adaptativo][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Emplea diseños fluidos e imágenes flexibles.  El diseño dinámico incluye los siguientes elementos que adaptan la experiencia de usuario al dispositivo del usuario.  
      
      *   Cuadrícula [][MDNCssGridLayout] CSS  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   Cuadrícula [][MDNCssGridLayout] CSS y [flexbox][MDNCssFlexibleBoxLayout]  
      *   [consultas multimedia][MDNMediaQueries]  
      *   [imágenes con capacidad de respuesta][MDNResponsiveImages]  
      
      Usa [herramientas de emulación][DevToolsGuideDeviceModeTestingOtherBrowsers] de dispositivos desde el explorador para probar localmente o crear una sesión de depuración remota en [Windows][DevtoolsRemoteDebuggingWindows] o [Android][DevtoolsRemoteDebuggingIndex] para probar directamente en un dispositivo de destino.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Vinculación profunda][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Enruta cada página del sitio a una dirección URL única para que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia a través del uso compartido de redes sociales.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Prácticas de validación y pruebas][Webhint]  
   :::column-end:::
   :::column span="2":::
      Usa herramientas de calidad de código como [webhint][Webhint] linter para optimizar la eficacia, la solidez, la seguridad y la accesibilidad de la aplicación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Lista de comprobación de PWA de Chromium][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Comprueba tu PWA con la lista de comprobación de PWA de línea base de Google.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Para convertir tu PWA en una [aplicación de Microsoft Store,][MicrosoftDeveloperStore] ve a [Aplicaciones web progresivas en la Microsoft Store][PwaChromiumMicrosoftStore].  
  
## <a name="see-also"></a>Consulte también  

*   [PwAs de descomisado de mitos][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Una guía básica progresiva para la aplicación web progresiva][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [POST sin conexión con aplicaciones web progresivas][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Apuestas en la Web][JoretegBlogBettingWeb]  
*   [Nomenclatura de aplicaciones web progresivas][Fberriman20170626NamingProgressiveWebApps]  
*   [Diseño y creación de una aplicación web progresiva sin marco (parte 1)][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [Diseño y creación de una aplicación web progresiva sin marco (parte 2)][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [Diseño y creación de una aplicación web progresiva sin marco (parte 3)][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introducción a la depuración remota de dispositivos Windows 10 | Microsoft Docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emular y probar otros exploradores | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Depurar aplicaciones web progresivas | Microsoft Docs"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Publicar la aplicación web progresiva en microsoft store | Microsoft Docs"



[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Información general Notification Services Windows Push (WNS) | Microsoft Docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Diseño para Xbox y tv | Microsoft Docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Consideraciones de la interfaz de usuario para dispositivos para UWP | Microsoft Docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "¿Qué es una aplicación para la Plataforma universal de Windows (UWP) | Microsoft Docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Admite la aplicación con tareas en segundo plano | Microsoft Docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publicar aplicaciones y juegos de Windows | Microsoft Docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Abrir una cuenta de desarrollador | Microsoft Docs"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Dar la bienvenida a las aplicaciones web progresivas para Microsoft Edge y Windows 10: blogs de Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de sincronización en segundo plano: estado de la plataforma Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifiesto de aplicación web: estado de la plataforma Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Pruebas instantáneas"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Realidad mixta para desarrolladores"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador de Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Activar o desactivar la ayuda de foco en Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Cambiar la configuración de notificaciones en Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Descripción de la mejora progresiva: una lista aparte"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "aplicaciones | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Pruebas entre exploradores | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Diseño de cuadro flexible CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Css Grid Layout | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Recuperación de api | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Consultas multimedia | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notificaciones API | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Api de inserción | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Detectable: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Instalable: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Vinculable: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Independiente de la red: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Progresiva: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Volver a interactuar: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Responsive: ventajas de la aplicación web progresiva"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Seguro: ventajas de la aplicación web progresiva"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imágenes dinámicas | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de trabajo de servicio | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de aplicación web | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Vídeo de PWA"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Una guía básica progresiva para la aplicación web progresiva"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PwAs de descomisado de mitos: la nueva edición perimetral"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Nomenclatura de aplicaciones web progresivas"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Apuestas en la Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "POST sin conexión con aplicaciones web progresivas"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Diseño y creación de una aplicación web progresiva sin marco (parte 1)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Diseño y creación de una aplicación web progresiva sin marco (parte 2)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Diseño y creación de una aplicación web progresiva sin un marco (parte 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "¿Qué hace que una aplicación web progresiva sea | web.dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculación profunda - Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS - Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Diseño web dinámico - Wikipedia"  
