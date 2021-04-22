---
description: Microsoft Edge en Linux, sugerencias de webhint mejoradas en la herramienta Problemas, nuevas características de depuración de trabajo de servicio y más.
title: Novedades de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.localizationpriority: high
ms.openlocfilehash: a63515060d989a84838e4a9ba7f803184a3fc91f
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514378"
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
# <a name="whats-new-in-devtools-microsoft-edge-88"></a><span data-ttu-id="c09e6-104">Novedades de DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="c09e6-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a><span data-ttu-id="c09e6-105">Microsoft Edge y el controlador de Microsoft Edge ahora están disponibles en Linux</span><span class="sxs-lookup"><span data-stu-id="c09e6-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="c09e6-106">Microsoft Edge Dev ahora es compatible con las distribuciones Ubuntu, Debian, Fedora y openSUSE.</span><span class="sxs-lookup"><span data-stu-id="c09e6-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="c09e6-107">Descargue e instale el `.deb` de Microsoft Edge Dev o el paquete de `.rpm` directamente desde el [sitio de Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] o use las herramientas de administración de paquetes estándar de su distribución de Linux.</span><span class="sxs-lookup"><span data-stu-id="c09e6-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="c09e6-108">Si está usando un entorno Linux en sus soluciones de integración y entrega continuas \(CI/CD\), el controlador de Microsoft Edge también está disponible en Linux.</span><span class="sxs-lookup"><span data-stu-id="c09e6-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="c09e6-109">Para empezar a automatizar Microsoft Edge Dev con el controlador de Microsoft Edge, navegue a la [página de Descargas del controlador de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="c09e6-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="c09e6-110">Para obtener ayuda con la automatización de Microsoft Edge Dev junto con el controlador de Microsoft Edge, navegue a [Usar Webdriver (Chromium) para la automatización de prueba][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="c09e6-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools en Microsoft Edge en Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="c09e6-112">DevTools en Microsoft Edge en Linux</span><span class="sxs-lookup"><span data-stu-id="c09e6-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a><span data-ttu-id="c09e6-113">Sugerencias de webhint y de plataforma mejoradas en la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="c09e6-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="c09e6-114">Una herramienta de código abierto, [webhint][WebhintMain], proporciona comentarios en tiempo real para sitios web y páginas web locales.</span><span class="sxs-lookup"><span data-stu-id="c09e6-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="c09e6-115">A partir de la [versión 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], revise los comentarios de webhint en la herramienta [Problemas][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="c09e6-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="c09e6-116">Los problemas que aparecen en la herramienta **Problemas** ahora son más fáciles de revisar con la adición de las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="c09e6-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="c09e6-117">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="c09e6-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="c09e6-118">Compatibilidad</span><span class="sxs-lookup"><span data-stu-id="c09e6-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="c09e6-119">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="c09e6-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="c09e6-120">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="c09e6-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="c09e6-121">PWA</span><span class="sxs-lookup"><span data-stu-id="c09e6-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="c09e6-122">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c09e6-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="c09e6-123">Ahora puede filtrar problemas de terceros mediante una nueva casilla.</span><span class="sxs-lookup"><span data-stu-id="c09e6-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="c09e6-124">La funcionalidad de filtro le ayuda a ocultar problemas relacionados con el código de bibliotecas de terceros u otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="c09e6-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="c09e6-125">Para ayudarle a revisar los problemas que revela [webhint][WebhintMain], la herramienta **Problemas** ahora muestra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="c09e6-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="c09e6-126">Fragmentos de código mejorados.</span><span class="sxs-lookup"><span data-stu-id="c09e6-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="c09e6-127">Vínculos a otros paneles relevantes.</span><span class="sxs-lookup"><span data-stu-id="c09e6-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="c09e6-128">Vínculos a documentación para ayudarle a solucionar problemas de su sitio web.</span><span class="sxs-lookup"><span data-stu-id="c09e6-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Herramienta Problemas" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="c09e6-130">Herramienta **Problemas**</span><span class="sxs-lookup"><span data-stu-id="c09e6-130">**Issues** tool</span></span>  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a><span data-ttu-id="c09e6-131">Las Capas compuestas ahora se encuentran en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="c09e6-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="c09e6-132">Ahora puede visualizar el contenido de las **Capas** junto con los valores de índice z y el modelo de objeto de documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="c09e6-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="c09e6-133">Esta característica le ayuda a depurar sin cambiar entre la [vista 3D][Devtools3dViewIndex] y las herramientas de **Capas** con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="c09e6-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="c09e6-134">Para obtener una experiencia de depuración visual completa, [ahora se combinan la vista 3D y las Capas compuestas][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="c09e6-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="c09e6-136">Panel **Capas compuestas**</span><span class="sxs-lookup"><span data-stu-id="c09e6-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a><span data-ttu-id="c09e6-137">Definiciones de variables CSS en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="c09e6-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="c09e6-138">En el panel **Estilos**, [las variables CSS][MdnUsingCssCustomProperties] ahora se vinculan directamente a cada definición.</span><span class="sxs-lookup"><span data-stu-id="c09e6-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="c09e6-139">Elija la variable para ver o cambiar fácilmente la definición de la variable CSS.</span><span class="sxs-lookup"><span data-stu-id="c09e6-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="c09e6-140">En el ejemplo, DevTools muestra los atributos CSS para el `body` elemento.</span><span class="sxs-lookup"><span data-stu-id="c09e6-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="c09e6-141">Para mostrar la definición de variable de la variable CSS `--theme-body-background`, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-142">En el panel **Estilos**, elija `var(--theme-body-background)`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="c09e6-143">El panel **Estilos** ahora muestra la definición de la variable CSS `--theme-body-background`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variable CSS vinculada al estilo" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="c09e6-145">Variable CSS vinculada al estilo</span><span class="sxs-lookup"><span data-stu-id="c09e6-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variable CSS vinculada al destino de estilo" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="c09e6-147">Variable CSS vinculada al destino de estilo</span><span class="sxs-lookup"><span data-stu-id="c09e6-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="service-worker-debugging-improvements"></a><span data-ttu-id="c09e6-148">Mejoras en la depuración de trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="c09e6-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="c09e6-149">Las siguientes características nuevas de las herramientas [Redes](#network-tool), [Aplicaciones](#application-tool) y [Fuentes](#sources-tool) le ayudan a crear su [PWA][ProgressiveWebAppsIndex].</span><span class="sxs-lookup"><span data-stu-id="c09e6-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsIndex].</span></span>  <span data-ttu-id="c09e6-150">Use las siguientes características cuando tenga dificultades para depurar el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="c09e6-151">El enrutamiento de solicitudes muestra los eventos `startup` y `fetch` en función de las solicitudes de red que se ejecutan a través de los trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="c09e6-152">Se obtiene acceso a las escalas de tiempo desde la herramienta **Aplicación** o **Red**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="c09e6-153">Las escalas de tiempo te ayudan cuando tienes problemas con los trabajadores del servicio y quieres mostrar si hay algún problema con el `startup` o `fetch` evento.</span><span class="sxs-lookup"><span data-stu-id="c09e6-153">The timelines help when you are having trouble with service workers and want to display if something is wrong with the `startup` or `fetch` event.</span></span>  

### <a name="application-tool"></a><span data-ttu-id="c09e6-154">Herramienta Aplicación</span><span class="sxs-lookup"><span data-stu-id="c09e6-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="c09e6-155">Vea toda la información de enrutamiento de solicitud de trabajo de servicio con el nuevo vínculo **Solicitudes de red**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="c09e6-156">Para mostrar contexto adicional al depurar el trabajo de servicio, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-157">Vaya a **Aplicación** > **Trabajos de servicio**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="c09e6-158">Elija **Solicitudes de red**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abrir la herramienta Red desde el panel Trabajo de servicios" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="c09e6-160">Abrir la herramienta **Red** desde el panel **Trabajo de servicios**</span><span class="sxs-lookup"><span data-stu-id="c09e6-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="c09e6-161">La herramienta **Red** se abre en el **cajón** y muestra todas las solicitudes de red relacionadas con los trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="c09e6-162">Las solicitudes de red se filtran mediante `is:service-worker-intercepted`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Herramienta Red en el cajón" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="c09e6-164">Herramienta **Red** en el **Cajón**</span><span class="sxs-lookup"><span data-stu-id="c09e6-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="c09e6-165">Para devolver la herramienta **Red** al panel superior, cierre el **Cajón**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Cerrar el cajón para devolver la herramienta Red" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="c09e6-167">Cerrar el **Cajón** para devolver la herramienta **Red**</span><span class="sxs-lookup"><span data-stu-id="c09e6-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <a name="network-tool"></a><span data-ttu-id="c09e6-168">Herramienta Red</span><span class="sxs-lookup"><span data-stu-id="c09e6-168">Network tool</span></span>  

<span data-ttu-id="c09e6-169">Depure las solicitudes de red que se ejecutan a través de los trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="c09e6-170">También puede abrir solicitudes de red desde la herramienta **Aplicación**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="c09e6-171">Para cada solicitud, DevTools muestra la siguiente información en el panel [Intervalos][DevtoolsNetworkReferenceViewTimingBreakdownRequest].</span><span class="sxs-lookup"><span data-stu-id="c09e6-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="c09e6-172">El inicio de una solicitud y la duración del arranque.</span><span class="sxs-lookup"><span data-stu-id="c09e6-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="c09e6-173">Cambios en el registro de trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="c09e6-174">El tiempo de ejecución de un controlador de evento `fetch`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="c09e6-175">El tiempo de ejecución de todos los eventos `fetch` para cargar un cliente.</span><span class="sxs-lookup"><span data-stu-id="c09e6-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Panel Intervalos" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="c09e6-177">Panel **Intervalos**</span><span class="sxs-lookup"><span data-stu-id="c09e6-177">**Timing** pane</span></span>  
:::image-end:::  

### <a name="sources-tool"></a><span data-ttu-id="c09e6-178">Herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="c09e6-178">Sources tool</span></span>  

<span data-ttu-id="c09e6-179">En versiones anteriores de Microsoft Edge, el nivel de profundidad en la pila de llamadas estaba limitado al código de JavaScript en el trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="c09e6-180">En Microsoft Edge 88, la pila de llamadas ahora muestra el iniciador de solicitudes que se ejecutan a través del trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="c09e6-181">Para buscar el iniciador de la solicitud, use la pila de llamadas de su código JavaScript en el trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="c09e6-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="c09e6-182">La pila de llamadas de las siguientes figuras comienza con el código de JavaScript en el trabajo de servicio y muestra una referencia a la solicitud original de la página web como `(index):157`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="c09e6-183">En la segunda figura, se elige la referencia y se abre el iniciador que realizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c09e6-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="c09e6-184">El iniciador de la segunda figura es la página web.</span><span class="sxs-lookup"><span data-stu-id="c09e6-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="El originador de la solicitud de resaltado de pila de llamadas y archivos de service-worker.js" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="c09e6-186">El originador de solicitudes de resaltado de pila de llamadas y archivos `service-worker.js`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La página web (índice) es el iniciador de la solicitud" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="c09e6-188">La página web `(index)` es el iniciador de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c09e6-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a><span data-ttu-id="c09e6-189">Copiar el valor de la propiedad de una solicitud de red</span><span class="sxs-lookup"><span data-stu-id="c09e6-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="c09e6-190">En la herramienta **Red**, copie el valor de la propiedad de una solicitud de red con la nueva opción **Copiar valor**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="c09e6-191">El valor de la propiedad se copia como un valor JSON descodificado.</span><span class="sxs-lookup"><span data-stu-id="c09e6-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="c09e6-192">En versiones anteriores de Microsoft Edge, tenía que copiar un valor con una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="c09e6-193">Resalte todo el texto y cópielo.</span><span class="sxs-lookup"><span data-stu-id="c09e6-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="c09e6-194">Almacene el valor como variable global, según sea el caso, y cópielo desde la [Consola][DevtoolsConsoleIndex] de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c09e6-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="c09e6-195">Para copiar el valor de la propiedad en el portapapeles, desplácese hasta [Copiar JSON de respuesta con formato en el portapapeles][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="c09e6-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="c09e6-196">Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="c09e6-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar el valor de la propiedad en DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="c09e6-198">Copiar el valor de la propiedad en DevTools</span><span class="sxs-lookup"><span data-stu-id="c09e6-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Valor de la propiedad Paste en Microsoft Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="c09e6-200">Valor de la propiedad Paste en Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c09e6-200">Paste property value in Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a><span data-ttu-id="c09e6-201">Personalizar métodos abreviados de teclado de varios clics</span><span class="sxs-lookup"><span data-stu-id="c09e6-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="c09e6-202">[A partir de Microsoft Edge versión 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], puede personalizar los métodos abreviados de teclado para cualquier acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="c09e6-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="c09e6-203">En Microsoft Edge versión 88, ahora puede crear métodos abreviados de teclado de varios clics.</span><span class="sxs-lookup"><span data-stu-id="c09e6-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="c09e6-204">Para establecer un método abreviado para una acción en DevTools, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y elija la casilla situada junto a **Habilitar el editor de métodos abreviados de teclado**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="c09e6-205">Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental del editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="c09e6-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="c09e6-206">Por ejemplo, el resaltado rojo muestra un método abreviado de teclado de varios clics personalizado para la acción **Iniciar grabación de eventos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="c09e6-207">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el [Problema N.°174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="c09e6-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Métodos abreviados de teclado de presión simultánea" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="c09e6-209">Métodos abreviados de teclado de varios clics</span><span class="sxs-lookup"><span data-stu-id="c09e6-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a><span data-ttu-id="c09e6-210">DevTools ahora coincide con el idioma del explorador</span><span class="sxs-lookup"><span data-stu-id="c09e6-210">DevTools now match browser language</span></span>  

<span data-ttu-id="c09e6-211">En Microsoft Edge versión 87, si activaba la opción **Coincidir con el idioma del explorador** en la [Configuración de DevTools][DevtoolsCustomizeIndexSettings], DevTools no coincidía con el idioma del explorador.</span><span class="sxs-lookup"><span data-stu-id="c09e6-211">In Microsoft Edge version 87, if you turned on the **Match browser language** setting in [DevTools Settings][DevtoolsCustomizeIndexSettings], DevTools did not match the browser language.</span></span>  <span data-ttu-id="c09e6-212">En la versión 88 de Microsoft Edge, DevTools coincide con el idioma del explorador si se activa la opción **Coincidir con el idioma del explorador**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-212">In Microsoft Edge version 88, DevTools now matches the browser language if you turn on the **Match browser language** setting.</span></span>  <span data-ttu-id="c09e6-213">Para obtener más información sobre la opción de DevTools **Coincidir con el idioma del explorador**, vaya a [Cambiar la configuración de idioma de DevTools][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="c09e6-213">For more information about the **Match browser language** DevTools Setting, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Opción de DevTools Coincidir con el idioma del explorador en japonés" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   <span data-ttu-id="c09e6-215">Opción de DevTools **Coincidir con el idioma del explorador** en japonés</span><span class="sxs-lookup"><span data-stu-id="c09e6-215">**Match browser language** DevTools setting in Japanese</span></span>  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="c09e6-216">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="c09e6-216">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a><span data-ttu-id="c09e6-217">Nuevas herramientas de visualización de ángulos CSS</span><span class="sxs-lookup"><span data-stu-id="c09e6-217">New CSS angle visualization tools</span></span>  

<span data-ttu-id="c09e6-218">DevTools ahora es más compatible con la depuración de ángulos de CSS.</span><span class="sxs-lookup"><span data-stu-id="c09e6-218">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="c09e6-219">Cuando se aplica un ángulo CSS a un elemento HTML de la página, se muestra un icono de reloj junto al ángulo en la herramienta **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-219">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="c09e6-220">Para activar o desactivar la superposición de reloj, elija el icono de reloj.</span><span class="sxs-lookup"><span data-stu-id="c09e6-220">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="c09e6-221">Para cambiar el ángulo, seleccione cualquier lugar del reloj o arrastre la aguja.</span><span class="sxs-lookup"><span data-stu-id="c09e6-221">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="c09e6-222">Para cambiar el valor de ángulo, también puede usar los métodos abreviados de teclado y el mouse.</span><span class="sxs-lookup"><span data-stu-id="c09e6-222">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="c09e6-223">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1126178][CR1126178] y [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="c09e6-223">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="c09e6-224">Para el ejemplo, se usa el siguiente ángulo de CSS.</span><span class="sxs-lookup"><span data-stu-id="c09e6-224">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ángulo CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="c09e6-226">Ángulo CSS</span><span class="sxs-lookup"><span data-stu-id="c09e6-226">CSS angle</span></span>  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a><span data-ttu-id="c09e6-227">Simular tamaño de la cuota de almacenamiento en el panel Almacenamiento</span><span class="sxs-lookup"><span data-stu-id="c09e6-227">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="c09e6-228">Ahora puede invalidar el tamaño de la cuota de almacenamiento en el panel **Almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-228">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="c09e6-229">Esta característica le permite simular diferentes dispositivos y probar el comportamiento de su sitio web o aplicación en escenarios de disponibilidad de disco baja.</span><span class="sxs-lookup"><span data-stu-id="c09e6-229">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="c09e6-230">Para simular la cuota de almacenamiento, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-230">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-231">Vaya a **Aplicación** > **Almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-231">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="c09e6-232">Active la casilla **Simular cuota de almacenamiento personalizada**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-232">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="c09e6-233">Escriba un número válido.</span><span class="sxs-lookup"><span data-stu-id="c09e6-233">Enter a valid number.</span></span>  
    
<span data-ttu-id="c09e6-234">Para obtener más información sobre cómo emular dispositivos móviles y otras características de DevTools, vaya a [Emular dispositivos móviles en Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="c09e6-234">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="c09e6-235">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [945786][CR945786] y [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="c09e6-235">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular tamaño de la cuota de almacenamiento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="c09e6-237">Simular tamaño de la cuota de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="c09e6-237">Simulate storage quota size</span></span>  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a><span data-ttu-id="c09e6-238">Notificar errores de CORS en la herramienta Red</span><span class="sxs-lookup"><span data-stu-id="c09e6-238">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="c09e6-239">Para probar esta característica, navegue a [Demo de error de CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="c09e6-239">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="c09e6-240">Abra la herramienta **Red**, actualice la página y observe la solicitud de red de CORS errónea.</span><span class="sxs-lookup"><span data-stu-id="c09e6-240">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="c09e6-241">En la columna de estado se muestra el **Error de CORS**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-241">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="c09e6-242">Al desplazar el puntero sobre el error, la información sobre herramientas muestra ahora el código de error.</span><span class="sxs-lookup"><span data-stu-id="c09e6-242">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="c09e6-243">En Microsoft Edge versión 87 y anteriores, DevTools solo mostraba el estado **(erróneo)** genérico para los errores de CORS.</span><span class="sxs-lookup"><span data-stu-id="c09e6-243">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="c09e6-244">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="c09e6-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Errores de CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="c09e6-246">Errores de CORS</span><span class="sxs-lookup"><span data-stu-id="c09e6-246">CORS errors</span></span>  
:::image-end:::  

### <a name="frame-details-view-updates"></a><span data-ttu-id="c09e6-247">Actualización de la vista de detalles del marco</span><span class="sxs-lookup"><span data-stu-id="c09e6-247">Frame details view updates</span></span>  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a><span data-ttu-id="c09e6-248">Información de aislamiento entre orígenes en la vista detalles del Marco</span><span class="sxs-lookup"><span data-stu-id="c09e6-248">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="c09e6-249">El estado aislado entre orígenes se muestra ahora en la sección **Seguridad y aislamiento**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-249">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="c09e6-250">La nueva sección **Disponibilidad de API** muestra la disponibilidad de `SharedArrayBuffer`s \(SAB\) y si los búferes se pueden compartir mediante `postMessage()`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-250">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="c09e6-251">Se muestra una advertencia de desuso si SAB y `postMessage()` están disponibles en este momento, pero el contexto no está aislado entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="c09e6-251">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="c09e6-252">Para obtener más información sobre el aislamiento entre orígenes y por qué es necesario para características como `SharedArrayBuffers`, vaya a [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="c09e6-252">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="c09e6-253">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="c09e6-253">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Información entre orígenes" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="c09e6-255">Información entre orígenes</span><span class="sxs-lookup"><span data-stu-id="c09e6-255">Cross-origin information</span></span>  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a><span data-ttu-id="c09e6-256">Nueva información de trabajos web en la vista detalles del Marco</span><span class="sxs-lookup"><span data-stu-id="c09e6-256">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="c09e6-257">DevTools ahora organiza los trabajos web en el marco principal correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c09e6-257">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="c09e6-258">Por ejemplo, si el marco `someName` crea `worker.js`, entonces `worker.js` aparecerá en `someName` en la lista **Marcos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-258">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="c09e6-259">Para ver los detalles del trabajo web, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-259">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-260">Abra la herramienta **Aplicación**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-260">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="c09e6-261">Expanda un marco que contenga los trabajos web.</span><span class="sxs-lookup"><span data-stu-id="c09e6-261">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="c09e6-262">Expanda el árbol de **Trabajos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-262">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="c09e6-263">Elija un trabajo.</span><span class="sxs-lookup"><span data-stu-id="c09e6-263">Choose a worker.</span></span>  
    
<span data-ttu-id="c09e6-264">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1122507][CR1122507] y [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="c09e6-264">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Información de los trabajos web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="c09e6-266">Información de los trabajos web</span><span class="sxs-lookup"><span data-stu-id="c09e6-266">Web workers information</span></span>  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a><span data-ttu-id="c09e6-267">Mostrar detalles del marco de apertura para las ventanas abiertas</span><span class="sxs-lookup"><span data-stu-id="c09e6-267">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="c09e6-268">DevTools ahora organiza las [ventanas][MdnWindowConstructors] abiertas en el [Marco][MdnWindowFrames] principal correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c09e6-268">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="c09e6-269">Por ejemplo, si el marco `top` abre un `Window` para `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, entonces el `Window` aparece en `top` en la lista **Marcos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-269">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="c09e6-270">Para mostrar el marco responsable de abrir otra ventana en la herramienta **Elementos**, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-270">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-271">Abra el árbol **Marcos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-271">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="c09e6-272">Expanda **Ventanas abiertas** y elija el `Window` correspondiente al marco principal que desea saber.</span><span class="sxs-lookup"><span data-stu-id="c09e6-272">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="c09e6-273">Elija el vínculo **Marco de apertura**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-273">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="c09e6-274">Se muestran los detalles sobre el marco que causaba la apertura de otro `Window`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-274">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="c09e6-275">Para mostrar el abridor en la herramienta **Elementos**, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-275">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-276">Abra el árbol **Marcos**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-276">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="c09e6-277">Elija una ventana abierta para abrir los detalles de `Window`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-277">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="c09e6-278">Elija el vínculo **Marco de apertura**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-278">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="c09e6-279">Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="c09e6-279">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalles del marco abierto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="c09e6-281">Detalles del marco abierto</span><span class="sxs-lookup"><span data-stu-id="c09e6-281">Opened frame details</span></span>  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a><span data-ttu-id="c09e6-282">Copiar el seguimiento de la pila para el iniciador de red</span><span class="sxs-lookup"><span data-stu-id="c09e6-282">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="c09e6-283">Para copiar el seguimiento de la pila en el portapapeles, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c09e6-283">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="c09e6-284">Abra el menú contextual \(haga clic con el botón derecho\).</span><span class="sxs-lookup"><span data-stu-id="c09e6-284">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="c09e6-285">Elija **Copiar**  >  **Copiar seguimiento de la pila**.</span><span class="sxs-lookup"><span data-stu-id="c09e6-285">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="c09e6-286">Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="c09e6-286">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar seguimiento de la pila" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="c09e6-288">Copiar seguimiento de la pila</span><span class="sxs-lookup"><span data-stu-id="c09e6-288">Copy stacktrace</span></span>  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a><span data-ttu-id="c09e6-289">Vista previa de valor de variable Wasm en mouseover</span><span class="sxs-lookup"><span data-stu-id="c09e6-289">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="c09e6-290">Use esta característica para revisar el valor de una variable webassembly \(Wasm\) cuando se haya pausado el código.</span><span class="sxs-lookup"><span data-stu-id="c09e6-290">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="c09e6-291">Para mostrar el valor actual de una variable, desplace el puntero sobre una variable.</span><span class="sxs-lookup"><span data-stu-id="c09e6-291">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="c09e6-292">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1058836][CR1058836] y [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="c09e6-292">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vista previa de variable Wasm en mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="c09e6-294">Vista previa de variable Wasm en mouseover</span><span class="sxs-lookup"><span data-stu-id="c09e6-294">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a><span data-ttu-id="c09e6-295">Unidades de medida coherentes para tamaños de archivos y memoria</span><span class="sxs-lookup"><span data-stu-id="c09e6-295">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="c09e6-296">DevTools ahora usa `kB` de forma consistente para mostrar los tamaños de los archivos y de la memoria.</span><span class="sxs-lookup"><span data-stu-id="c09e6-296">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="c09e6-297">Anteriormente, DevTools combinaba `kB` y `KiB`.</span><span class="sxs-lookup"><span data-stu-id="c09e6-297">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="c09e6-298">o kilobytes \(10^3 o 1000bytes\)</span><span class="sxs-lookup"><span data-stu-id="c09e6-298">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="c09e6-299">o kibibytes \(2^10 o 1024bytes\)</span><span class="sxs-lookup"><span data-stu-id="c09e6-299">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="c09e6-300">Por ejemplo, la herramienta **Red** anteriormente usaba `kB` en las etiquetas, pero usaba `KiB` en los cálculos.</span><span class="sxs-lookup"><span data-stu-id="c09e6-300">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="c09e6-301">Sus comentarios mostraron que esta inconstancia ocasionó confusión.</span><span class="sxs-lookup"><span data-stu-id="c09e6-301">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="c09e6-302">Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="c09e6-302">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="c09e6-303">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c09e6-303">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="c09e6-304">Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c09e6-304">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="c09e6-305">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c09e6-305">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="c09e6-306">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c09e6-306">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Vista 3D | Microsoft Docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Descripción general de la consola | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Cambiar la configuración de idioma de DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activar Capas compuestas en la vista 3D: características experimentales | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar JSON de respuesta con formato en el portapapeles: referencia de análisis de red | Microsoft Docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Ver el desglose de intervalos de una solicitud: referencia de análisis de red | Microsoft Docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Usar Webdriver (Chromium) para la automatización de prueba | Microsoft Docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft Docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: ../10/devtools.md#customize-keyboard-shortcuts-in-settings "Personalizar los métodos abreviados de teclado en Configuración: novedades de DevTools (Microsoft Edge 87) | Microsoft Docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: ../06/devtools.md#webhint-feedback-in-the-issues-panel "Comentarios sobre webhint en el panel Problemas: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar WebDriver | Desarrollador de Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Descargar Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir la personalización de métodos abreviados de teclado o enlaces de clave | Errores de Chromium"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir invalidar navigator.storage.estimate() | Errores de Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: reducir la sobrecarga de rendimiento del envío de mensajes de protocolo en el front-end | Errores de Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools debe usar de forma coherente MB para significar megabyte, no mebibyte | Errores de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con la depuración de COOP/COEP en DevTools | Errores de Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: problemas UX en torno a la depuración de Wasm | Errores de Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ experiencia de desarrolladores básica de Wasm | Errores de Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: mostrar información sobre los marcos generados por 'window.open()' en el árbol de marcos | Errores de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: información de los trabajos superficiales en la vista de árbol de marcos | Errores de Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: componentes <Type> de CSS | Errores de Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: comprobar las reservas de imagen (emulación) | Errores de Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: no se puede copiar fácilmente la carga útil de la solicitud JSON | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: herramientas de la caja flexible | Errores de Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: el componente <angle> de CSS debe reflejar la apariencia de la propiedad que se encuentra en el fondo del reloj | Errores de Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: el iniciador de red debe ofrecer la posibilidad de copiar el seguimiento de la pila | Errores de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: informar la disponibilidad de la API validada en la vista detalles del marco | Errores de Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: iconos de las propiedades de CSS de la caja flexible en el panel Estilos | Errores de Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: mejorar el informe de errores de CORS en DevTools | Errores de Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: agregar adornos de estilo flexibles al árbol Elementos | Errores de cromo"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: el texto borrado se sigue viendo en el cuadro de texto de la sección 'Almacenamiento ' de la ventana 'Dev Tools' | Errores de Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Errores de CORS | Problema"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Uso compartido de recursos entre orígenes (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas de CSS (variables) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructores: ventana | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accesibilidad | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidad | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Rendimiento | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Inconvenientes | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Seguridad | webhint"  

> [!NOTE]
> <span data-ttu-id="c09e6-359">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c09e6-359">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c09e6-360">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-88) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="c09e6-360">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-88) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c09e6-362">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c09e6-362">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
