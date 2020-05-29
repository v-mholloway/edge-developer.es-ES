---
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611892"
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





# <span data-ttu-id="e821c-103">Optimizar la velocidad del sitio web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e821c-103">Optimize Website Speed With Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="e821c-104">Objetivo del tutorial</span><span class="sxs-lookup"><span data-stu-id="e821c-104">Goal of tutorial</span></span>  

<span data-ttu-id="e821c-105">En este tutorial aprenderás a usar Microsoft Edge DevTools para encontrar formas de cargar tus sitios web más rápido.</span><span class="sxs-lookup"><span data-stu-id="e821c-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="e821c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e821c-106">Prerequisites</span></span>  

*   <span data-ttu-id="e821c-107">Debe tener experiencia básica de desarrollo web, similar a lo que enseñamos esta [Introducción a la clase de desarrollo web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="e821c-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="e821c-108">No es necesario que sepa nada sobre el rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="e821c-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="e821c-109">Puede obtener más información en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="e821c-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="e821c-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="e821c-110">Introduction</span></span>   

<span data-ttu-id="e821c-111">Es Tony.</span><span class="sxs-lookup"><span data-stu-id="e821c-111">This is Tony.</span></span>  <span data-ttu-id="e821c-112">Tony es muy famoso en el gato de la sociedad.</span><span class="sxs-lookup"><span data-stu-id="e821c-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="e821c-113">Ha creado un sitio web para que sus ventiladores puedan conocer sus alimentos favoritos.</span><span class="sxs-lookup"><span data-stu-id="e821c-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="e821c-114">Sus ventiladores adoran el sitio, pero Tony mantiene las quejas auditivas que el sitio carga lentamente.</span><span class="sxs-lookup"><span data-stu-id="e821c-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="e821c-115">Tony le ha pedido que le ayude a acelerar el sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-115">Tony has asked you to help him speed the site up.</span></span>  

> ##### <span data-ttu-id="e821c-116">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e821c-116">Figure 1</span></span>  
> <span data-ttu-id="e821c-117">Tony el gato</span><span class="sxs-lookup"><span data-stu-id="e821c-117">Tony the cat</span></span>  
> ![Tony el gato][ImageTony]  

## <span data-ttu-id="e821c-119">Paso 1: auditar el sitio</span><span class="sxs-lookup"><span data-stu-id="e821c-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="e821c-120">Siempre que lo establezca para mejorar el rendimiento de la carga de un sitio, **empiece siempre con una auditoría**.</span><span class="sxs-lookup"><span data-stu-id="e821c-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="e821c-121">La auditoría tiene dos funciones importantes:</span><span class="sxs-lookup"><span data-stu-id="e821c-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="e821c-122">Crea una **línea base** para medir los cambios posteriores.</span><span class="sxs-lookup"><span data-stu-id="e821c-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="e821c-123">Le ofrece **consejos útiles** sobre qué cambios son más impactantes.</span><span class="sxs-lookup"><span data-stu-id="e821c-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  

### <span data-ttu-id="e821c-124">Configuración</span><span class="sxs-lookup"><span data-stu-id="e821c-124">Set up</span></span>   

<span data-ttu-id="e821c-125">En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.</span><span class="sxs-lookup"><span data-stu-id="e821c-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="e821c-126">[Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="e821c-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="e821c-127">Esta pestaña se conoce como la **pestaña Editor**.</span><span class="sxs-lookup"><span data-stu-id="e821c-127">This tab is referred to as the **editor tab**.</span></span>  
    
    > ##### <span data-ttu-id="e821c-128">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e821c-128">Figure 2</span></span>  
    > <span data-ttu-id="e821c-129">Ficha Editor</span><span class="sxs-lookup"><span data-stu-id="e821c-129">The editor tab</span></span>  
    > ![Ficha Editor][ImageEditor]  

1.  <span data-ttu-id="e821c-131">Seleccione **Tony**.</span><span class="sxs-lookup"><span data-stu-id="e821c-131">Select **tony**.</span></span>  <span data-ttu-id="e821c-132">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="e821c-132">A menu appears.</span></span>  
    
    > ##### <span data-ttu-id="e821c-133">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="e821c-133">Figure 3</span></span>  
    > <span data-ttu-id="e821c-134">El menú que aparece después de hacer clic en **Tony**</span><span class="sxs-lookup"><span data-stu-id="e821c-134">The menu that appears after clicking **tony**</span></span>  
    > ![El menú que aparece después de hacer clic en Tony][ImageMenu]  
    
1.  <span data-ttu-id="e821c-136">Seleccione **proyecto Remix**.</span><span class="sxs-lookup"><span data-stu-id="e821c-136">Select **Remix Project**.</span></span>  <span data-ttu-id="e821c-137">El nombre del proyecto cambia de **Tony** a algún nombre generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="e821c-137">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="e821c-138">Ahora tiene su propia copia modificable del código.</span><span class="sxs-lookup"><span data-stu-id="e821c-138">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="e821c-139">Más adelante, puedes realizar cambios en este código.</span><span class="sxs-lookup"><span data-stu-id="e821c-139">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="e821c-140">Seleccione **Mostrar** y seleccione **en una nueva ventana**.</span><span class="sxs-lookup"><span data-stu-id="e821c-140">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="e821c-141">La demostración se abre en una nueva pestaña.  Esta pestaña se conoce como la **pestaña demo**.  Es posible que el sitio tarde un rato en cargarse.</span><span class="sxs-lookup"><span data-stu-id="e821c-141">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    > ##### <span data-ttu-id="e821c-142">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="e821c-142">Figure 4</span></span>  
    > <span data-ttu-id="e821c-143">La ficha demo</span><span class="sxs-lookup"><span data-stu-id="e821c-143">The demo tab</span></span>  
    > ![La ficha demo][ImageDemo]  

1.  <span data-ttu-id="e821c-145">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e821c-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="e821c-146">Microsoft Edge DevTools se abre junto con la demostración.</span><span class="sxs-lookup"><span data-stu-id="e821c-146">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    > ##### <span data-ttu-id="e821c-147">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="e821c-147">Figure 5</span></span>  
    > <span data-ttu-id="e821c-148">DevTools y la demostración</span><span class="sxs-lookup"><span data-stu-id="e821c-148">DevTools and the demo</span></span>  
    > ![DevTools y la demostración][ImageDevtools]  

<span data-ttu-id="e821c-150">Para el resto de las capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="e821c-150">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="e821c-151">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú comando, escriba `Undock` y, a continuación, seleccione **desacoplar en ventana independiente**.</span><span class="sxs-lookup"><span data-stu-id="e821c-151">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

> ##### <span data-ttu-id="e821c-152">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="e821c-152">Figure 6</span></span>  
> <span data-ttu-id="e821c-153">DevTools desacoplado</span><span class="sxs-lookup"><span data-stu-id="e821c-153">Undocked DevTools</span></span>  
> ![DevTools desacoplado][ImageUndocked]  

### <span data-ttu-id="e821c-155">Establecer una línea base</span><span class="sxs-lookup"><span data-stu-id="e821c-155">Establish a baseline</span></span>   

<span data-ttu-id="e821c-156">La línea base es un registro de cómo se realizó el sitio antes de realizar alguna mejora en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e821c-156">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="e821c-157">Seleccione la pestaña **auditorías** .  Es posible que esté oculto detrás **del** ![ botón más paneles ][ImageMorePanelsIcon] .</span><span class="sxs-lookup"><span data-stu-id="e821c-157">Select the **Audits** tab.  It may be hidden behind the **More Panels** ![More Panels][ImageMorePanelsIcon] button.</span></span>  <span data-ttu-id="e821c-158">Hay un Lighthouse en este panel porque el proyecto que alimenta el panel auditoría se denomina **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="e821c-158">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### <span data-ttu-id="e821c-159">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="e821c-159">Figure 7</span></span>  
    > <span data-ttu-id="e821c-160">Panel auditorías</span><span class="sxs-lookup"><span data-stu-id="e821c-160">The Audits panel</span></span>  
    > ![Panel auditorías][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="e821c-162">Ajuste la configuración de la auditoría a las opciones de la [Ilustración 7](#figure-7).</span><span class="sxs-lookup"><span data-stu-id="e821c-162">Match your audit configuration settings to those in [Figure 7](#figure-7).</span></span>  <span data-ttu-id="e821c-163">A continuación se explican las diferentes opciones:</span><span class="sxs-lookup"><span data-stu-id="e821c-163">Here is an explanation of the different options:</span></span>  

    *   <span data-ttu-id="e821c-164">**Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="e821c-164">**Device**.</span></span>  <span data-ttu-id="e821c-165">Configuración para **dispositivos móviles** cambia la cadena de agente de usuario y simula un área de visualización móvil.</span><span class="sxs-lookup"><span data-stu-id="e821c-165">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="e821c-166">La configuración en el **escritorio** simplemente deshabilita los cambios en el **teléfono móvil** .</span><span class="sxs-lookup"><span data-stu-id="e821c-166">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="e821c-167">**Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="e821c-167">**Audits**.</span></span>  <span data-ttu-id="e821c-168">Si deshabilita una categoría, evitará que el panel auditoría las ejecute y las excluirá de su informe.</span><span class="sxs-lookup"><span data-stu-id="e821c-168">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="e821c-169">Deje las otras categorías habilitadas si desea ver los tipos de recomendaciones proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="e821c-169">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="e821c-170">Al deshabilitar las categorías, se acelera ligeramente el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="e821c-170">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="e821c-171">**Limitación**.</span><span class="sxs-lookup"><span data-stu-id="e821c-171">**Throttling**.</span></span>  <span data-ttu-id="e821c-172">Configurada para **simular lentitud de 4G, con una ralentización** de la CPU de 4x simula las condiciones típicas de la navegación en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="e821c-172">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="e821c-173">Se denomina "simulado" porque en realidad el panel auditorías no se limita durante el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="e821c-173">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="e821c-174">En su lugar, simplemente extrapola cuánto tiempo tardará la página en cargarse en condiciones móviles.</span><span class="sxs-lookup"><span data-stu-id="e821c-174">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="e821c-175">Por otro lado, la opción de configuración **aplicado** , limita la CPU y la red, con la compensación de un proceso de auditoría más largo.</span><span class="sxs-lookup"><span data-stu-id="e821c-175">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="e821c-176">**Borrar almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="e821c-176">**Clear Storage**.</span></span>  <span data-ttu-id="e821c-177">Al habilitar esta casilla, se borra todo el almacenamiento asociado a la página antes de cada auditoría.</span><span class="sxs-lookup"><span data-stu-id="e821c-177">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="e821c-178">Deje esta configuración activada si desea auditar la experiencia de los visitantes por primera vez en su sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-178">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="e821c-179">Deshabilite esta configuración cuando quiera la experiencia de repetición de la visita.</span><span class="sxs-lookup"><span data-stu-id="e821c-179">Disable this setting when you want the repeat-visit experience.</span></span>  

1.  <span data-ttu-id="e821c-180">Seleccione **Ejecutar Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="e821c-180">Select **Run Audits**.</span></span>  <span data-ttu-id="e821c-181">Después de 10 a 30 segundos, el panel auditoría muestra un informe del rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-181">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    > ##### <span data-ttu-id="e821c-182">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="e821c-182">Figure 8</span></span>  
    > <span data-ttu-id="e821c-183">Informe para el panel auditoría del rendimiento del sitio</span><span class="sxs-lookup"><span data-stu-id="e821c-183">The report for the Audits panel of the performance of the site</span></span>  
    > ![Informe para el panel auditoría del rendimiento del sitio][ImageReport]  

#### <span data-ttu-id="e821c-185">Control de errores de informe</span><span class="sxs-lookup"><span data-stu-id="e821c-185">Handling report errors</span></span>   

<span data-ttu-id="e821c-186">Si alguna vez recibe un error en el informe del panel auditorías, pruebe a ejecutar la pestaña demostración desde una ventana **InPrivate** sin ninguna otra pestaña abierta.</span><span class="sxs-lookup"><span data-stu-id="e821c-186">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="e821c-187">Esto asegura que está ejecutando Microsoft Edge desde un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="e821c-187">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="e821c-188">Las extensiones de Microsoft Edge en particular suelen interferir con el proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="e821c-188">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### <span data-ttu-id="e821c-189">Comprender el informe</span><span class="sxs-lookup"><span data-stu-id="e821c-189">Understand your report</span></span>   

<span data-ttu-id="e821c-190">El número que aparece en la parte superior del informe es la puntuación de rendimiento general para el sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-190">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="e821c-191">Después, a medida que haga cambios en el código, debería ver que este número ha aumentado.</span><span class="sxs-lookup"><span data-stu-id="e821c-191">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="e821c-192">Una puntuación mayor supone un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e821c-192">A higher score means better performance.</span></span>  

> ##### <span data-ttu-id="e821c-193">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="e821c-193">Figure 9</span></span>  
> <span data-ttu-id="e821c-194">La puntuación general de rendimiento</span><span class="sxs-lookup"><span data-stu-id="e821c-194">The overall performance score</span></span>  
> <span data-ttu-id="e821c-195">! [La puntuación general de rendimiento] [ImageOverall]</span><span class="sxs-lookup"><span data-stu-id="e821c-195">![The overall performance score][ImageOverall]</span></span>  

<span data-ttu-id="e821c-196">La sección de **métricas** proporciona medidas cuantitativas en el rendimiento del sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-196">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="e821c-197">Cada métrica proporciona información sobre un aspecto diferente del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e821c-197">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="e821c-198">Por ejemplo, la **primera pintura con contenido** le indica cuando el contenido se pinta por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que el tiempo de marca **interactiva** es el punto en el que la página aparece lo suficientemente lista para controlar las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="e821c-198">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

> ##### <span data-ttu-id="e821c-199">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="e821c-199">Figure 10</span></span>  
> <span data-ttu-id="e821c-200">La sección métrica</span><span class="sxs-lookup"><span data-stu-id="e821c-200">The Metrics section</span></span>  
> <span data-ttu-id="e821c-201">! [Sección de métricas] [ImageMetrics]</span><span class="sxs-lookup"><span data-stu-id="e821c-201">![The Metrics section][ImageMetrics]</span></span>  

<span data-ttu-id="e821c-202">Seleccione el botón de alternancia resaltado en la [figura 11](#figure-11) para ver una descripción de cada métrica y haga clic en **obtener más información** para leer la documentación.</span><span class="sxs-lookup"><span data-stu-id="e821c-202">Select the highlighted toggle button in [Figure 11](#figure-11) to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

> ##### <span data-ttu-id="e821c-203">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="e821c-203">Figure 11</span></span>  
> <span data-ttu-id="e821c-204">Seleccione el botón de alternancia resaltado para expandir los elementos de **métrica**</span><span class="sxs-lookup"><span data-stu-id="e821c-204">Select the highlighted toggle button to expand the **Metrics** items</span></span>  
> <span data-ttu-id="e821c-205">! [Seleccione el botón de alternancia resaltado para expandir los elementos de métricas] [ImageFirstMeaningfulPaint]</span><span class="sxs-lookup"><span data-stu-id="e821c-205">![Select the highlighted toggle button to expand the Metrics items][ImageFirstMeaningfulPaint]</span></span>  

<span data-ttu-id="e821c-206">A continuación, se muestra una colección de capturas de pantallas en la que se muestra cómo se ha cargado la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-206">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

> ##### <span data-ttu-id="e821c-207">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="e821c-207">Figure 12</span></span>  
> <span data-ttu-id="e821c-208">Capturas de pantallas del aspecto de la página durante la carga</span><span class="sxs-lookup"><span data-stu-id="e821c-208">Screenshots of how the page looked while loading</span></span>  
> <span data-ttu-id="e821c-209">! [Capturas de pantallas de cómo se vio la página durante la carga] [ImageScreenshots]</span><span class="sxs-lookup"><span data-stu-id="e821c-209">![Screenshots of how the page looked while loading][ImageScreenshots]</span></span>  

<span data-ttu-id="e821c-210">La sección **oportunidades** proporciona sugerencias específicas sobre cómo mejorar el rendimiento de la carga de esta página específica.</span><span class="sxs-lookup"><span data-stu-id="e821c-210">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

> ##### <span data-ttu-id="e821c-211">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="e821c-211">Figure 13</span></span>  
> <span data-ttu-id="e821c-212">La sección oportunidades</span><span class="sxs-lookup"><span data-stu-id="e821c-212">The Opportunities section</span></span>  
> <span data-ttu-id="e821c-213">! [Sección de oportunidades] [ImageOpportunities]</span><span class="sxs-lookup"><span data-stu-id="e821c-213">![The Opportunities section][ImageOpportunities]</span></span>  

<span data-ttu-id="e821c-214">Seleccione una oportunidad para obtener más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="e821c-214">Select an opportunity to learn more about it.</span></span>  

> ##### <span data-ttu-id="e821c-215">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="e821c-215">Figure 14</span></span>  
> <span data-ttu-id="e821c-216">**Eliminar la oportunidad de recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="e821c-216">**Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="e821c-217">! [Eliminar oportunidad de recursos de bloqueo de procesamiento] [ImageCompression]</span><span class="sxs-lookup"><span data-stu-id="e821c-217">![Eliminate render-blocking resources opportunity][ImageCompression]</span></span>  

<span data-ttu-id="e821c-218">Seleccione **más información** para ver la documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo corregirla.</span><span class="sxs-lookup"><span data-stu-id="e821c-218">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

> ##### <span data-ttu-id="e821c-219">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="e821c-219">Figure 15</span></span>  
> <span data-ttu-id="e821c-220">Documentación de la oportunidad **eliminar recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="e821c-220">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="e821c-221">! [Documentación para la oportunidad eliminar recursos de bloqueo de representación] [ImageReference]</span><span class="sxs-lookup"><span data-stu-id="e821c-221">![Documentation for the Eliminate render-blocking resources opportunity][ImageReference]</span></span>  

<span data-ttu-id="e821c-222">La sección **diagnósticos** proporciona más información sobre los factores que contribuyen al tiempo de carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-222">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

> ##### <span data-ttu-id="e821c-223">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="e821c-223">Figure 16</span></span>  
> <span data-ttu-id="e821c-224">La sección diagnósticos</span><span class="sxs-lookup"><span data-stu-id="e821c-224">The Diagnostics section</span></span>  
> <span data-ttu-id="e821c-225">! [Sección de diagnósticos] [ImageDiagnostics]</span><span class="sxs-lookup"><span data-stu-id="e821c-225">![The Diagnostics section][ImageDiagnostics]</span></span>  

<span data-ttu-id="e821c-226">En la sección de **auditorías superada** se muestra lo que el sitio está haciendo correctamente.</span><span class="sxs-lookup"><span data-stu-id="e821c-226">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="e821c-227">Seleccione para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="e821c-227">Select to expand the section.</span></span>  

> ##### <span data-ttu-id="e821c-228">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="e821c-228">Figure 17</span></span>  
> <span data-ttu-id="e821c-229">La sección de auditorías superada</span><span class="sxs-lookup"><span data-stu-id="e821c-229">The Passed Audits section</span></span>  
> <span data-ttu-id="e821c-230">! [Sección de auditorías superada] [ImagePassed]</span><span class="sxs-lookup"><span data-stu-id="e821c-230">![The Passed Audits section][ImagePassed]</span></span>  

## <span data-ttu-id="e821c-231">Paso 2: experimento</span><span class="sxs-lookup"><span data-stu-id="e821c-231">Step 2: Experiment</span></span>   

<span data-ttu-id="e821c-232">La sección oportunidades de su informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-232">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="e821c-233">En esta sección, implementará los cambios recomendados en el código base, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-233">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="e821c-234">Habilitar compresión de texto</span><span class="sxs-lookup"><span data-stu-id="e821c-234">Enable text compression</span></span>   

<span data-ttu-id="e821c-235">El informe dice que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-235">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="e821c-236">Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-236">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="e821c-237">La compresión de texto es cuando se reduce, o comprime, el tamaño de un archivo de texto antes de enviarlo a través de la red.</span><span class="sxs-lookup"><span data-stu-id="e821c-237">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="e821c-238">Tipo de cómo puede comprimir una carpeta antes de enviarle un mensaje de correo electrónico para reducir el tamaño.</span><span class="sxs-lookup"><span data-stu-id="e821c-238">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="e821c-239">Antes de habilitar la compresión, hay un par de maneras de comprobar manualmente si los recursos de texto están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="e821c-239">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="e821c-240">Seleccione la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="e821c-240">Select the **Network** tab.</span></span>  
    
    > ##### <span data-ttu-id="e821c-241">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="e821c-241">Figure 18</span></span>  
    > <span data-ttu-id="e821c-242">Panel red</span><span class="sxs-lookup"><span data-stu-id="e821c-242">The Network panel</span></span>  
    > <span data-ttu-id="e821c-243">! [Panel de red] [ImageNetwork]</span><span class="sxs-lookup"><span data-stu-id="e821c-243">![The Network panel][ImageNetwork]</span></span>  
    
1.  <span data-ttu-id="e821c-244">Seleccione el icono de **configuración de red** .</span><span class="sxs-lookup"><span data-stu-id="e821c-244">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="e821c-245">Seleccione la casilla **usar filas de solicitudes grandes** .</span><span class="sxs-lookup"><span data-stu-id="e821c-245">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="e821c-246">Aumenta el alto de las filas de la tabla de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="e821c-246">The height of the rows in the table of network requests increases.</span></span>  
    
    > ##### <span data-ttu-id="e821c-247">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="e821c-247">Figure 19</span></span>  
    > <span data-ttu-id="e821c-248">Filas grandes en la tabla solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="e821c-248">Large rows in the network requests table</span></span>  
    > <span data-ttu-id="e821c-249">! [Filas grandes en la tabla solicitudes de red] [ImageLargeRows]</span><span class="sxs-lookup"><span data-stu-id="e821c-249">![Large rows in the network requests table][ImageLargeRows]</span></span>  
    
1.  <span data-ttu-id="e821c-250">Si no ve la columna **tamaño** en la tabla de solicitudes de red, haga clic en el encabezado de tabla y, a continuación, seleccione **tamaño**.</span><span class="sxs-lookup"><span data-stu-id="e821c-250">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="e821c-251">Cada celda de **tamaño** muestra dos valores.</span><span class="sxs-lookup"><span data-stu-id="e821c-251">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="e821c-252">El valor superior es el tamaño del recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="e821c-252">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="e821c-253">El valor inferior es el tamaño del recurso sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="e821c-253">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="e821c-254">Si los dos valores son iguales, el recurso no se comprimirá cuando se envíe a través de la red.</span><span class="sxs-lookup"><span data-stu-id="e821c-254">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="e821c-255">Por ejemplo, en la [figura 19](#figure-19) los valores superiores e inferiores de is `bundle.js` `1.2 MB` y `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="e821c-255">For example, in [Figure 19](#figure-19) the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="e821c-256">Para comprobar la compresión, inspeccione los encabezados HTTP de un recurso:</span><span class="sxs-lookup"><span data-stu-id="e821c-256">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="e821c-257">Seleccione **bundle. js**.</span><span class="sxs-lookup"><span data-stu-id="e821c-257">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="e821c-258">Seleccione la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="e821c-258">Select the **Headers** tab.</span></span>  
    
    > ##### <span data-ttu-id="e821c-259">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="e821c-259">Figure 20</span></span>  
    > <span data-ttu-id="e821c-260">La pestaña encabezados</span><span class="sxs-lookup"><span data-stu-id="e821c-260">The Headers tab</span></span>  
    > <span data-ttu-id="e821c-261">! [Ficha encabezados] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="e821c-261">![The Headers tab][ImageHeaders]</span></span>  
    
1.  <span data-ttu-id="e821c-262">Busque un encabezado en la sección de **encabezados de respuesta** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="e821c-262">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="e821c-263">No debe ver ninguno, lo que significa que `bundle.js` no se ha comprimido.</span><span class="sxs-lookup"><span data-stu-id="e821c-263">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="e821c-264">Cuando se comprime un recurso, este encabezado suele establecerse en `gzip` , `deflate` o `br` .</span><span class="sxs-lookup"><span data-stu-id="e821c-264">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="e821c-265">Vea las [directivas][MDNContentEncodingDirectives] para obtener una explicación de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e821c-265">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="e821c-266">Es suficiente con las explicaciones.</span><span class="sxs-lookup"><span data-stu-id="e821c-266">Enough with the explanations.</span></span>  <span data-ttu-id="e821c-267">Para hacer algunos cambios.</span><span class="sxs-lookup"><span data-stu-id="e821c-267">Time to make some changes!</span></span>  <span data-ttu-id="e821c-268">Habilite la compresión de texto agregando un par de líneas de código:</span><span class="sxs-lookup"><span data-stu-id="e821c-268">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="e821c-269">En la pestaña Editor, haga clic en **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="e821c-269">In the editor tab, click **server.js**.</span></span>  
    
    > ##### <span data-ttu-id="e821c-270">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="e821c-270">Figure 21</span></span>  
    > <span data-ttu-id="e821c-271">Edición de Server. js</span><span class="sxs-lookup"><span data-stu-id="e821c-271">Editing server.js</span></span>  
    > <span data-ttu-id="e821c-272">! [Editing Server. js] [ImageServer]</span><span class="sxs-lookup"><span data-stu-id="e821c-272">![Editing server.js][ImageServer]</span></span>  
    
1.  <span data-ttu-id="e821c-273">Agregue el código siguiente a **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="e821c-273">Add the following code to **server.js**.</span></span>  <span data-ttu-id="e821c-274">Asegúrate de poner `app.use(compression())` antes `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="e821c-274">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="e821c-275">Normalmente, tiene que instalar el `compression` paquete a través de algo similar `npm i -S compression` , pero esto ya se ha hecho para usted.</span><span class="sxs-lookup"><span data-stu-id="e821c-275">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="e821c-276">Espere a que se implemente la nueva compilación del sitio.</span><span class="sxs-lookup"><span data-stu-id="e821c-276">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="e821c-277">La animación más sofisticada junto a **herramientas** significa que el sitio se vuelve a generar y a implementar.</span><span class="sxs-lookup"><span data-stu-id="e821c-277">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="e821c-278">El cambio está listo cuando la animación junto a **herramientas** desaparece.</span><span class="sxs-lookup"><span data-stu-id="e821c-278">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="e821c-279">Seleccione **Mostrar** y vuelva a seleccionar **una nueva ventana** .</span><span class="sxs-lookup"><span data-stu-id="e821c-279">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
<span data-ttu-id="e821c-280">Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:</span><span class="sxs-lookup"><span data-stu-id="e821c-280">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="e821c-281">Vuelva a la pestaña demo y vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-281">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="e821c-282">La columna **tamaño** debería mostrar ahora dos valores diferentes para recursos de texto como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="e821c-282">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="e821c-283">En la [Figura 23](#figure-23) , el valor superior de `256 KB` para `bundle.js` es el tamaño del archivo que se envió a través de la red y el valor inferior de `1.2 MB` es el tamaño de archivo descomprimido.</span><span class="sxs-lookup"><span data-stu-id="e821c-283">In [Figure 23](#figure-23) the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    > ##### <span data-ttu-id="e821c-284">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="e821c-284">Figure 22</span></span>  
    > <span data-ttu-id="e821c-285">La columna tamaño muestra ahora 2 valores diferentes para los recursos de texto</span><span class="sxs-lookup"><span data-stu-id="e821c-285">The Size column now shows 2 different values for text resources</span></span>  
    > <span data-ttu-id="e821c-286">! [La columna tamaño ahora muestra 2 valores diferentes para los recursos de texto] [ImageRequests]</span><span class="sxs-lookup"><span data-stu-id="e821c-286">![The Size column now shows 2 different values for text resources][ImageRequests]</span></span>  
    
1.  <span data-ttu-id="e821c-287">La sección de **encabezados de respuesta** de `bundle.js` ahora debe incluir un `content-encoding: gzip` encabezado.</span><span class="sxs-lookup"><span data-stu-id="e821c-287">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    > ##### <span data-ttu-id="e821c-288">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="e821c-288">Figure 23</span></span>  
    > <span data-ttu-id="e821c-289">La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido</span><span class="sxs-lookup"><span data-stu-id="e821c-289">The Response Headers section now contains a content-encoding header</span></span>  
    > <span data-ttu-id="e821c-290">! [La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido] [ImageGzip]</span><span class="sxs-lookup"><span data-stu-id="e821c-290">![The Response Headers section now contains a content-encoding header][ImageGzip]</span></span>  
    
<span data-ttu-id="e821c-291">Audite de nuevo la página para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:</span><span class="sxs-lookup"><span data-stu-id="e821c-291">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="e821c-292">Seleccione la pestaña **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="e821c-292">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="e821c-293">Seleccione **realizar una** auditoría para realizar una auditoría ![ ][ImagePerformIcon] .</span><span class="sxs-lookup"><span data-stu-id="e821c-293">Select **Perform an audit** ![Perform an audit][ImagePerformIcon].</span></span>  
1.  <span data-ttu-id="e821c-294">Deje la configuración igual que antes.</span><span class="sxs-lookup"><span data-stu-id="e821c-294">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="e821c-295">Seleccione **Ejecutar auditoría**.</span><span class="sxs-lookup"><span data-stu-id="e821c-295">Select **Run audit**.</span></span>  
    
    > ##### <span data-ttu-id="e821c-296">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="e821c-296">Figure 24</span></span>  
    > <span data-ttu-id="e821c-297">Un informe de auditoría después de habilitar la compresión de texto</span><span class="sxs-lookup"><span data-stu-id="e821c-297">An Audits report after enabling text compression</span></span>  
    > <span data-ttu-id="e821c-298">! [Informe de auditoría después de habilitar la compresión de texto] [ImageReport2]</span><span class="sxs-lookup"><span data-stu-id="e821c-298">![An Audits report after enabling text compression][ImageReport2]</span></span>  
    
<span data-ttu-id="e821c-299">Woohoo!</span><span class="sxs-lookup"><span data-stu-id="e821c-299">Woohoo!</span></span>  <span data-ttu-id="e821c-300">El aspecto es el mismo.</span><span class="sxs-lookup"><span data-stu-id="e821c-300">That looks like progress.</span></span>  <span data-ttu-id="e821c-301">La puntuación de rendimiento general debería haber aumentado, lo que significa que el sitio se está acelerando.</span><span class="sxs-lookup"><span data-stu-id="e821c-301">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="e821c-302">Compresión de texto en el mundo real</span><span class="sxs-lookup"><span data-stu-id="e821c-302">Text compression in the real world</span></span>   

<span data-ttu-id="e821c-303">La mayoría de los servidores realmente tienen soluciones sencillas como esta para habilitar la compresión.</span><span class="sxs-lookup"><span data-stu-id="e821c-303">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="e821c-304">Solo tiene que hacer una búsqueda para configurar cualquier servidor que use para comprimir texto.</span><span class="sxs-lookup"><span data-stu-id="e821c-304">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="e821c-305">Cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="e821c-305">Resize images</span></span>   

<span data-ttu-id="e821c-306">El informe indica que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-306">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="e821c-307">Cambiar el tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.</span><span class="sxs-lookup"><span data-stu-id="e821c-307">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="e821c-308">Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, no hay ningún punto para enviar una imagen de ancho de 1500 píxeles.</span><span class="sxs-lookup"><span data-stu-id="e821c-308">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="e821c-309">Lo ideal es que envíes una imagen de ancho de 500 píxeles, como máximo.</span><span class="sxs-lookup"><span data-stu-id="e821c-309">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="e821c-310">En el informe, haga clic en **evitar cargas de red enormes** para ver las imágenes que se deben cambiar de tamaño.</span><span class="sxs-lookup"><span data-stu-id="e821c-310">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="e821c-311">Parece ser que 2 de los archivos jpg superan 2000 KB, lo cual es más grande de lo necesario.</span><span class="sxs-lookup"><span data-stu-id="e821c-311">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  <span data-ttu-id="e821c-312">De nuevo en la pestaña Editor, Abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="e821c-312">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="e821c-313">Reemplazar `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="e821c-313">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="e821c-314">Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="e821c-314">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="e821c-315">Audite de nuevo la página para ver cómo este cambio afecta al rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="e821c-315">Audit the page again to see how this change affects load performance.</span></span>  
    
    > ##### <span data-ttu-id="e821c-316">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="e821c-316">Figure 25</span></span>  
    > <span data-ttu-id="e821c-317">Un informe de auditoría después de cambiar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="e821c-317">An Audits report after resizing images</span></span>  
    > <span data-ttu-id="e821c-318">! [Informe de auditoría después de cambiar el tamaño de las imágenes] [ImageReport3]</span><span class="sxs-lookup"><span data-stu-id="e821c-318">![An Audits report after resizing images][ImageReport3]</span></span>  

<span data-ttu-id="e821c-319">Parece que el cambio sólo tiene un efecto menor en la puntuación de rendimiento general.</span><span class="sxs-lookup"><span data-stu-id="e821c-319">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="e821c-320">Sin embargo, un elemento que indica que la puntuación no se muestra claramente es cuántos datos de red está guardando los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e821c-320">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="e821c-321">El tamaño total de las fotos antiguas ocupaba alrededor de 5,3 megabytes, mientras que ahora solo es de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="e821c-321">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="e821c-322">Cambiar el tamaño de las imágenes en el mundo real</span><span class="sxs-lookup"><span data-stu-id="e821c-322">Resizing images in the real world</span></span>   

<span data-ttu-id="e821c-323">En el caso de una aplicación pequeña, realizar un ajuste de tamaño único como este puede ser lo suficientemente bueno.</span><span class="sxs-lookup"><span data-stu-id="e821c-323">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="e821c-324">Pero para una aplicación de gran tamaño obviamente, esto no es escalable.</span><span class="sxs-lookup"><span data-stu-id="e821c-324">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="e821c-325">Estas son algunas estrategias para administrar imágenes en aplicaciones de gran tamaño:</span><span class="sxs-lookup"><span data-stu-id="e821c-325">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="e821c-326">Cambie el tamaño de las imágenes durante el proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="e821c-326">Resize images during your build process.</span></span>  
*   <span data-ttu-id="e821c-327">Cree varios tamaños de cada imagen durante el proceso de compilación y, a continuación, utilícelos `srcset` en el código.</span><span class="sxs-lookup"><span data-stu-id="e821c-327">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="e821c-328">En tiempo de ejecución, el explorador se ocupa de elegir el tamaño más adecuado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e821c-328">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->

<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="e821c-329">Use una CDN de imagen que le permita cambiar el tamaño de una imagen dinámicamente cuando la solicite.</span><span class="sxs-lookup"><span data-stu-id="e821c-329">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="e821c-330">Como mínimo, optimiza cada imagen.</span><span class="sxs-lookup"><span data-stu-id="e821c-330">At the very least, optimize each image.</span></span>  <span data-ttu-id="e821c-331">Esto puede crear enormes descuentos.</span><span class="sxs-lookup"><span data-stu-id="e821c-331">This may create huge savings.</span></span>  
  <span data-ttu-id="e821c-332">La optimización es cuando se ejecuta una imagen a través de un programa especial que reduce el tamaño del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="e821c-332">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="e821c-333">Para obtener más información, consulta la [optimización básica de imágenes][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="e821c-333">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  

### <span data-ttu-id="e821c-334">Eliminar recursos de bloqueo de procesamiento</span><span class="sxs-lookup"><span data-stu-id="e821c-334">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="e821c-335">El último informe indica que la eliminación de recursos de bloqueo de procesamiento es ahora la mayor oportunidad.</span><span class="sxs-lookup"><span data-stu-id="e821c-335">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="e821c-336">Un recurso de bloqueo de representación es un archivo de JavaScript o CSS externo que el explorador debe descargar, analizar y ejecutar antes de mostrar la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-336">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="e821c-337">El objetivo es ejecutar solo el código CSS básico y JavaScript necesario para mostrar la página correctamente.</span><span class="sxs-lookup"><span data-stu-id="e821c-337">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="e821c-338">La primera tarea, a continuación, es buscar código que no es necesario ejecutar en la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-338">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="e821c-339">Seleccione **eliminar recursos de bloqueo de procesamiento** para ver los recursos que están bloqueando:</span><span class="sxs-lookup"><span data-stu-id="e821c-339">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="e821c-340">y `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="e821c-340">and `jquery.js`.</span></span>  
    
    > ##### <span data-ttu-id="e821c-341">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="e821c-341">Figure 26</span></span>  
    > <span data-ttu-id="e821c-342">Más información sobre la oportunidad **eliminar recursos de bloqueo de procesamiento**</span><span class="sxs-lookup"><span data-stu-id="e821c-342">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    > <span data-ttu-id="e821c-343">! [Más información sobre la oportunidad para eliminar recursos de bloqueo de representación] [ImageRender]</span><span class="sxs-lookup"><span data-stu-id="e821c-343">![More information about the Eliminate render-blocking resources opportunity][ImageRender]</span></span>  
    
1.  <span data-ttu-id="e821c-344">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, comience a escribir `Coverage` y, a continuación, seleccione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="e821c-344">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    > ##### <span data-ttu-id="e821c-345">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="e821c-345">Figure 27</span></span>  
    > <span data-ttu-id="e821c-346">Abrir el menú de comandos desde el panel auditorías</span><span class="sxs-lookup"><span data-stu-id="e821c-346">Opening the Command Menu from the Audits panel</span></span>  
    > <span data-ttu-id="e821c-347">! [Abrir el menú de comandos del panel auditorías] [ImageCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="e821c-347">![Opening the Command Menu from the Audits panel][ImageCommandMenu]</span></span>  
    
    > ##### <span data-ttu-id="e821c-348">Ilustración 28</span><span class="sxs-lookup"><span data-stu-id="e821c-348">Figure 28</span></span>  
    > <span data-ttu-id="e821c-349">La ficha cobertura</span><span class="sxs-lookup"><span data-stu-id="e821c-349">The Coverage tab</span></span>  
    > <span data-ttu-id="e821c-350">! [Ficha cobertura] [ImageCoverage]</span><span class="sxs-lookup"><span data-stu-id="e821c-350">![The Coverage tab][ImageCoverage]</span></span>  
    
1.  <span data-ttu-id="e821c-351">Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="e821c-351">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="e821c-352">La pestaña **cobertura** proporciona una descripción general de la parte del código de `bundle.js` , `jquery.js` y `lodash.js` se ejecuta mientras se carga la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-352">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="e821c-353">La [figura 30](#figure-30) indica 76 que no se usan los archivos de jQuery y Lodash, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e821c-353">[Figure 30](#figure-30) says that about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    > ##### <span data-ttu-id="e821c-354">Ilustración 29</span><span class="sxs-lookup"><span data-stu-id="e821c-354">Figure 29</span></span>  
    > <span data-ttu-id="e821c-355">El informe de cobertura</span><span class="sxs-lookup"><span data-stu-id="e821c-355">The Coverage report</span></span>  
    > <span data-ttu-id="e821c-356">! [Informe de cobertura] [ImageCoverageReport]</span><span class="sxs-lookup"><span data-stu-id="e821c-356">![The Coverage report][ImageCoverageReport]</span></span>  
    
1.  <span data-ttu-id="e821c-357">Seleccione la fila **jQuery. js** .</span><span class="sxs-lookup"><span data-stu-id="e821c-357">Select the **jquery.js** row.</span></span>  <span data-ttu-id="e821c-358">DevTools abre el archivo en el panel fuentes.</span><span class="sxs-lookup"><span data-stu-id="e821c-358">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="e821c-359">Se ejecutó una línea de código si tiene una barra azul al lado.</span><span class="sxs-lookup"><span data-stu-id="e821c-359">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="e821c-360">Una barra roja significa que no se ha ejecutado y, por supuesto, no es necesaria en la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-360">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    > ##### <span data-ttu-id="e821c-361">Ilustración 30</span><span class="sxs-lookup"><span data-stu-id="e821c-361">Figure 30</span></span>  
    > <span data-ttu-id="e821c-362">Visualización del archivo jQuery en el panel orígenes</span><span class="sxs-lookup"><span data-stu-id="e821c-362">Viewing the jQuery file in the Sources panel</span></span>  
    > <span data-ttu-id="e821c-363">! [Visualización del archivo jQuery en el panel orígenes] [ImageJQuery]</span><span class="sxs-lookup"><span data-stu-id="e821c-363">![Viewing the jQuery file in the Sources panel][ImageJQuery]</span></span>  
    
1.  <span data-ttu-id="e821c-364">Desplácese un poco por el código jQuery.</span><span class="sxs-lookup"><span data-stu-id="e821c-364">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="e821c-365">Algunas de las líneas que reciben "ejecutar" son realmente solo Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e821c-365">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="e821c-366">La ejecución de este código a través de un minifier que elimina los comentarios es otra forma de reducir el tamaño de este archivo.</span><span class="sxs-lookup"><span data-stu-id="e821c-366">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="e821c-367">En Resumen, cuando está trabajando con su propio código, la pestaña cobertura le ayuda a analizar el código, línea por línea, y solo envía el código necesario para la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-367">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="e821c-368">¿Los `jquery.js` archivos y son `lodash.js` necesarios para cargar la página?</span><span class="sxs-lookup"><span data-stu-id="e821c-368">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="e821c-369">La pestaña bloqueo de solicitud muestra lo que sucede cuando los recursos no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="e821c-369">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="e821c-370">Seleccione la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="e821c-370">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="e821c-371">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para volver a abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="e821c-371">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="e821c-372">Comience `blocking` a escribir y, a continuación, seleccione **Mostrar bloqueo de solicitud**.</span><span class="sxs-lookup"><span data-stu-id="e821c-372">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    > ##### <span data-ttu-id="e821c-373">Ilustración 31</span><span class="sxs-lookup"><span data-stu-id="e821c-373">Figure 31</span></span>  
    > <span data-ttu-id="e821c-374">La ficha solicitar bloqueo</span><span class="sxs-lookup"><span data-stu-id="e821c-374">The Request Blocking tab</span></span>  
    > <span data-ttu-id="e821c-375">! [Ficha de bloqueo de solicitud] [ImageBlocking]</span><span class="sxs-lookup"><span data-stu-id="e821c-375">![The Request Blocking tab][ImageBlocking]</span></span>  
    
1.  <span data-ttu-id="e821c-376">Seleccione **Agregar** patrón ![ Agregar patrón ][ImageAddPatternIcon] , escriba `/libs/*` y, a continuación, presione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="e821c-376">Select **Add Pattern** ![Add Pattern][ImageAddPatternIcon], type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    > ##### <span data-ttu-id="e821c-377">Ilustración 32</span><span class="sxs-lookup"><span data-stu-id="e821c-377">Figure 32</span></span>  
    > <span data-ttu-id="e821c-378">Agregar un patrón para bloquear cualquier solicitud al `libs` directorio</span><span class="sxs-lookup"><span data-stu-id="e821c-378">Adding a pattern to block any request to the `libs` directory</span></span>  
    > <span data-ttu-id="e821c-379">! [Agregando un patrón para bloquear cualquier solicitud al directorio de bibliotecas] [ImageLibs]</span><span class="sxs-lookup"><span data-stu-id="e821c-379">![Adding a pattern to block any request to the libs directory][ImageLibs]</span></span>  
    
1.  <span data-ttu-id="e821c-380">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-380">Refresh the page.</span></span>  <span data-ttu-id="e821c-381">Las solicitudes jQuery y Lodash son rojas, lo que significa que las solicitudes se han bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e821c-381">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="e821c-382">Aún se carga la página y es interactiva, por lo que parece que no se necesitan estos recursos.</span><span class="sxs-lookup"><span data-stu-id="e821c-382">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    > ##### <span data-ttu-id="e821c-383">Ilustración 33</span><span class="sxs-lookup"><span data-stu-id="e821c-383">Figure 33</span></span>  
    > <span data-ttu-id="e821c-384">El panel red muestra que las solicitudes han sido bloqueadas</span><span class="sxs-lookup"><span data-stu-id="e821c-384">The Network panel shows that the requests have been blocked</span></span>  
    > <span data-ttu-id="e821c-385">! [El panel red muestra que las solicitudes han sido bloqueadas] [ImageBlockedLibs]</span><span class="sxs-lookup"><span data-stu-id="e821c-385">![The Network panel shows that the requests have been blocked][ImageBlockedLibs]</span></span>  
    
1.  <span data-ttu-id="e821c-386">Seleccionar **quitar todos los patrones** ![ quite todos los patrones ][ImageRemoveIcon] para eliminar el `/libs/*` patrón de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e821c-386">Select **Remove all patterns** ![Remove all patterns][ImageRemoveIcon] to delete the `/libs/*` blocking pattern.</span></span>  

<span data-ttu-id="e821c-387">En general, la pestaña bloqueo de solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e821c-387">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="e821c-388">Ahora, quite las referencias a estos archivos del código y audite de nuevo la página:</span><span class="sxs-lookup"><span data-stu-id="e821c-388">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="e821c-389">De nuevo en la pestaña Editor, Abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="e821c-389">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="e821c-390">Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="e821c-390">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="e821c-391">Espere a que el sitio se vuelva a compilar y a implementar.</span><span class="sxs-lookup"><span data-stu-id="e821c-391">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="e821c-392">Audite la página de nuevo desde el panel **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="e821c-392">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="e821c-393">Tu puntuación general debería haber mejorado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="e821c-393">Your overall score should have improved again.</span></span>  
    
    > ##### <span data-ttu-id="e821c-394">Ilustración 34</span><span class="sxs-lookup"><span data-stu-id="e821c-394">Figure 34</span></span>  
    > <span data-ttu-id="e821c-395">Un informe de auditoría después de quitar los recursos de bloqueo de representación</span><span class="sxs-lookup"><span data-stu-id="e821c-395">An Audits report after removing the render-blocking resources</span></span>  
    > <span data-ttu-id="e821c-396">! [Informe de auditoría después de quitar los recursos de bloqueo de representación] [ImageReport4]</span><span class="sxs-lookup"><span data-stu-id="e821c-396">![An Audits report after removing the render-blocking resources][ImageReport4]</span></span>  

#### <span data-ttu-id="e821c-397">Optimizar la ruta de representación crítica en el mundo real</span><span class="sxs-lookup"><span data-stu-id="e821c-397">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="e821c-398">La **ruta de representación crítica** se refiere al código que necesita para cargar una página.</span><span class="sxs-lookup"><span data-stu-id="e821c-398">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="e821c-399">En general, para acelerar la carga de páginas solo tienes que enviar código crítico durante la carga de la página y, a continuación, cargar de forma diferida todo lo demás.</span><span class="sxs-lookup"><span data-stu-id="e821c-399">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="e821c-400">Es improbable que encuentre secuencias de comandos que pueda quitar de forma inadecuada, pero es posible que encuentre muchas secuencias de comandos que no necesita solicitar durante la carga de la página y que, en su lugar, las solicite.</span><span class="sxs-lookup"><span data-stu-id="e821c-400">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="e821c-401">Si está usando un marco, compruebe si tiene un modo de producción.</span><span class="sxs-lookup"><span data-stu-id="e821c-401">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="e821c-402">Este modo puede usar una característica, como el [agitador de árboles][WebpackTreeShaking] , para eliminar el código innecesario que está bloqueando el procesamiento crítico.</span><span class="sxs-lookup"><span data-stu-id="e821c-402">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  

<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="e821c-403">Hacer menos trabajo del subproceso principal</span><span class="sxs-lookup"><span data-stu-id="e821c-403">Do less main thread work</span></span>   

<span data-ttu-id="e821c-404">Su último informe muestra algunos ahorros potenciales menores en la sección oportunidades, pero si ve en la sección diagnósticos, parece que la mayor parte de la actividad principal es la actividad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e821c-404">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="e821c-405">El subproceso principal es el lugar donde el explorador hace la mayor parte del trabajo necesario para mostrar una página, como analizar y ejecutar HTML, CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e821c-405">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="e821c-406">El objetivo es usar el panel rendimiento para analizar qué trabajo está haciendo el subproceso principal mientras se carga la página y buscar formas de aplazar o quitar el trabajo innecesario.</span><span class="sxs-lookup"><span data-stu-id="e821c-406">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="e821c-407">Seleccione la pestaña **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="e821c-407">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="e821c-408">Seleccione configuración de captura de **configuración** de ![ captura ][ImageCaptureIcon] .</span><span class="sxs-lookup"><span data-stu-id="e821c-408">Select **Capture Settings** ![Capture Settings][ImageCaptureIcon].</span></span>  
1.  <span data-ttu-id="e821c-409">Configure la **red** como **3G lento** y **CPU** a **6X lentitud**.</span><span class="sxs-lookup"><span data-stu-id="e821c-409">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="e821c-410">Por lo general, los dispositivos móviles tienen más restricciones de hardware que los equipos portátiles o de escritorio, por lo que esta configuración le permite experimentar la carga de la página como si estuviera usando un dispositivo menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="e821c-410">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="e821c-411">Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="e821c-411">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="e821c-412">DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargarla.</span><span class="sxs-lookup"><span data-stu-id="e821c-412">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="e821c-413">Esta visualización se conoce como la **traza**.</span><span class="sxs-lookup"><span data-stu-id="e821c-413">This visualization is referred to as the **trace**.</span></span>  
    
    > ##### <span data-ttu-id="e821c-414">Ilustración 35</span><span class="sxs-lookup"><span data-stu-id="e821c-414">Figure 35</span></span>  
    > <span data-ttu-id="e821c-415">Seguimiento del panel rendimiento de la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="e821c-415">The Performance panel trace of the page load</span></span>  
    > <span data-ttu-id="e821c-416">! [El seguimiento del panel rendimiento de la carga de página] [ImagePerformance]</span><span class="sxs-lookup"><span data-stu-id="e821c-416">![The Performance panel trace of the page load][ImagePerformance]</span></span>  

<span data-ttu-id="e821c-417">La traza muestra la actividad cronológicamente, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="e821c-417">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="e821c-418">Los gráficos de CPS, CPU y NET de la parte superior le ofrecen una descripción general de los fotogramas por segundo, la actividad de la CPU y la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="e821c-418">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="e821c-419">El bloque de amarillo seleccionado que se muestra en la [figura 37](#figure-37) significa que la CPU estaba completamente ocupada con la actividad de scripting.</span><span class="sxs-lookup"><span data-stu-id="e821c-419">The block of yellow selected that you see in [Figure 37](#figure-37) means that the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="e821c-420">Esta es una pista de que puede acelerar la carga de la página haciendo menos trabajo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e821c-420">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

> ##### <span data-ttu-id="e821c-421">Ilustración 36</span><span class="sxs-lookup"><span data-stu-id="e821c-421">Figure 36</span></span>  
> <span data-ttu-id="e821c-422">La sección información general de la traza</span><span class="sxs-lookup"><span data-stu-id="e821c-422">The Overview section of the trace</span></span>  
> <span data-ttu-id="e821c-423">! [Sección información general de la traza] [ImageOverview]</span><span class="sxs-lookup"><span data-stu-id="e821c-423">![The Overview section of the trace][ImageOverview]</span></span>  

<span data-ttu-id="e821c-424">Investigue el seguimiento para encontrar formas de hacer que el trabajo de JavaScript sea menor:</span><span class="sxs-lookup"><span data-stu-id="e821c-424">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="e821c-425">Seleccione la sección **intervalos** para expandirlo.</span><span class="sxs-lookup"><span data-stu-id="e821c-425">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="e821c-426">Basándose en el hecho de que puede haber una gran cantidad de medidas de [intervalos][MDNUserTimingApi] de reAct, parece que la aplicación de Tony usa el modo de desarrollo de reAct.</span><span class="sxs-lookup"><span data-stu-id="e821c-426">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="e821c-427">El cambio al modo de producción de reAct puede dar lugar a un resultado de fácil rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e821c-427">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    > ##### <span data-ttu-id="e821c-428">Ilustración 37</span><span class="sxs-lookup"><span data-stu-id="e821c-428">Figure 37</span></span>  
    > <span data-ttu-id="e821c-429">La sección intervalos</span><span class="sxs-lookup"><span data-stu-id="e821c-429">The Timings section</span></span>  
    > <span data-ttu-id="e821c-430">! [Sección intervalos] [ImageUserTiming]</span><span class="sxs-lookup"><span data-stu-id="e821c-430">![The Timings section][ImageUserTiming]</span></span>  

1.  <span data-ttu-id="e821c-431">Vuelva a seleccionar los **intervalos** para contraer la sección.</span><span class="sxs-lookup"><span data-stu-id="e821c-431">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="e821c-432">Examinar la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="e821c-432">Browse the **Main** section.</span></span>  <span data-ttu-id="e821c-433">En esta sección se muestra un registro cronológico de la actividad principal de la conversación, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="e821c-433">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="e821c-434">El eje y (de arriba a abajo) muestra por qué se produjeron eventos.</span><span class="sxs-lookup"><span data-stu-id="e821c-434">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="e821c-435">Por ejemplo, en la [figura 39](#figure-39), el `Evaluate Script` evento ha provocado la ejecución de la `(anonymous)` función, provocada por la ejecución `(anonymous)` , que ha provocado que se ejecutó `__webpack__require__` , etc.</span><span class="sxs-lookup"><span data-stu-id="e821c-435">For example, in [Figure 39](#figure-39), the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    > ##### <span data-ttu-id="e821c-436">Ilustración 38</span><span class="sxs-lookup"><span data-stu-id="e821c-436">Figure 38</span></span>  
    > <span data-ttu-id="e821c-437">La sección principal</span><span class="sxs-lookup"><span data-stu-id="e821c-437">The Main section</span></span>  
    > <span data-ttu-id="e821c-438">! [Sección principal] [ImageMain]</span><span class="sxs-lookup"><span data-stu-id="e821c-438">![The Main section][ImageMain]</span></span>  

1.  <span data-ttu-id="e821c-439">Desplácese hacia abajo hasta la parte inferior de la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="e821c-439">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="e821c-440">Cuando se usa un marco, la mayor parte de la actividad superior está causada por el marco de trabajo, que normalmente está fuera de su control.</span><span class="sxs-lookup"><span data-stu-id="e821c-440">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="e821c-441">La actividad causada por la aplicación suele estar en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="e821c-441">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="e821c-442">En esta aplicación, parece que una función llamada `App` está causando un gran número de solicitudes a una `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="e821c-442">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="e821c-443">Suena como Tony podría estar usando los dispositivos de sus ventiladores para minar cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="e821c-443">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    > ##### <span data-ttu-id="e821c-444">Ilustración 39</span><span class="sxs-lookup"><span data-stu-id="e821c-444">Figure 39</span></span>  
    > <span data-ttu-id="e821c-445">Mantener el mouse sobre la `mineBitcoin` actividad</span><span class="sxs-lookup"><span data-stu-id="e821c-445">Hovering over the `mineBitcoin` activity</span></span>  
    > <span data-ttu-id="e821c-446">! [Situar el puntero sobre la actividad de mineBitcoin] [ImageMine]</span><span class="sxs-lookup"><span data-stu-id="e821c-446">![Hovering over the mineBitcoin activity][ImageMine]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e821c-447">A pesar de que las solicitudes que el marco de trabajo realiza generalmente están fuera de su control, a veces puede estructurar la aplicación de forma que el marco de trabajo se ejecute ineficazmente.</span><span class="sxs-lookup"><span data-stu-id="e821c-447">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="e821c-448">Reestructurar la aplicación para usar el marco de forma eficaz es una forma de hacer menos trabajo de los subprocesos principales.</span><span class="sxs-lookup"><span data-stu-id="e821c-448">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="e821c-449">Sin embargo, esto requiere un conocimiento profundo de cómo funciona el marco y qué tipo de cambios se realizan en el código propio para poder usar el marco de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="e821c-449">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  

1.  <span data-ttu-id="e821c-450">Expanda la sección de **abajo** .</span><span class="sxs-lookup"><span data-stu-id="e821c-450">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="e821c-451">Esta pestaña desglosa qué actividades ocuparon la mayor parte del tiempo.</span><span class="sxs-lookup"><span data-stu-id="e821c-451">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="e821c-452">Si no ve nada en la sección de la parte inferior, haga clic en la etiqueta de la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="e821c-452">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="e821c-453">En la sección de la **parte inferior** se muestra solo la información de cualquier actividad o grupo de actividades que haya seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e821c-453">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="e821c-454">Por ejemplo, si hizo clic en una de las `mineBitcoin` actividades, la sección de **abajo** se mostrará solo la información de esa actividad.</span><span class="sxs-lookup"><span data-stu-id="e821c-454">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    > ##### <span data-ttu-id="e821c-455">Ilustración 40</span><span class="sxs-lookup"><span data-stu-id="e821c-455">Figure 40</span></span>  
    > <span data-ttu-id="e821c-456">La pestaña abajo</span><span class="sxs-lookup"><span data-stu-id="e821c-456">The Bottom-Up tab</span></span>  
    > <span data-ttu-id="e821c-457">! [La pestaña de la parte inferior] [ImageBottomUp]</span><span class="sxs-lookup"><span data-stu-id="e821c-457">![The Bottom-Up tab][ImageBottomUp]</span></span>  

<span data-ttu-id="e821c-458">La columna **Self Time** muestra la cantidad de tiempo que se dedicó directamente en cada actividad.</span><span class="sxs-lookup"><span data-stu-id="e821c-458">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="e821c-459">Por ejemplo, la [figura 41](#figure-41) muestra que aproximadamente el 63% del tiempo de rosca principal se dedicó a la `mineBitcoin` función.</span><span class="sxs-lookup"><span data-stu-id="e821c-459">For example, [Figure 41](#figure-41) shows that about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="e821c-460">Tiempo para ver si usar el modo de producción y reducir la actividad de JavaScript puede acelerar la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-460">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="e821c-461">Empezar con el modo de producción:</span><span class="sxs-lookup"><span data-stu-id="e821c-461">Start with production mode:</span></span>  

1.  <span data-ttu-id="e821c-462">En la pestaña Editor, Abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="e821c-462">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="e821c-463">Cambiar `"mode":"development"` a `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="e821c-463">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="e821c-464">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="e821c-464">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="e821c-465">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-465">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="e821c-466">Ilustración 41</span><span class="sxs-lookup"><span data-stu-id="e821c-466">Figure 41</span></span>  
    > <span data-ttu-id="e821c-467">Un informe de auditoría después de configurar WebPack para usar el modo de producción</span><span class="sxs-lookup"><span data-stu-id="e821c-467">An Audits report after configuring webpack to use production mode</span></span>  
    > <span data-ttu-id="e821c-468">! [Informe de auditoría después de configurar WebPack para usar el modo de producción] [ImageReport5]</span><span class="sxs-lookup"><span data-stu-id="e821c-468">![An Audits report after configuring webpack to use production mode][ImageReport5]</span></span>  

<span data-ttu-id="e821c-469">Reduzca la actividad de JavaScript eliminando la solicitud a `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="e821c-469">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="e821c-470">En la pestaña Editor, Abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="e821c-470">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="e821c-471">Comente la solicitud para `this.mineBitcoin(1500)` en el `constructor` .</span><span class="sxs-lookup"><span data-stu-id="e821c-471">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="e821c-472">Espere a que se implemente la nueva compilación.</span><span class="sxs-lookup"><span data-stu-id="e821c-472">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="e821c-473">Vuelva a auditar la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-473">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="e821c-474">Ilustración 42</span><span class="sxs-lookup"><span data-stu-id="e821c-474">Figure 42</span></span>  
    > <span data-ttu-id="e821c-475">Un informe de auditoría después de quitar el trabajo de JavaScript innecesario</span><span class="sxs-lookup"><span data-stu-id="e821c-475">An Audits report after removing unnecessary JavaScript work</span></span>  
    > <span data-ttu-id="e821c-476">! [Informe de auditoría después de quitar el trabajo de JavaScript innecesario] [ImageReport6]</span><span class="sxs-lookup"><span data-stu-id="e821c-476">![An Audits report after removing unnecessary JavaScript work][ImageReport6]</span></span>  

<span data-ttu-id="e821c-477">Parece que el último cambio causó un aumento de rendimiento masivo.</span><span class="sxs-lookup"><span data-stu-id="e821c-477">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="e821c-478">En esta sección se ofreció una breve introducción al panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e821c-478">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="e821c-479">Consulte [referencia de análisis de rendimiento][DevtoolsEvaluatePerformanceReference] para obtener más información sobre cómo analizar el rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="e821c-479">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="e821c-480">Trabajar con menos subprocesos principales en el mundo real</span><span class="sxs-lookup"><span data-stu-id="e821c-480">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="e821c-481">En general, el panel **rendimiento** es la manera más común de comprender qué actividad hace el sitio mientras se carga, y buscar formas de quitar actividades innecesarias.</span><span class="sxs-lookup"><span data-stu-id="e821c-481">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="e821c-482">Si prefiere un método que se sienta `console.log()` de la mejor manera, la [API de temporización de usuario][MDNUserTimingApi] le permite marcar arbitrariamente determinadas fases del ciclo de vida de la aplicación para realizar un seguimiento del tiempo que toma cada una de esas fases.</span><span class="sxs-lookup"><span data-stu-id="e821c-482">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="e821c-483">Resumen</span><span class="sxs-lookup"><span data-stu-id="e821c-483">Summary</span></span>   

*   <span data-ttu-id="e821c-484">Siempre que lo establezca para optimizar el rendimiento de la carga de un sitio, empiece siempre con una auditoría.</span><span class="sxs-lookup"><span data-stu-id="e821c-484">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="e821c-485">La auditoría establece una línea de base y le ofrece sugerencias sobre cómo mejorar.</span><span class="sxs-lookup"><span data-stu-id="e821c-485">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="e821c-486">Realice un cambio a la vez y audite la página después de cada cambio para ver cómo afecta el cambio en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e821c-486">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Ilustración 1: Tony the cat"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Ilustración 2: la ficha Editor"  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Ilustración 3: el menú que aparece después de hacer clic en Tony"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Ilustración 4: la pestaña demo"  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Ilustración 5: DevTools y la demostración"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Ilustración 6: DevTools desacoplado"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Ilustración 7: panel auditorías"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Ilustración 8: el informe para el panel auditorías del rendimiento del sitio"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[ImageOverall]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Metrics-collapsed-Metrics-Highlighted.msft.png "Ilustración 9: la puntuación de rendimiento general"  
[ImageMetrics]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Metrics-collapsed-Highlighted.msft.png "Figura 10: la sección métrica"  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Metrics-Expanded.msft.png "ilustración 11: seleccionar el botón de alternancia resaltado para expandir los elementos de métrica"  
[ImageScreenshots]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-View-Trace.msft.png "Ilustración 12: capturas de pantallas de la página durante la carga  
[ImageOpportunities]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Opportunities.msft.png "figura 13: sección oportunidades"  
[ImageCompression]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Opportunities-Expanded.msft.png "Ilustración 14: eliminar la oportunidad de recursos de bloqueo de procesamiento"  
[ImageReference]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-web-dev-performance-Audits.msft.png "Ilustración 15: documentación para la oportunidad eliminar recursos de bloqueo de representación"  
[ImageDiagnostics]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Diagnostics.msft.png "Figura 16: la sección de diagnóstico"  
[ImagePassed]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Passed-Audits.msft.png "Ilustración 17: la sección de auditorías superada"  
[ImageNetwork]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network.msft.png "ilustración 18: el panel red"  
[ImageLargeRows]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-use-Large-request-Rows.msft.png "Ilustración 19: filas grandes en la tabla solicitudes de red"  
[ImageHeaders]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-use-Large-request-Rows-bundle-JS.msft.png "Ilustración 20: la pestaña encabezados"  
[ImageServer]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Server-JS.msft.png "figura 21: edición de Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[ImageRequests]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-Main.msft.png "Ilustración 22: la columna tamaño ahora muestra 2 valores diferentes para los recursos de texto"  
[ImageGzip]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-bundle-JS-headers-Response.msft.png "Ilustración 23: la sección de encabezados de respuesta ahora contiene un `content-encoding` encabezado"  
[ImageReport2]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance.msft.png "Ilustración 24: un informe de auditoría después de habilitar la compresión de texto"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Compression-Small-images-Audits-performance.msft.png "figura 25: un informe de auditoría después de cambiar el tamaño de las imágenes"  
[ImageRender]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded.msft.png "ilustración 26: más información sobre la oportunidad eliminar recursos de bloqueo de representación"  
[ImageCommandMenu]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded-Command-coverage.msft.png "Ilustración 27: abrir el menú de comandos desde el panel auditoría"  
[ImageCoverage]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded-Drawer-coverage.msft.png "Ilustración 28: la pestaña cobertura"  
[ImageCoverageReport]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded-Drawer-Coverage-reloaded.msft.png "Ilustración 29: el informe de cobertura"  
[ImageJQuery]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-sources-Drawer-Coverage-reloaded-jQuery-js.msft.png "Ilustración 30: ver el archivo jQuery en el panel orígenes"  
[ImageBlocking]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Network-Drawer-request-blocking-Empty.msft.png "Ilustración 31: la pestaña bloqueo de solicitudes"  
[ImageLibs]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Network-Drawer-request-blocking-Added.msft.png "ilustración 32: agregar un patrón para bloquear cualquier solicitud al directorio de bibliotecas"  
[ImageBlockedLibs]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Network-reloaded-Drawer-request-blocking-Added.msft.png "Ilustración 33: el panel red muestra que las solicitudes han sido bloqueadas"  
[ImageReport4]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-2-Audits-performance.msft.png "Ilustración 34: un informe de auditoría después de quitar los recursos de bloqueo de representación"  
[ImagePerformance]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU.msft.png "Ilustración 35: seguimiento del panel de rendimiento de la carga de la página"  
[ImageOverview]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-Main-Highlight.msft.png "Ilustración 36: la sección de información general de la traza"  
[ImageUserTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings.msft.png "Ilustración 37: la sección intervalos"  
[ImageMain]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-Main.msft.png "Ilustración 38: la sección principal"  
[ImageMine]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings-minebitcoin.msft.png "Ilustración 39: mantener el puntero sobre la actividad de mineBitcoin"  
[ImageBottomUp]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings-Summary-minebitcoin.msft.png "Ilustración 40: la pestaña de abajo arriba"  
[ImageReport5]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-3-Audits-performance.msft.png "Ilustración 41: un informe de auditoría después de configurar WebPack para usar el modo de producción"  
[ImageReport6]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-4-Audits-performance.msft.png "Ilustración 42: un informe de auditoría después de quitar el trabajo de JavaScript innecesario"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referencia de análisis de rendimiento"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introducción a la clase de desarrollo web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimización de imagen esencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directivas-codificación de contenido | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de temporización de usuario | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Sacudida de árboles | paquete de WebPack"  

> [!NOTE]
> <span data-ttu-id="e821c-535">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e821c-535">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e821c-536">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e821c-536">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e821c-538">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e821c-538">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
