---
description: Organice los recursos por marco, dominio, tipo u otros criterios.
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993593"
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





# <span data-ttu-id="49eb8-104">Ver recursos de página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49eb8-104">View page resources with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="49eb8-105">Esta guía le enseña cómo usar Microsoft Edge DevTools para ver los recursos de una página web.</span><span class="sxs-lookup"><span data-stu-id="49eb8-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="49eb8-106">Los recursos son los archivos que necesita una página para que se muestren correctamente.</span><span class="sxs-lookup"><span data-stu-id="49eb8-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="49eb8-107">Algunos ejemplos de recursos son los archivos CSS, JavaScript y HTML, así como las imágenes.</span><span class="sxs-lookup"><span data-stu-id="49eb8-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="49eb8-108">En esta guía se presupone que está familiarizado con los conceptos básicos de [desarrollo web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="49eb8-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="49eb8-109">Abrir recursos</span><span class="sxs-lookup"><span data-stu-id="49eb8-109">Open resources</span></span>   

<span data-ttu-id="49eb8-110">Cuando conoce el nombre del recurso que quiere inspeccionar, el **menú de comandos** proporciona una forma rápida de abrir el recurso.</span><span class="sxs-lookup"><span data-stu-id="49eb8-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="49eb8-111">Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="49eb8-111">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="49eb8-112">Se abrirá el cuadro de diálogo **Abrir archivo** .</span><span class="sxs-lookup"><span data-stu-id="49eb8-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="49eb8-114">Cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="49eb8-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49eb8-115">Seleccione el archivo de la lista desplegable o empiece a escribir el nombre de archivo y presione `Enter` una vez que el archivo correcto esté resaltado en el cuadro Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="49eb8-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Escribir un nombre de archivo en el cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="49eb8-117">Escribir un nombre de archivo en el cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="49eb8-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="49eb8-118">Abrir recursos en el panel red</span><span class="sxs-lookup"><span data-stu-id="49eb8-118">Open resources in the Network panel</span></span>   

<span data-ttu-id="49eb8-119">Consulte [inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="49eb8-119">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspeccionar un recurso en el panel red" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="49eb8-121">Inspeccionar un recurso en el panel **red**</span><span class="sxs-lookup"><span data-stu-id="49eb8-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="49eb8-122">Mostrar recursos en el panel de red de otros paneles</span><span class="sxs-lookup"><span data-stu-id="49eb8-122">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="49eb8-123">En la sección [examinar recursos](#browse-resources) que se muestra a continuación se muestra cómo ver los recursos de varias partes de la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="49eb8-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="49eb8-124">Si alguna vez desea inspeccionar un recurso en el panel **red** , haga clic con el botón derecho en el recurso y seleccione **Mostrar en el panel de red**.</span><span class="sxs-lookup"><span data-stu-id="49eb8-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Mostrar en el panel red" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="49eb8-126">Mostrar en el panel red</span><span class="sxs-lookup"><span data-stu-id="49eb8-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="49eb8-127">Examinar recursos</span><span class="sxs-lookup"><span data-stu-id="49eb8-127">Browse resources</span></span>   

### <span data-ttu-id="49eb8-128">Examinar recursos en el panel red</span><span class="sxs-lookup"><span data-stu-id="49eb8-128">Browse resources in the Network panel</span></span>   

<span data-ttu-id="49eb8-129">Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="49eb8-129">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página en el registro de red" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="49eb8-131">Recursos de página en el registro de **red**</span><span class="sxs-lookup"><span data-stu-id="49eb8-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="49eb8-132">Examinar por directorio</span><span class="sxs-lookup"><span data-stu-id="49eb8-132">Browse by directory</span></span>   

<span data-ttu-id="49eb8-133">Para ver los recursos de una página organizada por directorio:</span><span class="sxs-lookup"><span data-stu-id="49eb8-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="49eb8-134">Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="49eb8-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="49eb8-135">Haga clic en la pestaña de la **Página** para mostrar los recursos de la página.</span><span class="sxs-lookup"><span data-stu-id="49eb8-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="49eb8-136">Se abre el panel de **páginas** .</span><span class="sxs-lookup"><span data-stu-id="49eb8-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="El panel de páginas" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="49eb8-138">El panel de **páginas**</span><span class="sxs-lookup"><span data-stu-id="49eb8-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="49eb8-139">Este es un desglose de los elementos no obvios de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="49eb8-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="49eb8-140">Elemento de página</span><span class="sxs-lookup"><span data-stu-id="49eb8-140">Page item</span></span> | <span data-ttu-id="49eb8-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="49eb8-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="49eb8-142">[Contexto de examen][MDNInlineFrame]de documento principal.</span><span class="sxs-lookup"><span data-stu-id="49eb8-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="49eb8-143">El dominio.</span><span class="sxs-lookup"><span data-stu-id="49eb8-143">The domain.</span></span>  <span data-ttu-id="49eb8-144">Todos los recursos anidados en él provienen de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="49eb8-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="49eb8-145">Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="49eb8-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="49eb8-146">Un directorio.</span><span class="sxs-lookup"><span data-stu-id="49eb8-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="49eb8-147">Documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="49eb8-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="49eb8-148">Contexto en tiempo de ejecución de un trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="49eb8-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="49eb8-149">Haga clic en un recurso para verlo en el **Editor**.</span><span class="sxs-lookup"><span data-stu-id="49eb8-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Ver un archivo en el editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="49eb8-151">Ver un archivo en el **Editor**</span><span class="sxs-lookup"><span data-stu-id="49eb8-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="49eb8-152">Examinar por nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="49eb8-152">Browse by filename</span></span>   

<span data-ttu-id="49eb8-153">De forma predeterminada, el panel de **páginas** agrupa los recursos por directorio.</span><span class="sxs-lookup"><span data-stu-id="49eb8-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="49eb8-154">Para deshabilitar esta agrupación y ver los recursos de cada dominio como una lista plana:</span><span class="sxs-lookup"><span data-stu-id="49eb8-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="49eb8-155">Abra el panel de **páginas** .</span><span class="sxs-lookup"><span data-stu-id="49eb8-155">Open the **Page** pane.</span></span>  <span data-ttu-id="49eb8-156">Consulte [examinar por directorio](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="49eb8-156">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="49eb8-157">Haga clic en **más opciones** `...` y deshabilite **Agrupar por carpeta**.</span><span class="sxs-lookup"><span data-stu-id="49eb8-157">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="La opción agrupar por carpeta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="49eb8-159">La opción **Agrupar por carpeta**</span><span class="sxs-lookup"><span data-stu-id="49eb8-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="49eb8-160">Los recursos están organizados por tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="49eb8-160">Resources are organized by file type.</span></span>  <span data-ttu-id="49eb8-161">Dentro de cada tipo de archivo, los recursos están organizados alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="49eb8-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="El panel de páginas después de deshabilitar agrupar por carpeta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="49eb8-163">El panel de **páginas** después de deshabilitar **Agrupar por carpeta**</span><span class="sxs-lookup"><span data-stu-id="49eb8-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="49eb8-164">Examinar por tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="49eb8-164">Browse by file type</span></span>   

<span data-ttu-id="49eb8-165">Para agrupar recursos en función de su tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="49eb8-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="49eb8-166">Haga clic en la pestaña **aplicación** .  Se abre el panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="49eb8-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="49eb8-167">De forma predeterminada, el panel **manifiesto** generalmente se abre en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="49eb8-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="El panel de aplicaciones" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="49eb8-169">El panel de **aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="49eb8-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49eb8-170">Desplácese hacia abajo hasta el panel **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="49eb8-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="El panel marcos" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="49eb8-172">El panel **Marcos**</span><span class="sxs-lookup"><span data-stu-id="49eb8-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49eb8-173">Expanda las secciones en las que esté interesado.</span><span class="sxs-lookup"><span data-stu-id="49eb8-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="49eb8-174">Haga clic en un recurso para verlo.</span><span class="sxs-lookup"><span data-stu-id="49eb8-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Ver un recurso en el panel de aplicaciones" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="49eb8-176">Ver un recurso en el panel de **aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="49eb8-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="49eb8-177">Examinar archivos por tipo en el panel red</span><span class="sxs-lookup"><span data-stu-id="49eb8-177">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="49eb8-178">Consulte [filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="49eb8-178">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar por CSS en el registro de red" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="49eb8-180">Filtrar por CSS en el registro de **red**</span><span class="sxs-lookup"><span data-stu-id="49eb8-180">Filter for CSS in the **Network** Log</span></span>  
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
> <span data-ttu-id="49eb8-187">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49eb8-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49eb8-188">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="49eb8-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="49eb8-190">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49eb8-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
