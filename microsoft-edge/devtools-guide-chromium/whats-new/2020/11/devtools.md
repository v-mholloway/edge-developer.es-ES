---
description: Microsoft Edge en Linux, sugerencias de webhint mejoradas en la herramienta problemas, nuevas características de depuración de trabajo de servicio y más.
title: Novedades de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205246"
---
# <span data-ttu-id="1ac28-104">Novedades de DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="1ac28-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="1ac28-105">Microsoft Edge y el controlador Microsoft Edge ahora están disponibles en Linux</span><span class="sxs-lookup"><span data-stu-id="1ac28-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="1ac28-106">Microsoft Edge dev ahora es compatible con las distribuciones Ubuntu, Debian, Fedora y openSUSE.</span><span class="sxs-lookup"><span data-stu-id="1ac28-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="1ac28-107">Descarga e instala el programa o el `.deb` `.rpm` paquete de Microsoft Edge directamente desde el [sitio de Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] o usa las herramientas de administración de paquetes estándar de tu distribución de Linux.</span><span class="sxs-lookup"><span data-stu-id="1ac28-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="1ac28-108">Si está usando un entorno Linux en sus soluciones de integración y entrega continuas \ (CI/CD \), el controlador Microsoft Edge también está disponible en Linux.</span><span class="sxs-lookup"><span data-stu-id="1ac28-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="1ac28-109">Para empezar a automatizar Microsoft Edge dev con el controlador de Microsoft Edge, vaya a la [Página de descargas del controlador de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="1ac28-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="1ac28-110">Para obtener ayuda con la automatización de Microsoft Edge dev junto con el controlador de Microsoft Edge, navegue para [usar Webdriver (cromo) para la automatización de prueba][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="1ac28-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools en Microsoft Edge en Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="1ac28-112">DevTools en Microsoft Edge en Linux</span><span class="sxs-lookup"><span data-stu-id="1ac28-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <span data-ttu-id="1ac28-113">Sugerencias de webhint y de plataforma mejoradas en la herramienta problemas</span><span class="sxs-lookup"><span data-stu-id="1ac28-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="1ac28-114">Una herramienta de código abierto, [webhint][WebhintMain], proporciona comentarios en tiempo real para sitios web y páginas web locales.</span><span class="sxs-lookup"><span data-stu-id="1ac28-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="1ac28-115">A partir de la [versión 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], revise los comentarios de webhint en la herramienta [problemas][DevtoolsIssuesIndex] .</span><span class="sxs-lookup"><span data-stu-id="1ac28-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="1ac28-116">Los problemas que aparecen en la herramienta **problemas** ahora son más fáciles de revisar con la adición de las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="1ac28-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="1ac28-117">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="1ac28-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="1ac28-118">Compatibilidad</span><span class="sxs-lookup"><span data-stu-id="1ac28-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="1ac28-119">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="1ac28-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="1ac28-120">Problemas</span><span class="sxs-lookup"><span data-stu-id="1ac28-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="1ac28-121">PWA</span><span class="sxs-lookup"><span data-stu-id="1ac28-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="1ac28-122">Seguridad</span><span class="sxs-lookup"><span data-stu-id="1ac28-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="1ac28-123">Ahora puede filtrar problemas de terceros mediante una nueva casilla.</span><span class="sxs-lookup"><span data-stu-id="1ac28-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="1ac28-124">La funcionalidad de filtro le ayuda a ocultar problemas relacionados con el código de bibliotecas de terceros u otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="1ac28-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="1ac28-125">Para ayudarle a revisar los problemas que revela [webhint][WebhintMain], la herramienta **problemas** ahora muestra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="1ac28-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="1ac28-126">Fragmentos de código mejorados.</span><span class="sxs-lookup"><span data-stu-id="1ac28-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="1ac28-127">Vínculos a otros paneles relevantes.</span><span class="sxs-lookup"><span data-stu-id="1ac28-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="1ac28-128">Vínculos a la documentación para ayudarle a solucionar problemas de su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="1ac28-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Herramienta problemas" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="1ac28-130">Herramienta **problemas**</span><span class="sxs-lookup"><span data-stu-id="1ac28-130">**Issues** tool</span></span>  
:::image-end:::  

## <span data-ttu-id="1ac28-131">Las capas compuestas ahora se encuentran en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="1ac28-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="1ac28-132">Ahora puede visualizar el contenido de las **capas** junto con los valores de índice z y el modelo de objeto de documento \ (Dom \).</span><span class="sxs-lookup"><span data-stu-id="1ac28-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="1ac28-133">Esta característica le ayuda a depurar sin cambiar entre la [vista 3D][Devtools3dViewIndex] y las herramientas de **capas** con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1ac28-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="1ac28-134">Para obtener una experiencia de depuración visual completa, [ahora se combinan la vista 3D y las capas compuestas][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="1ac28-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Panel capas compuestas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="1ac28-136">Panel **capas compuestas**</span><span class="sxs-lookup"><span data-stu-id="1ac28-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="1ac28-137">Definiciones de variables CSS en el panel estilos</span><span class="sxs-lookup"><span data-stu-id="1ac28-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="1ac28-138">En el panel **estilos** , [las variables CSS][MdnUsingCssCustomProperties] ahora se vinculan directamente a cada definición.</span><span class="sxs-lookup"><span data-stu-id="1ac28-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="1ac28-139">Elija la variable para ver o cambiar fácilmente la definición de la variable CSS.</span><span class="sxs-lookup"><span data-stu-id="1ac28-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="1ac28-140">En el ejemplo, DevTools muestra los atributos CSS para el `body` elemento.</span><span class="sxs-lookup"><span data-stu-id="1ac28-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="1ac28-141">Para mostrar la definición de variable de la `--theme-body-background` variable CSS, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-142">En el panel **estilos** , elija `var(--theme-body-background)` .</span><span class="sxs-lookup"><span data-stu-id="1ac28-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="1ac28-143">El panel **estilos** ahora muestra la definición de la `--theme-body-background` variable CSS.</span><span class="sxs-lookup"><span data-stu-id="1ac28-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variable CSS vinculada al estilo" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="1ac28-145">Variable CSS vinculada al estilo</span><span class="sxs-lookup"><span data-stu-id="1ac28-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variable CSS vinculada al destino de estilo" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="1ac28-147">Variable CSS vinculada al destino de estilo</span><span class="sxs-lookup"><span data-stu-id="1ac28-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="1ac28-148">Mejoras en la depuración de trabajos de servicio</span><span class="sxs-lookup"><span data-stu-id="1ac28-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="1ac28-149">Las siguientes características nuevas de las herramientas de [redes](#network-tool), [aplicaciones](#application-tool)y [fuentes](#sources-tool) le ayudan a crear su [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="1ac28-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="1ac28-150">Use las siguientes características cuando tenga dificultades para depurar el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="1ac28-151">Enrutamiento de solicitudes muestra `startup` los `fetch` eventos y en función de las solicitudes de red que se ejecutan a través de los trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="1ac28-152">Se obtiene acceso a las escalas de tiempo desde la herramienta **aplicación** o **red** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="1ac28-153">La ayuda de las escalas de tiempo cuando tienes problemas con los trabajadores del servicio y deseas ver si hay algún problema con el `startup` `fetch` evento o.</span><span class="sxs-lookup"><span data-stu-id="1ac28-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <span data-ttu-id="1ac28-154">Herramienta de aplicación</span><span class="sxs-lookup"><span data-stu-id="1ac28-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="1ac28-155">Vea la información de enrutamiento de toda la solicitud de trabajo de servicio con el vínculo nuevas **solicitudes de red** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="1ac28-156">Para mostrar contexto adicional al depurar el trabajo del servicio, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-157">Vaya a los trabajadores del servicio de **aplicaciones**  >  \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="1ac28-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="1ac28-158">Elija **solicitudes de red**.</span><span class="sxs-lookup"><span data-stu-id="1ac28-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abrir la herramienta de red desde el panel de trabajo de servicios" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="1ac28-160">Abrir la herramienta de **red** desde el panel de **trabajo de servicios**</span><span class="sxs-lookup"><span data-stu-id="1ac28-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="1ac28-161">La herramienta **red** se abre en el **cajón** y muestra todas las solicitudes de red relacionadas con los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="1ac28-162">Las solicitudes de red se filtran mediante `is:service-worker-intercepted` .</span><span class="sxs-lookup"><span data-stu-id="1ac28-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Herramienta de red del cajón" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="1ac28-164">Herramienta de **red** del **cajón**</span><span class="sxs-lookup"><span data-stu-id="1ac28-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="1ac28-165">Para volver a la herramienta de **red** en el panel superior, cierre el **cajón**.</span><span class="sxs-lookup"><span data-stu-id="1ac28-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Cerrar el cajón para devolver la herramienta red" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="1ac28-167">Cerrar el **cajón** para devolver la herramienta **red**</span><span class="sxs-lookup"><span data-stu-id="1ac28-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="1ac28-168">Herramienta red</span><span class="sxs-lookup"><span data-stu-id="1ac28-168">Network tool</span></span>  

<span data-ttu-id="1ac28-169">Depure las solicitudes de red que se ejecutan a través de los trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="1ac28-170">También puede abrir solicitudes de red desde la herramienta de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="1ac28-171">Para cada solicitud, DevTools Mostrar la siguiente información en el panel [intervalos][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .</span><span class="sxs-lookup"><span data-stu-id="1ac28-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="1ac28-172">El inicio de una solicitud y la duración del bootstrap.</span><span class="sxs-lookup"><span data-stu-id="1ac28-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="1ac28-173">Cambios en el registro de trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="1ac28-174">El Runtime de un `fetch` controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="1ac28-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="1ac28-175">El motor en tiempo de ejecución de todos los `fetch` eventos para cargar un cliente.</span><span class="sxs-lookup"><span data-stu-id="1ac28-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Panel intervalos" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="1ac28-177">Panel **intervalos**</span><span class="sxs-lookup"><span data-stu-id="1ac28-177">**Timing** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-178">Herramienta orígenes</span><span class="sxs-lookup"><span data-stu-id="1ac28-178">Sources tool</span></span>  

<span data-ttu-id="1ac28-179">En versiones anteriores de Microsoft Edge, el nivel de profundidad en la pila de llamadas estaba limitado al código de JavaScript en el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="1ac28-180">En Microsoft Edge 88, la pila de llamadas ahora muestra el iniciador de solicitudes que se ejecutan a través del trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="1ac28-181">Para localizar el iniciador de la solicitud, usa la pila de llamadas de tu código de JavaScript en el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ac28-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="1ac28-182">La pila de llamadas de las siguientes figuras comienza con el código de JavaScript en el trabajo del servicio y muestra una referencia a la solicitud original de la Página Web `(index):157` .</span><span class="sxs-lookup"><span data-stu-id="1ac28-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="1ac28-183">En la segunda figura, se elige la referencia y se abre el iniciador que realizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ac28-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="1ac28-184">El iniciador de la segunda figura es la Página Web.</span><span class="sxs-lookup"><span data-stu-id="1ac28-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="El remitente de la solicitud de resaltado de pila de llamadas y archivos de service-worker.js" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="1ac28-186">El `service-worker.js` originador de solicitudes de resaltado de pila de llamadas y archivos</span><span class="sxs-lookup"><span data-stu-id="1ac28-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La página web (índice) es el iniciador de la solicitud" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="1ac28-188">La `(index)` Página Web es el iniciador de solicitudes</span><span class="sxs-lookup"><span data-stu-id="1ac28-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="1ac28-189">Copiar el valor de la propiedad de una solicitud de red</span><span class="sxs-lookup"><span data-stu-id="1ac28-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="1ac28-190">En la herramienta **red** , copie el valor de la propiedad de una solicitud de red con la opción nuevo **valor de copiado** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="1ac28-191">El valor de la propiedad se copia como un valor JSON descodificado.</span><span class="sxs-lookup"><span data-stu-id="1ac28-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="1ac28-192">En versiones anteriores de Microsoft Edge, tenía que copiar un valor con una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="1ac28-193">Resaltar todo el texto y copiarlo.</span><span class="sxs-lookup"><span data-stu-id="1ac28-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="1ac28-194">Almacene el valor como variable global, según sea el caso, y cópielo desde la [consola][DevtoolsConsoleIndex]de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1ac28-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="1ac28-195">Para copiar el valor de la propiedad en el portapapeles, desplácese hasta [copiar JSON de respuesta con formato en el portapapeles][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="1ac28-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="1ac28-196">Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="1ac28-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar el valor de la propiedad en DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="1ac28-198">Copiar el valor de la propiedad en DevTools</span><span class="sxs-lookup"><span data-stu-id="1ac28-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Pegar el valor de la propiedad en código de Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="1ac28-200">Pegar el valor de la propiedad en código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1ac28-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="1ac28-201">Personalizar métodos abreviados de teclado de pulsación múltiple</span><span class="sxs-lookup"><span data-stu-id="1ac28-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="1ac28-202">[Desde Microsoft Edge versión 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], puede personalizar los métodos abreviados de teclado para cualquier acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="1ac28-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="1ac28-203">En Microsoft Edge versión 88, ahora puede crear métodos abreviados de teclado de varios clics.</span><span class="sxs-lookup"><span data-stu-id="1ac28-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="1ac28-204">Para establecer un método abreviado para una acción en el DevTools, vaya a experimentos de [configuración][DevtoolsCustomizeIndexSettings]  >  \*\*\*\* y elija la casilla situada junto a **Habilitar el editor de métodos abreviados de teclado**.</span><span class="sxs-lookup"><span data-stu-id="1ac28-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="1ac28-205">Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="1ac28-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="1ac28-206">Por ejemplo, el resaltado rojo muestra un método abreviado de teclado con varias pulsaciones personalizado para la acción **iniciar grabación de eventos** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="1ac28-207">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#174309 de problemas][CR174309].</span><span class="sxs-lookup"><span data-stu-id="1ac28-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Métodos abreviados de teclado para cuerda" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="1ac28-209">Métodos abreviados de teclado de varias pulsaciones</span><span class="sxs-lookup"><span data-stu-id="1ac28-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <span data-ttu-id="1ac28-210">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="1ac28-210">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="1ac28-211">Nuevas herramientas de visualización de ángulos CSS</span><span class="sxs-lookup"><span data-stu-id="1ac28-211">New CSS angle visualization tools</span></span>  

<span data-ttu-id="1ac28-212">DevTools ahora es más compatible con la depuración de ángulos de CSS.</span><span class="sxs-lookup"><span data-stu-id="1ac28-212">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="1ac28-213">Cuando se aplica un ángulo CSS a un elemento HTML de la página, se muestra un icono de reloj junto al ángulo en la herramienta **estilos** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-213">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="1ac28-214">Para activar o desactivar la superposición de reloj, elija el icono de reloj.</span><span class="sxs-lookup"><span data-stu-id="1ac28-214">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="1ac28-215">Para cambiar el ángulo, seleccione cualquier lugar del reloj o arrastre la aguja.</span><span class="sxs-lookup"><span data-stu-id="1ac28-215">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="1ac28-216">Para cambiar el valor de ángulo, también puede usar los métodos abreviados de teclado y el mouse.</span><span class="sxs-lookup"><span data-stu-id="1ac28-216">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="1ac28-217">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [1126178][CR1126178] y [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="1ac28-217">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="1ac28-218">Para el ejemplo se usa el siguiente ángulo de CSS.</span><span class="sxs-lookup"><span data-stu-id="1ac28-218">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ángulo CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="1ac28-220">Ángulo CSS</span><span class="sxs-lookup"><span data-stu-id="1ac28-220">CSS angle</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-221">Simular tamaño de la cuota de almacenamiento en el panel almacenamiento</span><span class="sxs-lookup"><span data-stu-id="1ac28-221">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="1ac28-222">Ahora puede invalidar el tamaño de la cuota de almacenamiento en el panel **almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-222">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="1ac28-223">Esta característica te permite simular diferentes dispositivos y probar el comportamiento de tu sitio web o aplicación en escenarios de disponibilidad de espacio reducido.</span><span class="sxs-lookup"><span data-stu-id="1ac28-223">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="1ac28-224">Para simular la cuota de almacenamiento, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-224">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-225">Vaya a \*\*\*\*  >  **almacenamiento**de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-225">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="1ac28-226">Active la casilla **simular cuota de almacenamiento personalizada** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-226">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="1ac28-227">Escribe un número válido.</span><span class="sxs-lookup"><span data-stu-id="1ac28-227">Enter a valid number.</span></span>  
    
<span data-ttu-id="1ac28-228">Para obtener más información sobre cómo emular dispositivos móviles y otras características de la DevTools, vaya a [emular dispositivos móviles en Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="1ac28-228">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="1ac28-229">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [945786][CR945786] y [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="1ac28-229">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular tamaño de la cuota de almacenamiento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="1ac28-231">Simular tamaño de la cuota de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="1ac28-231">Simulate storage quota size</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-232">Notificar errores de CORS en la herramienta red</span><span class="sxs-lookup"><span data-stu-id="1ac28-232">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="1ac28-233">Para probar esta característica, navegue a la [demostración de error de CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="1ac28-233">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="1ac28-234">Abra la herramienta **red** , actualice la página y observe la solicitud de red de CORS errónea.</span><span class="sxs-lookup"><span data-stu-id="1ac28-234">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="1ac28-235">En la columna Estado se muestra el **error de CORS**.</span><span class="sxs-lookup"><span data-stu-id="1ac28-235">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="1ac28-236">Al desplazar el puntero sobre el error, la información sobre herramientas muestra ahora el código de error.</span><span class="sxs-lookup"><span data-stu-id="1ac28-236">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="1ac28-237">En Microsoft Edge versión 87 y anteriores, DevTools solo se muestra el estado Generic **(Failed)** para los errores de CORS.</span><span class="sxs-lookup"><span data-stu-id="1ac28-237">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="1ac28-238">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya al problema [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="1ac28-238">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Errores de CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="1ac28-240">Errores de CORS</span><span class="sxs-lookup"><span data-stu-id="1ac28-240">CORS errors</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-241">Actualización de la vista de detalles del marco</span><span class="sxs-lookup"><span data-stu-id="1ac28-241">Frame details view updates</span></span>  

#### <span data-ttu-id="1ac28-242">Información de aislamiento entre orígenes en la vista detalles del marco</span><span class="sxs-lookup"><span data-stu-id="1ac28-242">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="1ac28-243">El estado aislado de origen se muestra ahora en la sección **aislamiento del & de seguridad** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-243">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="1ac28-244">La nueva sección **disponibilidad de API** muestra la disponibilidad de `SharedArrayBuffer` s \ (Sab \) y si los búferes se pueden compartir mediante `postMessage()` .</span><span class="sxs-lookup"><span data-stu-id="1ac28-244">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="1ac28-245">Se muestra una advertencia de desuso si SAB y `postMessage()` está disponible en este momento, pero el contexto no está aislado de origen cruzado.</span><span class="sxs-lookup"><span data-stu-id="1ac28-245">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="1ac28-246">Para obtener más información sobre el aislamiento entre orígenes y por qué es necesario para características como `SharedArrayBuffers` , vaya a [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="1ac28-246">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="1ac28-247">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="1ac28-247">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Información de origen cruzado" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="1ac28-249">Información de origen cruzado</span><span class="sxs-lookup"><span data-stu-id="1ac28-249">Cross-origin information</span></span>  
:::image-end:::  

#### <span data-ttu-id="1ac28-250">Nueva información de trabajadores web en la vista detalles del marco</span><span class="sxs-lookup"><span data-stu-id="1ac28-250">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="1ac28-251">DevTools ahora organiza los trabajadores web en el marco principal correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1ac28-251">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="1ac28-252">Por ejemplo, si el `someName` marco se crea `worker.js` , `worker.js` aparecerá en `someName` la lista de **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-252">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="1ac28-253">Para ver los detalles del trabajo Web, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-253">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-254">Abrir herramienta de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-254">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="1ac28-255">Expandir un marco que contiene usuarios de Web.</span><span class="sxs-lookup"><span data-stu-id="1ac28-255">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="1ac28-256">Expanda el árbol de **trabajadores** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-256">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="1ac28-257">Elija un trabajador.</span><span class="sxs-lookup"><span data-stu-id="1ac28-257">Choose a worker.</span></span>  
    
<span data-ttu-id="1ac28-258">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [1122507][CR1122507] y [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="1ac28-258">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Información de los trabajadores web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="1ac28-260">Información de los trabajadores web</span><span class="sxs-lookup"><span data-stu-id="1ac28-260">Web workers information</span></span>  
:::image-end:::  

#### <span data-ttu-id="1ac28-261">Mostrar detalles de la trama de apertura para las ventanas abiertas</span><span class="sxs-lookup"><span data-stu-id="1ac28-261">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="1ac28-262">DevTools ahora organiza las [ventanas][MdnWindowConstructors] abiertas en el [marco][MdnWindowFrames]principal correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1ac28-262">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="1ac28-263">Por ejemplo, si el `top` marco abre un `Window` a `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , entonces el `Window` aparece debajo `top` de en la lista de **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-263">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="1ac28-264">Para mostrar el marco responsable de abrir otra ventana en la herramienta **elementos** , complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-264">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-265">Abra el árbol de **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-265">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="1ac28-266">Expanda las **ventanas abiertas** y elija el `Window` correspondiente al marco principal que desea saber.</span><span class="sxs-lookup"><span data-stu-id="1ac28-266">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="1ac28-267">Elija el vínculo de **marco de apertura** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-267">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="1ac28-268">Se muestran los detalles sobre el fotograma que causaba la apertura de otro `Window` .</span><span class="sxs-lookup"><span data-stu-id="1ac28-268">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="1ac28-269">Para mostrar el abrir en la herramienta **elementos** , complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-269">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-270">Abra el árbol de **Marcos** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-270">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="1ac28-271">Elija una ventana abierta para abrir los `Window` detalles.</span><span class="sxs-lookup"><span data-stu-id="1ac28-271">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="1ac28-272">Elija el vínculo de **marco de apertura** .</span><span class="sxs-lookup"><span data-stu-id="1ac28-272">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="1ac28-273">Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="1ac28-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalles del fotograma abierto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="1ac28-275">Detalles del fotograma abierto</span><span class="sxs-lookup"><span data-stu-id="1ac28-275">Opened frame details</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-276">Copiar StackTrace para el iniciador de red</span><span class="sxs-lookup"><span data-stu-id="1ac28-276">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="1ac28-277">Para copiar StackTrace en el portapapeles, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1ac28-277">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="1ac28-278">Abra el menú contextual \ (haga clic con el botón derecho \).</span><span class="sxs-lookup"><span data-stu-id="1ac28-278">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="1ac28-279">Elija **copiar**  >  **copia de StackTrace**.</span><span class="sxs-lookup"><span data-stu-id="1ac28-279">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="1ac28-280">Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="1ac28-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="1ac28-282">Copiar StackTrace</span><span class="sxs-lookup"><span data-stu-id="1ac28-282">Copy stacktrace</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-283">Vista previa de valor de variable de WASM en mouseover</span><span class="sxs-lookup"><span data-stu-id="1ac28-283">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="1ac28-284">Use esta característica para revisar el valor de una variable webassembly \ (WASM \) cuando se haya pausado el código.</span><span class="sxs-lookup"><span data-stu-id="1ac28-284">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="1ac28-285">Para mostrar el valor actual de una variable, desplace el puntero sobre una variable.</span><span class="sxs-lookup"><span data-stu-id="1ac28-285">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="1ac28-286">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [1058836][CR1058836] y [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="1ac28-286">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vista previa de WASM variable en mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="1ac28-288">Vista previa de WASM variable en mouseover</span><span class="sxs-lookup"><span data-stu-id="1ac28-288">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <span data-ttu-id="1ac28-289">Unidades de medida coherentes para tamaños de archivos y memoria</span><span class="sxs-lookup"><span data-stu-id="1ac28-289">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="1ac28-290">DevTools ahora `kB` para mostrar de forma coherente los tamaños de los archivos y de la memoria.</span><span class="sxs-lookup"><span data-stu-id="1ac28-290">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="1ac28-291">Anteriormente DevTools Mixed `kB` y `KiB` .</span><span class="sxs-lookup"><span data-stu-id="1ac28-291">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="1ac28-292">o kilobytes \ (10 ^ 3 o 1000 bytes \)</span><span class="sxs-lookup"><span data-stu-id="1ac28-292">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="1ac28-293">o Kibibyte \ (2 ^ 10 o 1024 bytes \)</span><span class="sxs-lookup"><span data-stu-id="1ac28-293">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="1ac28-294">Por ejemplo, la herramienta de **red** que se usó anteriormente `kB` en las etiquetas, pero que se usa `KiB` en los cálculos.</span><span class="sxs-lookup"><span data-stu-id="1ac28-294">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="1ac28-295">Sus comentarios mostraron que esta incoherencia ocasionó confusión.</span><span class="sxs-lookup"><span data-stu-id="1ac28-295">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="1ac28-296">Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="1ac28-296">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <span data-ttu-id="1ac28-297">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="1ac28-297">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="1ac28-298">Si está en Windows, Linux o macOS, considere la posibilidad de usar el [canales de Microsoft Edge Preview] [MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ac28-298">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="1ac28-299">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1ac28-299">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="1ac28-300">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1ac28-300">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Vista 3D | Microsoft docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Descripción general de la consola | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activar capas compuestas en vista 3D: características experimentales | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar JSON de respuesta con formato en el portapapeles: referencia de análisis de red | Microsoft docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Ver el desglose de intervalos de una solicitud-referencia de análisis de red | Microsoft docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Usar Webdriver (cromo) para automatización de prueba | Microsoft docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personalizar los métodos abreviados de teclado en configuración-novedades de DevTools (Microsoft Edge 87) | Microsoft docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Comentarios sobre webhint en el panel problemas: novedades de DevTools (Microsoft Edge 85) | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar Webdriver | Microsoft Developer"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Descargar los canales de Insider de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Código de Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir para personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir invalidar Navigator. Storage. Calculate () | Errores de cromo"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: reducir la sobrecarga de rendimiento del envío de mensajes de protocolo en el front-end | Errores de cromo"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools debe usar de forma coherente MB para significar megabyte, no Mebibyte | Errores de cromo"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con COOP/depuración de COEP en DevTools | Errores de cromo"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: experiencia del usuario en la depuración de WASM | Errores de cromo"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ WASM Basic Developer Experience | Errores de cromo"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: Mostrar información sobre los marcos generados por ' Window. Open () ' en árbol de marcos | Errores de cromo"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: información de los trabajadores superficiales en la vista árbol de marcos | Errores de cromo"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: CSS <Type> Components | Errores de cromo"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: comprobar las reservas de imagen (emulación) | Errores de cromo"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: no se puede copiar fácilmente la carga de la solicitud JSON | Errores de cromo"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: herramientas de Flexbox | Errores de cromo"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: el componente> Angle <de CSS debe reflejar la apariencia de la propiedad que se encuentra en el fondo del reloj | Errores de cromo"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: el iniciador de red debe ofrecer la posibilidad de copiar el seguimiento de la pila | Errores de cromo"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: disponibilidad del informe de API validada en la vista detalles del marco | Errores de cromo"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: iconos de las propiedades de CSS de Flexbox en el panel estilos | Errores de cromo"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: mejorar el informe de errores de CORS en DevTools | Errores de cromo"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: agregar adornos de estilo Flex al árbol de elementos | Errores de cromo"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: el texto borrado se sigue viendo en el cuadro de texto de la sección ' almacenamiento ' de la ventana ' herramientas de desarrollo ' | Errores de cromo"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Errores de CORS | Intento"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Uso compartido de recursos entre orígenes (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas (variables) de CSS | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructores-Window | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "sugerencia"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accesibilidad | sugerencia"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidad | sugerencia"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Rendimiento | sugerencia"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Problemas | sugerencia"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | sugerencia"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Seguridad | sugerencia"  

> [!NOTE]
> <span data-ttu-id="1ac28-351">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1ac28-351">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1ac28-352">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/11/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="1ac28-352">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1ac28-354">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1ac28-354">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
