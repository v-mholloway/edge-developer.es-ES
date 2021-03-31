---
description: Esta guía le ofrece información general sobre los conceptos básicos de PWA y herramientas para crear aplicaciones web progresivas en Windows.
title: Introducción a las aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, PWABuilder, manifiesto Web, trabajo de servicio, inserción
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235900"
---
# Introducción a las aplicaciones web progresivas  

Las aplicaciones web progresivas \(PWAs \) son simplemente aplicaciones web que se han [mejorado progresivamente][WikiProgressiveEnhancement] con características nativas de tipo aplicación en plataformas de soporte y motores de explorador, como la instalación de inicio desde pantalla Android, la compatibilidad sin conexión y las notificaciones de inserción.  En Windows 10 con el motor Microsoft Edge \(EdgeHTML \), PWAs disfruta de la ventaja agregada de ejecutar independientemente la ventana del explorador como aplicaciones para la [plataforma universal de Windows][WindowsUwpGetStartedWhat] .  

Esta guía le ofrece información general sobre los conceptos básicos de PWA mediante la creación de una `localhost` aplicación web simple como PWA con Microsoft Visual Studio y algunas utilidades de creación de PWA.  El producto finalizado funciona de forma similar en cualquier explorador que admita PWAs.  

> [!TIP]
> Para una forma rápida de convertir un sitio existente en un PWA y empaquetarlo para Windows 10 y otras plataformas de aplicaciones, revise el [creador de PWA][PwaBuilder].  

## Requisitos previos  

Puedes crear PWAs con cualquier IDE de desarrollo web.  A continuación se muestran solo los requisitos previos de esta guía, que le guiará a través de la compatibilidad de la herramienta PWA en el ecosistema de Windows Developer.  

*   Descargar la \(gratis \) [Visual Studio Community 2017][VisualStudioDownloads].  También puede usar las ediciones Professional, Enterprise o [Preview][VisualStudioPreview] .  Desde el instalador de Visual Studio, elija las siguientes cargas de trabajo.  
    
    *   **Desarrollo de la plataforma universal de Windows**  
    *   **Desarrollo Node.js**  

## Configurar una aplicación web básica  

Por razones de simplicidad, use la plantilla de aplicación de Visual Studio [Node.js y Express][VisualStudioNodeJsTutorial] para crear `localhost` una aplicación web que atienda una `index.html` página.  Imagínese que esto es un marcador de posición para la aplicación web atractiva y completa que está desarrollando como PWA.  

1.  Inicia Visual Studio y comienza un nuevo proyecto.  
    *   **Archivo**  >  **Nuevo**  >  **Proyecto...**  
    *   `Ctrl`+`Shift`+`N`  
1.  En **JavaScript**, seleccione la **aplicación básica Node.js Express 4**.  Establezca el nombre y la ubicación y elija **Aceptar**.  
    
    ![Selección de la plantilla de proyecto Node.js Express 4 en Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  Una vez que se cargue el nuevo proyecto, elija **generar** \( `Ctrl` + `Shift` + `B` \) y **iniciar la depuración** \( `F5` \).  Compruebe que el `index.html` archivo se cargue cuando vaya a `http://localhost:1337` .  
    
    ![Ejecutar el nuevo sitio en localhost][ImageVsNodejsExpressIndex]  

## Convertir la aplicación en un PWA  

Ahora es el momento de conectar los requisitos básicos de [PWA][PwaEdgehtmlIndexRequirements] para la aplicación web: un manifiesto de la *aplicación web*, *https* y *trabajadores de servicio*.  

### Manifiesto de la aplicación Web  

Un [manifiesto de la aplicación web][MDNWebAppManifest] es un archivo de metadatos JSON que describe la aplicación, incluido el nombre, el autor, la dirección URL de la página de entrada y uno o más iconos.  Dado que sigue un [esquema basado en estándares][W3cWebAppManifest], solo debe suministrar un manifiesto de aplicación web para el PWA que está instalando en cualquier combinación de plataforma, sistema operativo y dispositivo que admita PWAs.  En el ecosistema de Windows, el manifiesto de la aplicación web señala al indizador Web de Bing que su PWA es candidata para la inclusión automática en [Microsoft Store][PwaEdgehtmlMicrosoftStore], donde puede llegar a casi 700 millones usuarios mensuales activos como aplicación de Windows 10.  

Si se tratase de un sitio activo existente, puede generar un manifiesto de la aplicación web con el [creador de PWA][PwaBuilder].  Como es un proyecto sin publicar, copie un manifiesto de ejemplo.  

1.  En el explorador de *soluciones*de Visual Studio, haga clic con el botón secundario en la carpeta *pública* y seleccione **Agregar**  >  **nuevo archivo...**, especificando `manifest.json` el nombre del elemento.  
1.  En el `manifest.json` archivo, copie el siguiente código.  

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
    
    En un verdadero PWA, el siguiente paso es personalizar el *nombre*, *start_url*, *short_name*, *Descripción*e *iconos* \(los iconos se tratan en el siguiente paso \).  
    
    Para obtener más información sobre los distintos valores de miembro y los propósitos asociados, vea la referencia del manifiesto de la [aplicación web][MDNWebAppManifest] .  
    
1.  A continuación, rellene la `icons` matriz vacía con rutas de imagen reales mediante el generador de imágenes de la aplicación de PWA.  
    
    1.  Con un explorador Web, Descargue esta [imagen de PWA de 512x512 de ejemplo][ImagePwa].  
    1.  Vaya al [generador de imágenes][PwaBuilderAppImageGenerator]de la aplicación creador de PWA y seleccione la `pwa.png` imagen que acaba de guardar como **imagen de entrada** y, a continuación, elija el botón **Descargar** .  
    1.  **Abra** y **Extraiga** el archivo zip.  
    1.  En el explorador de soluciones de Visual Studio, haga clic con el botón secundario en la `public` carpeta y **Abra carpeta en el explorador de archivos**.  Cree una **nueva carpeta** llamada `images` .  
    1.  Copie todas las carpetas de plataforma \( `android` , `chrome` ,, etc `windows10` . \) del archivo zip extraído a la `images` carpeta y cierre la ventana del explorador de archivos.  Agregue las carpetas a su proyecto de Visual Studio \(en el explorador de soluciones, haga clic con el botón derecho en `images` carpeta y seleccione **Agregar**  >  **carpeta existente...** para cada una de las carpetas \).  
    1.  Abra \(con Visual Studio o cualquier editor \) el `icons.json` archivo del código postal extraído y copie la `"icons": [...]` matriz en el `manifest.json` archivo de su proyecto.  

1.  Ahora debe asociar el manifiesto de la aplicación web con la aplicación.  Abra el `layout.pug` archivo \(en la `views` carpeta \) para editarlo y agregue esta línea después del vínculo de la hoja de estilos.  \(Simplemente es la plantilla de [Pug][PugAttributes] de nodo para `<link rel='manifest' href='/manifest.json'>` \).  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
Con todo eso, tu aplicación web ahora está dando servicio a un manifiesto y pantalla Android iconos de aplicaciones listos para usar.  Intenta ejecutar la aplicación \( `F5` \) y cargar el manifiesto.  

![Cargar el manifiesto de la aplicación web desde localhost][ImageVsNodejsExpressManifest]  

Y uno de sus iconos.  

![Logotipo de la aplicación de Square71x71Logo que se carga desde localhost][ImageVsNodejsExpressIcon]  

Si publica la aplicación Live \(con un `start_url` \), el motor de búsqueda de Bing la identifica ahora como candidato para [el empaquetado y el envío automáticos a Microsoft Store][PwaEdgehtmlMicrosoftStore] como una aplicación de Windows 10 que se puede instalar.  Asegúrese de que su manifest.jsen archivo incluye las [señales de calidad de las aplicaciones web progresivas][WindowsBlogsPwaEdge] para las que los análisis de Bing incluyen los siguientes elementos.   

*   `name`  
*   `description`  
*   Al menos un icono de 512px cuadrado o superior \(para garantizar una fuente de imagen de la resolución suficiente para generar automáticamente la pantalla de presentación de la aplicación, almacenar la información en el icono, etc. \).  

Además, use [https](#https), los [trabajos de servicio](#service-workers)y cumpla con [las directivas de Microsoft Store][LegalWindowsAgrementsMicrosoftStorePolicies].  

### HTTPS  

[Los trabajadores del servicio][MDNServiceWorkerApi] y otras tecnologías de PWA clave que funcionan con los trabajos del servicio \(como la [caché][MDNCache], [inserción][MDNPushApi]y las API de [sincronización en segundo plano][MDNSyncManager] \) solo funcionan en conexiones seguras, lo que significa que es [https][WikiHttps] para los sitios activos o `localhost` para fines de depuración.  

Si [publica esta aplicación web como un sitio activo][VisualStudioNodejsTutorialPublishAzureAppService] \(por ejemplo, al configurar una [cuenta gratuita de Azure][AzureCreateFreeAccount]), debe asegurarse de que su servidor está configurado para HTTPS.  Si usa el [servicio de aplicaciones de Microsoft Azure][AzureWebApps] para hospedar su sitio, se ofrece a través de HTTPS de forma predeterminada.  

Para esta guía, continúe usando `http://localhost` como un marcador de posición para un sitio activo atendido `https://` .  

### Trabajos de servicio  

Los trabajadores del servicio son la tecnología clave que subyace a PWAs. Los trabajadores de servicio actúan como un proxy entre su PWA y la red para habilitar su sitio web para que funcione como una aplicación nativa instalada que sirve a los escenarios sin conexión, responde a las notificaciones push del servidor y ejecuta tareas en segundo plano.  Los trabajadores de servicios también abren nuevas estrategias de rendimiento.  No es necesario implementar una aplicación web completa para usar la caché de trabajo del servicio para mejorar el rendimiento de la carga de páginas de su sitio Web.  

Los trabajos de servicio son subprocesos de fondo activados por eventos que se ejecutan desde archivos de JavaScript que se han servido al lado de los scripts habituales que encienden tu aplicación Web.  Dado que los trabajos de servicio no se ejecutan en el subproceso de interfaz de usuario principal, los trabajadores del servicio no tienen acceso a DOM, aunque el [subproceso de interfaz de usuario][MDNWorkerPrototypePostMessage] y un [subproceso de trabajo][MDNDedicatedWorkerGlobalScopePostMessage] pueden comunicarse mediante `postMessage()` `onmessage` controladores de eventos y.  

Para asociar un trabajador de servicio a la aplicación, regístrelo en el origen de la dirección URL de su sitio \(o en una ruta de acceso especificada dentro de él \).  Una vez que se haya registrado, el archivo de trabajo del servicio se descargará, se instalará y se activará en el equipo del usuario.  Para obtener más información, MDN web docs tiene una guía completa sobre el uso de los [trabajos de servicio][MDNUsingServiceWorkers] y una referencia detallada de API de [trabajadores de servicios][MDNServiceWorkerApi] .  

Para este tutorial, use el script de trabajo servicio de páginas sin conexión en el [creador de PWA][PwaBuilderServiceWorker].  Empiece por personalizar la secuencia de comandos con más funciones según sus requisitos de rendimiento, ancho de banda de red, etc.  Revise el [manual del trabajo de servicio][ServiceWorkerCookbook]  proporcionado por Mozilla para obtener varias ideas útiles para almacenar en caché de trabajo de servicio.  

1.  Abra [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] y seleccione el trabajo del servicio de **páginas sin conexión** \(predeterminado \) y haga clic en el botón **Descargar trabajador de servicio** .  
1.  Abra la carpeta de descarga y copie los dos archivos siguientes:  

    *   ServiceWorker1\pwabuilder-sw-register.js  
    *   ServiceWorker1\pwabuilder-sw.js  
    
    Guarde los archivos en la `public` carpeta del proyecto de Visual Studio Web App.  \(En Visual Studio, use `Ctrl` + `O` para abrir el explorador de archivos a su proyecto y vaya a la `public` carpeta \).  
    
    En el explorador de soluciones, abra el `public/pwabuilder-sw.js` archivo y cambie el valor de `offlineFallbackPage` a `offline.html` .  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    Merece la pena revisar el código en estos dos archivos para saber cómo registrar un trabajador de servicio que almacene una página designada \( `offline.html` \) y la sirva cuando se produzca un error en la recuperación de red.  Después, cree una `offline.html` página simple como marcador de posición para la funcionalidad sin conexión de la aplicación.  
    
1.  En el explorador de soluciones, abra el `views/layout.pug` archivo y agregue la siguiente línea debajo de las etiquetas de vínculos.  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    Su sitio carga y ejecuta el script de registro de trabajadores del servicio.  
    
1.  En el explorador de soluciones, haga clic con el botón derecho en la `public` carpeta y seleccione **Agregar**  >  **nuevo archivo...**.  Asígnele un nombre y `offline.html` agregue `<title>` el contenido del cuerpo, por ejemplo, el siguiente código.  
    
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
    
    En este momento, la `public` carpeta debería tener tres archivos nuevos.  
    
    ![Archivos agregados a la carpeta pública de la solución][ImageVsNodejsExpressPublic]  
    
1.  En el explorador de soluciones, abra el `routes\index.js` archivo y agregue el código siguiente justo antes del comando final \( `module.exports = router;` \).  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    Esto indica a tu aplicación que atienda el `offline.html` archivo \(cuando el trabajador del servicio lo recupere para la caché sin conexión \).  
    
1.  Pruebe su PWA.  Compila \( `Ctrl` + `Shift` + `B` \) y ejecuta \( `F5` \) tu aplicación web para iniciar Microsoft Edge y abrir la `localhost` página.  A continuación, complete los siguientes pasos.  
    
    1.  Abre la **consola** de DevTools perimetral \( `Ctrl` + `Shift` + `J` \) y verifica que el trabajador del servicio se haya registrado.  
    1.  En el panel **depurador** , expanda el control de **trabajos del servicio** y haga clic en su origen.  En la **Descripción general del trabajo del servicio**, verifique que el trabajador del servicio esté activado y ejecutándose.  
        
        ![Información general del trabajo del servicio Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  Expanda el control de **caché** y compruebe que la `offline.html` página se almacena en caché.  
        
        ![Caché de trabajo del servicio Edge DevTools][ImageDevtoolsSwCache]  
        
1.  Tiempo para probar su PWA como una aplicación sin conexión.  En Visual Studio, **detenga la depuración** \( `Shift` + `F5` \) la aplicación web y, a continuación, abra Microsoft Edge \(o actualizar \) en la dirección de localhost de su sitio Web.  Ahora debe cargar la `offline.html` Página \(gracias a su trabajo de servicio y a la caché sin conexión \).  
    
    ![offline.html de http://localhost:1337 cargado en Microsoft Edge][ImageOfflineHtml]  

## Agregar notificaciones push  

Haz que tu PWA sea más similar a la aplicación agregando compatibilidad de cliente para las notificaciones push mediante la [API de inserción][MDNPushApi] para suscribirte a un servicio de mensajería y la [API de notificaciones][MDNNotificationsApi] para mostrar un mensaje del sistema al recibir un mensaje.  Al igual que con los trabajadores del servicio, estas son API basadas en estándares que funcionan entre exploradores, de modo que solo tienes que escribir el código una vez para que funcione en todas partes PWAs se admita.  En el servidor, use la biblioteca de código abierto de [inserción web][NPMWebPush] para controlar las diferencias que implica la entrega de mensajes Push a varios exploradores.  

Lo siguiente está adaptado de la demostración de Push rico en el [manual de trabajos de trabajo][ServiceWorkerCookbookPushRichDemo] de los trabajos de Mozilla, que vale la pena consultar para obtener una serie de recetas útiles para trabajos de servicio y servicios Web.  

### Paso 1: instalar la biblioteca de inserción web NPM  

En el explorador de soluciones de Visual Studio, haga clic con el botón secundario en el proyecto y **abra Node.js ventana interactiva...**  Escriba el código siguiente.  

```javascript
.npm install web-push
```  

Esto instala la biblioteca [de inserción por web][NPMWebPush] .  Después, abra el `index.js` archivo y agregue la línea siguiente a la parte superior del archivo después de las otras instrucciones de requisito.  

```javascript
var webpush = require('web-push');
```  

### Paso 2: generar claves de VAPID para el servidor  

A continuación, debe generar las claves de VAPID \(identificación de servidor de aplicaciones voluntaria \) para que el servidor envíe mensajes Push al cliente de PWA.  Solo tiene que hacer esto una vez \(es decir, su servidor solo requiere un par de claves de VAPID \).  En la ventana interactiva Node.js, escriba el siguiente código.  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

El resultado debe dar lugar a un objeto JSON que contenga una clave pública y privada, que se copiará en la lógica del servidor.  

En el `index.js` archivo, justo antes de la línea final \( `module.exports = router` \), agregue el siguiente código.  

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

Copie los `publicKey` valores de y `privateKey` que acaba de generar.  Personaliza `mailto` también la dirección (aunque no es necesario para ejecutar este ejemplo, \)).  

El [blog de ingeniería de servicios de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] ofrece un buen explicación sobre VAPID y webpush si estás interesado en la información sobre cómo funciona en segundo plano.  

### Paso 3: controlar las solicitudes del servidor relacionadas con inserción  

Ahora configure rutas para procesar las solicitudes de inserción del cliente de PWA, incluido el servicio de la clave pública VAPID y el registro del cliente para recibir mensajes Push.  

En un escenario real, una notificación push probablemente se origina desde un evento de la lógica del servidor.  Para simplificar las cosas aquí, debes agregar un botón de **notificación de inserción** a nuestra página principal de PWA para generar las inserciones de nuestro servidor y un `/sendNotification` extremo \(ruta de servidor \) para administrar dichas solicitudes.  

En el `index.js` archivo, Anexe las siguientes rutas justo después del código de inicialización VAPID que agregó en [paso 2] [#step-2---Generate-VAPID-for-Server].  

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

Con el código del lado del servidor en contexto, se sondea en las notificaciones Push en el cliente de PWA.  

### Paso 4: suscribirse a notificaciones push  

Como parte de su rol como proxy de redes de PWA, los trabajos de servicio controlan los eventos Push y las interacciones de notificaciones del sistema.  Sin embargo, como lo configuramos primero \(o registrando \) un trabajador de servicio, se realiza una suscripción a las notificaciones push de servidor en el subproceso de interfaz de usuario principal de PWA y se requiere conectividad de red.  La suscripción a notificaciones Push requiere un registro de trabajo de servicio activo, por lo que primero debes verificar que el trabajo de tu servicio esté instalado y activo antes de intentar suscribirte a las notificaciones Push.  

Antes de crear una nueva suscripción de inserción, Microsoft Edge comprueba si el usuario ha concedido permiso de PWA para recibir notificaciones.  En caso contrario, el explorador le pide permiso para el usuario.  Si el permiso es denegado, la solicitud para `registration.pushManager.subscribe` iniciar un `DOMException` , por lo tanto, debe controlarlo.  Para obtener más información sobre la administración de permisos, vea [notificaciones Push en Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

En el `pwabuilder-sw-register.js` archivo, Anexe el siguiente código.  

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

Revise la documentación de MDN en la interfaz de [PushManager][MDNPushManager] y en los documentos de NPM en la biblioteca de [inserción web][NPMWebPushUsage] para obtener más información sobre cómo funcionan las API y las distintas opciones relacionadas.  

### Paso 5: configurar los controladores de eventos Push y notificationclick  

Con nuestra configuración de suscripciones Push, el resto del trabajo se realiza en el trabajador del servicio.  En primer lugar debe configurar un controlador para eventos Push enviados por el servidor y responder con una notificación del sistema \(si se ha concedido permiso \) que muestra la carga de datos Push.  A continuación, agrega un controlador de clic para que la notificación del sistema descarte la notificación y se ordene mediante una lista de las ventanas abiertas para abrir, enfocar o abrir y centrar la página de cliente de PWA prevista.  

En el `pwabuilder-sw.js` archivo, anexe los controladores siguientes.  

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

### Paso 6: pruébelo  

Tiempo para probar las notificaciones Push en el PWA.  

1.  Ejecute \( `F5` \) su PWA en el explorador.  Debido a que modificó el código de trabajo de servicio \( `pwabuilder-sw.js` \), debe abrir el depurador de DevTools \( `F12` \) en el panel de **información general de trabajos del servicio** y **anular el registro** del trabajador del servicio y volver a cargar \( `F5` \) la página para volver a registrarlo \(o hacer clic en **Actualizar**\).  En un escenario de producción, el explorador comprueba periódicamente si hay actualizaciones de los trabajadores del servicio e instala las actualizaciones en segundo plano.  Para obtener resultados inmediatos, debes forzarlo aquí.  
    
    Como el trabajador de servicio se activa e intenta suscribir su PWA a las notificaciones push, debe ver un cuadro de diálogo de permisos en la parte inferior de la página.  
    
    ![Cuadro de diálogo de permisos para habilitar las notificaciones][ImageNotificationPermission]  
    
    Elija **sí** para habilitar las notificaciones del sistema para su PWA.  
    
1.  En el panel Descripción general del trabajo del servicio, intente elegir el botón de  **comando** .  Debe aparecer una notificación del sistema con el \(mensaje de inserción de prueba "DevTools" \).  
    
    ![Insertar una notificación desde DevTools][ImageDevtoolsPush]  
    
1.  A continuación, seleccione el botón **Enviar notificación** en la Página principal de su PWA.  Esta vez aparece una notificación del sistema con la carga de su servidor.  
    
    ![Insertar una notificación desde el servidor PWA][ImagePwaPush]  
    
    Si no hace clic en \(o activa \) una notificación del sistema, se descarta después de varios segundos y se pone en cola en el centro de actividades de Windows.  
    
    ![Notificaciones en el centro de actividades de Windows][ImageWindowsActionCenter]  
    
    Tiene los conceptos básicos de las notificaciones push de PWA.  En una aplicación real, los pasos siguientes se implementan de una manera de administrar y almacenar suscripciones Push y de [cifrar][NPMWebPushEncrypt] correctamente los datos de carga que se envían a través de la red.  
    
## Ir más allá  

Esta guía demostró la anatomía básica de una aplicación web progresiva y herramientas de desarrollo de PWA de Microsoft, como Visual Studio, PWA Builder y Edge DevTools.  

Por supuesto, hay mucho más que suponen [un excelente PWA][PwaEdgehtmlIndexRequirements] más allá de lo que Lee aquí, como el diseño con capacidad de respuesta, la vinculación profunda, las [pruebas entre exploradores][BrowserStackTestEdgeBrowser] y otras [prácticas recomendadas][Webhint] \(sin mencionar la funcionalidad de la aplicación! \), pero espero que esta guía le haya proporcionado una sólida introducción de conceptos básicos de PWA y algunas ideas para empezar.  Si tiene más preguntas sobre el desarrollo de PWA con Windows o con Visual Studio, deje un comentario.  

Revise las demás guías de PWA para obtener información sobre cómo incrementar la participación de los clientes y ofrecer una experiencia de la aplicación integrada en el sistema operativo.  

*   [Adaptación de ventanas][PwaEdgehtmlWindowsFeatures]. Con la simple detección de características, puede mejorar progresivamente su PWA para los clientes de Windows 10 a través de las API de Windows Runtime \(WinRT \) nativas, como las que se usan para personalizar las notificaciones del menú **Inicio** de Windows y la barra de tareas Jumplists, y \(tras el permiso \) trabajar con recursos de usuario, como fotos, música y calendario.  
*   [PWAs en Microsoft Store][PwaEdgehtmlMicrosoftStore].  Obtenga más información sobre las ventajas de la distribución de la tienda de aplicaciones y cómo enviar su PWA.  

## Consulte también  

*   [Aplicaciones web progresivas en los documentos web de MDN][MDNProgressiveWebApps] : guía excelente sobre aplicaciones web progresivas.  
*   [Aplicaciones web progresivas en Web. dev][WebDevProgressiveWebApps] : excelente guía sobre las aplicaciones web progresivas.  
*   [Rocks de aplicaciones web progresivas][ProgressiveWebApps] : exhibe ejemplos reales de PWAs.  
*   [Lectores de noticias de piratas informáticos como aplicaciones web progresivas][HackerNewsProgressiveWebApps] : compara diferentes marcos de trabajo y patrones de rendimiento para implementar un ejemplo \(lector de noticias de hacker \) PWA.  

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

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requisitos: aplicaciones web progresivas \(EdgeHTML \) en Windows | Microsoft docs"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Aplicaciones web progresivas \(EdgeHTML \) en Microsoft Store | Microsoft docs"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Personalizar su PWA \(EdgeHTML \) para Windows | Microsoft docs"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Directivas de Microsoft Store | Microsoft docs"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Tutorial: crear una aplicación de Node.js y Express en Visual Studio | Microsoft docs"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publicar en el servicio de aplicaciones de Azure: crear una aplicación de Node.js y Express en Visual Studio | Microsoft docs"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "¿Qué es una aplicación de la plataforma universal de Windows \(UWP \)?  | Microsoft docs"  

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
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. PostMessage \(\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicaciones web progresivas \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabajadores de servicio | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifiesto de la aplicación Web | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. prototype. PostMessage \(\) | MDN"  

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
