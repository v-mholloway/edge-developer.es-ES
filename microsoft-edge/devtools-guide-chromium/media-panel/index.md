---
description: Use el panel multimedia para ver información y depurar los reproductores multimedia por pestaña del explorador.
title: Ver y depurar información de los reproductores multimedia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e6259cf573b76df7e281527ad30360b8f473a165
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230953"
---
# <span data-ttu-id="2be7f-104">Ver y depurar información de los reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-104">View and debug media players information</span></span>  

<span data-ttu-id="2be7f-105">Use el panel **multimedia** en Microsoft Edge DevTools para ver información y depurar los reproductores multimedia por pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="2be7f-105">Use the **Media** panel in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <span data-ttu-id="2be7f-106">Abrir el panel multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-106">Open the Media panel</span></span>  

<span data-ttu-id="2be7f-107">El panel **multimedia** es el lugar principal en DevTools para inspeccionar el reproductor multimedia de una página web.</span><span class="sxs-lookup"><span data-stu-id="2be7f-107">The **Media** panel is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="2be7f-108">[Abra DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="2be7f-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="2be7f-109">Para abrir el panel **multimedia** , elija **personalizar y controle DevTools** `...`  >  **más herramientas**  >  **multimedia**.</span><span class="sxs-lookup"><span data-stu-id="2be7f-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panel multimedia" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="2be7f-111">Panel **multimedia**</span><span class="sxs-lookup"><span data-stu-id="2be7f-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2be7f-112">Ver información de los reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-112">View media players information</span></span>  

1.  <span data-ttu-id="2be7f-113">Vaya a una página web con un reproductor multimedia, como la siguiente página web.</span><span class="sxs-lookup"><span data-stu-id="2be7f-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="2be7f-114">Maximizar la productividad con las herramientas para desarrolladores perimetrales</span><span class="sxs-lookup"><span data-stu-id="2be7f-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="2be7f-115">En el menú **Players** , se muestra un reproductor de medios.</span><span class="sxs-lookup"><span data-stu-id="2be7f-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="2be7f-116">Seleccione el reproductor.</span><span class="sxs-lookup"><span data-stu-id="2be7f-116">Select the player.</span></span>  <span data-ttu-id="2be7f-117">La pestaña **propiedades** muestra las propiedades del reproductor multimedia.</span><span class="sxs-lookup"><span data-stu-id="2be7f-117">The **Properties** tab displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propiedades de elementos multimedia" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="2be7f-119">Propiedades de elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2be7f-120">Para ver todos los eventos del reproductor multimedia, elija la pestaña **eventos** .</span><span class="sxs-lookup"><span data-stu-id="2be7f-120">To view all the media player events, choose the **Events** tab.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Eventos multimedia" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="2be7f-122">Eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2be7f-123">Para ver los registros de mensajes del reproductor multimedia, elija la pestaña **mensajes** .  Puede filtrar los mensajes por nivel de registro o cadena.</span><span class="sxs-lookup"><span data-stu-id="2be7f-123">To view the media player message logs, choose the **Messages** tab.  You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mensajes multimedia" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="2be7f-125">Mensajes multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-125">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2be7f-126">En la pestaña **escala de tiempo** , la reproducción multimedia y el estado del búfer se muestran en vivo.</span><span class="sxs-lookup"><span data-stu-id="2be7f-126">On the **Timeline** tab, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Escala de tiempo multimedia" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="2be7f-128">Escala de tiempo multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-128">Media timeline</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="2be7f-129">Depuración remota</span><span class="sxs-lookup"><span data-stu-id="2be7f-129">Remote debugging</span></span>  

<span data-ttu-id="2be7f-130">Ver la información de los reproductores multimedia en un dispositivo Android desde un equipo Windows o macOS.</span><span class="sxs-lookup"><span data-stu-id="2be7f-130">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="2be7f-131">Para configurar la depuración remota, vaya a introducción a la [depuración remota de dispositivos Android][DevtoolsGuideChromiumRemoteDebuggingIndex].</span><span class="sxs-lookup"><span data-stu-id="2be7f-131">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="2be7f-132">Ver la información de los reproductores multimedia de forma remota.</span><span class="sxs-lookup"><span data-stu-id="2be7f-132">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <span data-ttu-id="2be7f-133">Ocultar y mostrar reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-133">Hide and show media players</span></span>  

<span data-ttu-id="2be7f-134">A veces ejecuta más de un reproductor multimedia en una página web o usa la misma pestaña de explorador para examinar diferentes páginas web, cada una con reproductores multimedia.</span><span class="sxs-lookup"><span data-stu-id="2be7f-134">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="2be7f-135">Puede ocultar \ (o mostrar \) cada reproductor multimedia para una experiencia de depuración más sencilla.</span><span class="sxs-lookup"><span data-stu-id="2be7f-135">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="2be7f-136">Vaya a varias páginas web de vídeo diferentes usando la misma pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="2be7f-136">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="2be7f-137">Para ocultar reproductores multimedia, lleve a cabo una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2be7f-137">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="2be7f-138">Para ocultar un reproductor multimedia, desplace el puntero sobre un reproductor multimedia, abra el menú contextual \ (haga clic con el botón derecho \) y elija **ocultar reproductor**.</span><span class="sxs-lookup"><span data-stu-id="2be7f-138">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="2be7f-139">Para ocultar todos los demás reproductores multimedia, desplace el puntero sobre un reproductor multimedia y abra el menú contextual \ (haga clic con el botón derecho \) y elija **ocultar todos los demás**.</span><span class="sxs-lookup"><span data-stu-id="2be7f-139">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ocultar reproductores multimedia" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="2be7f-141">Ocultar reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-141">Hide media players</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2be7f-142">Exportar información de reproductor multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-142">Export media player information</span></span>  

1.  <span data-ttu-id="2be7f-143">Para descargar la información del reproductor multimedia como un archivo JSON, desplace el puntero sobre un reproductor multimedia y abra el menú contextual \ (haga clic con el botón derecho \) y elija **Guardar información del reproductor**.</span><span class="sxs-lookup"><span data-stu-id="2be7f-143">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportar información multimedia" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="2be7f-145">Exportar información multimedia</span><span class="sxs-lookup"><span data-stu-id="2be7f-145">Export media information</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2be7f-146">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2be7f-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abrir Microsoft Edge (cromo) DevTools | Microsoft docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximizar la productividad con las herramientas para desarrolladores de Edge | Vídeo de Bing"  

> [!NOTE]
> <span data-ttu-id="2be7f-150">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2be7f-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2be7f-151">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="2be7f-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2be7f-153">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2be7f-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

