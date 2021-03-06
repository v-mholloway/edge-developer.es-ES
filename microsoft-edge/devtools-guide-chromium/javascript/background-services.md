---
description: Cómo depurar la captura en segundo plano, la sincronización en segundo plano, las notificaciones y los mensajes de inserción con Microsoft Edge DevTools.
title: Depurar servicios en segundo plano con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cf3459e7b5f80a695a855ffdd0c249c2bc223d31
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398640"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a>Depurar servicios en segundo plano con Microsoft Edge DevTools  

La sección **Servicios** en segundo plano de Microsoft Edge DevTools es una colección de herramientas para las API de JavaScript que permite al sitio web enviar y recibir actualizaciones incluso cuando un usuario no tiene el sitio web abierto.  
Un servicio en segundo plano es funcionalmente similar a un [proceso en segundo plano][WikiBackgroundProcess].  
Microsoft Edge DevTools considera que cada una de las siguientes API es un servicio en segundo plano:  

*   [Captura en segundo plano](#background-fetch)  
*   [Sincronización en segundo plano](#background-sync)  
*   [Notificaciones](#notifications)  
*   [Mensajes de inserción](#push-messages)  
    
Microsoft Edge DevTools puede registrar eventos de servicio en segundo plano durante 3 días, incluso cuando DevTools no está abierto.  
El registro de eventos de servicio en segundo plano puede ayudarle a asegurarse de que los eventos se envían y reciben según lo esperado.  También puede inspeccionar los detalles de cada evento.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="El panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   El **panel Mensajería de inserción**  
:::image-end:::  

## <a name="background-fetch"></a>Captura en segundo plano  

La **API de captura en** segundo plano permite a un trabajador de servicio descargar recursos grandes de forma confiable, como películas o podcasts, como un servicio en segundo plano. ****  Para registrar el evento Background Fetch durante 3 días, incluso cuando DevTools no está abierto:  

<!--Todo: add background fetch api section when available -->  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra la **herramienta Aplicación.**  
1.  Abra el **panel Captura en** segundo plano.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Panel Captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Panel **Captura en** segundo plano  
    :::image-end:::  
    
1.  Elija **Record** \( ![ Record ][ImageRecordIcon] \).  
   Después de desencadenar alguna actividad de captura en segundo plano, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Registro de eventos en el panel Captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Registro de eventos en el panel **Captura en** segundo plano  
    :::image-end:::  
    
1.  Elija un evento para ver sus detalles en el espacio debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Ver los detalles de un evento en el panel Captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Ver los detalles de un evento en el panel **Captura en** segundo plano  
    :::image-end:::  
    
## <a name="background-sync"></a>Sincronización en segundo plano  

La API de sincronización **** **en** segundo plano permite a un trabajador del servicio sin conexión enviar datos a un servidor una vez que haya vuelto a establecer una conexión a Internet confiable.  Para registrar eventos de sincronización en segundo plano durante 3 días, incluso cuando DevTools no está abierto:  

<!--Todo: add background sync api section when available -->  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra la **herramienta Aplicación.**  
1.  Abra el **panel Sincronización en** segundo plano.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Panel Sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Panel **Sincronización en** segundo plano  
    :::image-end:::  
    
1.  Elija **Record** \( ![ Record ][ImageRecordIcon] \).  
   Después de desencadenar alguna actividad de sincronización en segundo plano, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Un registro de eventos en el panel Sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Un registro de eventos en el panel **Sincronización en** segundo plano  
    :::image-end:::  
    
1.  Elija un evento para ver sus detalles en el espacio debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Ver los detalles de un evento en el panel Sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Ver los detalles de un evento en el panel **Sincronización en** segundo plano  
    :::image-end:::  
    
## <a name="notifications"></a>Notificaciones  

Después de **que un trabajador de** servicio haya recibido un mensaje [de][MDNPush] inserción de un servidor, el trabajador del servicio usa la [API de][MDNNotifications] notificaciones para mostrar los datos a un usuario.  Para registrar notificaciones durante 3 días, incluso cuando DevTools no está abierto:  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra la **herramienta Aplicación.**  
1.  Abra el **panel Notificaciones.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Panel Notificaciones" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Panel **Notificaciones**  
    :::image-end:::  
    
1.  Elija **Record** \( ![ Record ][ImageRecordIcon] \).  
   Después de desencadenar alguna actividad notifications, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Un registro de eventos en el panel Notificaciones" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Un registro de eventos en el **panel Notificaciones**  
    :::image-end:::  
    
1.  Elija un evento para ver sus detalles en el espacio debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Ver los detalles de un evento en el panel Notificaciones" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Ver los detalles de un evento en el **panel Notificaciones**  
    :::image-end:::  
    
## <a name="push-messages"></a>Mensajes de inserción  

Para mostrar una notificación de **** inserción a un usuario, un trabajador del servicio primero debe usar la [API][MDNPush] de mensajes de inserción para recibir datos de un servidor.  Cuando el trabajador del servicio está listo para mostrar la notificación, usa la [API de notificaciones][MDNNotifications].  Para registrar mensajes de inserción durante 3 días, incluso cuando DevTools no está abierto:  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra la **herramienta Aplicación.**  
1.  Abra el **panel Mensajería de inserción.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Abrir el panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Abrir el **panel Mensajería de inserción**  
    :::image-end:::  
    
1.  Elija **Record** \( ![ Record ][ImageRecordIcon] \).  
    Después de desencadenar alguna actividad de mensaje de inserción, DevTools registra los eventos en la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Registro de eventos en el panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Registro de eventos en el panel **Mensajería de** inserción  
    :::image-end:::  
    
1.  Elija un evento para ver los detalles en el espacio debajo de la tabla.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Ver los detalles de un evento en el panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Ver los detalles de un evento en el **panel Mensajería de** inserción  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Abra Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notificaciones API | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Api de inserción | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Proceso en segundo plano - Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
