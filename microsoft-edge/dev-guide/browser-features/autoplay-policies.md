---
description: Garantizar que el contenido multimedia de su sitio se comparará como se pretendía
title: 'Guía de desarrollo: directivas de reproducción automática'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 9/17/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, multimedia, vídeo, audio, reproducción automática
ms.custom: seodec18
ms.openlocfilehash: 397c6f0a22359dbfab7c44370b0429147b7c9834
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572969"
---
# <span data-ttu-id="ab751-104">Directivas de reproducción automática</span><span class="sxs-lookup"><span data-stu-id="ab751-104">Autoplay Policies</span></span>

<span data-ttu-id="ab751-105">Microsoft Edge proporciona a los clientes la posibilidad de personalizar sus preferencias de navegación en sitios web con sonido de reproducción automática con el fin de minimizar las distracciones en la web y ahorrar ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="ab751-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="ab751-106">Además, Microsoft Edge suprime automáticamente la reproducción automática de los elementos multimedia en las pestañas de fondo.</span><span class="sxs-lookup"><span data-stu-id="ab751-106">Additionaly, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="ab751-107">Los usuarios pueden personalizar el comportamiento de los medios con controles de reproducción automática [globales](#global-media-autoplay-settings) y [por sitio](#per-site-media-autoplay-settings) , que proporcionan las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ab751-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>

- <span data-ttu-id="ab751-108">**Permitir** es el predeterminado y continuará reproduciendo vídeos cuando una pestaña se visualiza por primera vez en primer plano, a la discreción del sitio.</span><span class="sxs-lookup"><span data-stu-id="ab751-108">**Allow**  is the default and will continue to play videos when a tab is first viewed in the foreground, at the site’s discretion.</span></span>

- <span data-ttu-id="ab751-109">**Límite** restringirá la reproducción automática para que solo funcionen los vídeos silenciados, de modo que los usuarios nunca se sorprendan por sonido.</span><span class="sxs-lookup"><span data-stu-id="ab751-109">**Limit** will restrict autoplay to only work when videos are muted, so users are never surprised by sound.</span></span> <span data-ttu-id="ab751-110">Una vez que el usuario hace clic en cualquier lugar de la página, la reproducción automática se vuelve a habilitar y seguirá estando permitida dentro de ese dominio en esa pestaña.</span><span class="sxs-lookup"><span data-stu-id="ab751-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>

- <span data-ttu-id="ab751-111">**Bloquear** evitará la reproducción automática en todos los sitios hasta que los usuarios interactúen directamente con el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="ab751-111">**Block** will prevent autoplay on all sites until users directly interact with the media content.</span></span>

## <span data-ttu-id="ab751-112">Configuración de la reproducción automática de multimedia global</span><span class="sxs-lookup"><span data-stu-id="ab751-112">Global media autoplay settings</span></span>

<span data-ttu-id="ab751-113">Los usuarios pueden controlar el comportamiento predeterminado de reproducción automática de todos los sitios en **Configuración avanzada**  >  **reproducción automática de multimedia**.</span><span class="sxs-lookup"><span data-stu-id="ab751-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>

![Configuración de la reproducción automática de multimedia global](../media/autoplay_global.png)

## <span data-ttu-id="ab751-115">Configuración de reproducción automática multimedia por sitio</span><span class="sxs-lookup"><span data-stu-id="ab751-115">Per-site media autoplay settings</span></span>

<span data-ttu-id="ab751-116">Los usuarios pueden controlar el comportamiento de la reproducción automática en función de cada sitio en la sección **permisos de sitios web** del panel información del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="ab751-116">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span> <span data-ttu-id="ab751-117">Para encontrar esta configuración, haga clic en el icono de información o en el icono de candado situado en el lado izquierdo de la barra de direcciones y haga clic en "configuración de reproducción automática de multimedia" para comenzar.</span><span class="sxs-lookup"><span data-stu-id="ab751-117">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on “Media autoplay settings” to get started.</span></span>

<span data-ttu-id="ab751-118">La configuración por sitio invalida la configuración global.</span><span class="sxs-lookup"><span data-stu-id="ab751-118">Per-site settings override the global setting.</span></span> <span data-ttu-id="ab751-119">Por ejemplo, si un usuario tiene su configuración global establecida en "permitir" pero cambia una configuración por sitio a "bloquear", la reproducción automática se bloqueará para ese sitio.</span><span class="sxs-lookup"><span data-stu-id="ab751-119">For example, if a user has their global setting set to “Allow” but changes a per-site setting to “Block”, autoplay will be blocked for that site.</span></span>

![Configuración de reproducción automática multimedia por sitio](../media/autoplay_per-site.png)
 
## <span data-ttu-id="ab751-121">Procedimientos recomendados para desarrolladores web</span><span class="sxs-lookup"><span data-stu-id="ab751-121">Best Practices for Web Developers</span></span>

<span data-ttu-id="ab751-122">A continuación se explica cómo garantizar una buena experiencia de usuario con elementos multimedia hospedados en su sitio:</span><span class="sxs-lookup"><span data-stu-id="ab751-122">Here's how to ensure a good user experience with media hosted on your site:</span></span>

- <span data-ttu-id="ab751-123">Supongamos que cada uso de un elemento multimedia se requiere un gesto del usuario para iniciar la reproducción (a medida que los usuarios pueden bloquear la reproducción automática en cualquier momento) y planificar según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ab751-123">Assume  each use of a media element wil require a user gesture to start the playback (as users can block autoplay at any point in time) and plan accordingly.</span></span>  <span data-ttu-id="ab751-124">Las directivas de reproducción automática global y por sitio se aplican a todos los `<audio>` `<video>` elementos y, independientemente de cómo se usan en su sitio.</span><span class="sxs-lookup"><span data-stu-id="ab751-124">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>

- <span data-ttu-id="ab751-125">Asegúrate de que los controles multimedia estén siempre presentes tanto en los medios del sitio como en el contenido de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ab751-125">Ensure that media controls are always present on both site media and ad content.</span></span> <span data-ttu-id="ab751-126">Esto proporcionará a los usuarios la posibilidad de reiniciar la reproducción si la reproducción automática está bloqueada en la página.</span><span class="sxs-lookup"><span data-stu-id="ab751-126">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>

- <span data-ttu-id="ab751-127">Evalúe cómo la reproducción automática puede influir en la experiencia de los usuarios en su sitio web y considere la posibilidad de usar la reproducción automática para minimizar la reproducción de archivos multimedia no deseados.</span><span class="sxs-lookup"><span data-stu-id="ab751-127">Evaluate how autoplay may affect users’ experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span> <span data-ttu-id="ab751-128">Si la reproducción automática es una parte crucial de su experiencia, considere la posibilidad de usar contenido silenciado para iniciar y permitir que el usuario reactive el audio.</span><span class="sxs-lookup"><span data-stu-id="ab751-128">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span> <span data-ttu-id="ab751-129">Para el contenido silenciado en la reproducción automática, el origen de audio debe estar silenciado o no se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="ab751-129">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span> <span data-ttu-id="ab751-130">En caso contrario, el elemento no se considerará silenciado.</span><span class="sxs-lookup"><span data-stu-id="ab751-130">Otherwise the element will not be considered as muted.</span></span>

- <span data-ttu-id="ab751-131">A menos que sea absolutamente necesario hacer lo contrario, use los controles de explorador nativos para la reproducción de contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="ab751-131">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span> <span data-ttu-id="ab751-132">Esto asegurará una experiencia coherente para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ab751-132">This will ensure a consistent experience for users.</span></span> <span data-ttu-id="ab751-133">Si está creando controles personalizados en su lugar, asegúrese de que los controles multimedia estén siempre presentes y de que los controles respondan correctamente a la supresión de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="ab751-133">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>

### <span data-ttu-id="ab751-134">Delegación de iframe</span><span class="sxs-lookup"><span data-stu-id="ab751-134">Iframe delegation</span></span>

<span data-ttu-id="ab751-135">La reproducción automática en una `<iframe>` heredará el permiso de reproducción automática de la Página principal, independientemente del origen del contenido.</span><span class="sxs-lookup"><span data-stu-id="ab751-135">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span> <span data-ttu-id="ab751-136">En un escenario de lista de reproducción en el que cada archivo multimedia está hospedado por un iframe independiente, el usuario solo necesita iniciar la reproducción una vez para toda la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ab751-136">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>

### <span data-ttu-id="ab751-137">Detectar cuándo está permitida la reproducción automática</span><span class="sxs-lookup"><span data-stu-id="ab751-137">Detecting when autoplay is allowed</span></span>

<span data-ttu-id="ab751-138">Puede ajustar los controles de reproducción para que muestren el estado correcto cuando se bloquea la reproducción automática examinando la promesa devuelta por la `play()` función en el elemento multimedia:</span><span class="sxs-lookup"><span data-stu-id="ab751-138">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>

```Javascript

var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}

```
