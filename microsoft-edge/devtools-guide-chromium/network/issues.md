---
description: Obtenga información sobre cómo detectar problemas de red en el panel Red de Microsoft Edge DevTools.
title: Guía de problemas de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 9b92ca7b759fab80d7d829b31f605ccb8062a816
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439622"
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

# <a name="network-issues-guide"></a><span data-ttu-id="acf68-104">Guía de problemas de red</span><span class="sxs-lookup"><span data-stu-id="acf68-104">Network issues guide</span></span>  

<span data-ttu-id="acf68-105">En esta guía se muestra cómo detectar problemas de red o oportunidades de optimización en el panel Red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="acf68-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="acf68-106">Para obtener información sobre los conceptos básicos de la **herramienta Red,** vaya a [Introducción.][NetworkPerformance]</span><span class="sxs-lookup"><span data-stu-id="acf68-106">To learn the basics of the **Network** tool, navigate to [Get Started][NetworkPerformance].</span></span>  

## <a name="queued-or-stalled-requests"></a><span data-ttu-id="acf68-107">Solicitudes en cola o en espera</span><span class="sxs-lookup"><span data-stu-id="acf68-107">Queued or stalled requests</span></span>  

**<span data-ttu-id="acf68-108">Síntomas</span><span class="sxs-lookup"><span data-stu-id="acf68-108">Symptoms</span></span>**  

<span data-ttu-id="acf68-109">Seis solicitudes se descargan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="acf68-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="acf68-110">Después de eso, una serie de solicitudes se ponen en cola o se detienen.</span><span class="sxs-lookup"><span data-stu-id="acf68-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="acf68-111">Una vez que finaliza una de las seis primeras solicitudes, se inicia una de las solicitudes de la cola.</span><span class="sxs-lookup"><span data-stu-id="acf68-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="acf68-112">En la **cascada de** la siguiente figura, las seis primeras solicitudes del activo se `edge-iconx1024.msft.png` inician simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="acf68-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="acf68-113">Las solicitudes posteriores se detienen hasta que uno de los seis finales originales.</span><span class="sxs-lookup"><span data-stu-id="acf68-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Un ejemplo de una serie en cola o en espera en el panel Red" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="acf68-115">Un ejemplo de una serie en cola o en espera en la **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="acf68-115">An example of a queued or stalled series in the **Network** tool</span></span>  
:::image-end:::  

**<span data-ttu-id="acf68-116">Causas</span><span class="sxs-lookup"><span data-stu-id="acf68-116">Causes</span></span>**  

<span data-ttu-id="acf68-117">Se están haciendo demasiadas solicitudes en un solo dominio.</span><span class="sxs-lookup"><span data-stu-id="acf68-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="acf68-118">En las conexiones HTTP/1.0 o HTTP/1.1, Microsoft Edge permite un máximo de seis conexiones TCP simultáneas por host.</span><span class="sxs-lookup"><span data-stu-id="acf68-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="acf68-119">Correcciones</span><span class="sxs-lookup"><span data-stu-id="acf68-119">Fixes</span></span>**  

*   <span data-ttu-id="acf68-120">Implemente el particionamiento de dominios si debe usar HTTP/1.0 o HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="acf68-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="acf68-121">Use HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="acf68-121">Use HTTP/2.</span></span>  <span data-ttu-id="acf68-122">No use el particionamiento de dominios con HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="acf68-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="acf68-123">Quite o aplaza las solicitudes innecesarias para que las solicitudes críticas se descarguen anteriormente.</span><span class="sxs-lookup"><span data-stu-id="acf68-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <a name="slow-time-to-first-byte-ttfb"></a><span data-ttu-id="acf68-124">Tiempo lento hasta el primer byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="acf68-124">Slow Time To First Byte (TTFB)</span></span>  

**<span data-ttu-id="acf68-125">Síntomas</span><span class="sxs-lookup"><span data-stu-id="acf68-125">Symptoms</span></span>**  

<span data-ttu-id="acf68-126">Una solicitud pasa mucho tiempo esperando a recibir el primer byte del servidor.</span><span class="sxs-lookup"><span data-stu-id="acf68-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="acf68-127">En la siguiente figura, la barra verde y larga de **la cascada** indica que la solicitud estaba esperando mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="acf68-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="acf68-128">Esto se simuló con un perfil para restringir la velocidad de red y agregar un retraso.</span><span class="sxs-lookup"><span data-stu-id="acf68-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Un ejemplo de una solicitud con un tiempo lento al primer byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="acf68-130">Un ejemplo de una solicitud con un tiempo lento al primer byte</span><span class="sxs-lookup"><span data-stu-id="acf68-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="acf68-131">Causas</span><span class="sxs-lookup"><span data-stu-id="acf68-131">Causes</span></span>**  

*   <span data-ttu-id="acf68-132">La conexión entre el cliente y el servidor es lenta.</span><span class="sxs-lookup"><span data-stu-id="acf68-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="acf68-133">El servidor es lento para responder.</span><span class="sxs-lookup"><span data-stu-id="acf68-133">The server is slow to respond.</span></span>  <span data-ttu-id="acf68-134">Hospedar el servidor localmente para determinar si la conexión o el servidor es lento.</span><span class="sxs-lookup"><span data-stu-id="acf68-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="acf68-135">Si sigue teniendo un tiempo lento al primer byte \(TTFB\) al obtener acceso a un servidor local, el servidor será lento.</span><span class="sxs-lookup"><span data-stu-id="acf68-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="acf68-136">Correcciones</span><span class="sxs-lookup"><span data-stu-id="acf68-136">Fixes</span></span>**  

*   <span data-ttu-id="acf68-137">Si la conexión es lenta, considere la posibilidad de hospedar el contenido en una red CDN o cambiar los proveedores de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="acf68-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="acf68-138">Si el servidor es lento, considere la posibilidad de optimizar las consultas de base de datos, implementar una memoria caché o modificar la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="acf68-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <a name="slow-content-download"></a><span data-ttu-id="acf68-139">Descarga lenta de contenido</span><span class="sxs-lookup"><span data-stu-id="acf68-139">Slow content download</span></span>  

**<span data-ttu-id="acf68-140">Síntomas</span><span class="sxs-lookup"><span data-stu-id="acf68-140">Symptoms</span></span>**  

<span data-ttu-id="acf68-141">Una solicitud tarda mucho tiempo en descargarse.</span><span class="sxs-lookup"><span data-stu-id="acf68-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="acf68-142">En la siguiente figura, la barra larga y azul de **la cascada** junto al png significa que tardó mucho tiempo en descargarse.</span><span class="sxs-lookup"><span data-stu-id="acf68-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Un ejemplo de una solicitud que tarda mucho tiempo en descargarse" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="acf68-144">Un ejemplo de una solicitud que tarda mucho tiempo en descargarse</span><span class="sxs-lookup"><span data-stu-id="acf68-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="acf68-145">Causas</span><span class="sxs-lookup"><span data-stu-id="acf68-145">Causes</span></span>**  

*   <span data-ttu-id="acf68-146">La conexión entre el cliente y el servidor es lenta.</span><span class="sxs-lookup"><span data-stu-id="acf68-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="acf68-147">Se está descargando gran cantidad de contenido.</span><span class="sxs-lookup"><span data-stu-id="acf68-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="acf68-148">Correcciones</span><span class="sxs-lookup"><span data-stu-id="acf68-148">Fixes</span></span>**  

*   <span data-ttu-id="acf68-149">Considere la posibilidad de hospedar el contenido en una red CDN o cambiar los proveedores de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="acf68-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="acf68-150">Envíe menos bytes optimizando las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="acf68-150">Send fewer bytes by optimizing your requests.</span></span>  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="acf68-151">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="acf68-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nuevo problema: MicrosoftDocs/edge-developer"  

> [!NOTE]
> <span data-ttu-id="acf68-154">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="acf68-154">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="acf68-155">La página original [](https://developers.google.com/web/tools/chrome-devtools/network/issues) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span><span class="sxs-lookup"><span data-stu-id="acf68-155">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="acf68-157">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="acf68-157">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
