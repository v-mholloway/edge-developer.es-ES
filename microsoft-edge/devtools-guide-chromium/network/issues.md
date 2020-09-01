---
title: Guía de problemas de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a9a3234f3516bef16328102858363ffcb06251ec
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985399"
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





# <span data-ttu-id="235af-103">Guía de problemas de red</span><span class="sxs-lookup"><span data-stu-id="235af-103">Network issues guide</span></span>   




<span data-ttu-id="235af-104">En esta guía se muestra cómo detectar problemas de red o oportunidades de optimización en el panel red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="235af-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="235af-105">Consulte [Introducción][NetworkPerformance] a los conceptos básicos del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="235af-105">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="235af-106">Solicitudes en cola o detenidas</span><span class="sxs-lookup"><span data-stu-id="235af-106">Queued or stalled requests</span></span>   

**<span data-ttu-id="235af-107">Síntomas</span><span class="sxs-lookup"><span data-stu-id="235af-107">Symptoms</span></span>**  

<span data-ttu-id="235af-108">Se están descargando seis solicitudes al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="235af-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="235af-109">Después de eso, una serie de solicitudes se ponen en cola o se detienen.</span><span class="sxs-lookup"><span data-stu-id="235af-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="235af-110">Una vez finalizada una de las primeras seis solicitudes, se inicia una de las solicitudes de la cola.</span><span class="sxs-lookup"><span data-stu-id="235af-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="235af-111">En la **cascada** de la siguiente ilustración, las seis primeras solicitudes del `edge-iconx1024.msft.png` activo se inician simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="235af-111">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="235af-112">Las siguientes solicitudes se detienen hasta que se haya completado una de seis originales.</span><span class="sxs-lookup"><span data-stu-id="235af-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Ejemplo de una serie en cola o detenida en el panel red" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="235af-114">Ejemplo de una serie en cola o detenida en el panel **red**</span><span class="sxs-lookup"><span data-stu-id="235af-114">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="235af-115">Causas</span><span class="sxs-lookup"><span data-stu-id="235af-115">Causes</span></span>**  

<span data-ttu-id="235af-116">Se están realizando demasiadas solicitudes en un solo dominio.</span><span class="sxs-lookup"><span data-stu-id="235af-116">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="235af-117">En las conexiones HTTP/1.0 o HTTP/1.1, Microsoft Edge permite un máximo de seis conexiones TCP simultáneas por host.</span><span class="sxs-lookup"><span data-stu-id="235af-117">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="235af-118">Arreglos</span><span class="sxs-lookup"><span data-stu-id="235af-118">Fixes</span></span>**  

*   <span data-ttu-id="235af-119">Implemente la particionamiento del dominio si necesita usar HTTP/1.0 o HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="235af-119">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="235af-120">Use HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="235af-120">Use HTTP/2.</span></span>  <span data-ttu-id="235af-121">No use el particionamiento del dominio con HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="235af-121">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="235af-122">Quite o aplaza las solicitudes innecesarias para que las solicitudes críticas se descarguen anteriormente.</span><span class="sxs-lookup"><span data-stu-id="235af-122">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="235af-123">Tiempo lento para el primer byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="235af-123">Slow Time To First Byte (TTFB)</span></span>   

**<span data-ttu-id="235af-124">Síntomas</span><span class="sxs-lookup"><span data-stu-id="235af-124">Symptoms</span></span>**  

<span data-ttu-id="235af-125">Una solicitud dedica mucho tiempo a esperar a recibir el primer byte del servidor.</span><span class="sxs-lookup"><span data-stu-id="235af-125">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="235af-126">En la siguiente ilustración, la larga barra verde en la **cascada** indica que la solicitud estaba esperando mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="235af-126">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="235af-127">Esto se ha simulado usando un perfil para restringir la velocidad de la red y agregar un retraso.</span><span class="sxs-lookup"><span data-stu-id="235af-127">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Ejemplo de una solicitud con un tiempo lento para el primer byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="235af-129">Ejemplo de una solicitud con un tiempo lento para el primer byte</span><span class="sxs-lookup"><span data-stu-id="235af-129">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="235af-130">Causas</span><span class="sxs-lookup"><span data-stu-id="235af-130">Causes</span></span>**  

*   <span data-ttu-id="235af-131">La conexión entre el cliente y el servidor es lenta.</span><span class="sxs-lookup"><span data-stu-id="235af-131">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="235af-132">El servidor tarda en responder.</span><span class="sxs-lookup"><span data-stu-id="235af-132">The server is slow to respond.</span></span>  <span data-ttu-id="235af-133">Aloje el servidor de forma local para determinar si es la conexión o el servidor que es lento.</span><span class="sxs-lookup"><span data-stu-id="235af-133">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="235af-134">Si sigue demorando el primer byte \ (TTFB \) durante el acceso a un servidor local, entonces el servidor es lento.</span><span class="sxs-lookup"><span data-stu-id="235af-134">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="235af-135">Arreglos</span><span class="sxs-lookup"><span data-stu-id="235af-135">Fixes</span></span>**  

*   <span data-ttu-id="235af-136">Si la conexión es lenta, considere la posibilidad de hospedar el contenido en una red CDN o de cambiar los proveedores de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="235af-136">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="235af-137">Si el servidor es lento, considere la posibilidad de optimizar las consultas de la base de datos, implementar una caché o modificar la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="235af-137">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="235af-138">Descarga de contenido lento</span><span class="sxs-lookup"><span data-stu-id="235af-138">Slow content download</span></span>   

**<span data-ttu-id="235af-139">Síntomas</span><span class="sxs-lookup"><span data-stu-id="235af-139">Symptoms</span></span>**  

<span data-ttu-id="235af-140">Una solicitud tarda mucho tiempo en descargarse.</span><span class="sxs-lookup"><span data-stu-id="235af-140">A request takes a long time to download.</span></span>  

<span data-ttu-id="235af-141">En la siguiente ilustración, la larga barra azul en la **cascada** que se encuentra junto al formato PNG significa que se ha tardado mucho tiempo en descargarlo.</span><span class="sxs-lookup"><span data-stu-id="235af-141">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Ejemplo de una solicitud que tarda mucho tiempo en descargarse" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="235af-143">Ejemplo de una solicitud que tarda mucho tiempo en descargarse</span><span class="sxs-lookup"><span data-stu-id="235af-143">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="235af-144">Causas</span><span class="sxs-lookup"><span data-stu-id="235af-144">Causes</span></span>**  

*   <span data-ttu-id="235af-145">La conexión entre el cliente y el servidor es lenta.</span><span class="sxs-lookup"><span data-stu-id="235af-145">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="235af-146">Se está descargando una gran cantidad de contenido.</span><span class="sxs-lookup"><span data-stu-id="235af-146">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="235af-147">Arreglos</span><span class="sxs-lookup"><span data-stu-id="235af-147">Fixes</span></span>**  

*   <span data-ttu-id="235af-148">Considere la posibilidad de hospedar el contenido en una red CDN o de cambiar proveedores de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="235af-148">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="235af-149">Reenvíes menos bytes optimizando las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="235af-149">Send fewer bytes by optimizing your requests.</span></span>  
    
## <span data-ttu-id="235af-150">Conocimiento de colaboración</span><span class="sxs-lookup"><span data-stu-id="235af-150">Contribute knowledge</span></span>  

<span data-ttu-id="235af-151">¿Tiene un problema de red que debe agregarse a esta guía?</span><span class="sxs-lookup"><span data-stu-id="235af-151">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="235af-152">Envía un Tweet a [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="235af-152">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="235af-153">Seleccione **Enviar comentarios** \ ( ![ Enviar comentarios ][ImageSendFeedbackIcon] \) en la DevTools o pulse `Alt` + `Shift` + `I` \ (Windows \) o `Option` + `Shift` + `I` \ (MacOS \) para proporcionar respuestas o solicitudes de características.</span><span class="sxs-lookup"><span data-stu-id="235af-153">Select **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="235af-154">[Abra un problema][WebFundamentalsIssue] en el repositorio de docs.</span><span class="sxs-lookup"><span data-stu-id="235af-154">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspeccionar la actividad de la red en Microsoft Edge DevTools | Microsoft docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nuevo problema: MicrosoftDocs/Edge-Developer"  

> [!NOTE]
> <span data-ttu-id="235af-157">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="235af-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="235af-158">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/issues) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Jonathan confuso][JonathanGarbee] \ (Google Developer Expert para tecnología web \).</span><span class="sxs-lookup"><span data-stu-id="235af-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="235af-160">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="235af-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
