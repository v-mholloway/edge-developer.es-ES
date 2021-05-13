---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para encontrar formas de hacer que sus sitios web se carguen más rápido.
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 304cf9e36260b8637af38ed0dfe1ba91f3a56504
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564885"
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
# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a><span data-ttu-id="b6765-104">Optimizar la velocidad del sitio web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b6765-104">Optimize website speed with Microsoft Edge DevTools</span></span>  

## <a name="goal-of-tutorial"></a><span data-ttu-id="b6765-105">Objetivo del tutorial</span><span class="sxs-lookup"><span data-stu-id="b6765-105">Goal of tutorial</span></span>  

<span data-ttu-id="b6765-106">Este tutorial le enseña a usar Microsoft Edge DevTools para encontrar formas de hacer que sus sitios web se carguen más rápido.</span><span class="sxs-lookup"><span data-stu-id="b6765-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b6765-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6765-107">Prerequisites</span></span>  

*   <span data-ttu-id="b6765-108">Debe tener experiencia básica de desarrollo web, similar a lo que se enseña en esta [clase Introduction to Web Development][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="b6765-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="b6765-109">No es necesario saber nada sobre el rendimiento de carga.</span><span class="sxs-lookup"><span data-stu-id="b6765-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="b6765-110">Obtenga información sobre esto en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="b6765-110">You learn about it in this tutorial.</span></span>  

## <a name="introduction"></a><span data-ttu-id="b6765-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="b6765-111">Introduction</span></span>  

<span data-ttu-id="b6765-112">Este es Tony.</span><span class="sxs-lookup"><span data-stu-id="b6765-112">This is Tony.</span></span>  <span data-ttu-id="b6765-113">Tony es muy famoso en la sociedad de gatos.</span><span class="sxs-lookup"><span data-stu-id="b6765-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="b6765-114">Ha creado un sitio web para que sus fans puedan aprender sobre sus alimentos favoritos.</span><span class="sxs-lookup"><span data-stu-id="b6765-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="b6765-115">A sus fans les encanta el sitio, pero Tony sigue escuchando quejas de que el sitio se carga lentamente.</span><span class="sxs-lookup"><span data-stu-id="b6765-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="b6765-116">Tony te ha pedido que le ayudes a acelerar el sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony el gato" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="b6765-118">Tony el gato</span><span class="sxs-lookup"><span data-stu-id="b6765-118">Tony the cat</span></span>  
:::image-end:::  

## <a name="step-1-audit-the-site"></a><span data-ttu-id="b6765-119">Paso 1: Auditar el sitio</span><span class="sxs-lookup"><span data-stu-id="b6765-119">Step 1: Audit the site</span></span>  

<span data-ttu-id="b6765-120">Siempre que se establezca para mejorar el rendimiento de carga de un sitio, **comience siempre con una auditoría**.</span><span class="sxs-lookup"><span data-stu-id="b6765-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="b6765-121">La auditoría tiene 2 funciones importantes:</span><span class="sxs-lookup"><span data-stu-id="b6765-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="b6765-122">Crea una línea **base con** la que medir los cambios posteriores.</span><span class="sxs-lookup"><span data-stu-id="b6765-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="b6765-123">Le ofrece **sugerencias de acción sobre** los cambios que tienen más impacto.</span><span class="sxs-lookup"><span data-stu-id="b6765-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <a name="set-up"></a><span data-ttu-id="b6765-124">Configuración</span><span class="sxs-lookup"><span data-stu-id="b6765-124">Set up</span></span>  

<span data-ttu-id="b6765-125">En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.</span><span class="sxs-lookup"><span data-stu-id="b6765-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="b6765-126">[Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="b6765-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="b6765-127">Esta pestaña se conoce como pestaña **editor**.</span><span class="sxs-lookup"><span data-stu-id="b6765-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Pestaña editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="b6765-129">Pestaña **editor**</span><span class="sxs-lookup"><span data-stu-id="b6765-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-130">Elija **tony**.</span><span class="sxs-lookup"><span data-stu-id="b6765-130">Choose **tony**.</span></span>  <span data-ttu-id="b6765-131">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="b6765-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Menú que aparece después de elegir Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="b6765-133">Menú que aparece después de elegir **Tony**</span><span class="sxs-lookup"><span data-stu-id="b6765-133">The menu that appears after choosing **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-134">Elija **Remezcla Project**.</span><span class="sxs-lookup"><span data-stu-id="b6765-134">Choose **Remix Project**.</span></span>  <span data-ttu-id="b6765-135">El nombre del proyecto cambia de **tony** a algún nombre generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="b6765-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="b6765-136">Ahora tiene su propia copia editable del código.</span><span class="sxs-lookup"><span data-stu-id="b6765-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="b6765-137">Más adelante, puede realizar cambios en este código.</span><span class="sxs-lookup"><span data-stu-id="b6765-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="b6765-138">Elija **Mostrar** y **elija En una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="b6765-138">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="b6765-139">La demostración se abre en una pestaña nueva.  Esta pestaña se conoce como pestaña **de demostración**.  El sitio puede tardar un tiempo en cargarse.</span><span class="sxs-lookup"><span data-stu-id="b6765-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Pestaña de demostración" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="b6765-141">Pestaña de demostración</span><span class="sxs-lookup"><span data-stu-id="b6765-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-142">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="b6765-142">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="b6765-143">Microsoft Edge DevTools se abre junto con la demostración.</span><span class="sxs-lookup"><span data-stu-id="b6765-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools y la demostración" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="b6765-145">DevTools y la demostración</span><span class="sxs-lookup"><span data-stu-id="b6765-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-146">Para el resto de capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="b6765-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="b6765-147">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) `Undock` \*\*\*\* para abrir el menú comando, escribir y, a continuación, seleccionar Desacoplar en una ventana independiente .</span><span class="sxs-lookup"><span data-stu-id="b6765-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools desacopladas" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="b6765-149">DevTools desacopladas</span><span class="sxs-lookup"><span data-stu-id="b6765-149">Undocked DevTools</span></span>  
:::image-end:::  

### <a name="establish-a-baseline"></a><span data-ttu-id="b6765-150">Establecer una línea base</span><span class="sxs-lookup"><span data-stu-id="b6765-150">Establish a baseline</span></span>  

<span data-ttu-id="b6765-151">La línea base es un registro de cómo se realizó el sitio antes de realizar cualquier mejora de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="b6765-152">Elija la **herramienta Auditorías.**</span><span class="sxs-lookup"><span data-stu-id="b6765-152">Choose the **Audits** tool.</span></span>  <span data-ttu-id="b6765-153">Puede estar oculto detrás del **botón Más paneles** \( Más paneles ![ ](../media/more-panels-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b6765-153">It may be hidden behind the **More Panels** \(![More Panels](../media/more-panels-icon.msft.png)\) button.</span></span>  <span data-ttu-id="b6765-154">Hay un Faro en este panel porque el proyecto que impulsa el panel Auditorías se denomina **Faro**.</span><span class="sxs-lookup"><span data-stu-id="b6765-154">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="La herramienta Auditorías" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="b6765-156">La **herramienta Auditorías**</span><span class="sxs-lookup"><span data-stu-id="b6765-156">The **Audits** tool</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="b6765-157">Haga coincidir las opciones de configuración de auditoría con las de la figura anterior.</span><span class="sxs-lookup"><span data-stu-id="b6765-157">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="b6765-158">Esta es una explicación de las diferentes opciones:</span><span class="sxs-lookup"><span data-stu-id="b6765-158">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="b6765-159">**Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="b6765-159">**Device**.</span></span>  <span data-ttu-id="b6765-160">Establecer en **Móvil cambia** la cadena del agente de usuario y simula una ventanilla móvil.</span><span class="sxs-lookup"><span data-stu-id="b6765-160">Set to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="b6765-161">Si se **establece en Escritorio,** se desactivan los **cambios de** Móvil.</span><span class="sxs-lookup"><span data-stu-id="b6765-161">Set to **Desktop** pretty much just turns off the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="b6765-162">**Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="b6765-162">**Audits**.</span></span>  <span data-ttu-id="b6765-163">Desactive una categoría para impedir que el panel Auditorías ejecute **dichas** auditorías y las excluye del informe.</span><span class="sxs-lookup"><span data-stu-id="b6765-163">Turn off a category to prevent the **Audits** panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="b6765-164">Deje las otras categorías Activadas, si desea mostrar los tipos de recomendaciones que se proporcionan.</span><span class="sxs-lookup"><span data-stu-id="b6765-164">Leave the other categories Turned on, if you want to display the types of recommendations that are provided.</span></span>  <span data-ttu-id="b6765-165">Desactiva las categorías para acelerar ligeramente el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="b6765-165">Turn off categories to slightly speed up the auditing process.</span></span>  
    *   <span data-ttu-id="b6765-166">**Limitación**.</span><span class="sxs-lookup"><span data-stu-id="b6765-166">**Throttling**.</span></span>  <span data-ttu-id="b6765-167">Establecida en **Simulated Slow 4G, 4x CPU Slowdown** simula las condiciones típicas de navegación en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="b6765-167">Set to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="b6765-168">Se denomina "simulado" porque el panel Auditorías no limita realmente durante el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="b6765-168">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="b6765-169">En su lugar, solo extrapola el tiempo que tarda la página en cargarse en condiciones móviles.</span><span class="sxs-lookup"><span data-stu-id="b6765-169">Instead, it just extrapolates how long the page takes to load under mobile conditions.</span></span>  <span data-ttu-id="b6765-170">Por **otro lado,** la configuración Aplicado... limita realmente la CPU y la red, con la negociación de un proceso de auditoría más largo.</span><span class="sxs-lookup"><span data-stu-id="b6765-170">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="b6765-171">**Desactive Storage**.</span><span class="sxs-lookup"><span data-stu-id="b6765-171">**Clear Storage**.</span></span>  <span data-ttu-id="b6765-172">Active la casilla para borrar todo el almacenamiento asociado a la página antes de cada auditoría.</span><span class="sxs-lookup"><span data-stu-id="b6765-172">Turn on the checkbox to clear all storage associated with the page before every audit.</span></span>  <span data-ttu-id="b6765-173">Deje esta configuración en si desea auditar la experiencia de los visitantes por primera vez en su sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-173">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="b6765-174">Desactiva esta configuración cuando quieras la experiencia de repetición de visita.</span><span class="sxs-lookup"><span data-stu-id="b6765-174">Turn off this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="b6765-175">Elija **Ejecutar auditorías**.</span><span class="sxs-lookup"><span data-stu-id="b6765-175">Choose **Run Audits**.</span></span>  <span data-ttu-id="b6765-176">Después de 10 a 30 segundos, el panel **Auditorías** muestra un informe del rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-176">After 10 to 30 seconds, the **Audits** panel displays a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Informe del panel Auditorías del rendimiento del sitio" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="b6765-178">Informe del panel Auditorías del rendimiento del sitio</span><span class="sxs-lookup"><span data-stu-id="b6765-178">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a><span data-ttu-id="b6765-179">Controlar errores de informe</span><span class="sxs-lookup"><span data-stu-id="b6765-179">Handling report errors</span></span>  

<span data-ttu-id="b6765-180">Si alguna vez recibe un error en el informe del panel Auditorías, intente ejecutar la pestaña de demostración desde una ventana **de InPrivate** sin otras pestañas abiertas.</span><span class="sxs-lookup"><span data-stu-id="b6765-180">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="b6765-181">Esto garantiza que se está ejecutando Microsoft Edge desde un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="b6765-181">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="b6765-182">Microsoft Edge Las extensiones, en particular, suelen interferir con el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="b6765-182">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a><span data-ttu-id="b6765-183">Comprender el informe</span><span class="sxs-lookup"><span data-stu-id="b6765-183">Understand your report</span></span>  

<span data-ttu-id="b6765-184">El número en la parte superior del informe es la puntuación de rendimiento general del sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-184">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="b6765-185">Más adelante, al realizar cambios en el código, el número que se muestra debe aumentar.</span><span class="sxs-lookup"><span data-stu-id="b6765-185">Later, as you make changes to the code, the number displayed should rise.</span></span>  <span data-ttu-id="b6765-186">Una puntuación más alta significa un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-186">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Puntuación general de rendimiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="b6765-188">Puntuación general de rendimiento</span><span class="sxs-lookup"><span data-stu-id="b6765-188">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-189">La **sección Métricas** proporciona medidas cuantitativas del rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-189">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="b6765-190">Cada métrica proporciona información sobre un aspecto diferente del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-190">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="b6765-191">Por ejemplo, **First Contentful Paint** indica cuándo el contenido se pinta por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que **Time To Interactive** marca el punto en el que la página parece lo suficientemente lista para controlar las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="b6765-191">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Sección Métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="b6765-193">Sección **Métricas**</span><span class="sxs-lookup"><span data-stu-id="b6765-193">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-194">Elija el botón de alternancia resaltado en la siguiente figura para mostrar una descripción para cada métrica y elija **Obtener** más información para leer la documentación al respecto.</span><span class="sxs-lookup"><span data-stu-id="b6765-194">Choose the highlighted toggle button in the following figure to display a description for each metric, and choose **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Elija el botón de alternancia resaltado para expandir los elementos de métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="b6765-196">Elija el botón de alternancia resaltado para expandir los elementos de métricas</span><span class="sxs-lookup"><span data-stu-id="b6765-196">Choose the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-197">Debajo de Métricas se muestra una colección de capturas de pantalla que muestran cómo se cargó la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-197">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de pantalla de cómo se veía la página durante la carga" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="b6765-199">Capturas de pantalla de cómo se veía la página durante la carga</span><span class="sxs-lookup"><span data-stu-id="b6765-199">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-200">La sección Oportunidades proporciona **sugerencias** específicas sobre cómo mejorar el rendimiento de carga de esta página específica.</span><span class="sxs-lookup"><span data-stu-id="b6765-200">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Sección Oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="b6765-202">Sección **Oportunidades**</span><span class="sxs-lookup"><span data-stu-id="b6765-202">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-203">Elija una oportunidad para obtener más información sobre él.</span><span class="sxs-lookup"><span data-stu-id="b6765-203">Choose an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar la oportunidad de recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="b6765-205">**Eliminar la oportunidad de recursos de bloqueo de** representación</span><span class="sxs-lookup"><span data-stu-id="b6765-205">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-206">Elija **Obtener más información** para mostrar documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo solucionarla.</span><span class="sxs-lookup"><span data-stu-id="b6765-206">Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentación para la oportunidad Eliminar recursos de bloqueo de representación" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="b6765-208">Documentación para la **oportunidad Eliminar recursos de bloqueo de** representación</span><span class="sxs-lookup"><span data-stu-id="b6765-208">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-209">La **sección Diagnóstico proporciona** más información sobre los factores que contribuyen al tiempo de carga de la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-209">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Sección Diagnóstico" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="b6765-211">Sección **Diagnóstico**</span><span class="sxs-lookup"><span data-stu-id="b6765-211">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-212">La **sección Auditorías pasadas** muestra lo que el sitio está haciendo correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6765-212">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="b6765-213">Elija expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="b6765-213">Choose to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Sección Auditorías pasadas" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="b6765-215">Sección **Auditorías pasadas**</span><span class="sxs-lookup"><span data-stu-id="b6765-215">The **Passed Audits** section</span></span>  
:::image-end:::  

## <a name="step-2-experiment"></a><span data-ttu-id="b6765-216">Paso 2: Experimento</span><span class="sxs-lookup"><span data-stu-id="b6765-216">Step 2: Experiment</span></span>  

<span data-ttu-id="b6765-217">La sección Oportunidades del informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-217">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="b6765-218">En esta sección, se implementan los cambios recomendados en la base de código, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-218">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <a name="enable-text-compression"></a><span data-ttu-id="b6765-219">Habilitar compresión de texto</span><span class="sxs-lookup"><span data-stu-id="b6765-219">Enable text compression</span></span>  

<span data-ttu-id="b6765-220">El informe indica que evitar enormes cargas de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-220">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="b6765-221">Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-221">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="b6765-222">La compresión de texto es cuando se reduce o se comprime el tamaño de un archivo de texto antes de enviarlo a través de la red.</span><span class="sxs-lookup"><span data-stu-id="b6765-222">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="b6765-223">Similar a cómo archivar un directorio antes de enviarlo para reducir el tamaño.</span><span class="sxs-lookup"><span data-stu-id="b6765-223">Similar to how you may archive a directory before sending it to reduce the size.</span></span>  

<span data-ttu-id="b6765-224">Antes de habilitar la compresión, estas son algunas formas de comprobar manualmente si los recursos de texto están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="b6765-224">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="b6765-225">Elija la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="b6765-225">Choose the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panel Red" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="b6765-227">La **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="b6765-227">The **Network** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-228">Elija el **icono Configuración de** red.</span><span class="sxs-lookup"><span data-stu-id="b6765-228">Choose the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="b6765-229">Seleccione la casilla **Usar filas de solicitud grandes.**</span><span class="sxs-lookup"><span data-stu-id="b6765-229">Choose the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="b6765-230">Aumenta el alto de las filas de la tabla de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="b6765-230">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Filas grandes en la tabla de solicitudes de red" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="b6765-232">Filas grandes en la tabla de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="b6765-232">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-233">Si no **se muestra** la columna Tamaño de la tabla de solicitudes de red, elija el encabezado de la tabla > **Size**.</span><span class="sxs-lookup"><span data-stu-id="b6765-233">If the **Size** column in the table of network requests is not displayed, choose the table header > **Size**.</span></span>  

<span data-ttu-id="b6765-234">Cada **celda Size** muestra dos valores.</span><span class="sxs-lookup"><span data-stu-id="b6765-234">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="b6765-235">El valor superior es el tamaño del recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="b6765-235">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="b6765-236">El valor inferior es el tamaño del recurso sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b6765-236">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="b6765-237">Si los dos valores son los mismos, no se está comprimiendo el recurso cuando se envía a través de la red.</span><span class="sxs-lookup"><span data-stu-id="b6765-237">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="b6765-238">Por ejemplo, en la figura anterior, los valores superior e inferior `bundle.js` para son `1.2 MB` y `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="b6765-238">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="b6765-239">Compruebe la compresión inspeccionando los encabezados HTTP de un recurso:</span><span class="sxs-lookup"><span data-stu-id="b6765-239">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="b6765-240">Elija `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="b6765-240">Choose `bundle.js`.</span></span>  
1.  <span data-ttu-id="b6765-241">Elija el panel **Encabezados.**</span><span class="sxs-lookup"><span data-stu-id="b6765-241">Choose the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Panel Encabezados" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="b6765-243">Panel **Encabezados**</span><span class="sxs-lookup"><span data-stu-id="b6765-243">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-244">Busque un **encabezado en la sección Encabezados** de `content-encoding` respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6765-244">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="b6765-245">No `content-encoding` se muestra un encabezado, lo que significa que no se `bundle.js` comprimió.</span><span class="sxs-lookup"><span data-stu-id="b6765-245">A `content-encoding` heading is not displayed, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="b6765-246">Cuando se comprime un recurso, este encabezado normalmente se establece en `gzip` , `deflate` o `br` .</span><span class="sxs-lookup"><span data-stu-id="b6765-246">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="b6765-247">Para obtener una explicación de los valores, vaya a [Directivas][MDNContentEncodingDirectives].</span><span class="sxs-lookup"><span data-stu-id="b6765-247">For an explanation of the values, navigate to [Directives][MDNContentEncodingDirectives].</span></span>  

<span data-ttu-id="b6765-248">Suficiente con las explicaciones.</span><span class="sxs-lookup"><span data-stu-id="b6765-248">Enough with the explanations.</span></span>  <span data-ttu-id="b6765-249">Hora de realizar algunos cambios.</span><span class="sxs-lookup"><span data-stu-id="b6765-249">Time to make some changes.</span></span>  <span data-ttu-id="b6765-250">Habilite la compresión de texto agregando un par de líneas de código:</span><span class="sxs-lookup"><span data-stu-id="b6765-250">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="b6765-251">En la pestaña editor, elija **server.js**.</span><span class="sxs-lookup"><span data-stu-id="b6765-251">In the editor tab, choose **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Editar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="b6765-253">Editar</span><span class="sxs-lookup"><span data-stu-id="b6765-253">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-254">Agregue el siguiente código a **server.js**.</span><span class="sxs-lookup"><span data-stu-id="b6765-254">Add the following code to **server.js**.</span></span>  <span data-ttu-id="b6765-255">Asegúrese de colocar antes `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="b6765-255">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="b6765-256">Por lo general, debe instalar el paquete a través de algo `compression` como , pero esto ya se ha hecho por `npm i -S compression` usted.</span><span class="sxs-lookup"><span data-stu-id="b6765-256">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="b6765-257">Espere a que Glitch implemente la nueva compilación del sitio.</span><span class="sxs-lookup"><span data-stu-id="b6765-257">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="b6765-258">La animación de lujo junto **a Herramientas** significa que el sitio se está recompilando y reimplementando.</span><span class="sxs-lookup"><span data-stu-id="b6765-258">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="b6765-259">El cambio está listo cuando desaparece la animación junto **a Herramientas.**</span><span class="sxs-lookup"><span data-stu-id="b6765-259">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="b6765-260">Elija **Mostrar** y **vuelva a elegir En una nueva** ventana.</span><span class="sxs-lookup"><span data-stu-id="b6765-260">Choose **Show** and choose **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="b6765-261">Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:</span><span class="sxs-lookup"><span data-stu-id="b6765-261">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="b6765-262">Vuelva a la pestaña de demostración y actualice la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-262">Go back to the demo tab and refresh the page.</span></span>  <span data-ttu-id="b6765-263">La **columna** Tamaño ahora debe mostrar 2 valores diferentes para recursos de texto como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="b6765-263">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="b6765-264">En la figura siguiente, el valor superior de for es el tamaño del archivo que se envió a través de la red y el valor inferior de es el tamaño del archivo `256 KB` `bundle.js` sin `1.2 MB` comprimir.</span><span class="sxs-lookup"><span data-stu-id="b6765-264">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La columna Tamaño muestra ahora 2 valores diferentes para recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="b6765-266">La **columna** Tamaño muestra ahora 2 valores diferentes para recursos de texto</span><span class="sxs-lookup"><span data-stu-id="b6765-266">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-267">La **sección Encabezados de** respuesta para ahora debe incluir un `bundle.js` `content-encoding: gzip` encabezado.</span><span class="sxs-lookup"><span data-stu-id="b6765-267">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La sección Encabezados de respuesta ahora contiene un encabezado de codificación de contenido" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="b6765-269">La **sección Encabezados de** respuesta ahora contiene un encabezado de codificación de contenido</span><span class="sxs-lookup"><span data-stu-id="b6765-269">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-270">Audite la página de nuevo para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:</span><span class="sxs-lookup"><span data-stu-id="b6765-270">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="b6765-271">Elija la **herramienta Auditorías.**</span><span class="sxs-lookup"><span data-stu-id="b6765-271">Choose the **Audits** tool.</span></span>  
1.  <span data-ttu-id="b6765-272">Elija **Realizar una auditoría** \( Realizar una auditoría ![ ](../media/perform-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b6765-272">Choose **Perform an audit** \(![Perform an audit](../media/perform-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="b6765-273">Deje la configuración igual que antes.</span><span class="sxs-lookup"><span data-stu-id="b6765-273">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="b6765-274">Elija **Ejecutar auditoría**.</span><span class="sxs-lookup"><span data-stu-id="b6765-274">Choose **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Informe auditorías después de habilitar la compresión de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="b6765-276">Informe auditorías después de habilitar la compresión de texto</span><span class="sxs-lookup"><span data-stu-id="b6765-276">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="b6765-277">La puntuación general de rendimiento debería haber aumentado, lo que significa que el sitio es cada vez más rápido.</span><span class="sxs-lookup"><span data-stu-id="b6765-277">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <a name="text-compression-in-the-real-world"></a><span data-ttu-id="b6765-278">Compresión de texto en el mundo real</span><span class="sxs-lookup"><span data-stu-id="b6765-278">Text compression in the real world</span></span>  

<span data-ttu-id="b6765-279">La mayoría de los servidores realmente tienen correcciones sencillas como esta para habilitar la compresión.</span><span class="sxs-lookup"><span data-stu-id="b6765-279">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="b6765-280">Simplemente haga una búsqueda sobre cómo configurar cualquier servidor que use para comprimir texto.</span><span class="sxs-lookup"><span data-stu-id="b6765-280">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <a name="resize-images"></a><span data-ttu-id="b6765-281">Cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="b6765-281">Resize images</span></span>  

<span data-ttu-id="b6765-282">El informe indica que evitar enormes cargas de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-282">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="b6765-283">El tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.</span><span class="sxs-lookup"><span data-stu-id="b6765-283">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="b6765-284">Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, realmente no tiene sentido enviar una imagen de 1500 píxeles.</span><span class="sxs-lookup"><span data-stu-id="b6765-284">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="b6765-285">Lo ideal es enviar una imagen de 500 píxeles, como máximo.</span><span class="sxs-lookup"><span data-stu-id="b6765-285">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="b6765-286">En el informe, elija **Evitar enormes cargas de red** para mostrar qué imágenes deben cambiar de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b6765-286">In your report, choose **Avoid enormous network payloads** to display which images should be resized.</span></span>  <span data-ttu-id="b6765-287">Parece que 2 de los archivos jpg tienen más de 2000 KB, lo que es más grande de lo necesario.</span><span class="sxs-lookup"><span data-stu-id="b6765-287">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="b6765-288">De nuevo en la pestaña editor, abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="b6765-288">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="b6765-289">Reemplace `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="b6765-289">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="b6765-290">Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b6765-290">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="b6765-291">Audite la página de nuevo para mostrar cómo afecta el cambio al rendimiento de carga.</span><span class="sxs-lookup"><span data-stu-id="b6765-291">Audit the page again to display how the change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un informe de auditorías después de redimensionar imágenes" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="b6765-293">Un informe de auditorías después de redimensionar imágenes</span><span class="sxs-lookup"><span data-stu-id="b6765-293">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-294">El cambio que se muestra solo tiene un efecto menor en la puntuación de rendimiento general.</span><span class="sxs-lookup"><span data-stu-id="b6765-294">The change displays only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="b6765-295">Sin embargo, una cosa que la puntuación no muestra claramente es la cantidad de datos de red que está guardando los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b6765-295">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="b6765-296">El tamaño total de las fotos antiguas era de unos 5,3 megabytes, mientras que ahora solo es de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="b6765-296">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <a name="resizing-images-in-the-real-world"></a><span data-ttu-id="b6765-297">Cambio de tamaño de imágenes en el mundo real</span><span class="sxs-lookup"><span data-stu-id="b6765-297">Resizing images in the real world</span></span>  

<span data-ttu-id="b6765-298">Para una aplicación pequeña, hacer un cambio de tamaño único como este puede ser lo suficientemente bueno.</span><span class="sxs-lookup"><span data-stu-id="b6765-298">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="b6765-299">Pero para una aplicación grande, esto obviamente no es escalable.</span><span class="sxs-lookup"><span data-stu-id="b6765-299">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="b6765-300">Estas son algunas estrategias para administrar imágenes en aplicaciones grandes:</span><span class="sxs-lookup"><span data-stu-id="b6765-300">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="b6765-301">Cambie el tamaño de las imágenes durante el proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="b6765-301">Resize images during your build process.</span></span>  
*   <span data-ttu-id="b6765-302">Cree varios tamaños de cada imagen durante el proceso de compilación y, a continuación, `srcset` úselo en el código.</span><span class="sxs-lookup"><span data-stu-id="b6765-302">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="b6765-303">En tiempo de ejecución, el explorador se encarga de elegir el tamaño más adecuado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6765-303">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="b6765-304">Usa una imagen CDN que te permita cambiar el tamaño dinámicamente de una imagen cuando la solicites.</span><span class="sxs-lookup"><span data-stu-id="b6765-304">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="b6765-305">Como mínimo, optimice cada imagen.</span><span class="sxs-lookup"><span data-stu-id="b6765-305">At the very least, optimize each image.</span></span>  <span data-ttu-id="b6765-306">Esto puede crear grandes ahorros.</span><span class="sxs-lookup"><span data-stu-id="b6765-306">This may create huge savings.</span></span>  
  <span data-ttu-id="b6765-307">La optimización es cuando se ejecuta una imagen a través de un programa especial que reduce el tamaño del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="b6765-307">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="b6765-308">Para obtener más sugerencias, vaya a [Optimización de imagen esencial.][EssentialImageOptimization]</span><span class="sxs-lookup"><span data-stu-id="b6765-308">For more tips, navigate to [Essential Image Optimization][EssentialImageOptimization].</span></span>  
    
### <a name="eliminate-render-blocking-resources"></a><span data-ttu-id="b6765-309">Eliminar recursos de bloqueo de representación</span><span class="sxs-lookup"><span data-stu-id="b6765-309">Eliminate render-blocking resources</span></span>  

<span data-ttu-id="b6765-310">El informe más reciente indica que eliminar los recursos de bloqueo de representación es ahora la mayor oportunidad.</span><span class="sxs-lookup"><span data-stu-id="b6765-310">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="b6765-311">Un recurso de bloqueo de representación es un archivo JavaScript o CSS externo que el explorador debe descargar, analizar y ejecutar antes de mostrar la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-311">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="b6765-312">El objetivo es ejecutar solo el código CSS y JavaScript principal necesario para mostrar la página correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6765-312">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="b6765-313">La primera tarea, a continuación, es buscar código que no es necesario ejecutar en la carga de página.</span><span class="sxs-lookup"><span data-stu-id="b6765-313">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="b6765-314">Elija **Eliminar recursos de bloqueo de representación** para mostrar los recursos que están bloqueando:</span><span class="sxs-lookup"><span data-stu-id="b6765-314">Choose **Eliminate render-blocking resources** to display the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="b6765-315">y `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="b6765-315">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Más información sobre la oportunidad Eliminar recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="b6765-317">Más información sobre la oportunidad **Eliminar recursos de bloqueo de** representación</span><span class="sxs-lookup"><span data-stu-id="b6765-317">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-318">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) `Coverage` \*\*\*\* para abrir el menú comando, empiece a escribir y, a continuación, elija Mostrar cobertura .</span><span class="sxs-lookup"><span data-stu-id="b6765-318">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then choose **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abra el menú comando desde el panel Auditorías" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="b6765-320">Abra el menú comando desde el panel **Auditorías**</span><span class="sxs-lookup"><span data-stu-id="b6765-320">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="La herramienta Cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="b6765-322">La **herramienta Cobertura**</span><span class="sxs-lookup"><span data-stu-id="b6765-322">The **Coverage** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-323">Elija **Actualizar** \( ![ Actualizar ](../media/reload-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b6765-323">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\).</span></span>  <span data-ttu-id="b6765-324">La **herramienta Cobertura** proporciona información general sobre la cantidad de código en , y se ejecuta mientras se carga la `bundle.js` `jquery.js` `lodash.js` página.</span><span class="sxs-lookup"><span data-stu-id="b6765-324">The **Coverage** tool provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="b6765-325">En la figura siguiente, aproximadamente el 76 % y el 30 % de los archivos jQuery y Lodash no se usan, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b6765-325">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="El informe de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="b6765-327">El informe de cobertura</span><span class="sxs-lookup"><span data-stu-id="b6765-327">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-328">Elija la `jquery.js` fila.</span><span class="sxs-lookup"><span data-stu-id="b6765-328">Choose the `jquery.js` row.</span></span>  <span data-ttu-id="b6765-329">DevTools abre el archivo en la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="b6765-329">DevTools opens the file in the **Sources** tool.</span></span>  <span data-ttu-id="b6765-330">Si se ejecutó una línea de código, aparece una barra azul junto a ella.</span><span class="sxs-lookup"><span data-stu-id="b6765-330">If a line of code ran, a blue bar appears next to it.</span></span>  <span data-ttu-id="b6765-331">Una barra roja significa que la línea de código no se ha ejecutado y, definitivamente, no es necesaria en la carga de la página web.</span><span class="sxs-lookup"><span data-stu-id="b6765-331">A red bar means the line of code was not run, and is definitely not needed on load of the webpage.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Visualización del archivo jQuery en la herramienta Orígenes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="b6765-333">Visualización del archivo jQuery en la **herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="b6765-333">Viewing the jQuery file in the **Sources** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-334">Desplácese por el código jQuery.</span><span class="sxs-lookup"><span data-stu-id="b6765-334">Scroll through the jQuery code.</span></span>  <span data-ttu-id="b6765-335">Algunas de las líneas que se ejecutan son solo comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6765-335">Some of the lines that run are actually just comments.</span></span>  <span data-ttu-id="b6765-336">Para quitar comentarios y reducir el tamaño del archivo, ejecute el código a través de una aplicación o un script de compresión.</span><span class="sxs-lookup"><span data-stu-id="b6765-336">To strip comments and reduce the size of the file, run the code through a minifier app or script.</span></span>  

<span data-ttu-id="b6765-337">En resumen, cuando trabaja con su \*\*\*\* propio código, la herramienta Cobertura le ayuda a analizar el código, línea por línea y solo enviar el código necesario para la carga de página.</span><span class="sxs-lookup"><span data-stu-id="b6765-337">In short, when you are working with your own code, the **Coverage** tool helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="b6765-338">¿Son `jquery.js` necesarios los archivos y incluso para cargar la `lodash.js` página?</span><span class="sxs-lookup"><span data-stu-id="b6765-338">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="b6765-339">La **herramienta de bloqueo** de solicitudes muestra lo que sucede cuando los recursos no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b6765-339">The **Request blocking** tool displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="b6765-340">Elija la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="b6765-340">Choose the **Network** tool.</span></span>  
1.  <span data-ttu-id="b6765-341">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir de nuevo el menú comando.</span><span class="sxs-lookup"><span data-stu-id="b6765-341">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="b6765-342">Empiece a escribir `blocking` y, a continuación, **elija Mostrar bloqueo de solicitudes**.</span><span class="sxs-lookup"><span data-stu-id="b6765-342">Start typing `blocking` and then choose **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="La herramienta de bloqueo de solicitudes" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="b6765-344">La **herramienta de bloqueo de solicitudes**</span><span class="sxs-lookup"><span data-stu-id="b6765-344">The **Request blocking** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-345">Elija **Agregar patrón** \( Agregar patrón ![ ](../media/add-pattern-icon.msft.png) \), escriba `/libs/*` y, a continuación, `Enter` seleccione para confirmar.</span><span class="sxs-lookup"><span data-stu-id="b6765-345">Choose **Add Pattern** \(![Add Pattern](../media/add-pattern-icon.msft.png)\), type `/libs/*`, and then select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Agregar un patrón para bloquear cualquier solicitud al directorio libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="b6765-347">Agregar un patrón para bloquear cualquier solicitud al `libs` directorio</span><span class="sxs-lookup"><span data-stu-id="b6765-347">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-348">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-348">Refresh the page.</span></span>  <span data-ttu-id="b6765-349">Las solicitudes jQuery y Lodash son de color rojo, lo que significa que las solicitudes se bloquearon.</span><span class="sxs-lookup"><span data-stu-id="b6765-349">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="b6765-350">La página aún se carga y es interactiva, por lo que parece que estos recursos no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="b6765-350">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="El panel Red muestra que las solicitudes se han bloqueado" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="b6765-352">La **herramienta Red** muestra que las solicitudes se han bloqueado</span><span class="sxs-lookup"><span data-stu-id="b6765-352">The **Network** tool shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-353">Elija **Quitar todos los patrones** \( Quitar todos los patrones ![ ](../media/remove-icon.msft.png) \) para eliminar el patrón de `/libs/*` bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b6765-353">Choose **Remove all patterns** \(![Remove all patterns](../media/remove-icon.msft.png)\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="b6765-354">En general, la **herramienta de bloqueo de** solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b6765-354">In general, the **Request blocking** tool is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="b6765-355">Ahora, quite las referencias a estos archivos del código y vuelva a auditar la página:</span><span class="sxs-lookup"><span data-stu-id="b6765-355">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="b6765-356">De nuevo en la pestaña editor, abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="b6765-356">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="b6765-357">Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="b6765-357">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="b6765-358">Espere a que el sitio vuelva a compilarse e implementarse de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b6765-358">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="b6765-359">Vuelva a auditar la página desde la **herramienta Auditorías.**</span><span class="sxs-lookup"><span data-stu-id="b6765-359">Audit the page again from the **Audits** tool.</span></span>  <span data-ttu-id="b6765-360">La puntuación general debería haber mejorado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b6765-360">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un informe de auditorías después de quitar los recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="b6765-362">Un **informe de auditorías** después de quitar los recursos de bloqueo de representación</span><span class="sxs-lookup"><span data-stu-id="b6765-362">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a><span data-ttu-id="b6765-363">Optimización de la ruta de representación crítica en el mundo real</span><span class="sxs-lookup"><span data-stu-id="b6765-363">Optimizing the Critical Rendering Path in the real-world</span></span>  

<span data-ttu-id="b6765-364">La **ruta de representación crítica** hace referencia al código que necesita para cargar una página.</span><span class="sxs-lookup"><span data-stu-id="b6765-364">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="b6765-365">En general, acelera la carga de la página solo enviando código crítico durante la carga de la página y, a continuación, cargando todo lo demás.</span><span class="sxs-lookup"><span data-stu-id="b6765-365">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="b6765-366">Es poco probable que pueda encontrar scripts que pueda quitar directamente, pero es posible que encuentre muchos scripts que no necesita solicitar durante la carga de la página y, en su lugar, se pueden solicitar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b6765-366">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--Navigate to [Using async or defer][async].  -->  
*   <span data-ttu-id="b6765-367">Si usa un marco, compruebe si tiene un modo de producción.</span><span class="sxs-lookup"><span data-stu-id="b6765-367">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="b6765-368">Este modo puede usar [][WebpackTreeShaking] una característica como la agitación de árbol para eliminar el código innecesario que bloquea la representación crítica.</span><span class="sxs-lookup"><span data-stu-id="b6765-368">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a><span data-ttu-id="b6765-369">Hacer menos trabajo de subprocesos principales</span><span class="sxs-lookup"><span data-stu-id="b6765-369">Do less main thread work</span></span>  

<span data-ttu-id="b6765-370">El informe más reciente muestra algunos posibles ahorros menores en la sección Oportunidades, pero si mira hacia abajo en la sección Diagnósticos, parece que el cuello de botella más grande es demasiada actividad de subprocesos principal.</span><span class="sxs-lookup"><span data-stu-id="b6765-370">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="b6765-371">El subproceso principal es donde el explorador realiza la mayor parte del trabajo necesario para mostrar una página, como analizar y ejecutar HTML, CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b6765-371">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="b6765-372">El objetivo es usar el panel Rendimiento para analizar el trabajo que está realizando el subproceso principal mientras se carga la página y encontrar formas de aplazar o quitar el trabajo innecesario.</span><span class="sxs-lookup"><span data-stu-id="b6765-372">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="b6765-373">Elija la **herramienta** Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-373">Choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="b6765-374">Elija **Capturar Configuración** \( Capturar Configuración ![ ](../media/capture-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b6765-374">Choose **Capture Settings** \(![Capture Settings](../media/capture-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="b6765-375">Establezca **Network** en **Slow 3G** y **CPU** en **6x slowdown**.</span><span class="sxs-lookup"><span data-stu-id="b6765-375">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="b6765-376">Los dispositivos móviles suelen tener más restricciones de hardware que portátiles o escritorios, por lo que esta configuración te permite experimentar la carga de la página como si estuvieras usando un dispositivo menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="b6765-376">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="b6765-377">Elija **Actualizar** \( ![ Actualizar ](../media/reload-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b6765-377">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\).</span></span>  <span data-ttu-id="b6765-378">DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargar la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-378">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="b6765-379">Esta visualización se conoce como **seguimiento**.</span><span class="sxs-lookup"><span data-stu-id="b6765-379">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Seguimiento de la herramienta rendimiento de la carga de página" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="b6765-381">Seguimiento **de la herramienta** rendimiento de la carga de página</span><span class="sxs-lookup"><span data-stu-id="b6765-381">The **Performance** tool trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-382">El seguimiento muestra la actividad cronológicamente, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="b6765-382">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="b6765-383">Los gráficos DE FPS, CPU y NET en la parte superior le dan información general sobre fotogramas por segundo, actividad de CPU y actividad de red.</span><span class="sxs-lookup"><span data-stu-id="b6765-383">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="b6765-384">El bloque de color amarillo resaltado en la figura después de la siguiente, la CPU estaba completamente ocupada con la actividad de scripting.</span><span class="sxs-lookup"><span data-stu-id="b6765-384">The block of yellow highlighted in the figure after the next, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="b6765-385">Esta es una pista de que puede acelerar la carga de página haciendo menos trabajo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b6765-385">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="La sección Información general del seguimiento" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="b6765-387">La sección Información general del seguimiento</span><span class="sxs-lookup"><span data-stu-id="b6765-387">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="b6765-388">Investigue el seguimiento para encontrar formas de hacer menos trabajo de JavaScript:</span><span class="sxs-lookup"><span data-stu-id="b6765-388">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="b6765-389">Elija la **sección Timings** para expandirla.</span><span class="sxs-lookup"><span data-stu-id="b6765-389">Choose the **Timings** section to expand it.</span></span>  <span data-ttu-id="b6765-390">Basándose en el hecho de que puede haber un montón de medidas de [timings][MDNUserTimingApi] de React, parece que la aplicación de Tony está usando el modo de desarrollo de React.</span><span class="sxs-lookup"><span data-stu-id="b6765-390">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="b6765-391">Cambiar al modo de producción de React puede producir algunas ganancias de rendimiento fáciles.</span><span class="sxs-lookup"><span data-stu-id="b6765-391">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Sección Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="b6765-393">Sección **Timings**</span><span class="sxs-lookup"><span data-stu-id="b6765-393">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-394">Elija **Timings** de nuevo para contraer esa sección.</span><span class="sxs-lookup"><span data-stu-id="b6765-394">Choose **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="b6765-395">Examine la **sección** Principal.</span><span class="sxs-lookup"><span data-stu-id="b6765-395">Browse the **Main** section.</span></span>  <span data-ttu-id="b6765-396">En esta sección se muestra un registro cronológico de la actividad del subproceso principal, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="b6765-396">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="b6765-397">El eje Y (de arriba a abajo) muestra por qué se produjeron eventos.</span><span class="sxs-lookup"><span data-stu-id="b6765-397">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="b6765-398">Por ejemplo, en la higoría después de lo siguiente, el evento provocó la ejecución de la función, lo que provocó la ejecución, lo que provocó la `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` ejecución, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="b6765-398">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Sección Principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="b6765-400">Sección \*\*\*\* Principal</span><span class="sxs-lookup"><span data-stu-id="b6765-400">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b6765-401">Desplácese hacia abajo hasta la parte inferior de **la sección** Principal.</span><span class="sxs-lookup"><span data-stu-id="b6765-401">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="b6765-402">Cuando se usa un marco, la mayor parte de la actividad superior se debe al marco, que suele estar fuera de su control.</span><span class="sxs-lookup"><span data-stu-id="b6765-402">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="b6765-403">La actividad causada por la aplicación suele estar en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="b6765-403">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="b6765-404">En esta aplicación, parece que una función llamada está provocando muchas solicitudes `App` a una `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="b6765-404">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="b6765-405">Parece que Tony puede estar usando los dispositivos de sus fans para extraer criptodivisa...</span><span class="sxs-lookup"><span data-stu-id="b6765-405">It sounds like Tony may be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Mantener el mouse en la actividad mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="b6765-407">Mantener el mouse en la `mineBitcoin` actividad</span><span class="sxs-lookup"><span data-stu-id="b6765-407">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b6765-408">Aunque las solicitudes que realiza el marco suelen estar fuera de tu control, a veces puedes estructurar la aplicación de una manera que haga que el marco se ejecute de forma ineficaz.</span><span class="sxs-lookup"><span data-stu-id="b6765-408">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="b6765-409">Reestructurar la aplicación para usar el marco de forma eficiente es una forma de hacer menos trabajo principal de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b6765-409">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="b6765-410">Sin embargo, esto requiere una comprensión profunda de cómo funciona el marco y qué tipo de cambios realiza en su propio código para poder usar el marco de trabajo de forma más eficiente.</span><span class="sxs-lookup"><span data-stu-id="b6765-410">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="b6765-411">Expanda la **sección Abajo** arriba.</span><span class="sxs-lookup"><span data-stu-id="b6765-411">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="b6765-412">Esta pestaña desglosa las actividades que más tiempo tardaron en realizarse.</span><span class="sxs-lookup"><span data-stu-id="b6765-412">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="b6765-413">Si no se muestra nada en la Bottom-Up, elija la etiqueta de **la sección** Principal.</span><span class="sxs-lookup"><span data-stu-id="b6765-413">If nothing is displayed in the Bottom-Up section, choose the label for **Main** section.</span></span>  <span data-ttu-id="b6765-414">La **sección Abajo arriba** solo muestra información sobre cualquier actividad o grupo de actividad que haya seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b6765-414">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="b6765-415">Por ejemplo, si elige una de las actividades, la sección Abajo arriba solo mostrará `mineBitcoin` información para esa actividad. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b6765-415">For example, if you chose one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="La Bottom-Up pestaña" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="b6765-417">Ficha **Abajo arriba**</span><span class="sxs-lookup"><span data-stu-id="b6765-417">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-418">La **columna Tiempo de** autoservicio muestra cuánto tiempo se ha invertido directamente en cada actividad.</span><span class="sxs-lookup"><span data-stu-id="b6765-418">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="b6765-419">Por ejemplo, en la siguiente figura, aproximadamente el 63 % del tiempo de subproceso principal se ha invertido en la `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="b6765-419">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="b6765-420">Tiempo para revisar si el uso del modo de producción y la reducción de la actividad de JavaScript pueden acelerar la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-420">Time to review whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="b6765-421">Comience con el modo de producción:</span><span class="sxs-lookup"><span data-stu-id="b6765-421">Start with production mode:</span></span>  

1.  <span data-ttu-id="b6765-422">En la pestaña editor, abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="b6765-422">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="b6765-423">Cambiar `"mode":"development"` a `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="b6765-423">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="b6765-424">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="b6765-424">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="b6765-425">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-425">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Informe auditorías después de configurar webpack para usar el modo de producción" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="b6765-427">Informe auditorías después de configurar webpack para usar el modo de producción</span><span class="sxs-lookup"><span data-stu-id="b6765-427">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-428">Reduzca la actividad de JavaScript quitando la solicitud a `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="b6765-428">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="b6765-429">En la pestaña editor, abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="b6765-429">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="b6765-430">Comenta la solicitud en `this.mineBitcoin(1500)` `constructor` el archivo .</span><span class="sxs-lookup"><span data-stu-id="b6765-430">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="b6765-431">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="b6765-431">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="b6765-432">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="b6765-432">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un informe de auditorías después de quitar el trabajo de JavaScript innecesario" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="b6765-434">Un informe de auditorías después de quitar el trabajo de JavaScript innecesario</span><span class="sxs-lookup"><span data-stu-id="b6765-434">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b6765-435">Parece que el último cambio causó un salto masivo en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-435">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="b6765-436">En esta sección se proporciona una introducción bastante breve al panel Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-436">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="b6765-437">Para obtener más información sobre cómo analizar el rendimiento de la página, vaya a [Referencia de análisis de rendimiento][DevtoolsEvaluatePerformanceReference].</span><span class="sxs-lookup"><span data-stu-id="b6765-437">To learn more about how to analyze page performance, navigate to [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span></span>  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a><span data-ttu-id="b6765-438">Hacer menos trabajo de subprocesos principales en el mundo real</span><span class="sxs-lookup"><span data-stu-id="b6765-438">Doing less main thread work in the real world</span></span>  

<span data-ttu-id="b6765-439">En general, la **herramienta** Rendimiento es la forma más común de comprender qué actividad realiza el sitio a medida que se carga y encontrar formas de quitar actividad innecesaria.</span><span class="sxs-lookup"><span data-stu-id="b6765-439">In general, the **Performance** tool is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="b6765-440">Si prefiere un enfoque que se parece más a , la API de tiempo de usuario le permite marcar arbitrariamente determinadas fases del ciclo de vida de la aplicación, con el fin de realizar un seguimiento del tiempo que tarda cada una de estas `console.log()` fases. [][MDNUserTimingApi]</span><span class="sxs-lookup"><span data-stu-id="b6765-440">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <a name="summary"></a><span data-ttu-id="b6765-441">Resumen</span><span class="sxs-lookup"><span data-stu-id="b6765-441">Summary</span></span>  

*   <span data-ttu-id="b6765-442">Siempre que se configure para optimizar el rendimiento de carga de un sitio, comience siempre con una auditoría.</span><span class="sxs-lookup"><span data-stu-id="b6765-442">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="b6765-443">La auditoría establece una línea base y le ofrece sugerencias sobre cómo mejorar.</span><span class="sxs-lookup"><span data-stu-id="b6765-443">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="b6765-444">Realice un cambio a la vez y audite la página web después de cada cambio para mostrar cómo ese cambio aislado afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6765-444">Make one change at a time, and audit the webpage after each change in order to display how that isolated change affects performance.</span></span>  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b6765-445">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b6765-445">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referencia de análisis de rendimiento | Microsoft Docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introducción a la clase de desarrollo web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimización de imagen esencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directivas: codificación de contenido | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Api de tiempo de usuario | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Tree Shaking | webpack"  

> [!NOTE]
> <span data-ttu-id="b6765-452">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6765-452">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b6765-453">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b6765-453">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b6765-455">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6765-455">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
