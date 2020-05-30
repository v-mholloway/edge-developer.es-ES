---
title: Buscar y solucionar problemas con la herramienta problemas de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 394ea0e831e3b60a60a149d1281c5cca382a887d
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688132"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="c0df4-103">Buscar y solucionar problemas con la herramienta problemas de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c0df4-103">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>   



<span data-ttu-id="c0df4-104">La herramienta **problemas** de Microsoft Edge DevTools reduce la fatiga de las notificaciones y el desorden de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="c0df4-104">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="c0df4-105">Utilícelo para buscar soluciones a problemas detectados por el explorador, como problemas de cookies y contenido mixto.</span><span class="sxs-lookup"><span data-stu-id="c0df4-105">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="c0df4-106">En Microsoft Edge 84, la herramienta **problemas** admite tres tipos de problemas:</span><span class="sxs-lookup"><span data-stu-id="c0df4-106">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="c0df4-107">Problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="c0df4-107">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="c0df4-108">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="c0df4-108">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="c0df4-109">Problemas de COEP</span><span class="sxs-lookup"><span data-stu-id="c0df4-109">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="c0df4-110">El equipo de Microsoft Edge DevTools planea admitir más tipos de problemas en futuras versiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0df4-110">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="c0df4-111">Abrir la herramienta problemas en el cajón de DevTools</span><span class="sxs-lookup"><span data-stu-id="c0df4-111">Open the Issues tool in the DevTools drawer</span></span>   

1.  <span data-ttu-id="c0df4-112">Visite una página, como [SameSite-Sandbox.Glitch.me][GlitchSamesiteSandbox], que contiene problemas para corregir.</span><span class="sxs-lookup"><span data-stu-id="c0df4-112">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="c0df4-113">[Abra DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="c0df4-113">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="c0df4-114">Seleccione el botón **ir a problemas** de la barra de advertencia amarilla.</span><span class="sxs-lookup"><span data-stu-id="c0df4-114">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Botón ir a problemas de la barra de advertencia amarilla cuando se detectan problemas" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="c0df4-116">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="c0df4-116">Figure 1.</span></span>  <span data-ttu-id="c0df4-117">El botón **ir a problemas** de la barra de advertencia amarilla cuando se detectan problemas.</span><span class="sxs-lookup"><span data-stu-id="c0df4-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="c0df4-118">También puede seleccionar **problemas** en el menú **más herramientas** .</span><span class="sxs-lookup"><span data-stu-id="c0df4-118">Alternatively, select **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Herramienta problemas en el menú más herramientas" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="c0df4-120">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="c0df4-120">Figure 2.</span></span>  <span data-ttu-id="c0df4-121">Herramienta **problemas** en el menú **más herramientas**</span><span class="sxs-lookup"><span data-stu-id="c0df4-121">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="c0df4-122">Seleccione el botón **volver a cargar la página** , si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c0df4-122">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Herramienta problemas del cajón de DevTools con el botón volver a cargar página" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="c0df4-124">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="c0df4-124">Figure 3.</span></span>  <span data-ttu-id="c0df4-125">Herramienta **problemas** del cajón de DevTools con el botón **volver a cargar página**</span><span class="sxs-lookup"><span data-stu-id="c0df4-125">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="c0df4-126">Los problemas notificados en la **consola** son difíciles de comprender, como las advertencias de cookie en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="c0df4-126">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="c0df4-127">En función de los problemas que se hayan informado, es posible que no tenga claro lo que debe hacer.</span><span class="sxs-lookup"><span data-stu-id="c0df4-127">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Herramienta problemas en el cajón de DevTools con tres problemas de cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="c0df4-129">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="c0df4-129">Figure 4.</span></span>  <span data-ttu-id="c0df4-130">Herramienta **problemas** en el cajón de DevTools con tres problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="c0df4-130">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c0df4-131">Ver los elementos de la herramienta problemas</span><span class="sxs-lookup"><span data-stu-id="c0df4-131">View items in the Issues tool</span></span>   

<span data-ttu-id="c0df4-132">La herramienta **problemas** del alimentador de DevTools presenta advertencias en una forma estructurada, agregada y que se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="c0df4-132">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="c0df4-133">Seleccione un elemento de la herramienta **problemas** para obtener información sobre cómo corregir el problema y encontrar los recursos afectados.</span><span class="sxs-lookup"><span data-stu-id="c0df4-133">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar las cookies entre sitios como un problema seguro abierto en la herramienta problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="c0df4-135">Figura 5.</span><span class="sxs-lookup"><span data-stu-id="c0df4-135">Figure 5.</span></span>  <span data-ttu-id="c0df4-136">**Marcar las cookies entre sitios como** un problema seguro abierto en la herramienta **problemas**</span><span class="sxs-lookup"><span data-stu-id="c0df4-136">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="c0df4-137">Cada elemento tiene cuatro componentes:</span><span class="sxs-lookup"><span data-stu-id="c0df4-137">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="c0df4-138">Un titular que describe el problema.</span><span class="sxs-lookup"><span data-stu-id="c0df4-138">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="c0df4-139">Descripción que proporciona el contexto y la solución.</span><span class="sxs-lookup"><span data-stu-id="c0df4-139">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="c0df4-140">Una sección de **recursos afectados** con vínculos a recursos dentro del contexto de DevTools adecuado, como el panel red.</span><span class="sxs-lookup"><span data-stu-id="c0df4-140">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="c0df4-141">Vínculos a más instrucciones.</span><span class="sxs-lookup"><span data-stu-id="c0df4-141">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="c0df4-142">Seleccione los elementos de **recursos afectados** para ver los detalles.</span><span class="sxs-lookup"><span data-stu-id="c0df4-142">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="c0df4-143">En el siguiente ejemplo, la **marca de las cookies entre sitios como** un problema seguro afecta a una cookie y a dos solicitudes.</span><span class="sxs-lookup"><span data-stu-id="c0df4-143">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afectados abiertos en la pestaña "problemas"" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="c0df4-145">Figura 6.</span><span class="sxs-lookup"><span data-stu-id="c0df4-145">Figure 6.</span></span>  <span data-ttu-id="c0df4-146">Recursos afectados abiertos en la herramienta **problemas** del cajón de DevTools</span><span class="sxs-lookup"><span data-stu-id="c0df4-146">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c0df4-147">Ver problemas en contexto</span><span class="sxs-lookup"><span data-stu-id="c0df4-147">View issues in context</span></span>   

1.  <span data-ttu-id="c0df4-148">Seleccione un vínculo de recursos para ver el elemento en el contexto adecuado dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0df4-148">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="c0df4-149">En el ejemplo siguiente, seleccione `samesite-sandbox.glitch.me` en **solicitudes** para mostrar las cookies adjuntas a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0df4-149">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Ver la cookie afectada en el panel de red DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="c0df4-151">Figura 7.</span><span class="sxs-lookup"><span data-stu-id="c0df4-151">Figure 7.</span></span>  <span data-ttu-id="c0df4-152">Ver la cookie afectada en el panel de red DevTools</span><span class="sxs-lookup"><span data-stu-id="c0df4-152">View the affected cookie in the DevTools Network panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="c0df4-153">Desplácese para ver el elemento con un problema: en el ejemplo siguiente, la `ck02` cookie.</span><span class="sxs-lookup"><span data-stu-id="c0df4-153">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="c0df4-154">Desplace el puntero sobre la columna **SameSite** para ver el `None` valor detectado por el problema.</span><span class="sxs-lookup"><span data-stu-id="c0df4-154">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Valor NONE en la columna SameSite de la cookie CK02 en el panel DevTools red" lightbox="../media/issues-tab-view-issue.msft.png":::
       <span data-ttu-id="c0df4-156">Figura 8.</span><span class="sxs-lookup"><span data-stu-id="c0df4-156">Figure 8.</span></span>  `None` <span data-ttu-id="c0df4-157">valor de la columna **SameSite** de la `ck02` cookie en el panel de **red** DevTools</span><span class="sxs-lookup"><span data-stu-id="c0df4-157">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

<!--## Feedback  -->  



<!-- image links -->  

<!-- links -->  

[DevtoolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools | Microsoft docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Pruebas de cookie SameSite | Intento"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenido mixto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Directiva de Embedder entre orígenes | Grupo de comunidades de la web"  

> [!NOTE]
> <span data-ttu-id="c0df4-163">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0df4-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c0df4-164">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/issues/index) y está creada por [Sam Dutton][SamDutton] \ (Defensor del desarrollador \).</span><span class="sxs-lookup"><span data-stu-id="c0df4-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c0df4-166">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0df4-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
