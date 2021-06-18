---
description: Las aplicaciones web progresivas (Chromium) se ejecutan de forma nativa en Windows 10.  Este es todo lo que necesita saber como desarrollador web.
title: Aplicaciones web progresivas en Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 47c6f98329a1da67e0f2c1a8e6243250992fb599
ms.sourcegitcommit: f4488cf2dfef0aeec04712b2ed933d68b8e93a94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "11608842"
---
# <a name="progressive-web-apps-on-windows-overview"></a><span data-ttu-id="3c1bf-105">Introducción a Las aplicaciones web progresivas en Windows</span><span class="sxs-lookup"><span data-stu-id="3c1bf-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="3c1bf-106">[Las aplicaciones web][MDNApps] progresivas \(PWAs\) proporcionan acceso a tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionan a los usuarios una experiencia nativa y parecida a una aplicación personalizada para sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span> <span data-ttu-id="3c1bf-107">Las PWA son sitios web que se [mejoran progresivamente][AListApartUnderstandingProgressiveEnhancement] para que funcionen como aplicaciones nativas en plataformas de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span> <span data-ttu-id="3c1bf-108">Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a><span data-ttu-id="3c1bf-109">[Detectable][MDNPwaAdvantagesDiscoverable]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a><span data-ttu-id="3c1bf-110">[Instalable][MDNPwaAdvantagesInstallable]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-110">[Installable][MDNPwaAdvantagesInstallable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a><span data-ttu-id="3c1bf-111">[Reenganable][MDNPwaAdvantagesReEngageable]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-111">[Re-engageable][MDNPwaAdvantagesReEngageable]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="3c1bf-112">Desde resultados de búsqueda web y almacenes de aplicaciones compatibles</span><span class="sxs-lookup"><span data-stu-id="3c1bf-112">From web search results and supporting app stores</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="3c1bf-113">Anclar e iniciar desde la pantalla principal, menú Inicio, barra de tareas, y así sucesivamente</span><span class="sxs-lookup"><span data-stu-id="3c1bf-113">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="3c1bf-114">Enviar notificaciones de inserción, incluso cuando la aplicación no está activa</span><span class="sxs-lookup"><span data-stu-id="3c1bf-114">Send push notifications, even when the app is not active</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a><span data-ttu-id="3c1bf-115">[Independiente de red][MDNPwaAdvantagesNetworkIndependent]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-115">[Network Independent][MDNPwaAdvantagesNetworkIndependent]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a><span data-ttu-id="3c1bf-116">[Progresivo][MDNPwaAdvantagesProgressive]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-116">[Progressive][MDNPwaAdvantagesProgressive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a><span data-ttu-id="3c1bf-117">[Seguro][MDNPwaAdvantagesSafe]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-117">[Safe][MDNPwaAdvantagesSafe]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="3c1bf-118">Funciona sin conexión y en condiciones de red baja</span><span class="sxs-lookup"><span data-stu-id="3c1bf-118">Works offline and in low-network conditions</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="3c1bf-119">La experiencia escala hacia arriba (o hacia abajo) con funcionalidades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c1bf-119">Experience scales up (or down) with device capabilities</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="3c1bf-120">Proporciona un punto de conexión HTTPS seguro y otras protecciones de usuario</span><span class="sxs-lookup"><span data-stu-id="3c1bf-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a><span data-ttu-id="3c1bf-121">[Dinámica][MDNPwaAdvantagesResponsive]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-121">[Responsive][MDNPwaAdvantagesResponsive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a><span data-ttu-id="3c1bf-122">[Vinculable][MDNPwaAdvantagesLinkable]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-122">[Linkable][MDNPwaAdvantagesLinkable]</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="3c1bf-123">Se adapta al tamaño de pantalla u orientación del usuario y al método de entrada</span><span class="sxs-lookup"><span data-stu-id="3c1bf-123">Adapts to the user's screen size or orientation and input method</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="3c1bf-124">Compartir e iniciar desde un hipervínculo estándar</span><span class="sxs-lookup"><span data-stu-id="3c1bf-124">Share and launch from a standard hyperlink</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="3c1bf-125">Cree \(o convertir\) su sitio web existente en una PWA para mejorar la interacción con los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-125">Build \(or convert\) your existing website to a PWA to enhance engagement with your users.</span></span> <span data-ttu-id="3c1bf-126">Las mejoras incluyen notificaciones de inserción, integración como aplicaciones y compatibilidad sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-126">Enhancements include push notifications, app-like integration, and offline support.</span></span> <span data-ttu-id="3c1bf-127">Siga construyendo su audiencia en la web abierta para que los usuarios descubran su PWA a través de la búsqueda y el uso compartido de vínculos.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span> <span data-ttu-id="3c1bf-128">Lo mejor de todo es que la aplicación se actualiza con el código del servidor web.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-128">Best of all, your app is updated using your web server code.</span></span>  

## <a name="pwas-on-microsoft-edge-chromium"></a><span data-ttu-id="3c1bf-129">PWAs en Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="3c1bf-130">Al crear una API estándar web de aplicación web progresiva, es posible que la aplicación se implemente en plataformas y dispositivos y aproveche las capacidades específicas del dispositivo según esté disponible.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-130">When you build a Progressive Web App targeting web standard APIs, your app may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span> <span data-ttu-id="3c1bf-131">Las PWA de Microsoft Edge \(Chromium\) agregan las siguientes ventajas a su sitio web.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="3c1bf-132">La aplicación se basa en una plataforma web basada en estándares.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="3c1bf-133">Permite a los usuarios instalar la aplicación directamente desde el explorador.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-133">Allows your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="3c1bf-134">Permite a los usuarios instalar la aplicación sin una implementación o registro basado en la Tienda.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-134">Allows your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="3c1bf-135">Las PWA de escritorio se admiten en cualquiera de las plataformas en las que Microsoft Edge \(Chromium\) está [disponible.](https://www.microsoft.com/edge)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is [available](https://www.microsoft.com/edge).</span></span> <span data-ttu-id="3c1bf-136">Se incluyen las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-136">The following benefits are included.</span></span>

*   <span data-ttu-id="3c1bf-137">Las aplicaciones se pueden instalar directamente desde el explorador mediante el **icono Instalar** en la barra de navegación.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-137">Apps may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Instalar el icono y el menú desplegable de la aplicación" lightbox="./media/install-progressive-web-app-icon.png":::
       <span data-ttu-id="3c1bf-139">Instalar el icono y el menú desplegable de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3c1bf-139">Install app flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="3c1bf-140">Las aplicaciones también pueden instalarse, ejecutarse y administrarse desde el **menú Aplicaciones**  >  **de** configuración</span><span class="sxs-lookup"><span data-stu-id="3c1bf-140">Apps may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="Elementos de menú de la aplicación en configuración" lightbox="./media/app-menus.png":::
       <span data-ttu-id="3c1bf-142">Elementos de menú de la aplicación en configuración</span><span class="sxs-lookup"><span data-stu-id="3c1bf-142">App menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="3c1bf-143">Las notificaciones web están integradas en el sistema de notificaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="3c1bf-143">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="3c1bf-144">Almacén de cookies compartido con el perfil del explorador que instaló la aplicación</span><span class="sxs-lookup"><span data-stu-id="3c1bf-144">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="3c1bf-145">Acceso a otras características del explorador mediante el menú **Configuración** y más \( \) que incluye validación de certificados, permisos de sitio, protección de seguimiento y extensiones `...` de explorador</span><span class="sxs-lookup"><span data-stu-id="3c1bf-145">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="3c1bf-146">Acceso total a [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para depurar la aplicación</span><span class="sxs-lookup"><span data-stu-id="3c1bf-146">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!NOTE]
> <span data-ttu-id="3c1bf-147">Para obtener más información sobre las ventajas de PWA, las próximas características y las demostraciones breves, vaya a [La compilación 2020 sesión de PWA][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="3c1bf-147">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <a name="requirements"></a><span data-ttu-id="3c1bf-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c1bf-148">Requirements</span></span>  

<span data-ttu-id="3c1bf-149">Para ejecutarse como PWA, la aplicación web hospedada en el servidor debe incluir los siguientes requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-149">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-150">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3c1bf-150">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-151">Protege a los usuarios proporcionando una conexión segura para la comunicación de aplicaciones o servidores.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-151">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="3c1bf-152">Los trabajadores de servicio y otras tecnologías de PWA solo funcionan con recursos web que se sirven a través de una conexión segura \(o desde `localhost` para fines de depuración\).</span><span class="sxs-lookup"><span data-stu-id="3c1bf-152">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-153">Trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="3c1bf-153">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-154">Usa subprocesos de trabajo de servicio para actuar como servidores proxy de red entre el servidor y la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-154">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="3c1bf-155">Los subprocesos de trabajo de servicio proporcionan compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones de inserción, sincronización de datos en segundo plano y optimizaciones de rendimiento de carga de página.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-155">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-156">Manifiesto de aplicación web</span><span class="sxs-lookup"><span data-stu-id="3c1bf-156">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-157">Proporciona un archivo de metadatos basado en JSON que describe información clave sobre la aplicación web, de modo que Windows 10 y otras plataformas host proporcionan a los usuarios de PWA una experiencia de aplicación nativa instalable.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-157">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="3c1bf-158">La información clave incluye iconos, idioma y punto de entrada de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-158">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3c1bf-159">Para ser un gran PWA, la aplicación también debe cumplir los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-159">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-160">Compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="3c1bf-160">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-161">Asegúrese de que su PWA funciona [mediante pruebas][MicrosoftDeveloperEdgeToolsRemote] en diferentes exploradores y entornos.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-161">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-162">Diseño adaptativo</span><span class="sxs-lookup"><span data-stu-id="3c1bf-162">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-163">Emplea diseños fluidos e imágenes flexibles.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-163">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="3c1bf-164">El diseño dinámico incluye los siguientes elementos que adaptan la experiencia de usuario al dispositivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-164">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="3c1bf-165">Cuadrícula [][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="3c1bf-165">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="3c1bf-166">flexbox</span><span class="sxs-lookup"><span data-stu-id="3c1bf-166">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="3c1bf-167">Cuadrícula [][MDNCssGridLayout] CSS y [flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="3c1bf-167">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="3c1bf-168">consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="3c1bf-168">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="3c1bf-169">imágenes con capacidad de respuesta</span><span class="sxs-lookup"><span data-stu-id="3c1bf-169">responsive images</span></span>][MDNResponsiveImages]  
          
      <span data-ttu-id="3c1bf-170">Usa [herramientas de emulación][DevToolsGuideDeviceModeTestingOtherBrowsers] de dispositivos desde el explorador para probar localmente o crear una sesión de depuración remota en [Windows][DevtoolsRemoteDebuggingWindows] o [Android][DevtoolsRemoteDebuggingIndex] para probar directamente en un dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-170">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-171">Vinculación profunda</span><span class="sxs-lookup"><span data-stu-id="3c1bf-171">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-172">Enruta cada página del sitio a una dirección URL única para que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia a través del uso compartido de redes sociales.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-172">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-173">Prácticas de validación y pruebas</span><span class="sxs-lookup"><span data-stu-id="3c1bf-173">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-174">Usa herramientas de calidad de código como [webhint][Webhint] linter para optimizar la eficacia, la solidez, la seguridad y la accesibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-174">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="3c1bf-175">Lista de comprobación de PWA de Chromium</span><span class="sxs-lookup"><span data-stu-id="3c1bf-175">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3c1bf-176">Comprueba tu PWA con la lista de comprobación de PWA de línea base de Google.</span><span class="sxs-lookup"><span data-stu-id="3c1bf-176">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="3c1bf-177">Para convertir tu PWA en una [aplicación de Microsoft Store,][MicrosoftDeveloperStore] ve a [Aplicaciones web progresivas en la Microsoft Store][PwaChromiumMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="3c1bf-177">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] app, navigate to [Progressive Web Apps in the Microsoft Store][PwaChromiumMicrosoftStore].</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c1bf-178">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3c1bf-178">See also</span></span>  

*   [<span data-ttu-id="3c1bf-179">PwAs de descomisado de mitos</span><span class="sxs-lookup"><span data-stu-id="3c1bf-179">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="3c1bf-180">Una guía básica progresiva para la aplicación web progresiva</span><span class="sxs-lookup"><span data-stu-id="3c1bf-180">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="3c1bf-181">POST sin conexión con aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="3c1bf-181">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="3c1bf-182">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="3c1bf-182">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="3c1bf-183">Apuestas en la Web</span><span class="sxs-lookup"><span data-stu-id="3c1bf-183">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="3c1bf-184">Nomenclatura de aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="3c1bf-184">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="3c1bf-185">Diseño y creación de una aplicación web progresiva sin marco (parte 1)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-185">Designing And Building A Progressive Web App Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [<span data-ttu-id="3c1bf-186">Diseño y creación de una aplicación web progresiva sin marco (parte 2)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-186">Designing And Building A Progressive Web App Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [<span data-ttu-id="3c1bf-187">Diseño y creación de una aplicación web progresiva sin marco (parte 3)</span><span class="sxs-lookup"><span data-stu-id="3c1bf-187">Designing And Building A Progressive Web App Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
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
