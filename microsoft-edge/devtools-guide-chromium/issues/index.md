---
description: Use la herramienta Problemas para buscar y solucionar problemas con su sitio web.
title: Buscar y solucionar problemas con la Microsoft Edge de problemas de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 64954d632416f7d1353269d04c1550ca7a0652b7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564185"
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
# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a><span data-ttu-id="6a014-104">Buscar y solucionar problemas con la Microsoft Edge de problemas de DevTools</span><span class="sxs-lookup"><span data-stu-id="6a014-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="6a014-105">La **herramienta Problemas** en Microsoft Edge DevTools reduce la fatiga de notificación y el desorden de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="6a014-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="6a014-106">Úselo para buscar soluciones a problemas detectados por el explorador, como problemas de cookies y contenido mixto.</span><span class="sxs-lookup"><span data-stu-id="6a014-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="6a014-107">En Microsoft Edge 84, la **herramienta Problemas** admite tres tipos de problema:</span><span class="sxs-lookup"><span data-stu-id="6a014-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="6a014-108">Problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="6a014-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="6a014-109">Contenido mixto</span><span class="sxs-lookup"><span data-stu-id="6a014-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="6a014-110">Problemas del COEP</span><span class="sxs-lookup"><span data-stu-id="6a014-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="6a014-111">El Microsoft Edge de DevTools planea admitir más tipos de problemas en versiones futuras de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6a014-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="6a014-112">Abra la herramienta Problemas en el cajón DevTools</span><span class="sxs-lookup"><span data-stu-id="6a014-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="6a014-113">Navegue a una página web, como [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], que contiene problemas que corregir.</span><span class="sxs-lookup"><span data-stu-id="6a014-113">Navigate to a webpage, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="6a014-114">[Abra DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="6a014-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="6a014-115">Elija el **botón Ir a problemas** en la barra de advertencia amarilla.</span><span class="sxs-lookup"><span data-stu-id="6a014-115">Choose the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Vaya al botón Problemas en la barra de advertencia amarilla cuando se detecten problemas" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="6a014-117">El **botón Ir a Problemas** de la barra de advertencia amarilla cuando se detectan problemas.</span><span class="sxs-lookup"><span data-stu-id="6a014-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="6a014-118">Como alternativa, elija **Problemas** en el **menú Más** herramientas.</span><span class="sxs-lookup"><span data-stu-id="6a014-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Herramienta Problemas en el menú Más herramientas" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="6a014-120">**Herramienta Problemas** en **el menú Más** herramientas</span><span class="sxs-lookup"><span data-stu-id="6a014-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="6a014-121">Elija el **botón Volver a cargar** página, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6a014-121">Choose the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Herramienta Problemas en el botón de página DevTools Drawer with Reload" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="6a014-123">**Herramienta Problemas** en el botón de página DevTools Drawer with **Reload**</span><span class="sxs-lookup"><span data-stu-id="6a014-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="6a014-124">Los problemas notificados en **la consola** son bastante difíciles de comprender, como las advertencias de cookies de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="6a014-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="6a014-125">En función de los problemas notificados, puede que no esté claro lo que debe hacer.</span><span class="sxs-lookup"><span data-stu-id="6a014-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Herramienta Problemas en el cajón de DevTools con tres problemas de cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="6a014-127">**Herramienta** Problemas en el cajón de DevTools con tres problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="6a014-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a><span data-ttu-id="6a014-128">Ver elementos en la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="6a014-128">View items in the Issues tool</span></span>  

<span data-ttu-id="6a014-129">La **herramienta Problemas** del cajón DevTools presenta advertencias de una forma estructurada, agregada y que puede actuar.</span><span class="sxs-lookup"><span data-stu-id="6a014-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="6a014-130">Elija un elemento en la **herramienta Problemas** para obtener instrucciones sobre cómo solucionar el problema y encontrar los recursos afectados.</span><span class="sxs-lookup"><span data-stu-id="6a014-130">Choose an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar las cookies entre sitios como problema seguro abierto en la herramienta Problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="6a014-132">**Marcar las cookies entre sitios como problema seguro** abierto en la herramienta **Problemas**</span><span class="sxs-lookup"><span data-stu-id="6a014-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="6a014-133">Cada elemento tiene cuatro componentes:</span><span class="sxs-lookup"><span data-stu-id="6a014-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="6a014-134">Un titular que describe el problema.</span><span class="sxs-lookup"><span data-stu-id="6a014-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="6a014-135">Una descripción que proporciona el contexto y la solución.</span><span class="sxs-lookup"><span data-stu-id="6a014-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="6a014-136">Sección **RECURSOS AFECTADOS que** vincula a recursos dentro del contexto de DevTools adecuado, como el panel Red.</span><span class="sxs-lookup"><span data-stu-id="6a014-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="6a014-137">Vínculos a más instrucciones.</span><span class="sxs-lookup"><span data-stu-id="6a014-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="6a014-138">Elija elementos en **RECURSOS AFECTADOS** para ver detalles.</span><span class="sxs-lookup"><span data-stu-id="6a014-138">Choose items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="6a014-139">En el siguiente ejemplo, el problema **Marcar las cookies entre** sitios como seguridad afecta a una cookie y dos solicitudes.</span><span class="sxs-lookup"><span data-stu-id="6a014-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afectados abiertos en la herramienta Problemas" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="6a014-141">Recursos afectados abiertos en la **herramienta Problemas** en el cajón DevTools</span><span class="sxs-lookup"><span data-stu-id="6a014-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a><span data-ttu-id="6a014-142">Ver problemas en contexto</span><span class="sxs-lookup"><span data-stu-id="6a014-142">View issues in context</span></span>  

1.  <span data-ttu-id="6a014-143">Elija un vínculo de recurso para ver el elemento en el contexto adecuado dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="6a014-143">Choose a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="6a014-144">En el ejemplo siguiente, elija `samesite-sandbox.glitch.me` en **Solicitudes** para mostrar las cookies adjuntas a esa solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a014-144">In the following example, choose `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Ver la cookie afectada en la herramienta DevTools Network" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="6a014-146">Ver la cookie afectada en la herramienta DevTools **Network**</span><span class="sxs-lookup"><span data-stu-id="6a014-146">View the affected cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="6a014-147">Desplácese para ver el elemento con un problema: para el siguiente ejemplo, la `ck02` cookie.</span><span class="sxs-lookup"><span data-stu-id="6a014-147">Scroll to view the item with a problem:  for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="6a014-148">Mantenga el mouse en **la columna SameSite** para revisar `None` el valor detectado por el problema.</span><span class="sxs-lookup"><span data-stu-id="6a014-148">Hover on the **SameSite** column to review the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Valor ninguno en la columna SameSite para la cookie de ck02 en la herramienta DevTools Network" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="6a014-150">valor de la **columna SameSite** de `ck02` la cookie en la herramienta DevTools **Network**</span><span class="sxs-lookup"><span data-stu-id="6a014-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6a014-151">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6a014-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Pruebas de cookies de SameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies de SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenido mixto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Directiva de incrustación entre orígenes | Grupo de Community web de la Community web"  

> [!NOTE]
> <span data-ttu-id="6a014-157">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a014-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6a014-158">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/issues/index) y es creado por [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="6a014-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6a014-160">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a014-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton  
