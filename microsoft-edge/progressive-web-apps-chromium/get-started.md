---
description: Esta guía le ofrece información general sobre los conceptos básicos de PWA y herramientas para crear aplicaciones web progresivas en Windows.
title: Introducción a las aplicaciones web progresivas (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto Web, trabajo de servicio, inserción
ms.openlocfilehash: a9a0cad2d771e52b783053e36f0f23dec5d8e70c
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894713"
---
# <span data-ttu-id="2af25-104">Introducción a las aplicaciones web progresivas (cromo)</span><span class="sxs-lookup"><span data-stu-id="2af25-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="2af25-105">Las aplicaciones web progresivas \ (PWAs \) son aplicaciones web que se han [mejorado progresivamente][WikiProgressiveEnhancement] con características de tipo aplicación, como la instalación, el soporte técnico sin conexión y las notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="2af25-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement] with app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="2af25-106">También puede haber empaquetado su PWA para los almacenes de aplicaciones, incluyendo Microsoft Store, así como Google Play, Mac App Store y mucho más.</span><span class="sxs-lookup"><span data-stu-id="2af25-106">You may also packaged your PWA for app stores, including the Microsoft Store as well as Google Play, Mac App Store and more.</span></span>  <span data-ttu-id="2af25-107">Microsoft Store es el almacén de aplicaciones comerciales integrado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2af25-107">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="2af25-108">La siguiente guía le ofrece una descripción general de los conceptos básicos de PWA mediante la creación de una aplicación web simple y su extensión como PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-108">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="2af25-109">El proyecto finalizado funciona en exploradores modernos.</span><span class="sxs-lookup"><span data-stu-id="2af25-109">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="2af25-110">Puede usar [PWABuilder][PwaBuilder] para crear un nuevo PWA, mejorar su PWA existente o empaquetar su PWA para los almacenes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2af25-110">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="2af25-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2af25-111">Prerequisites</span></span>  

*   <span data-ttu-id="2af25-112">Use [código de vs][VisualstudioCodeMain] para editar el código fuente de PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-112">Use [VS Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="2af25-113">Use [Node.js][NodejsMain] como su servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="2af25-113">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="2af25-114">Configurar una aplicación web básica</span><span class="sxs-lookup"><span data-stu-id="2af25-114">Set up a basic web app</span></span>  

<span data-ttu-id="2af25-115">Para crear una aplicación Web vacía, siga los pasos que se indican en el [generador de aplicaciones de node Express][ExpressjsApplicationGenerator]y asigne un nombre a la aplicación `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="2af25-115">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="2af25-116">En el símbolo del sistema, ejecute los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="2af25-116">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="2af25-117">Los comandos crean una aplicación Web vacía e instalan cualquier dependencia.</span><span class="sxs-lookup"><span data-stu-id="2af25-117">The commands creates an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="2af25-118">Ahora tiene una aplicación web simple y funcional.</span><span class="sxs-lookup"><span data-stu-id="2af25-118">Now you have a simple, functional web app.</span></span>  <span data-ttu-id="2af25-119">Para iniciarlo, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="2af25-119">To start it, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="2af25-120">Ahora, vaya a `http://localhost:3000` ver su nueva aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="2af25-120">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ejecutar su nuevo PWA en localhost":::
   <span data-ttu-id="2af25-122">Ejecutar su nuevo PWA en localhost</span><span class="sxs-lookup"><span data-stu-id="2af25-122">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="2af25-123">Empezar a crear un PWA</span><span class="sxs-lookup"><span data-stu-id="2af25-123">Get started building a PWA</span></span>  

<span data-ttu-id="2af25-124">Ahora que tiene una aplicación web simple, amplíela como PWA agregando los 3 requisitos para PWAs</span><span class="sxs-lookup"><span data-stu-id="2af25-124">Now that you have a simple web app, extend it as a PWA by adding the 3 requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="2af25-125">: [Https](#step-1---use-https), un [manifiesto de la aplicación web](#step-2---create-a-web-app-manifest)y un [trabajador de servicio](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="2af25-125">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="2af25-126">Paso 1: usar HTTPS</span><span class="sxs-lookup"><span data-stu-id="2af25-126">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="2af25-127">Las partes clave de la plataforma PWA, como los [trabajos de servicio][MDNServiceWorkerApi], requieren el uso de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2af25-127">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="2af25-128">Cuando su PWA se activa, debe publicarlo en una dirección URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2af25-128">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="2af25-129">Para fines de depuración, Microsoft Edge también permite `http://localhost` el uso de las API de PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-129">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="2af25-130">Si [publica la aplicación web como un sitio activo][VisualStudioNodejsTutorialPublishAzureAppService] \ (por ejemplo, al configurar una [cuenta gratuita de Azure][AzureCreateFreeAccount]), debe asegurarse de que su servidor está configurado para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2af25-130">If you [publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="2af25-131">Si usa el [servicio de aplicaciones de Microsoft Azure][AzureWebApps] para hospedar su sitio, se ofrece a través de HTTPS de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2af25-131">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="2af25-132">La guía siguiente, `http://localhost` que se usa para crear su PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-132">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="2af25-133">Paso 2: crear un manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="2af25-133">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="2af25-134">Un [manifiesto de la aplicación web][MDNWebAppManifest] es un archivo JSON que contiene metadatos sobre la aplicación, como el nombre, la descripción, los iconos, etc.</span><span class="sxs-lookup"><span data-stu-id="2af25-134">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="2af25-135">Para agregar un manifiesto de la aplicación a la aplicación web:</span><span class="sxs-lookup"><span data-stu-id="2af25-135">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="2af25-136">En vs Code, vaya **File**  >  a la**carpeta abrir** archivo y elija el `MySamplePwa` directorio que creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2af25-136">In VS Code, go **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="2af25-137">Presione `Ctrl` + `N` para crear un archivo nuevo y péguelo en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="2af25-137">Press `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="2af25-138">Guarde el archivo como `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="2af25-138">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="2af25-139">Agregue una imagen del icono de la aplicación de 512x512 con el nombre `icon512.png` a `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="2af25-139">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="2af25-140">Puede usar la [imagen de ejemplo][ImagePwa] para realizar pruebas.</span><span class="sxs-lookup"><span data-stu-id="2af25-140">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="2af25-141">En VS Code, Abra `/public/index.html` y agregue el siguiente fragmento de código dentro de la `<head>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2af25-141">In VS Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="2af25-142">Paso 3: agregar un trabajo de servicio</span><span class="sxs-lookup"><span data-stu-id="2af25-142">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="2af25-143">Los trabajadores de servicios son la tecnología clave que subyace a PWAs, habilita escenarios como la compatibilidad sin conexión, el almacenamiento avanzado y la ejecución de tareas en segundo plano previamente limitadas a aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="2af25-143">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="2af25-144">Los trabajos de servicio son tareas en segundo plano que interceptan solicitudes de red de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="2af25-144">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="2af25-145">Realizan tareas, incluso si su PWA no se está ejecutando, como servir recursos solicitados de una caché, enviar notificaciones push, ejecutar tareas de captura en segundo plano, iconos de distintivos, etc.</span><span class="sxs-lookup"><span data-stu-id="2af25-145">They perform tasks, even when your PWA is not running, such as serving requested resources from a cache, sending push notifications, running background fetch tasks, badging icons, and so on.</span></span>  <span data-ttu-id="2af25-146">Los trabajadores del servicio se definen en un archivo especial de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2af25-146">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="2af25-147">Para obtener más información, vea [usar trabajadores de servicio][MDNUsingServiceWorkers] y [API de trabajo de servicio][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="2af25-147">For more information, see [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="2af25-148">Para compilar un trabajo de servicio en el proyecto, use la receta de trabajo de servicio de red en la **memoria caché** del [creador de PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="2af25-148">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="2af25-149">Vaya a [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], seleccione el trabajo **de servicio caché-primer** servicio de red y seleccione el botón **Descargar** .</span><span class="sxs-lookup"><span data-stu-id="2af25-149">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="2af25-150">El archivo descargado contiene los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="2af25-150">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="2af25-151">Copie los archivos descargados en la `public` carpeta del proyecto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="2af25-151">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="2af25-152">En VS Code, Abra `/public/index.html` y agregue el siguiente fragmento de código dentro de la `<head>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2af25-152">In VS Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="2af25-153">Su aplicación web ahora tiene un trabajador de servicio que usa la primera estrategia de almacenamiento en caché, que recupera los recursos como imágenes, JS, CSS y HTML en primer lugar de la caché, y retrocede a la red según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2af25-153">Your web app now has a service worker that uses the cache-first strategy, which fetches resources like images, JS, CSS, and HTML from the cache first, and falls back to the network as needed.</span></span>  

<span data-ttu-id="2af25-154">Use los siguientes pasos para confirmar que el trabajo de servicio se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="2af25-154">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="2af25-155">Vaya a su aplicación web con `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="2af25-155">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="2af25-156">Si la aplicación web no está disponible, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="2af25-156">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="2af25-157">En Microsoft Edge, seleccione `F12` para abrir la DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2af25-157">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="2af25-158">Seleccione la **aplicación**y, a continuación, los **trabajadores del servicio** para ver los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="2af25-158">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="2af25-159">Si no ve el trabajo de servicio, es posible que tenga que actualizar la página.</span><span class="sxs-lookup"><span data-stu-id="2af25-159">If you do not see the service worker, you may need to refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Información general del trabajo del servicio Microsoft Edge DevTools":::
       <span data-ttu-id="2af25-161">Información general del trabajo del servicio Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2af25-161">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="2af25-162">Visualice la caché de trabajos del servicio expandiendo el **almacenamiento en caché** y seleccione **pwabuilder-precache**.</span><span class="sxs-lookup"><span data-stu-id="2af25-162">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="2af25-163">Debería ver todos los recursos almacenados en caché por el trabajo del servicio, como el icono de la aplicación, el manifiesto de la aplicación, los archivos CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2af25-163">You should see all the resources cached by the service worker, such as the app icon, app manifest, CSS and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Caché de trabajo de servicio en Microsoft Edge DevTools":::
       <span data-ttu-id="2af25-165">Caché de trabajo de servicio en Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="2af25-165">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="2af25-166">Pruebe su PWA como una aplicación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2af25-166">Try your PWA as an offline app.</span></span>  <span data-ttu-id="2af25-167">En Microsoft Edge DevTools \ ( `F12` \), seleccione **red** y, a continuación, cambie el estado de **conexión** a **sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="2af25-167">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools":::
       <span data-ttu-id="2af25-169">Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2af25-169">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="2af25-170">Actualice la aplicación y verá que se está trabajando sin conexión atendiendo los recursos de la aplicación desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="2af25-170">Refresh your app and you should see it working offline by serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA que se ejecuta sin conexión":::
       <span data-ttu-id="2af25-172">PWA que se ejecuta sin conexión</span><span class="sxs-lookup"><span data-stu-id="2af25-172">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="2af25-173">Agregar notificaciones Push a su PWA</span><span class="sxs-lookup"><span data-stu-id="2af25-173">Add push notifications to your PWA</span></span>  

<span data-ttu-id="2af25-174">Puede crear PWAs que admitan las notificaciones de inserción completando las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="2af25-174">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="2af25-175">Suscribirse a un servicio de mensajería mediante la [API de inserción][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="2af25-175">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="2af25-176">Mostrar un mensaje de notificación del sistema cuando se recibe un mensaje del servicio con la [API de notificaciones][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="2af25-176">Display a toast messages when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  

<span data-ttu-id="2af25-177">Al igual que con los trabajadores del servicio, estas son API basadas en estándares que funcionan en exploradores, de modo que solo tienes que escribir el código una vez para que funcione en todos los casos en que PWAs sea compatible.</span><span class="sxs-lookup"><span data-stu-id="2af25-177">As with Service Workers, these are standards-based APIs that work across browsers, so you only have to write the code once for it to work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="2af25-178">Para obtener más información sobre cómo entregar mensajes Push a diferentes exploradores de su servidor, use la biblioteca de código abierto de [inserción web][NPMWebPush] .</span><span class="sxs-lookup"><span data-stu-id="2af25-178">For more information on delivering push messages to different browsers on your server, use the [Web-Push][NPMWebPush] open-source library.</span></span>  

<span data-ttu-id="2af25-179">Los siguientes pasos han sido adaptados desde la demostración de inserción enriquecida en el [manual de trabajos de trabajo][ServiceWorkerCookbookPushRichDemo] de Mozilla, que tiene varias otras recetas útiles de inserción de web y de trabajadores de servicios.</span><span class="sxs-lookup"><span data-stu-id="2af25-179">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="2af25-180">Paso 1: generar claves VAPID</span><span class="sxs-lookup"><span data-stu-id="2af25-180">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="2af25-181">Las notificaciones push requieren claves de VAPID \ (identificación de servidor de aplicaciones voluntaria \) para poder enviar mensajes Push al cliente de PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-181">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="2af25-182">Hay varios generadores de claves de VAPID disponibles en línea \ (por ejemplo, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="2af25-182">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="2af25-183">Después de la generación, debe obtener un objeto JSON que contenga una clave pública y privada.</span><span class="sxs-lookup"><span data-stu-id="2af25-183">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="2af25-184">Guarde las claves para los pasos siguientes en el siguiente tutorial.</span><span class="sxs-lookup"><span data-stu-id="2af25-184">Save the keys for subsequent steps in the following tutorial.</span></span>  <span data-ttu-id="2af25-185">Para obtener información sobre el funcionamiento de VAPID y webpush, consulte [envío de notificaciones de webpush identificadas por el servicio de inserción de VAPID][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="2af25-185">For information on how VAPID and WebPush works, see [Sending VAPID identified WebPush Notifications via Mozilla's Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="2af25-186">Paso 2: suscribirse a notificaciones push</span><span class="sxs-lookup"><span data-stu-id="2af25-186">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="2af25-187">Los trabajos del servicio controlan los eventos Push y las interacciones de notificaciones del sistema en tu PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-187">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="2af25-188">Para suscribir las notificaciones push de PWA a Server, asegúrese de que se cumplan las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="2af25-188">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="2af25-189">PWA está instalado, activo y registrado</span><span class="sxs-lookup"><span data-stu-id="2af25-189">Your PWA is installed, active and registered</span></span>  
*   <span data-ttu-id="2af25-190">El código que realiza la tarea de suscripción se encuentra en el subproceso de la interfaz de usuario principal del PWA</span><span class="sxs-lookup"><span data-stu-id="2af25-190">Your code that performs the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="2af25-191">Tiene conectividad de red</span><span class="sxs-lookup"><span data-stu-id="2af25-191">You have network connectivity</span></span>  

<span data-ttu-id="2af25-192">Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario ha concedido permiso de PWA para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2af25-192">Before a new push subscription is created, Microsoft Edge checks if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="2af25-193">En caso contrario, el explorador le pide permiso para el usuario.</span><span class="sxs-lookup"><span data-stu-id="2af25-193">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="2af25-194">Si el permiso es denegado, la solicitud para `registration.pushManager.subscribe` iniciar una `DOMException` , que se debe controlar.</span><span class="sxs-lookup"><span data-stu-id="2af25-194">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="2af25-195">Para obtener más información sobre la administración de permisos, vea [notificaciones Push en Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="2af25-195">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="2af25-196">En el `pwabuilder-sw-register.js` archivo, Anexe el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="2af25-196">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="2af25-197">Para obtener más información, consulte [PushManager][MDNPushManager] y [inserción web][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="2af25-197">For more information, see [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="2af25-198">Paso 3: escuchar las notificaciones push</span><span class="sxs-lookup"><span data-stu-id="2af25-198">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="2af25-199">Ahora que se ha configurado una suscripción en PWA, agregue controladores al trabajo del servicio para responder a los eventos Push \ (enviados desde el servidor \) para mostrar las notificaciones del sistema con los datos de un mensaje recibido.</span><span class="sxs-lookup"><span data-stu-id="2af25-199">Now that a subscription is set up in your PWA, add handlers to the service worker to respond to push events \(sent from the server\) to display toast notifications with the data of a received message.</span></span>  <span data-ttu-id="2af25-200">Debes agregar un controlador de clics para realizar cualquiera de las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="2af25-200">You must add a click handler to perform the any of the following tasks.</span></span>  
*   <span data-ttu-id="2af25-201">descartar la notificación del sistema</span><span class="sxs-lookup"><span data-stu-id="2af25-201">dismiss the toast notification</span></span>  
*   <span data-ttu-id="2af25-202">abrir, enfocar o abrir y enfocar cualquier ventana abierta</span><span class="sxs-lookup"><span data-stu-id="2af25-202">open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="2af25-203">abrir y enfocar una nueva ventana para mostrar una página de cliente de PWA</span><span class="sxs-lookup"><span data-stu-id="2af25-203">open and focus a new window to display a PWA client page</span></span>  

<span data-ttu-id="2af25-204">En el `pwabuilder-sw.js` archivo, agregue los siguientes controladores.</span><span class="sxs-lookup"><span data-stu-id="2af25-204">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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
    
    // This looks to see if the current notification is already open and focuses it.
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

### <span data-ttu-id="2af25-205">Paso 4: pruébelo</span><span class="sxs-lookup"><span data-stu-id="2af25-205">Step 4 - Try it out</span></span>  

<span data-ttu-id="2af25-206">Realice los siguientes pasos para probar las notificaciones Push en su PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-206">Perform the following steps to test push notifications in your PWA.</span></span>  

1.  <span data-ttu-id="2af25-207">Vaya a su PWA en `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="2af25-207">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="2af25-208">Cuando el trabajador de servicio se activa e intenta suscribirse a las notificaciones push de PWA, Microsoft Edge le pide que permita a su PWA Mostrar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2af25-208">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="2af25-209">Seleccione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="2af25-209">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Cuadro de diálogo de permisos para habilitar las notificaciones":::
       <span data-ttu-id="2af25-211">Cuadro de diálogo de permisos para habilitar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="2af25-211">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
    
1.  <span data-ttu-id="2af25-212">Simular una notificación de inserción del servidor.</span><span class="sxs-lookup"><span data-stu-id="2af25-212">Simulate a server-side push notification.</span></span>  <span data-ttu-id="2af25-213">Con el PWA abierto en `http://localhost:3000` en el explorador, seleccione `F12` para abrir el DevTools.</span><span class="sxs-lookup"><span data-stu-id="2af25-213">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="2af25-214">Elija **Application**  >  **Service Worker**  >  **Push** de trabajo de servicio de aplicaciones para enviar una notificación de inserción de prueba a su PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-214">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  <span data-ttu-id="2af25-215">Debería ver una notificación de inserción cerca de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="2af25-215">You should see a push notification appear near the taskbar.</span></span>  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Insertar una notificación desde DevTools":::
       <span data-ttu-id="2af25-217">Insertar una notificación desde DevTools</span><span class="sxs-lookup"><span data-stu-id="2af25-217">Push a notification from DevTools</span></span>
    :::image-end:::
     
    <span data-ttu-id="2af25-218">Si no selecciona \ (o activa \) una notificación del sistema, se descarta después de varios segundos y se pone en cola en el centro de actividades de Windows.</span><span class="sxs-lookup"><span data-stu-id="2af25-218">If you do not select \(or activate\) a toast notification, it is dismissed after several seconds and queues up in your Windows Action Center.</span></span>  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificaciones en el centro de actividades de Windows":::
       <span data-ttu-id="2af25-220">Notificaciones en el centro de actividades de Windows</span><span class="sxs-lookup"><span data-stu-id="2af25-220">Notifications in Windows Action Center</span></span>
    :::image-end:::
    
    
## <span data-ttu-id="2af25-221">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="2af25-221">Next steps</span></span>  

<span data-ttu-id="2af25-222">A continuación se muestra una lista de tareas adicionales para aprender a crear PWAs del mundo real:</span><span class="sxs-lookup"><span data-stu-id="2af25-222">The following is a list of additional tasks to learn when building real-world PWAs:</span></span>  

*  <span data-ttu-id="2af25-223">Administrar y almacenar suscripciones de inserción</span><span class="sxs-lookup"><span data-stu-id="2af25-223">Manage and store push subscriptions</span></span>  
*  <span data-ttu-id="2af25-224">[Cifrar][NPMWebPushEncrypt] datos de carga</span><span class="sxs-lookup"><span data-stu-id="2af25-224">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*  <span data-ttu-id="2af25-225">Diseño adaptativo</span><span class="sxs-lookup"><span data-stu-id="2af25-225">Responsive design</span></span>  
*  <span data-ttu-id="2af25-226">Vínculos profundos</span><span class="sxs-lookup"><span data-stu-id="2af25-226">Deep-linking</span></span>  
*  [<span data-ttu-id="2af25-227">Pruebas entre exploradores</span><span class="sxs-lookup"><span data-stu-id="2af25-227">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*  <span data-ttu-id="2af25-228">Implementar procedimientos recomendados, como [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="2af25-228">Implement best practices such as [Webhint][Webhint]</span></span>  

## <span data-ttu-id="2af25-229">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2af25-229">See also</span></span>  

*   <span data-ttu-id="2af25-230">[Aplicaciones web progresivas en documentos web de MDN][MDNProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="2af25-230">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps].</span></span>  
*   <span data-ttu-id="2af25-231">[Aplicaciones web progresivas en Web. dev][WebDevProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="2af25-231">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps].</span></span>  
*   <span data-ttu-id="2af25-232">[Lectores de noticias de piratas informáticos como aplicaciones web progresivas][HackerNewsProgressiveWebApps] : compara diferentes marcos de trabajo y patrones de rendimiento para implementar un ejemplo \ (lector de noticias de hacker \) PWA.</span><span class="sxs-lookup"><span data-stu-id="2af25-232">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implementar una aplicación de Node.js en Azure con VS Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Crear cuenta gratuita de Azure Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicaciones Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificaciones Web en Microsoft Edge | Blogs de Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Código de Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Pruebas gratuitas del navegador Microsoft Edge en Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Generador de aplicaciones Express | Explícita" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lectores de noticias de piratas informáticos como aplicaciones web progresivas"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicaciones web progresivas \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabajadores de servicio | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de la aplicación Web | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envío de notificaciones por inserción de VAPID identificadas por el servicio de inserción de Mozilla | Servicios de Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-insertar | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, payload, contentEncoding)-web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso-web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicaciones web progresivas"  

[PwaBuilder]: https://www.pwabuilder.com "Creador de PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Trabajo del servicio | Creador de PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Demostración de inserción enriquecida | ServiceWorker"  

[VapidkeysMain]: https://vapidkeys.com "Generador de claves de VAPID seguro | VapidKeys" 

[Webhint]: https://sonarwhal.com "webhint, el motor de sugerencias para los procedimientos recomendados para Web"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicaciones web progresivas | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Mejora progresiva | Wikipedia"  
