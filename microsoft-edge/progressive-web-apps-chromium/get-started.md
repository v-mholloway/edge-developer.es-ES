---
description: Esta guía le ofrece información general sobre los conceptos básicos de PWA y herramientas para crear aplicaciones web progresivas (cromo) en Windows.
title: Introducción a las aplicaciones web progresivas (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto Web, trabajo de servicio, inserción
ms.openlocfilehash: 065ced3afa8ecd4165325fd4f10a673d86c72fa7
ms.sourcegitcommit: be76feed0d616a96c77ea2748a9f0d6c0c06284b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2020
ms.locfileid: "11103927"
---
# Introducción a las aplicaciones web progresivas (cromo)  

Las aplicaciones web progresivas \ (PWAs \) son aplicaciones web que se han [mejorado progresivamente][WikiProgressiveEnhancement].  Las mejoras progresivas incluyen características similares a las de la aplicación, como la instalación, el soporte técnico sin conexión y las notificaciones Push.  También puede empaquetar su PWA para los almacenes de aplicaciones.  Entre los posibles almacenes de aplicaciones se incluyen Microsoft Store, Google Play, Mac App Store y mucho más.  Microsoft Store es el almacén de aplicaciones comerciales integrado en Windows 10.  

La siguiente guía le ofrece una descripción general de los conceptos básicos de PWA mediante la creación de una aplicación web simple y su extensión como PWA.  El proyecto finalizado funciona en exploradores modernos.  

> [!TIP]
> Puede usar [PWABuilder][PwaBuilder] para crear un nuevo PWA, mejorar su PWA existente o empaquetar su PWA para los almacenes de aplicaciones.  

## Requisitos previos  

*   Use [código de Visual Studio][VisualstudioCodeMain] para editar el código fuente de PWA.  
*   Use [Node.js][NodejsMain] como su servidor Web local.  

## Crear una aplicación web básica  

Para crear una aplicación Web vacía, siga los pasos que se indican en el [generador de aplicaciones de node Express][ExpressjsApplicationGenerator]y asigne un nombre a la aplicación `MySamplePwa` .  

En el símbolo del sistema, ejecute los siguientes comandos.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Los comandos crean una aplicación Web vacía e instalan cualquier dependencia.  

Ahora tiene una aplicación web simple y funcional.  Para iniciar la aplicación Web, ejecute el siguiente comando.  

```shell
npm start
```  

Ahora, vaya a `http://localhost:3000` ver su nueva aplicación Web.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/vs-nodejs-express-index.png":::
   Ejecutar su nuevo PWA en localhost
:::image-end:::

## Empezar a crear un PWA  

Ahora que tiene una aplicación web simple, amplíela como PWA agregando los tres requisitos para PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), un [manifiesto de la aplicación web](#step-2---create-a-web-app-manifest)y un [trabajador de servicio](#step-3---add-a-service-worker).  

### Paso 1: usar HTTPS  

Las partes clave de la plataforma PWA, como los [trabajos de servicio][MDNServiceWorkerApi], requieren el uso de HTTPS.  Cuando su PWA se activa, debe publicarlo en una dirección URL HTTPS.  

Para fines de depuración, Microsoft Edge también permite `http://localhost` el uso de las API de PWA.  

[Publique la aplicación web como un sitio activo][VisualStudioNodejsTutorialPublishAzureAppService], pero asegúrese de que su servidor está configurado para HTTPS.  Por ejemplo, puede crear una [cuenta gratuita de Azure][AzureCreateFreeAccount].  Hospede su sitio en el [servicio de aplicaciones de Microsoft Azure][AzureWebApps] y se ofrece a través de HTTPS de forma predeterminada.  

La guía siguiente, `http://localhost` que se usa para crear su PWA.  

### Paso 2: crear un manifiesto de la aplicación Web  

Un [manifiesto de la aplicación web][MDNWebAppManifest] es un archivo JSON que contiene metadatos sobre la aplicación, como el nombre, la descripción, los iconos, etc.  

Para agregar un manifiesto de la aplicación a la aplicación web:  

1.  En Visual Studio Code, seleccione **archivo**  >  **Abrir carpeta** y elija el `MySamplePwa` directorio que creó anteriormente.  
1.  Seleccione `Ctrl` + `N` para crear un archivo nuevo y péguelo en el siguiente fragmento de código.  
    
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
1.  Agregue una imagen del icono de la aplicación de 512x512 con el nombre `icon512.png` a `/MySamplePwa/public/images` .  Puede usar la [imagen de ejemplo][ImagePwa] para realizar pruebas.  
1.  En Visual Studio Code, abre `/public/index.html` y agrega el siguiente fragmento de código dentro de la `<head>` etiqueta.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Paso 3: agregar un trabajo de servicio  

Los trabajadores de servicios son la tecnología clave que subyace a PWAs, habilita escenarios como la compatibilidad sin conexión, el almacenamiento avanzado y la ejecución de tareas en segundo plano previamente limitadas a aplicaciones nativas.  

Los trabajos de servicio son tareas en segundo plano que interceptan solicitudes de red de la aplicación Web.  Los trabajadores de servicio intentan completar las tareas, incluso cuando su PWA no se está ejecutando.  Las tareas incluyen las siguientes acciones.  

*   Dar servicio a los recursos solicitados desde una caché  
*   Enviar notificaciones push  
*   Ejecución de tareas de captura en segundo plano  
*   Iconos de distintivos  
*   y mucho más  

Los trabajadores del servicio se definen en un archivo especial de JavaScript.  Para obtener más información, vaya a [usar los trabajos de servicio][MDNUsingServiceWorkers] y la API de trabajo de [servicio][MDNServiceWorkerApi].  

Para compilar un trabajo de servicio en el proyecto, use la receta de trabajo de servicio de red en la **memoria caché** del [creador de PWA][PwaBuilderServiceWorker].  

1.  Vaya a [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], seleccione el trabajo **de servicio caché-primer** servicio de red y seleccione el botón **Descargar** .  El archivo descargado contiene los siguientes archivos:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  Copie los archivos descargados en la `public` carpeta del proyecto de la aplicación Web.  
    
1.  En Visual Studio Code, abre `/public/index.html` y agrega el siguiente fragmento de código dentro de la `<head>` etiqueta.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Su aplicación web ahora tiene un trabajador de servicio que usa la primera estrategia de almacenamiento en caché.  El trabajador de servicio nuevo primero obtiene los recursos de la caché y de la red solo según sea necesario.  Entre los recursos almacenados en caché se incluyen imágenes, JavaScript, CSS y HTML.

Use los siguientes pasos para confirmar que el trabajo de servicio se ejecuta.  

1.  Vaya a su aplicación web con `http://localhost:3000` .  Si la aplicación web no está disponible, ejecute el siguiente comando.   
    
    ```shell
    npm start
    ```
    
1.  En Microsoft Edge, seleccione `F12` para abrir la DevTools de Microsoft Edge.  Seleccione la **aplicación**y, a continuación, los **trabajadores del servicio** para ver los trabajadores del servicio.  Si el trabajo de servicio no se muestra, actualice la página.  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/devtools-sw-overview.png":::
       Información general del trabajo del servicio Microsoft Edge DevTools
    :::image-end:::
    
1.  Visualice la caché de trabajos del servicio expandiendo el **almacenamiento en caché** y seleccione **pwabuilder-precache**.  Deben mostrarse todos los recursos almacenados en la caché por el trabajo del servicio.  Los recursos almacenados en caché por el trabajo del servicio incluyen el icono de la aplicación, el manifiesto de la aplicación, los archivos CSS y JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/devtools-cache.png":::
       Caché de trabajo de servicio en Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Pruebe su PWA como una aplicación sin conexión.  En Microsoft Edge DevTools \ ( `F12` \), seleccione **red** y, a continuación, cambie el estado de **conexión** a **sin conexión**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/devtools-offline.png":::
       Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools
    :::image-end:::
    
1.  Actualice la aplicación y debería mostrar el mecanismo sin conexión para servir los recursos de la aplicación desde la memoria caché.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/vs-nodejs-express-index.png":::
       PWA que se ejecuta sin conexión
    :::image-end:::
    
## Agregar notificaciones Push a su PWA  

Puede crear PWAs que admitan las notificaciones de inserción completando las siguientes tareas.  

1.  Suscribirse a un servicio de mensajería mediante la [API de inserción][MDNPushApi]  
1.  Mostrar un mensaje de notificación del sistema cuando se recibe un mensaje del servicio con la [API de notificaciones][MDNNotificationsApi]  
    
Al igual que con los trabajadores del servicio, las API de notificaciones push son API basadas en estándares.  Las API de notificaciones push funcionan en todos los exploradores, por lo que el código debería funcionar siempre que se admitan PWAs.  Para obtener más información sobre cómo enviar mensajes Push a diferentes exploradores de su servidor, vaya a inserción en la [Web][NPMWebPush].  

Los siguientes pasos han sido adaptados desde la demostración de inserción enriquecida en el [manual de trabajos de trabajo][ServiceWorkerCookbookPushRichDemo] de Mozilla, que tiene varias otras recetas útiles de inserción de web y de trabajadores de servicios.  

### Paso 1: generar claves VAPID  

Las notificaciones push requieren claves de VAPID \ (identificación de servidor de aplicaciones voluntaria \) para poder enviar mensajes Push al cliente de PWA.  Hay varios generadores de claves de VAPID disponibles en línea \ (por ejemplo, [vapidkeys.com][VapidkeysMain]\).  Después de la generación, debe obtener un objeto JSON que contenga una clave pública y privada.  Guarde las teclas para pasos posteriores en el siguiente tutorial.  Para obtener más información sobre VAPID y webpush, vaya al [envío de VAPID de notificaciones de webpush identificadas con el servicio de inserción de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Paso 2: suscribirse a notificaciones push  

Los trabajos del servicio controlan los eventos Push y las interacciones de notificaciones del sistema en tu PWA.  Para suscribir las notificaciones push de PWA a Server, asegúrese de que se cumplan las siguientes condiciones.  

*   PWA está instalado, activo y registrado  
*   El código para completar la tarea de suscripción se encuentra en el subproceso de la interfaz de usuario principal del PWA  
*   Tiene conectividad de red  
    
Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario ha concedido permiso de PWA para recibir notificaciones.  En caso contrario, el explorador le pide permiso para el usuario.  Si el permiso es denegado, la solicitud para `registration.pushManager.subscribe` iniciar una `DOMException` , que se debe controlar.  Para obtener más información sobre la administración de permisos, vaya a [notificaciones Push en Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

En el `pwabuilder-sw-register.js` archivo, Anexe el siguiente fragmento de código.  

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

Para obtener más información, vaya a [PushManager][MDNPushManager] y [inserción web][NPMWebPushUsage].  

### Paso 3: escuchar las notificaciones push  

Después de crear una suscripción en PWA, agregue controladores al trabajo del servicio para responder a los eventos Push.  El evento Push se envía desde el servidor para mostrar las notificaciones del sistema.  Las notificaciones del sistema muestran los datos de un mensaje recibido.  Para completar las siguientes tareas, debe agregar un controlador de clics.  

*   Descartar la notificación del sistema  
*   Abrir, enfocar o abrir y enfocar cualquier ventana abierta  
*   Abrir y enfocar una nueva ventana para mostrar una página de cliente de PWA  
    
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

### Paso 4: pruébelo  

Siga los pasos que se indican a continuación para probar las notificaciones push para su PWA.  

1.  Vaya a su PWA en `http://localhost:3000` .  Cuando el trabajador de servicio se activa e intenta suscribirse a las notificaciones push de PWA, Microsoft Edge le pide que permita a su PWA Mostrar notificaciones.  Seleccione **permitir**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/notification-permission.png":::
       Cuadro de diálogo de permisos para habilitar las notificaciones
    :::image-end:::
    
1.  Simular una notificación de inserción del servidor.  Con el PWA abierto en `http://localhost:3000` en el explorador, seleccione `F12` para abrir el DevTools.  Elija **Application**  >  **Service Worker**  >  **Push** de trabajo de servicio de aplicaciones para enviar una notificación de inserción de prueba a su PWA.  
    :::row:::
       :::column span="":::
          Una notificación de inserción debe mostrarse cerca de la barra de tareas.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/devtools-push.png":::
             Insertar una notificación desde DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si no selecciona \ (o activa \) una notificación del sistema, el sistema la descarta automáticamente después de varios segundos y la coloca en la cola del centro de actividades de Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Ejecutar su nuevo PWA en localhost" lightbox="./media/windows-action-center.png":::
             Notificaciones en el centro de actividades de Windows :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## Pasos siguientes  

Los pasos siguientes incluyen tareas adicionales para ayudarle a comprender la creación de PWAs del mundo real.  

*   Administrar y almacenar suscripciones de inserción  
*   [Cifrar][NPMWebPushEncrypt] datos de carga  
*   Diseño adaptativo  
*   Vínculos profundos  
*   [Pruebas entre exploradores][BrowserStackTestEdgeBrowser]  
*   Implementar procedimientos de validación y pruebas, como [webhint][Webhint]  
   
## Consulte también  

*   [Aplicaciones web progresivas en documentos web de MDN][MDNProgressiveWebApps]  
*   [Aplicaciones web progresivas en Web. dev][WebDevProgressiveWebApps]  
*   [Lectores de noticias de piratas informáticos como aplicaciones web progresivas][HackerNewsProgressiveWebApps] : compara diferentes marcos de trabajo y patrones de rendimiento para implementar un ejemplo \ (lector de noticias de hacker \) PWA.  
*   [PWAs de mitos][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Una guía básica para la aplicación web progresiva][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Publicaciones sin conexión con aplicaciones web progresivas][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [Q&A DE PWA][AaronGustafsonNotebookPwaQa]  
*   [Apuestas en la web][JoretegBlogBettingWeb]  
*   [Asignar nombres a aplicaciones web progresivas][Fberriman20170626NamingProgressiveWebApps]  
*   [Diseñar y crear una aplicación web progresiva sin un marco (parte 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Diseñar y crear una aplicación web progresiva sin un marco (parte 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Diseñar y crear una aplicación web progresiva sin un marco (parte 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implementar una aplicación de Node.js en Azure con Visual Studio Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Crear cuenta gratuita de Azure Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicaciones Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificaciones Web en Microsoft Edge | Blogs de Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Código de Visual Studio"  

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

[Webhint]: https://webhint.io "sugerencia"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicaciones web progresivas | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Mejora progresiva | Wikipedia"  
