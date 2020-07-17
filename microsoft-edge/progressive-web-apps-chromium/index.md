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
# <span data-ttu-id="b451f-105">Aplicaciones web progresivas en Windows</span><span class="sxs-lookup"><span data-stu-id="b451f-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="b451f-106">Con las [aplicaciones web progresivas][MDNApps] \ (o simplemente PWAs \), no tiene que decidir entre usar las tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionar a los usuarios una experiencia nativa de tipo aplicación personalizada para sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b451f-106">With [Progressive Web Apps][MDNApps] \(or simply PWAs\), you do not have to decide between using open web technologies for cross-platform interoperability and providing your users with a native app-like experience customized for their devices.</span></span>  <span data-ttu-id="b451f-107">PWAs son solo sitios web que se han [mejorado progresivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicaciones nativas en plataformas compatibles.</span><span class="sxs-lookup"><span data-stu-id="b451f-107">PWAs are just websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="b451f-108">Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.</span><span class="sxs-lookup"><span data-stu-id="b451f-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        ![Icono de descubrimiento][ImageISearch]
        ### [<span data-ttu-id="b451f-110">Reconocible</span><span class="sxs-lookup"><span data-stu-id="b451f-110">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="b451f-111">Desde los resultados de la búsqueda web y los almacenes de aplicaciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="b451f-111">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        ![Icono de instalación][ImageIPackage]
        ### [<span data-ttu-id="b451f-113">Instalables</span><span class="sxs-lookup"><span data-stu-id="b451f-113">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="b451f-114">Anclar e iniciar desde la pantalla principal, el menú Inicio, la barra de tareas, etc.</span><span class="sxs-lookup"><span data-stu-id="b451f-114">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        ![Icono volver a participar][ImageIPushNotification]
        ### [<span data-ttu-id="b451f-116">Reactivable</span><span class="sxs-lookup"><span data-stu-id="b451f-116">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="b451f-117">Enviar notificaciones push, incluso cuando la aplicación no está activa</span><span class="sxs-lookup"><span data-stu-id="b451f-117">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
    :::column:::
        ![Icono independiente de red][ImageIOffline]
        ### [<span data-ttu-id="b451f-119">Independiente de la red</span><span class="sxs-lookup"><span data-stu-id="b451f-119">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="b451f-120">Trabaja sin conexión y en condiciones de redes bajas</span><span class="sxs-lookup"><span data-stu-id="b451f-120">Works offline and in low-network conditions</span></span>
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Icono de progresivo][ImageIProgressive]
        ### [<span data-ttu-id="b451f-122">Reduci</span><span class="sxs-lookup"><span data-stu-id="b451f-122">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="b451f-123">Experiencia de ampliación (o de baja) con capacidades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b451f-123">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        ![Icono de seguridad][ImageISecurity]
        ### [<span data-ttu-id="b451f-125">Seguros</span><span class="sxs-lookup"><span data-stu-id="b451f-125">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="b451f-126">Proporciona un punto de conexión HTTPS seguro y otras medidas de seguridad para el usuario</span><span class="sxs-lookup"><span data-stu-id="b451f-126">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
    :::column:::
        ![Icono de respuesta][ImageIResponsive]
        ### [<span data-ttu-id="b451f-128">Dinámica</span><span class="sxs-lookup"><span data-stu-id="b451f-128">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="b451f-129">Se adapta al tamaño de la pantalla o a la orientación y el método de entrada del usuario</span><span class="sxs-lookup"><span data-stu-id="b451f-129">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        ![Icono de vínculo][ImageILink]
        ### [<span data-ttu-id="b451f-131">Linkable</span><span class="sxs-lookup"><span data-stu-id="b451f-131">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="b451f-132">Compartir e iniciar desde un hipervínculo estándar</span><span class="sxs-lookup"><span data-stu-id="b451f-132">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="b451f-133">Al crear o convertir el sitio existente en un PWA, usted se compromete mejor con su audiencia existente mediante notificaciones push, integración de tipo aplicación y soporte técnico sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b451f-133">By building or converting your existing site to a PWA, you engage better with your existing audience using push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="b451f-134">Al mismo tiempo, debe continuar con la creación de la audiencia en la web abierta, ya que los usuarios pueden descubrir su PWA mediante la búsqueda y el uso compartido de vínculos.</span><span class="sxs-lookup"><span data-stu-id="b451f-134">At the same time, you should continue to build your audience on the open web, as users discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="b451f-135">Lo mejor de todo es que puedes actualizar tu aplicación actualizando el código de tu servidor Web.</span><span class="sxs-lookup"><span data-stu-id="b451f-135">Best of all, you may update your app by simply updating your web server code.</span></span>  

## <span data-ttu-id="b451f-136">PWAs en Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="b451f-136">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="b451f-137">Al crear una aplicación web progresiva dirigida a las API de Web Standard, la aplicación puede implementarse en varias plataformas y dispositivos, y aprovechar las capacidades específicas del dispositivo según esté disponible.</span><span class="sxs-lookup"><span data-stu-id="b451f-137">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device specific capabilities as available.</span></span>  <span data-ttu-id="b451f-138">PWAs en Microsoft Edge \ (cromo \) se basa completamente en estándares desde una perspectiva de plataforma web y permite a los usuarios instalar la aplicación directamente desde el explorador sin necesidad de un registro o implementación basado en la tienda.</span><span class="sxs-lookup"><span data-stu-id="b451f-138">PWAs in Microsoft Edge \(Chromium\) are completely standards-based from a web platform perspective and enable users to install the app directly from within the browser without the need for Store-based deployment or registration.</span></span>  <span data-ttu-id="b451f-139">Los PWAs de escritorio son compatibles con cualquiera de las plataformas Microsoft Edge \ (cromo \) está disponible, incluidos Windows 7, Windows 10 y macOS.</span><span class="sxs-lookup"><span data-stu-id="b451f-139">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available, including Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="b451f-140">Otros beneficios son:</span><span class="sxs-lookup"><span data-stu-id="b451f-140">Other benefits include:</span></span>  

*   <span data-ttu-id="b451f-141">Las aplicaciones se pueden instalar directamente desde el explorador mediante el icono de **instalación** de la barra de navegación.</span><span class="sxs-lookup"><span data-stu-id="b451f-141">Applications may be installed directly from within the browser via the **Install** icon in the navigation bar.</span></span>  
    
    ![Instalar el control flotante y el icono de la aplicación][ImageInstallPwa]  
    
*   <span data-ttu-id="b451f-143">Las aplicaciones también pueden instalarse, ejecutarse y administrarse desde el menú de **Settings**  >  **aplicaciones** de configuración</span><span class="sxs-lookup"><span data-stu-id="b451f-143">Applications may also be installed, run and managed from the **Settings** > **Apps** menu</span></span>  
    
    ![Elementos de menú de la aplicación en configuración][ImageAppMenus]  

*   <span data-ttu-id="b451f-145">Las notificaciones web están integradas en el sistema de notificaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="b451f-145">Web Notifications are integrated into the Windows notification system</span></span>
*   <span data-ttu-id="b451f-146">Almacén de cookies compartido con el perfil de explorador que instaló la aplicación</span><span class="sxs-lookup"><span data-stu-id="b451f-146">Shared cookie store with the browser profile that installed the app</span></span>
*   <span data-ttu-id="b451f-147">Acceso a otras características del explorador mediante el `...` menú, como la validación de certificados, los permisos de sitio, la protección de rastreo y las extensiones de explorador</span><span class="sxs-lookup"><span data-stu-id="b451f-147">Access to other browser features via the `...` menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>
*   <span data-ttu-id="b451f-148">Acceso total a [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para la depuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b451f-148">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b451f-149">Para personalizar PWAs específicamente para Windows 10 que realizan solicitudes de API de WinRT con JavaScript, consulta la [documentación específica de las características de EDGEHTML PWA][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="b451f-149">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, see the [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="b451f-150">Obtenga más información sobre cómo probar su PWA en Windows 10 y cómo distribuirlo en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="b451f-150">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="b451f-151">Consulte la [sesión de compilación 2020 PWA][BuildVideo] para obtener información general sobre los beneficios de PWA, las próximas características y las demostraciones breves.</span><span class="sxs-lookup"><span data-stu-id="b451f-151">Check out the [Build 2020 PWA session][BuildVideo] for an overview of PWA benefits, upcoming features and short demos.</span></span> 

## <span data-ttu-id="b451f-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b451f-152">Requirements</span></span>  

<span data-ttu-id="b451f-153">Para ejecutar como PWA, la aplicación web hospedada por el servidor debe incluir los siguientes requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="b451f-153">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

| <span data-ttu-id="b451f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b451f-154">Requirement</span></span> | <span data-ttu-id="b451f-155">Detalles</span><span class="sxs-lookup"><span data-stu-id="b451f-155">Details</span></span> | 
|:--- |:--- |  
| [<span data-ttu-id="b451f-156">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b451f-156">HTTPS</span></span>][WikiHttps] | <span data-ttu-id="b451f-157">Proteger a los usuarios proporcionando una conexión segura para la comunicación entre servidores o aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b451f-157">Protect your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="b451f-158">Los trabajadores del servicio y otras tecnologías de PWA solo funcionan con recursos Web servidos a través de una conexión segura \ (o de `localhost` para fines de depuración \).</span><span class="sxs-lookup"><span data-stu-id="b451f-158">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  |  
| [<span data-ttu-id="b451f-159">Trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="b451f-159">Service Workers</span></span>][MDNServiceWorkerApi] | <span data-ttu-id="b451f-160">Use los subprocesos de trabajo de servicio para actuar como proxies de red entre su servidor y la aplicación cliente a fin de proporcionar compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones push, sincronización de datos en segundo plano y optimizaciones del rendimiento de carga de la página.</span><span class="sxs-lookup"><span data-stu-id="b451f-160">Use Service Worker threads to act as network proxies between your server and client app in order to provide offline support, resource caching, push notifications, background data sync, and  page load perf optimizations.</span></span>  |  
| [<span data-ttu-id="b451f-161">Manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="b451f-161">Web App Manifest</span></span>][MDNWebAppManifest] | <span data-ttu-id="b451f-162">Proporcione un archivo de metadatos basado en JSON que describa la información clave de la aplicación web \ (como iconos, idioma y punto de entrada de dirección URL \), para que Windows 10 y otras plataformas de hospedaje puedan proporcionar a los usuarios de PWA una experiencia de aplicación nativa, instalable y de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b451f-162">Provide a JSON-based metadata file describing key information about your web app \(such as icons, language, and URL entry point\), so that Windows 10 and other host platforms are able to provide your PWA users with an installable, native app-like experience.</span></span>  |  

<span data-ttu-id="b451f-163">Para ser un fantástico PWA, tu aplicación también debe cumplir con los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="b451f-163">To be a great PWA, your app must also meet the following requirements.</span></span>  

| <span data-ttu-id="b451f-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b451f-164">Requirement</span></span> | <span data-ttu-id="b451f-165">Detalles</span><span class="sxs-lookup"><span data-stu-id="b451f-165">Details</span></span> | 
|:--- |:--- |  
| [<span data-ttu-id="b451f-166">Compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="b451f-166">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting] | <span data-ttu-id="b451f-167">Asegúrese de que su PWA funciona [probando][MicrosoftDeveloperEdgeToolsRemote] en exploradores y entornos diferentes.</span><span class="sxs-lookup"><span data-stu-id="b451f-167">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  |  
| [<span data-ttu-id="b451f-168">Diseño adaptativo</span><span class="sxs-lookup"><span data-stu-id="b451f-168">Responsive design</span></span>][WikiResponsiveWebDesign] | <span data-ttu-id="b451f-169">Use diseños fluidos y imágenes flexibles con CSS [Grid][MDNCssGridLayout], [Flexbox][MDNCssFlexibleBoxLayout], CSS [Grid][MDNCssGridLayout] y [Flexbox][MDNCssFlexibleBoxLayout] , [consultas de medios][MDNMediaQueries]e [imágenes de respuesta][MDNResponsiveImages] para adaptar su UX al dispositivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="b451f-169">Employ fluid layouts and flexible images with CSS [grid][MDNCssGridLayout], [flexbox][MDNCssFlexibleBoxLayout], CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout] , [media queries][MDNMediaQueries], and [responsive images][MDNResponsiveImages] to adapt your UX to your user's device.</span></span>  <span data-ttu-id="b451f-170">Use [las herramientas de emulación de dispositivos][DevToolsGuide|::ref1::|] de su explorador para probar de forma local o configure una [sesión de depuración remota][DevToolsProtocolClientsEdgeDevToolsPreview] para probar directamente en un dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="b451f-170">Use [device emulation tools][DevToolsGuide|::ref1::|] from your browser to test locally, or set up a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>  |  
| [<span data-ttu-id="b451f-171">Vinculación profunda</span><span class="sxs-lookup"><span data-stu-id="b451f-171">Deep linking</span></span>][WikiDeepLinking] | <span data-ttu-id="b451f-172">Enrute cada página de su sitio a una dirección URL única de modo que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia mediante el uso compartido de los medios sociales.</span><span class="sxs-lookup"><span data-stu-id="b451f-172">Route each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  |  
| [<span data-ttu-id="b451f-173">Procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="b451f-173">Best practices</span></span>][Webhint] | <span data-ttu-id="b451f-174">Usa herramientas de calidad de código como [webhint][Webhint] pelusa para optimizar la eficacia, solidez, seguridad y accesibilidad de tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="b451f-174">Use code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  |  
| [<span data-ttu-id="b451f-175">Lista de comprobación de cromo PWA</span><span class="sxs-lookup"><span data-stu-id="b451f-175">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist] | <span data-ttu-id="b451f-176">Consulte su PWA con la lista de comprobación de Google Baseline PWA.</span><span class="sxs-lookup"><span data-stu-id="b451f-176">Check your PWA against the Google baseline PWA checklist.</span></span>  |  

<span data-ttu-id="b451f-177">Si quiere convertir su PWA en una aplicación de [Microsoft Store][MicrosoftDeveloperStore] , vaya a la documentación de las [aplicaciones web progresivas (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .</span><span class="sxs-lookup"><span data-stu-id="b451f-177">If you want to turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, head to the [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] documentation.</span></span>  
  

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
