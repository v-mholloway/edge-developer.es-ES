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
# <span data-ttu-id="f4ff8-105">Descripción general de las aplicaciones web progresivas en Windows</span><span class="sxs-lookup"><span data-stu-id="f4ff8-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="f4ff8-106">[Aplicaciones web progresivas][MDNApps] \ (PWAs \) proporcionan acceso a las tecnologías web abiertas para la interoperabilidad entre plataformas y proporcionan a los usuarios una experiencia nativa, como la aplicación personalizada para sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="f4ff8-107">PWAs son sitios web que se han [mejorado progresivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicaciones nativas en plataformas compatibles.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="f4ff8-108">Las cualidades de una PWA combinan lo mejor de las aplicaciones web y nativas.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [<span data-ttu-id="f4ff8-109">Reconocible</span><span class="sxs-lookup"><span data-stu-id="f4ff8-109">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="f4ff8-110">Desde los resultados de la búsqueda web y los almacenes de aplicaciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="f4ff8-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [<span data-ttu-id="f4ff8-111">Instalables</span><span class="sxs-lookup"><span data-stu-id="f4ff8-111">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="f4ff8-112">Anclar e iniciar desde la pantalla principal, el menú Inicio, la barra de tareas, etc.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [<span data-ttu-id="f4ff8-113">Reactivable</span><span class="sxs-lookup"><span data-stu-id="f4ff8-113">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="f4ff8-114">Enviar notificaciones push, incluso cuando la aplicación no está activa</span><span class="sxs-lookup"><span data-stu-id="f4ff8-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [<span data-ttu-id="f4ff8-115">Independiente de la red</span><span class="sxs-lookup"><span data-stu-id="f4ff8-115">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="f4ff8-116">Trabaja sin conexión y en condiciones de redes bajas</span><span class="sxs-lookup"><span data-stu-id="f4ff8-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [<span data-ttu-id="f4ff8-117">Reduci</span><span class="sxs-lookup"><span data-stu-id="f4ff8-117">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="f4ff8-118">Experiencia de ampliación (o de baja) con capacidades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f4ff8-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [<span data-ttu-id="f4ff8-119">Seguros</span><span class="sxs-lookup"><span data-stu-id="f4ff8-119">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="f4ff8-120">Proporciona un punto de conexión HTTPS seguro y otras medidas de seguridad para el usuario</span><span class="sxs-lookup"><span data-stu-id="f4ff8-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [<span data-ttu-id="f4ff8-121">Dinámica</span><span class="sxs-lookup"><span data-stu-id="f4ff8-121">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="f4ff8-122">Se adapta al tamaño de la pantalla o a la orientación y el método de entrada del usuario</span><span class="sxs-lookup"><span data-stu-id="f4ff8-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [<span data-ttu-id="f4ff8-123">Linkable</span><span class="sxs-lookup"><span data-stu-id="f4ff8-123">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="f4ff8-124">Compartir e iniciar desde un hipervínculo estándar</span><span class="sxs-lookup"><span data-stu-id="f4ff8-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="f4ff8-125">Cree \ (o convierta \) su sitio web existente en un PWA para mejorar su compromiso con los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="f4ff8-126">Las mejoras incluyen las notificaciones push, la integración como la aplicación y el soporte técnico sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="f4ff8-127">Continúe con la creación de la audiencia en la web abierta para que los usuarios puedan descubrir su PWA mediante la búsqueda y el uso compartido de vínculos.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="f4ff8-128">Y lo mejor de todo es que la aplicación se actualiza con el código de servidor Web.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-128">Best of all, your app is updated in using your web server code.</span></span>  

## <span data-ttu-id="f4ff8-129">PWAs en Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="f4ff8-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f4ff8-130">Cuando se crea una aplicación Web de acceso público orientada a las API estándar Web, la aplicación puede implementarse en todas las plataformas y dispositivos, y aprovechar las capacidades específicas del dispositivo según esté disponible.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-130">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="f4ff8-131">PWAs en Microsoft Edge \ (cromo \) agrega las siguientes ventajas a tu sitio Web.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="f4ff8-132">Tu aplicación se ha creado en una plataforma web basada en estándares.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="f4ff8-133">Permite a los usuarios instalar la aplicación directamente desde el explorador.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="f4ff8-134">Permite a los usuarios instalar la aplicación sin un registro o implementación basado en la tienda.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="f4ff8-135">Los PWAs de escritorio se admiten en cualquiera de las plataformas disponibles Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="f4ff8-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="f4ff8-136">Microsoft Edge \ (cromo \) está disponible en Windows 7, Windows 10 y macOS.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="f4ff8-137">Se incluyen los siguientes beneficios:</span><span class="sxs-lookup"><span data-stu-id="f4ff8-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="f4ff8-138">Las aplicaciones se pueden instalar directamente desde el explorador mediante el icono de **instalación** de la barra de navegación.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-138">Applications may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Instalar el control flotante y el icono de la aplicación" lightbox="./media/install_pwa_icon.png":::
       <span data-ttu-id="f4ff8-140">Instalar el control flotante y el icono de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f4ff8-140">Install application flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="f4ff8-141">Las aplicaciones también pueden instalarse, ejecutarse y administrarse \*\*\*\* desde el menú de  >  **aplicaciones** de configuración</span><span class="sxs-lookup"><span data-stu-id="f4ff8-141">Applications may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Elementos de menú de la aplicación en configuración" lightbox="./media/app_menus.png":::
       <span data-ttu-id="f4ff8-143">Elementos de menú de la aplicación en configuración</span><span class="sxs-lookup"><span data-stu-id="f4ff8-143">Application menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="f4ff8-144">Las notificaciones web están integradas en el sistema de notificaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="f4ff8-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="f4ff8-145">Almacén de cookies compartido con el perfil de explorador que instaló la aplicación</span><span class="sxs-lookup"><span data-stu-id="f4ff8-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="f4ff8-146">Acceso a otras características del explorador con la **configuración y más** el `...` menú \ (\), incluidos la validación de certificados, los permisos de sitio, la protección de rastreo y las extensiones de explorador</span><span class="sxs-lookup"><span data-stu-id="f4ff8-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="f4ff8-147">Acceso total a [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para la depuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f4ff8-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="f4ff8-148">Para personalizar PWAs específicamente para Windows 10 que realicen solicitudes de API de WinRT con JavaScript, vaya a [documentación específica para las características de EdgeHTML PWA] [PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="f4ff8-148">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, navigate to [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="f4ff8-149">Obtenga más información sobre cómo probar su PWA en Windows 10 y cómo distribuirlo en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-149">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="f4ff8-150">Para obtener más información sobre los beneficios de PWA, las próximas características y las demostraciones breves, vaya a la sesión de la [compilación 2020 PWA][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="f4ff8-150">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <span data-ttu-id="f4ff8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4ff8-151">Requirements</span></span>  

<span data-ttu-id="f4ff8-152">Para ejecutar como PWA, la aplicación web hospedada por el servidor debe incluir los siguientes requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-153">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f4ff8-153">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-154">Protege a los usuarios proporcionando una conexión segura para la comunicación entre servidores o aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-154">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="f4ff8-155">Los trabajadores del servicio y otras tecnologías de PWA solo funcionan con recursos Web servidos a través de una conexión segura \ (o de `localhost` para fines de depuración \).</span><span class="sxs-lookup"><span data-stu-id="f4ff8-155">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-156">Trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="f4ff8-156">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-157">Usa subprocesos de trabajo de servicio para actuar como servidores proxy de red entre la aplicación de servidor y la de cliente.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-157">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="f4ff8-158">Los subprocesos de trabajo del servicio proporcionan compatibilidad sin conexión, almacenamiento en caché de recursos, notificaciones push, sincronización de datos en segundo plano y optimizaciones de rendimiento de carga de página.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-158">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-159">Manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="f4ff8-159">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-160">Proporciona un archivo de metadatos basado en JSON que describe información clave sobre su aplicación web para que Windows 10 y otras plataformas de hospedaje ofrezcan a los usuarios de PWA una experiencia de aplicaciones nativas instalables.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-160">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="f4ff8-161">La información de clave incluye iconos, idiomas y el punto de entrada de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-161">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="f4ff8-162">Para ser un fantástico PWA, tu aplicación también debe cumplir con los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-162">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-163">Compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="f4ff8-163">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-164">Asegúrese de que su PWA funciona [probando][MicrosoftDeveloperEdgeToolsRemote] en exploradores y entornos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-164">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-165">Diseño adaptativo</span><span class="sxs-lookup"><span data-stu-id="f4ff8-165">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-166">Emplea diseños fluidos y imágenes flexibles.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-166">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="f4ff8-167">El diseño dinámico incluye los siguientes elementos que adaptan su UX al dispositivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-167">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="f4ff8-168">[Cuadrícula][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="f4ff8-168">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="f4ff8-169">Flexbox</span><span class="sxs-lookup"><span data-stu-id="f4ff8-169">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="f4ff8-170">[Cuadrícula][MDNCssGridLayout] CSS y [Flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="f4ff8-170">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="f4ff8-171">consultas de medios</span><span class="sxs-lookup"><span data-stu-id="f4ff8-171">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="f4ff8-172">imágenes con capacidad de respuesta</span><span class="sxs-lookup"><span data-stu-id="f4ff8-172">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="f4ff8-173">Usa [herramientas de emulación de dispositivos][DevToolsGuideDeviceModeTestingOtherBrowsers] de su explorador para probar localmente o crear una sesión de depuración remota en [Windows][DevtoolsRemoteDebuggingWindows] o [Android][DevtoolsRemoteDebuggingIndex] para probar directamente en un dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-173">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-174">Vinculación profunda</span><span class="sxs-lookup"><span data-stu-id="f4ff8-174">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-175">Dirige cada página del sitio a una dirección URL única de modo que los usuarios existentes puedan ayudarle a atraer a una audiencia aún más amplia mediante el uso compartido de los medios sociales.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-175">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-176">Prácticas de validación y pruebas</span><span class="sxs-lookup"><span data-stu-id="f4ff8-176">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-177">Usa herramientas de calidad de código como [webhint][Webhint] pelusa para optimizar la eficacia, solidez, seguridad y accesibilidad de tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-177">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="f4ff8-178">Lista de comprobación de cromo PWA</span><span class="sxs-lookup"><span data-stu-id="f4ff8-178">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f4ff8-179">Verifica su PWA con la lista de comprobación de la referencia de PWA de Google.</span><span class="sxs-lookup"><span data-stu-id="f4ff8-179">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="f4ff8-180">Para convertir su PWA en una aplicación de [Microsoft Store][MicrosoftDeveloperStore] , vaya a [aplicaciones web progresivas (EdgeHTML) en Microsoft Store] [PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="f4ff8-180">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <span data-ttu-id="f4ff8-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4ff8-181">See also</span></span>  

*   [<span data-ttu-id="f4ff8-182">PWAs de mitos</span><span class="sxs-lookup"><span data-stu-id="f4ff8-182">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="f4ff8-183">Una guía básica para la aplicación web progresiva</span><span class="sxs-lookup"><span data-stu-id="f4ff8-183">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="f4ff8-184">Publicaciones sin conexión con aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="f4ff8-184">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="f4ff8-185">Q&A DE PWA</span><span class="sxs-lookup"><span data-stu-id="f4ff8-185">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="f4ff8-186">Apuestas en la web</span><span class="sxs-lookup"><span data-stu-id="f4ff8-186">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="f4ff8-187">Asignar nombres a aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="f4ff8-187">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="f4ff8-188">Diseñar y crear una aplicación web progresiva sin un marco (parte 1)</span><span class="sxs-lookup"><span data-stu-id="f4ff8-188">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="f4ff8-189">Diseñar y crear una aplicación web progresiva sin un marco (parte 2)</span><span class="sxs-lookup"><span data-stu-id="f4ff8-189">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="f4ff8-190">Diseñar y crear una aplicación web progresiva sin un marco (parte 3)</span><span class="sxs-lookup"><span data-stu-id="f4ff8-190">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
