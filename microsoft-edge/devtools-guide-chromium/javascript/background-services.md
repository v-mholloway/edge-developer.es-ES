---
description: Cómo depurar la captura en segundo plano, la sincronización en segundo plano, las notificaciones y los mensajes de inserción con Microsoft Edge DevTools.
title: Depurar servicios en segundo plano con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 15023098c547d31bf46bd387f849b365c13b38f6
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439531"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a><span data-ttu-id="92379-104">Depurar servicios en segundo plano con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92379-104">Debug Background Services with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="92379-105">La sección **Servicios** en segundo plano de Microsoft Edge DevTools es una colección de herramientas para las API de JavaScript que permite al sitio web enviar y recibir actualizaciones incluso cuando un usuario no tiene el sitio web abierto.</span><span class="sxs-lookup"><span data-stu-id="92379-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="92379-106">Un servicio en segundo plano es funcionalmente similar a un [proceso en segundo plano][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="92379-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="92379-107">Microsoft Edge DevTools considera que cada una de las siguientes API es un servicio en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="92379-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="92379-108">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="92379-109">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="92379-110">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="92379-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="92379-111">Mensajes de inserción</span><span class="sxs-lookup"><span data-stu-id="92379-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="92379-112">Microsoft Edge DevTools puede registrar eventos de servicio en segundo plano durante 3 días, incluso cuando DevTools no está abierto.</span><span class="sxs-lookup"><span data-stu-id="92379-112">Microsoft Edge DevTools may log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="92379-113">El registro de eventos de servicio en segundo plano puede ayudarle a asegurarse de que los eventos se envían y reciben según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="92379-113">The background service events log may help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="92379-114">También puede inspeccionar los detalles de cada evento.</span><span class="sxs-lookup"><span data-stu-id="92379-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="El panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="92379-116">El **panel Mensajería de inserción**</span><span class="sxs-lookup"><span data-stu-id="92379-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <a name="background-fetch"></a><span data-ttu-id="92379-117">Captura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-117">Background Fetch</span></span>  

<span data-ttu-id="92379-118">La **API de captura en** segundo plano permite a un trabajador de servicio descargar recursos grandes de forma confiable, como películas o podcasts, como un servicio en segundo plano. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="92379-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="92379-119">Para registrar el evento Background Fetch durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="92379-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="92379-120">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92379-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92379-121">Abra la **herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="92379-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92379-122">Abra el **panel Captura en** segundo plano.</span><span class="sxs-lookup"><span data-stu-id="92379-122">Open the **Background Fetch** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Panel Captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="92379-124">Panel **Captura en** segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-124">The **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-125">Elija **Record** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92379-125">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="92379-126">Después de desencadenar alguna actividad de captura en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Registro de eventos en el panel Captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="92379-128">Registro de eventos en el panel **Captura en** segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-128">A log of events in the **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-129">Elija un evento para ver sus detalles en el espacio debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-129">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Ver los detalles de un evento en el panel Captura en segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="92379-131">Ver los detalles de un evento en el panel **Captura en** segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <a name="background-sync"></a><span data-ttu-id="92379-132">Sincronización en segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-132">Background Sync</span></span>  

<span data-ttu-id="92379-133">La API de sincronización \*\*\*\* **en** segundo plano permite a un trabajador del servicio sin conexión enviar datos a un servidor una vez que haya vuelto a establecer una conexión a Internet confiable.</span><span class="sxs-lookup"><span data-stu-id="92379-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="92379-134">Para registrar eventos de sincronización en segundo plano durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="92379-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="92379-135">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92379-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92379-136">Abra la **herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="92379-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92379-137">Abra el **panel Sincronización en** segundo plano.</span><span class="sxs-lookup"><span data-stu-id="92379-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Panel Sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="92379-139">Panel **Sincronización en** segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-140">Elija **Record** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92379-140">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="92379-141">Después de desencadenar alguna actividad de sincronización en segundo plano, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Un registro de eventos en el panel Sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="92379-143">Un registro de eventos en el panel **Sincronización en** segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-144">Elija un evento para ver sus detalles en el espacio debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-144">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Ver los detalles de un evento en el panel Sincronización en segundo plano" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="92379-146">Ver los detalles de un evento en el panel **Sincronización en** segundo plano</span><span class="sxs-lookup"><span data-stu-id="92379-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <a name="notifications"></a><span data-ttu-id="92379-147">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="92379-147">Notifications</span></span>  

<span data-ttu-id="92379-148">Después de **que un trabajador de** servicio haya recibido un mensaje [de][MDNPush] inserción de un servidor, el trabajador del servicio usa la [API de][MDNNotifications] notificaciones para mostrar los datos a un usuario.</span><span class="sxs-lookup"><span data-stu-id="92379-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="92379-149">Para registrar notificaciones durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="92379-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="92379-150">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92379-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92379-151">Abra la **herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="92379-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92379-152">Abra el **panel Notificaciones.**</span><span class="sxs-lookup"><span data-stu-id="92379-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Panel Notificaciones" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="92379-154">Panel **Notificaciones**</span><span class="sxs-lookup"><span data-stu-id="92379-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-155">Elija **Record** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92379-155">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="92379-156">Después de desencadenar alguna actividad notifications, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Un registro de eventos en el panel Notificaciones" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="92379-158">Un registro de eventos en el **panel Notificaciones**</span><span class="sxs-lookup"><span data-stu-id="92379-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-159">Elija un evento para ver sus detalles en el espacio debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-159">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Ver los detalles de un evento en el panel Notificaciones" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="92379-161">Ver los detalles de un evento en el **panel Notificaciones**</span><span class="sxs-lookup"><span data-stu-id="92379-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <a name="push-messages"></a><span data-ttu-id="92379-162">Mensajes de inserción</span><span class="sxs-lookup"><span data-stu-id="92379-162">Push Messages</span></span>  

<span data-ttu-id="92379-163">Para mostrar una notificación de \*\*\*\* inserción a un usuario, un trabajador del servicio primero debe usar la [API][MDNPush] de mensajes de inserción para recibir datos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="92379-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="92379-164">Cuando el trabajador del servicio está listo para mostrar la notificación, usa la [API de notificaciones][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="92379-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="92379-165">Para registrar mensajes de inserción durante 3 días, incluso cuando DevTools no está abierto:</span><span class="sxs-lookup"><span data-stu-id="92379-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="92379-166">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92379-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92379-167">Abra la **herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="92379-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92379-168">Abra el **panel Mensajería de inserción.**</span><span class="sxs-lookup"><span data-stu-id="92379-168">Open the **Push Messaging** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Abrir el panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="92379-170">Abrir el **panel Mensajería de inserción**</span><span class="sxs-lookup"><span data-stu-id="92379-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-171">Elija **Record** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92379-171">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
    <span data-ttu-id="92379-172">Después de desencadenar alguna actividad de mensaje de inserción, DevTools registra los eventos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Registro de eventos en el panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="92379-174">Registro de eventos en el panel **Mensajería de** inserción</span><span class="sxs-lookup"><span data-stu-id="92379-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92379-175">Elija un evento para ver los detalles en el espacio debajo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="92379-175">Choose an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Ver los detalles de un evento en el panel Mensajería de inserción" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="92379-177">Ver los detalles de un evento en el **panel Mensajería de** inserción</span><span class="sxs-lookup"><span data-stu-id="92379-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="92379-178">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92379-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Abra Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notificaciones API | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Api de inserción | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Proceso en segundo plano - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="92379-183">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92379-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="92379-184">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="92379-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="92379-186">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92379-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
