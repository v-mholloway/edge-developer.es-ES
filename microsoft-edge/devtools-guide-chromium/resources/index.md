---
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4265841501bdd74d2976ecab1c2a07f1fb215535
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984475"
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





# <span data-ttu-id="06b58-103">Ver recursos de página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="06b58-103">View page resources with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="06b58-104">Esta guía le enseña cómo usar Microsoft Edge DevTools para ver los recursos de una página web.</span><span class="sxs-lookup"><span data-stu-id="06b58-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="06b58-105">Los recursos son los archivos que necesita una página para que se muestren correctamente.</span><span class="sxs-lookup"><span data-stu-id="06b58-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="06b58-106">Algunos ejemplos de recursos son los archivos CSS, JavaScript y HTML, así como las imágenes.</span><span class="sxs-lookup"><span data-stu-id="06b58-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="06b58-107">En esta guía se presupone que está familiarizado con los conceptos básicos de [desarrollo web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="06b58-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="06b58-108">Abrir recursos</span><span class="sxs-lookup"><span data-stu-id="06b58-108">Open resources</span></span>   

<span data-ttu-id="06b58-109">Cuando conoce el nombre del recurso que quiere inspeccionar, el **menú de comandos** proporciona una forma rápida de abrir el recurso.</span><span class="sxs-lookup"><span data-stu-id="06b58-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="06b58-110">Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="06b58-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="06b58-111">Se abrirá el cuadro de diálogo **Abrir archivo** .</span><span class="sxs-lookup"><span data-stu-id="06b58-111">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="06b58-113">Cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="06b58-113">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="06b58-114">Seleccione el archivo de la lista desplegable o empiece a escribir el nombre de archivo y presione `Enter` una vez que el archivo correcto esté resaltado en el cuadro Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="06b58-114">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Escribir un nombre de archivo en el cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="06b58-116">Escribir un nombre de archivo en el cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="06b58-116">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="06b58-117">Abrir recursos en el panel red</span><span class="sxs-lookup"><span data-stu-id="06b58-117">Open resources in the Network panel</span></span>   

<span data-ttu-id="06b58-118">Consulte [inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="06b58-118">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspeccionar un recurso en el panel red" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="06b58-120">Inspeccionar un recurso en el panel **red**</span><span class="sxs-lookup"><span data-stu-id="06b58-120">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="06b58-121">Mostrar recursos en el panel de red de otros paneles</span><span class="sxs-lookup"><span data-stu-id="06b58-121">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="06b58-122">En la sección [examinar recursos](#browse-resources) que se muestra a continuación se muestra cómo ver los recursos de varias partes de la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="06b58-122">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="06b58-123">Si alguna vez desea inspeccionar un recurso en el panel **red** , haga clic con el botón derecho en el recurso y seleccione **Mostrar en el panel de red**.</span><span class="sxs-lookup"><span data-stu-id="06b58-123">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Mostrar en el panel red" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="06b58-125">Mostrar en el panel red</span><span class="sxs-lookup"><span data-stu-id="06b58-125">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="06b58-126">Examinar recursos</span><span class="sxs-lookup"><span data-stu-id="06b58-126">Browse resources</span></span>   

### <span data-ttu-id="06b58-127">Examinar recursos en el panel red</span><span class="sxs-lookup"><span data-stu-id="06b58-127">Browse resources in the Network panel</span></span>   

<span data-ttu-id="06b58-128">Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="06b58-128">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página en el registro de red" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="06b58-130">Recursos de página en el registro de **red**</span><span class="sxs-lookup"><span data-stu-id="06b58-130">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="06b58-131">Examinar por directorio</span><span class="sxs-lookup"><span data-stu-id="06b58-131">Browse by directory</span></span>   

<span data-ttu-id="06b58-132">Para ver los recursos de una página organizada por directorio:</span><span class="sxs-lookup"><span data-stu-id="06b58-132">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="06b58-133">Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="06b58-133">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="06b58-134">Haga clic en la pestaña de la **Página** para mostrar los recursos de la página.</span><span class="sxs-lookup"><span data-stu-id="06b58-134">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="06b58-135">Se abre el panel de **páginas** .</span><span class="sxs-lookup"><span data-stu-id="06b58-135">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="El panel de páginas" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="06b58-137">El panel de **páginas**</span><span class="sxs-lookup"><span data-stu-id="06b58-137">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="06b58-138">Este es un desglose de los elementos no obvios de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="06b58-138">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="06b58-139">Elemento de página</span><span class="sxs-lookup"><span data-stu-id="06b58-139">Page item</span></span> | <span data-ttu-id="06b58-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="06b58-140">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="06b58-141">[Contexto de examen][MDNInlineFrame]de documento principal.</span><span class="sxs-lookup"><span data-stu-id="06b58-141">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="06b58-142">El dominio.</span><span class="sxs-lookup"><span data-stu-id="06b58-142">The domain.</span></span>  <span data-ttu-id="06b58-143">Todos los recursos anidados en él provienen de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="06b58-143">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="06b58-144">Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="06b58-144">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="06b58-145">Un directorio.</span><span class="sxs-lookup"><span data-stu-id="06b58-145">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="06b58-146">Documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="06b58-146">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="06b58-147">Contexto en tiempo de ejecución de un trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="06b58-147">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="06b58-148">Haga clic en un recurso para verlo en el **Editor**.</span><span class="sxs-lookup"><span data-stu-id="06b58-148">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Ver un archivo en el editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="06b58-150">Ver un archivo en el **Editor**</span><span class="sxs-lookup"><span data-stu-id="06b58-150">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="06b58-151">Examinar por nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="06b58-151">Browse by filename</span></span>   

<span data-ttu-id="06b58-152">De forma predeterminada, el panel de **páginas** agrupa los recursos por directorio.</span><span class="sxs-lookup"><span data-stu-id="06b58-152">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="06b58-153">Para deshabilitar esta agrupación y ver los recursos de cada dominio como una lista plana:</span><span class="sxs-lookup"><span data-stu-id="06b58-153">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="06b58-154">Abra el panel de **páginas** .</span><span class="sxs-lookup"><span data-stu-id="06b58-154">Open the **Page** pane.</span></span>  <span data-ttu-id="06b58-155">Consulte [examinar por directorio](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="06b58-155">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="06b58-156">Haga clic en **más opciones** `...` y deshabilite **Agrupar por carpeta**.</span><span class="sxs-lookup"><span data-stu-id="06b58-156">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="La opción agrupar por carpeta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="06b58-158">La opción **Agrupar por carpeta**</span><span class="sxs-lookup"><span data-stu-id="06b58-158">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="06b58-159">Los recursos están organizados por tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="06b58-159">Resources are organized by file type.</span></span>  <span data-ttu-id="06b58-160">Dentro de cada tipo de archivo, los recursos están organizados alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="06b58-160">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="El panel de páginas después de deshabilitar agrupar por carpeta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="06b58-162">El panel de **páginas** después de deshabilitar **Agrupar por carpeta**</span><span class="sxs-lookup"><span data-stu-id="06b58-162">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="06b58-163">Examinar por tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="06b58-163">Browse by file type</span></span>   

<span data-ttu-id="06b58-164">Para agrupar recursos en función de su tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="06b58-164">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="06b58-165">Haga clic en la pestaña **aplicación** .  Se abre el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="06b58-165">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="06b58-166">De forma predeterminada, el panel **manifiesto** generalmente se abre en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="06b58-166">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="El panel de aplicaciones" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="06b58-168">El panel de **aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="06b58-168">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="06b58-169">Desplácese hacia abajo hasta el panel **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="06b58-169">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="El panel marcos" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="06b58-171">El panel **Marcos**</span><span class="sxs-lookup"><span data-stu-id="06b58-171">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="06b58-172">Expanda las secciones en las que esté interesado.</span><span class="sxs-lookup"><span data-stu-id="06b58-172">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="06b58-173">Haga clic en un recurso para verlo.</span><span class="sxs-lookup"><span data-stu-id="06b58-173">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Ver un recurso en el panel de aplicaciones" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="06b58-175">Ver un recurso en el panel de **aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="06b58-175">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="06b58-176">Examinar archivos por tipo en el panel red</span><span class="sxs-lookup"><span data-stu-id="06b58-176">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="06b58-177">Consulte [filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="06b58-177">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar por CSS en el registro de red" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="06b58-179">Filtrar por CSS en el registro de **red**</span><span class="sxs-lookup"><span data-stu-id="06b58-179">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso-comprobar actividad de red en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Revise los detalles de la actividad de red inspeccionar recursos en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Registrar actividad de red: inspeccionar actividad de red en Microsoft Edge DevTools | Microsoft docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> iframe: el elemento marco alineado | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprenda el desarrollo web | MDN"  

> [!NOTE]
> <span data-ttu-id="06b58-186">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06b58-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="06b58-187">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="06b58-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="06b58-189">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06b58-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
