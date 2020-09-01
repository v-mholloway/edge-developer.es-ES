---
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984811"
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





# <span data-ttu-id="45375-103">Optimizar la velocidad del sitio web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="45375-103">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="45375-104">Objetivo del tutorial</span><span class="sxs-lookup"><span data-stu-id="45375-104">Goal of tutorial</span></span>  

<span data-ttu-id="45375-105">En este tutorial aprenderás a usar Microsoft Edge DevTools para encontrar formas de cargar tus sitios web más rápido.</span><span class="sxs-lookup"><span data-stu-id="45375-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="45375-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="45375-106">Prerequisites</span></span>  

*   <span data-ttu-id="45375-107">Debe tener experiencia básica de desarrollo web, similar a lo que enseñamos esta [Introducción a la clase de desarrollo web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="45375-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="45375-108">No es necesario que sepa nada sobre el rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="45375-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="45375-109">Puede obtener más información en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="45375-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="45375-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="45375-110">Introduction</span></span>   

<span data-ttu-id="45375-111">Es Tony.</span><span class="sxs-lookup"><span data-stu-id="45375-111">This is Tony.</span></span>  <span data-ttu-id="45375-112">Tony es muy famoso en el gato de la sociedad.</span><span class="sxs-lookup"><span data-stu-id="45375-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="45375-113">Ha creado un sitio web para que sus ventiladores puedan conocer sus alimentos favoritos.</span><span class="sxs-lookup"><span data-stu-id="45375-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="45375-114">Sus ventiladores adoran el sitio, pero Tony mantiene las quejas auditivas que el sitio carga lentamente.</span><span class="sxs-lookup"><span data-stu-id="45375-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="45375-115">Tony le ha pedido que le ayude a acelerar el sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-115">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony el gato" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="45375-117">Tony el gato</span><span class="sxs-lookup"><span data-stu-id="45375-117">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="45375-118">Paso 1: auditar el sitio</span><span class="sxs-lookup"><span data-stu-id="45375-118">Step 1: Audit the site</span></span>   

<span data-ttu-id="45375-119">Siempre que lo establezca para mejorar el rendimiento de la carga de un sitio, **empiece siempre con una auditoría**.</span><span class="sxs-lookup"><span data-stu-id="45375-119">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="45375-120">La auditoría tiene dos funciones importantes:</span><span class="sxs-lookup"><span data-stu-id="45375-120">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="45375-121">Crea una **línea base** para medir los cambios posteriores.</span><span class="sxs-lookup"><span data-stu-id="45375-121">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="45375-122">Le ofrece **consejos útiles** sobre qué cambios son más impactantes.</span><span class="sxs-lookup"><span data-stu-id="45375-122">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="45375-123">Configuración</span><span class="sxs-lookup"><span data-stu-id="45375-123">Set up</span></span>   

<span data-ttu-id="45375-124">En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.</span><span class="sxs-lookup"><span data-stu-id="45375-124">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="45375-125">[Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="45375-125">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="45375-126">Esta pestaña se conoce como la **pestaña Editor**.</span><span class="sxs-lookup"><span data-stu-id="45375-126">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Ficha Editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="45375-128">**Ficha Editor**</span><span class="sxs-lookup"><span data-stu-id="45375-128">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-129">Seleccione **Tony**.</span><span class="sxs-lookup"><span data-stu-id="45375-129">Select **tony**.</span></span>  <span data-ttu-id="45375-130">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="45375-130">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="El menú que aparece después de hacer clic en Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="45375-132">El menú que aparece después de hacer clic en **Tony**</span><span class="sxs-lookup"><span data-stu-id="45375-132">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-133">Seleccione **proyecto Remix**.</span><span class="sxs-lookup"><span data-stu-id="45375-133">Select **Remix Project**.</span></span>  <span data-ttu-id="45375-134">El nombre del proyecto cambia de **Tony** a algún nombre generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="45375-134">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="45375-135">Ahora tiene su propia copia modificable del código.</span><span class="sxs-lookup"><span data-stu-id="45375-135">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="45375-136">Más adelante, puedes realizar cambios en este código.</span><span class="sxs-lookup"><span data-stu-id="45375-136">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="45375-137">Seleccione **Mostrar** y seleccione **en una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="45375-137">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="45375-138">La demostración se abre en una nueva pestaña.  Esta pestaña se conoce como la **pestaña demo**.  Es posible que el sitio tarde un rato en cargarse.</span><span class="sxs-lookup"><span data-stu-id="45375-138">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="La ficha demo" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="45375-140">La ficha demo</span><span class="sxs-lookup"><span data-stu-id="45375-140">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-141">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="45375-141">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="45375-142">Microsoft Edge DevTools se abre junto con la demostración.</span><span class="sxs-lookup"><span data-stu-id="45375-142">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools y la demostración" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="45375-144">DevTools y la demostración</span><span class="sxs-lookup"><span data-stu-id="45375-144">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-145">Para el resto de las capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="45375-145">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="45375-146">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú comando, escriba `Undock` y, a continuación, seleccione **desacoplar en ventana independiente**.</span><span class="sxs-lookup"><span data-stu-id="45375-146">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools desacoplado" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="45375-148">DevTools desacoplado</span><span class="sxs-lookup"><span data-stu-id="45375-148">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="45375-149">Establecer una línea base</span><span class="sxs-lookup"><span data-stu-id="45375-149">Establish a baseline</span></span>   

<span data-ttu-id="45375-150">La línea base es un registro de cómo se realizó el sitio antes de realizar alguna mejora en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45375-150">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="45375-151">Seleccione la pestaña **auditorías** .  Es posible que esté oculto detrás **del** botón \ ( ![ más paneles ][ImageMorePanelsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="45375-151">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="45375-152">Hay un Lighthouse en este panel porque el proyecto que alimenta el panel auditoría se denomina **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="45375-152">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Panel auditorías" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="45375-154">Panel **auditorías**</span><span class="sxs-lookup"><span data-stu-id="45375-154">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="45375-155">Ajuste las opciones de configuración de auditoría a las de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="45375-155">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="45375-156">A continuación se explican las diferentes opciones:</span><span class="sxs-lookup"><span data-stu-id="45375-156">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="45375-157">**Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="45375-157">**Device**.</span></span>  <span data-ttu-id="45375-158">Configuración para **dispositivos móviles** cambia la cadena de agente de usuario y simula un área de visualización móvil.</span><span class="sxs-lookup"><span data-stu-id="45375-158">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="45375-159">La configuración en el **escritorio** simplemente deshabilita los cambios en el **teléfono móvil** .</span><span class="sxs-lookup"><span data-stu-id="45375-159">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="45375-160">**Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="45375-160">**Audits**.</span></span>  <span data-ttu-id="45375-161">Si deshabilita una categoría, evitará que el panel auditoría las ejecute y las excluirá de su informe.</span><span class="sxs-lookup"><span data-stu-id="45375-161">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="45375-162">Deje las otras categorías habilitadas si desea ver los tipos de recomendaciones proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="45375-162">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="45375-163">Al deshabilitar las categorías, se acelera ligeramente el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="45375-163">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="45375-164">**Limitación**.</span><span class="sxs-lookup"><span data-stu-id="45375-164">**Throttling**.</span></span>  <span data-ttu-id="45375-165">Configurada para **simular lentitud de 4G, con una ralentización** de la CPU de 4x simula las condiciones típicas de la navegación en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="45375-165">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="45375-166">Se denomina "simulado" porque en realidad el panel auditorías no se limita durante el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="45375-166">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="45375-167">En su lugar, simplemente extrapola cuánto tiempo tardará la página en cargarse en condiciones móviles.</span><span class="sxs-lookup"><span data-stu-id="45375-167">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="45375-168">Por otro lado, la opción de configuración **aplicado** , limita la CPU y la red, con la compensación de un proceso de auditoría más largo.</span><span class="sxs-lookup"><span data-stu-id="45375-168">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="45375-169">**Borrar almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="45375-169">**Clear Storage**.</span></span>  <span data-ttu-id="45375-170">Al habilitar esta casilla, se borra todo el almacenamiento asociado a la página antes de cada auditoría.</span><span class="sxs-lookup"><span data-stu-id="45375-170">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="45375-171">Deje esta configuración activada si desea auditar la experiencia de los visitantes por primera vez en su sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-171">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="45375-172">Deshabilite esta configuración cuando quiera la experiencia de repetición de la visita.</span><span class="sxs-lookup"><span data-stu-id="45375-172">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="45375-173">Seleccione **Ejecutar Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="45375-173">Select **Run Audits**.</span></span>  <span data-ttu-id="45375-174">Después de 10 a 30 segundos, el panel auditoría muestra un informe del rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-174">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Informe para el panel auditoría del rendimiento del sitio" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="45375-176">Informe para el panel auditoría del rendimiento del sitio</span><span class="sxs-lookup"><span data-stu-id="45375-176">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="45375-177">Control de errores de informe</span><span class="sxs-lookup"><span data-stu-id="45375-177">Handling report errors</span></span>   

<span data-ttu-id="45375-178">Si alguna vez recibe un error en el informe del panel auditorías, pruebe a ejecutar la pestaña demostración desde una ventana **InPrivate** sin ninguna otra pestaña abierta.</span><span class="sxs-lookup"><span data-stu-id="45375-178">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="45375-179">Esto asegura que está ejecutando Microsoft Edge desde un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="45375-179">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="45375-180">Las extensiones de Microsoft Edge en particular suelen interferir con el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="45375-180">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="45375-181">Comprender el informe</span><span class="sxs-lookup"><span data-stu-id="45375-181">Understand your report</span></span>   

<span data-ttu-id="45375-182">El número que aparece en la parte superior del informe es la puntuación de rendimiento general para el sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-182">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="45375-183">Después, a medida que haga cambios en el código, debería ver que este número ha aumentado.</span><span class="sxs-lookup"><span data-stu-id="45375-183">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="45375-184">Una puntuación mayor supone un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45375-184">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="La puntuación general de rendimiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="45375-186">La puntuación general de rendimiento</span><span class="sxs-lookup"><span data-stu-id="45375-186">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="45375-187">La sección de **métricas** proporciona medidas cuantitativas en el rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-187">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="45375-188">Cada métrica proporciona información sobre un aspecto diferente del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45375-188">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="45375-189">Por ejemplo, la **primera pintura con contenido** le indica cuando el contenido se pinta por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que el tiempo de marca **interactiva** es el punto en el que la página aparece lo suficientemente lista para controlar las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="45375-189">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="La sección métrica" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="45375-191">La sección **métrica**</span><span class="sxs-lookup"><span data-stu-id="45375-191">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="45375-192">Seleccione el botón de alternancia resaltado en la siguiente ilustración para ver una descripción de cada métrica y haga clic en **obtener más información** para leer la documentación de la misma.</span><span class="sxs-lookup"><span data-stu-id="45375-192">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Seleccione el botón de alternancia resaltado para expandir los elementos de métrica" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="45375-194">Seleccione el botón de alternancia resaltado para expandir los elementos de métrica</span><span class="sxs-lookup"><span data-stu-id="45375-194">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="45375-195">A continuación, se muestra una colección de capturas de pantallas en la que se muestra cómo se ha cargado la página.</span><span class="sxs-lookup"><span data-stu-id="45375-195">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de pantallas del aspecto de la página durante la carga" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="45375-197">Capturas de pantallas del aspecto de la página durante la carga</span><span class="sxs-lookup"><span data-stu-id="45375-197">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="45375-198">La sección **oportunidades** proporciona sugerencias específicas sobre cómo mejorar el rendimiento de la carga de esta página específica.</span><span class="sxs-lookup"><span data-stu-id="45375-198">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="La sección oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="45375-200">La sección **oportunidades**</span><span class="sxs-lookup"><span data-stu-id="45375-200">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="45375-201">Seleccione una oportunidad para obtener más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="45375-201">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar la oportunidad de recursos de bloqueo de procesamiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="45375-203">**Eliminar la oportunidad de recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="45375-203">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="45375-204">Seleccione **más información** para ver la documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo corregirla.</span><span class="sxs-lookup"><span data-stu-id="45375-204">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentación de la oportunidad eliminar recursos de bloqueo de procesamiento" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="45375-206">Documentación de la oportunidad **eliminar recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="45375-206">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="45375-207">La sección **diagnósticos** proporciona más información sobre los factores que contribuyen al tiempo de carga de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-207">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="La sección diagnósticos" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="45375-209">La sección **diagnósticos**</span><span class="sxs-lookup"><span data-stu-id="45375-209">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="45375-210">En la sección de **auditorías superada** se muestra lo que el sitio está haciendo correctamente.</span><span class="sxs-lookup"><span data-stu-id="45375-210">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="45375-211">Seleccione para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="45375-211">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="La sección de auditorías superada" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="45375-213">La sección de **auditorías superada**</span><span class="sxs-lookup"><span data-stu-id="45375-213">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="45375-214">Paso 2: experimento</span><span class="sxs-lookup"><span data-stu-id="45375-214">Step 2: Experiment</span></span>   

<span data-ttu-id="45375-215">La sección oportunidades de su informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-215">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="45375-216">En esta sección, implementará los cambios recomendados en el código base, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-216">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="45375-217">Habilitar compresión de texto</span><span class="sxs-lookup"><span data-stu-id="45375-217">Enable text compression</span></span>   

<span data-ttu-id="45375-218">El informe dice que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-218">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="45375-219">Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-219">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="45375-220">La compresión de texto es cuando se reduce, o comprime, el tamaño de un archivo de texto antes de enviarlo a través de la red.</span><span class="sxs-lookup"><span data-stu-id="45375-220">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="45375-221">Tipo de cómo puede comprimir una carpeta antes de enviarle un mensaje de correo electrónico para reducir el tamaño.</span><span class="sxs-lookup"><span data-stu-id="45375-221">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="45375-222">Antes de habilitar la compresión, hay un par de maneras de comprobar manualmente si los recursos de texto están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="45375-222">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="45375-223">Seleccione la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="45375-223">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panel red" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="45375-225">Panel **red**</span><span class="sxs-lookup"><span data-stu-id="45375-225">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-226">Seleccione el icono de **configuración de red** .</span><span class="sxs-lookup"><span data-stu-id="45375-226">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="45375-227">Seleccione la casilla **usar filas de solicitudes grandes** .</span><span class="sxs-lookup"><span data-stu-id="45375-227">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="45375-228">Aumenta el alto de las filas de la tabla de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="45375-228">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Filas grandes en la tabla solicitudes de red" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="45375-230">Filas grandes en la tabla solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="45375-230">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-231">Si no ve la columna **tamaño** en la tabla de solicitudes de red, haga clic en el encabezado de tabla y, a continuación, seleccione **tamaño**.</span><span class="sxs-lookup"><span data-stu-id="45375-231">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="45375-232">Cada celda de **tamaño** muestra dos valores.</span><span class="sxs-lookup"><span data-stu-id="45375-232">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="45375-233">El valor superior es el tamaño del recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="45375-233">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="45375-234">El valor inferior es el tamaño del recurso sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="45375-234">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="45375-235">Si los dos valores son iguales, el recurso no se comprimirá cuando se envíe a través de la red.</span><span class="sxs-lookup"><span data-stu-id="45375-235">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="45375-236">Por ejemplo, en la ilustración anterior, los valores superiores e inferiores de `bundle.js` is `1.2 MB` y `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="45375-236">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="45375-237">Para comprobar la compresión, inspeccione los encabezados HTTP de un recurso:</span><span class="sxs-lookup"><span data-stu-id="45375-237">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="45375-238">Seleccione **bundle.js**.</span><span class="sxs-lookup"><span data-stu-id="45375-238">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="45375-239">Seleccione la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="45375-239">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="La pestaña encabezados" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="45375-241">La pestaña **encabezados**</span><span class="sxs-lookup"><span data-stu-id="45375-241">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-242">Busque un encabezado en la sección de **encabezados de respuesta** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="45375-242">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="45375-243">No debe ver ninguno, lo que significa que `bundle.js` no se ha comprimido.</span><span class="sxs-lookup"><span data-stu-id="45375-243">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="45375-244">Cuando se comprime un recurso, este encabezado suele establecerse en `gzip` , `deflate` o `br` .</span><span class="sxs-lookup"><span data-stu-id="45375-244">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="45375-245">Vea las [directivas][MDNContentEncodingDirectives] para obtener una explicación de estos valores.</span><span class="sxs-lookup"><span data-stu-id="45375-245">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="45375-246">Es suficiente con las explicaciones.</span><span class="sxs-lookup"><span data-stu-id="45375-246">Enough with the explanations.</span></span>  <span data-ttu-id="45375-247">Para hacer algunos cambios.</span><span class="sxs-lookup"><span data-stu-id="45375-247">Time to make some changes!</span></span>  <span data-ttu-id="45375-248">Habilite la compresión de texto agregando un par de líneas de código:</span><span class="sxs-lookup"><span data-stu-id="45375-248">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="45375-249">En la pestaña Editor, haga clic en **server.js**.</span><span class="sxs-lookup"><span data-stu-id="45375-249">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modificar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="45375-251">Editar</span><span class="sxs-lookup"><span data-stu-id="45375-251">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-252">Agregue el código siguiente a **server.js**.</span><span class="sxs-lookup"><span data-stu-id="45375-252">Add the following code to **server.js**.</span></span>  <span data-ttu-id="45375-253">Asegúrate de poner `app.use(compression())` antes `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="45375-253">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="45375-254">Normalmente, tiene que instalar el `compression` paquete a través de algo similar `npm i -S compression` , pero esto ya se ha hecho para usted.</span><span class="sxs-lookup"><span data-stu-id="45375-254">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="45375-255">Espere a que se implemente la nueva compilación del sitio.</span><span class="sxs-lookup"><span data-stu-id="45375-255">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="45375-256">La animación más sofisticada junto a **herramientas** significa que el sitio se vuelve a generar y a implementar.</span><span class="sxs-lookup"><span data-stu-id="45375-256">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="45375-257">El cambio está listo cuando la animación junto a **herramientas** desaparece.</span><span class="sxs-lookup"><span data-stu-id="45375-257">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="45375-258">Seleccione **Mostrar** y vuelva a seleccionar **una nueva ventana** .</span><span class="sxs-lookup"><span data-stu-id="45375-258">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="45375-259">Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:</span><span class="sxs-lookup"><span data-stu-id="45375-259">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="45375-260">Vuelva a la pestaña demo y vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="45375-260">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="45375-261">La columna **tamaño** debería mostrar ahora dos valores diferentes para recursos de texto como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="45375-261">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="45375-262">En la ilustración siguiente, el valor superior de `256 KB` para `bundle.js` es el tamaño del archivo que se envió a través de la red y el valor inferior de `1.2 MB` es el tamaño de archivo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="45375-262">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La columna tamaño muestra ahora 2 valores diferentes para los recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="45375-264">La columna **tamaño** muestra ahora 2 valores diferentes para los recursos de texto</span><span class="sxs-lookup"><span data-stu-id="45375-264">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-265">La sección de **encabezados de respuesta** de `bundle.js` ahora debe incluir un `content-encoding: gzip` encabezado.</span><span class="sxs-lookup"><span data-stu-id="45375-265">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="45375-267">La sección de **encabezados de respuesta** ahora contiene un encabezado de codificación de contenido</span><span class="sxs-lookup"><span data-stu-id="45375-267">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-268">Audite de nuevo la página para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:</span><span class="sxs-lookup"><span data-stu-id="45375-268">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="45375-269">Seleccione la pestaña **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="45375-269">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="45375-270">Seleccione **realizar una auditoría** \ ( ![ realizar una auditoría ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="45375-270">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="45375-271">Deje la configuración igual que antes.</span><span class="sxs-lookup"><span data-stu-id="45375-271">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="45375-272">Seleccione **Ejecutar auditoría**.</span><span class="sxs-lookup"><span data-stu-id="45375-272">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Un informe de auditoría después de habilitar la compresión de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="45375-274">Un informe de auditoría después de habilitar la compresión de texto</span><span class="sxs-lookup"><span data-stu-id="45375-274">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="45375-275">La puntuación de rendimiento general debería haber aumentado, lo que significa que el sitio se está acelerando.</span><span class="sxs-lookup"><span data-stu-id="45375-275">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="45375-276">Compresión de texto en el mundo real</span><span class="sxs-lookup"><span data-stu-id="45375-276">Text compression in the real world</span></span>   

<span data-ttu-id="45375-277">La mayoría de los servidores realmente tienen soluciones sencillas como esta para habilitar la compresión.</span><span class="sxs-lookup"><span data-stu-id="45375-277">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="45375-278">Solo tiene que hacer una búsqueda para configurar cualquier servidor que use para comprimir texto.</span><span class="sxs-lookup"><span data-stu-id="45375-278">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="45375-279">Cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="45375-279">Resize images</span></span>   

<span data-ttu-id="45375-280">El informe indica que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-280">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="45375-281">Cambiar el tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.</span><span class="sxs-lookup"><span data-stu-id="45375-281">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="45375-282">Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, no hay ningún punto para enviar una imagen de ancho de 1500 píxeles.</span><span class="sxs-lookup"><span data-stu-id="45375-282">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="45375-283">Lo ideal es que envíes una imagen de ancho de 500 píxeles, como máximo.</span><span class="sxs-lookup"><span data-stu-id="45375-283">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="45375-284">En el informe, haga clic en **evitar cargas de red enormes** para ver las imágenes que se deben cambiar de tamaño.</span><span class="sxs-lookup"><span data-stu-id="45375-284">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="45375-285">Parece ser que 2 de los archivos jpg superan 2000 KB, lo cual es más grande de lo necesario.</span><span class="sxs-lookup"><span data-stu-id="45375-285">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="45375-286">De nuevo en la pestaña Editor, Abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="45375-286">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="45375-287">Reemplazar `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="45375-287">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="45375-288">Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="45375-288">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="45375-289">Audite de nuevo la página para ver cómo este cambio afecta al rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="45375-289">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un informe de auditoría después de cambiar el tamaño de las imágenes" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="45375-291">Un informe de auditoría después de cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="45375-291">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-292">Parece que el cambio sólo tiene un efecto menor en la puntuación de rendimiento general.</span><span class="sxs-lookup"><span data-stu-id="45375-292">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="45375-293">Sin embargo, un elemento que indica que la puntuación no se muestra claramente es cuántos datos de red está guardando los usuarios.</span><span class="sxs-lookup"><span data-stu-id="45375-293">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="45375-294">El tamaño total de las fotos antiguas ocupaba alrededor de 5,3 megabytes, mientras que ahora solo es de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="45375-294">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="45375-295">Cambiar el tamaño de las imágenes en el mundo real</span><span class="sxs-lookup"><span data-stu-id="45375-295">Resizing images in the real world</span></span>   

<span data-ttu-id="45375-296">En el caso de una aplicación pequeña, realizar un ajuste de tamaño único como este puede ser lo suficientemente bueno.</span><span class="sxs-lookup"><span data-stu-id="45375-296">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="45375-297">Pero para una aplicación de gran tamaño obviamente, esto no es escalable.</span><span class="sxs-lookup"><span data-stu-id="45375-297">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="45375-298">Estas son algunas estrategias para administrar imágenes en aplicaciones de gran tamaño:</span><span class="sxs-lookup"><span data-stu-id="45375-298">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="45375-299">Cambie el tamaño de las imágenes durante el proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="45375-299">Resize images during your build process.</span></span>  
*   <span data-ttu-id="45375-300">Cree varios tamaños de cada imagen durante el proceso de compilación y, a continuación, utilícelos `srcset` en el código.</span><span class="sxs-lookup"><span data-stu-id="45375-300">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="45375-301">En tiempo de ejecución, el explorador se ocupa de elegir el tamaño más adecuado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45375-301">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="45375-302">Use una CDN de imagen que le permita cambiar el tamaño de una imagen dinámicamente cuando la solicite.</span><span class="sxs-lookup"><span data-stu-id="45375-302">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="45375-303">Como mínimo, optimiza cada imagen.</span><span class="sxs-lookup"><span data-stu-id="45375-303">At the very least, optimize each image.</span></span>  <span data-ttu-id="45375-304">Esto puede crear enormes descuentos.</span><span class="sxs-lookup"><span data-stu-id="45375-304">This may create huge savings.</span></span>  
  <span data-ttu-id="45375-305">La optimización es cuando se ejecuta una imagen a través de un programa especial que reduce el tamaño del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="45375-305">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="45375-306">Para obtener más información, consulta la [optimización básica de imágenes][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="45375-306">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="45375-307">Eliminar recursos de bloqueo de procesamiento</span><span class="sxs-lookup"><span data-stu-id="45375-307">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="45375-308">El último informe indica que la eliminación de recursos de bloqueo de procesamiento es ahora la mayor oportunidad.</span><span class="sxs-lookup"><span data-stu-id="45375-308">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="45375-309">Un recurso de bloqueo de representación es un archivo de JavaScript o CSS externo que el explorador debe descargar, analizar y ejecutar antes de mostrar la página.</span><span class="sxs-lookup"><span data-stu-id="45375-309">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="45375-310">El objetivo es ejecutar solo el código CSS básico y JavaScript necesario para mostrar la página correctamente.</span><span class="sxs-lookup"><span data-stu-id="45375-310">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="45375-311">La primera tarea, a continuación, es buscar código que no es necesario ejecutar en la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-311">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="45375-312">Seleccione **eliminar recursos de bloqueo de procesamiento** para ver los recursos que están bloqueando:</span><span class="sxs-lookup"><span data-stu-id="45375-312">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="45375-313">y `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="45375-313">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Más información sobre la oportunidad eliminar recursos de bloqueo de procesamiento" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="45375-315">Más información sobre la oportunidad **eliminar recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="45375-315">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-316">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, comience a escribir `Coverage` y, a continuación, seleccione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="45375-316">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abrir el menú de comandos desde el panel auditorías" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="45375-318">Abrir el menú de comandos desde el panel **auditorías**</span><span class="sxs-lookup"><span data-stu-id="45375-318">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="La ficha cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="45375-320">La ficha **cobertura**</span><span class="sxs-lookup"><span data-stu-id="45375-320">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-321">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="45375-321">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="45375-322">La pestaña **cobertura** proporciona una descripción general de la parte del código de `bundle.js` , `jquery.js` y `lodash.js` se ejecuta mientras se carga la página.</span><span class="sxs-lookup"><span data-stu-id="45375-322">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="45375-323">En la ilustración siguiente, unos 76% y un 30% de los archivos de jQuery y Lodash no se usan, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="45375-323">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="El informe de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="45375-325">El informe de cobertura</span><span class="sxs-lookup"><span data-stu-id="45375-325">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-326">Seleccione la fila **jquery.js** .</span><span class="sxs-lookup"><span data-stu-id="45375-326">Select the **jquery.js** row.</span></span>  <span data-ttu-id="45375-327">DevTools abre el archivo en el panel fuentes.</span><span class="sxs-lookup"><span data-stu-id="45375-327">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="45375-328">Se ejecutó una línea de código si tiene una barra azul al lado.</span><span class="sxs-lookup"><span data-stu-id="45375-328">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="45375-329">Una barra roja significa que no se ha ejecutado y, por supuesto, no es necesaria en la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-329">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Visualización del archivo jQuery en el panel orígenes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="45375-331">Visualización del archivo jQuery en el panel **orígenes**</span><span class="sxs-lookup"><span data-stu-id="45375-331">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-332">Desplácese un poco por el código jQuery.</span><span class="sxs-lookup"><span data-stu-id="45375-332">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="45375-333">Algunas de las líneas que reciben "ejecutar" son realmente solo Comentarios.</span><span class="sxs-lookup"><span data-stu-id="45375-333">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="45375-334">La ejecución de este código a través de un minifier que elimina los comentarios es otra forma de reducir el tamaño de este archivo.</span><span class="sxs-lookup"><span data-stu-id="45375-334">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="45375-335">En Resumen, cuando está trabajando con su propio código, la pestaña cobertura le ayuda a analizar el código, línea por línea, y solo envía el código necesario para la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-335">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="45375-336">¿Los `jquery.js` archivos y son `lodash.js` necesarios para cargar la página?</span><span class="sxs-lookup"><span data-stu-id="45375-336">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="45375-337">La pestaña bloqueo de solicitud muestra lo que sucede cuando los recursos no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="45375-337">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="45375-338">Seleccione la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="45375-338">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="45375-339">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para volver a abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="45375-339">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="45375-340">Comience `blocking` a escribir y, a continuación, seleccione **Mostrar bloqueo de solicitud**.</span><span class="sxs-lookup"><span data-stu-id="45375-340">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="La ficha solicitar bloqueo" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="45375-342">La ficha **solicitar bloqueo**</span><span class="sxs-lookup"><span data-stu-id="45375-342">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-343">Seleccione **Agregar patrón** \ ( ![ Agregar patrón ][ImageAddPatternIcon] \), escriba `/libs/*` y, a continuación, presione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="45375-343">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Agregar un patrón para bloquear cualquier solicitud al directorio de bibliotecas" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="45375-345">Agregar un patrón para bloquear cualquier solicitud al `libs` directorio</span><span class="sxs-lookup"><span data-stu-id="45375-345">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-346">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="45375-346">Refresh the page.</span></span>  <span data-ttu-id="45375-347">Las solicitudes jQuery y Lodash son rojas, lo que significa que las solicitudes se han bloqueado.</span><span class="sxs-lookup"><span data-stu-id="45375-347">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="45375-348">Aún se carga la página y es interactiva, por lo que parece que no se necesitan estos recursos.</span><span class="sxs-lookup"><span data-stu-id="45375-348">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="El panel red muestra que las solicitudes han sido bloqueadas" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="45375-350">El panel **red** muestra que las solicitudes han sido bloqueadas</span><span class="sxs-lookup"><span data-stu-id="45375-350">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-351">Seleccione **quitar todos los patrones** \ ( ![ quitar todos los patrones ][ImageRemoveIcon] \) para eliminar el `/libs/*` patrón de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="45375-351">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="45375-352">En general, la pestaña bloqueo de solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="45375-352">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="45375-353">Ahora, quite las referencias a estos archivos del código y audite de nuevo la página:</span><span class="sxs-lookup"><span data-stu-id="45375-353">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="45375-354">De nuevo en la pestaña Editor, Abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="45375-354">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="45375-355">Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="45375-355">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="45375-356">Espere a que el sitio se vuelva a compilar y a implementar.</span><span class="sxs-lookup"><span data-stu-id="45375-356">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="45375-357">Audite la página de nuevo desde el panel **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="45375-357">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="45375-358">Tu puntuación general debería haber mejorado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="45375-358">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un informe de auditoría después de quitar los recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="45375-360">Un informe de **Auditoría** después de quitar los recursos de bloqueo de representación</span><span class="sxs-lookup"><span data-stu-id="45375-360">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="45375-361">Optimizar la ruta de representación crítica en el mundo real</span><span class="sxs-lookup"><span data-stu-id="45375-361">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="45375-362">La **ruta de representación crítica** se refiere al código que necesita para cargar una página.</span><span class="sxs-lookup"><span data-stu-id="45375-362">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="45375-363">En general, para acelerar la carga de páginas solo tienes que enviar código crítico durante la carga de la página y, a continuación, cargar de forma diferida todo lo demás.</span><span class="sxs-lookup"><span data-stu-id="45375-363">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="45375-364">Es improbable que encuentre secuencias de comandos que pueda quitar de forma inadecuada, pero es posible que encuentre muchas secuencias de comandos que no necesita solicitar durante la carga de la página y que, en su lugar, las solicite.</span><span class="sxs-lookup"><span data-stu-id="45375-364">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="45375-365">Si está usando un marco, compruebe si tiene un modo de producción.</span><span class="sxs-lookup"><span data-stu-id="45375-365">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="45375-366">Este modo puede usar una característica, como el [agitador de árboles][WebpackTreeShaking] , para eliminar el código innecesario que está bloqueando el procesamiento crítico.</span><span class="sxs-lookup"><span data-stu-id="45375-366">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="45375-367">Hacer menos trabajo del subproceso principal</span><span class="sxs-lookup"><span data-stu-id="45375-367">Do less main thread work</span></span>   

<span data-ttu-id="45375-368">Su último informe muestra algunos ahorros potenciales menores en la sección oportunidades, pero si ve en la sección diagnósticos, parece que la mayor parte de la actividad principal es la actividad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="45375-368">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="45375-369">El subproceso principal es el lugar donde el explorador hace la mayor parte del trabajo necesario para mostrar una página, como analizar y ejecutar HTML, CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="45375-369">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="45375-370">El objetivo es usar el panel rendimiento para analizar qué trabajo está haciendo el subproceso principal mientras se carga la página y buscar formas de aplazar o quitar el trabajo innecesario.</span><span class="sxs-lookup"><span data-stu-id="45375-370">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="45375-371">Seleccione la pestaña **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="45375-371">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="45375-372">Seleccione **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="45375-372">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="45375-373">Configure la **red** como **3G lento** y **CPU** a **6X lentitud**.</span><span class="sxs-lookup"><span data-stu-id="45375-373">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="45375-374">Por lo general, los dispositivos móviles tienen más restricciones de hardware que los equipos portátiles o de escritorio, por lo que esta configuración le permite experimentar la carga de la página como si estuviera usando un dispositivo menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="45375-374">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="45375-375">Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="45375-375">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="45375-376">DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargarla.</span><span class="sxs-lookup"><span data-stu-id="45375-376">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="45375-377">Esta visualización se conoce como la **traza**.</span><span class="sxs-lookup"><span data-stu-id="45375-377">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Seguimiento del panel rendimiento de la carga de páginas" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="45375-379">Seguimiento del panel **rendimiento** de la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="45375-379">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-380">La traza muestra la actividad cronológicamente, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="45375-380">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="45375-381">Los gráficos de CPS, CPU y NET de la parte superior le ofrecen una descripción general de los fotogramas por segundo, la actividad de la CPU y la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="45375-381">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="45375-382">El bloque de amarillo seleccionado que aparece en la ilustración después de lo siguiente, la CPU estaba completamente ocupada por la actividad de scripting.</span><span class="sxs-lookup"><span data-stu-id="45375-382">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="45375-383">Esta es una pista de que puede acelerar la carga de la página haciendo menos trabajo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="45375-383">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="La sección información general de la traza" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="45375-385">La sección información general de la traza</span><span class="sxs-lookup"><span data-stu-id="45375-385">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="45375-386">Investigue el seguimiento para encontrar formas de hacer que el trabajo de JavaScript sea menor:</span><span class="sxs-lookup"><span data-stu-id="45375-386">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="45375-387">Seleccione la sección **intervalos** para expandirlo.</span><span class="sxs-lookup"><span data-stu-id="45375-387">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="45375-388">Basándose en el hecho de que puede haber una gran cantidad de medidas de [intervalos][MDNUserTimingApi] de reAct, parece que la aplicación de Tony usa el modo de desarrollo de reAct.</span><span class="sxs-lookup"><span data-stu-id="45375-388">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="45375-389">El cambio al modo de producción de reAct puede dar lugar a un resultado de fácil rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45375-389">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="La sección intervalos" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="45375-391">La sección **intervalos**</span><span class="sxs-lookup"><span data-stu-id="45375-391">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-392">Vuelva a seleccionar los **intervalos** para contraer la sección.</span><span class="sxs-lookup"><span data-stu-id="45375-392">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="45375-393">Examinar la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="45375-393">Browse the **Main** section.</span></span>  <span data-ttu-id="45375-394">En esta sección se muestra un registro cronológico de la actividad principal de la conversación, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="45375-394">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="45375-395">El eje y (de arriba a abajo) muestra por qué se produjeron eventos.</span><span class="sxs-lookup"><span data-stu-id="45375-395">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="45375-396">Por ejemplo, en el figyre después de lo siguiente, el `Evaluate Script` evento ha provocado la ejecución de la `(anonymous)` función, que ha provocado que `(anonymous)` se ejecutara, `__webpack__require__` y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="45375-396">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="La sección principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="45375-398">La sección **principal**</span><span class="sxs-lookup"><span data-stu-id="45375-398">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45375-399">Desplácese hacia abajo hasta la parte inferior de la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="45375-399">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="45375-400">Cuando se usa un marco, la mayor parte de la actividad superior está causada por el marco de trabajo, que normalmente está fuera de su control.</span><span class="sxs-lookup"><span data-stu-id="45375-400">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="45375-401">La actividad causada por la aplicación suele estar en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="45375-401">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="45375-402">En esta aplicación, parece que una función llamada `App` está causando un gran número de solicitudes a una `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="45375-402">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="45375-403">Suena como Tony podría estar usando los dispositivos de sus ventiladores para minar cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="45375-403">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Desplazarse por la actividad de mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="45375-405">Desplazar el puntero sobre la `mineBitcoin` actividad</span><span class="sxs-lookup"><span data-stu-id="45375-405">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="45375-406">A pesar de que las solicitudes que el marco de trabajo realiza generalmente están fuera de su control, a veces puede estructurar la aplicación de forma que el marco de trabajo se ejecute ineficazmente.</span><span class="sxs-lookup"><span data-stu-id="45375-406">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="45375-407">Reestructurar la aplicación para usar el marco de forma eficaz es una forma de hacer menos trabajo de los subprocesos principales.</span><span class="sxs-lookup"><span data-stu-id="45375-407">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="45375-408">Sin embargo, esto requiere un conocimiento profundo de cómo funciona el marco y qué tipo de cambios se realizan en el código propio para poder usar el marco de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="45375-408">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="45375-409">Expanda la sección de **abajo** .</span><span class="sxs-lookup"><span data-stu-id="45375-409">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="45375-410">Esta pestaña desglosa qué actividades ocuparon la mayor parte del tiempo.</span><span class="sxs-lookup"><span data-stu-id="45375-410">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="45375-411">Si no ve nada en la sección de la parte inferior, haga clic en la etiqueta de la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="45375-411">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="45375-412">En la sección de la **parte inferior** se muestra solo la información de cualquier actividad o grupo de actividades que haya seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="45375-412">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="45375-413">Por ejemplo, si hizo clic en una de las `mineBitcoin` actividades, la sección de **abajo** se mostrará solo la información de esa actividad.</span><span class="sxs-lookup"><span data-stu-id="45375-413">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="La pestaña abajo" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="45375-415">La pestaña **abajo**</span><span class="sxs-lookup"><span data-stu-id="45375-415">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-416">La columna **Self Time** muestra la cantidad de tiempo que se dedicó directamente en cada actividad.</span><span class="sxs-lookup"><span data-stu-id="45375-416">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="45375-417">Por ejemplo, en la siguiente ilustración, se dedicó un 63% del tiempo de rosca principal en la `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="45375-417">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="45375-418">Tiempo para ver si usar el modo de producción y reducir la actividad de JavaScript puede acelerar la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-418">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="45375-419">Empezar con el modo de producción:</span><span class="sxs-lookup"><span data-stu-id="45375-419">Start with production mode:</span></span>  

1.  <span data-ttu-id="45375-420">En la pestaña Editor, Abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="45375-420">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="45375-421">Cambiar `"mode":"development"` a `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="45375-421">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="45375-422">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="45375-422">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="45375-423">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="45375-423">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Un informe de auditoría después de configurar WebPack para usar el modo de producción" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="45375-425">Un informe de auditoría después de configurar WebPack para usar el modo de producción</span><span class="sxs-lookup"><span data-stu-id="45375-425">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-426">Reduzca la actividad de JavaScript eliminando la solicitud a `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="45375-426">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="45375-427">En la pestaña Editor, Abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="45375-427">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="45375-428">Comente la solicitud para `this.mineBitcoin(1500)` en el `constructor` .</span><span class="sxs-lookup"><span data-stu-id="45375-428">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="45375-429">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="45375-429">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="45375-430">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="45375-430">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un informe de auditoría después de quitar el trabajo de JavaScript innecesario" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="45375-432">Un informe de auditoría después de quitar el trabajo de JavaScript innecesario</span><span class="sxs-lookup"><span data-stu-id="45375-432">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45375-433">Parece que el último cambio causó un aumento de rendimiento masivo.</span><span class="sxs-lookup"><span data-stu-id="45375-433">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="45375-434">En esta sección se ofreció una breve introducción al panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45375-434">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="45375-435">Consulte [referencia de análisis de rendimiento][DevtoolsEvaluatePerformanceReference] para obtener más información sobre cómo analizar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="45375-435">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="45375-436">Trabajar con menos subprocesos principales en el mundo real</span><span class="sxs-lookup"><span data-stu-id="45375-436">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="45375-437">En general, el panel **rendimiento** es la manera más común de comprender qué actividad hace el sitio mientras se carga, y buscar formas de quitar actividades innecesarias.</span><span class="sxs-lookup"><span data-stu-id="45375-437">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="45375-438">Si prefiere un método que se sienta `console.log()` de la mejor manera, la [API de temporización de usuario][MDNUserTimingApi] le permite marcar arbitrariamente determinadas fases del ciclo de vida de la aplicación para realizar un seguimiento del tiempo que toma cada una de esas fases.</span><span class="sxs-lookup"><span data-stu-id="45375-438">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="45375-439">Resumen</span><span class="sxs-lookup"><span data-stu-id="45375-439">Summary</span></span>   

*   <span data-ttu-id="45375-440">Siempre que lo establezca para optimizar el rendimiento de la carga de un sitio, empiece siempre con una auditoría.</span><span class="sxs-lookup"><span data-stu-id="45375-440">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="45375-441">La auditoría establece una línea de base y le ofrece sugerencias sobre cómo mejorar.</span><span class="sxs-lookup"><span data-stu-id="45375-441">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="45375-442">Realice un cambio a la vez y audite la página después de cada cambio para ver cómo afecta el cambio en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45375-442">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

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
> <span data-ttu-id="45375-449">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45375-449">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="45375-450">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="45375-450">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="45375-452">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45375-452">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
