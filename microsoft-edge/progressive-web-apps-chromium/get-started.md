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
# Introducción a las aplicaciones web progresivas (cromo)  

Las aplicaciones web progresivas \ (PWAs \) son aplicaciones web que se han [mejorado progresivamente][WikiProgressiveEnhancement] con características de tipo aplicación, como la instalación, el soporte técnico sin conexión y las notificaciones Push.  También puede haber empaquetado su PWA para los almacenes de aplicaciones, incluyendo Microsoft Store, así como Google Play, Mac App Store y mucho más.  Microsoft Store es el almacén de aplicaciones comerciales integrado en Windows 10.  

La siguiente guía le ofrece una descripción general de los conceptos básicos de PWA mediante la creación de una aplicación web simple y su extensión como PWA.  El proyecto finalizado funciona en exploradores modernos.  

> [!TIP]
> Puede usar [PWABuilder][PwaBuilder] para crear un nuevo PWA, mejorar su PWA existente o empaquetar su PWA para los almacenes de aplicaciones.  

## Requisitos previos  

*   Use [código de vs][VisualstudioCodeMain] para editar el código fuente de PWA.  
*   Use [Node.js][NodejsMain] como su servidor Web local.  

## Configurar una aplicación web básica  

Para crear una aplicación Web vacía, siga los pasos que se indican en el [generador de aplicaciones de node Express][ExpressjsApplicationGenerator]y asigne un nombre a la aplicación `MySamplePwa` .  

En el símbolo del sistema, ejecute los siguientes comandos.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Los comandos crean una aplicación Web vacía e instalan cualquier dependencia.  

Ahora tiene una aplicación web simple y funcional.  Para iniciarlo, ejecute el siguiente comando.  

```shell
npm start
```  

Ahora, vaya a `http://localhost:3000` ver su nueva aplicación Web.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ejecutar su nuevo PWA en localhost":::
   Ejecutar su nuevo PWA en localhost
:::image-end:::

## Empezar a crear un PWA  

Ahora que tiene una aplicación web simple, amplíela como PWA agregando los 3 requisitos para PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), un [manifiesto de la aplicación web](#step-2---create-a-web-app-manifest)y un [trabajador de servicio](#step-3---add-a-service-worker).  

### Paso 1: usar HTTPS  

Las partes clave de la plataforma PWA, como los [trabajos de servicio][MDNServiceWorkerApi], requieren el uso de HTTPS.  Cuando su PWA se activa, debe publicarlo en una dirección URL HTTPS.  

Para fines de depuración, Microsoft Edge también permite `http://localhost` el uso de las API de PWA.  

Si [publica la aplicación web como un sitio activo][VisualStudioNodejsTutorialPublishAzureAppService] \ (por ejemplo, al configurar una [cuenta gratuita de Azure][AzureCreateFreeAccount]), debe asegurarse de que su servidor está configurado para HTTPS.  Si usa el [servicio de aplicaciones de Microsoft Azure][AzureWebApps] para hospedar su sitio, se ofrece a través de HTTPS de forma predeterminada.  

La guía siguiente, `http://localhost` que se usa para crear su PWA.  

### Paso 2: crear un manifiesto de la aplicación Web  

Un [manifiesto de la aplicación web][MDNWebAppManifest] es un archivo JSON que contiene metadatos sobre la aplicación, como el nombre, la descripción, los iconos, etc.  

Para agregar un manifiesto de la aplicación a la aplicación web:  

1.  En vs Code, vaya **File**  >  a la**carpeta abrir** archivo y elija el `MySamplePwa` directorio que creó anteriormente.  
1.  Presione `Ctrl` + `N` para crear un archivo nuevo y péguelo en el siguiente fragmento de código.  
    
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
1.  En VS Code, Abra `/public/index.html` y agregue el siguiente fragmento de código dentro de la `<head>` etiqueta.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Paso 3: agregar un trabajo de servicio  

Los trabajadores de servicios son la tecnología clave que subyace a PWAs, habilita escenarios como la compatibilidad sin conexión, el almacenamiento avanzado y la ejecución de tareas en segundo plano previamente limitadas a aplicaciones nativas.  

Los trabajos de servicio son tareas en segundo plano que interceptan solicitudes de red de la aplicación Web.  Realizan tareas, incluso si su PWA no se está ejecutando, como servir recursos solicitados de una caché, enviar notificaciones push, ejecutar tareas de captura en segundo plano, iconos de distintivos, etc.  Los trabajadores del servicio se definen en un archivo especial de JavaScript.  Para obtener más información, vea [usar trabajadores de servicio][MDNUsingServiceWorkers] y [API de trabajo de servicio][MDNServiceWorkerApi].  

Para compilar un trabajo de servicio en el proyecto, use la receta de trabajo de servicio de red en la **memoria caché** del [creador de PWA][PwaBuilderServiceWorker].  

1.  Vaya a [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], seleccione el trabajo **de servicio caché-primer** servicio de red y seleccione el botón **Descargar** .  El archivo descargado contiene los siguientes archivos:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  Copie los archivos descargados en la `public` carpeta del proyecto de la aplicación Web.  
    
1.  En VS Code, Abra `/public/index.html` y agregue el siguiente fragmento de código dentro de la `<head>` etiqueta.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Su aplicación web ahora tiene un trabajador de servicio que usa la primera estrategia de almacenamiento en caché, que recupera los recursos como imágenes, JS, CSS y HTML en primer lugar de la caché, y retrocede a la red según sea necesario.  

Use los siguientes pasos para confirmar que el trabajo de servicio se ejecuta.  

1.  Vaya a su aplicación web con `http://localhost:3000` .  Si la aplicación web no está disponible, ejecute el siguiente comando.   
    
    ```shell
    npm start
    ```
    
1.  En Microsoft Edge, seleccione `F12` para abrir la DevTools de Microsoft Edge.  Seleccione la **aplicación**y, a continuación, los **trabajadores del servicio** para ver los trabajadores del servicio.  Si no ve el trabajo de servicio, es posible que tenga que actualizar la página.  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Información general del trabajo del servicio Microsoft Edge DevTools":::
       Información general del trabajo del servicio Microsoft Edge DevTools
    :::image-end:::
    
1.  Visualice la caché de trabajos del servicio expandiendo el **almacenamiento en caché** y seleccione **pwabuilder-precache**.  Debería ver todos los recursos almacenados en caché por el trabajo del servicio, como el icono de la aplicación, el manifiesto de la aplicación, los archivos CSS y JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Caché de trabajo de servicio en Microsoft Edge DevTools":::
       Caché de trabajo de servicio en Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Pruebe su PWA como una aplicación sin conexión.  En Microsoft Edge DevTools \ ( `F12` \), seleccione **red** y, a continuación, cambie el estado de **conexión** a **sin conexión**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools":::
       Establecer la aplicación en el modo sin conexión en Microsoft Edge DevTools
    :::image-end:::
    
1.  Actualice la aplicación y verá que se está trabajando sin conexión atendiendo los recursos de la aplicación desde la memoria caché.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA que se ejecuta sin conexión":::
       PWA que se ejecuta sin conexión
    :::image-end:::
    
## Agregar notificaciones Push a su PWA  

Puede crear PWAs que admitan las notificaciones de inserción completando las siguientes tareas.  

1.  Suscribirse a un servicio de mensajería mediante la [API de inserción][MDNPushApi]  
1.  Mostrar un mensaje de notificación del sistema cuando se recibe un mensaje del servicio con la [API de notificaciones][MDNNotificationsApi]  

Al igual que con los trabajadores del servicio, estas son API basadas en estándares que funcionan en exploradores, de modo que solo tienes que escribir el código una vez para que funcione en todos los casos en que PWAs sea compatible.  Para obtener más información sobre cómo entregar mensajes Push a diferentes exploradores de su servidor, use la biblioteca de código abierto de [inserción web][NPMWebPush] .  

Los siguientes pasos han sido adaptados desde la demostración de inserción enriquecida en el [manual de trabajos de trabajo][ServiceWorkerCookbookPushRichDemo] de Mozilla, que tiene varias otras recetas útiles de inserción de web y de trabajadores de servicios.  

### Paso 1: generar claves VAPID  

Las notificaciones push requieren claves de VAPID \ (identificación de servidor de aplicaciones voluntaria \) para poder enviar mensajes Push al cliente de PWA.  Hay varios generadores de claves de VAPID disponibles en línea \ (por ejemplo, [vapidkeys.com][VapidkeysMain]\).  Después de la generación, debe obtener un objeto JSON que contenga una clave pública y privada.  Guarde las claves para los pasos siguientes en el siguiente tutorial.  Para obtener información sobre el funcionamiento de VAPID y webpush, consulte [envío de notificaciones de webpush identificadas por el servicio de inserción de VAPID][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Paso 2: suscribirse a notificaciones push  

Los trabajos del servicio controlan los eventos Push y las interacciones de notificaciones del sistema en tu PWA.  Para suscribir las notificaciones push de PWA a Server, asegúrese de que se cumplan las siguientes condiciones.  

*   PWA está instalado, activo y registrado  
*   El código que realiza la tarea de suscripción se encuentra en el subproceso de la interfaz de usuario principal del PWA  
*   Tiene conectividad de red  

Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario ha concedido permiso de PWA para recibir notificaciones.  En caso contrario, el explorador le pide permiso para el usuario.  Si el permiso es denegado, la solicitud para `registration.pushManager.subscribe` iniciar una `DOMException` , que se debe controlar.  Para obtener más información sobre la administración de permisos, vea [notificaciones Push en Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

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

Para obtener más información, consulte [PushManager][MDNPushManager] y [inserción web][NPMWebPushUsage].  

### Paso 3: escuchar las notificaciones push  

Ahora que se ha configurado una suscripción en PWA, agregue controladores al trabajo del servicio para responder a los eventos Push \ (enviados desde el servidor \) para mostrar las notificaciones del sistema con los datos de un mensaje recibido.  Debes agregar un controlador de clics para realizar cualquiera de las siguientes tareas.  
*   descartar la notificación del sistema  
*   abrir, enfocar o abrir y enfocar cualquier ventana abierta  
*   abrir y enfocar una nueva ventana para mostrar una página de cliente de PWA  

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

### Paso 4: pruébelo  

Realice los siguientes pasos para probar las notificaciones Push en su PWA.  

1.  Vaya a su PWA en `http://localhost:3000` .  Cuando el trabajador de servicio se activa e intenta suscribirse a las notificaciones push de PWA, Microsoft Edge le pide que permita a su PWA Mostrar notificaciones.  Seleccione **permitir**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Cuadro de diálogo de permisos para habilitar las notificaciones":::
       Cuadro de diálogo de permisos para habilitar las notificaciones
    :::image-end:::
    
    
1.  Simular una notificación de inserción del servidor.  Con el PWA abierto en `http://localhost:3000` en el explorador, seleccione `F12` para abrir el DevTools.  Elija **Application**  >  **Service Worker**  >  **Push** de trabajo de servicio de aplicaciones para enviar una notificación de inserción de prueba a su PWA.  Debería ver una notificación de inserción cerca de la barra de tareas.  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Insertar una notificación desde DevTools":::
       Insertar una notificación desde DevTools
    :::image-end:::
     
    Si no selecciona \ (o activa \) una notificación del sistema, se descarta después de varios segundos y se pone en cola en el centro de actividades de Windows.  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificaciones en el centro de actividades de Windows":::
       Notificaciones en el centro de actividades de Windows
    :::image-end:::
    
    
## Pasos siguientes  

A continuación se muestra una lista de tareas adicionales para aprender a crear PWAs del mundo real:  

*  Administrar y almacenar suscripciones de inserción  
*  [Cifrar][NPMWebPushEncrypt] datos de carga  
*  Diseño adaptativo  
*  Vínculos profundos  
*  [Pruebas entre exploradores][BrowserStackTestEdgeBrowser]  
*  Implementar procedimientos recomendados, como [webhint][Webhint]  

## Consulte también  

*   [Aplicaciones web progresivas en documentos web de MDN][MDNProgressiveWebApps].  
*   [Aplicaciones web progresivas en Web. dev][WebDevProgressiveWebApps].  
*   [Lectores de noticias de piratas informáticos como aplicaciones web progresivas][HackerNewsProgressiveWebApps] : compara diferentes marcos de trabajo y patrones de rendimiento para implementar un ejemplo \ (lector de noticias de hacker \) PWA.  

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
