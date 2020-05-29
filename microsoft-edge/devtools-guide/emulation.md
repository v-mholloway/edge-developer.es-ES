---
description: Use el panel de emulación para probar diferentes perfiles de explorador, tamaños de pantalla y resoluciones, y coordenadas de ubicación GPS
title: 'DevTools: emulación'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, emulación de dispositivos, diseño dinámico, ubicación geográfica, resolución
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573838"
---
# <span data-ttu-id="95906-104">Emulación</span><span class="sxs-lookup"><span data-stu-id="95906-104">Emulation</span></span>

<span data-ttu-id="95906-105">El panel de *emulación* le ayuda a:</span><span class="sxs-lookup"><span data-stu-id="95906-105">The *Emulation* panel helps you to:</span></span>
 - <span data-ttu-id="95906-106">Simular diversos [perfiles de dispositivos](#device), [exploradores](#browser-profile), [tamaños de pantalla y resoluciones](#display)</span><span class="sxs-lookup"><span data-stu-id="95906-106">Simulate various [device profiles](#device), [browsers](#browser-profile), [screen sizes and resolutions](#display)</span></span>
 - <span data-ttu-id="95906-107">Probar distintas [configuraciones y coordenadas geolocales](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="95906-107">Test different [geolocation settings and coordinates](#geolocation)</span></span>

![El panel de emulación DevTools de Microsoft Edge](./media/emulation.png)

1. <span data-ttu-id="95906-109">El botón **conservar la configuración de emulación** guardará los cambios que haya realizado desde la configuración de emulación de escritorio predeterminada, incluso cuando cierra y vuelve a abrir la DevTools.</span><span class="sxs-lookup"><span data-stu-id="95906-109">The **Persist Emulation settings** button will save any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span> 

2. <span data-ttu-id="95906-110">El botón **restablecer configuración de emulación** restablecerá la configuración de emulación al perfil de explorador de *escritorio* predeterminado y a la cadena de agente de usuario de Microsoft Edge con GPS desactivado.</span><span class="sxs-lookup"><span data-stu-id="95906-110">The **Reset Emulation settings** button will reset your emulation settings back to the default *Desktop* browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>

3. <span data-ttu-id="95906-111">Cuando se cambia la configuración predeterminada de cualquiera de estas opciones, la pestaña **emulación** mostrará una alerta informativa para indicar que se está emulando algún aspecto del comportamiento del explorador.</span><span class="sxs-lookup"><span data-stu-id="95906-111">When any of these options are changed from the default, the **Emulation** tab will show an informational alert to indicate that some aspect of your browser's behavior is being emulated.</span></span>

## <span data-ttu-id="95906-112">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="95906-112">Device</span></span>

<span data-ttu-id="95906-113">Elija entre una lista preestablecida de perfiles de dispositivo de Windows que configure automáticamente las demás opciones de emulación o especifique su propia configuración *personalizada* .</span><span class="sxs-lookup"><span data-stu-id="95906-113">Pick from a preset list of Windows device profiles which  automatically configure the other emulation options or specify your own *Custom* configuation.</span></span> <span data-ttu-id="95906-114">Cambie de nuevo a *predeterminado* para restablecer todas las herramientas de emulación.</span><span class="sxs-lookup"><span data-stu-id="95906-114">Switch back to *Default* to reset all the emulation tools.</span></span>

## <span data-ttu-id="95906-115">Modo</span><span class="sxs-lookup"><span data-stu-id="95906-115">Mode</span></span>

### <span data-ttu-id="95906-116">Perfil de explorador</span><span class="sxs-lookup"><span data-stu-id="95906-116">Browser profile</span></span>
<span data-ttu-id="95906-117">Una forma rápida de simular una página en un dispositivo Windows Phone es cambiar la configuración del **Perfil del explorador** a *Windows Phone*.</span><span class="sxs-lookup"><span data-stu-id="95906-117">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to *Windows Phone*.</span></span>

#### <span data-ttu-id="95906-118">Cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="95906-118">User agent string</span></span>

<span data-ttu-id="95906-119">Modificar la cadena de agente de usuario para imitar a otro explorador es un buen primer paso en la depuración de errores que solo ocurren en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="95906-119">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span> 

<span data-ttu-id="95906-120">Los scripts de front-end y/o back-end a veces usan la cadena de agente de usuario para detectar qué explorador está usando.</span><span class="sxs-lookup"><span data-stu-id="95906-120">Front end and/or back end scripts sometimes use the user agent string  to detect which browser you're using.</span></span> <span data-ttu-id="95906-121">Y incluso si no usa la detección del explorador en su propio código, es posible que esté usando una biblioteca de JavaScript de terceros o una secuencia de comandos del servidor que sí lo hace.</span><span class="sxs-lookup"><span data-stu-id="95906-121">And even when you're not using browser detection in your own code, you may be using a third-party JavaScript library or server-side script that does.</span></span>

<span data-ttu-id="95906-122">El problema con la detección de explorador es que a menudo se usa para cambiar de tamaño o cambiar las características de una página web en función de lo que el desarrollador que escribe la secuencia de comandos cree que su explorador puede hacer, en lugar de detectar qué es lo que su explorador puede hacer realmente usando la detección de características.</span><span class="sxs-lookup"><span data-stu-id="95906-122">The problem with browser detection is that it's often used to scale back or change the features in a webpage based on what the developer writing the script thinks your browser can do, rather than detecting what your browser can actually do using feature detection.</span></span> <span data-ttu-id="95906-123">Esto puede provocar un comportamiento inesperado, ya que el código destinado a Windows Internet Explorer 8 puede ejecutarse de forma muy diferente en Microsoft Edge. o una característica que el explorador sea perfectamente capaz de admitir puede estar deshabilitada debido a una suposición realizada por el desarrollador.</span><span class="sxs-lookup"><span data-stu-id="95906-123">This can cause unexpected behavior, because code targeted at Windows Internet Explorer 8 can run very differently in Microsoft Edge; or a feature your browser is perfectly capable of supporting might be disabled because of an assumption made by the developer.</span></span>

<span data-ttu-id="95906-124">Si al cambiar la cadena de agente de usuario se elimina el problema, es probable que la detección del explorador causase.</span><span class="sxs-lookup"><span data-stu-id="95906-124">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>

## <span data-ttu-id="95906-125">Pantalla</span><span class="sxs-lookup"><span data-stu-id="95906-125">Display</span></span>

<span data-ttu-id="95906-126">La emulación de pantalla le permite obtener una vista previa del sitio en diferentes tamaños y resoluciones de pantalla: desde monitores de escritorio convencionales hasta pantallas móviles más pequeñas o pantallas de alta resolución más recientes.</span><span class="sxs-lookup"><span data-stu-id="95906-126">Display emulation lets you preview your site on different screen sizes and resolutions: from conventional desktop monitors to smaller mobile screens or newer high-resolution displays.</span></span>

<span data-ttu-id="95906-127">Las emulaciones están adaptadas para probar y hacer coincidir las dimensiones físicas de las pantallas que se están emulando.</span><span class="sxs-lookup"><span data-stu-id="95906-127">Emulations are adapted to try and match the physical dimensions of the screens being emulated.</span></span> <span data-ttu-id="95906-128">Es posible que los píxeles emulados parezcan comprimidos o expandidos, y no se recomienda la emulación si necesita probar la posición perfecta de los elementos HTML en píxeles.</span><span class="sxs-lookup"><span data-stu-id="95906-128">Emulated pixels might appear compressed or expanded, and emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span> <span data-ttu-id="95906-129">La emulación es, no obstante, adecuada para probar diseños con capacidad de respuesta e identificar problemas de posicionamiento de elementos más grandes.</span><span class="sxs-lookup"><span data-stu-id="95906-129">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>

### <span data-ttu-id="95906-130">Orientación</span><span class="sxs-lookup"><span data-stu-id="95906-130">Orientation</span></span>

<span data-ttu-id="95906-131">Elija entre el modo *horizontal* o el *vertical* .</span><span class="sxs-lookup"><span data-stu-id="95906-131">Choose from *Landscape* or *Portrait* mode.</span></span>

### <span data-ttu-id="95906-132">Resolución</span><span class="sxs-lookup"><span data-stu-id="95906-132">Resolution</span></span>

<span data-ttu-id="95906-133">Elija una lista preestablecida de resoluciones de dispositivos populares o especifique su propia configuración *personalizada* . Se admiten resoluciones de hasta 80 pulgadas y 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="95906-133">Choose from a preset list of popular device resolutions, or specify your own *Custom* config. Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>

## <span data-ttu-id="95906-134">Geolocalización</span><span class="sxs-lookup"><span data-stu-id="95906-134">Geolocation</span></span>

<span data-ttu-id="95906-135">Si su sitio usa la [API de ubicación](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) geográfica para proporcionar servicios basados en la ubicación, puede probar fácilmente distintas coordenadas GPS y Estados de los sensores desde la comodidad de su escritorio.</span><span class="sxs-lookup"><span data-stu-id="95906-135">If your site uses the [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) to provide location-based services, you can easily test different GPS coordinates and sensor states from the convenience of your desktop.</span></span> <span data-ttu-id="95906-136">Esta configuración invalidará las coordenadas de GPS reales y el estado de sensor en los equipos que admitan geolocalización.</span><span class="sxs-lookup"><span data-stu-id="95906-136">These settings will override any actual GPS coordinates and the sensor state on machines that support geolocation.</span></span> 

<span data-ttu-id="95906-137">Al igual que con el uso de datos personales en la web, los usuarios primero tendrán que conceder permiso a su sitio para usar su ubicación.</span><span class="sxs-lookup"><span data-stu-id="95906-137">As with any usage of personal data on the web, your users will first need to grant your site permission to use their location.</span></span> <span data-ttu-id="95906-138">Puede probar cómo se comporta su sitio con y sin permisos de ubicación en el panel de *configuración* de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="95906-138">You can test how your site behaves with and without location permissions from the Microsoft Edge *Settings* panel:</span></span>

<span data-ttu-id="95906-139">**...** >  **Configuración**  >  **Ver configuración avanzada**  >  Permisos de sitio **Web**  >  **Administrar**</span><span class="sxs-lookup"><span data-stu-id="95906-139">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>

![Administrar permisos de sitio web desde el panel de configuración de Microsoft Edge](./media/settings_manage_permissions.png)

## <span data-ttu-id="95906-141">Abreviados</span><span class="sxs-lookup"><span data-stu-id="95906-141">Shortcuts</span></span>

| <span data-ttu-id="95906-142">Acción</span><span class="sxs-lookup"><span data-stu-id="95906-142">Action</span></span>                   | <span data-ttu-id="95906-143">Método abreviado</span><span class="sxs-lookup"><span data-stu-id="95906-143">Shortcut</span></span>               |
|:-------------------------|:-----------------------|
| <span data-ttu-id="95906-144">Restablecer la configuración de emulación</span><span class="sxs-lookup"><span data-stu-id="95906-144">Reset Emulation settings</span></span> | `CTRL` + `SHIFT` + `L` |
