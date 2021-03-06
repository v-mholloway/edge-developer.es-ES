---
description: En esta guía se proporciona información general sobre las características y estándares del desarrollador incluidos en EdgeHTML 16.
title: Nuevas características y API en EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, web development, html, css, javascript, developer
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399200"
---
# <a name="whats-new-in-edgehtml-16"></a><span data-ttu-id="93948-104">Novedades de EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="93948-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="93948-105">Esta es una lista de las características nuevas y actualizadas que se incluyen en la plataforma web [EdgeHTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) como parte de [windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, compilación 16299\).</span><span class="sxs-lookup"><span data-stu-id="93948-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="93948-106">Para ver los cambios en compilaciones específicas de Windows Insider Preview, consulta el Registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) y Novedades [de EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="93948-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="93948-107">Este es el vínculo permanente para la siguiente lista de cambios:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="93948-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <a name="new-and-updated-features"></a><span data-ttu-id="93948-108">Características nuevas y actualizadas</span><span class="sxs-lookup"><span data-stu-id="93948-108">New and updated features</span></span>  

### <a name="css-grid-layout"></a><span data-ttu-id="93948-109">Diseño de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="93948-109">CSS Grid Layout</span></span>  

<span data-ttu-id="93948-110">Microsoft Edge ahora admite la implementación sin prefijo del diseño [de cuadrícula CSS](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="93948-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="93948-111">[Diseño de](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) cuadrícula define un sistema de diseño basado en cuadrícula bidimensional que permite más fluidez de diseño que posible con el posicionamiento mediante floats o scripts.</span><span class="sxs-lookup"><span data-stu-id="93948-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="93948-112">En el ejemplo siguiente se usa el diseño de cuadrícula CSS para crear la estructura de una página web básica.</span><span class="sxs-lookup"><span data-stu-id="93948-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="93948-113">Diseño de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="93948-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="93948-114">Vea el diseño de <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> cuadrícula CSS del lápiz por </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) en </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="93948-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <a name="css-object-fit-and-object-position"></a><span data-ttu-id="93948-115">Ajuste de objeto CSS y posición de objeto</span><span class="sxs-lookup"><span data-stu-id="93948-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="93948-116">EdgeHTML 16 presenta compatibilidad con las propiedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) y [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="93948-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="93948-117">Estas propiedades controlan la posición y el tamaño del contenido reemplazado dentro del cuadro de contenido.</span><span class="sxs-lookup"><span data-stu-id="93948-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <a name="developer-tools"></a><span data-ttu-id="93948-118">Herramientas de desarrollo</span><span class="sxs-lookup"><span data-stu-id="93948-118">Developer Tools</span></span>  

<span data-ttu-id="93948-119">En esta versión, iniciamos un gran esfuerzo de refactorización de Microsoft Edge DevTools para mejorar la robustez y el rendimiento, y también agregamos un montón de nuevas características que puedes empezar a usar hoy en las compilaciones de [Windows Insider.](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="93948-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="93948-120">Echa un vistazo a [la guía de Microsoft Edge DevTools](../whats-new.md) para obtener más información sobre lo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="93948-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <a name="javascript"></a><span data-ttu-id="93948-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="93948-121">JavaScript</span></span>  

<span data-ttu-id="93948-122">[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) se basa en optimizaciones de rendimiento de Javascript de versiones anteriores al expandir la capacidad del motor Decácrate para aplazar o volver a aplazar funciones, usar cachés en línea polimórficas y optimizar funciones con `try` / `finally` bloques.</span><span class="sxs-lookup"><span data-stu-id="93948-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="93948-123">Además, las características vistas previamente en EdgeHTML 15 ahora son estables y están habilitadas de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="93948-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <a name="new-features"></a><span data-ttu-id="93948-124">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="93948-124">New features</span></span>  

<span data-ttu-id="93948-125">Activado de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="93948-125">On by default</span></span>  

*   <span data-ttu-id="93948-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="93948-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="93948-127">Memoria compartida y atómicos</span><span class="sxs-lookup"><span data-stu-id="93948-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a><span data-ttu-id="93948-128">API de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="93948-128">Payment Request API</span></span>  

<span data-ttu-id="93948-129">La [API de](../windows-integration/payment-request-api.md) solicitud de pago es un estándar abierto entre exploradores que permite a los exploradores actuar como intermediarios entre comerciantes, consumidores y métodos de pago \(como tarjetas de crédito\) que los consumidores han almacenado en la nube.</span><span class="sxs-lookup"><span data-stu-id="93948-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="93948-130">La API de EdgeHTML 16 se ha actualizado para que coincida con la última especificación de la [API](https://w3c.github.io/payment-request) de solicitud de pago de W3C.</span><span class="sxs-lookup"><span data-stu-id="93948-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="93948-131">Esto incluye:</span><span class="sxs-lookup"><span data-stu-id="93948-131">This includes:</span></span>  

*   <span data-ttu-id="93948-132">Compatibilidad con el `canMakePayment()` método</span><span class="sxs-lookup"><span data-stu-id="93948-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="93948-133">Compatibilidad con la `requestId` propiedad</span><span class="sxs-lookup"><span data-stu-id="93948-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="93948-134">Compatibilidad con la `id` propiedad</span><span class="sxs-lookup"><span data-stu-id="93948-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="93948-135">El valor predeterminado del `complete()` parámetro del método `result` cambió de " " a "unknown"</span><span class="sxs-lookup"><span data-stu-id="93948-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <a name="service-workers"></a><span data-ttu-id="93948-136">Trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="93948-136">Service Workers</span></span>  

<span data-ttu-id="93948-137">[Los trabajadores](https://www.w3.org/TR/service-workers-1) de servicio son scripts controlados por eventos que se ejecutan en segundo plano de una página web.</span><span class="sxs-lookup"><span data-stu-id="93948-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="93948-138">Los trabajadores del servicio solo habilitan la funcionalidad que anteriormente solo está disponible con aplicaciones nativas, como interceptar y controlar solicitudes de la red, administrar y administrar la sincronización en segundo plano, el almacenamiento local y las notificaciones push.</span><span class="sxs-lookup"><span data-stu-id="93948-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="93948-139">La compatibilidad con el trabajador de servicio aún está en desarrollo, pero puede probar su PWA en Microsoft Edge con nuestro soporte técnico experimental del trabajador de servicio habilitando la característica de trabajador de servicio en `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="93948-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <a name="webvr"></a><span data-ttu-id="93948-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="93948-140">WebVR</span></span>  

<span data-ttu-id="93948-141">WebVR para Microsoft Edge ha agregado compatibilidad con controladores [de movimiento.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)</span><span class="sxs-lookup"><span data-stu-id="93948-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="93948-142">Estos controladores tienen una posición precisa en el espacio, lo que permite una interacción detallada con objetos digitales en la realidad virtual.</span><span class="sxs-lookup"><span data-stu-id="93948-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de movimiento" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="93948-144">Controladores de movimiento</span><span class="sxs-lookup"><span data-stu-id="93948-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="93948-145">WebVR también se ha optimizado para admitir dos tipos diferentes de experiencias.</span><span class="sxs-lookup"><span data-stu-id="93948-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="93948-146">**Equipos con Windows Mixed Reality:** equipos de escritorio y portátiles con gráficos integrados.</span><span class="sxs-lookup"><span data-stu-id="93948-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="93948-147">Cuando se conecta a estos dispositivos, nuestros auriculares envolventes se ejecutarán a 60 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="93948-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="93948-148">**Equipos Windows Mixed Reality Ultra:** equipos de escritorio y portátiles con gráficos discretos.</span><span class="sxs-lookup"><span data-stu-id="93948-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="93948-149">Cuando se conecta a estos dispositivos, nuestros auriculares envolventes se ejecutarán a 90 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="93948-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="93948-150">Ambas configuraciones admitirán las mismas experiencias envolventes de vídeo y juegos.</span><span class="sxs-lookup"><span data-stu-id="93948-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="93948-151">Para obtener más información acerca de las próximas actualizaciones de Windows Mixed Reality, consulta la entrada de blog de actualización de días festivos de [Windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)</span><span class="sxs-lookup"><span data-stu-id="93948-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="93948-152">Para obtener guías y demostraciones, dirígete a [la Guía para desarrolladores de WebVR.](/microsoft-edge/webvr)</span><span class="sxs-lookup"><span data-stu-id="93948-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="93948-153">Dado que la especificación webVR todavía está en desarrollo, la implementación de Microsoft Edge puede cambiar más adelante hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="93948-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <a name="new-apis-in-edgehtml-16"></a><span data-ttu-id="93948-154">Nuevas API en EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="93948-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="93948-155">Esta es la lista completa de nuevas API en EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="93948-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="93948-156">Se enumeran con el formato `[interface name].[api name]` de .</span><span class="sxs-lookup"><span data-stu-id="93948-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="93948-157">Aunque las siguientes API se exponen en el DOM, el comportamiento de extremo a extremo de algunas puede estar todavía en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="93948-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="93948-158">Consulte Estado de [la plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para obtener información oficial sobre la compatibilidad con características.</span><span class="sxs-lookup"><span data-stu-id="93948-158">Refer to [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="93948-159">Nuevas API en EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="93948-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="93948-160">Vea las API nuevas del lápiz <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> en EdgeHTML 16 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) en </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="93948-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <a name="previous-edgehtml-releases"></a><span data-ttu-id="93948-161">Versiones anteriores de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="93948-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="93948-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="93948-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="93948-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="93948-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="93948-164">EdgeHTML 14 / Compilación de Windows 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="93948-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="93948-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="93948-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
