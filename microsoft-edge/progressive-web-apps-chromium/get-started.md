---
description: En esta guía se ofrece información general sobre los conceptos básicos y las herramientas de PWA para crear aplicaciones web progresivas (Chromium) en Windows.
title: Introducción a Las aplicaciones web progresivas (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto web, trabajador de servicio, inserción
ms.openlocfilehash: 3023c38790185ca6989f4a487928abc79b1d5a2c
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480198"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a>Introducción a Las aplicaciones web progresivas (Chromium)  

Las aplicaciones web progresivas \(PWAs\) son aplicaciones web que se mejoran [progresivamente.][WikiProgressiveEnhancement]  Las mejoras progresivas incluyen características como aplicaciones, como la instalación, la compatibilidad sin conexión y las notificaciones de inserción.  También puedes empaquetar tu PWA para almacenes de aplicaciones.  Entre las posibles tiendas de aplicaciones se incluyen Microsoft Store, Google Play, Mac App Store y mucho más.  Microsoft Store es la tienda de aplicaciones comercial integrada en Windows 10.  

En la siguiente guía se ofrece información general sobre los conceptos básicos de PWA mediante la creación de una aplicación web sencilla y su extensión como PWA.  El proyecto terminado funciona en exploradores modernos.  

> [!TIP]
> Puedes usar [PWABuilder para][PwaBuilder] crear una PWA nueva, mejorar tu PWA existente o empaquetar tu PWA para almacenes de aplicaciones.  

## <a name="prerequisites"></a>Requisitos previos  

*   Use [Visual Studio code para][VisualstudioCodeMain] editar el código fuente de PWA.  
*   Use [Node.js][NodejsMain] como servidor web local.  
    
## <a name="create-a-basic-web-app"></a>Crear una aplicación web básica  

Para crear una aplicación web vacía, siga los pasos de [Node Express App Generator][ExpressjsApplicationGenerator]y asigne un nombre a la aplicación `MySamplePwa` .  

En el símbolo del sistema, ejecute los siguientes comandos.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Los comandos crean una aplicación web vacía e instalan cualquier dependencia.  

Ahora tienes una aplicación web sencilla y funcional.  Para iniciar la aplicación web, ejecute el siguiente comando.  

```shell
npm start
```  

Ahora vaya a `http://localhost:3000` ver la nueva aplicación web.  

:::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="Ejecutar el nuevo PWA en localhost" lightbox="./media/visual-studio-nodejs-express-index.png":::
   Ejecutar el nuevo PWA en localhost  
:::image-end:::  

## <a name="get-started-building-a-pwa"></a>Introducción a la creación de un PWA  

Ahora que tienes una aplicación web sencilla, prorrogarla como PWA agregando los tres requisitos para las PWA<!--[3 requirements for PWAs][ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]-->: [HTTPS](#step-1---use-https), un [manifiesto de aplicación web](#step-2---create-a-web-app-manifest)y un trabajador de [servicio](#step-3---add-a-service-worker).  

### <a name="step-1---use-https"></a>Paso 1: Usar HTTPS  

Las partes clave de la plataforma PWA, como [los trabajadores de][MDNServiceWorkerApi]servicio, requieren el uso de HTTPS.  Cuando el PWA entre en servicio, debes publicarlo en una dirección URL HTTPS.  

Para fines de depuración, Microsoft Edge también permite usar `http://localhost` las API de PWA.  

[Publique la aplicación web como un sitio en directo,][VisualStudioNodejsTutorialPublishAzureAppService]pero asegúrese de que el servidor está configurado para HTTPS.  Por ejemplo, puede crear una cuenta [gratuita de Azure][AzureCreateFreeAccount].  Hospedar el sitio en [el Servicio de aplicaciones de Microsoft Azure][AzureWebApps] y se sirve a través de HTTPS de forma predeterminada.  

La siguiente guía, use `http://localhost` para crear su PWA.  

### <a name="step-2---create-a-web-app-manifest"></a>Paso 2: Crear un manifiesto de aplicación web  

Un [manifiesto de aplicación web][MDNWebAppManifest] es un archivo JSON que contiene metadatos sobre la aplicación, como el nombre, la descripción, los iconos y mucho más.  

Para agregar un manifiesto de aplicación a la aplicación web:  

1.  En Visual Studio, elija **Archivo**  >  **abrir carpeta** y elija el directorio que `MySamplePwa` creó anteriormente.  
1.  Seleccione `Ctrl` + `N` para crear un nuevo archivo y pegue el siguiente fragmento de código.  
    
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
    
1.  Guarde el archivo como `/MySamplePwa/public/manifest.json` .  
1.  Agregue una imagen de icono de aplicación de 512x512 denominada `icon512.png` a `/MySamplePwa/public/images` .  Puede usar la imagen [de ejemplo con](./media/progressive-web-app.png) fines de prueba.  
1.  En Visual Studio, abra y agregue el siguiente fragmento `/public/index.html` de código dentro de la `<head>` etiqueta.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a>Paso 3: Agregar un trabajador de servicio  

Los trabajadores de servicio son la tecnología clave detrás de las PWA, lo que permite escenarios como la compatibilidad sin conexión, el almacenamiento en caché avanzado y la ejecución de tareas en segundo plano anteriormente limitadas a aplicaciones nativas.  

Los trabajadores de servicio son tareas en segundo plano que interceptan solicitudes de red desde la aplicación web.  Los trabajadores del servicio intentan completar tareas, incluso cuando el PWA no se está ejecutando.  Las tareas incluyen las siguientes acciones.  

*   Servir recursos solicitados desde una memoria caché  
*   Envío de notificaciones de inserción  
*   Ejecutar tareas de captura en segundo plano  
*   Iconos de badging  
*   y mucho más  
    
Los trabajadores de servicio se definen en un archivo JavaScript especial.  Para obtener más información, vaya a [Using Service Workers][MDNUsingServiceWorkers] and Service Worker [API][MDNServiceWorkerApi].  

Para crear un trabajador de servicio en el proyecto, use la receta **de** trabajo de servicio de red de caché de [PWA Builder][PwaBuilderServiceWorker].  

1.  Vaya a [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], seleccione el trabajador de **servicio** de red primero en caché y seleccione el **botón** Descargar.  El archivo descargado contiene los siguientes archivos:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Copie los archivos descargados en la `public` carpeta del proyecto de la aplicación web.  
1.  En Visual Studio code, abra y agregue el siguiente fragmento `/public/index.html` de código dentro de la `<head>` etiqueta.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
La aplicación web ahora tiene un trabajador de servicio que usa la estrategia de primero en caché.  El nuevo trabajador de servicio captura primero los recursos de la memoria caché y de la red solo según sea necesario.  Los recursos almacenados en caché incluyen imágenes, JavaScript, CSS y HTML.

Siga estos pasos para confirmar que se ejecuta el trabajador de servicio.  

1.  Navegue a la aplicación web con `http://localhost:3000` .  Si la aplicación web no está disponible, ejecute el siguiente comando.   
    
    ```shell
    npm start
    ```
    
1.  En Microsoft Edge, seleccione `F12` para abrir Microsoft Edge DevTools.  Seleccione **Aplicación**y, a continuación, **Trabajadores de** servicio para ver los trabajadores del servicio.  Si no se muestra el trabajador del servicio, actualice la página.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Introducción al trabajador del servicio DevTools de Microsoft Edge" lightbox="./media/devtools-sw-overview.png":::
       Introducción al trabajador del servicio DevTools de Microsoft Edge  
    :::image-end:::  
    
1.  Para ver la caché de trabajo de servicio, expanda **Almacenamiento en caché** y seleccione **pwabuilder-precache**.  Se deben mostrar todos los recursos almacenados en caché por el trabajador de servicio.  Los recursos almacenados en caché por el trabajador de servicio incluyen el icono de la aplicación, el manifiesto de la aplicación, CSS y los archivos JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Caché de trabajo de servicio en Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Caché del trabajador de servicio en Microsoft Edge DevTools \(F12\)  
    :::image-end:::  
    
1.  Prueba tu PWA como una aplicación sin conexión.  En Microsoft Edge DevTools \( `F12` \), **** elija **Red** y, a continuación, cambie el estado En línea a **Sin conexión**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Establecer la aplicación en modo sin conexión en Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Establecer la aplicación en modo sin conexión en Microsoft Edge DevTools  
    :::image-end:::  
    
1.  Actualiza la aplicación y debería mostrar el mecanismo sin conexión para servir los recursos de la aplicación desde la memoria caché.  
    
    :::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="PWA que se ejecuta sin conexión" lightbox="./media/visual-studio-nodejs-express-index.png":::
       PWA que se ejecuta sin conexión  
    :::image-end:::  
    
## <a name="add-push-notifications-to-your-pwa"></a>Agregar notificaciones de inserción a su PWA  

Puede crear PWA que admitan notificaciones de inserción completando las siguientes tareas.  

1.  Suscribirse a un servicio de mensajería mediante la [API de inserción][MDNPushApi]  
1.  Mostrar un mensaje del sistema cuando se recibe un mensaje del servicio mediante la [API de notificaciones][MDNNotificationsApi]  
    
Al igual que con los trabajadores de servicio, las API de notificación de inserción son API basadas en estándares.  Las API de notificación de inserción funcionan en todos los exploradores, por lo que el código debe funcionar en todas partes en las que se admiten las PWA.  Para obtener más información acerca de cómo entregar mensajes de inserción a diferentes exploradores del servidor, vaya a [Web-Push][NPMWebPush].  

Los siguientes pasos se han adaptado del Libro de recetas Push Rich Demo in [Service Worker][ServiceWorkerCookbookPushRichDemo] proporcionado por Mozilla, que tiene una serie de otras recetas útiles de inserción web y de trabajo de servicio.  

### <a name="step-1---generate-vapid-keys"></a>Paso 1: Generar claves VAPID  

Las notificaciones push requieren claves VAPID \(Voluntary Application Server Identification\) para enviar mensajes de inserción al cliente de PWA.  Hay varios generadores de claves VAPID disponibles en línea \(por ejemplo, [vapidkeys.com][VapidkeysMain]\).  Después de la generación, debe obtener un objeto JSON que contenga una clave pública y privada.  Guarde las claves para los pasos posteriores del siguiente tutorial.  Para obtener información acerca de VAPID y WebPush, vaya a Enviar notificaciones [de WebPush identificadas por VAPID mediante el Servicio de inserción de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### <a name="step-2---subscribe-to-push-notifications"></a>Paso 2: suscribirse a notificaciones de inserción  

Los trabajadores de servicio controlan eventos de inserción e interacciones de notificación del sistema en su PWA.  Para suscribir el PWA a las notificaciones de inserción del servidor, asegúrese de que se cumplen las siguientes condiciones.  

*   El PWA está instalado, activo y registrado  
*   El código para completar la tarea de suscripción está en el subproceso de interfaz de usuario principal de la PWA  
*   Tiene conectividad de red  
    
Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario concedió el permiso de PWA para recibir notificaciones.  Si no es así, el explorador le pedirá permiso al usuario.  Si se deniega el permiso, la solicitud `registration.pushManager.subscribe` para iniciar un , que debe `DOMException` controlarse.  Para obtener más información sobre la administración de permisos, vaya a [Notificaciones de inserción en Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

En el `pwabuilder-sw-register.js` archivo, anexa el siguiente fragmento de código.  

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

Para obtener más información, vaya a [PushManager][MDNPushManager] y [Web-Push][NPMWebPushUsage].  

### <a name="step-3---listen-for-push-notifications"></a>Paso 3: escuchar notificaciones de inserción  

Después de crear una suscripción en su PWA, agregue controladores al trabajador del servicio para responder a eventos de inserción.  El evento Push se envía desde el servidor para mostrar notificaciones del sistema.  Las notificaciones del sistema muestran los datos de un mensaje recibido.  Para completar las siguientes tareas, debe agregar un `click` controlador.  

*   Descartar la notificación del sistema  
*   Abrir, enfocar o abrir y enfocar cualquier ventana abierta  
*   Abrir y centrar una nueva ventana para mostrar una página de cliente de PWA  
    
En el `pwabuilder-sw.js` archivo, agregue los siguientes controladores.  

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

### <a name="step-4---try-it-out"></a>Paso 4: Pruébalo  

Para probar las notificaciones de inserción de su PWA, siga estos pasos.  

1.  Vaya a su PWA en `http://localhost:3000` .  Cuando el trabajador de servicio se activa e intenta suscribir su PWA a notificaciones push, Microsoft Edge le pide que permita que su PWA muestre notificaciones.  Seleccione **Permitir**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Cuadro de diálogo de permisos para habilitar notificaciones" lightbox="./media/notification-permission.png":::
       Cuadro de diálogo de permisos para habilitar notificaciones  
    :::image-end:::  
    
1.  Simular una notificación de inserción del lado servidor.  Con el PWA abierto en `http://localhost:3000` el explorador, seleccione `F12` para abrir DevTools.  Elija **Inserción**del trabajador del servicio de  >  ****  >  **** aplicación para enviar una notificación de inserción de prueba a su PWA.  
    
    :::row:::
       :::column span="":::
          Una notificación de inserción debe mostrarse cerca de la barra de tareas.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Insertar una notificación desde DevTools" lightbox="./media/devtools-push.png":::
             Insertar una notificación desde DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si no seleccionas \(o activate\) una notificación del sistema, el sistema la descarta automáticamente después de varios segundos y la pone en cola en el Centro de acciones de Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificaciones en el Centro de acciones de Windows" lightbox="./media/windows-action-center.png":::
             Notificaciones en el Centro de acciones de Windows  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a>Pasos siguientes  

Los siguientes pasos incluyen tareas adicionales que le ayudarán a comprender la creación de pwas reales.  

*   Administrar y almacenar suscripciones de inserción  
*   [Cifrar datos][NPMWebPushEncrypt] de carga útil  
*   Diseño adaptativo  
*   Vinculación profunda  
*   [Pruebas entre exploradores][BrowserStackTestEdgeBrowser]  
*   Implementar prácticas de validación y pruebas como [Webhint][Webhint]  
    
## <a name="see-also"></a>Consulte también  

*   [Aplicaciones web progresivas en documentos web de MDN][MDNProgressiveWebApps]  
*   [Aplicaciones web progresivas en web.dev][WebDevProgressiveWebApps]  
*   [Lectores de noticias de][HackerNewsProgressiveWebApps] hacker como aplicaciones web progresivas: compara diferentes marcos y patrones de rendimiento para implementar un PWA de ejemplo \(Lector de noticias de hacker\).  
*   [PwAs de descomisado de mitos][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Una guía básica progresiva para la aplicación web progresiva][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [POST sin conexión con aplicaciones web progresivas][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Apuestas en la Web][JoretegBlogBettingWeb]  
*   [Nomenclatura de aplicaciones web progresivas][Fberriman20170626NamingProgressiveWebApps]  
*   [Diseño y creación de una aplicación web progresiva sin marco (parte 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Diseño y creación de una aplicación web progresiva sin marco (parte 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Diseño y creación de una aplicación web progresiva sin un marco (parte 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  

<!-- links -->  

<!--[ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]: /archive/microsoft-edge/legacy/developer/progressive-web-apps/index#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

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
