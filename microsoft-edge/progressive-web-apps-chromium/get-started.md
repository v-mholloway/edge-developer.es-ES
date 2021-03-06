---
description: En esta guía se ofrece información general sobre los conceptos básicos y las herramientas de PWA para crear aplicaciones web progresivas (Chromium) en Windows.
title: Introducción a Las aplicaciones web progresivas (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto web, trabajador de servicio, inserción
ms.openlocfilehash: 6ff24b2e9219b2f3755bb2e8f6db137dc7a721ec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398136"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a><span data-ttu-id="d0563-104">Introducción a Las aplicaciones web progresivas (Chromium)</span><span class="sxs-lookup"><span data-stu-id="d0563-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="d0563-105">Las aplicaciones web progresivas \(PWAs\) son aplicaciones web que se mejoran [progresivamente.][WikiProgressiveEnhancement]</span><span class="sxs-lookup"><span data-stu-id="d0563-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="d0563-106">Las mejoras progresivas incluyen características como aplicaciones, como la instalación, la compatibilidad sin conexión y las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="d0563-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="d0563-107">También puedes empaquetar tu PWA para almacenes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d0563-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="d0563-108">Entre las posibles tiendas de aplicaciones se incluyen Microsoft Store, Google Play, Mac App Store y mucho más.</span><span class="sxs-lookup"><span data-stu-id="d0563-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="d0563-109">Microsoft Store es la tienda de aplicaciones comercial integrada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d0563-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="d0563-110">En la siguiente guía se ofrece información general sobre los conceptos básicos de PWA mediante la creación de una aplicación web sencilla y su extensión como PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="d0563-111">El proyecto terminado funciona en exploradores modernos.</span><span class="sxs-lookup"><span data-stu-id="d0563-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="d0563-112">Puedes usar [PWABuilder para][PwaBuilder] crear una PWA nueva, mejorar tu PWA existente o empaquetar tu PWA para almacenes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d0563-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="d0563-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0563-113">Prerequisites</span></span>  

*   <span data-ttu-id="d0563-114">Use [Visual Studio code para][VisualstudioCodeMain] editar el código fuente de PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="d0563-115">Use [Node.js][NodejsMain] como servidor web local.</span><span class="sxs-lookup"><span data-stu-id="d0563-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <a name="create-a-basic-web-app"></a><span data-ttu-id="d0563-116">Crear una aplicación web básica</span><span class="sxs-lookup"><span data-stu-id="d0563-116">Create a basic web app</span></span>  

<span data-ttu-id="d0563-117">Para crear una aplicación web vacía, siga los pasos de [Node Express App Generator][ExpressjsApplicationGenerator]y asigne un nombre a la aplicación `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="d0563-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="d0563-118">En el símbolo del sistema, ejecute los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="d0563-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="d0563-119">Los comandos crean una aplicación web vacía e instalan cualquier dependencia.</span><span class="sxs-lookup"><span data-stu-id="d0563-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="d0563-120">Ahora tienes una aplicación web sencilla y funcional.</span><span class="sxs-lookup"><span data-stu-id="d0563-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="d0563-121">Para iniciar la aplicación web, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d0563-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="d0563-122">Ahora vaya a `http://localhost:3000` ver la nueva aplicación web.</span><span class="sxs-lookup"><span data-stu-id="d0563-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ejecutar el nuevo PWA en localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="d0563-124">Ejecutar el nuevo PWA en localhost</span><span class="sxs-lookup"><span data-stu-id="d0563-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <a name="get-started-building-a-pwa"></a><span data-ttu-id="d0563-125">Introducción a la creación de un PWA</span><span class="sxs-lookup"><span data-stu-id="d0563-125">Get started building a PWA</span></span>  

<span data-ttu-id="d0563-126">Ahora que tienes una aplicación web sencilla, prorrogarla como PWA agregando los tres requisitos para las PWA</span><span class="sxs-lookup"><span data-stu-id="d0563-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="d0563-127">: [HTTPS](#step-1---use-https), un [manifiesto de aplicación web](#step-2---create-a-web-app-manifest)y un trabajador de [servicio](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="d0563-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <a name="step-1---use-https"></a><span data-ttu-id="d0563-128">Paso 1: Usar HTTPS</span><span class="sxs-lookup"><span data-stu-id="d0563-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="d0563-129">Las partes clave de la plataforma PWA, como [los trabajadores de][MDNServiceWorkerApi]servicio, requieren el uso de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d0563-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="d0563-130">Cuando el PWA entre en servicio, debes publicarlo en una dirección URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d0563-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="d0563-131">Para fines de depuración, Microsoft Edge también permite usar `http://localhost` las API de PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="d0563-132">[Publique la aplicación web como un sitio en directo,][VisualStudioNodejsTutorialPublishAzureAppService]pero asegúrese de que el servidor está configurado para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d0563-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="d0563-133">Por ejemplo, puede crear una cuenta [gratuita de Azure][AzureCreateFreeAccount].</span><span class="sxs-lookup"><span data-stu-id="d0563-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="d0563-134">Hospedar el sitio en [el Servicio de aplicaciones de Microsoft Azure][AzureWebApps] y se sirve a través de HTTPS de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d0563-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="d0563-135">La siguiente guía, use `http://localhost` para crear su PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <a name="step-2---create-a-web-app-manifest"></a><span data-ttu-id="d0563-136">Paso 2: Crear un manifiesto de aplicación web</span><span class="sxs-lookup"><span data-stu-id="d0563-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="d0563-137">Un [manifiesto de aplicación web][MDNWebAppManifest] es un archivo JSON que contiene metadatos sobre la aplicación, como el nombre, la descripción, los iconos y mucho más.</span><span class="sxs-lookup"><span data-stu-id="d0563-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="d0563-138">Para agregar un manifiesto de aplicación a la aplicación web:</span><span class="sxs-lookup"><span data-stu-id="d0563-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="d0563-139">En Visual Studio, elija **Archivo**  >  **abrir carpeta** y elija el directorio que `MySamplePwa` creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d0563-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="d0563-140">Seleccione `Ctrl` + `N` para crear un nuevo archivo y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="d0563-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  <span data-ttu-id="d0563-141">Guarde el archivo como `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="d0563-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="d0563-142">Agregue una imagen de icono de aplicación de 512x512 denominada `icon512.png` a `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="d0563-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="d0563-143">Puede usar la imagen [de ejemplo con][ImagePwa] fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="d0563-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="d0563-144">En Visual Studio, abra y agregue el siguiente fragmento `/public/index.html` de código dentro de la `<head>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="d0563-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a><span data-ttu-id="d0563-145">Paso 3: Agregar un trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="d0563-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="d0563-146">Los trabajadores de servicio son la tecnología clave detrás de las PWA, lo que permite escenarios como la compatibilidad sin conexión, el almacenamiento en caché avanzado y la ejecución de tareas en segundo plano anteriormente limitadas a aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="d0563-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="d0563-147">Los trabajadores de servicio son tareas en segundo plano que interceptan solicitudes de red desde la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="d0563-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="d0563-148">Los trabajadores del servicio intentan completar tareas, incluso cuando el PWA no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d0563-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="d0563-149">Las tareas incluyen las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="d0563-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="d0563-150">Servir recursos solicitados desde una memoria caché</span><span class="sxs-lookup"><span data-stu-id="d0563-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="d0563-151">Envío de notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="d0563-151">Sending push notifications</span></span>  
*   <span data-ttu-id="d0563-152">Ejecutar tareas de captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="d0563-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="d0563-153">Iconos de badging</span><span class="sxs-lookup"><span data-stu-id="d0563-153">Badging icons</span></span>  
*   <span data-ttu-id="d0563-154">y mucho más</span><span class="sxs-lookup"><span data-stu-id="d0563-154">and more</span></span>  
    
<span data-ttu-id="d0563-155">Los trabajadores de servicio se definen en un archivo JavaScript especial.</span><span class="sxs-lookup"><span data-stu-id="d0563-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="d0563-156">Para obtener más información, vaya a [Using Service Workers][MDNUsingServiceWorkers] and Service Worker [API][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="d0563-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="d0563-157">Para crear un trabajador de servicio en el proyecto, use la receta **de** trabajo de servicio de red de caché de [PWA Builder][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="d0563-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="d0563-158">Vaya a [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], seleccione el trabajador de **servicio** de red primero en caché y seleccione el **botón** Descargar.</span><span class="sxs-lookup"><span data-stu-id="d0563-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="d0563-159">El archivo descargado contiene los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="d0563-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="d0563-160">Copie los archivos descargados en la `public` carpeta del proyecto de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="d0563-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="d0563-161">En Visual Studio code, abra y agregue el siguiente fragmento `/public/index.html` de código dentro de la `<head>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="d0563-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="d0563-162">La aplicación web ahora tiene un trabajador de servicio que usa la estrategia de primero en caché.</span><span class="sxs-lookup"><span data-stu-id="d0563-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="d0563-163">El nuevo trabajador de servicio captura primero los recursos de la memoria caché y de la red solo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d0563-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="d0563-164">Los recursos almacenados en caché incluyen imágenes, JavaScript, CSS y HTML.</span><span class="sxs-lookup"><span data-stu-id="d0563-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="d0563-165">Siga estos pasos para confirmar que se ejecuta el trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="d0563-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="d0563-166">Navegue a la aplicación web con `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="d0563-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="d0563-167">Si la aplicación web no está disponible, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d0563-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="d0563-168">En Microsoft Edge, seleccione `F12` para abrir Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d0563-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="d0563-169">Seleccione **Aplicación**y, a continuación, **Trabajadores de** servicio para ver los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="d0563-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="d0563-170">Si no se muestra el trabajador del servicio, actualice la página.</span><span class="sxs-lookup"><span data-stu-id="d0563-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Introducción al trabajador del servicio DevTools de Microsoft Edge" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="d0563-172">Introducción al trabajador del servicio DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d0563-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="d0563-173">Para ver la caché de trabajo de servicio, expanda **Almacenamiento en caché** y seleccione **pwabuilder-precache**.</span><span class="sxs-lookup"><span data-stu-id="d0563-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="d0563-174">Se deben mostrar todos los recursos almacenados en caché por el trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="d0563-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="d0563-175">Los recursos almacenados en caché por el trabajador de servicio incluyen el icono de la aplicación, el manifiesto de la aplicación, CSS y los archivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d0563-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Caché de trabajo de servicio en Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="d0563-177">Caché del trabajador de servicio en Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="d0563-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="d0563-178">Prueba tu PWA como una aplicación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d0563-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="d0563-179">En Microsoft Edge DevTools \( `F12` \), \*\*\*\* elija **Red** y, a continuación, cambie el estado En línea a **Sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="d0563-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Establecer la aplicación en modo sin conexión en Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="d0563-181">Establecer la aplicación en modo sin conexión en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d0563-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="d0563-182">Actualiza la aplicación y debería mostrar el mecanismo sin conexión para servir los recursos de la aplicación desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="d0563-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA que se ejecuta sin conexión" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="d0563-184">PWA que se ejecuta sin conexión</span><span class="sxs-lookup"><span data-stu-id="d0563-184">PWA running offline</span></span>
    :::image-end:::
    
## <a name="add-push-notifications-to-your-pwa"></a><span data-ttu-id="d0563-185">Agregar notificaciones de inserción a su PWA</span><span class="sxs-lookup"><span data-stu-id="d0563-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="d0563-186">Puede crear PWA que admitan notificaciones de inserción completando las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="d0563-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="d0563-187">Suscribirse a un servicio de mensajería mediante la [API de inserción][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="d0563-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="d0563-188">Mostrar un mensaje del sistema cuando se recibe un mensaje del servicio mediante la [API de notificaciones][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="d0563-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="d0563-189">Al igual que con los trabajadores de servicio, las API de notificación de inserción son API basadas en estándares.</span><span class="sxs-lookup"><span data-stu-id="d0563-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="d0563-190">Las API de notificación de inserción funcionan en todos los exploradores, por lo que el código debe funcionar en todas partes en las que se admiten las PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="d0563-191">Para obtener más información acerca de cómo entregar mensajes de inserción a diferentes exploradores del servidor, vaya a [Web-Push][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="d0563-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="d0563-192">Los siguientes pasos se han adaptado del Libro de recetas Push Rich Demo in [Service Worker][ServiceWorkerCookbookPushRichDemo] proporcionado por Mozilla, que tiene una serie de otras recetas útiles de inserción web y de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="d0563-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <a name="step-1---generate-vapid-keys"></a><span data-ttu-id="d0563-193">Paso 1: Generar claves VAPID</span><span class="sxs-lookup"><span data-stu-id="d0563-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="d0563-194">Las notificaciones push requieren claves VAPID \(Voluntary Application Server Identification\) para enviar mensajes de inserción al cliente de PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="d0563-195">Hay varios generadores de claves VAPID disponibles en línea \(por ejemplo, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="d0563-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="d0563-196">Después de la generación, debe obtener un objeto JSON que contenga una clave pública y privada.</span><span class="sxs-lookup"><span data-stu-id="d0563-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="d0563-197">Guarde las claves para los pasos posteriores del siguiente tutorial.</span><span class="sxs-lookup"><span data-stu-id="d0563-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="d0563-198">Para obtener información acerca de VAPID y WebPush, vaya a Enviar notificaciones [de WebPush identificadas por VAPID mediante el Servicio de inserción de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="d0563-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <a name="step-2---subscribe-to-push-notifications"></a><span data-ttu-id="d0563-199">Paso 2: suscribirse a notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="d0563-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="d0563-200">Los trabajadores de servicio controlan eventos de inserción e interacciones de notificación del sistema en su PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="d0563-201">Para suscribir el PWA a las notificaciones de inserción del servidor, asegúrese de que se cumplen las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="d0563-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="d0563-202">El PWA está instalado, activo y registrado</span><span class="sxs-lookup"><span data-stu-id="d0563-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="d0563-203">El código para completar la tarea de suscripción está en el subproceso de interfaz de usuario principal de la PWA</span><span class="sxs-lookup"><span data-stu-id="d0563-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="d0563-204">Tiene conectividad de red</span><span class="sxs-lookup"><span data-stu-id="d0563-204">You have network connectivity</span></span>  
    
<span data-ttu-id="d0563-205">Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario concedió el permiso de PWA para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d0563-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="d0563-206">Si no es así, el explorador le pedirá permiso al usuario.</span><span class="sxs-lookup"><span data-stu-id="d0563-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="d0563-207">Si se deniega el permiso, la solicitud `registration.pushManager.subscribe` para iniciar un , que debe `DOMException` controlarse.</span><span class="sxs-lookup"><span data-stu-id="d0563-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="d0563-208">Para obtener más información sobre la administración de permisos, vaya a [Notificaciones de inserción en Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="d0563-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="d0563-209">En el `pwabuilder-sw-register.js` archivo, anexa el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="d0563-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
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

<span data-ttu-id="d0563-210">Para obtener más información, vaya a [PushManager][MDNPushManager] y [Web-Push][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="d0563-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <a name="step-3---listen-for-push-notifications"></a><span data-ttu-id="d0563-211">Paso 3: escuchar notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="d0563-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="d0563-212">Después de crear una suscripción en su PWA, agregue controladores al trabajador del servicio para responder a eventos de inserción.</span><span class="sxs-lookup"><span data-stu-id="d0563-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="d0563-213">El evento Push se envía desde el servidor para mostrar notificaciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0563-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="d0563-214">Las notificaciones del sistema muestran los datos de un mensaje recibido.</span><span class="sxs-lookup"><span data-stu-id="d0563-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="d0563-215">Para completar las siguientes tareas, debe agregar un `click` controlador.</span><span class="sxs-lookup"><span data-stu-id="d0563-215">To complete the following tasks, you must add a `click` handler.</span></span>  

*   <span data-ttu-id="d0563-216">Descartar la notificación del sistema</span><span class="sxs-lookup"><span data-stu-id="d0563-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="d0563-217">Abrir, enfocar o abrir y enfocar cualquier ventana abierta</span><span class="sxs-lookup"><span data-stu-id="d0563-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="d0563-218">Abrir y centrar una nueva ventana para mostrar una página de cliente de PWA</span><span class="sxs-lookup"><span data-stu-id="d0563-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="d0563-219">En el `pwabuilder-sw.js` archivo, agregue los siguientes controladores.</span><span class="sxs-lookup"><span data-stu-id="d0563-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
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

### <a name="step-4---try-it-out"></a><span data-ttu-id="d0563-220">Paso 4: Pruébalo</span><span class="sxs-lookup"><span data-stu-id="d0563-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="d0563-221">Para probar las notificaciones de inserción de su PWA, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d0563-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="d0563-222">Vaya a su PWA en `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="d0563-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="d0563-223">Cuando el trabajador de servicio se activa e intenta suscribir su PWA a notificaciones push, Microsoft Edge le pide que permita que su PWA muestre notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d0563-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="d0563-224">Seleccione **Permitir**.</span><span class="sxs-lookup"><span data-stu-id="d0563-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Cuadro de diálogo de permisos para habilitar notificaciones" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="d0563-226">Cuadro de diálogo de permisos para habilitar notificaciones</span><span class="sxs-lookup"><span data-stu-id="d0563-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="d0563-227">Simular una notificación de inserción del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="d0563-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="d0563-228">Con el PWA abierto en `http://localhost:3000` el explorador, seleccione `F12` para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="d0563-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="d0563-229">Elija **Inserción**del trabajador del servicio de  >  \*\*\*\*  >  \*\*\*\* aplicación para enviar una notificación de inserción de prueba a su PWA.</span><span class="sxs-lookup"><span data-stu-id="d0563-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="d0563-230">Una notificación de inserción debe mostrarse cerca de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="d0563-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Insertar una notificación desde DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="d0563-232">Insertar una notificación desde DevTools</span><span class="sxs-lookup"><span data-stu-id="d0563-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="d0563-233">Si no seleccionas \(o activate\) una notificación del sistema, el sistema la descarta automáticamente después de varios segundos y la pone en cola en el Centro de acciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="d0563-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificaciones en el Centro de acciones de Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="d0563-235">Notificaciones en el Centro de acciones de Windows</span><span class="sxs-lookup"><span data-stu-id="d0563-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="d0563-236">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="d0563-236">Next steps</span></span>  

<span data-ttu-id="d0563-237">Los siguientes pasos incluyen tareas adicionales que le ayudarán a comprender la creación de pwas reales.</span><span class="sxs-lookup"><span data-stu-id="d0563-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="d0563-238">Administrar y almacenar suscripciones de inserción</span><span class="sxs-lookup"><span data-stu-id="d0563-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="d0563-239">[Cifrar datos][NPMWebPushEncrypt] de carga útil</span><span class="sxs-lookup"><span data-stu-id="d0563-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="d0563-240">Diseño adaptativo</span><span class="sxs-lookup"><span data-stu-id="d0563-240">Responsive design</span></span>  
*   <span data-ttu-id="d0563-241">Vinculación profunda</span><span class="sxs-lookup"><span data-stu-id="d0563-241">Deep-linking</span></span>  
*   [<span data-ttu-id="d0563-242">Pruebas entre exploradores</span><span class="sxs-lookup"><span data-stu-id="d0563-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="d0563-243">Implementar prácticas de validación y pruebas como [Webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="d0563-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="d0563-244">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d0563-244">See also</span></span>  

*   [<span data-ttu-id="d0563-245">Aplicaciones web progresivas en documentos web de MDN</span><span class="sxs-lookup"><span data-stu-id="d0563-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="d0563-246">Aplicaciones web progresivas en web.dev</span><span class="sxs-lookup"><span data-stu-id="d0563-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="d0563-247">[Lectores de noticias de][HackerNewsProgressiveWebApps] hacker como aplicaciones web progresivas: compara diferentes marcos y patrones de rendimiento para implementar un PWA de ejemplo \(Lector de noticias de hacker\).</span><span class="sxs-lookup"><span data-stu-id="d0563-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="d0563-248">PwAs de descomisado de mitos</span><span class="sxs-lookup"><span data-stu-id="d0563-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="d0563-249">Una guía básica progresiva para la aplicación web progresiva</span><span class="sxs-lookup"><span data-stu-id="d0563-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="d0563-250">POST sin conexión con aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="d0563-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="d0563-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="d0563-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="d0563-252">Apuestas en la Web</span><span class="sxs-lookup"><span data-stu-id="d0563-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="d0563-253">Nomenclatura de aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="d0563-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="d0563-254">Diseño y creación de una aplicación web progresiva sin marco (parte 1)</span><span class="sxs-lookup"><span data-stu-id="d0563-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="d0563-255">Diseño y creación de una aplicación web progresiva sin marco (parte 2)</span><span class="sxs-lookup"><span data-stu-id="d0563-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="d0563-256">Diseño y creación de una aplicación web progresiva sin un marco (parte 3)</span><span class="sxs-lookup"><span data-stu-id="d0563-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implementar una aplicación Node.js en Azure con Visual Studio código | Microsoft Docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Crear una cuenta gratuita de Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificaciones web en Microsoft Edge | Windows Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Pruebas de explorador de Microsoft Edge gratuitas en Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Una guía básica progresiva para la aplicación web progresiva"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PwAs de descomisado de mitos: la nueva edición perimetral"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Generador de aplicaciones express | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Nomenclatura de aplicaciones web progresivas"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lectores de noticias de hacker como aplicaciones web progresivas"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Apuestas en la Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notificaciones API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicaciones web progresivas \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Api de inserción | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de trabajo de servicio | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Uso de trabajadores de servicio | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de aplicación web | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "POST sin conexión con aplicaciones web progresivas"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Enviar notificaciones de WebPush identificadas por VAPID a través del servicio de inserción de Mozilla | Servicios de Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) - web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso: | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicaciones web progresivas"  

[PwaBuilder]: https://www.pwabuilder.com "Generador de PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | Generador de PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | Libro de recetas de ServiceWorker"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Diseño y creación de una aplicación web progresiva sin marco (parte 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Diseño y creación de una aplicación web progresiva sin marco (parte 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Diseño y creación de una aplicación web progresiva sin un marco (parte 3)"  

[VapidkeysMain]: https://vapidkeys.com "Generador de claves VAPID seguro | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicaciones web progresivas | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Mejoras progresivas | Wikipedia"  
