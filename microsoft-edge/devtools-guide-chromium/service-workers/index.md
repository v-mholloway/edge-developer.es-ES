---
description: Todo sobre las mejoras del trabajador de servicio y cómo usar cada una de ellas.
title: Mejoras del trabajador de servicio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, service worker, PWA
ms.openlocfilehash: c00b7c7fd18d4bb3d413369ec1464c0cb0255311
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597139"
---
# <a name="service-worker-improvements"></a><span data-ttu-id="e4e25-104">Mejoras del trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="e4e25-104">Service Worker improvements</span></span>  

<span data-ttu-id="e4e25-105">En este artículo se le enseña acerca [][MdnServiceWorkerApi] de las mejoras de las herramientas de desarrollo para trabajar con los trabajadores de servicio y las solicitudes de red que pasan por cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="e4e25-105">This article teaches you about improvements to developer tools for working with [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="e4e25-106">Las **mejoras del trabajador de servicio** se encuentran en las herramientas **Red,** **Aplicación** **y** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="e4e25-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="e4e25-107">Las mejoras simplifican las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="e4e25-107">The improvements simplify the following tasks.</span></span>  

*   <span data-ttu-id="e4e25-108">Depuración basada en las escalas de tiempo del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="e4e25-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="e4e25-109">El inicio de una solicitud y la duración del arranque.</span><span class="sxs-lookup"><span data-stu-id="e4e25-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="e4e25-110">Actualizar al registro del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="e4e25-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="e4e25-111">Tiempo de ejecución de una solicitud mediante el [controlador de eventos fetch.][MdnFetchEvent]</span><span class="sxs-lookup"><span data-stu-id="e4e25-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="e4e25-112">Tiempo de ejecución de todos los eventos de captura para cargar un cliente.</span><span class="sxs-lookup"><span data-stu-id="e4e25-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="e4e25-113">Explore los detalles en tiempo de ejecución de los controladores de eventos de captura, instale controladores de eventos y active controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="e4e25-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="e4e25-114">Paso a paso hacia dentro y fuera del controlador de eventos de captura con [información de script de página](#sources).</span><span class="sxs-lookup"><span data-stu-id="e4e25-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  
    
<span data-ttu-id="e4e25-115">Las experiencias abarcan tres herramientas de desarrollador diferentes.</span><span class="sxs-lookup"><span data-stu-id="e4e25-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="e4e25-116">La [herramienta Red.](#network)</span><span class="sxs-lookup"><span data-stu-id="e4e25-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="e4e25-117">Elija una solicitud de red que se ejecute a través de un trabajador de servicio y obtenga acceso a la escala de tiempo correspondiente del trabajador de servicio en la **herramienta Timing.**</span><span class="sxs-lookup"><span data-stu-id="e4e25-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="e4e25-118">La [herramienta Aplicación.](#application)</span><span class="sxs-lookup"><span data-stu-id="e4e25-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="e4e25-119">Para depurar los trabajadores del servicio, vaya a la **herramienta Trabajadores de** servicio.</span><span class="sxs-lookup"><span data-stu-id="e4e25-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="e4e25-120">La [herramienta Orígenes.](#sources)</span><span class="sxs-lookup"><span data-stu-id="e4e25-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="e4e25-121">Obtener acceso a la información de script de página al acceder a controladores de eventos de captura.</span><span class="sxs-lookup"><span data-stu-id="e4e25-121">Access page script information when stepping into fetch event handlers.</span></span>  
    
## <a name="network"></a><span data-ttu-id="e4e25-122">Red</span><span class="sxs-lookup"><span data-stu-id="e4e25-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Escala de tiempo de trabajo de servicio en la herramienta Red" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="e4e25-124">Vista de red</span><span class="sxs-lookup"><span data-stu-id="e4e25-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="e4e25-125">Para obtener acceso a las características de depuración de trabajadores de servicio en la **herramienta Red,** realice una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e4e25-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="e4e25-126">Accede directamente a la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="e4e25-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="e4e25-127">Se inició en **la herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="e4e25-127">Started in the **Application** tool.</span></span>  
    
### <a name="request-routing"></a><span data-ttu-id="e4e25-128">Enrutamiento de solicitudes</span><span class="sxs-lookup"><span data-stu-id="e4e25-128">Request routing</span></span>  

<span data-ttu-id="e4e25-129">Para facilitar la visualización del enrutamiento de solicitudes, las escalas de tiempo ahora muestran el inicio del trabajador de servicio y los eventos `respondWith` de captura.</span><span class="sxs-lookup"><span data-stu-id="e4e25-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="e4e25-130">Para depurar y visualizar una solicitud de red que pasó a través de un trabajador de servicio, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e4e25-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="e4e25-131">Elija la solicitud de red que ha pasado por un trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="e4e25-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="e4e25-132">Abra la **herramienta Temporización.**</span><span class="sxs-lookup"><span data-stu-id="e4e25-132">Open the **Timing** tool.</span></span>  
    
### <a name="fetch-events"></a><span data-ttu-id="e4e25-133">Eventos de captura</span><span class="sxs-lookup"><span data-stu-id="e4e25-133">Fetch events</span></span>  

<span data-ttu-id="e4e25-134">Para obtener más información sobre los eventos de captura, elija la flecha `respondWith` desplegable situada a la izquierda del archivo `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="e4e25-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="e4e25-135">Para obtener más información acerca de la solicitud **original** y **la respuesta recibida,** use las flechas desplegables correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e4e25-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <a name="application"></a><span data-ttu-id="e4e25-136">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4e25-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Vista Aplicación" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="e4e25-138">Vista Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4e25-138">Application view</span></span>  
:::image-end:::  

### <a name="service-worker-update-timeline"></a><span data-ttu-id="e4e25-139">Escala de tiempo de actualización del trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="e4e25-139">Service worker update timeline</span></span>  

<span data-ttu-id="e4e25-140">El Microsoft Edge DevTools agregó una escala de tiempo en la **herramienta Aplicación** para reflejar el ciclo de vida de actualización del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="e4e25-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="e4e25-141">Muestra los eventos de instalación y activación.</span><span class="sxs-lookup"><span data-stu-id="e4e25-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="e4e25-142">Cada uno de los eventos tiene una flecha desplegable correspondiente para darle más detalles.</span><span class="sxs-lookup"><span data-stu-id="e4e25-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <a name="request-routing-and-fetch-events"></a><span data-ttu-id="e4e25-143">Eventos de enrutamiento y captura de solicitudes</span><span class="sxs-lookup"><span data-stu-id="e4e25-143">Request routing and fetch events</span></span>  

<span data-ttu-id="e4e25-144">Ahora puede acceder a las escalas de tiempo del trabajador de servicio a través **de la herramienta Red** en el cajón de la consola.</span><span class="sxs-lookup"><span data-stu-id="e4e25-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="e4e25-145">La característica beneficia el rendimiento, minimiza la duplicación de la interfaz de usuario y crea una experiencia de depuración más completa.</span><span class="sxs-lookup"><span data-stu-id="e4e25-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="e4e25-146">Abra el trabajador de servicio que está depurando.</span><span class="sxs-lookup"><span data-stu-id="e4e25-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="e4e25-147">Elija el **botón Red** para abrir la experiencia de enrutamiento [de solicitudes.](#network)</span><span class="sxs-lookup"><span data-stu-id="e4e25-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="e4e25-148">Use los desplegables **respondWith** para obtener información sobre la solicitud de evento y la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4e25-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="e4e25-149">La **herramienta Red** muestra las solicitudes de red que pasaron por el trabajador de servicio que está depurando.</span><span class="sxs-lookup"><span data-stu-id="e4e25-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="e4e25-150">El filtro automático es una forma de restringir la exploración.</span><span class="sxs-lookup"><span data-stu-id="e4e25-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <a name="sources"></a><span data-ttu-id="e4e25-151">Orígenes</span><span class="sxs-lookup"><span data-stu-id="e4e25-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Árbol DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="e4e25-153">Árbol DOM</span><span class="sxs-lookup"><span data-stu-id="e4e25-153">DOM tree</span></span>  
:::image-end:::  

<span data-ttu-id="e4e25-154">Para encontrar más información sobre la pila, establezca un punto de interrupción en el controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="e4e25-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="e4e25-155">Los detalles llevan a dónde se solicita el recurso en el script de página.</span><span class="sxs-lookup"><span data-stu-id="e4e25-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="e4e25-156">Cuando el depurador se detiene dentro de un controlador de captura, se muestra una información de pila combinada en el panel a la derecha.</span><span class="sxs-lookup"><span data-stu-id="e4e25-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="e4e25-157">Después de eso, puede moverse en los marcos de la pila.</span><span class="sxs-lookup"><span data-stu-id="e4e25-157">After that, you may move around in the stack frames.</span></span>  

### <a name="future-work"></a><span data-ttu-id="e4e25-158">Trabajo futuro</span><span class="sxs-lookup"><span data-stu-id="e4e25-158">Future work</span></span>  

<span data-ttu-id="e4e25-159">El Microsoft Edge de DevTools planea desarrollar aún más los detalles de la memoria caché y están investigando más formas de mejorar la experiencia de depuración del trabajador del servicio para desarrolladores de [aplicaciones web][MdnProgressiveWebApps] progresivas.</span><span class="sxs-lookup"><span data-stu-id="e4e25-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e4e25-160">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e4e25-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicaciones web progresivas (PWA) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de trabajo de servicio | MDN"  
