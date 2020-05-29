---
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611920"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="63dec-103">Ver recursos de página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63dec-103">View Page Resources With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="63dec-104">Esta guía le enseña cómo usar Microsoft Edge DevTools para ver los recursos de una página web.</span><span class="sxs-lookup"><span data-stu-id="63dec-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="63dec-105">Los recursos son los archivos que necesita una página para que se muestren correctamente.</span><span class="sxs-lookup"><span data-stu-id="63dec-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="63dec-106">Algunos ejemplos de recursos son los archivos CSS, JavaScript y HTML, así como las imágenes.</span><span class="sxs-lookup"><span data-stu-id="63dec-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="63dec-107">En esta guía se presupone que está familiarizado con los conceptos básicos de [desarrollo web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="63dec-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="63dec-108">Abrir recursos</span><span class="sxs-lookup"><span data-stu-id="63dec-108">Open resources</span></span>   

<span data-ttu-id="63dec-109">Cuando conoce el nombre del recurso que quiere inspeccionar, el **menú de comandos** proporciona una forma rápida de abrir el recurso.</span><span class="sxs-lookup"><span data-stu-id="63dec-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="63dec-110">Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="63dec-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="63dec-111">Se abrirá el cuadro de diálogo **Abrir archivo** .</span><span class="sxs-lookup"><span data-stu-id="63dec-111">The **Open File** dialog opens.</span></span>  
    
    > ##### <span data-ttu-id="63dec-112">Figura 1</span><span class="sxs-lookup"><span data-stu-id="63dec-112">Figure 1</span></span>  
    > <span data-ttu-id="63dec-113">Cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="63dec-113">The **Open File** dialog</span></span>  
    > ![Cuadro de diálogo Abrir archivo][ImageOpenFile]  
    
1.  <span data-ttu-id="63dec-115">Seleccione el archivo de la lista desplegable o empiece a escribir el nombre de archivo y presione `Enter` una vez que el archivo correcto esté resaltado en el cuadro Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="63dec-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    > ##### <span data-ttu-id="63dec-116">Figura 2</span><span class="sxs-lookup"><span data-stu-id="63dec-116">Figure 2</span></span>  
    > <span data-ttu-id="63dec-117">Escribir un nombre de archivo en el cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="63dec-117">Typing a filename in the **Open File** dialog</span></span>  
    > ![Escribir un nombre de archivo en el cuadro de diálogo Abrir archivo][ImageFileSearch]  
    
### <span data-ttu-id="63dec-119">Abrir recursos en el panel red</span><span class="sxs-lookup"><span data-stu-id="63dec-119">Open resources in the Network panel</span></span>   

<span data-ttu-id="63dec-120">Consulte [inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="63dec-120">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

> ##### <span data-ttu-id="63dec-121">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="63dec-121">Figure 3</span></span>  
> <span data-ttu-id="63dec-122">Inspeccionar un recurso en el panel red</span><span class="sxs-lookup"><span data-stu-id="63dec-122">Inspecting a resource in the Network panel</span></span>  
> ![Inspeccionar un recurso en el panel red][ImageNetworkResponse]  

### <span data-ttu-id="63dec-124">Mostrar recursos en el panel de red de otros paneles</span><span class="sxs-lookup"><span data-stu-id="63dec-124">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="63dec-125">En la sección [examinar recursos](#browse-resources) que se muestra a continuación se muestra cómo ver los recursos de varias partes de la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="63dec-125">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="63dec-126">Si alguna vez desea inspeccionar un recurso en el panel **red** , haga clic con el botón derecho en el recurso y seleccione **Mostrar en el panel de red**.</span><span class="sxs-lookup"><span data-stu-id="63dec-126">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

> ##### <span data-ttu-id="63dec-127">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="63dec-127">Figure 4</span></span>  
> <span data-ttu-id="63dec-128">Opción **Mostrar en el panel red**</span><span class="sxs-lookup"><span data-stu-id="63dec-128">The **Reveal in Network panel** option</span></span>  
> ![Mostrar en el panel red][ImageRevealNetwork]  

## <span data-ttu-id="63dec-130">Examinar recursos</span><span class="sxs-lookup"><span data-stu-id="63dec-130">Browse resources</span></span>   

### <span data-ttu-id="63dec-131">Examinar recursos en el panel red</span><span class="sxs-lookup"><span data-stu-id="63dec-131">Browse resources in the Network panel</span></span>   

<span data-ttu-id="63dec-132">Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="63dec-132">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

> ##### <span data-ttu-id="63dec-133">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="63dec-133">Figure 5</span></span>  
> <span data-ttu-id="63dec-134">Recursos de página en el registro de red</span><span class="sxs-lookup"><span data-stu-id="63dec-134">Page resources in the Network Log</span></span>  
> ![Recursos de página en el registro de red][ImageNetworkLog]  

### <span data-ttu-id="63dec-136">Examinar por directorio</span><span class="sxs-lookup"><span data-stu-id="63dec-136">Browse by directory</span></span>   

<span data-ttu-id="63dec-137">Para ver los recursos de una página organizada por directorio:</span><span class="sxs-lookup"><span data-stu-id="63dec-137">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="63dec-138">Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="63dec-138">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="63dec-139">Haga clic en la pestaña de la **Página** para mostrar los recursos de la página.</span><span class="sxs-lookup"><span data-stu-id="63dec-139">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="63dec-140">Se abre el panel de **páginas** .</span><span class="sxs-lookup"><span data-stu-id="63dec-140">The **Page** pane opens.</span></span>  
    
    > ##### <span data-ttu-id="63dec-141">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="63dec-141">Figure 6</span></span>  
    > <span data-ttu-id="63dec-142">El panel de **páginas**</span><span class="sxs-lookup"><span data-stu-id="63dec-142">The **Page** pane</span></span>  
    > ![El panel de páginas][ImagePage]  
    
    <span data-ttu-id="63dec-144">A continuación se muestra un desglose de los elementos no obvios de la [Ilustración 6](#figure-6):</span><span class="sxs-lookup"><span data-stu-id="63dec-144">Here is a breakdown of the non-obvious items in [Figure 6](#figure-6):</span></span>  
    
    | <span data-ttu-id="63dec-145">Elemento de página</span><span class="sxs-lookup"><span data-stu-id="63dec-145">Page item</span></span> | <span data-ttu-id="63dec-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="63dec-146">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="63dec-147">[Contexto de examen][MDNInlineFrame]de documento principal.</span><span class="sxs-lookup"><span data-stu-id="63dec-147">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="63dec-148">El dominio.</span><span class="sxs-lookup"><span data-stu-id="63dec-148">The domain.</span></span>  <span data-ttu-id="63dec-149">Todos los recursos anidados en él provienen de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="63dec-149">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="63dec-150">Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="63dec-150">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="63dec-151">Un directorio.</span><span class="sxs-lookup"><span data-stu-id="63dec-151">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="63dec-152">Documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="63dec-152">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="63dec-153">Contexto en tiempo de ejecución de un trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="63dec-153">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="63dec-154">Haga clic en un recurso para verlo en el **Editor**.</span><span class="sxs-lookup"><span data-stu-id="63dec-154">Click a resource to view it in the **Editor**.</span></span>  
    
    > ##### <span data-ttu-id="63dec-155">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="63dec-155">Figure 7</span></span>  
    > <span data-ttu-id="63dec-156">Ver un archivo en el **Editor**</span><span class="sxs-lookup"><span data-stu-id="63dec-156">Viewing a file in the **Editor**</span></span>  
    > ![Ver un archivo en el editor][ImageSourcesView]  
    
### <span data-ttu-id="63dec-158">Examinar por nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="63dec-158">Browse by filename</span></span>   

<span data-ttu-id="63dec-159">De forma predeterminada, el panel de **páginas** agrupa los recursos por directorio.</span><span class="sxs-lookup"><span data-stu-id="63dec-159">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="63dec-160">Para deshabilitar esta agrupación y ver los recursos de cada dominio como una lista plana:</span><span class="sxs-lookup"><span data-stu-id="63dec-160">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="63dec-161">Abra el panel de **páginas** .</span><span class="sxs-lookup"><span data-stu-id="63dec-161">Open the **Page** pane.</span></span>  <span data-ttu-id="63dec-162">Consulte [examinar por directorio](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="63dec-162">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="63dec-163">Haga clic en **más opciones** `...` y deshabilite **Agrupar por carpeta**.</span><span class="sxs-lookup"><span data-stu-id="63dec-163">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    > ##### <span data-ttu-id="63dec-164">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="63dec-164">Figure 8</span></span>  
    > <span data-ttu-id="63dec-165">La opción **Agrupar por carpeta**</span><span class="sxs-lookup"><span data-stu-id="63dec-165">The **Group By Folder** option</span></span>  
    > ![La opción agrupar por carpeta][ImageGroupByFolder]  
    
    <span data-ttu-id="63dec-167">Los recursos están organizados por tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="63dec-167">Resources are organized by file type.</span></span>  <span data-ttu-id="63dec-168">Dentro de cada tipo de archivo, los recursos están organizados alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="63dec-168">Within each file type the resources are organized alphabetically.</span></span>  
    
    > ##### <span data-ttu-id="63dec-169">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="63dec-169">Figure 9</span></span>  
    > <span data-ttu-id="63dec-170">El panel de **páginas** después de deshabilitar **Agrupar por carpeta**</span><span class="sxs-lookup"><span data-stu-id="63dec-170">The **Page** pane after disabling **Group By Folder**</span></span>  
    > ![El panel de páginas después de deshabilitar agrupar por carpeta][ImageFileNames]  
    
### <span data-ttu-id="63dec-172">Examinar por tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="63dec-172">Browse by file type</span></span>   

<span data-ttu-id="63dec-173">Para agrupar recursos en función de su tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="63dec-173">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="63dec-174">Haga clic en la pestaña **aplicación** .  Se abre el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="63dec-174">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="63dec-175">De forma predeterminada, el panel **manifiesto** generalmente se abre en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="63dec-175">By default the **Manifest** pane usually opens first.</span></span>  
    
    > ##### <span data-ttu-id="63dec-176">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="63dec-176">Figure 10</span></span>  
    > <span data-ttu-id="63dec-177">El panel de **aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="63dec-177">The **Application** panel</span></span>  
    > ![El panel de aplicaciones][ImageApplication]  
    
1.  <span data-ttu-id="63dec-179">Desplácese hacia abajo hasta el panel **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="63dec-179">Scroll down to the **Frames** pane.</span></span>  
    
    > ##### <span data-ttu-id="63dec-180">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="63dec-180">Figure 11</span></span>  
    > <span data-ttu-id="63dec-181">El panel **Marcos**</span><span class="sxs-lookup"><span data-stu-id="63dec-181">The **Frames** pane</span></span>  
    > ![El panel marcos][ImageFrames]  
    
1.  <span data-ttu-id="63dec-183">Expanda las secciones en las que esté interesado.</span><span class="sxs-lookup"><span data-stu-id="63dec-183">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="63dec-184">Haga clic en un recurso para verlo.</span><span class="sxs-lookup"><span data-stu-id="63dec-184">Click a resource to view it.</span></span>  
    
    > ##### <span data-ttu-id="63dec-185">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="63dec-185">Figure 12</span></span>  
    > <span data-ttu-id="63dec-186">Ver un recurso en el panel de la **aplicación**</span><span class="sxs-lookup"><span data-stu-id="63dec-186">Viewing a resource in the **Application** panel</span></span>  
    > ![Ver un recurso en el panel de la aplicación][ImageApplicationView]  

#### <span data-ttu-id="63dec-188">Examinar archivos por tipo en el panel red</span><span class="sxs-lookup"><span data-stu-id="63dec-188">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="63dec-189">Consulte [filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="63dec-189">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

> ##### <span data-ttu-id="63dec-190">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="63dec-190">Figure 13</span></span>  
> <span data-ttu-id="63dec-191">Filtrar por CSS en el registro de red</span><span class="sxs-lookup"><span data-stu-id="63dec-191">Filtering for CSS in the Network Log</span></span>  
> ![Filtrar por CSS en el registro de red][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Ilustración 1: el cuadro de diálogo Abrir archivo"  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Ilustración 2: escribir un nombre de archivo en el cuadro de diálogo Abrir archivo"  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Ilustración 3: inspección de un recurso en el panel * * red * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Ilustración 4: Mostrar en el panel red"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Ilustración 5: recursos de página en el registro de red"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Ilustración 6: el panel de páginas"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Ilustración 7: visualización de un archivo en el editor"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Ilustración 8: opción Group by Folder"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Ilustración 9: el panel de páginas después de deshabilitar agrupar por carpeta"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Ilustración 10: el panel de la aplicación"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Ilustración 11: el panel marcos"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Ilustración 12: visualización de un recurso en el panel de aplicaciones"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Ilustración 13: filtrar por CSS en el registro de red"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Filtrar por tipo de recurso-comprobar actividad de red en Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Comprobar los detalles de la actividad de red inspeccionar recursos en Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red: inspeccionar actividad de red en Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> iframe: el elemento marco alineado | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprenda el desarrollo web | MDN"  

> [!NOTE]
> <span data-ttu-id="63dec-212">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63dec-212">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63dec-213">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="63dec-213">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="63dec-215">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63dec-215">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
