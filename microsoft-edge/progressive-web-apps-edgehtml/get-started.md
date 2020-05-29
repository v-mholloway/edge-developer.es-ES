---
description: Esta guía le ofrece información general sobre los conceptos básicos de PWA y herramientas para crear aplicaciones web progresivas en Windows.
title: Introducción a las aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto Web, trabajo de servicio, inserción
ms.openlocfilehash: 4d7b571b83048f9ce271f451a7537027bb92eebc
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583787"
---
# <span data-ttu-id="feaa8-104">Introducción a las aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="feaa8-104">Get started with Progressive Web Apps</span></span>  

<span data-ttu-id="feaa8-105">Las aplicaciones web progresivas \ (PWAs \) son simplemente aplicaciones web que se han [mejorado progresivamente][WikiProgressiveEnhancement] con características nativas de tipo aplicación en plataformas de soporte y motores de explorador, como la instalación de inicio desde pantalla Android, la compatibilidad sin conexión y las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="feaa8-105">Progressive Web Apps \(PWAs\) are simply web apps that are [progressively enhanced][WikiProgressiveEnhancement] with native app-like features on supporting platforms and browser engines, such as launch-from-homescreen installation, offline support, and push notifications.</span></span>  <span data-ttu-id="feaa8-106">En Windows 10 con el motor Microsoft Edge \ (EdgeHTML \), PWAs disfruta de la ventaja agregada de ejecutar independientemente la ventana del explorador como aplicaciones para la [plataforma universal de Windows][WindowsUwpGetStartedWhat] .</span><span class="sxs-lookup"><span data-stu-id="feaa8-106">On Windows 10 with the Microsoft Edge \(EdgeHTML\) engine, PWAs enjoy the added advantage of running independently of the browser window as [Universal Windows Platform][WindowsUwpGetStartedWhat] apps.</span></span>  

<span data-ttu-id="feaa8-107">Esta guía le ofrece información general sobre los conceptos básicos de PWA mediante la creación de una `localhost` aplicación web simple como PWA con Microsoft Visual Studio y algunas utilidades de creación de PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-107">This guide gives you an overview of PWA basics by building a simple `localhost` web app as a PWA using Microsoft Visual Studio and some PWA Builder utilities.</span></span>  <span data-ttu-id="feaa8-108">El producto finalizado funciona de forma similar en cualquier explorador que admita PWAs.</span><span class="sxs-lookup"><span data-stu-id="feaa8-108">The finished product works similarly across any browser that supports PWAs.</span></span>  

> [!TIP]
> <span data-ttu-id="feaa8-109">Para una forma rápida de convertir un sitio existente en un PWA y empaquetarlo para Windows 10 y otras plataformas de aplicaciones, revise el [creador de PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="feaa8-109">For a quick way to convert an existing site to a PWA and package it for Windows 10 and other app platforms, review [PWA Builder][PwaBuilder].</span></span>  

## <span data-ttu-id="feaa8-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="feaa8-110">Prerequisites</span></span>  

<span data-ttu-id="feaa8-111">Puedes crear PWAs con cualquier IDE de desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="feaa8-111">You may build PWAs with any web development IDE.</span></span>  <span data-ttu-id="feaa8-112">A continuación se muestran solo los requisitos previos de esta guía, que le guiará a través de la compatibilidad de la herramienta PWA en el ecosistema de Windows Developer.</span><span class="sxs-lookup"><span data-stu-id="feaa8-112">The following are only prerequisites for this guide, which walks you through PWA tooling support in the Windows developer ecosystem.</span></span>  

*   <span data-ttu-id="feaa8-113">Descargar la \ (gratis \) [Visual Studio Community 2017][VisualStudioDownloads].</span><span class="sxs-lookup"><span data-stu-id="feaa8-113">Download the \(free\) [Visual Studio Community 2017][VisualStudioDownloads].</span></span>  <span data-ttu-id="feaa8-114">También puede usar las ediciones Professional, Enterprise o [Preview][VisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="feaa8-114">You may also use the Professional, Enterprise, or [Preview][VisualStudioPreview] editions.</span></span>  <span data-ttu-id="feaa8-115">Desde el instalador de Visual Studio, elija las siguientes cargas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="feaa8-115">From the Visual Studio Installer, choose the following Workloads.</span></span>  
    
    *   **<span data-ttu-id="feaa8-116">Desarrollo de la plataforma universal de Windows</span><span class="sxs-lookup"><span data-stu-id="feaa8-116">Universal Windows Platform development</span></span>**  
    *   **<span data-ttu-id="feaa8-117">Desarrollo de node. js</span><span class="sxs-lookup"><span data-stu-id="feaa8-117">Node.js development</span></span>**  

## <span data-ttu-id="feaa8-118">Configurar una aplicación web básica</span><span class="sxs-lookup"><span data-stu-id="feaa8-118">Set up a basic web app</span></span>  

<span data-ttu-id="feaa8-119">Por razones de simplicidad, use la plantilla de [aplicación de nodo. js y][VisualStudioNodeJsTutorial] de Visual Studio para crear `localhost` una aplicación web que atienda una `index.html` página.</span><span class="sxs-lookup"><span data-stu-id="feaa8-119">For the sake of simplicity, use the Visual Studio [Node.js and Express app][VisualStudioNodeJsTutorial] template to create `localhost` web app that serves up an `index.html` page.</span></span>  <span data-ttu-id="feaa8-120">Imagínese que esto es un marcador de posición para la aplicación web atractiva y completa que está desarrollando como PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-120">Imagine this as a placeholder for the compelling, full-featured web app that you are developing as a PWA.</span></span>  

1.  <span data-ttu-id="feaa8-121">Inicia Visual Studio y comienza un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="feaa8-121">Launch Visual Studio, and start a new project.</span></span>  
    *   <span data-ttu-id="feaa8-122">**Archivo**  >  **Nuevo**  >  **Proyecto...**</span><span class="sxs-lookup"><span data-stu-id="feaa8-122">**File** > **New** > **Project...**</span></span>  
    *   `Ctrl`+`Shift`+`N`  
1.  <span data-ttu-id="feaa8-123">En **JavaScript**, seleccione **aplicación básica de nodo. js Express 4**.</span><span class="sxs-lookup"><span data-stu-id="feaa8-123">Under **JavaScript**, select **Basic Node.js Express 4 Application**.</span></span>  <span data-ttu-id="feaa8-124">Establezca el nombre y la ubicación y elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="feaa8-124">Set the name and location and choose **OK**.</span></span>  
    
    ![Selección de la plantilla de proyecto node. js Express 4 en Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  <span data-ttu-id="feaa8-126">Una vez que se cargue el nuevo proyecto, elija **generar** \ ( `Ctrl` + `Shift` + `B` \) y **iniciar la depuración** \ ( `F5` \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-126">Once your new project loads, choose **Build** \(`Ctrl`+`Shift`+`B`\) and **Start Debugging** \(`F5`\).</span></span>  <span data-ttu-id="feaa8-127">Compruebe que el `index.html` archivo se cargue cuando vaya a `http://localhost:1337` .</span><span class="sxs-lookup"><span data-stu-id="feaa8-127">Verify that your `index.html` file loads when you browse to `http://localhost:1337`.</span></span>  
    
    ![Ejecutar el nuevo sitio en localhost][ImageVsNodejsExpressIndex]  

## <span data-ttu-id="feaa8-129">Convertir la aplicación en un PWA</span><span class="sxs-lookup"><span data-stu-id="feaa8-129">Turn your app into a PWA</span></span>  

<span data-ttu-id="feaa8-130">Ahora es el momento de conectar los requisitos básicos de [PWA][PwaEdgehtmlIndexRequirements] para la aplicación web: un manifiesto de la *aplicación web*, *https* y *trabajadores de servicio*.</span><span class="sxs-lookup"><span data-stu-id="feaa8-130">Now it is time to wire up the basic [PWA requirements][PwaEdgehtmlIndexRequirements] for your web app: a *Web App Manifest*, *HTTPS* and *Service Workers*.</span></span>  

### <span data-ttu-id="feaa8-131">Manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="feaa8-131">Web App Manifest</span></span>  

<span data-ttu-id="feaa8-132">Un [manifiesto de la aplicación web][MDNWebAppManifest] es un archivo de metadatos JSON que describe la aplicación, incluido el nombre, el autor, la dirección URL de la página de entrada y uno o más iconos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-132">A [Web App Manifest][MDNWebAppManifest] is a JSON metadata file describing your app, including the name, author, entry page URL, and one or more icons.</span></span>  <span data-ttu-id="feaa8-133">Dado que sigue un [esquema basado en estándares][W3cWebAppManifest], solo debe suministrar un manifiesto de aplicación web para el PWA que está instalando en cualquier combinación de plataforma, sistema operativo y dispositivo que admita PWAs.</span><span class="sxs-lookup"><span data-stu-id="feaa8-133">Because it follows a [standards-based schema][W3cWebAppManifest], you must only supply a single web app manifest for the PWA that you are installing on any platform, OS, and device combination that supports PWAs.</span></span>  <span data-ttu-id="feaa8-134">En el ecosistema de Windows, el manifiesto de la aplicación web señala al indizador Web de Bing que su PWA es candidata para la inclusión automática en [Microsoft Store][PwaEdgehtmlMicrosoftStore], donde puede llegar a casi 700 millones usuarios mensuales activos como aplicación de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="feaa8-134">In the Windows ecosystem, your web app manifest signals to the Bing web indexer that your PWA is a candidate for automatic inclusion in the [Microsoft Store][PwaEdgehtmlMicrosoftStore], where it may reach nearly 700 million active monthly users as a Windows 10 app.</span></span>  

<span data-ttu-id="feaa8-135">Si se tratase de un sitio activo existente, puede generar un manifiesto de la aplicación web con el [creador de PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="feaa8-135">If this were an existing live site, you may generate a web app manifest using [PWA Builder][PwaBuilder].</span></span>  <span data-ttu-id="feaa8-136">Como es un proyecto sin publicar, copie un manifiesto de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="feaa8-136">Since it is still an unpublished project, copy a sample manifest.</span></span>  

1.  <span data-ttu-id="feaa8-137">En el explorador de *soluciones*de Visual Studio, haga clic con el botón secundario en la carpeta *pública* y seleccione **Agregar**  >  **nuevo archivo...**, especificando `manifest.json` el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="feaa8-137">In the Visual Studio *Solution Explorer*, right-click the *public* folder and select **Add** > **New File...**, specifying `manifest.json` as the item name.</span></span>  
1.  <span data-ttu-id="feaa8-138">En el `manifest.json` archivo, copie el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="feaa8-138">In the `manifest.json` file, copy the following code.</span></span>  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    <span data-ttu-id="feaa8-139">En un verdadero PWA, el siguiente paso es personalizar el *nombre*, *start_url*, *short_name*, *Descripción*e *iconos* \ (los iconos se tratan en el siguiente paso \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-139">In a real PWA, the next step is to customize *name*, *start_url*, *short_name*, *description*, and *icons* \(icons are covered in the next step\).</span></span>  
    
    <span data-ttu-id="feaa8-140">Para obtener más información sobre los distintos valores de miembro y los propósitos asociados, vea la referencia del manifiesto de la [aplicación web][MDNWebAppManifest] .</span><span class="sxs-lookup"><span data-stu-id="feaa8-140">To learn more about the different member values and associated purposes, see the [Web App Manifest][MDNWebAppManifest] reference.</span></span>  
    
1.  <span data-ttu-id="feaa8-141">A continuación, rellene la `icons` matriz vacía con rutas de imagen reales mediante el generador de imágenes de la aplicación de PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-141">Next, fill in the empty `icons` array with actual image paths by using the PWA Builder App Image Generator.</span></span>  
    
    1.  <span data-ttu-id="feaa8-142">Con un explorador Web, Descargue esta [imagen de PWA de 512x512 de ejemplo][ImagePwa].</span><span class="sxs-lookup"><span data-stu-id="feaa8-142">Using a web browser, download this [sample 512x512 PWA image][ImagePwa].</span></span>  
    1.  <span data-ttu-id="feaa8-143">Vaya al [generador de imágenes][PwaBuilderAppImageGenerator]de la aplicación creador de PWA y seleccione la `pwa.png` imagen que acaba de guardar como **imagen de entrada** y, a continuación, elija el botón **Descargar** .</span><span class="sxs-lookup"><span data-stu-id="feaa8-143">Go to the PWA Builder [App Image Generator][PwaBuilderAppImageGenerator], and select the `pwa.png` image you just saved as the **Input Image** and then choose the **Download** button.</span></span>  
    1.  <span data-ttu-id="feaa8-144">**Abra** y **Extraiga** el archivo zip.</span><span class="sxs-lookup"><span data-stu-id="feaa8-144">**Open** and **Extract** the zip file.</span></span>  
    1.  <span data-ttu-id="feaa8-145">En el explorador de soluciones de Visual Studio, haga clic con el botón secundario en la `public` carpeta y **Abra carpeta en el explorador de archivos**.</span><span class="sxs-lookup"><span data-stu-id="feaa8-145">In the Visual Studio Solution Explorer, right-click the `public` folder and **Open Folder in File Explorer**.</span></span>  <span data-ttu-id="feaa8-146">Cree una **nueva carpeta** llamada `images` .</span><span class="sxs-lookup"><span data-stu-id="feaa8-146">Create a **New folder** named `images`.</span></span>  
    1.  <span data-ttu-id="feaa8-147">Copie todas las carpetas de plataforma \ ( `android` , `chrome` ,, etc `windows10` . \) del archivo zip extraído a la `images` carpeta y cierre la ventana del explorador de archivos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-147">Copy all of the platform folders \(`android`, `chrome`, `windows10`, and so on\) from your extracted zip to the `images` folder and close the file explorer window.</span></span>  <span data-ttu-id="feaa8-148">Agregue las carpetas a su proyecto de Visual Studio \ (en el explorador de soluciones, haga clic con el botón derecho en `images` carpeta y seleccione **Agregar**  >  **carpeta existente...** para cada una de las carpetas \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-148">Add the folders to your Visual Studio project \(in Solution Explorer, right-click `images` folder and select **Add** > **Existing folder...** for each of the folders\).</span></span>  
    1.  <span data-ttu-id="feaa8-149">Abra \ (con Visual Studio o cualquier editor \) el `icons.json` archivo del código postal extraído y copie la `"icons": [...]` matriz en el `manifest.json` archivo de su proyecto.</span><span class="sxs-lookup"><span data-stu-id="feaa8-149">Open \(with Visual Studio or any editor\) the `icons.json` file from the extracted zip and copy the `"icons": [...]` array into the `manifest.json` file of your project.</span></span>  

1.  <span data-ttu-id="feaa8-150">Ahora debe asociar el manifiesto de la aplicación web con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="feaa8-150">Now you must associate your web app manifest with your app.</span></span>  <span data-ttu-id="feaa8-151">Abra el `layout.pug` archivo \ (en la `views` carpeta \) para editarlo y agregue esta línea después del vínculo de la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-151">Open the `layout.pug` file \(in `views` folder\) for editing, and add this line right after the stylesheet link.</span></span>  <span data-ttu-id="feaa8-152">\ (Simplemente es la plantilla de [Pug][PugAttributes] de nodo para `<link rel='manifest' href='/manifest.json'>` \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-152">\(It is simply the Node [pug][PugAttributes] template shorthand for `<link rel='manifest' href='/manifest.json'>`\).</span></span>  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
<span data-ttu-id="feaa8-153">Con todo eso, tu aplicación web ahora está dando servicio a un manifiesto y pantalla Android iconos de aplicaciones listos para usar.</span><span class="sxs-lookup"><span data-stu-id="feaa8-153">With all that in place, your web app is now serving up a manifest and homescreen-ready app icons!</span></span>  <span data-ttu-id="feaa8-154">Intenta ejecutar la aplicación \ ( `F5` \) y cargar el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="feaa8-154">Try running your app \(`F5`\) and loading up the manifest.</span></span>  

![Cargar el manifiesto de la aplicación web desde localhost][ImageVsNodejsExpressManifest]  

<span data-ttu-id="feaa8-156">Y uno de sus iconos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-156">And one of your icons.</span></span>  

![Logotipo de la aplicación de Square71x71Logo que se carga desde localhost][ImageVsNodejsExpressIcon]  

<span data-ttu-id="feaa8-158">Si publica la aplicación Live \ (con un `start_url` \), el motor de búsqueda de Bing la identifica ahora como candidato para [el empaquetado y el envío automáticos a Microsoft Store][PwaEdgehtmlMicrosoftStore] como una aplicación de Windows 10 que se puede instalar.</span><span class="sxs-lookup"><span data-stu-id="feaa8-158">If you publish the app live \(with an actual `start_url`\), the Bing search engine now identifies it as a candidate for [automatic packaging and submission to the Microsoft Store][PwaEdgehtmlMicrosoftStore] as an installable Windows 10 app.</span></span>  <span data-ttu-id="feaa8-159">Asegúrese de que el archivo manifest. JSON incluya las [señales de calidad de las aplicaciones web progresivas][WindowsBlogsPwaEdge] para las que los análisis de Bing incluyen los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-159">Ensure that your manifest.json file includes the [Quality signals for Progressive Web Apps][WindowsBlogsPwaEdge] for which Bing scans including the following items.</span></span>   

*   `name`  
*   `description`  
*   <span data-ttu-id="feaa8-160">Al menos un icono de 512px cuadrado o superior \ (para garantizar una fuente de imagen de la resolución suficiente para generar automáticamente la pantalla de presentación de la aplicación, almacenar la información en el icono, etc. \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-160">At least one icon 512px square or larger \(to ensure an image source of sufficient resolution for auto-generating the splash screen of your app, store listing, tile image, and so on\).</span></span>  

<span data-ttu-id="feaa8-161">Además, use [https](#https), los [trabajos de servicio](#service-workers)y cumpla con [las directivas de Microsoft Store][LegalWindowsAgrementsMicrosoftStorePolicies].</span><span class="sxs-lookup"><span data-stu-id="feaa8-161">In addition, use [HTTPS](#https), [service workers](#service-workers), and comply with [Microsoft Store Policies][LegalWindowsAgrementsMicrosoftStorePolicies].</span></span>  

### <span data-ttu-id="feaa8-162">HTTPS</span><span class="sxs-lookup"><span data-stu-id="feaa8-162">HTTPS</span></span>  

<span data-ttu-id="feaa8-163">[Los trabajadores del servicio][MDNServiceWorkerApi] y otras tecnologías de PWA clave que funcionan con los trabajos del servicio \ (como la [caché][MDNCache], [inserción][MDNPushApi]y las API de [sincronización en segundo plano][MDNSyncManager] \) solo funcionan en conexiones seguras, lo que significa que es [https][WikiHttps] para los sitios activos o `localhost` para fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="feaa8-163">[Service Workers][MDNServiceWorkerApi] and other key PWA technologies that work with service workers \(such as the [Cache][MDNCache], [Push][MDNPushApi], and [Background Sync][MDNSyncManager] APIs\) only work across secure connections, which means [HTTPS][WikiHttps] for live sites or `localhost` for debugging purposes.</span></span>  

<span data-ttu-id="feaa8-164">Si [publica esta aplicación web como un sitio activo][VisualStudioNodejsTutorialPublishAzureAppService] \ (por ejemplo, al configurar una [cuenta gratuita de Azure][AzureCreateFreeAccount]), debe asegurarse de que su servidor está configurado para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="feaa8-164">If you [publish this web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="feaa8-165">Si usa el [servicio de aplicaciones de Microsoft Azure][AzureWebApps] para hospedar su sitio, se ofrece a través de HTTPS de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="feaa8-165">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="feaa8-166">Para esta guía, continúe usando `http://localhost` como un marcador de posición para un sitio activo atendido `https://` .</span><span class="sxs-lookup"><span data-stu-id="feaa8-166">For this guide, continue using `http://localhost` as a placeholder for a live site served over `https://`.</span></span>  

### <span data-ttu-id="feaa8-167">Trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="feaa8-167">Service Workers</span></span>  

<span data-ttu-id="feaa8-168">Los trabajadores del servicio son la tecnología clave que subyace a PWAs.</span><span class="sxs-lookup"><span data-stu-id="feaa8-168">Service Workers is the key technology behind PWAs.</span></span> <span data-ttu-id="feaa8-169">Los trabajadores de servicio actúan como un proxy entre su PWA y la red para habilitar su sitio web para que funcione como una aplicación nativa instalada que sirve a los escenarios sin conexión, responde a las notificaciones push del servidor y ejecuta tareas en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="feaa8-169">Service Workers act as a proxy between your PWA and the network to enable your website to function as an installed native app that serves up offline scenarios, responds to server push notifications, and runs background tasks.</span></span>  <span data-ttu-id="feaa8-170">Los trabajadores de servicios también abren nuevas estrategias de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="feaa8-170">Service workers also open up new performance strategies.</span></span>  <span data-ttu-id="feaa8-171">No es necesario implementar una aplicación web completa para usar la caché de trabajo del servicio para mejorar el rendimiento de la carga de páginas de su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="feaa8-171">You are not required to implement a full web app to use the service worker cache for fine-tuned page load performance for your website.</span></span>  

<span data-ttu-id="feaa8-172">Los trabajos de servicio son subprocesos de fondo activados por eventos que se ejecutan desde archivos de JavaScript que se han servido al lado de los scripts habituales que encienden tu aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="feaa8-172">Service workers are event-driven background threads that run from JavaScript files served up alongside the regular scripts that power your web app.</span></span>  <span data-ttu-id="feaa8-173">Dado que los trabajos de servicio no se ejecutan en el subproceso de interfaz de usuario principal, los trabajadores del servicio no tienen acceso a DOM, aunque el [subproceso de interfaz de usuario][MDNWorkerPrototypePostMessage] y un [subproceso de trabajo][MDNDedicatedWorkerGlobalScopePostMessage] pueden comunicarse mediante `postMessage()` `onmessage` controladores de eventos y.</span><span class="sxs-lookup"><span data-stu-id="feaa8-173">Because Service workers do not run on the main UI thread, service workers do not have DOM access, though the [UI thread][MDNWorkerPrototypePostMessage] and a [worker thread][MDNDedicatedWorkerGlobalScopePostMessage] is able to communicate using `postMessage()` and `onmessage` event handlers.</span></span>  

<span data-ttu-id="feaa8-174">Para asociar un trabajador de servicio a la aplicación, regístrelo en el origen de la dirección URL de su sitio \ (o en una ruta de acceso especificada dentro de él \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-174">You associate a service worker with your app by registering it to the URL origin of your site \(or a specified path within it\).</span></span>  <span data-ttu-id="feaa8-175">Una vez que se haya registrado, el archivo de trabajo del servicio se descargará, se instalará y se activará en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="feaa8-175">Once registered, the service worker file is then downloaded, installed, and activated on the user machine.</span></span>  <span data-ttu-id="feaa8-176">Para obtener más información, MDN web docs tiene una guía completa sobre el uso de los [trabajos de servicio][MDNUsingServiceWorkers] y una referencia detallada de API de [trabajadores de servicios][MDNServiceWorkerApi] .</span><span class="sxs-lookup"><span data-stu-id="feaa8-176">For more, MDN web docs has a comprehensive guide on [Using Service Workers][MDNUsingServiceWorkers] and a detailed [Service Worker API][MDNServiceWorkerApi] reference.</span></span>  

<span data-ttu-id="feaa8-177">Para este tutorial, use el script de trabajo servicio de páginas sin conexión en el [creador de PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="feaa8-177">For this tutorial, use the Offline page service worker script on [PWA Builder][PwaBuilderServiceWorker].</span></span>  <span data-ttu-id="feaa8-178">Empiece por personalizar la secuencia de comandos con más funciones según sus requisitos de rendimiento, ancho de banda de red, etc.</span><span class="sxs-lookup"><span data-stu-id="feaa8-178">Start by customizing the script with more functionality according to your performance requirements, network bandwidth, and so on.</span></span>  <span data-ttu-id="feaa8-179">Revise el [manual del trabajo de servicio][ServiceWorkerCookbook] proporcionado por Mozilla para obtener varias ideas útiles para almacenar en caché de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="feaa8-179">Review the [Service Worker Cookbook][ServiceWorkerCookbook]  provided by Mozilla for a number of useful service worker caching ideas.</span></span>  

1.  <span data-ttu-id="feaa8-180">Abra [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] y seleccione el trabajo del servicio de **páginas sin conexión** \ (predeterminado \) y haga clic en el botón **Descargar trabajador de servicio** .</span><span class="sxs-lookup"><span data-stu-id="feaa8-180">Open [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] and select the \(default\) **Offline page** service worker and click the **Download service worker** button.</span></span>  
1.  <span data-ttu-id="feaa8-181">Abra la carpeta de descarga y copie los dos archivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="feaa8-181">Open the download folder and copy the following two files</span></span>  

    *   <span data-ttu-id="feaa8-182">ServiceWorker1\pwabuilder-sw-register.js</span><span class="sxs-lookup"><span data-stu-id="feaa8-182">ServiceWorker1\pwabuilder-sw-register.js</span></span>  
    *   <span data-ttu-id="feaa8-183">ServiceWorker1\pwabuilder-sw.js</span><span class="sxs-lookup"><span data-stu-id="feaa8-183">ServiceWorker1\pwabuilder-sw.js</span></span>  
    
    <span data-ttu-id="feaa8-184">Guarde los archivos en la `public` carpeta del proyecto de Visual Studio Web App.</span><span class="sxs-lookup"><span data-stu-id="feaa8-184">Save the files to the `public` folder of your Visual Studio web app project.</span></span>  <span data-ttu-id="feaa8-185">\ (En Visual Studio, use `Ctrl` + `O` para abrir el explorador de archivos a su proyecto y vaya a la `public` carpeta \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-185">\(From Visual Studio, use `Ctrl`+`O` to open file explorer to your project and navigate to the `public` folder\).</span></span>  
    
    <span data-ttu-id="feaa8-186">Merece la pena revisar el código en estos dos archivos para saber cómo registrar un trabajador de servicio que almacene una página designada \ ( `offline.html` \) y la sirva cuando se produzca un error en la recuperación de red.</span><span class="sxs-lookup"><span data-stu-id="feaa8-186">It is worth reviewing the code in both of these files, to get the gist of how to register a service worker that caches a designated page \(`offline.html`\) and serves it when a network fetch fails.</span></span>  <span data-ttu-id="feaa8-187">Después, cree una `offline.html` página simple como marcador de posición para la funcionalidad sin conexión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="feaa8-187">Next, create a simple `offline.html` page as a placeholder for the offline functionality of your app.</span></span>  
    
1.  <span data-ttu-id="feaa8-188">En el explorador de soluciones, abra el `views/layout.pug` archivo y agregue la siguiente línea debajo de las etiquetas de vínculos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-188">In Solution Explorer, open the `views/layout.pug` file, and add the following line below your link tags.</span></span>  
    
    ```html
    script(src='/pwabuilder-sw-register.js')
    ```  
    
    <span data-ttu-id="feaa8-189">Su sitio carga y ejecuta el script de registro de trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="feaa8-189">Your site loads and runs your service worker registration script.</span></span>  
    
1.  <span data-ttu-id="feaa8-190">En el explorador de soluciones, haga clic con el botón derecho en la `public` carpeta y seleccione **Agregar**  >  **nuevo archivo...**.  Asígnele un nombre y `offline.html` agregue `<title>` el contenido del cuerpo, por ejemplo, el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="feaa8-190">In Solution Explorer, right-click on the `public` folder and select **Add** > **New File...**.  Name it `offline.html`, and add a `<title>` and some body content, for example the following code.</span></span>  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    <span data-ttu-id="feaa8-191">En este momento, la `public` carpeta debería tener tres archivos nuevos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-191">At this point, your `public` folder should have three new files.</span></span>  
    
    ![Archivos agregados a la carpeta pública de la solución][ImageVsNodejsExpressPublic]  
    
1.  <span data-ttu-id="feaa8-193">En el explorador de soluciones, abra el `routes\index.js` archivo y agregue el código siguiente justo antes del comando final \ ( `module.exports = router;` \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-193">In Solution Explorer, open the `routes\index.js` file, and add the following code just before the final command \(`module.exports = router;`\).</span></span>  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    <span data-ttu-id="feaa8-194">Esto indica a tu aplicación que atienda el `offline.html` archivo \ (cuando el trabajador del servicio lo recupere para la caché sin conexión \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-194">This instructs your app to serve the `offline.html` file \(when your service worker fetches it for the offline cache\).</span></span>  
    
1.  <span data-ttu-id="feaa8-195">Pruebe su PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-195">Test out your PWA!</span></span>  <span data-ttu-id="feaa8-196">Compila \ ( `Ctrl` + `Shift` + `B` \) y ejecuta \ ( `F5` \) tu aplicación web para iniciar Microsoft Edge y abrir la `localhost` página.</span><span class="sxs-lookup"><span data-stu-id="feaa8-196">Build \(`Ctrl`+`Shift`+`B`\) and Run \(`F5`\) your web app to launch Microsoft Edge and open your `localhost` page.</span></span>  <span data-ttu-id="feaa8-197">A continuación, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="feaa8-197">Then complete the following steps.</span></span>  
    
    1.  <span data-ttu-id="feaa8-198">Abre la **consola** de DevTools perimetral \ ( `Ctrl` + `Shift` + `J` \) y verifica que el trabajador del servicio se haya registrado.</span><span class="sxs-lookup"><span data-stu-id="feaa8-198">Open the Edge DevTools **Console** \(`Ctrl`+`Shift`+`J`\) and verify the Service worker was registered.</span></span>  
    1.  <span data-ttu-id="feaa8-199">En el panel **depurador** , expanda el control de **trabajos del servicio** y haga clic en su origen.</span><span class="sxs-lookup"><span data-stu-id="feaa8-199">In the **Debugger** panel, expand the **Service Workers** control and click on your origin.</span></span>  <span data-ttu-id="feaa8-200">En la **Descripción general del trabajo del servicio**, verifique que el trabajador del servicio esté activado y ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="feaa8-200">In the **Service Worker Overview**, verify your service worker is activated and running.</span></span>  
        
        ![Información general del trabajo del servicio Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  <span data-ttu-id="feaa8-202">Expanda el control de **caché** y compruebe que la `offline.html` página se almacena en caché.</span><span class="sxs-lookup"><span data-stu-id="feaa8-202">Expand the **Cache** control and verify that the `offline.html` page is cached.</span></span>  
        
        ![Caché de trabajo del servicio Edge DevTools][ImageDevtoolsSwCache]  
        
1.  <span data-ttu-id="feaa8-204">Tiempo para probar su PWA como una aplicación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="feaa8-204">Time to try your PWA as an offline app!</span></span>  <span data-ttu-id="feaa8-205">En Visual Studio, **detenga la depuración** \ ( `Shift` + `F5` \) la aplicación web y, a continuación, abra Microsoft Edge \ (o actualizar \) en la dirección de localhost de su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="feaa8-205">In Visual Studio, **Stop Debugging** \(`Shift`+`F5`\) your web app, then open Microsoft Edge \(or refresh\) to the localhost address of your website.</span></span>  <span data-ttu-id="feaa8-206">Ahora debe cargar la `offline.html` Página \ (gracias a su trabajo de servicio y a la caché sin conexión \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-206">It should now load the `offline.html` page \(thanks to your service worker and offline cache\)!</span></span>  
    
    ![offline. html de http://localhost:1337 cargado en Microsoft Edge][ImageOfflineHtml]  

## <span data-ttu-id="feaa8-208">Agregar notificaciones push</span><span class="sxs-lookup"><span data-stu-id="feaa8-208">Add push notifications</span></span>  

<span data-ttu-id="feaa8-209">Haz que tu PWA sea más similar a la aplicación agregando compatibilidad de cliente para las notificaciones push mediante la [API de inserción][MDNPushApi] para suscribirte a un servicio de mensajería y la [API de notificaciones][MDNNotificationsApi] para mostrar un mensaje del sistema al recibir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="feaa8-209">Make your PWA more app-like by adding client-side support for push notifications using the [Push API][MDNPushApi] to subscribe to a messaging service and the [Notifications API][MDNNotificationsApi] to display a toast message upon receiving a message.</span></span>  <span data-ttu-id="feaa8-210">Al igual que con los trabajadores del servicio, estas son API basadas en estándares que funcionan entre exploradores, de modo que solo tienes que escribir el código una vez para que funcione en todas partes PWAs se admita.</span><span class="sxs-lookup"><span data-stu-id="feaa8-210">As with Service Workers, these are standards-based APIs that work cross-browser, so you only have to write the code once for it to work everywhere PWAs are supported.</span></span>  <span data-ttu-id="feaa8-211">En el servidor, use la biblioteca de código abierto de [inserción web][NPMWebPush] para controlar las diferencias que implica la entrega de mensajes Push a varios exploradores.</span><span class="sxs-lookup"><span data-stu-id="feaa8-211">On the server side, use the [Web-Push][NPMWebPush] open-source library to handle the differences involved in delivering push messages to various browsers.</span></span>  

<span data-ttu-id="feaa8-212">Lo siguiente está adaptado de la demostración de Push rico en el [manual de trabajos de trabajo][ServiceWorkerCookbookPushRichDemo] de los trabajos de Mozilla, que vale la pena consultar para obtener una serie de recetas útiles para trabajos de servicio y servicios Web.</span><span class="sxs-lookup"><span data-stu-id="feaa8-212">The following is adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which is worth checking out for a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="feaa8-213">Paso 1: instalar la biblioteca de inserción web NPM</span><span class="sxs-lookup"><span data-stu-id="feaa8-213">Step 1 - Install the NPM web-push library</span></span>  

<span data-ttu-id="feaa8-214">En el explorador de soluciones de Visual Studio, haga clic con el botón secundario en el proyecto y **Abra la ventana interactiva node. js...**  Escriba el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="feaa8-214">In Visual Studio Solution Explorer, right-click your project and **Open Node.js Interactive Window...**.  In it, type the following code.</span></span>  

```javascript
.npm install web-push
```  

<span data-ttu-id="feaa8-215">Esto instala la biblioteca [de inserción por web][NPMWebPush] .</span><span class="sxs-lookup"><span data-stu-id="feaa8-215">This installs the [Web-Push][NPMWebPush] library.</span></span>  <span data-ttu-id="feaa8-216">Después, abra el `index.js` archivo y agregue la línea siguiente a la parte superior del archivo después de las otras instrucciones de requisito.</span><span class="sxs-lookup"><span data-stu-id="feaa8-216">Then, open up your `index.js` file, and add the following line to the top of your file after the other requirement statements.</span></span>  

```javascript
var webpush = require('web-push');
```  

### <span data-ttu-id="feaa8-217">Paso 2: generar claves de VAPID para el servidor</span><span class="sxs-lookup"><span data-stu-id="feaa8-217">Step 2 - Generate VAPID keys for your server</span></span>  

<span data-ttu-id="feaa8-218">A continuación, debe generar las claves de VAPID \ (identificación de servidor de aplicaciones voluntaria \) para que el servidor envíe mensajes Push al cliente de PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-218">Next you must generate VAPID \(Voluntary Application Server Identification\) keys for your server to send push messages to the PWA client.</span></span>  <span data-ttu-id="feaa8-219">Solo tiene que hacer esto una vez \ (es decir, su servidor solo requiere un par de claves de VAPID \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-219">You only have to do this once \(that is, your server only requires a single pair of VAPID keys\).</span></span>  <span data-ttu-id="feaa8-220">En la ventana interactiva de node. js, escriba el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="feaa8-220">In the Node.js Interactive Window, type the following code.</span></span>  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

<span data-ttu-id="feaa8-221">El resultado debe dar lugar a un objeto JSON que contenga una clave pública y privada, que se copiará en la lógica del servidor.</span><span class="sxs-lookup"><span data-stu-id="feaa8-221">The output should result in a JSON object containing a public and private key, which you copy into your server logic.</span></span>  

<span data-ttu-id="feaa8-222">En el `index.js` archivo, justo antes de la línea final \ ( `module.exports = router` \), agregue el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="feaa8-222">In your `index.js` file, just before the final  \(`module.exports = router`\) line, add the following code.</span></span>  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

<span data-ttu-id="feaa8-223">Copie los `publicKey` valores de y `privateKey` que acaba de generar.</span><span class="sxs-lookup"><span data-stu-id="feaa8-223">Copy the `publicKey` and `privateKey` values that you just generated.</span></span>  <span data-ttu-id="feaa8-224">Personaliza `mailto` también la dirección (aunque no es necesario para ejecutar este ejemplo, \)).</span><span class="sxs-lookup"><span data-stu-id="feaa8-224">Feel free to customize the `mailto` address as well \(though it is not required in order to run this sample\).</span></span>  

<span data-ttu-id="feaa8-225">El [blog de ingeniería de servicios de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] ofrece un buen explicación sobre VAPID y webpush si estás interesado en la información sobre cómo funciona en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="feaa8-225">The [Mozilla Services engineering blog][MozillaServicesSendingVapidWebPushNotificationsPush] has a nice explainer on VAPID and WebPush if you are interested in the details of how it works behind the scenes.</span></span>  

### <span data-ttu-id="feaa8-226">Paso 3: controlar las solicitudes del servidor relacionadas con inserción</span><span class="sxs-lookup"><span data-stu-id="feaa8-226">Step 3 - Handle push-related server requests</span></span>  

<span data-ttu-id="feaa8-227">Ahora configure rutas para procesar las solicitudes de inserción del cliente de PWA, incluido el servicio de la clave pública VAPID y el registro del cliente para recibir mensajes Push.</span><span class="sxs-lookup"><span data-stu-id="feaa8-227">Now set up routes for handling push-related requests from the PWA client, including serving up the VAPID public key and registering the client to receive pushes.</span></span>  

<span data-ttu-id="feaa8-228">En un escenario real, una notificación push probablemente se origina desde un evento de la lógica del servidor.</span><span class="sxs-lookup"><span data-stu-id="feaa8-228">In a real scenario, a push notification likely originates from an event in your server logic.</span></span>  <span data-ttu-id="feaa8-229">Para simplificar las cosas aquí, debes agregar un botón de **notificación de inserción** a nuestra página principal de PWA para generar las inserciones de nuestro servidor y un `/sendNotification` extremo \ (ruta de servidor \) para administrar dichas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="feaa8-229">To simplify things here, you must add a **Push Notification** button to our PWA homepage for generating pushes from our server, and a `/sendNotification` endpoint \(server route\)for handling those requests.</span></span>  

<span data-ttu-id="feaa8-230">En el `index.js` archivo, Anexe las siguientes rutas justo después del código de inicialización VAPID que agregó en [paso 2] [#step-2---Generate-VAPID-for-Server].</span><span class="sxs-lookup"><span data-stu-id="feaa8-230">In your `index.js` file, append the following routes just after the VAPID initialization code you added in [Step 2][#step-2---generate-vapid-keys-for-your-server].</span></span>  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

<span data-ttu-id="feaa8-231">Con el código del lado del servidor en contexto, se sondea en las notificaciones Push en el cliente de PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-231">With the server-side code in place, plumb in push notifications on the PWA client.</span></span>  

### <span data-ttu-id="feaa8-232">Paso 4: suscribirse a notificaciones push</span><span class="sxs-lookup"><span data-stu-id="feaa8-232">Step 4 - Subscribe to push notifications</span></span>  

<span data-ttu-id="feaa8-233">Como parte de su rol como proxy de redes de PWA, los trabajos de servicio controlan los eventos Push y las interacciones de notificaciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="feaa8-233">As part of their role as PWA network proxies, service workers handle push events and toast notification interactions.</span></span>  <span data-ttu-id="feaa8-234">Sin embargo, como lo configuramos primero \ (o registrando \) un trabajador de servicio, se realiza una suscripción a las notificaciones push de servidor en el subproceso de interfaz de usuario principal de PWA y se requiere conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="feaa8-234">However, as it is with first setting up \(or registering\) a service worker, subscribing the PWA to server push notifications happens on the main UI thread of the PWA and requires network connectivity.</span></span>  <span data-ttu-id="feaa8-235">La suscripción a notificaciones Push requiere un registro de trabajo de servicio activo, por lo que primero debes verificar que el trabajo de tu servicio esté instalado y activo antes de intentar suscribirte a las notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="feaa8-235">Subscribing to push notifications requires an active service worker registration, so you must first verify that your service worker is installed and active before trying to subscribe it to push notifications.</span></span>  

<span data-ttu-id="feaa8-236">Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario ha concedido permiso de PWA para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="feaa8-236">Before a new push subscription is created, Microsoft Edge check if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="feaa8-237">En caso contrario, el explorador le pide permiso para el usuario.</span><span class="sxs-lookup"><span data-stu-id="feaa8-237">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="feaa8-238">Si el permiso es denegado, la solicitud para `registration.pushManager.subscribe` iniciar un `DOMException` , por lo tanto, debe controlarlo.</span><span class="sxs-lookup"><span data-stu-id="feaa8-238">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, so you must handle it.</span></span>  <span data-ttu-id="feaa8-239">Para obtener más información sobre la administración de permisos, vea [notificaciones Push en Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="feaa8-239">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="feaa8-240">En el `pwabuilder-sw-register.js` archivo, Anexe el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="feaa8-240">In your `pwabuilder-sw-register.js` file, append the following code.</span></span>  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
            });
        });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

<span data-ttu-id="feaa8-241">Revise la documentación de MDN en la interfaz de [PushManager][MDNPushManager] y en los documentos de NPM en la biblioteca de [inserción web][NPMWebPushUsage] para obtener más información sobre cómo funcionan las API y las distintas opciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="feaa8-241">Review the MDN documentation on the [PushManager][MDNPushManager] interface and NPM docs on the [Web-Push][NPMWebPushUsage] library for more details on how the APIs work and various related options.</span></span>  

### <span data-ttu-id="feaa8-242">Paso 5: configurar los controladores de eventos Push y notificationclick</span><span class="sxs-lookup"><span data-stu-id="feaa8-242">Step 5 - Set up push and notificationclick event handlers</span></span>  

<span data-ttu-id="feaa8-243">Con nuestra configuración de suscripciones Push, el resto del trabajo se realiza en el trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="feaa8-243">With our push subscription set up, the remainder of the work happens in the service worker.</span></span>  <span data-ttu-id="feaa8-244">En primer lugar debe configurar un controlador para eventos Push enviados por el servidor y responder con una notificación del sistema \ (si se ha concedido permiso \) que muestra la carga de datos Push.</span><span class="sxs-lookup"><span data-stu-id="feaa8-244">First you must set up a handler for server-sent push events, and respond with a toast notification \(if permission was granted\) displaying the push data payload.</span></span>  <span data-ttu-id="feaa8-245">A continuación, agrega un controlador de clic para que la notificación del sistema descarte la notificación y se ordene mediante una lista de las ventanas abiertas para abrir, enfocar o abrir y centrar la página de cliente de PWA prevista.</span><span class="sxs-lookup"><span data-stu-id="feaa8-245">Next you add a click handler for the toast to dismiss the notification and sort through a list of currently open windows to open, focus, or open and focus the intended PWA client page.</span></span>  

<span data-ttu-id="feaa8-246">En el `pwabuilder-sw.js` archivo, anexe los controladores siguientes.</span><span class="sxs-lookup"><span data-stu-id="feaa8-246">In your `pwabuilder-sw.js` file, append the following handlers.</span></span>  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### <span data-ttu-id="feaa8-247">Paso 6: pruébelo</span><span class="sxs-lookup"><span data-stu-id="feaa8-247">Step 6 - Try it out</span></span>  

<span data-ttu-id="feaa8-248">Tiempo para probar las notificaciones Push en el PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-248">Time to test push notifications in your PWA!</span></span>  

1.  <span data-ttu-id="feaa8-249">Ejecute \ ( `F5` \) su PWA en el explorador.</span><span class="sxs-lookup"><span data-stu-id="feaa8-249">Run \(`F5`\) your PWA in the browser.</span></span>  <span data-ttu-id="feaa8-250">Debido a que modificó el código de trabajo de servicio \ ( `pwabuilder-sw.js` \), debe abrir el depurador de DevTools \ ( `F12` \) en el panel de **información general de trabajos del servicio** y **anular el registro** del trabajador del servicio y volver a cargar \ ( `F5` \) la página para volver a registrarlo \ (o hacer clic en **Actualizar**\).</span><span class="sxs-lookup"><span data-stu-id="feaa8-250">Because you modified the service worker code \(`pwabuilder-sw.js`\), you must open the DevTools Debugger \(`F12`\) to the **Service Worker Overview** panel and **Unregister** the service worker and reload \(`F5`\) the page to re-register it \(or you click **Update**\).</span></span>  <span data-ttu-id="feaa8-251">En un escenario de producción, el explorador comprueba periódicamente si hay actualizaciones de los trabajadores del servicio e instala las actualizaciones en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="feaa8-251">In a production scenario, the browser checks regularly check for service worker updates and install the updates in the background.</span></span>  <span data-ttu-id="feaa8-252">Para obtener resultados inmediatos, debes forzarlo aquí.</span><span class="sxs-lookup"><span data-stu-id="feaa8-252">You should force it here for immediate results.</span></span>  
    
    <span data-ttu-id="feaa8-253">Como el trabajador de servicio se activa e intenta suscribir su PWA a las notificaciones push, debe ver un cuadro de diálogo de permisos en la parte inferior de la página.</span><span class="sxs-lookup"><span data-stu-id="feaa8-253">As your service worker activates and attempts to subscribe your PWA to push notifications, you should see a permission dialog at the bottom of the page.</span></span>  
    
    ![Cuadro de diálogo de permisos para habilitar las notificaciones][ImageNotificationPermission]  
    
    <span data-ttu-id="feaa8-255">Elija **sí** para habilitar las notificaciones del sistema para su PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-255">Choose **Yes** to enable toast notifications for your PWA.</span></span>  
    
1.  <span data-ttu-id="feaa8-256">En el panel Descripción general del trabajo del servicio, intente elegir el botón de **comando** .</span><span class="sxs-lookup"><span data-stu-id="feaa8-256">From the Service Worker Overview pane, try choosing the  **Push** button.</span></span>  <span data-ttu-id="feaa8-257">Debe aparecer una notificación del sistema con el \ (mensaje de inserción de prueba "DevTools" \).</span><span class="sxs-lookup"><span data-stu-id="feaa8-257">A toast notification with the \(hard-coded "Test push message from DevTools"\) payload should appear.</span></span>  
    
    ![Insertar una notificación desde DevTools][ImageDevtoolsPush]  
    
1.  <span data-ttu-id="feaa8-259">A continuación, seleccione el botón **Enviar notificación** en la Página principal de su PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-259">Next try choosing the **Send Notification** button on the homepage of your PWA.</span></span>  <span data-ttu-id="feaa8-260">Esta vez aparece una notificación del sistema con la carga de su servidor.</span><span class="sxs-lookup"><span data-stu-id="feaa8-260">This time a toast with the payload from your server appears.</span></span>  
    
    ![Insertar una notificación desde el servidor PWA][ImagePwaPush]  
    
    <span data-ttu-id="feaa8-262">Si no hace clic en \ (o activa \) una notificación del sistema, se descarta después de varios segundos y se pone en cola en el centro de actividades de Windows.</span><span class="sxs-lookup"><span data-stu-id="feaa8-262">If you do not click \(or activate\) a toast notification, it is dismissed after several seconds and queue up in your Windows Action Center.</span></span>  
    
    ![Notificaciones en el centro de actividades de Windows][ImageWindowsActionCenter]  
    
    <span data-ttu-id="feaa8-264">Tiene los conceptos básicos de las notificaciones push de PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-264">You have the basics of PWA push notifications.</span></span>  <span data-ttu-id="feaa8-265">En una aplicación real, los pasos siguientes se implementan de una manera de administrar y almacenar suscripciones Push y de [cifrar][NPMWebPushEncrypt] correctamente los datos de carga que se envían a través de la red.</span><span class="sxs-lookup"><span data-stu-id="feaa8-265">In a real app, the next steps are implemented in a way to manage and store push subscriptions and to properly [encrypt][NPMWebPushEncrypt] payload data being sent across the wire.</span></span>  
    
## <span data-ttu-id="feaa8-266">Ir más allá</span><span class="sxs-lookup"><span data-stu-id="feaa8-266">Going further</span></span>  

<span data-ttu-id="feaa8-267">Esta guía demostró la anatomía básica de una aplicación web progresiva y herramientas de desarrollo de PWA de Microsoft, como Visual Studio, PWA Builder y Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="feaa8-267">This guide demonstrated the basic anatomy of a Progressive Web App and Microsoft PWA development tools including Visual Studio, PWA Builder, and Edge DevTools.</span></span>  

<span data-ttu-id="feaa8-268">Por supuesto, hay mucho más que suponen [un excelente PWA][PwaEdgehtmlIndexRequirements] más allá de lo que Lee aquí, como el diseño con capacidad de respuesta, la vinculación profunda, las [pruebas entre exploradores][BrowserStackTestEdgeBrowser] y otras [prácticas recomendadas][Webhint] \ (sin mencionar la funcionalidad de la aplicación! \), pero espero que esta guía le haya proporcionado una sólida introducción de conceptos básicos de PWA y algunas ideas para empezar.</span><span class="sxs-lookup"><span data-stu-id="feaa8-268">Of course, there is a lot more that goes into [making a great PWA][PwaEdgehtmlIndexRequirements] beyond what you read here, including responsive design, deep-linking, [cross-browser testing][BrowserStackTestEdgeBrowser] and other [best practices][Webhint] \(not to mention your app functionality!\), but hopefully this guide gave you a solid introduction of PWA basics and some ideas on getting started.</span></span>  <span data-ttu-id="feaa8-269">Si tiene más preguntas sobre el desarrollo de PWA con Windows o con Visual Studio, deje un comentario.</span><span class="sxs-lookup"><span data-stu-id="feaa8-269">If you have further questions on PWA development with Windows or with Visual Studio, please leave a comment!</span></span>  

<span data-ttu-id="feaa8-270">Revise las demás guías de PWA para obtener información sobre cómo incrementar la participación de los clientes y ofrecer una experiencia de la aplicación integrada en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="feaa8-270">Review the other PWA guides to learn how to increase customer engagement and provide a more seamless, OS-integrated app experience.</span></span>  

*   <span data-ttu-id="feaa8-271">[Adaptación de ventanas][PwaEdgehtmlWindowsFeatures].</span><span class="sxs-lookup"><span data-stu-id="feaa8-271">[Windows tailoring][PwaEdgehtmlWindowsFeatures].</span></span> <span data-ttu-id="feaa8-272">Con la simple detección de características, puede mejorar progresivamente su PWA para los clientes de Windows 10 a través de las API de Windows Runtime \ (WinRT \) nativas, como las que se usan para personalizar las notificaciones del menú **Inicio** de Windows y la barra de tareas Jumplists, y \ (tras el permiso \) trabajar con recursos de usuario, como fotos, música y calendario.</span><span class="sxs-lookup"><span data-stu-id="feaa8-272">Using simple feature detection, you may progressively enhance your PWA for Windows 10 customers through native Windows Runtime \(WinRT\) APIs, such as those for customizing Windows **Start** menu tile notifications and taskbar jumplists, and \(upon permission\) working with user resources, such as photos, music, and calendar.</span></span>  
*   <span data-ttu-id="feaa8-273">[PWAs en Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="feaa8-273">[PWAs in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  <span data-ttu-id="feaa8-274">Obtenga más información sobre las ventajas de la distribución de la tienda de aplicaciones y cómo enviar su PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-274">Learn more about the benefits of app store distribution and how to submit your PWA.</span></span>  

## <span data-ttu-id="feaa8-275">Consulte también</span><span class="sxs-lookup"><span data-stu-id="feaa8-275">See also</span></span>  

*   <span data-ttu-id="feaa8-276">[Aplicaciones web progresivas en los documentos web de MDN][MDNProgressiveWebApps] : guía excelente sobre aplicaciones web progresivas.</span><span class="sxs-lookup"><span data-stu-id="feaa8-276">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="feaa8-277">[Aplicaciones web progresivas en Web. dev][WebDevProgressiveWebApps] : excelente guía sobre las aplicaciones web progresivas.</span><span class="sxs-lookup"><span data-stu-id="feaa8-277">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="feaa8-278">[Rocks de aplicaciones web progresivas][ProgressiveWebApps] : exhibe ejemplos reales de PWAs.</span><span class="sxs-lookup"><span data-stu-id="feaa8-278">[Progressive Web Apps rocks][ProgressiveWebApps] - Showcases real-world examples of PWAs.</span></span>  
*   <span data-ttu-id="feaa8-279">[Lectores de noticias de piratas informáticos como aplicaciones web progresivas][HackerNewsProgressiveWebApps] : compara diferentes marcos de trabajo y patrones de rendimiento para implementar un ejemplo \ (lector de noticias de hacker \) PWA.</span><span class="sxs-lookup"><span data-stu-id="feaa8-279">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requisitos: aplicaciones web progresivas \ (EdgeHTML \) en Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Aplicaciones web progresivas \ (EdgeHTML \) en Microsoft Store"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps-edgehtml/windows-features.md "Personalizar su PWA \ (EdgeHTML \) para Windows"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Directivas de Microsoft Store | Microsoft docs"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Tutorial: crear un nodo. js y una aplicación Express en Visual Studio | Microsoft docs"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publicar en el servicio de aplicaciones de Azure: cree un nodo. js y una aplicación Express en Visual Studio | Microsoft docs"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "¿Qué es una aplicación de la plataforma universal de Windows \ (UWP \)?  | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Crear cuenta gratuita de Azure Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicaciones Web | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Bienvenida a aplicaciones web progresivas a Microsoft Edge y Windows 10 | Blogs de Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificaciones Web en Microsoft Edge | Blogs de Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Descargas | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Software para desarrolladores gratis & Services | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Vista previa de Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Pruebas gratuitas del navegador Microsoft Edge en Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lectores de noticias de piratas informáticos como aplicaciones web progresivas"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. PostMessage \ (\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicaciones web progresivas \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabajadores de servicio | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de la aplicación Web | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. prototype. PostMessage \ (\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envío de notificaciones por inserción de VAPID identificadas por el servicio de inserción de Mozilla | Servicios de Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-insertar | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, payload, contentEncoding)-web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso-web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicaciones web progresivas"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Atributos | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Creador de PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Generador de imágenes de aplicaciones"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Trabajo del servicio | Creador de PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "ServiceWorker"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Demostración de inserción enriquecida | ServiceWorker"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Manifiesto de la aplicación Web | RELATIVA"  

[Webhint]: https://sonarwhal.com "webhint, el motor de sugerencias para los procedimientos recomendados para Web" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usar los trabajadores web" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicaciones web progresivas | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Wikipedia"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Mejora progresiva | Wikipedia"  
