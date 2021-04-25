---
description: Organice los recursos por marco, dominio, tipo u otros criterios.
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 818b93c1c07a93baa8972a530871d20446fd687f
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519446"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a><span data-ttu-id="9cfb6-104">Ver recursos de página con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9cfb6-104">View page resources with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="9cfb6-105">Esta guía le enseña a usar Microsoft Edge DevTools para ver los recursos de una página web.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="9cfb6-106">Los recursos son los archivos que necesita una página para mostrarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="9cfb6-107">Algunos ejemplos de recursos incluyen archivos CSS, JavaScript y HTML, así como imágenes.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="9cfb6-108">En esta guía se supone que está familiarizado con los conceptos básicos del desarrollo [web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-resources"></a><span data-ttu-id="9cfb6-109">Recursos abiertos</span><span class="sxs-lookup"><span data-stu-id="9cfb6-109">Open resources</span></span>  

<span data-ttu-id="9cfb6-110">Cuando conoce el nombre del recurso que desea inspeccionar, el menú **comando** proporciona una forma rápida de abrir el recurso.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="9cfb6-111">Seleccione `Control` + `P` \(Windows, Linux\) o `Command` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9cfb6-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="9cfb6-112">Se **abre el cuadro de diálogo** Abrir archivo.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="9cfb6-114">Cuadro **de diálogo Abrir** archivo</span><span class="sxs-lookup"><span data-stu-id="9cfb6-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9cfb6-115">Elija el archivo en el desplegable o empiece a escribir el nombre de archivo y seleccione una vez que el archivo correcto esté `Enter` resaltado en el cuadro autocompletar.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-115">Choose the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Escriba un nombre de archivo en el cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="9cfb6-117">Escriba un nombre de archivo en el **cuadro de diálogo Abrir** archivo</span><span class="sxs-lookup"><span data-stu-id="9cfb6-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a><span data-ttu-id="9cfb6-118">Abrir recursos en la herramienta Red</span><span class="sxs-lookup"><span data-stu-id="9cfb6-118">Open resources in the Network tool</span></span>  

<span data-ttu-id="9cfb6-119">Vaya a [Inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspeccionar un recurso en la herramienta Red" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="9cfb6-121">Inspeccionar un recurso en la **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-121">Inspect a resource in the **Network** tool</span></span>  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a><span data-ttu-id="9cfb6-122">Mostrar recursos de la herramienta Red desde otros paneles</span><span class="sxs-lookup"><span data-stu-id="9cfb6-122">Reveal resources in the Network tool from other panels</span></span>  

<span data-ttu-id="9cfb6-123">La [sección Examinar recursos](#browse-resources) siguiente muestra cómo ver recursos de varias partes de la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="9cfb6-124">Si alguna vez desea inspeccionar \*\*\*\* un recurso en la herramienta Red, mantenga el mouse en el recurso, abra el menú contextual \(clic con el botón secundario\) y elija Mostrar en el **panel Red**.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-124">If you ever want to inspect a resource in the **Network** tool,  hover on the resource, open the contextual menu \(right-click\), and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Mostrar en el panel Red" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="9cfb6-126">Mostrar en el panel Red</span><span class="sxs-lookup"><span data-stu-id="9cfb6-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <a name="browse-resources"></a><span data-ttu-id="9cfb6-127">Examinar recursos</span><span class="sxs-lookup"><span data-stu-id="9cfb6-127">Browse resources</span></span>  

### <a name="browse-resources-in-the-network-panel"></a><span data-ttu-id="9cfb6-128">Examinar recursos en el panel Red</span><span class="sxs-lookup"><span data-stu-id="9cfb6-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="9cfb6-129">Vaya a [Registrar actividad de red][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página en el registro de red" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="9cfb6-131">Recursos de página en el **registro de** red</span><span class="sxs-lookup"><span data-stu-id="9cfb6-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <a name="browse-by-directory"></a><span data-ttu-id="9cfb6-132">Examinar por directorio</span><span class="sxs-lookup"><span data-stu-id="9cfb6-132">Browse by directory</span></span>  

<span data-ttu-id="9cfb6-133">Para ver los recursos de una página web organizada por directorio:</span><span class="sxs-lookup"><span data-stu-id="9cfb6-133">To view the resources of a webpage organized by directory:</span></span>  

1.  <span data-ttu-id="9cfb6-134">Abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-134">Open DevTools.</span></span>
1.  <span data-ttu-id="9cfb6-135">Elija la **herramienta Orígenes** y, a continuación, en el **panel** Navegador de la parte superior izquierda, elija la **pestaña** Página.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-135">Choose the **Sources** tool, and then in the **Navigator** pane in the upper left, choose the **Page** tab.</span></span>
1.  <span data-ttu-id="9cfb6-136">Elija el **botón Más opciones** (...) a la derecha de la pestaña **Página** y, a continuación, elija Agrupar **por carpeta**.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-136">Choose the **More options** (...) button to the right of the **Page** tab, and then choose **Group by folder**.</span></span>
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="La pestaña Página del panel Navegador de la herramienta Orígenes" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="9cfb6-138">La **pestaña Página** del panel **Navegador** de la herramienta **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-138">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="9cfb6-139">Este es un desglose de los elementos no obvios de la figura anterior.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="9cfb6-140">Elemento de página</span><span class="sxs-lookup"><span data-stu-id="9cfb6-140">Page item</span></span> | <span data-ttu-id="9cfb6-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cfb6-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="9cfb6-142">El contexto de [exploración del documento principal][MDNInlineFrame].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="9cfb6-143">El dominio.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-143">The domain.</span></span>  <span data-ttu-id="9cfb6-144">Todos los recursos anidados en él proceden de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="9cfb6-145">Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="9cfb6-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="9cfb6-146">Un directorio.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="9cfb6-147">El documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="9cfb6-148">Contexto de tiempo de ejecución de un trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="9cfb6-149">Elija un recurso para verlo en el **Editor**.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-149">Choose a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Ver un archivo en el Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="9cfb6-151">Ver un archivo en el **Editor**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-filename"></a><span data-ttu-id="9cfb6-152">Examinar por nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="9cfb6-152">Browse by filename</span></span>  

<span data-ttu-id="9cfb6-153">De forma predeterminada, la pestaña **Página** agrupa los recursos por directorio.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-153">By default, the **Page** tab groups resources by directory.</span></span>  <span data-ttu-id="9cfb6-154">Para mostrar los recursos de cada dominio como una lista plana, en lugar de agruparlos por directorio:</span><span class="sxs-lookup"><span data-stu-id="9cfb6-154">To display the resources for each domain as a flat list, instead of grouping them by directory:</span></span>

1.  <span data-ttu-id="9cfb6-155">Vaya a la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-155">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="9cfb6-156">En el **panel** Navegador (a la izquierda), elija la **pestaña** Página.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-156">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="9cfb6-157">Elija **Más opciones y,** `...` a continuación, desactive la marca de verificación junto **a Grupo por carpeta**.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-157">Choose **More options** `...` and then clear the checkmark next to **Group by folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="La opción Agrupar por carpeta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="9cfb6-159">La **opción Agrupar por** carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfb6-159">The **Group by folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="9cfb6-160">Los recursos se organizan por tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-160">Resources are organized by file type.</span></span>  <span data-ttu-id="9cfb6-161">Dentro de cada tipo de archivo, los recursos se organizan alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-161">Within each file type, the resources are organized alphabetically.</span></span>  

    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="La pestaña Página después de borrar la marca de verificación Grupo por carpeta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="9cfb6-163">La **pestaña Página** después de borrar la marca de verificación Grupo **por** carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfb6-163">The **Page** tab after clearing the **Group by folder** check mark</span></span>  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a><span data-ttu-id="9cfb6-164">Examinar por tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="9cfb6-164">Browse by file type</span></span>  

<span data-ttu-id="9cfb6-165">Para agrupar recursos en función de su tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="9cfb6-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="9cfb6-166">Elija la **pestaña** Aplicación.  Se **abre la herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-166">Choose the **Application** tab.  The **Application** tool opens.</span></span>  <span data-ttu-id="9cfb6-167">De forma predeterminada, **el panel** Manifiesto normalmente se abre primero.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="La herramienta Aplicación" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="9cfb6-169">La **herramienta Aplicación**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-169">The **Application** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9cfb6-170">Desplácese hacia abajo hasta el **panel Marcos.**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Panel Marcos" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="9cfb6-172">Panel **Marcos**</span><span class="sxs-lookup"><span data-stu-id="9cfb6-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9cfb6-173">Expanda las secciones en las que está interesado.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="9cfb6-174">Elija un recurso para verlo.</span><span class="sxs-lookup"><span data-stu-id="9cfb6-174">Choose a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Ver un recurso en el panel Aplicación" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="9cfb6-176">Ver un recurso en **el** panel Aplicación</span><span class="sxs-lookup"><span data-stu-id="9cfb6-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a><span data-ttu-id="9cfb6-177">Examinar archivos por tipo en el panel Red</span><span class="sxs-lookup"><span data-stu-id="9cfb6-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="9cfb6-178">Vaya a [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar para CSS en el registro de red" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="9cfb6-180">Filtrar para CSS en el registro **de** red</span><span class="sxs-lookup"><span data-stu-id="9cfb6-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9cfb6-181">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9cfb6-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspeccionar los detalles del recurso: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Actividad de red de registro: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: el elemento Frame en línea | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Información sobre desarrollo web | MDN"  

> [!NOTE]
> <span data-ttu-id="9cfb6-188">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9cfb6-189">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9cfb6-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9cfb6-191">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9cfb6-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
