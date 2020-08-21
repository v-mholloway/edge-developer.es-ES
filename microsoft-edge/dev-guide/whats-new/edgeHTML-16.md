---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Esta guía proporciona una descripción general de las características y los estándares del desarrollador que se incluyen en Microsoft Edge.
title: Nuevas características y API de EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: a15888bc8c1314d61d436759e5d63be942174ea4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941933"
---
# <span data-ttu-id="88f1b-104">Novedades de EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="88f1b-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="88f1b-105">A continuación se ofrece una lista de las características nuevas y actualizadas que se incluyen en la plataforma Web [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) , como parte de [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \ (10/2017, compilación 16299 \).</span><span class="sxs-lookup"><span data-stu-id="88f1b-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="88f1b-106">Para obtener información sobre los cambios en las compilaciones específicas de Windows Insider Preview, vea el registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) y las novedades [de EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="88f1b-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="88f1b-107">Este es el vínculo permanente de la siguiente lista de cambios:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="88f1b-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="88f1b-108">Características nuevas y actualizadas</span><span class="sxs-lookup"><span data-stu-id="88f1b-108">New and updated features</span></span>  

### <span data-ttu-id="88f1b-109">Diseño de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="88f1b-109">CSS Grid Layout</span></span>  

<span data-ttu-id="88f1b-110">Microsoft Edge ahora es compatible con la implementación prefija de [diseño de cuadrícula CSS](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="88f1b-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="88f1b-111">[Diseño de cuadrícula](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define un sistema de diseño basado en cuadrícula bidimensional que permite más fluidez de diseño que el que se puede realizar con el posicionamiento mediante flotadores o secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="88f1b-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="88f1b-112">En el siguiente ejemplo se usa el diseño de cuadrícula CSS para crear la estructura de una página web básica.</span><span class="sxs-lookup"><span data-stu-id="88f1b-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="88f1b-113">Diseño de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="88f1b-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="88f1b-114">Consulta el <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> diseño de cuadrícula CSS de lápiz </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="88f1b-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="88f1b-115">Ajuste de objetos CSS y posición de objeto</span><span class="sxs-lookup"><span data-stu-id="88f1b-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="88f1b-116">EdgeHTML 16 introduce compatibilidad con propiedades de CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) y [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="88f1b-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="88f1b-117">Estas propiedades controlan la posición y el tamaño del contenido reemplazado en el cuadro de contenido.</span><span class="sxs-lookup"><span data-stu-id="88f1b-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="88f1b-118">Herramientas de desarrollo</span><span class="sxs-lookup"><span data-stu-id="88f1b-118">Developer Tools</span></span>  

<span data-ttu-id="88f1b-119">Esta versión comenzamos un importante esfuerzo de Microsoft Edge para refactorizar DevTools para mejorar la solidez y el rendimiento, además de agregar un conjunto de nuevas características que puede comenzar a usar hoy en las compilaciones de [Windows Insider](https://insider.windows.com) .</span><span class="sxs-lookup"><span data-stu-id="88f1b-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="88f1b-120">Consulte la [Guía de DevTools Microsoft Edge](../whats-new.md) para obtener más información sobre lo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="88f1b-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="88f1b-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="88f1b-121">JavaScript</span></span>  

<span data-ttu-id="88f1b-122">[EdgeHTML 16 desarrolla](https://blogs.windows.com/msedgedev/2017/10/31) las optimizaciones de rendimiento de JavaScript de versiones anteriores expandiendo la capacidad del motor de Chakra para aplazar o volver a aplazar funciones, usar memorias caché polimórficos y optimizar funciones con `try` / `finally` bloques.</span><span class="sxs-lookup"><span data-stu-id="88f1b-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="88f1b-123">Además, características que aparecen en la primera vista previa de la EdgeHTML 15 ahora son estables y habilitadas de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="88f1b-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="88f1b-124">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="88f1b-124">New features</span></span>  

<span data-ttu-id="88f1b-125">Activado de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="88f1b-125">On by default</span></span>  

*   <span data-ttu-id="88f1b-126">[Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \ ([Demo](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="88f1b-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="88f1b-127">Memoria compartida y atómicas</span><span class="sxs-lookup"><span data-stu-id="88f1b-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="88f1b-128">API de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="88f1b-128">Payment Request API</span></span>  

<span data-ttu-id="88f1b-129">La [API de solicitud de pago](../windows-integration/payment-request-api.md) es un estándar entre exploradores abierto que permite que los exploradores actúen como intermediario entre comerciantes, consumidores y formas de pago \ (como tarjetas de crédito \) que los consumidores han almacenado en la nube.</span><span class="sxs-lookup"><span data-stu-id="88f1b-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="88f1b-130">La API de EdgeHTML 16 se ha actualizado para coincidir con la última especificación de [API de solicitud de pago](https://w3c.github.io/payment-request) de W3C.</span><span class="sxs-lookup"><span data-stu-id="88f1b-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="88f1b-131">Esto incluye:</span><span class="sxs-lookup"><span data-stu-id="88f1b-131">This includes:</span></span>  

*   <span data-ttu-id="88f1b-132">Compatibilidad con el `canMakePayment()` método</span><span class="sxs-lookup"><span data-stu-id="88f1b-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="88f1b-133">Compatibilidad con la `requestId` propiedad</span><span class="sxs-lookup"><span data-stu-id="88f1b-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="88f1b-134">Compatibilidad con la `id` propiedad</span><span class="sxs-lookup"><span data-stu-id="88f1b-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="88f1b-135">El valor predeterminado del `complete()` parámetro del método `result` ha cambiado de "" a "desconocido".</span><span class="sxs-lookup"><span data-stu-id="88f1b-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="88f1b-136">Trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="88f1b-136">Service Workers</span></span>  

<span data-ttu-id="88f1b-137">Los [trabajadores del servicio](https://www.w3.org/TR/service-workers-1) son scripts controlados por eventos que se ejecutan en el fondo de una página web.</span><span class="sxs-lookup"><span data-stu-id="88f1b-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="88f1b-138">Los trabajadores de servicio habilitan la funcionalidad anteriormente solo disponible con aplicaciones nativas, como interceptar y administrar solicitudes de la red, administrar y controlar la sincronización en segundo plano, el almacenamiento local y las notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="88f1b-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="88f1b-139">El soporte técnico para el servicio de trabajo de servicio aún está en desarrollo, pero puede probar su PWA en Microsoft Edge con nuestro soporte técnico de trabajo de servicio experimental habilitando la característica de trabajo de servicio en `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="88f1b-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="88f1b-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="88f1b-140">WebVR</span></span>  

<span data-ttu-id="88f1b-141">WebVR para Microsoft Edge ha agregado compatibilidad con [los controladores de movimiento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span><span class="sxs-lookup"><span data-stu-id="88f1b-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="88f1b-142">Estos controladores tienen una posición precisa en el espacio, lo que permite una interacción minuciosa con objetos digitales en realidad virtual.</span><span class="sxs-lookup"><span data-stu-id="88f1b-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de movimiento" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="88f1b-144">Controladores de movimiento</span><span class="sxs-lookup"><span data-stu-id="88f1b-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="88f1b-145">WebVR también se ha optimizado para admitir dos tipos diferentes de experiencias.</span><span class="sxs-lookup"><span data-stu-id="88f1b-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="88f1b-146">Equipos de escritorio y portátiles **Windows Mixed Reality** con gráficos integrados.</span><span class="sxs-lookup"><span data-stu-id="88f1b-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="88f1b-147">Cuando esté conectado a estos dispositivos, nuestros auriculares con micrófono tan solo se ejecutarán a 60 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="88f1b-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="88f1b-148">**Windows Mixed Reality ultra PCS** : computadoras de escritorio y portátiles con gráficos discretos.</span><span class="sxs-lookup"><span data-stu-id="88f1b-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="88f1b-149">Cuando esté conectado a estos dispositivos, nuestros auriculares con micrófono tan solo se ejecutarán a 90 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="88f1b-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="88f1b-150">Ambas configuraciones soportarán el mismo video y las experiencias de juego.</span><span class="sxs-lookup"><span data-stu-id="88f1b-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="88f1b-151">Para obtener más información sobre las próximas actualizaciones de Windows Mixed Reality, consulta la entrada de blog de actualización de festividades de [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) .</span><span class="sxs-lookup"><span data-stu-id="88f1b-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="88f1b-152">Para obtener guías y demostraciones, vaya a la [Guía para desarrolladores de WebVR](/microsoft-edge/webvr).</span><span class="sxs-lookup"><span data-stu-id="88f1b-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="88f1b-153">Puesto que la especificación de WebVR aún está en desarrollo, la implementación de Microsoft Edge puede cambiar más adelante en la línea.</span><span class="sxs-lookup"><span data-stu-id="88f1b-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="88f1b-154">Nuevas API en EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="88f1b-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="88f1b-155">Esta es la lista completa de las API nuevas de EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="88f1b-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="88f1b-156">Se muestran en el formato de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="88f1b-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="88f1b-157">A pesar de que las siguientes API están expuestas en el DOM, el comportamiento end-to-end de algunos podría estar aún en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="88f1b-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="88f1b-158">Consulta el  [Estado de la plataforma de Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para la compatibilidad de características de Word oficial.</span><span class="sxs-lookup"><span data-stu-id="88f1b-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="88f1b-159">Nuevas API en EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="88f1b-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="88f1b-160">Consulta las <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> nuevas API de Pen en EdgeHTML 16 de </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="88f1b-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="88f1b-161">Versiones anteriores de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="88f1b-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="88f1b-162">EdgeHTML 12/Windows compilación 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="88f1b-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="88f1b-163">EdgeHTML 13/Windows compilación 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="88f1b-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="88f1b-164">EdgeHTML 14/Windows compilación 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="88f1b-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="88f1b-165">EdgeHTML 15/Windows compilación 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="88f1b-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
