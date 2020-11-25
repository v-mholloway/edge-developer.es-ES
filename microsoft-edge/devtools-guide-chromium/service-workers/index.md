---
description: Todo sobre las mejoras de los trabajadores de servicios y cómo usar cada una de ellas.
title: Mejoras de los trabajos de servicio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, trabajo de servicios, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190049"
---
# <span data-ttu-id="b314a-104">Mejoras de los trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="b314a-104">Service Worker improvements</span></span>  

<span data-ttu-id="b314a-105">Este artículo le enseña acerca de las mejoras en los [trabajadores de servicios][MdnServiceWorkerApi] y las solicitudes de red que pasan por cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="b314a-105">This article teaches you about improvements to [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="b314a-106">Las **mejoras** de los trabajos de servicio se encuentran en las herramientas **red**, **aplicaciones**y **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="b314a-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="b314a-107">Las mejoras incluyen las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="b314a-107">The improvements include the following tasks.</span></span>  

*   <span data-ttu-id="b314a-108">Depurar en función de escalas de tiempo de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="b314a-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="b314a-109">El inicio de una solicitud y la duración del bootstrap.</span><span class="sxs-lookup"><span data-stu-id="b314a-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="b314a-110">Actualice el registro de trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="b314a-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="b314a-111">El motor en tiempo de ejecución de una solicitud mediante el controlador de [eventos fetch][MdnFetchEvent] .</span><span class="sxs-lookup"><span data-stu-id="b314a-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="b314a-112">El motor en tiempo de ejecución de todos los eventos fetch para cargar un cliente.</span><span class="sxs-lookup"><span data-stu-id="b314a-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="b314a-113">Explore los detalles de tiempo de ejecución de los controladores de eventos de Fetch, instale controladores de eventos y Active controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="b314a-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="b314a-114">Ir hacia dentro y fuera del controlador de eventos de Fetch con [información de script de página](#sources).</span><span class="sxs-lookup"><span data-stu-id="b314a-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  

<span data-ttu-id="b314a-115">Las experiencias abarcan tres herramientas de desarrollador diferentes.</span><span class="sxs-lookup"><span data-stu-id="b314a-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="b314a-116">La herramienta [red](#network) .</span><span class="sxs-lookup"><span data-stu-id="b314a-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="b314a-117">Elija una solicitud de red que se ejecute a través de un trabajador de servicio y obtenga acceso a la escala de tiempo correspondiente del trabajo de servicio en la herramienta **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="b314a-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="b314a-118">La herramienta de [aplicación](#application) .</span><span class="sxs-lookup"><span data-stu-id="b314a-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="b314a-119">Para depurar los trabajos de servicio, vaya a la herramienta de **trabajos de servicio** .</span><span class="sxs-lookup"><span data-stu-id="b314a-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="b314a-120">La herramienta [orígenes](#sources) .</span><span class="sxs-lookup"><span data-stu-id="b314a-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="b314a-121">Obtenga acceso a la información de script de página al entrar en los controladores de eventos de Fetch.</span><span class="sxs-lookup"><span data-stu-id="b314a-121">Access page script information when stepping into fetch event handlers.</span></span>  

## <span data-ttu-id="b314a-122">Red</span><span class="sxs-lookup"><span data-stu-id="b314a-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Escala de tiempo de trabajo del servicio en la herramienta red" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="b314a-124">Vista de red</span><span class="sxs-lookup"><span data-stu-id="b314a-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="b314a-125">Para obtener acceso a las características de depuración de trabajos de servicio de la herramienta **red** , complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b314a-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="b314a-126">Acceso directo en la herramienta **red** .</span><span class="sxs-lookup"><span data-stu-id="b314a-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="b314a-127">Se inició en la herramienta de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="b314a-127">Started in the **Application** tool.</span></span>  
    
### <span data-ttu-id="b314a-128">Enrutamiento de solicitudes</span><span class="sxs-lookup"><span data-stu-id="b314a-128">Request routing</span></span>  

<span data-ttu-id="b314a-129">Para facilitar la visualización del enrutamiento de solicitudes, las escalas de tiempo ahora muestran los eventos inicio de trabajo de servicio y `respondWith` captura.</span><span class="sxs-lookup"><span data-stu-id="b314a-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="b314a-130">Para depurar y visualizar una solicitud de red que pasó a través de un trabajo de servicio, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b314a-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="b314a-131">Elija la solicitud de red que pasó a un trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="b314a-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="b314a-132">Abrir la herramienta **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="b314a-132">Open the **Timing** tool.</span></span>  
    
### <span data-ttu-id="b314a-133">Eventos fetch</span><span class="sxs-lookup"><span data-stu-id="b314a-133">Fetch events</span></span>  

<span data-ttu-id="b314a-134">Para obtener más información sobre los `respondWith` eventos de captura, elija la flecha de lista desplegable a la izquierda de la `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="b314a-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="b314a-135">Para obtener más información sobre la **solicitud original** y la **respuesta recibida**, use las flechas desplegables correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b314a-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <span data-ttu-id="b314a-136">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b314a-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Vista de aplicación" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="b314a-138">Vista de aplicación</span><span class="sxs-lookup"><span data-stu-id="b314a-138">Application view</span></span>  
:::image-end:::  

### <span data-ttu-id="b314a-139">Escala de tiempo de actualización de trabajo del servicio</span><span class="sxs-lookup"><span data-stu-id="b314a-139">Service worker update timeline</span></span>  

<span data-ttu-id="b314a-140">El equipo de DevTools Microsoft Edge agregó una escala de tiempo en la herramienta de **aplicaciones** para reflejar el ciclo de vida de actualización del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="b314a-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="b314a-141">Muestra los eventos de instalación y activación.</span><span class="sxs-lookup"><span data-stu-id="b314a-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="b314a-142">Cada uno de los eventos tiene una flecha desplegable correspondiente para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b314a-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <span data-ttu-id="b314a-143">Solicitar eventos de enrutamiento y búsqueda</span><span class="sxs-lookup"><span data-stu-id="b314a-143">Request routing and fetch events</span></span>  

<span data-ttu-id="b314a-144">Ahora puede acceder a las escalas de tiempo de los trabajos de servicio a través de la herramienta de **red** en el cajón de la consola.</span><span class="sxs-lookup"><span data-stu-id="b314a-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="b314a-145">La característica beneficia el rendimiento, minimiza la duplicación de la interfaz de usuario y crea una experiencia de depuración más completa.</span><span class="sxs-lookup"><span data-stu-id="b314a-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="b314a-146">Abra el trabajador de servicio que está depurando.</span><span class="sxs-lookup"><span data-stu-id="b314a-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="b314a-147">Haga clic en el botón **red** para abrir la [experiencia de enrutamiento](#network)de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b314a-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="b314a-148">Use los menús desplegables **respondWith** para obtener información de solicitud y respuesta de evento.</span><span class="sxs-lookup"><span data-stu-id="b314a-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="b314a-149">La herramienta **red** muestra las solicitudes de red que pasaron por el trabajo de servicio que está depurando.</span><span class="sxs-lookup"><span data-stu-id="b314a-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="b314a-150">El filtro automático es una forma de restringir la exploración.</span><span class="sxs-lookup"><span data-stu-id="b314a-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <span data-ttu-id="b314a-151">Orígenes</span><span class="sxs-lookup"><span data-stu-id="b314a-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Vista DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="b314a-153">Vista DOM</span><span class="sxs-lookup"><span data-stu-id="b314a-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="b314a-154">Para obtener más información sobre la pila, establezca un punto de interrupción en el controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="b314a-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="b314a-155">Los detalles conducen a la ubicación del recurso en la secuencia de comandos de la página.</span><span class="sxs-lookup"><span data-stu-id="b314a-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="b314a-156">Cuando el depurador se detiene en un controlador de captura, se muestra la información de la pila combinada en el panel de la derecha.</span><span class="sxs-lookup"><span data-stu-id="b314a-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="b314a-157">Después de eso, puede desplazarse por los marcos de pila.</span><span class="sxs-lookup"><span data-stu-id="b314a-157">After that, you may move around in the stack frames.</span></span>  

### <span data-ttu-id="b314a-158">Trabajo futuro</span><span class="sxs-lookup"><span data-stu-id="b314a-158">Future work</span></span>  

<span data-ttu-id="b314a-159">El equipo de Microsoft Edge DevTools planea seguir desarrollando el detalle de la caché y está investigando más formas de mejorar la experiencia de depuración de los trabajos de servicio para los programadores de [aplicaciones web progresivas][MdnProgressiveWebApps] .</span><span class="sxs-lookup"><span data-stu-id="b314a-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <span data-ttu-id="b314a-160">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b314a-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicaciones web progresivas (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  
