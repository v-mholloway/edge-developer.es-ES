---
title: Depurar servicios en segundo plano con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0ac2a057307a939069cbb3b48ecd38c9de71e5db
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581834"
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





# <span data-ttu-id="f4866-103">Depurar servicios en segundo plano con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f4866-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="f4866-104">La sección de **servicios en segundo plano** de Microsoft Edge DevTools es una colección de herramientas para las API de JavaScript que permite que el sitio web envíe y reciba actualizaciones incluso cuando un usuario no tiene abierto su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="f4866-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="f4866-105">Un servicio en segundo plano es funcionalmente similar a [proceso en segundo plano] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="f4866-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="f4866-106">Microsoft Edge DevTools considera que cada una de las siguientes API es un servicio en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="f4866-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="f4866-107">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="f4866-108">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="f4866-109">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="f4866-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="f4866-110">Mensajes Push</span><span class="sxs-lookup"><span data-stu-id="f4866-110">Push Messages</span></span>](#push-messages)  

<span data-ttu-id="f4866-111">Microsoft Edge DevTools puede registrar eventos de servicio en segundo plano durante 3 días, incluso cuando DevTools no está abierto.</span><span class="sxs-lookup"><span data-stu-id="f4866-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="f4866-112">Esto puede ayudarte a asegurarte de que los eventos se envían y reciben según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="f4866-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="f4866-113">También puede inspeccionar los detalles de cada evento.</span><span class="sxs-lookup"><span data-stu-id="f4866-113">You can also inspect the details of each event.</span></span>  

> ##### <span data-ttu-id="f4866-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="f4866-114">Figure 1</span></span>  
> <span data-ttu-id="f4866-115">Ver los detalles de un evento en el panel de mensajes Push</span><span class="sxs-lookup"><span data-stu-id="f4866-115">Viewing the details of an event in the Push Messaging pane</span></span>  
> ![Ver los detalles de un evento en el panel de mensajes Push][PushDetails]  

## <span data-ttu-id="f4866-117">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-117">Background Fetch</span></span>   

<span data-ttu-id="f4866-118">La *API de captura en segundo plano*\* permite a un **trabajador de servicio** descargar de manera confiable recursos grandes, como películas o podcasts, como un servicio en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f4866-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="f4866-119">Para registrar el evento de captura en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="f4866-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="f4866-120">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="f4866-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="f4866-121">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="f4866-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="f4866-122">Abrir el panel de **captura en segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="f4866-122">Open the **Background Fetch** pane.</span></span>  
    
    > ##### <span data-ttu-id="f4866-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="f4866-123">Figure 2</span></span>  
    > <span data-ttu-id="f4866-124">El panel captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-124">The Background Fetch pane</span></span>  
    > ![El panel captura en segundo plano][FetchEmpty]  
    
1.  <span data-ttu-id="f4866-126">Haga **clic en grabar** ![ Registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="f4866-126">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="f4866-127">Después de desencadenar cierta actividad de captura en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-127">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-128">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="f4866-128">Figure 3</span></span>  
    > <span data-ttu-id="f4866-129">Registro de eventos en el panel captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-129">A log of events in the Background Fetch pane</span></span>  
    > ![Registro de eventos en el panel captura en segundo plano][FetchLog]  
    
1.  <span data-ttu-id="f4866-131">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-131">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-132">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="f4866-132">Figure 4</span></span>  
    > <span data-ttu-id="f4866-133">Ver los detalles de un evento en el panel captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-133">Viewing the details of an event in the Background Fetch pane</span></span>  
    > ![Ver los detalles de un evento en el panel captura en segundo plano][FetchDetails]  

## <span data-ttu-id="f4866-135">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-135">Background Sync</span></span>   

<span data-ttu-id="f4866-136">La **API de sincronización en segundo plano** permite a un **trabajador de servicios** sin conexión enviar datos a un servidor una vez que se ha restablecido una conexión de Internet confiable.</span><span class="sxs-lookup"><span data-stu-id="f4866-136">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="f4866-137">Para registrar eventos de sincronización en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="f4866-137">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="f4866-138">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="f4866-138">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="f4866-139">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="f4866-139">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="f4866-140">Abrir el panel **sincronización en segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="f4866-140">Open the **Background Sync** pane.</span></span>  
    
    > ##### <span data-ttu-id="f4866-141">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="f4866-141">Figure 5</span></span>  
    > <span data-ttu-id="f4866-142">El panel sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-142">The Background Sync pane</span></span>  
    > ![El panel sincronización en segundo plano][SyncEmpty]  
    
1.  <span data-ttu-id="f4866-144">Haga **clic en grabar** ![ Registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="f4866-144">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="f4866-145">Después de desencadenar cierta actividad de sincronización en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-145">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-146">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="f4866-146">Figure 6</span></span>  
    > <span data-ttu-id="f4866-147">Registro de eventos en el panel de sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-147">A log of events in the Background Sync pane</span></span>  
    > ![Registro de eventos en el panel de sincronización en segundo plano][SyncLog]  
    
1.  <span data-ttu-id="f4866-149">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-149">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-150">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="f4866-150">Figure 7</span></span>  
    > <span data-ttu-id="f4866-151">Ver los detalles de un evento en el panel de sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4866-151">Viewing the details of an event in the Background Sync pane</span></span>  
    > ![Ver los detalles de un evento en el panel de sincronización en segundo plano][SyncDetails]  
    
## <span data-ttu-id="f4866-153">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="f4866-153">Notifications</span></span> 

<span data-ttu-id="f4866-154">Después de que un **trabajador de servicio** ha recibido un [mensaje de inserción][MDNPush] de un servidor, el trabajador de servicio usa la [API de notificaciones][MDNNotifications] para mostrar los datos a un usuario.</span><span class="sxs-lookup"><span data-stu-id="f4866-154">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="f4866-155">Para registrar las notificaciones por 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="f4866-155">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="f4866-156">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="f4866-156">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="f4866-157">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="f4866-157">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="f4866-158">Abrir el panel **notificaciones** .</span><span class="sxs-lookup"><span data-stu-id="f4866-158">Open the **Notifications** pane.</span></span>  
    
    > ##### <span data-ttu-id="f4866-159">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="f4866-159">Figure 8</span></span>  
    > <span data-ttu-id="f4866-160">El panel notificaciones</span><span class="sxs-lookup"><span data-stu-id="f4866-160">The Notifications pane</span></span>  
    > ![El panel notificaciones][NotificationsEmpty]  
    
1.  <span data-ttu-id="f4866-162">Haga **clic en grabar** ![ Registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="f4866-162">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="f4866-163">Después de desencadenar cierta actividad de notificaciones, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-163">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-164">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="f4866-164">Figure 9</span></span>  
    > <span data-ttu-id="f4866-165">Registro de eventos en el panel de notificaciones</span><span class="sxs-lookup"><span data-stu-id="f4866-165">A log of events in the Notifications pane</span></span>  
    > ![Registro de eventos en el panel de notificaciones][NotificationsLog]  
    
1.  <span data-ttu-id="f4866-167">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-167">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-168">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="f4866-168">Figure 10</span></span>  
    > <span data-ttu-id="f4866-169">Ver los detalles de un evento en el panel de notificaciones</span><span class="sxs-lookup"><span data-stu-id="f4866-169">Viewing the details of an event in the Notifications pane</span></span>  
    > ![Ver los detalles de un evento en el panel de notificaciones][NotificationsDetails]  
    
## <span data-ttu-id="f4866-171">Mensajes Push</span><span class="sxs-lookup"><span data-stu-id="f4866-171">Push Messages</span></span> 

<span data-ttu-id="f4866-172">Para mostrar una notificación de inserción a un usuario, un **trabajador de servicio** primero debe usar la API de [mensajes Push][MDNPush] para recibir datos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="f4866-172">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="f4866-173">Cuando el trabajador del servicio está listo para mostrar la notificación, usa la [API de notificaciones][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="f4866-173">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="f4866-174">Para registrar mensajes de inserción por 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="f4866-174">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="f4866-175">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="f4866-175">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="f4866-176">Abra el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="f4866-176">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="f4866-177">Abra el panel de **mensajes Push** .</span><span class="sxs-lookup"><span data-stu-id="f4866-177">Open the **Push Messaging** pane.</span></span>  
    
    > ##### <span data-ttu-id="f4866-178">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="f4866-178">Figure 11</span></span>  
    > <span data-ttu-id="f4866-179">El panel de mensajes Push</span><span class="sxs-lookup"><span data-stu-id="f4866-179">The Push Messaging pane</span></span>  
    > ![El panel de mensajes Push][PushEmpty]  

1.  <span data-ttu-id="f4866-181">Haga **clic en grabar** ![ Registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="f4866-181">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="f4866-182">Después de desencadenar cierta actividad de mensajes Push, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-182">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-183">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="f4866-183">Figure 12</span></span>  
    > <span data-ttu-id="f4866-184">Registro de eventos en el panel mensajes Push</span><span class="sxs-lookup"><span data-stu-id="f4866-184">A log of events in the Push Messaging pane</span></span>  
    > ![Registro de eventos en el panel mensajes Push][PushLog]  

1.  <span data-ttu-id="f4866-186">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4866-186">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="f4866-187">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="f4866-187">Figure 13</span></span>  
    > <span data-ttu-id="f4866-188">Ver los detalles de un evento en el panel de mensajes Push</span><span class="sxs-lookup"><span data-stu-id="f4866-188">Viewing the details of an event in the Push Messaging pane</span></span>  
    > ![Ver los detalles de un evento en el panel de mensajes Push][PushDetails2]  
    
 



<!-- image links -->  

[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[PushDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Ilustración 1: ver los detalles de un evento en el panel de mensajes Push"  
[FetchEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-empty.msft.png "Ilustración 2: el panel de captura en segundo plano"  
[FetchLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch.msft.png "Ilustración 3: un registro de eventos en el panel captura en segundo plano"  
[FetchDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-details.msft.png "Figura 4: visualización de los detalles de un evento en el panel captura en segundo plano"  
[SyncEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-empty.msft.png "Ilustración 5: el panel de sincronización en segundo plano"  
[SyncLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync.msft.png "Ilustración 6: un registro de eventos en el panel de sincronización en segundo plano"  
[SyncDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-details.msft.png "Ilustración 7: visualización de los detalles de un evento en el panel de sincronización en segundo plano"  
[NotificationsEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-empty.msft.png "Ilustración 8: el panel notificaciones"  
[NotificationsLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications.msft.png "Ilustración 9: un registro de eventos en el panel de notificaciones"  
[NotificationsDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-details.msft.png "Ilustración 10: visualización de los detalles de un evento en el panel de notificaciones"  
[PushEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-empty.msft.png "Ilustración 11: el panel de mensajes Push"  
[PushLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Ilustración 12: un registro de eventos en el panel Push Messaging"  
[PushDetails2]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-details.msft.png "Ilustración 13: ver los detalles de un evento en el panel de mensajes Push"  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Abrir las herramientas para desarrolladores de Microsoft Edge (cromo)"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "proceso en segundo plano: Wikipedia"  

> [!NOTE]
> <span data-ttu-id="f4866-207">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f4866-207">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f4866-208">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f4866-208">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f4866-210">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f4866-210">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
