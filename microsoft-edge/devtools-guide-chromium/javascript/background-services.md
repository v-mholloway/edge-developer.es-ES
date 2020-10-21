---
description: Cómo depurar la recuperación en segundo plano, la sincronización en segundo plano, las notificaciones y los mensajes push con Microsoft Edge DevTools.
title: Depurar servicios en segundo plano con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fb5e408eb261ae3b2145780a1d7d5566c4501936
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124820"
---
<!-- Copyright Kayce Basques 
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0
       
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Depurar servicios en segundo plano con Microsoft Edge DevTools  

La sección de **servicios en segundo plano** de Microsoft Edge DevTools es una colección de herramientas para las API de JavaScript que permite que el sitio web envíe y reciba actualizaciones incluso cuando un usuario no tiene abierto su sitio Web.  
Un servicio en segundo plano es funcionalmente similar a [proceso en segundo plano] [WikiBackgroundProcess].  
Microsoft Edge DevTools considera que cada una de las siguientes API es un servicio en segundo plano:  

*   [Captura en segundo plano](#background-fetch)  
*   [Sincronización en segundo plano](#background-sync)  
*   [Notificaciones](#notifications)  
*   [Mensajes Push](#push-messages)  
    
Microsoft Edge DevTools puede registrar eventos de servicio en segundo plano durante 3 días, incluso cuando DevTools no está abierto.  
Esto puede ayudarte a asegurarte de que los eventos se envían y reciben según lo previsto.  También puedes inspeccionar los detalles de cada evento.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   El panel de **mensajes Push**  
:::image-end:::  

## Captura en segundo plano  

La **API de captura en segundo plano** permite a un **trabajador de servicio** descargar de manera confiable recursos grandes, como películas o podcasts, como un servicio en segundo plano.  Para registrar el evento de captura en segundo plano durante 3 días, incluso cuando DevTools no está abierto:  

<!--Todo: add background fetch api section when available -->  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra el panel de la **aplicación** .  
1.  Abrir el panel de **captura en segundo plano** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       El panel **captura en segundo plano**  
    :::image-end:::  
    
1.  Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).  
   Después de desencadenar cierta actividad de captura en segundo plano, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Registro de eventos en el panel **captura en segundo plano**  
    :::image-end:::  
    
1.  Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Ver los detalles de un evento en el panel **captura en segundo plano**  
    :::image-end:::  
    
## Sincronización en segundo plano  

La **API de sincronización en segundo plano** permite a un **trabajador de servicios** sin conexión enviar datos a un servidor una vez que se ha restablecido una conexión de Internet confiable.  Para registrar eventos de sincronización en segundo plano durante 3 días, incluso cuando DevTools no está abierto:  

<!--Todo: add background sync api section when available -->  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra el panel de la **aplicación** .  
1.  Abrir el panel **sincronización en segundo plano** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       El panel **sincronización en segundo plano**  
    :::image-end:::  
    
1.  Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).  
   Después de desencadenar cierta actividad de sincronización en segundo plano, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Registro de eventos en el panel de **sincronización en segundo plano**  
    :::image-end:::  
    
1.  Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Ver los detalles de un evento en el panel de **sincronización en segundo plano**  
    :::image-end:::  
    
## Notificaciones  

Después de que un **trabajador de servicio** ha recibido un [mensaje de inserción][MDNPush] de un servidor, el trabajador de servicio usa la [API de notificaciones][MDNNotifications] para mostrar los datos a un usuario.  Para registrar las notificaciones por 3 días, incluso cuando DevTools no está abierto:  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra el panel de la **aplicación** .  
1.  Abrir el panel **notificaciones** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       El panel **notificaciones**  
    :::image-end:::  
    
1.  Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).  
   Después de desencadenar cierta actividad de notificaciones, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Registro de eventos en el panel de **notificaciones**  
    :::image-end:::  
    
1.  Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Ver los detalles de un evento en el panel de **notificaciones**  
    :::image-end:::  
    
## Mensajes Push  

Para mostrar una notificación de inserción a un usuario, un **trabajador de servicio** primero debe usar la API de [mensajes Push][MDNPush] para recibir datos de un servidor.  Cuando el trabajador del servicio está listo para mostrar la notificación, usa la [API de notificaciones][MDNNotifications].  Para registrar mensajes de inserción por 3 días, incluso cuando DevTools no está abierto:  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra el panel de la **aplicación** .  
1.  Abra el panel de **mensajes Push** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Abrir el panel de **mensajes Push**  
    :::image-end:::  
    
1.  Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).  
    Después de desencadenar cierta actividad de mensajes Push, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Registro de eventos en el panel **mensajes Push**  
    :::image-end:::  
    
1.  Haga clic en un evento para ver los detalles en el espacio situado debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Ver los detalles de un evento en el panel de **mensajes Push**  
    :::image-end:::  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Abrir herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "proceso en segundo plano: Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
