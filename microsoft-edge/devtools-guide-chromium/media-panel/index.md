---
description: Usa la herramienta Multimedia para ver información y depurar los reproductores multimedia por pestaña del explorador.
title: Ver y depurar información de reproductores multimedia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0d2a60c31d5239a4b47102ae96a713b8bfcf46f3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564066"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="view-and-debug-media-players-information"></a><span data-ttu-id="46fde-104">Ver y depurar información de reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-104">View and debug media players information</span></span>  

<span data-ttu-id="46fde-105">Use la **herramienta Multimedia** en Microsoft Edge DevTools para ver información y depurar los reproductores multimedia por pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="46fde-105">Use the **Media** tool in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <a name="open-the-media-tool"></a><span data-ttu-id="46fde-106">Abrir la herramienta Multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-106">Open the Media tool</span></span>  

<span data-ttu-id="46fde-107">La **herramienta** Multimedia es el lugar principal en DevTools para inspeccionar el reproductor multimedia de una página web.</span><span class="sxs-lookup"><span data-stu-id="46fde-107">The **Media** tool is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="46fde-108">[Abra DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="46fde-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="46fde-109">Para abrir el panel **Multimedia,** elija **Personalizar y controlar DevTools** `...`  >  **Más herramientas**  >  **Multimedia**.</span><span class="sxs-lookup"><span data-stu-id="46fde-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panel multimedia" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="46fde-111">**Panel multimedia**</span><span class="sxs-lookup"><span data-stu-id="46fde-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <a name="view-media-players-information"></a><span data-ttu-id="46fde-112">Ver información de reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-112">View media players information</span></span>  

1.  <span data-ttu-id="46fde-113">Navegue a una página web con un reproductor multimedia, como la siguiente página web.</span><span class="sxs-lookup"><span data-stu-id="46fde-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="46fde-114">Maximizar la productividad con edge Developer Tools</span><span class="sxs-lookup"><span data-stu-id="46fde-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="46fde-115">En el **menú Reproductores,** se muestra un reproductor multimedia.</span><span class="sxs-lookup"><span data-stu-id="46fde-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="46fde-116">Elige el jugador.</span><span class="sxs-lookup"><span data-stu-id="46fde-116">Choose the player.</span></span>  <span data-ttu-id="46fde-117">El **panel** Propiedades muestra las propiedades del reproductor multimedia.</span><span class="sxs-lookup"><span data-stu-id="46fde-117">The **Properties** panel displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propiedades multimedia" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="46fde-119">Propiedades multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46fde-120">Para ver todos los eventos del reproductor multimedia, elija el panel **Eventos.**</span><span class="sxs-lookup"><span data-stu-id="46fde-120">To view all the media player events, choose the **Events** panel.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Eventos multimedia" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="46fde-122">Eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46fde-123">Para ver los registros de mensajes del reproductor multimedia, elija **el** panel Mensajes.</span><span class="sxs-lookup"><span data-stu-id="46fde-123">To view the media player message logs, choose the **Messages** panel.</span></span>  <span data-ttu-id="46fde-124">Puede filtrar los mensajes por nivel de registro o cadena.</span><span class="sxs-lookup"><span data-stu-id="46fde-124">You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mensajes multimedia" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="46fde-126">Mensajes multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-126">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46fde-127">En el panel **Escala de** tiempo, la reproducción multimedia y el estado del búfer se muestran en directo.</span><span class="sxs-lookup"><span data-stu-id="46fde-127">On the **Timeline** panel, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Escala de tiempo de medios" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="46fde-129">Escala de tiempo de medios</span><span class="sxs-lookup"><span data-stu-id="46fde-129">Media timeline</span></span>  
    :::image-end:::  
    
### <a name="remote-debugging"></a><span data-ttu-id="46fde-130">Depuración remota</span><span class="sxs-lookup"><span data-stu-id="46fde-130">Remote debugging</span></span>  

<span data-ttu-id="46fde-131">Consulta la información de reproductores multimedia en un dispositivo Android desde tu equipo Windows o macOS.</span><span class="sxs-lookup"><span data-stu-id="46fde-131">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="46fde-132">Para configurar la depuración remota, vaya a [Introducción a la depuración remota de dispositivos Android.][DevtoolsGuideChromiumRemoteDebuggingIndex]</span><span class="sxs-lookup"><span data-stu-id="46fde-132">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="46fde-133">Ver la información de reproductores multimedia de forma remota.</span><span class="sxs-lookup"><span data-stu-id="46fde-133">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a><span data-ttu-id="46fde-134">Ocultar y mostrar reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-134">Hide and show media players</span></span>  

<span data-ttu-id="46fde-135">A veces, ejecutas más de un reproductor multimedia en una página web o usas la misma pestaña del explorador para explorar diferentes páginas web, cada una con reproductores multimedia.</span><span class="sxs-lookup"><span data-stu-id="46fde-135">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="46fde-136">Puede elegir ocultar \(o mostrar\) cada reproductor multimedia para una experiencia de depuración más sencilla.</span><span class="sxs-lookup"><span data-stu-id="46fde-136">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="46fde-137">Vaya a varias páginas web de vídeo diferentes con la misma pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="46fde-137">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="46fde-138">Para ocultar reproductores multimedia, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="46fde-138">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="46fde-139">Para ocultar un reproductor multimedia, mantenga el mouse en un reproductor multimedia, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Ocultar reproductor**.</span><span class="sxs-lookup"><span data-stu-id="46fde-139">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="46fde-140">Para ocultar todos los demás reproductores multimedia, mantenga el mouse en un reproductor multimedia, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Ocultar todos los demás**.</span><span class="sxs-lookup"><span data-stu-id="46fde-140">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ocultar reproductores multimedia" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="46fde-142">Ocultar reproductores multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-142">Hide media players</span></span>  
    :::image-end:::  
    
## <a name="export-media-player-information"></a><span data-ttu-id="46fde-143">Exportar información del reproductor multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-143">Export media player information</span></span>  

1.  <span data-ttu-id="46fde-144">Para descargar la información del reproductor multimedia como un archivo JSON, mantenga el mouse en un reproductor multimedia, abra el menú contextual \(clic con el botón secundario\) y elija **Guardar información del reproductor**.</span><span class="sxs-lookup"><span data-stu-id="46fde-144">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportar información multimedia" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="46fde-146">Exportar información multimedia</span><span class="sxs-lookup"><span data-stu-id="46fde-146">Export media information</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="46fde-147">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="46fde-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximización de la productividad con las herramientas para desarrolladores perimetrales | Bing Vídeo"  

> [!NOTE]
> <span data-ttu-id="46fde-151">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46fde-151">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="46fde-152">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="46fde-152">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="46fde-154">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46fde-154">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

