---
description: Use el panel de emulación para probar diferentes perfiles de explorador, tamaños de pantalla y resoluciones, y coordenadas de ubicación GPS
title: 'DevTools: emulación'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, emulación de dispositivos, diseño dinámico, ubicación geográfica, resolución
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236139"
---
# <span data-ttu-id="2349d-104">Emulación</span><span class="sxs-lookup"><span data-stu-id="2349d-104">Emulation</span></span>  

> [!NOTE]
> <span data-ttu-id="2349d-105">El nuevo Microsoft Edge se ha creado con cromo y comienza en la versión 75.</span><span class="sxs-lookup"><span data-stu-id="2349d-105">The new Microsoft Edge is built using Chromium, and starts at version 75.</span></span>  <span data-ttu-id="2349d-106">Para obtener más información, [descarga el nuevo Microsoft Edge][MicrosoftNewEdge]y prueba las nuevas [herramientas para desarrolladores de Microsoft Edge (cromo)][DevtoolsGuideChromium].</span><span class="sxs-lookup"><span data-stu-id="2349d-106">For more information, [download the new Microsoft Edge][MicrosoftNewEdge], and try out the new [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromium].</span></span>  
> 
> <span data-ttu-id="2349d-107">Para emular diferentes dispositivos, exploradores, tamaños de pantalla y resoluciones en el nuevo DevTools, vaya a [emular dispositivos móviles en Microsoft Edge \(cromo \) DevTools][DevtoolsGuideChromiumDeviceMode].</span><span class="sxs-lookup"><span data-stu-id="2349d-107">To emulate different devices, browsers, screen sizes, and resolutions in the new DevTools, navigate to [Emulate Mobile Devices in Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span></span>  

<span data-ttu-id="2349d-108">El panel de **emulación** ayuda a realizar las siguientes actividades.</span><span class="sxs-lookup"><span data-stu-id="2349d-108">The **Emulation** panel helps with the following activities.</span></span>    

*   <span data-ttu-id="2349d-109">Simular diversos [perfiles de dispositivos](#device), [exploradores](#browser-profile), [tamaños de pantalla y resoluciones](#display)</span><span class="sxs-lookup"><span data-stu-id="2349d-109">Simulate various [device profiles](#device), [browsers](#browser-profile), and [screen sizes and resolutions](#display)</span></span>  
*   <span data-ttu-id="2349d-110">Probar distintas [configuraciones y coordenadas geolocales](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="2349d-110">Test different [geolocation settings and coordinates](#geolocation)</span></span>  

:::image type="complex" source="./media/emulation.png" alt-text="El panel de emulación DevTools de Microsoft Edge" lightbox="./media/emulation.png":::
   <span data-ttu-id="2349d-112">El panel de **emulación** DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2349d-112">The Microsoft Edge DevTools **Emulation** panel</span></span>  
:::image-end:::  

1.  <span data-ttu-id="2349d-113">El botón **conservar la configuración de emulación** guarda los cambios realizados en la configuración de emulación de escritorio predeterminada, incluso cuando se cierra y vuelve a abrir la DevTools.</span><span class="sxs-lookup"><span data-stu-id="2349d-113">The **Persist Emulation settings** button saves any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span>  

1.  <span data-ttu-id="2349d-114">El botón **restablecer configuración de emulación** restablece la configuración de emulación al perfil de explorador de escritorio predeterminado y a la cadena de agente de usuario de Microsoft Edge con GPS desactivado.</span><span class="sxs-lookup"><span data-stu-id="2349d-114">The **Reset Emulation settings** button resets your emulation settings back to the default Desktop browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>  

1.  <span data-ttu-id="2349d-115">Cuando se cambia la configuración predeterminada de cualquiera de estas opciones, la pestaña **emulación** muestra una alerta informativa para indicar que se está emulando algún aspecto del comportamiento de su explorador.</span><span class="sxs-lookup"><span data-stu-id="2349d-115">When any of these options are changed from the default, the **Emulation** tab displays an informational alert to indicate that some aspect of the behavior of your browser is being emulated.</span></span>  

## <span data-ttu-id="2349d-116">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="2349d-116">Device</span></span>  

<span data-ttu-id="2349d-117">Elija entre una lista preestablecida de perfiles de dispositivo de Windows que configure automáticamente las demás opciones de emulación o especifique su propia configuración **personalizada** .</span><span class="sxs-lookup"><span data-stu-id="2349d-117">Pick from a preset list of Windows device profiles that automatically configure the other emulation options or specify your own **Custom** configuration.</span></span>  <span data-ttu-id="2349d-118">Cambie de nuevo a **predeterminado** para restablecer todas las herramientas de emulación.</span><span class="sxs-lookup"><span data-stu-id="2349d-118">Switch back to **Default** to reset all the emulation tools.</span></span>  

## <span data-ttu-id="2349d-119">Modo</span><span class="sxs-lookup"><span data-stu-id="2349d-119">Mode</span></span>  

### <span data-ttu-id="2349d-120">Perfil de explorador</span><span class="sxs-lookup"><span data-stu-id="2349d-120">Browser profile</span></span>  

<span data-ttu-id="2349d-121">Una forma rápida de simular una página en un dispositivo Windows Phone es cambiar la configuración del **Perfil del explorador** a **Windows Phone**.</span><span class="sxs-lookup"><span data-stu-id="2349d-121">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to **Windows Phone**.</span></span>  

#### <span data-ttu-id="2349d-122">Cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="2349d-122">User agent string</span></span>  

<span data-ttu-id="2349d-123">Modificar la cadena de agente de usuario para imitar a otro explorador es un buen primer paso en la depuración de errores que solo ocurren en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2349d-123">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span>  

<span data-ttu-id="2349d-124">Los scripts usan la cadena de agente de usuario para detectar qué explorador se usa.</span><span class="sxs-lookup"><span data-stu-id="2349d-124">Scripts use the user agent string to detect which browser is used.</span></span>  <span data-ttu-id="2349d-125">El script puede ser front-end, back-end o front-end y back-end.</span><span class="sxs-lookup"><span data-stu-id="2349d-125">Script may be front-end, back-end, or front-end and back-end.</span></span>  <span data-ttu-id="2349d-126">Aunque el código no usa la detección del explorador, el código puede heredarlo de una biblioteca de JavaScript de terceros o de una secuencia de comandos del servidor.</span><span class="sxs-lookup"><span data-stu-id="2349d-126">Although your code does not use browser detection, your code may inherit it from a third-party JavaScript library or server-side script.</span></span>  

<span data-ttu-id="2349d-127">El problema con la detección de explorador es que puede escalar \(o cambiar \) características en la página web con suposiciones acerca de las capacidades del explorador.</span><span class="sxs-lookup"><span data-stu-id="2349d-127">The problem with browser detection is that you may scale-back \(or change\) features in your webpage using assumptions about browser capabilities.</span></span> <span data-ttu-id="2349d-128">En su lugar, debe considerar la posibilidad de usar la detección de características para detectar las capacidades de su explorador.</span><span class="sxs-lookup"><span data-stu-id="2349d-128">Instead, you should consider using feature detection to detect the capabilities of your browser.</span></span>  <span data-ttu-id="2349d-129">Se puede producir un comportamiento inesperado debido a una de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="2349d-129">Unexpected behavior may occur because of one of the following situations.</span></span>  

*   <span data-ttu-id="2349d-130">El código dirigido a Windows Internet Explorer 8 puede ejecutarse de forma diferente en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2349d-130">Code targeted at Windows Internet Explorer 8 may run differently in Microsoft Edge.</span></span>  
*   <span data-ttu-id="2349d-131">Una característica que el explorador debe admitir está deshabilitada debido a una suposición realizada por el desarrollador.</span><span class="sxs-lookup"><span data-stu-id="2349d-131">A feature that your browser should support is disabled, because of an assumption made by the developer.</span></span>  

<span data-ttu-id="2349d-132">Si al cambiar la cadena de agente de usuario se elimina el problema, es probable que la detección del explorador causase.</span><span class="sxs-lookup"><span data-stu-id="2349d-132">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>  

## <span data-ttu-id="2349d-133">Pantalla</span><span class="sxs-lookup"><span data-stu-id="2349d-133">Display</span></span>  

<span data-ttu-id="2349d-134">Emulación de pantalla para obtener una vista previa del sitio en diferentes tamaños y resoluciones de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2349d-134">Display emulation to preview your site on different screen sizes and resolutions.</span></span>  

*   <span data-ttu-id="2349d-135">monitores de escritorio convencionales</span><span class="sxs-lookup"><span data-stu-id="2349d-135">conventional desktop monitors</span></span>  
*   <span data-ttu-id="2349d-136">pantallas móviles más pequeñas</span><span class="sxs-lookup"><span data-stu-id="2349d-136">smaller mobile screens</span></span>  
*   <span data-ttu-id="2349d-137">pantallas más recientes de alta resolución</span><span class="sxs-lookup"><span data-stu-id="2349d-137">newer high-resolution displays</span></span>  

<span data-ttu-id="2349d-138">Las emulaciones están adaptadas para intentar coincidir las dimensiones físicas de las pantallas que se están emulando.</span><span class="sxs-lookup"><span data-stu-id="2349d-138">Emulations are adapted to try to match the physical dimensions of the screens being emulated.</span></span>  <span data-ttu-id="2349d-139">Los píxeles emulados pueden parecer comprimidos o expandidos.</span><span class="sxs-lookup"><span data-stu-id="2349d-139">Emulated pixels may appear compressed or expanded.</span></span> <span data-ttu-id="2349d-140">No se recomienda la emulación si necesita probar la posición perfecta de los elementos HTML en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2349d-140">Emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span>  <span data-ttu-id="2349d-141">La emulación es, no obstante, adecuada para probar diseños con capacidad de respuesta e identificar problemas de posicionamiento de elementos más grandes.</span><span class="sxs-lookup"><span data-stu-id="2349d-141">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>  

### <span data-ttu-id="2349d-142">Orientación</span><span class="sxs-lookup"><span data-stu-id="2349d-142">Orientation</span></span>  

<span data-ttu-id="2349d-143">Elija entre el modo **horizontal** o el **vertical** .</span><span class="sxs-lookup"><span data-stu-id="2349d-143">Choose from **Landscape** or **Portrait** mode.</span></span>  

### <span data-ttu-id="2349d-144">Resolución</span><span class="sxs-lookup"><span data-stu-id="2349d-144">Resolution</span></span>  

<span data-ttu-id="2349d-145">Elija una lista preestablecida de resoluciones de dispositivos populares o especifique su propia configuración **personalizada** .  Se admiten resoluciones de hasta 80 pulgadas y 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="2349d-145">Choose from a preset list of popular device resolutions, or specify your own **Custom** config.  Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>  

## <span data-ttu-id="2349d-146">Geolocalización</span><span class="sxs-lookup"><span data-stu-id="2349d-146">Geolocation</span></span>  

<span data-ttu-id="2349d-147">Si su sitio Web usa la [API de ubicación geográfica][MdnGeolocationUsing] para proporcionar servicios basados en la ubicación, las siguientes actividades estarán disponibles desde la comodidad de su escritorio.</span><span class="sxs-lookup"><span data-stu-id="2349d-147">If your website uses the [Geolocation API][MdnGeolocationUsing] to provide location-based services, the following activities are available from the convenience of your desktop.</span></span>  

*   <span data-ttu-id="2349d-148">Pruebe fácilmente distintas coordenadas GPS</span><span class="sxs-lookup"><span data-stu-id="2349d-148">easily test different GPS coordinates</span></span>  
*   <span data-ttu-id="2349d-149">prueba fácilmente diferentes Estados de los sensores</span><span class="sxs-lookup"><span data-stu-id="2349d-149">easily test different sensor states</span></span>  

<span data-ttu-id="2349d-150">La configuración suplanta las coordenadas de GPS reales y el estado de sensor en dispositivos que admiten geolocalización.</span><span class="sxs-lookup"><span data-stu-id="2349d-150">The settings override any actual GPS coordinates and the sensor state on devices that support geolocation.</span></span>  

<span data-ttu-id="2349d-151">Tu sitio web debe solicitar y tener permiso de un usuario antes de usar la ubicación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2349d-151">Your website must request and be granted permission from a user before using the device location.</span></span>  <span data-ttu-id="2349d-152">Pruebe cómo se comporta su sitio con y sin permisos de ubicación en el panel de **configuración** de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2349d-152">Test how your site behaves with and without location permissions from the Microsoft Edge **Settings** panel.</span></span>  

<span data-ttu-id="2349d-153">**...** >  **Configuración**  >  **Ver configuración avanzada**  >  Permisos de sitio **Web**  >  **Administrar**</span><span class="sxs-lookup"><span data-stu-id="2349d-153">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Administrar permisos de sitio web desde el panel de configuración de Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   <span data-ttu-id="2349d-155">Administrar permisos de sitio web desde el panel de **configuración** de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2349d-155">Manage website permissions from the Microsoft Edge **Settings** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="2349d-156">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="2349d-156">Shortcuts</span></span>

| <span data-ttu-id="2349d-157">Acción</span><span class="sxs-lookup"><span data-stu-id="2349d-157">Action</span></span>  | <span data-ttu-id="2349d-158">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="2349d-158">Shortcut</span></span>  |  
|:--- |:--- |  
| <span data-ttu-id="2349d-159">Restablecer la configuración de emulación</span><span class="sxs-lookup"><span data-stu-id="2349d-159">Reset Emulation settings</span></span> | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API de ubicación geográfica | MDN"  
