---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para encontrar formas de hacer que sus sitios web se carguen más rápido.
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: dafcb9c4d1194239baed7507e505d74d2b4ce1c8
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993446"
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





# <span data-ttu-id="73685-104">Optimizar la velocidad del sitio web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="73685-104">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="73685-105">Objetivo del tutorial</span><span class="sxs-lookup"><span data-stu-id="73685-105">Goal of tutorial</span></span>  

<span data-ttu-id="73685-106">En este tutorial aprenderás a usar Microsoft Edge DevTools para encontrar formas de cargar tus sitios web más rápido.</span><span class="sxs-lookup"><span data-stu-id="73685-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="73685-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="73685-107">Prerequisites</span></span>  

*   <span data-ttu-id="73685-108">Debe tener experiencia básica de desarrollo web, similar a lo que enseñamos esta [Introducción a la clase de desarrollo web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="73685-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="73685-109">No es necesario que sepa nada sobre el rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="73685-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="73685-110">Puede obtener más información en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="73685-110">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="73685-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="73685-111">Introduction</span></span>   

<span data-ttu-id="73685-112">Es Tony.</span><span class="sxs-lookup"><span data-stu-id="73685-112">This is Tony.</span></span>  <span data-ttu-id="73685-113">Tony es muy famoso en el gato de la sociedad.</span><span class="sxs-lookup"><span data-stu-id="73685-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="73685-114">Ha creado un sitio web para que sus ventiladores puedan conocer sus alimentos favoritos.</span><span class="sxs-lookup"><span data-stu-id="73685-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="73685-115">Sus ventiladores adoran el sitio, pero Tony mantiene las quejas auditivas que el sitio carga lentamente.</span><span class="sxs-lookup"><span data-stu-id="73685-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="73685-116">Tony le ha pedido que le ayude a acelerar el sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony el gato" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="73685-118">Tony el gato</span><span class="sxs-lookup"><span data-stu-id="73685-118">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="73685-119">Paso 1: auditar el sitio</span><span class="sxs-lookup"><span data-stu-id="73685-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="73685-120">Siempre que lo establezca para mejorar el rendimiento de la carga de un sitio, **empiece siempre con una auditoría**.</span><span class="sxs-lookup"><span data-stu-id="73685-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="73685-121">La auditoría tiene dos funciones importantes:</span><span class="sxs-lookup"><span data-stu-id="73685-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="73685-122">Crea una **línea base** para medir los cambios posteriores.</span><span class="sxs-lookup"><span data-stu-id="73685-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="73685-123">Le ofrece **consejos útiles** sobre qué cambios son más impactantes.</span><span class="sxs-lookup"><span data-stu-id="73685-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="73685-124">Configuración</span><span class="sxs-lookup"><span data-stu-id="73685-124">Set up</span></span>   

<span data-ttu-id="73685-125">En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.</span><span class="sxs-lookup"><span data-stu-id="73685-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="73685-126">[Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="73685-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="73685-127">Esta pestaña se conoce como la **pestaña Editor**.</span><span class="sxs-lookup"><span data-stu-id="73685-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Ficha Editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="73685-129">**Ficha Editor**</span><span class="sxs-lookup"><span data-stu-id="73685-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-130">Seleccione **Tony**.</span><span class="sxs-lookup"><span data-stu-id="73685-130">Select **tony**.</span></span>  <span data-ttu-id="73685-131">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="73685-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="El menú que aparece después de hacer clic en Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="73685-133">El menú que aparece después de hacer clic en **Tony**</span><span class="sxs-lookup"><span data-stu-id="73685-133">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-134">Seleccione **proyecto Remix**.</span><span class="sxs-lookup"><span data-stu-id="73685-134">Select **Remix Project**.</span></span>  <span data-ttu-id="73685-135">El nombre del proyecto cambia de **Tony** a algún nombre generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="73685-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="73685-136">Ahora tiene su propia copia modificable del código.</span><span class="sxs-lookup"><span data-stu-id="73685-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="73685-137">Más adelante, puedes realizar cambios en este código.</span><span class="sxs-lookup"><span data-stu-id="73685-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="73685-138">Seleccione **Mostrar** y seleccione **en una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="73685-138">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="73685-139">La demostración se abre en una nueva pestaña.  Esta pestaña se conoce como la **pestaña demo**.  Es posible que el sitio tarde un rato en cargarse.</span><span class="sxs-lookup"><span data-stu-id="73685-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="La ficha demo" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="73685-141">La ficha demo</span><span class="sxs-lookup"><span data-stu-id="73685-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-142">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="73685-142">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="73685-143">Microsoft Edge DevTools se abre junto con la demostración.</span><span class="sxs-lookup"><span data-stu-id="73685-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools y la demostración" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="73685-145">DevTools y la demostración</span><span class="sxs-lookup"><span data-stu-id="73685-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-146">Para el resto de las capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="73685-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="73685-147">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú comando, escriba `Undock` y, a continuación, seleccione **desacoplar en ventana independiente**.</span><span class="sxs-lookup"><span data-stu-id="73685-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools desacoplado" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="73685-149">DevTools desacoplado</span><span class="sxs-lookup"><span data-stu-id="73685-149">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="73685-150">Establecer una línea base</span><span class="sxs-lookup"><span data-stu-id="73685-150">Establish a baseline</span></span>   

<span data-ttu-id="73685-151">La línea base es un registro de cómo se realizó el sitio antes de realizar alguna mejora en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73685-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="73685-152">Seleccione la pestaña **auditorías** .  Es posible que esté oculto detrás **del** botón \ ( ![ más paneles ][ImageMorePanelsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="73685-152">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="73685-153">Hay un Lighthouse en este panel porque el proyecto que alimenta el panel auditoría se denomina **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="73685-153">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Panel auditorías" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="73685-155">Panel **auditorías**</span><span class="sxs-lookup"><span data-stu-id="73685-155">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="73685-156">Ajuste las opciones de configuración de auditoría a las de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="73685-156">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="73685-157">A continuación se explican las diferentes opciones:</span><span class="sxs-lookup"><span data-stu-id="73685-157">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="73685-158">**Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="73685-158">**Device**.</span></span>  <span data-ttu-id="73685-159">Configuración para **dispositivos móviles** cambia la cadena de agente de usuario y simula un área de visualización móvil.</span><span class="sxs-lookup"><span data-stu-id="73685-159">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="73685-160">La configuración en el **escritorio** simplemente deshabilita los cambios en el **teléfono móvil** .</span><span class="sxs-lookup"><span data-stu-id="73685-160">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="73685-161">**Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="73685-161">**Audits**.</span></span>  <span data-ttu-id="73685-162">Si deshabilita una categoría, evitará que el panel auditoría las ejecute y las excluirá de su informe.</span><span class="sxs-lookup"><span data-stu-id="73685-162">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="73685-163">Deje las otras categorías habilitadas si desea ver los tipos de recomendaciones proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="73685-163">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="73685-164">Al deshabilitar las categorías, se acelera ligeramente el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="73685-164">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="73685-165">**Limitación**.</span><span class="sxs-lookup"><span data-stu-id="73685-165">**Throttling**.</span></span>  <span data-ttu-id="73685-166">Configurada para **simular lentitud de 4G, con una ralentización** de la CPU de 4x simula las condiciones típicas de la navegación en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="73685-166">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="73685-167">Se denomina "simulado" porque en realidad el panel auditorías no se limita durante el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="73685-167">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="73685-168">En su lugar, simplemente extrapola cuánto tiempo tardará la página en cargarse en condiciones móviles.</span><span class="sxs-lookup"><span data-stu-id="73685-168">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="73685-169">Por otro lado, la opción de configuración **aplicado** , limita la CPU y la red, con la compensación de un proceso de auditoría más largo.</span><span class="sxs-lookup"><span data-stu-id="73685-169">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="73685-170">**Borrar almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="73685-170">**Clear Storage**.</span></span>  <span data-ttu-id="73685-171">Al habilitar esta casilla, se borra todo el almacenamiento asociado a la página antes de cada auditoría.</span><span class="sxs-lookup"><span data-stu-id="73685-171">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="73685-172">Deje esta configuración activada si desea auditar la experiencia de los visitantes por primera vez en su sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-172">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="73685-173">Deshabilite esta configuración cuando quiera la experiencia de repetición de la visita.</span><span class="sxs-lookup"><span data-stu-id="73685-173">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="73685-174">Seleccione **Ejecutar Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="73685-174">Select **Run Audits**.</span></span>  <span data-ttu-id="73685-175">Después de 10 a 30 segundos, el panel auditoría muestra un informe del rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-175">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Informe para el panel auditoría del rendimiento del sitio" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="73685-177">Informe para el panel auditoría del rendimiento del sitio</span><span class="sxs-lookup"><span data-stu-id="73685-177">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="73685-178">Control de errores de informe</span><span class="sxs-lookup"><span data-stu-id="73685-178">Handling report errors</span></span>   

<span data-ttu-id="73685-179">Si alguna vez recibe un error en el informe del panel auditorías, pruebe a ejecutar la pestaña demostración desde una ventana **InPrivate** sin ninguna otra pestaña abierta.</span><span class="sxs-lookup"><span data-stu-id="73685-179">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="73685-180">Esto asegura que está ejecutando Microsoft Edge desde un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="73685-180">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="73685-181">Las extensiones de Microsoft Edge en particular suelen interferir con el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="73685-181">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="73685-182">Comprender el informe</span><span class="sxs-lookup"><span data-stu-id="73685-182">Understand your report</span></span>   

<span data-ttu-id="73685-183">El número que aparece en la parte superior del informe es la puntuación de rendimiento general para el sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-183">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="73685-184">Después, a medida que haga cambios en el código, debería ver que este número ha aumentado.</span><span class="sxs-lookup"><span data-stu-id="73685-184">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="73685-185">Una puntuación mayor supone un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73685-185">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="La puntuación general de rendimiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="73685-187">La puntuación general de rendimiento</span><span class="sxs-lookup"><span data-stu-id="73685-187">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="73685-188">La sección de **métricas** proporciona medidas cuantitativas en el rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-188">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="73685-189">Cada métrica proporciona información sobre un aspecto diferente del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73685-189">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="73685-190">Por ejemplo, la **primera pintura con contenido** le indica cuando el contenido se pinta por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que el tiempo de marca **interactiva** es el punto en el que la página aparece lo suficientemente lista para controlar las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="73685-190">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="La sección métrica" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="73685-192">La sección **métrica**</span><span class="sxs-lookup"><span data-stu-id="73685-192">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="73685-193">Seleccione el botón de alternancia resaltado en la siguiente ilustración para ver una descripción de cada métrica y haga clic en **obtener más información** para leer la documentación de la misma.</span><span class="sxs-lookup"><span data-stu-id="73685-193">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Seleccione el botón de alternancia resaltado para expandir los elementos de métrica" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="73685-195">Seleccione el botón de alternancia resaltado para expandir los elementos de métrica</span><span class="sxs-lookup"><span data-stu-id="73685-195">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="73685-196">A continuación, se muestra una colección de capturas de pantallas en la que se muestra cómo se ha cargado la página.</span><span class="sxs-lookup"><span data-stu-id="73685-196">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de pantallas del aspecto de la página durante la carga" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="73685-198">Capturas de pantallas del aspecto de la página durante la carga</span><span class="sxs-lookup"><span data-stu-id="73685-198">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="73685-199">La sección **oportunidades** proporciona sugerencias específicas sobre cómo mejorar el rendimiento de la carga de esta página específica.</span><span class="sxs-lookup"><span data-stu-id="73685-199">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="La sección oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="73685-201">La sección **oportunidades**</span><span class="sxs-lookup"><span data-stu-id="73685-201">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="73685-202">Seleccione una oportunidad para obtener más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="73685-202">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar la oportunidad de recursos de bloqueo de procesamiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="73685-204">**Eliminar la oportunidad de recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="73685-204">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="73685-205">Seleccione **más información** para ver la documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo corregirla.</span><span class="sxs-lookup"><span data-stu-id="73685-205">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentación de la oportunidad eliminar recursos de bloqueo de procesamiento" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="73685-207">Documentación de la oportunidad **eliminar recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="73685-207">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="73685-208">La sección **diagnósticos** proporciona más información sobre los factores que contribuyen al tiempo de carga de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-208">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="La sección diagnósticos" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="73685-210">La sección **diagnósticos**</span><span class="sxs-lookup"><span data-stu-id="73685-210">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="73685-211">En la sección de **auditorías superada** se muestra lo que el sitio está haciendo correctamente.</span><span class="sxs-lookup"><span data-stu-id="73685-211">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="73685-212">Seleccione para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="73685-212">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="La sección de auditorías superada" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="73685-214">La sección de **auditorías superada**</span><span class="sxs-lookup"><span data-stu-id="73685-214">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="73685-215">Paso 2: experimento</span><span class="sxs-lookup"><span data-stu-id="73685-215">Step 2: Experiment</span></span>   

<span data-ttu-id="73685-216">La sección oportunidades de su informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-216">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="73685-217">En esta sección, implementará los cambios recomendados en el código base, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-217">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="73685-218">Habilitar compresión de texto</span><span class="sxs-lookup"><span data-stu-id="73685-218">Enable text compression</span></span>   

<span data-ttu-id="73685-219">El informe dice que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-219">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="73685-220">Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-220">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="73685-221">La compresión de texto es cuando se reduce, o comprime, el tamaño de un archivo de texto antes de enviarlo a través de la red.</span><span class="sxs-lookup"><span data-stu-id="73685-221">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="73685-222">Tipo de cómo puede comprimir una carpeta antes de enviarle un mensaje de correo electrónico para reducir el tamaño.</span><span class="sxs-lookup"><span data-stu-id="73685-222">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="73685-223">Antes de habilitar la compresión, hay un par de maneras de comprobar manualmente si los recursos de texto están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="73685-223">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="73685-224">Seleccione la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="73685-224">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panel red" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="73685-226">Panel **red**</span><span class="sxs-lookup"><span data-stu-id="73685-226">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-227">Seleccione el icono de **configuración de red** .</span><span class="sxs-lookup"><span data-stu-id="73685-227">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="73685-228">Seleccione la casilla **usar filas de solicitudes grandes** .</span><span class="sxs-lookup"><span data-stu-id="73685-228">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="73685-229">Aumenta el alto de las filas de la tabla de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="73685-229">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Filas grandes en la tabla solicitudes de red" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="73685-231">Filas grandes en la tabla solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="73685-231">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-232">Si no ve la columna **tamaño** en la tabla de solicitudes de red, haga clic en el encabezado de tabla y, a continuación, seleccione **tamaño**.</span><span class="sxs-lookup"><span data-stu-id="73685-232">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="73685-233">Cada celda de **tamaño** muestra dos valores.</span><span class="sxs-lookup"><span data-stu-id="73685-233">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="73685-234">El valor superior es el tamaño del recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="73685-234">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="73685-235">El valor inferior es el tamaño del recurso sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="73685-235">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="73685-236">Si los dos valores son iguales, el recurso no se comprimirá cuando se envíe a través de la red.</span><span class="sxs-lookup"><span data-stu-id="73685-236">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="73685-237">Por ejemplo, en la ilustración anterior, los valores superiores e inferiores de `bundle.js` is `1.2 MB` y `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="73685-237">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="73685-238">Para comprobar la compresión, inspeccione los encabezados HTTP de un recurso:</span><span class="sxs-lookup"><span data-stu-id="73685-238">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="73685-239">Seleccione **bundle.js**.</span><span class="sxs-lookup"><span data-stu-id="73685-239">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="73685-240">Seleccione la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="73685-240">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="La pestaña encabezados" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="73685-242">La pestaña **encabezados**</span><span class="sxs-lookup"><span data-stu-id="73685-242">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-243">Busque un encabezado en la sección de **encabezados de respuesta** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="73685-243">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="73685-244">No debe ver ninguno, lo que significa que `bundle.js` no se ha comprimido.</span><span class="sxs-lookup"><span data-stu-id="73685-244">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="73685-245">Cuando se comprime un recurso, este encabezado suele establecerse en `gzip` , `deflate` o `br` .</span><span class="sxs-lookup"><span data-stu-id="73685-245">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="73685-246">Vea las [directivas][MDNContentEncodingDirectives] para obtener una explicación de estos valores.</span><span class="sxs-lookup"><span data-stu-id="73685-246">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="73685-247">Es suficiente con las explicaciones.</span><span class="sxs-lookup"><span data-stu-id="73685-247">Enough with the explanations.</span></span>  <span data-ttu-id="73685-248">Para hacer algunos cambios.</span><span class="sxs-lookup"><span data-stu-id="73685-248">Time to make some changes!</span></span>  <span data-ttu-id="73685-249">Habilite la compresión de texto agregando un par de líneas de código:</span><span class="sxs-lookup"><span data-stu-id="73685-249">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="73685-250">En la pestaña Editor, haga clic en **server.js**.</span><span class="sxs-lookup"><span data-stu-id="73685-250">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modificar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="73685-252">Editar</span><span class="sxs-lookup"><span data-stu-id="73685-252">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-253">Agregue el código siguiente a **server.js**.</span><span class="sxs-lookup"><span data-stu-id="73685-253">Add the following code to **server.js**.</span></span>  <span data-ttu-id="73685-254">Asegúrate de poner `app.use(compression())` antes `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="73685-254">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="73685-255">Normalmente, tiene que instalar el `compression` paquete a través de algo similar `npm i -S compression` , pero esto ya se ha hecho para usted.</span><span class="sxs-lookup"><span data-stu-id="73685-255">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="73685-256">Espere a que se implemente la nueva compilación del sitio.</span><span class="sxs-lookup"><span data-stu-id="73685-256">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="73685-257">La animación más sofisticada junto a **herramientas** significa que el sitio se vuelve a generar y a implementar.</span><span class="sxs-lookup"><span data-stu-id="73685-257">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="73685-258">El cambio está listo cuando la animación junto a **herramientas** desaparece.</span><span class="sxs-lookup"><span data-stu-id="73685-258">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="73685-259">Seleccione **Mostrar** y vuelva a seleccionar **una nueva ventana** .</span><span class="sxs-lookup"><span data-stu-id="73685-259">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="73685-260">Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:</span><span class="sxs-lookup"><span data-stu-id="73685-260">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="73685-261">Vuelva a la pestaña demo y vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="73685-261">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="73685-262">La columna **tamaño** debería mostrar ahora dos valores diferentes para recursos de texto como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="73685-262">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="73685-263">En la ilustración siguiente, el valor superior de `256 KB` para `bundle.js` es el tamaño del archivo que se envió a través de la red y el valor inferior de `1.2 MB` es el tamaño de archivo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="73685-263">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La columna tamaño muestra ahora 2 valores diferentes para los recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="73685-265">La columna **tamaño** muestra ahora 2 valores diferentes para los recursos de texto</span><span class="sxs-lookup"><span data-stu-id="73685-265">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-266">La sección de **encabezados de respuesta** de `bundle.js` ahora debe incluir un `content-encoding: gzip` encabezado.</span><span class="sxs-lookup"><span data-stu-id="73685-266">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="73685-268">La sección de **encabezados de respuesta** ahora contiene un encabezado de codificación de contenido</span><span class="sxs-lookup"><span data-stu-id="73685-268">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-269">Audite de nuevo la página para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:</span><span class="sxs-lookup"><span data-stu-id="73685-269">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="73685-270">Seleccione la pestaña **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="73685-270">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="73685-271">Seleccione **realizar una auditoría** \ ( ![ realizar una auditoría ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="73685-271">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="73685-272">Deje la configuración igual que antes.</span><span class="sxs-lookup"><span data-stu-id="73685-272">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="73685-273">Seleccione **Ejecutar auditoría**.</span><span class="sxs-lookup"><span data-stu-id="73685-273">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Un informe de auditoría después de habilitar la compresión de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="73685-275">Un informe de auditoría después de habilitar la compresión de texto</span><span class="sxs-lookup"><span data-stu-id="73685-275">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="73685-276">La puntuación de rendimiento general debería haber aumentado, lo que significa que el sitio se está acelerando.</span><span class="sxs-lookup"><span data-stu-id="73685-276">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="73685-277">Compresión de texto en el mundo real</span><span class="sxs-lookup"><span data-stu-id="73685-277">Text compression in the real world</span></span>   

<span data-ttu-id="73685-278">La mayoría de los servidores realmente tienen soluciones sencillas como esta para habilitar la compresión.</span><span class="sxs-lookup"><span data-stu-id="73685-278">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="73685-279">Solo tiene que hacer una búsqueda para configurar cualquier servidor que use para comprimir texto.</span><span class="sxs-lookup"><span data-stu-id="73685-279">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="73685-280">Cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="73685-280">Resize images</span></span>   

<span data-ttu-id="73685-281">El informe indica que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-281">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="73685-282">Cambiar el tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.</span><span class="sxs-lookup"><span data-stu-id="73685-282">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="73685-283">Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, no hay ningún punto para enviar una imagen de ancho de 1500 píxeles.</span><span class="sxs-lookup"><span data-stu-id="73685-283">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="73685-284">Lo ideal es que envíes una imagen de ancho de 500 píxeles, como máximo.</span><span class="sxs-lookup"><span data-stu-id="73685-284">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="73685-285">En el informe, haga clic en **evitar cargas de red enormes** para ver las imágenes que se deben cambiar de tamaño.</span><span class="sxs-lookup"><span data-stu-id="73685-285">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="73685-286">Parece ser que 2 de los archivos jpg superan 2000 KB, lo cual es más grande de lo necesario.</span><span class="sxs-lookup"><span data-stu-id="73685-286">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="73685-287">De nuevo en la pestaña Editor, Abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="73685-287">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="73685-288">Reemplazar `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="73685-288">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="73685-289">Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="73685-289">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="73685-290">Audite de nuevo la página para ver cómo este cambio afecta al rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="73685-290">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un informe de auditoría después de cambiar el tamaño de las imágenes" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="73685-292">Un informe de auditoría después de cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="73685-292">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-293">Parece que el cambio sólo tiene un efecto menor en la puntuación de rendimiento general.</span><span class="sxs-lookup"><span data-stu-id="73685-293">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="73685-294">Sin embargo, un elemento que indica que la puntuación no se muestra claramente es cuántos datos de red está guardando los usuarios.</span><span class="sxs-lookup"><span data-stu-id="73685-294">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="73685-295">El tamaño total de las fotos antiguas ocupaba alrededor de 5,3 megabytes, mientras que ahora solo es de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="73685-295">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="73685-296">Cambiar el tamaño de las imágenes en el mundo real</span><span class="sxs-lookup"><span data-stu-id="73685-296">Resizing images in the real world</span></span>   

<span data-ttu-id="73685-297">En el caso de una aplicación pequeña, realizar un ajuste de tamaño único como este puede ser lo suficientemente bueno.</span><span class="sxs-lookup"><span data-stu-id="73685-297">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="73685-298">Pero para una aplicación de gran tamaño obviamente, esto no es escalable.</span><span class="sxs-lookup"><span data-stu-id="73685-298">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="73685-299">Estas son algunas estrategias para administrar imágenes en aplicaciones de gran tamaño:</span><span class="sxs-lookup"><span data-stu-id="73685-299">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="73685-300">Cambie el tamaño de las imágenes durante el proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="73685-300">Resize images during your build process.</span></span>  
*   <span data-ttu-id="73685-301">Cree varios tamaños de cada imagen durante el proceso de compilación y, a continuación, utilícelos `srcset` en el código.</span><span class="sxs-lookup"><span data-stu-id="73685-301">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="73685-302">En tiempo de ejecución, el explorador se ocupa de elegir el tamaño más adecuado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73685-302">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="73685-303">Use una CDN de imagen que le permita cambiar el tamaño de una imagen dinámicamente cuando la solicite.</span><span class="sxs-lookup"><span data-stu-id="73685-303">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="73685-304">Como mínimo, optimiza cada imagen.</span><span class="sxs-lookup"><span data-stu-id="73685-304">At the very least, optimize each image.</span></span>  <span data-ttu-id="73685-305">Esto puede crear enormes descuentos.</span><span class="sxs-lookup"><span data-stu-id="73685-305">This may create huge savings.</span></span>  
  <span data-ttu-id="73685-306">La optimización es cuando se ejecuta una imagen a través de un programa especial que reduce el tamaño del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="73685-306">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="73685-307">Para obtener más información, consulta la [optimización básica de imágenes][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="73685-307">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="73685-308">Eliminar recursos de bloqueo de procesamiento</span><span class="sxs-lookup"><span data-stu-id="73685-308">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="73685-309">El último informe indica que la eliminación de recursos de bloqueo de procesamiento es ahora la mayor oportunidad.</span><span class="sxs-lookup"><span data-stu-id="73685-309">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="73685-310">Un recurso de bloqueo de representación es un archivo de JavaScript o CSS externo que el explorador debe descargar, analizar y ejecutar antes de mostrar la página.</span><span class="sxs-lookup"><span data-stu-id="73685-310">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="73685-311">El objetivo es ejecutar solo el código CSS básico y JavaScript necesario para mostrar la página correctamente.</span><span class="sxs-lookup"><span data-stu-id="73685-311">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="73685-312">La primera tarea, a continuación, es buscar código que no es necesario ejecutar en la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-312">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="73685-313">Seleccione **eliminar recursos de bloqueo de procesamiento** para ver los recursos que están bloqueando:</span><span class="sxs-lookup"><span data-stu-id="73685-313">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="73685-314">y `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="73685-314">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Más información sobre la oportunidad eliminar recursos de bloqueo de procesamiento" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="73685-316">Más información sobre la oportunidad **eliminar recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="73685-316">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-317">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, comience a escribir `Coverage` y, a continuación, seleccione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="73685-317">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abrir el menú de comandos desde el panel auditorías" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="73685-319">Abrir el menú de comandos desde el panel **auditorías**</span><span class="sxs-lookup"><span data-stu-id="73685-319">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="La ficha cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="73685-321">La ficha **cobertura**</span><span class="sxs-lookup"><span data-stu-id="73685-321">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-322">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="73685-322">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="73685-323">La pestaña **cobertura** proporciona una descripción general de la parte del código de `bundle.js` , `jquery.js` y `lodash.js` se ejecuta mientras se carga la página.</span><span class="sxs-lookup"><span data-stu-id="73685-323">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="73685-324">En la ilustración siguiente, unos 76% y un 30% de los archivos de jQuery y Lodash no se usan, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="73685-324">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="El informe de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="73685-326">El informe de cobertura</span><span class="sxs-lookup"><span data-stu-id="73685-326">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-327">Seleccione la fila **jquery.js** .</span><span class="sxs-lookup"><span data-stu-id="73685-327">Select the **jquery.js** row.</span></span>  <span data-ttu-id="73685-328">DevTools abre el archivo en el panel fuentes.</span><span class="sxs-lookup"><span data-stu-id="73685-328">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="73685-329">Se ejecutó una línea de código si tiene una barra azul al lado.</span><span class="sxs-lookup"><span data-stu-id="73685-329">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="73685-330">Una barra roja significa que no se ha ejecutado y, por supuesto, no es necesaria en la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-330">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Visualización del archivo jQuery en el panel orígenes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="73685-332">Visualización del archivo jQuery en el panel **orígenes**</span><span class="sxs-lookup"><span data-stu-id="73685-332">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-333">Desplácese un poco por el código jQuery.</span><span class="sxs-lookup"><span data-stu-id="73685-333">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="73685-334">Algunas de las líneas que reciben "ejecutar" son realmente solo Comentarios.</span><span class="sxs-lookup"><span data-stu-id="73685-334">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="73685-335">La ejecución de este código a través de un minifier que elimina los comentarios es otra forma de reducir el tamaño de este archivo.</span><span class="sxs-lookup"><span data-stu-id="73685-335">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="73685-336">En Resumen, cuando está trabajando con su propio código, la pestaña cobertura le ayuda a analizar el código, línea por línea, y solo envía el código necesario para la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-336">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="73685-337">¿Los `jquery.js` archivos y son `lodash.js` necesarios para cargar la página?</span><span class="sxs-lookup"><span data-stu-id="73685-337">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="73685-338">La pestaña bloqueo de solicitud muestra lo que sucede cuando los recursos no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="73685-338">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="73685-339">Seleccione la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="73685-339">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="73685-340">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para volver a abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="73685-340">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="73685-341">Comience `blocking` a escribir y, a continuación, seleccione **Mostrar bloqueo de solicitud**.</span><span class="sxs-lookup"><span data-stu-id="73685-341">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="La ficha solicitar bloqueo" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="73685-343">La ficha **solicitar bloqueo**</span><span class="sxs-lookup"><span data-stu-id="73685-343">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-344">Seleccione **Agregar patrón** \ ( ![ Agregar patrón ][ImageAddPatternIcon] \), escriba `/libs/*` y, a continuación, presione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="73685-344">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Agregar un patrón para bloquear cualquier solicitud al directorio de bibliotecas" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="73685-346">Agregar un patrón para bloquear cualquier solicitud al `libs` directorio</span><span class="sxs-lookup"><span data-stu-id="73685-346">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-347">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="73685-347">Refresh the page.</span></span>  <span data-ttu-id="73685-348">Las solicitudes jQuery y Lodash son rojas, lo que significa que las solicitudes se han bloqueado.</span><span class="sxs-lookup"><span data-stu-id="73685-348">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="73685-349">Aún se carga la página y es interactiva, por lo que parece que no se necesitan estos recursos.</span><span class="sxs-lookup"><span data-stu-id="73685-349">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="El panel red muestra que las solicitudes han sido bloqueadas" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="73685-351">El panel **red** muestra que las solicitudes han sido bloqueadas</span><span class="sxs-lookup"><span data-stu-id="73685-351">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-352">Seleccione **quitar todos los patrones** \ ( ![ quitar todos los patrones ][ImageRemoveIcon] \) para eliminar el `/libs/*` patrón de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="73685-352">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="73685-353">En general, la pestaña bloqueo de solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="73685-353">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="73685-354">Ahora, quite las referencias a estos archivos del código y audite de nuevo la página:</span><span class="sxs-lookup"><span data-stu-id="73685-354">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="73685-355">De nuevo en la pestaña Editor, Abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="73685-355">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="73685-356">Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="73685-356">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="73685-357">Espere a que el sitio se vuelva a compilar y a implementar.</span><span class="sxs-lookup"><span data-stu-id="73685-357">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="73685-358">Audite la página de nuevo desde el panel **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="73685-358">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="73685-359">Tu puntuación general debería haber mejorado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="73685-359">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un informe de auditoría después de quitar los recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="73685-361">Un informe de **Auditoría** después de quitar los recursos de bloqueo de representación</span><span class="sxs-lookup"><span data-stu-id="73685-361">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="73685-362">Optimizar la ruta de representación crítica en el mundo real</span><span class="sxs-lookup"><span data-stu-id="73685-362">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="73685-363">La **ruta de representación crítica** se refiere al código que necesita para cargar una página.</span><span class="sxs-lookup"><span data-stu-id="73685-363">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="73685-364">En general, para acelerar la carga de páginas solo tienes que enviar código crítico durante la carga de la página y, a continuación, cargar de forma diferida todo lo demás.</span><span class="sxs-lookup"><span data-stu-id="73685-364">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="73685-365">Es improbable que encuentre secuencias de comandos que pueda quitar de forma inadecuada, pero es posible que encuentre muchas secuencias de comandos que no necesita solicitar durante la carga de la página y que, en su lugar, las solicite.</span><span class="sxs-lookup"><span data-stu-id="73685-365">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="73685-366">Si está usando un marco, compruebe si tiene un modo de producción.</span><span class="sxs-lookup"><span data-stu-id="73685-366">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="73685-367">Este modo puede usar una característica, como el [agitador de árboles][WebpackTreeShaking] , para eliminar el código innecesario que está bloqueando el procesamiento crítico.</span><span class="sxs-lookup"><span data-stu-id="73685-367">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="73685-368">Hacer menos trabajo del subproceso principal</span><span class="sxs-lookup"><span data-stu-id="73685-368">Do less main thread work</span></span>   

<span data-ttu-id="73685-369">Su último informe muestra algunos ahorros potenciales menores en la sección oportunidades, pero si ve en la sección diagnósticos, parece que la mayor parte de la actividad principal es la actividad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="73685-369">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="73685-370">El subproceso principal es el lugar donde el explorador hace la mayor parte del trabajo necesario para mostrar una página, como analizar y ejecutar HTML, CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73685-370">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="73685-371">El objetivo es usar el panel rendimiento para analizar qué trabajo está haciendo el subproceso principal mientras se carga la página y buscar formas de aplazar o quitar el trabajo innecesario.</span><span class="sxs-lookup"><span data-stu-id="73685-371">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="73685-372">Seleccione la pestaña **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="73685-372">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="73685-373">Seleccione **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="73685-373">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="73685-374">Configure la **red** como **3G lento** y **CPU** a **6X lentitud**.</span><span class="sxs-lookup"><span data-stu-id="73685-374">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="73685-375">Por lo general, los dispositivos móviles tienen más restricciones de hardware que los equipos portátiles o de escritorio, por lo que esta configuración le permite experimentar la carga de la página como si estuviera usando un dispositivo menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="73685-375">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="73685-376">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="73685-376">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="73685-377">DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargarla.</span><span class="sxs-lookup"><span data-stu-id="73685-377">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="73685-378">Esta visualización se conoce como la **traza**.</span><span class="sxs-lookup"><span data-stu-id="73685-378">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Seguimiento del panel rendimiento de la carga de páginas" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="73685-380">Seguimiento del panel **rendimiento** de la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="73685-380">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-381">La traza muestra la actividad cronológicamente, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="73685-381">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="73685-382">Los gráficos de CPS, CPU y NET de la parte superior le ofrecen una descripción general de los fotogramas por segundo, la actividad de la CPU y la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="73685-382">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="73685-383">El bloque de amarillo seleccionado que aparece en la ilustración después de lo siguiente, la CPU estaba completamente ocupada por la actividad de scripting.</span><span class="sxs-lookup"><span data-stu-id="73685-383">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="73685-384">Esta es una pista de que puede acelerar la carga de la página haciendo menos trabajo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73685-384">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="La sección información general de la traza" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="73685-386">La sección información general de la traza</span><span class="sxs-lookup"><span data-stu-id="73685-386">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="73685-387">Investigue el seguimiento para encontrar formas de hacer que el trabajo de JavaScript sea menor:</span><span class="sxs-lookup"><span data-stu-id="73685-387">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="73685-388">Seleccione la sección **intervalos** para expandirlo.</span><span class="sxs-lookup"><span data-stu-id="73685-388">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="73685-389">Basándose en el hecho de que puede haber una gran cantidad de medidas de [intervalos][MDNUserTimingApi] de reAct, parece que la aplicación de Tony usa el modo de desarrollo de reAct.</span><span class="sxs-lookup"><span data-stu-id="73685-389">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="73685-390">El cambio al modo de producción de reAct puede dar lugar a un resultado de fácil rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73685-390">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="La sección intervalos" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="73685-392">La sección **intervalos**</span><span class="sxs-lookup"><span data-stu-id="73685-392">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-393">Vuelva a seleccionar los **intervalos** para contraer la sección.</span><span class="sxs-lookup"><span data-stu-id="73685-393">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="73685-394">Examinar la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="73685-394">Browse the **Main** section.</span></span>  <span data-ttu-id="73685-395">En esta sección se muestra un registro cronológico de la actividad principal de la conversación, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="73685-395">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="73685-396">El eje y (de arriba a abajo) muestra por qué se produjeron eventos.</span><span class="sxs-lookup"><span data-stu-id="73685-396">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="73685-397">Por ejemplo, en el figyre después de lo siguiente, el `Evaluate Script` evento ha provocado la ejecución de la `(anonymous)` función, que ha provocado que `(anonymous)` se ejecutara, `__webpack__require__` y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="73685-397">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="La sección principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="73685-399">La sección **principal**</span><span class="sxs-lookup"><span data-stu-id="73685-399">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73685-400">Desplácese hacia abajo hasta la parte inferior de la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="73685-400">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="73685-401">Cuando se usa un marco, la mayor parte de la actividad superior está causada por el marco de trabajo, que normalmente está fuera de su control.</span><span class="sxs-lookup"><span data-stu-id="73685-401">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="73685-402">La actividad causada por la aplicación suele estar en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="73685-402">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="73685-403">En esta aplicación, parece que una función llamada `App` está causando un gran número de solicitudes a una `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="73685-403">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="73685-404">Suena como Tony podría estar usando los dispositivos de sus ventiladores para minar cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="73685-404">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Desplazarse por la actividad de mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="73685-406">Desplazar el puntero sobre la `mineBitcoin` actividad</span><span class="sxs-lookup"><span data-stu-id="73685-406">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="73685-407">A pesar de que las solicitudes que el marco de trabajo realiza generalmente están fuera de su control, a veces puede estructurar la aplicación de forma que el marco de trabajo se ejecute ineficazmente.</span><span class="sxs-lookup"><span data-stu-id="73685-407">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="73685-408">Reestructurar la aplicación para usar el marco de forma eficaz es una forma de hacer menos trabajo de los subprocesos principales.</span><span class="sxs-lookup"><span data-stu-id="73685-408">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="73685-409">Sin embargo, esto requiere un conocimiento profundo de cómo funciona el marco y qué tipo de cambios se realizan en el código propio para poder usar el marco de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="73685-409">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="73685-410">Expanda la sección de **abajo** .</span><span class="sxs-lookup"><span data-stu-id="73685-410">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="73685-411">Esta pestaña desglosa qué actividades ocuparon la mayor parte del tiempo.</span><span class="sxs-lookup"><span data-stu-id="73685-411">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="73685-412">Si no ve nada en la sección de la parte inferior, haga clic en la etiqueta de la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="73685-412">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="73685-413">En la sección de la **parte inferior** se muestra solo la información de cualquier actividad o grupo de actividades que haya seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="73685-413">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="73685-414">Por ejemplo, si hizo clic en una de las `mineBitcoin` actividades, la sección de **abajo** se mostrará solo la información de esa actividad.</span><span class="sxs-lookup"><span data-stu-id="73685-414">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="La pestaña abajo" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="73685-416">La pestaña **abajo**</span><span class="sxs-lookup"><span data-stu-id="73685-416">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-417">La columna **Self Time** muestra la cantidad de tiempo que se dedicó directamente en cada actividad.</span><span class="sxs-lookup"><span data-stu-id="73685-417">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="73685-418">Por ejemplo, en la siguiente ilustración, se dedicó un 63% del tiempo de rosca principal en la `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="73685-418">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="73685-419">Tiempo para ver si usar el modo de producción y reducir la actividad de JavaScript puede acelerar la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-419">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="73685-420">Empezar con el modo de producción:</span><span class="sxs-lookup"><span data-stu-id="73685-420">Start with production mode:</span></span>  

1.  <span data-ttu-id="73685-421">En la pestaña Editor, Abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="73685-421">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="73685-422">Cambiar `"mode":"development"` a `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="73685-422">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="73685-423">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="73685-423">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="73685-424">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="73685-424">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Un informe de auditoría después de configurar WebPack para usar el modo de producción" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="73685-426">Un informe de auditoría después de configurar WebPack para usar el modo de producción</span><span class="sxs-lookup"><span data-stu-id="73685-426">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-427">Reduzca la actividad de JavaScript eliminando la solicitud a `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="73685-427">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="73685-428">En la pestaña Editor, Abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="73685-428">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="73685-429">Comente la solicitud para `this.mineBitcoin(1500)` en el `constructor` .</span><span class="sxs-lookup"><span data-stu-id="73685-429">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="73685-430">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="73685-430">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="73685-431">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="73685-431">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un informe de auditoría después de quitar el trabajo de JavaScript innecesario" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="73685-433">Un informe de auditoría después de quitar el trabajo de JavaScript innecesario</span><span class="sxs-lookup"><span data-stu-id="73685-433">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="73685-434">Parece que el último cambio causó un aumento de rendimiento masivo.</span><span class="sxs-lookup"><span data-stu-id="73685-434">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="73685-435">En esta sección se ofreció una breve introducción al panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73685-435">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="73685-436">Consulte [referencia de análisis de rendimiento][DevtoolsEvaluatePerformanceReference] para obtener más información sobre cómo analizar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="73685-436">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="73685-437">Trabajar con menos subprocesos principales en el mundo real</span><span class="sxs-lookup"><span data-stu-id="73685-437">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="73685-438">En general, el panel **rendimiento** es la manera más común de comprender qué actividad hace el sitio mientras se carga, y buscar formas de quitar actividades innecesarias.</span><span class="sxs-lookup"><span data-stu-id="73685-438">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="73685-439">Si prefiere un método que se sienta `console.log()` de la mejor manera, la [API de temporización de usuario][MDNUserTimingApi] le permite marcar arbitrariamente determinadas fases del ciclo de vida de la aplicación para realizar un seguimiento del tiempo que toma cada una de esas fases.</span><span class="sxs-lookup"><span data-stu-id="73685-439">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="73685-440">Resumen</span><span class="sxs-lookup"><span data-stu-id="73685-440">Summary</span></span>   

*   <span data-ttu-id="73685-441">Siempre que lo establezca para optimizar el rendimiento de la carga de un sitio, empiece siempre con una auditoría.</span><span class="sxs-lookup"><span data-stu-id="73685-441">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="73685-442">La auditoría establece una línea de base y le ofrece sugerencias sobre cómo mejorar.</span><span class="sxs-lookup"><span data-stu-id="73685-442">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="73685-443">Realice un cambio a la vez y audite la página después de cada cambio para ver cómo afecta el cambio en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73685-443">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referencia del análisis de rendimiento | Microsoft docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introducción a la clase de desarrollo web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimización de imagen esencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directivas-codificación de contenido | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de temporización de usuario | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Sacudida de árboles | paquete de WebPack"  

> [!NOTE]
> <span data-ttu-id="73685-450">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="73685-450">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="73685-451">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="73685-451">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="73685-453">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="73685-453">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
