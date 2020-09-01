---
title: Depurar servicios en segundo plano con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1fecd6f9c1dceb39482bf8c4ade71918e32dec00
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983327"
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





# <span data-ttu-id="31c4a-103">Depurar servicios en segundo plano con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="31c4a-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="31c4a-104">La sección de **servicios en segundo plano** de Microsoft Edge DevTools es una colección de herramientas para las API de JavaScript que permite que el sitio web envíe y reciba actualizaciones incluso cuando un usuario no tiene abierto su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="31c4a-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="31c4a-105">Un servicio en segundo plano es funcionalmente similar a [proceso en segundo plano] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="31c4a-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="31c4a-106">Microsoft Edge DevTools considera que cada una de las siguientes API es un servicio en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="31c4a-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="31c4a-107">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="31c4a-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="31c4a-108">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="31c4a-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="31c4a-109">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="31c4a-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="31c4a-110">Mensajes Push</span><span class="sxs-lookup"><span data-stu-id="31c4a-110">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="31c4a-111">Microsoft Edge DevTools puede registrar eventos de servicio en segundo plano durante 3 días, incluso cuando DevTools no está abierto.</span><span class="sxs-lookup"><span data-stu-id="31c4a-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="31c4a-112">Esto puede ayudarte a asegurarte de que los eventos se envían y reciben según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="31c4a-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="31c4a-113">También puedes inspeccionar los detalles de cada evento.</span><span class="sxs-lookup"><span data-stu-id="31c4a-113">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Ver los detalles de un evento en el panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="31c4a-115">Ver los detalles de un evento en el panel de **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="31c4a-115">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="31c4a-116">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="31c4a-116">Background Fetch</span></span>   

<span data-ttu-id="31c4a-117">La *API de captura en segundo plano*\* permite a un **trabajador de servicio** descargar de manera confiable recursos grandes, como películas o podcasts, como un servicio en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="31c4a-117">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="31c4a-118">Para registrar el evento de captura en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="31c4a-118">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="31c4a-119">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="31c4a-119">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="31c4a-120">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-120">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="31c4a-121">Abrir el panel de **captura en segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-121">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="El panel captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="31c4a-123">El panel **captura en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="31c4a-123">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-124">Haga clic en **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31c4a-124">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="31c4a-125">Después de desencadenar cierta actividad de captura en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-125">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Registro de eventos en el panel captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="31c4a-127">Registro de eventos en el panel **captura en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="31c4a-127">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-128">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-128">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Ver los detalles de un evento en el panel captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="31c4a-130">Ver los detalles de un evento en el panel **captura en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="31c4a-130">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31c4a-131">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="31c4a-131">Background Sync</span></span>   

<span data-ttu-id="31c4a-132">La **API de sincronización en segundo plano** permite a un **trabajador de servicios** sin conexión enviar datos a un servidor una vez que se ha restablecido una conexión de Internet confiable.</span><span class="sxs-lookup"><span data-stu-id="31c4a-132">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="31c4a-133">Para registrar eventos de sincronización en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="31c4a-133">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="31c4a-134">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="31c4a-134">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="31c4a-135">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-135">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="31c4a-136">Abrir el panel **sincronización en segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-136">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="El panel sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="31c4a-138">El panel **sincronización en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="31c4a-138">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-139">Haga clic en **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31c4a-139">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="31c4a-140">Después de desencadenar cierta actividad de sincronización en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-140">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Registro de eventos en el panel de sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="31c4a-142">Registro de eventos en el panel de **sincronización en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="31c4a-142">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-143">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-143">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Ver los detalles de un evento en el panel de sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="31c4a-145">Ver los detalles de un evento en el panel de **sincronización en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="31c4a-145">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31c4a-146">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="31c4a-146">Notifications</span></span> 

<span data-ttu-id="31c4a-147">Después de que un **trabajador de servicio** ha recibido un [mensaje de inserción][MDNPush] de un servidor, el trabajador de servicio usa la [API de notificaciones][MDNNotifications] para mostrar los datos a un usuario.</span><span class="sxs-lookup"><span data-stu-id="31c4a-147">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="31c4a-148">Para registrar las notificaciones por 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="31c4a-148">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="31c4a-149">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="31c4a-149">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="31c4a-150">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-150">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="31c4a-151">Abrir el panel **notificaciones** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-151">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="El panel notificaciones" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="31c4a-153">El panel **notificaciones**</span><span class="sxs-lookup"><span data-stu-id="31c4a-153">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-154">Haga clic en **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31c4a-154">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="31c4a-155">Después de desencadenar cierta actividad de notificaciones, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-155">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Registro de eventos en el panel de notificaciones" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="31c4a-157">Registro de eventos en el panel de **notificaciones**</span><span class="sxs-lookup"><span data-stu-id="31c4a-157">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-158">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-158">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Ver los detalles de un evento en el panel de notificaciones" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="31c4a-160">Ver los detalles de un evento en el panel de **notificaciones**</span><span class="sxs-lookup"><span data-stu-id="31c4a-160">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31c4a-161">Mensajes Push</span><span class="sxs-lookup"><span data-stu-id="31c4a-161">Push Messages</span></span> 

<span data-ttu-id="31c4a-162">Para mostrar una notificación de inserción a un usuario, un **trabajador de servicio** primero debe usar la API de [mensajes Push][MDNPush] para recibir datos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="31c4a-162">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="31c4a-163">Cuando el trabajador del servicio está listo para mostrar la notificación, usa la [API de notificaciones][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="31c4a-163">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="31c4a-164">Para registrar mensajes de inserción por 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="31c4a-164">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="31c4a-165">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="31c4a-165">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="31c4a-166">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-166">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="31c4a-167">Abra el panel de **mensajes Push** .</span><span class="sxs-lookup"><span data-stu-id="31c4a-167">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="31c4a-169">El panel de **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="31c4a-169">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-170">Haga clic en **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31c4a-170">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="31c4a-171">Después de desencadenar cierta actividad de mensajes Push, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-171">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Registro de eventos en el panel mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="31c4a-173">Registro de eventos en el panel **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="31c4a-173">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31c4a-174">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="31c4a-174">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Ver los detalles de un evento en el panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="31c4a-176">Ver los detalles de un evento en el panel de **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="31c4a-176">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

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
> <span data-ttu-id="31c4a-181">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31c4a-181">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="31c4a-182">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="31c4a-182">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="31c4a-184">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31c4a-184">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
