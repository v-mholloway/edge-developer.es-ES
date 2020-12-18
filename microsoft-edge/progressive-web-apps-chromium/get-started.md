---
description: Esta guía le ofrece información general sobre los conceptos básicos de PWA y herramientas para crear aplicaciones web progresivas (cromo) en Windows.
title: Introducción a las aplicaciones web progresivas (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto Web, trabajo de servicio, inserción
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231226"
---
# <span data-ttu-id="98967-104">Introducción a las aplicaciones web progresivas (cromo)</span><span class="sxs-lookup"><span data-stu-id="98967-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="98967-105">Las aplicaciones web progresivas \ (PWAs \) son aplicaciones web que se han [mejorado progresivamente][WikiProgressiveEnhancement].</span><span class="sxs-lookup"><span data-stu-id="98967-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="98967-106">Las mejoras progresivas incluyen características similares a las de la aplicación, como la instalación, el soporte técnico sin conexión y las notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="98967-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="98967-107">También puede empaquetar su PWA para los almacenes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="98967-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="98967-108">Entre los posibles almacenes de aplicaciones se incluyen Microsoft Store, Google Play, Mac App Store y mucho más.</span><span class="sxs-lookup"><span data-stu-id="98967-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="98967-109">Microsoft Store es el almacén de aplicaciones comerciales integrado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="98967-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="98967-110">La siguiente guía le ofrece una descripción general de los conceptos básicos de PWA mediante la creación de una aplicación web simple y su extensión como PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="98967-111">El proyecto finalizado funciona en exploradores modernos.</span><span class="sxs-lookup"><span data-stu-id="98967-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="98967-112">Puede usar [PWABuilder][PwaBuilder] para crear un nuevo PWA, mejorar su PWA existente o empaquetar su PWA para los almacenes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="98967-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="98967-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="98967-113">Prerequisites</span></span>  

*   <span data-ttu-id="98967-114">Use [código de Visual Studio][VisualstudioCodeMain] para editar el código fuente de PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="98967-115">Use [Node.js][NodejsMain] como su servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="98967-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <span data-ttu-id="98967-116">Crear una aplicación web básica</span><span class="sxs-lookup"><span data-stu-id="98967-116">Create a basic web app</span></span>  

<span data-ttu-id="98967-117">Para crear una aplicación Web vacía, siga los pasos que se indican en el [generador de aplicaciones de node Express][ExpressjsApplicationGenerator]y asigne un nombre a la aplicación `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="98967-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="98967-118">En el símbolo del sistema, ejecute los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="98967-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="98967-119">Los comandos crean una aplicación Web vacía e instalan cualquier dependencia.</span><span class="sxs-lookup"><span data-stu-id="98967-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="98967-120">Ahora tiene una aplicación web simple y funcional.</span><span class="sxs-lookup"><span data-stu-id="98967-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="98967-121">Para iniciar la aplicación Web, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="98967-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="98967-122">Ahora, vaya a `http://localhost:3000` ver su nueva aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="98967-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="98967-124">Ejecutar su nuevo PWA en localhost</span><span class="sxs-lookup"><span data-stu-id="98967-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="98967-125">Empezar a crear un PWA</span><span class="sxs-lookup"><span data-stu-id="98967-125">Get started building a PWA</span></span>  

<span data-ttu-id="98967-126">Ahora que tiene una aplicación web simple, amplíela como PWA agregando los tres requisitos para PWAs</span><span class="sxs-lookup"><span data-stu-id="98967-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="98967-127">: [Https](#step-1---use-https), un [manifiesto de la aplicación web](#step-2---create-a-web-app-manifest)y un [trabajador de servicio](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="98967-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="98967-128">Paso 1: usar HTTPS</span><span class="sxs-lookup"><span data-stu-id="98967-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="98967-129">Las partes clave de la plataforma PWA, como los [trabajos de servicio][MDNServiceWorkerApi], requieren el uso de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="98967-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="98967-130">Cuando su PWA se activa, debe publicarlo en una dirección URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="98967-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="98967-131">Para fines de depuración, Microsoft Edge también permite `http://localhost` el uso de las API de PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="98967-132">[Publique la aplicación web como un sitio activo][VisualStudioNodejsTutorialPublishAzureAppService], pero asegúrese de que su servidor está configurado para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="98967-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="98967-133">Por ejemplo, puede crear una [cuenta gratuita de Azure][AzureCreateFreeAccount].</span><span class="sxs-lookup"><span data-stu-id="98967-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="98967-134">Hospede su sitio en el [servicio de aplicaciones de Microsoft Azure][AzureWebApps] y se ofrece a través de HTTPS de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="98967-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="98967-135">La guía siguiente, `http://localhost` que se usa para crear su PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="98967-136">Paso 2: crear un manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="98967-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="98967-137">Un [manifiesto de la aplicación web][MDNWebAppManifest] es un archivo JSON que contiene metadatos sobre la aplicación, como el nombre, la descripción, los iconos, etc.</span><span class="sxs-lookup"><span data-stu-id="98967-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="98967-138">Para agregar un manifiesto de la aplicación a la aplicación web:</span><span class="sxs-lookup"><span data-stu-id="98967-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="98967-139">En Visual Studio Code, seleccione **archivo**  >  **Abrir carpeta** y elija el `MySamplePwa` directorio que creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="98967-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="98967-140">Seleccione `Ctrl` + `N` para crear un archivo nuevo y péguelo en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="98967-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="98967-141">Guarde el archivo como `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="98967-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="98967-142">Agregue una imagen del icono de la aplicación de 512x512 con el nombre `icon512.png` a `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="98967-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="98967-143">Puede usar la [imagen de ejemplo][ImagePwa] para realizar pruebas.</span><span class="sxs-lookup"><span data-stu-id="98967-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="98967-144">En Visual Studio Code, abre `/public/index.html` y agrega el siguiente fragmento de código dentro de la `<head>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="98967-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="98967-145">Paso 3: agregar un trabajo de servicio</span><span class="sxs-lookup"><span data-stu-id="98967-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="98967-146">Los trabajadores de servicios son la tecnología clave que subyace a PWAs, habilita escenarios como la compatibilidad sin conexión, el almacenamiento avanzado y la ejecución de tareas en segundo plano previamente limitadas a aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="98967-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="98967-147">Los trabajos de servicio son tareas en segundo plano que interceptan solicitudes de red de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="98967-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="98967-148">Los trabajadores de servicio intentan completar las tareas, incluso cuando su PWA no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="98967-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="98967-149">Las tareas incluyen las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="98967-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="98967-150">Dar servicio a los recursos solicitados desde una caché</span><span class="sxs-lookup"><span data-stu-id="98967-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="98967-151">Enviar notificaciones push</span><span class="sxs-lookup"><span data-stu-id="98967-151">Sending push notifications</span></span>  
*   <span data-ttu-id="98967-152">Ejecución de tareas de captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="98967-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="98967-153">Iconos de distintivos</span><span class="sxs-lookup"><span data-stu-id="98967-153">Badging icons</span></span>  
*   <span data-ttu-id="98967-154">y mucho más</span><span class="sxs-lookup"><span data-stu-id="98967-154">and more</span></span>  
    
<span data-ttu-id="98967-155">Los trabajadores del servicio se definen en un archivo especial de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98967-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="98967-156">Para obtener más información, vaya a [usar los trabajos de servicio][MDNUsingServiceWorkers] y la API de trabajo de [servicio][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="98967-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="98967-157">Para compilar un trabajo de servicio en el proyecto, use la receta de trabajo de servicio de red en la **memoria caché** del [creador de PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="98967-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="98967-158">Vaya a [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], seleccione el trabajo **de servicio caché-primer** servicio de red y seleccione el botón **Descargar** .</span><span class="sxs-lookup"><span data-stu-id="98967-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="98967-159">El archivo descargado contiene los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="98967-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="98967-160">Copie los archivos descargados en la `public` carpeta del proyecto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="98967-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="98967-161">En Visual Studio Code, abre `/public/index.html` y agrega el siguiente fragmento de código dentro de la `<head>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="98967-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="98967-162">Su aplicación web ahora tiene un trabajador de servicio que usa la primera estrategia de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="98967-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="98967-163">El trabajador de servicio nuevo primero obtiene los recursos de la caché y de la red solo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="98967-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="98967-164">Entre los recursos almacenados en caché se incluyen imágenes, JavaScript, CSS y HTML.</span><span class="sxs-lookup"><span data-stu-id="98967-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="98967-165">Use los siguientes pasos para confirmar que el trabajo de servicio se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="98967-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="98967-166">Vaya a su aplicación web con `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="98967-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="98967-167">Si la aplicación web no está disponible, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="98967-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="98967-168">En Microsoft Edge, seleccione `F12` para abrir la DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="98967-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="98967-169">Seleccione la **aplicación**y, a continuación, los **trabajadores del servicio** para ver los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="98967-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="98967-170">Si el trabajo de servicio no se muestra, actualice la página.</span><span class="sxs-lookup"><span data-stu-id="98967-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Información general del trabajo del servicio Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="98967-172">Información general del trabajo del servicio Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="98967-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="98967-173">Visualice la caché de trabajos del servicio expandiendo el **almacenamiento en caché** y seleccione **pwabuilder-precache**.</span><span class="sxs-lookup"><span data-stu-id="98967-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="98967-174">Deben mostrarse todos los recursos almacenados en la caché por el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="98967-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="98967-175">Los recursos almacenados en caché por el trabajo del servicio incluyen el icono de la aplicación, el manifiesto de la aplicación, los archivos CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98967-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Caché de trabajo de servicio en Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="98967-177">Caché de trabajo de servicio en Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="98967-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="98967-178">Pruebe su PWA como una aplicación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="98967-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="98967-179">En Microsoft Edge DevTools \ ( `F12` \), seleccione **red** y, a continuación, cambie el estado de **conexión** a **sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="98967-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="98967-181">Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="98967-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="98967-182">Actualice la aplicación y debería mostrar el mecanismo sin conexión para servir los recursos de la aplicación desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="98967-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA que se ejecuta sin conexión" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="98967-184">PWA que se ejecuta sin conexión</span><span class="sxs-lookup"><span data-stu-id="98967-184">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="98967-185">Agregar notificaciones Push a su PWA</span><span class="sxs-lookup"><span data-stu-id="98967-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="98967-186">Puede crear PWAs que admitan las notificaciones de inserción completando las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="98967-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="98967-187">Suscribirse a un servicio de mensajería mediante la [API de inserción][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="98967-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="98967-188">Mostrar un mensaje de notificación del sistema cuando se recibe un mensaje del servicio con la [API de notificaciones][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="98967-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="98967-189">Al igual que con los trabajadores del servicio, las API de notificaciones push son API basadas en estándares.</span><span class="sxs-lookup"><span data-stu-id="98967-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="98967-190">Las API de notificaciones push funcionan en todos los exploradores, por lo que el código debería funcionar siempre que se admitan PWAs.</span><span class="sxs-lookup"><span data-stu-id="98967-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="98967-191">Para obtener más información sobre cómo enviar mensajes Push a diferentes exploradores de su servidor, vaya a inserción en la [Web][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="98967-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="98967-192">Los siguientes pasos han sido adaptados desde la demostración de inserción enriquecida en el [manual de trabajos de trabajo][ServiceWorkerCookbookPushRichDemo] de Mozilla, que tiene varias otras recetas útiles de inserción de web y de trabajadores de servicios.</span><span class="sxs-lookup"><span data-stu-id="98967-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="98967-193">Paso 1: generar claves VAPID</span><span class="sxs-lookup"><span data-stu-id="98967-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="98967-194">Las notificaciones push requieren claves de VAPID \ (identificación de servidor de aplicaciones voluntaria \) para poder enviar mensajes Push al cliente de PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="98967-195">Hay varios generadores de claves de VAPID disponibles en línea \ (por ejemplo, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="98967-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="98967-196">Después de la generación, debe obtener un objeto JSON que contenga una clave pública y privada.</span><span class="sxs-lookup"><span data-stu-id="98967-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="98967-197">Guarde las teclas para pasos posteriores en el siguiente tutorial.</span><span class="sxs-lookup"><span data-stu-id="98967-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="98967-198">Para obtener más información sobre VAPID y webpush, vaya al [envío de VAPID de notificaciones de webpush identificadas con el servicio de inserción de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="98967-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="98967-199">Paso 2: suscribirse a notificaciones push</span><span class="sxs-lookup"><span data-stu-id="98967-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="98967-200">Los trabajos del servicio controlan los eventos Push y las interacciones de notificaciones del sistema en tu PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="98967-201">Para suscribir las notificaciones push de PWA a Server, asegúrese de que se cumplan las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="98967-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="98967-202">PWA está instalado, activo y registrado</span><span class="sxs-lookup"><span data-stu-id="98967-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="98967-203">El código para completar la tarea de suscripción se encuentra en el subproceso de la interfaz de usuario principal del PWA</span><span class="sxs-lookup"><span data-stu-id="98967-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="98967-204">Tiene conectividad de red</span><span class="sxs-lookup"><span data-stu-id="98967-204">You have network connectivity</span></span>  
    
<span data-ttu-id="98967-205">Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario ha concedido permiso de PWA para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="98967-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="98967-206">En caso contrario, el explorador le pide permiso para el usuario.</span><span class="sxs-lookup"><span data-stu-id="98967-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="98967-207">Si el permiso es denegado, la solicitud para `registration.pushManager.subscribe` iniciar una `DOMException` , que se debe controlar.</span><span class="sxs-lookup"><span data-stu-id="98967-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="98967-208">Para obtener más información sobre la administración de permisos, vaya a [notificaciones Push en Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="98967-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="98967-209">En el `pwabuilder-sw-register.js` archivo, Anexe el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="98967-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="98967-210">Para obtener más información, vaya a [PushManager][MDNPushManager] y [inserción web][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="98967-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="98967-211">Paso 3: escuchar las notificaciones push</span><span class="sxs-lookup"><span data-stu-id="98967-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="98967-212">Después de crear una suscripción en PWA, agregue controladores al trabajo del servicio para responder a los eventos Push.</span><span class="sxs-lookup"><span data-stu-id="98967-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="98967-213">El evento Push se envía desde el servidor para mostrar las notificaciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="98967-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="98967-214">Las notificaciones del sistema muestran los datos de un mensaje recibido.</span><span class="sxs-lookup"><span data-stu-id="98967-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="98967-215">Para completar las siguientes tareas, debe agregar un controlador de clics.</span><span class="sxs-lookup"><span data-stu-id="98967-215">To complete the following tasks, you must add a click handler.</span></span>  

*   <span data-ttu-id="98967-216">Descartar la notificación del sistema</span><span class="sxs-lookup"><span data-stu-id="98967-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="98967-217">Abrir, enfocar o abrir y enfocar cualquier ventana abierta</span><span class="sxs-lookup"><span data-stu-id="98967-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="98967-218">Abrir y enfocar una nueva ventana para mostrar una página de cliente de PWA</span><span class="sxs-lookup"><span data-stu-id="98967-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="98967-219">En el `pwabuilder-sw.js` archivo, agregue los siguientes controladores.</span><span class="sxs-lookup"><span data-stu-id="98967-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <span data-ttu-id="98967-220">Paso 4: pruébelo</span><span class="sxs-lookup"><span data-stu-id="98967-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="98967-221">Siga los pasos que se indican a continuación para probar las notificaciones push para su PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="98967-222">Vaya a su PWA en `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="98967-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="98967-223">Cuando el trabajador de servicio se activa e intenta suscribirse a las notificaciones push de PWA, Microsoft Edge le pide que permita a su PWA Mostrar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="98967-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="98967-224">Seleccione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="98967-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Cuadro de diálogo de permisos para habilitar las notificaciones" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="98967-226">Cuadro de diálogo de permisos para habilitar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="98967-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="98967-227">Simular una notificación de inserción del servidor.</span><span class="sxs-lookup"><span data-stu-id="98967-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="98967-228">Con el PWA abierto en `http://localhost:3000` en el explorador, seleccione `F12` para abrir el DevTools.</span><span class="sxs-lookup"><span data-stu-id="98967-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="98967-229">Elija \*\*\*\*  >  \*\*\*\*  >  **Push** de trabajo de servicio de aplicaciones para enviar una notificación de inserción de prueba a su PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="98967-230">Una notificación de inserción debe mostrarse cerca de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="98967-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Insertar una notificación desde DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="98967-232">Insertar una notificación desde DevTools</span><span class="sxs-lookup"><span data-stu-id="98967-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="98967-233">Si no selecciona \ (o activa \) una notificación del sistema, el sistema la descarta automáticamente después de varios segundos y la coloca en la cola del centro de actividades de Windows.</span><span class="sxs-lookup"><span data-stu-id="98967-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificaciones en el centro de actividades de Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="98967-235">Notificaciones en el centro de actividades de Windows</span><span class="sxs-lookup"><span data-stu-id="98967-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="98967-236">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="98967-236">Next steps</span></span>  

<span data-ttu-id="98967-237">Los pasos siguientes incluyen tareas adicionales para ayudarle a comprender la creación de PWAs del mundo real.</span><span class="sxs-lookup"><span data-stu-id="98967-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="98967-238">Administrar y almacenar suscripciones de inserción</span><span class="sxs-lookup"><span data-stu-id="98967-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="98967-239">[Cifrar][NPMWebPushEncrypt] datos de carga</span><span class="sxs-lookup"><span data-stu-id="98967-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="98967-240">Diseño adaptativo</span><span class="sxs-lookup"><span data-stu-id="98967-240">Responsive design</span></span>  
*   <span data-ttu-id="98967-241">Vínculos profundos</span><span class="sxs-lookup"><span data-stu-id="98967-241">Deep-linking</span></span>  
*   [<span data-ttu-id="98967-242">Pruebas entre exploradores</span><span class="sxs-lookup"><span data-stu-id="98967-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="98967-243">Implementar procedimientos de validación y pruebas, como [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="98967-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <span data-ttu-id="98967-244">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98967-244">See also</span></span>  

*   [<span data-ttu-id="98967-245">Aplicaciones web progresivas en documentos web de MDN</span><span class="sxs-lookup"><span data-stu-id="98967-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="98967-246">Aplicaciones web progresivas en Web. dev</span><span class="sxs-lookup"><span data-stu-id="98967-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="98967-247">[Lectores de noticias de piratas informáticos como aplicaciones web progresivas][HackerNewsProgressiveWebApps] : compara diferentes marcos de trabajo y patrones de rendimiento para implementar un ejemplo \ (lector de noticias de hacker \) PWA.</span><span class="sxs-lookup"><span data-stu-id="98967-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="98967-248">PWAs de mitos</span><span class="sxs-lookup"><span data-stu-id="98967-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="98967-249">Una guía básica para la aplicación web progresiva</span><span class="sxs-lookup"><span data-stu-id="98967-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="98967-250">Publicaciones sin conexión con aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="98967-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="98967-251">Q&A DE PWA</span><span class="sxs-lookup"><span data-stu-id="98967-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="98967-252">Apuestas en la web</span><span class="sxs-lookup"><span data-stu-id="98967-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="98967-253">Asignar nombres a aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="98967-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="98967-254">Diseñar y crear una aplicación web progresiva sin un marco (parte 1)</span><span class="sxs-lookup"><span data-stu-id="98967-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="98967-255">Diseñar y crear una aplicación web progresiva sin un marco (parte 2)</span><span class="sxs-lookup"><span data-stu-id="98967-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="98967-256">Diseñar y crear una aplicación web progresiva sin un marco (parte 3)</span><span class="sxs-lookup"><span data-stu-id="98967-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implementar una aplicación de Node.js en Azure con Visual Studio Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Crear cuenta gratuita de Azure Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicaciones Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificaciones Web en Microsoft Edge | Blogs de Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "Q&A DE PWA"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Pruebas gratuitas del navegador Microsoft Edge en Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Una guía básica para la aplicación web progresiva"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs de mitos: la nueva edición de Edge"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Generador de aplicaciones Express | Explícita" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Asignar nombres a aplicaciones web progresivas"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lectores de noticias de piratas informáticos como aplicaciones web progresivas"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Apuestas en la web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicaciones web progresivas \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabajadores de servicio | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de la aplicación Web | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Publicaciones sin conexión con aplicaciones web progresivas"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envío de notificaciones por inserción de VAPID identificadas por el servicio de inserción de Mozilla | Servicios de Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-insertar | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, payload, contentEncoding)-web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso-web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicaciones web progresivas"  

[PwaBuilder]: https://www.pwabuilder.com "Creador de PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Trabajo del servicio | Creador de PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Demostración de inserción enriquecida | ServiceWorker"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Diseñar y crear una aplicación web progresiva sin un marco (parte 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Diseñar y crear una aplicación web progresiva sin un marco (parte 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Diseñar y crear una aplicación web progresiva sin un marco (parte 3)"  

[VapidkeysMain]: https://vapidkeys.com "Generador de claves de VAPID seguro | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicaciones web progresivas | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Mejora progresiva | Wikipedia"  
