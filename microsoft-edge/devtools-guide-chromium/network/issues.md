---
description: Obtenga información sobre cómo detectar problemas de red en el panel de red de Microsoft Edge DevTools.
title: Guía de problemas de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4713dc252d428abbf5b60ee5f74a7316a102dab6
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125380"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="7dd24-104">Guía de problemas de red</span><span class="sxs-lookup"><span data-stu-id="7dd24-104">Network issues guide</span></span>  

<span data-ttu-id="7dd24-105">En esta guía se muestra cómo detectar problemas de red o oportunidades de optimización en el panel red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7dd24-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="7dd24-106">Consulte [Introducción][NetworkPerformance] a los conceptos básicos del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="7dd24-106">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="7dd24-107">Solicitudes en cola o detenidas</span><span class="sxs-lookup"><span data-stu-id="7dd24-107">Queued or stalled requests</span></span>  

**<span data-ttu-id="7dd24-108">Síntomas</span><span class="sxs-lookup"><span data-stu-id="7dd24-108">Symptoms</span></span>**  

<span data-ttu-id="7dd24-109">Se están descargando seis solicitudes al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7dd24-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="7dd24-110">Después de eso, una serie de solicitudes se ponen en cola o se detienen.</span><span class="sxs-lookup"><span data-stu-id="7dd24-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="7dd24-111">Una vez finalizada una de las primeras seis solicitudes, se inicia una de las solicitudes de la cola.</span><span class="sxs-lookup"><span data-stu-id="7dd24-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="7dd24-112">En la **cascada** de la siguiente ilustración, las seis primeras solicitudes del `edge-iconx1024.msft.png` activo se inician simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="7dd24-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="7dd24-113">Las siguientes solicitudes se detienen hasta que se haya completado una de seis originales.</span><span class="sxs-lookup"><span data-stu-id="7dd24-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="7dd24-115">Ejemplo de una serie en cola o detenida en el panel **red**</span><span class="sxs-lookup"><span data-stu-id="7dd24-115">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="7dd24-116">Causas</span><span class="sxs-lookup"><span data-stu-id="7dd24-116">Causes</span></span>**  

<span data-ttu-id="7dd24-117">Se están realizando demasiadas solicitudes en un solo dominio.</span><span class="sxs-lookup"><span data-stu-id="7dd24-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="7dd24-118">En las conexiones HTTP/1.0 o HTTP/1.1, Microsoft Edge permite un máximo de seis conexiones TCP simultáneas por host.</span><span class="sxs-lookup"><span data-stu-id="7dd24-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="7dd24-119">Arreglos</span><span class="sxs-lookup"><span data-stu-id="7dd24-119">Fixes</span></span>**  

*   <span data-ttu-id="7dd24-120">Implemente la particionamiento del dominio si necesita usar HTTP/1.0 o HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="7dd24-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="7dd24-121">Use HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="7dd24-121">Use HTTP/2.</span></span>  <span data-ttu-id="7dd24-122">No use el particionamiento del dominio con HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="7dd24-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="7dd24-123">Quite o aplaza las solicitudes innecesarias para que las solicitudes críticas se descarguen anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7dd24-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="7dd24-124">Tiempo lento para el primer byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="7dd24-124">Slow Time To First Byte (TTFB)</span></span>  

**<span data-ttu-id="7dd24-125">Síntomas</span><span class="sxs-lookup"><span data-stu-id="7dd24-125">Symptoms</span></span>**  

<span data-ttu-id="7dd24-126">Una solicitud dedica mucho tiempo a esperar a recibir el primer byte del servidor.</span><span class="sxs-lookup"><span data-stu-id="7dd24-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="7dd24-127">En la siguiente ilustración, la larga barra verde en la **cascada** indica que la solicitud estaba esperando mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="7dd24-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="7dd24-128">Esto se ha simulado usando un perfil para restringir la velocidad de la red y agregar un retraso.</span><span class="sxs-lookup"><span data-stu-id="7dd24-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="7dd24-130">Ejemplo de una solicitud con un tiempo lento para el primer byte</span><span class="sxs-lookup"><span data-stu-id="7dd24-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="7dd24-131">Causas</span><span class="sxs-lookup"><span data-stu-id="7dd24-131">Causes</span></span>**  

*   <span data-ttu-id="7dd24-132">La conexión entre el cliente y el servidor es lenta.</span><span class="sxs-lookup"><span data-stu-id="7dd24-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="7dd24-133">El servidor tarda en responder.</span><span class="sxs-lookup"><span data-stu-id="7dd24-133">The server is slow to respond.</span></span>  <span data-ttu-id="7dd24-134">Aloje el servidor de forma local para determinar si es la conexión o el servidor que es lento.</span><span class="sxs-lookup"><span data-stu-id="7dd24-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="7dd24-135">Si sigue demorando el primer byte \ (TTFB \) durante el acceso a un servidor local, entonces el servidor es lento.</span><span class="sxs-lookup"><span data-stu-id="7dd24-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="7dd24-136">Arreglos</span><span class="sxs-lookup"><span data-stu-id="7dd24-136">Fixes</span></span>**  

*   <span data-ttu-id="7dd24-137">Si la conexión es lenta, considere la posibilidad de hospedar el contenido en una red CDN o de cambiar los proveedores de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7dd24-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="7dd24-138">Si el servidor es lento, considere la posibilidad de optimizar las consultas de la base de datos, implementar una caché o modificar la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="7dd24-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="7dd24-139">Descarga de contenido lento</span><span class="sxs-lookup"><span data-stu-id="7dd24-139">Slow content download</span></span>  

**<span data-ttu-id="7dd24-140">Síntomas</span><span class="sxs-lookup"><span data-stu-id="7dd24-140">Symptoms</span></span>**  

<span data-ttu-id="7dd24-141">Una solicitud tarda mucho tiempo en descargarse.</span><span class="sxs-lookup"><span data-stu-id="7dd24-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="7dd24-142">En la siguiente ilustración, la larga barra azul en la **cascada** que se encuentra junto al formato PNG significa que se ha tardado mucho tiempo en descargarlo.</span><span class="sxs-lookup"><span data-stu-id="7dd24-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="7dd24-144">Ejemplo de una solicitud que tarda mucho tiempo en descargarse</span><span class="sxs-lookup"><span data-stu-id="7dd24-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="7dd24-145">Causas</span><span class="sxs-lookup"><span data-stu-id="7dd24-145">Causes</span></span>**  

*   <span data-ttu-id="7dd24-146">La conexión entre el cliente y el servidor es lenta.</span><span class="sxs-lookup"><span data-stu-id="7dd24-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="7dd24-147">Se está descargando una gran cantidad de contenido.</span><span class="sxs-lookup"><span data-stu-id="7dd24-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="7dd24-148">Arreglos</span><span class="sxs-lookup"><span data-stu-id="7dd24-148">Fixes</span></span>**  

*   <span data-ttu-id="7dd24-149">Considere la posibilidad de hospedar el contenido en una red CDN o de cambiar proveedores de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7dd24-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="7dd24-150">Reenvíes menos bytes optimizando las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="7dd24-150">Send fewer bytes by optimizing your requests.</span></span>  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <span data-ttu-id="7dd24-151">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7dd24-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspeccionar la actividad de la red en Microsoft Edge DevTools | Microsoft docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nuevo problema: MicrosoftDocs/Edge-Developer"  

> [!NOTE]
> <span data-ttu-id="7dd24-154">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7dd24-154">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7dd24-155">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/issues) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Jonathan confuso][JonathanGarbee] \ (Google Developer Expert para tecnología web \).</span><span class="sxs-lookup"><span data-stu-id="7dd24-155">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7dd24-157">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7dd24-157">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
