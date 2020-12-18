---
description: Cómo depurar la recuperación en segundo plano, la sincronización en segundo plano, las notificaciones y los mensajes push con Microsoft Edge DevTools.
title: Depurar servicios en segundo plano con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: df832ed2f56faf6412fd42bc080d8af7705d26d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230680"
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

# <span data-ttu-id="c8b71-104">Depurar servicios en segundo plano con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c8b71-104">Debug Background Services With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c8b71-105">La sección de **servicios en segundo plano** de Microsoft Edge DevTools es una colección de herramientas para las API de JavaScript que permite que el sitio web envíe y reciba actualizaciones incluso cuando un usuario no tiene abierto su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="c8b71-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="c8b71-106">Un servicio en segundo plano es funcionalmente similar a [proceso en segundo plano] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="c8b71-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="c8b71-107">Microsoft Edge DevTools considera que cada una de las siguientes API es un servicio en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="c8b71-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="c8b71-108">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8b71-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="c8b71-109">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8b71-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="c8b71-110">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="c8b71-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="c8b71-111">Mensajes Push</span><span class="sxs-lookup"><span data-stu-id="c8b71-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="c8b71-112">Microsoft Edge DevTools puede registrar eventos de servicio en segundo plano durante 3 días, incluso cuando DevTools no está abierto.</span><span class="sxs-lookup"><span data-stu-id="c8b71-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="c8b71-113">Esto puede ayudarte a asegurarte de que los eventos se envían y reciben según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="c8b71-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="c8b71-114">También puedes inspeccionar los detalles de cada evento.</span><span class="sxs-lookup"><span data-stu-id="c8b71-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="El panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="c8b71-116">El panel de **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="c8b71-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="c8b71-117">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8b71-117">Background Fetch</span></span>  

<span data-ttu-id="c8b71-118">La **API de captura en segundo plano** permite a un **trabajador de servicio** descargar de manera confiable recursos grandes, como películas o podcasts, como un servicio en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c8b71-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="c8b71-119">Para registrar el evento de captura en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="c8b71-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="c8b71-120">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c8b71-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c8b71-121">Abra la herramienta **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="c8b71-122">Abrir el panel de **captura en segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="El panel captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="c8b71-124">El panel **captura en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c8b71-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-125">Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c8b71-125">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c8b71-126">Después de desencadenar cierta actividad de captura en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Registro de eventos en el panel captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="c8b71-128">Registro de eventos en el panel **captura en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c8b71-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-129">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Ver los detalles de un evento en el panel captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="c8b71-131">Ver los detalles de un evento en el panel **captura en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c8b71-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c8b71-132">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8b71-132">Background Sync</span></span>  

<span data-ttu-id="c8b71-133">La **API de sincronización en segundo plano** permite a un **trabajador de servicios** sin conexión enviar datos a un servidor una vez que se ha restablecido una conexión de Internet confiable.</span><span class="sxs-lookup"><span data-stu-id="c8b71-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="c8b71-134">Para registrar eventos de sincronización en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="c8b71-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="c8b71-135">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c8b71-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c8b71-136">Abra la herramienta **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="c8b71-137">Abrir el panel **sincronización en segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="El panel sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="c8b71-139">El panel **sincronización en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c8b71-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-140">Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c8b71-140">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c8b71-141">Después de desencadenar cierta actividad de sincronización en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Registro de eventos en el panel de sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="c8b71-143">Registro de eventos en el panel de **sincronización en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c8b71-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-144">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Ver los detalles de un evento en el panel de sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="c8b71-146">Ver los detalles de un evento en el panel de **sincronización en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c8b71-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c8b71-147">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="c8b71-147">Notifications</span></span>  

<span data-ttu-id="c8b71-148">Después de que un **trabajador de servicio** ha recibido un [mensaje de inserción][MDNPush] de un servidor, el trabajador de servicio usa la [API de notificaciones][MDNNotifications] para mostrar los datos a un usuario.</span><span class="sxs-lookup"><span data-stu-id="c8b71-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="c8b71-149">Para registrar las notificaciones por 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="c8b71-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c8b71-150">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c8b71-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c8b71-151">Abra la herramienta **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="c8b71-152">Abrir el panel **notificaciones** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="El panel notificaciones" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="c8b71-154">El panel **notificaciones**</span><span class="sxs-lookup"><span data-stu-id="c8b71-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-155">Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c8b71-155">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c8b71-156">Después de desencadenar cierta actividad de notificaciones, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Registro de eventos en el panel de notificaciones" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="c8b71-158">Registro de eventos en el panel de **notificaciones**</span><span class="sxs-lookup"><span data-stu-id="c8b71-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-159">Haga clic en un evento para ver sus detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Ver los detalles de un evento en el panel de notificaciones" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="c8b71-161">Ver los detalles de un evento en el panel de **notificaciones**</span><span class="sxs-lookup"><span data-stu-id="c8b71-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c8b71-162">Mensajes Push</span><span class="sxs-lookup"><span data-stu-id="c8b71-162">Push Messages</span></span>  

<span data-ttu-id="c8b71-163">Para mostrar una notificación de inserción a un usuario, un **trabajador de servicio** primero debe usar la API de [mensajes Push][MDNPush] para recibir datos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="c8b71-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="c8b71-164">Cuando el trabajador del servicio está listo para mostrar la notificación, usa la [API de notificaciones][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="c8b71-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="c8b71-165">Para registrar mensajes de inserción por 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="c8b71-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c8b71-166">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c8b71-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c8b71-167">Abra la herramienta **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="c8b71-168">Abra el panel de **mensajes Push** .</span><span class="sxs-lookup"><span data-stu-id="c8b71-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Abrir el panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="c8b71-170">Abrir el panel de **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="c8b71-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-171">Elija **grabar** \ ( ![ grabar ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c8b71-171">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="c8b71-172">Después de desencadenar cierta actividad de mensajes Push, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Registro de eventos en el panel mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="c8b71-174">Registro de eventos en el panel **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="c8b71-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8b71-175">Haga clic en un evento para ver los detalles en el espacio situado debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8b71-175">Click an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Ver los detalles de un evento en el panel de mensajes Push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="c8b71-177">Ver los detalles de un evento en el panel de **mensajes Push**</span><span class="sxs-lookup"><span data-stu-id="c8b71-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c8b71-178">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c8b71-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Abrir herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificaciones | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API de inserción | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "proceso en segundo plano: Wikipedia"  

> [!NOTE]
> <span data-ttu-id="c8b71-183">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8b71-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c8b71-184">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c8b71-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c8b71-186">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8b71-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
