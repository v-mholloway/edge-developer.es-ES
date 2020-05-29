---
title: Inspeccionar la actividad de la red en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611815"
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





# <span data-ttu-id="a9b9c-103">Inspeccionar la actividad de la red en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a9b9c-103">Inspect Network Activity In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="a9b9c-104">Este es un tutorial práctico de algunas de las características de DevTools más usadas relacionadas con la inspección de la actividad de red de una página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="a9b9c-105">Consulte [referencia de red][DevtoolsNetworkReference] si desea examinar las características en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="a9b9c-106">Cuándo usar el panel red</span><span class="sxs-lookup"><span data-stu-id="a9b9c-106">When to use the Network panel</span></span>   

<span data-ttu-id="a9b9c-107">En general, use el panel red cuando necesite asegurarse de que los recursos se van a descargar o cargar según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="a9b9c-108">Los casos de uso más comunes para el panel red son:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="a9b9c-109">Asegurándote de que los recursos se carguen o descarguen realmente.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="a9b9c-110">Inspeccione las propiedades de un recurso individual, como los encabezados HTTP, el contenido, el tamaño, etc.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  

<span data-ttu-id="a9b9c-111">Si está buscando formas de mejorar el rendimiento de la carga de páginas, **no** empiece por el panel red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="a9b9c-112">Hay muchos tipos de problemas de rendimiento de la carga que no están relacionados con la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="a9b9c-113">Comience con el panel auditorías porque le ofrece sugerencias específicas sobre cómo mejorar la página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="a9b9c-114">Consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="a9b9c-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="a9b9c-115">Abrir el panel de red</span><span class="sxs-lookup"><span data-stu-id="a9b9c-115">Open the Network panel</span></span>   

<span data-ttu-id="a9b9c-116">Para sacar el máximo provecho de este tutorial, abra la demostración y pruebe las características de la página de demostración.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="a9b9c-117">Abra la [demostración introducción][GlitchNetworkGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-117">Open the [Get Started Demo][GlitchNetworkGetStarted] .</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-118">Figura 1</span><span class="sxs-lookup"><span data-stu-id="a9b9c-118">Figure 1</span></span>  
    > <span data-ttu-id="a9b9c-119">La demostración</span><span class="sxs-lookup"><span data-stu-id="a9b9c-119">The demo</span></span>  
    > ![La demostración][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  <span data-ttu-id="a9b9c-121">[Abra DevTools][DevToolsOpen] presionando `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="a9b9c-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="a9b9c-122">Se abre el panel de la **consola** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-122">The **Console** panel opens.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="a9b9c-123">Figure 2</span></span>  
    > <span data-ttu-id="a9b9c-124">La consola</span><span class="sxs-lookup"><span data-stu-id="a9b9c-124">The Console</span></span>  
    > <span data-ttu-id="a9b9c-125">! [La consola] [ImagesTutorialConsole]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-125">![The Console][ImagesTutorialConsole]</span></span>  
    
    <span data-ttu-id="a9b9c-126">Es posible que prefiera [acoplar DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="a9b9c-126">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-127">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="a9b9c-127">Figure 3</span></span>  
    > <span data-ttu-id="a9b9c-128">DevTools acoplado en la parte inferior de la ventana</span><span class="sxs-lookup"><span data-stu-id="a9b9c-128">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="a9b9c-129">! [DevTools acoplada a la parte inferior de la ventana] [ImagesTutorialDocked]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-129">![DevTools docked to the bottom of the window][ImagesTutorialDocked]</span></span>  

1.  <span data-ttu-id="a9b9c-130">Seleccione la pestaña **red** .  Se abre el panel red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-130">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-131">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="a9b9c-131">Figure 4</span></span>  
    > <span data-ttu-id="a9b9c-132">DevTools acoplado en la parte inferior de la ventana</span><span class="sxs-lookup"><span data-stu-id="a9b9c-132">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="a9b9c-133">! [DevTools acoplada a la parte inferior de la ventana] [ImagesTutorialNetwork]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-133">![DevTools docked to the bottom of the window][ImagesTutorialNetwork]</span></span>  

<span data-ttu-id="a9b9c-134">Ahora el panel red está vacío.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-134">Right now the Network panel is empty.</span></span>  <span data-ttu-id="a9b9c-135">DevTools solo registra la actividad de la red después de abrirla y no se ha producido ninguna actividad de red desde que abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-135">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="a9b9c-136">Registrar actividad de la red</span><span class="sxs-lookup"><span data-stu-id="a9b9c-136">Log network activity</span></span>   

<span data-ttu-id="a9b9c-137">Para ver la actividad de red que provoca una página:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-137">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="a9b9c-138">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-138">Reload the page.</span></span>  <span data-ttu-id="a9b9c-139">El panel red registra toda la actividad de la red en el **registro de red**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-139">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-140">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="a9b9c-140">Figure 5</span></span>  
    > <span data-ttu-id="a9b9c-141">El registro de red</span><span class="sxs-lookup"><span data-stu-id="a9b9c-141">The Network Log</span></span>  
    > <span data-ttu-id="a9b9c-142">! [El registro de red] [ImagesTutorialLog]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-142">![The Network Log][ImagesTutorialLog]</span></span>  
    
    <span data-ttu-id="a9b9c-143">Cada fila del **registro de red** representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-143">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="a9b9c-144">De forma predeterminada, los recursos se muestran cronológicamente.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-144">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="a9b9c-145">El recurso superior suele ser el documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-145">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="a9b9c-146">El recurso inferior es el último que se solicitó.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-146">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="a9b9c-147">Cada columna representa información acerca de un recurso.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-147">Each column represents information about a resource.</span></span>  <span data-ttu-id="a9b9c-148">En la [**figura 6**](#figure-6) se muestran las columnas predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-148">[**Figure 6**](#figure-6) shows the default columns:</span></span>  

    *   <span data-ttu-id="a9b9c-149">**Estado**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-149">**Status**.</span></span>  <span data-ttu-id="a9b9c-150">El código de Estado HTTP para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-150">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="a9b9c-151">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-151">**Type**.</span></span>  <span data-ttu-id="a9b9c-152">El tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-152">The resource type.</span></span>  
    *   <span data-ttu-id="a9b9c-153">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-153">**Initiator**.</span></span>  <span data-ttu-id="a9b9c-154">La causa de la solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-154">The cause of the resource request.</span></span>  <span data-ttu-id="a9b9c-155">Al seleccionar un vínculo en la columna iniciador, se le lleva al código fuente que causó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-155">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="a9b9c-156">**Momento**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-156">**Time**.</span></span>  <span data-ttu-id="a9b9c-157">La duración de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-157">The duration of the request.</span></span>  
    *   <span data-ttu-id="a9b9c-158">**Cascada**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-158">**Waterfall**.</span></span>  <span data-ttu-id="a9b9c-159">Una representación gráfica de las distintas etapas de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-159">A graphical representation of the different stages of the request.</span></span>  
        <span data-ttu-id="a9b9c-160">Desplace el puntero sobre una cascada para ver un desglose.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-160">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a9b9c-161">El gráfico que se encuentra sobre el registro de red se denomina Descripción general.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-161">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="a9b9c-162">No usará el gráfico de información general en este tutorial, por lo que puede ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-162">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="a9b9c-163">Vea [ocultar el panel de información general][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="a9b9c-163">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
        
1.  <span data-ttu-id="a9b9c-164">Después de abrir DevTools, registra la actividad de la red en el registro de red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-164">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="a9b9c-165">Para demostrarlo, primero mire la parte inferior del **registro de red** y tome nota mental de la última actividad.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-165">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="a9b9c-166">Ahora, seleccione el botón **obtener datos** en la demostración.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-166">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="a9b9c-167">Vuelva a mirar la parte inferior del **registro de red** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-167">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="a9b9c-168">Debería ver un nuevo recurso denominado `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-168">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="a9b9c-169">Si selecciona el botón **obtener datos** , la página solicitará este archivo.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-169">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-170">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="a9b9c-170">Figure 6</span></span>  
    > <span data-ttu-id="a9b9c-171">Un nuevo recurso en el registro de red</span><span class="sxs-lookup"><span data-stu-id="a9b9c-171">A new resource in the Network Log</span></span>  
    > <span data-ttu-id="a9b9c-172">! [Un nuevo recurso en el registro de red] [ImagesTutorialRuntime]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-172">![A new resource in the Network Log][ImagesTutorialRuntime]</span></span>  

## <span data-ttu-id="a9b9c-173">Mostrar más información</span><span class="sxs-lookup"><span data-stu-id="a9b9c-173">Show more information</span></span>   

<span data-ttu-id="a9b9c-174">Las columnas del registro de red se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-174">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="a9b9c-175">Puede ocultar las columnas que no está usando.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-175">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="a9b9c-176">También hay muchas columnas que están ocultas de forma predeterminada, que pueden resultarle útiles.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-176">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="a9b9c-177">Haga clic con el botón derecho en el encabezado de la tabla registro de red y seleccione **dominio**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-177">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="a9b9c-178">Ahora se muestra el dominio de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-178">The domain of each resource is now shown.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-179">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="a9b9c-179">Figure 7</span></span>  
    > <span data-ttu-id="a9b9c-180">Habilitar la columna dominio</span><span class="sxs-lookup"><span data-stu-id="a9b9c-180">Enabling the Domain column</span></span>  
    > <span data-ttu-id="a9b9c-181">! [Habilitar la columna dominio] [ImagesTutorialDomain]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-181">![Enabling the Domain column][ImagesTutorialDomain]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="a9b9c-182">Vea la dirección URL completa de un recurso colocando el puntero sobre la celda en la columna **nombre** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-182">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  

## <span data-ttu-id="a9b9c-183">Simular una conexión de red más lenta</span><span class="sxs-lookup"><span data-stu-id="a9b9c-183">Simulate a slower network connection</span></span>   

<span data-ttu-id="a9b9c-184">Es probable que la conexión de red del equipo que use para crear sitios sea más rápida que las conexiones de red de los dispositivos móviles de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-184">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="a9b9c-185">Al limitar la página, se obtiene una idea más extensa de cuánto tarda una página en cargarse en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-185">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="a9b9c-186">Seleccione la lista desplegable **límite** , que está establecida en **conectado** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-186">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-187">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="a9b9c-187">Figure 8</span></span>  
    > <span data-ttu-id="a9b9c-188">Habilitar la limitación</span><span class="sxs-lookup"><span data-stu-id="a9b9c-188">Enabling throttling</span></span>  
    > <span data-ttu-id="a9b9c-189">! [Habilitar limitación de peticiones] [ImagesTutorialThrottling]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-189">![Enabling throttling][ImagesTutorialThrottling]</span></span>  
    
1.  <span data-ttu-id="a9b9c-190">Seleccione **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-190">Select **Slow 3G**.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-191">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="a9b9c-191">Figure 9</span></span>  
    > <span data-ttu-id="a9b9c-192">Selección de 3G lento</span><span class="sxs-lookup"><span data-stu-id="a9b9c-192">Selecting Slow 3G</span></span>  
    > <span data-ttu-id="a9b9c-193">! [Seleccionando 3G lento] [ImagesTutorialSlow3G]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-193">![Selecting Slow 3G][ImagesTutorialSlow3G]</span></span>  
    
1.  <span data-ttu-id="a9b9c-194">Haga **clic en volver a** cargar ![ ][ImageRefreshIcon] y, después, seleccione **vaciar caché y volver a carga**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-194">Long-press **Reload** ![Reload][ImageRefreshIcon] and then select **Empty Cache And Hard Reload**.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-195">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="a9b9c-195">Figure 10</span></span>  
    > <span data-ttu-id="a9b9c-196">Memoria caché vacía y recarga duro</span><span class="sxs-lookup"><span data-stu-id="a9b9c-196">Empty Cache And Hard Reload</span></span>  
    > <span data-ttu-id="a9b9c-197">! [Caché vacía y recargada de disco duro] [ImagesTutorialHardReload]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-197">![Empty Cache And Hard Reload][ImagesTutorialHardReload]</span></span>  
    
    <span data-ttu-id="a9b9c-198">En las visitas repetidas, el explorador generalmente sirve algunos archivos de la [caché][MDNHTTPCache] , lo que acelera la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-198">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache] , which speeds up the page load.</span></span>  <span data-ttu-id="a9b9c-199">**Vaciar la memoria caché y la recarga de disco** obliga al explorador a dirigirse a la red para todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-199">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="a9b9c-200">Esto es útil cuando desea ver cómo experimenta un primer visitante la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-200">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a9b9c-201">El flujo de trabajo **vacío y la recarga de disco duro** solo está disponible cuando DevTools está abierto.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-201">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  

## <span data-ttu-id="a9b9c-202">Capturar capturas de pantallas</span><span class="sxs-lookup"><span data-stu-id="a9b9c-202">Capture screenshots</span></span>   

<span data-ttu-id="a9b9c-203">Las capturas de pantallas le permiten ver cómo se ha enviado una página a lo largo del tiempo mientras se cargaba.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-203">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="a9b9c-204">Seleccione ![ configuración de red ][ImageSettingsIcon] y seleccione la casilla **capturar capturas de pantallas** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-204">Select ![Network settings][ImageSettingsIcon] and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="a9b9c-205">Vuelva a cargar la página a través del flujo de trabajo **vacío y de recarga de disco** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-205">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="a9b9c-206">Consulte [simular una conexión más lenta](#simulate-a-slower-network-connection) si necesita un aviso sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-206">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="a9b9c-207">El panel capturas de pantallas proporciona miniaturas de la apariencia de la página en varios puntos durante el proceso de carga.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-207">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-208">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="a9b9c-208">Figure 11</span></span>  
    > <span data-ttu-id="a9b9c-209">Capturas de pantallas de la carga de la página</span><span class="sxs-lookup"><span data-stu-id="a9b9c-209">Screenshots of the page load</span></span>  
    > <span data-ttu-id="a9b9c-210">! [Capturas de pantallas de la carga de la página] [ImagesTutorialAllScreenshots]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-210">![Screenshots of the page load][ImagesTutorialAllScreenshots]</span></span>  

1.  <span data-ttu-id="a9b9c-211">Seleccionar la primera miniatura.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-211">Select the first thumbnail.</span></span>  <span data-ttu-id="a9b9c-212">DevTools muestra qué actividad de la red tuvo lugar en ese momento.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-212">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-213">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="a9b9c-213">Figure 12</span></span>  
    > <span data-ttu-id="a9b9c-214">La actividad de red que se produjo durante la primera captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="a9b9c-214">The network activity that was happening during the first screenshot</span></span>  
    > <span data-ttu-id="a9b9c-215">! [La actividad de red que se estaba realizando durante la primera captura de pantalla] [ImagesTutorialFirstScreenshot]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-215">![The network activity that was happening during the first screenshot][ImagesTutorialFirstScreenshot]</span></span>  

1.  <span data-ttu-id="a9b9c-216">Vuelva a seleccionar ![ la configuración de red ][ImageSettingsIcon] y desactive la casilla **capturar capturas** de pantallas para cerrar el panel capturas de pantallas.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-216">Select ![Network settings][ImageSettingsIcon] again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="a9b9c-217">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-217">Reload the page again.</span></span>  

## <span data-ttu-id="a9b9c-218">Inspeccionar los detalles del recurso</span><span class="sxs-lookup"><span data-stu-id="a9b9c-218">Inspect the details of the resource</span></span>   

<span data-ttu-id="a9b9c-219">Seleccione un recurso para obtener más información sobre él.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-219">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="a9b9c-220">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-220">Try it now:</span></span>  

1.  <span data-ttu-id="a9b9c-221">Seleccione `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-221">Select `getstarted.html`.</span></span>  <span data-ttu-id="a9b9c-222">Se muestra la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-222">The **Headers** tab is shown.</span></span>  <span data-ttu-id="a9b9c-223">Use esta pestaña para inspeccionar los encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-223">Use this tab to inspect HTTP headers.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-224">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="a9b9c-224">Figure 13</span></span>  
    > <span data-ttu-id="a9b9c-225">La pestaña encabezados</span><span class="sxs-lookup"><span data-stu-id="a9b9c-225">The Headers tab</span></span>  
    > <span data-ttu-id="a9b9c-226">! [Ficha encabezados] [ImagesTutorialHeaders]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-226">![The Headers tab][ImagesTutorialHeaders]</span></span>  
    
1.  <span data-ttu-id="a9b9c-227">Seleccione la pestaña **vista previa** .  Se muestra una representación básica del HTML.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-227">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-228">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="a9b9c-228">Figure 14</span></span>  
    > <span data-ttu-id="a9b9c-229">La ficha vista previa</span><span class="sxs-lookup"><span data-stu-id="a9b9c-229">The Preview tab</span></span>  
    > <span data-ttu-id="a9b9c-230">! [Ficha vista previa] [ImagesTutorialPreview]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-230">![The Preview tab][ImagesTutorialPreview]</span></span>  

     <span data-ttu-id="a9b9c-231">Esta pestaña es útil cuando una API devuelve un código de error en HTML.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-231">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="a9b9c-232">Es posible que le resulte más fácil leer el código HTML representado que el código fuente HTML o cuando Inspeccione imágenes.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-232">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="a9b9c-233">Seleccione la pestaña **respuesta** .  Se muestra el código fuente HTML.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-233">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-234">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="a9b9c-234">Figure 15</span></span>  
    > <span data-ttu-id="a9b9c-235">La ficha respuesta</span><span class="sxs-lookup"><span data-stu-id="a9b9c-235">The Response tab</span></span>  
    > <span data-ttu-id="a9b9c-236">! [La pestaña respuesta] [ImagesTutorialResponse]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-236">![The Response tab][ImagesTutorialResponse]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="a9b9c-237">Cuando se minified un archivo, al seleccionar **el** ![ botón formato de formato ][ImageFormatIcon] en la parte inferior de la pestaña **respuesta** , se cambia el formato del contenido para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-237">When a file is minified, selecting the **Format** ![Format][ImageFormatIcon] button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  

1.  <span data-ttu-id="a9b9c-238">Seleccione la pestaña **intervalos** .  Se muestra un desglose de la actividad de red de este recurso.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-238">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-239">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="a9b9c-239">Figure 16</span></span>  
    > <span data-ttu-id="a9b9c-240">La ficha intervalos</span><span class="sxs-lookup"><span data-stu-id="a9b9c-240">The Timing tab</span></span>  
    > <span data-ttu-id="a9b9c-241">! [Ficha intervalos] [ImagesTutorialTiming]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-241">![The Timing tab][ImagesTutorialTiming]</span></span>  

1.  <span data-ttu-id="a9b9c-242">Seleccione **cerrar** ![ y, a continuación, ][ImageCloseIcon] vuelva a ver el registro de red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-242">Select **Close** ![Close][ImageCloseIcon] to view the Network Log again.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-243">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="a9b9c-243">Figure 17</span></span>  
    > <span data-ttu-id="a9b9c-244">Botón cerrar</span><span class="sxs-lookup"><span data-stu-id="a9b9c-244">The Close button</span></span>  
    > <span data-ttu-id="a9b9c-245">! [El botón cerrar] [ImagesTutorialCloseTiming]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-245">![The Close button][ImagesTutorialCloseTiming]</span></span>  

## <span data-ttu-id="a9b9c-246">Buscar encabezados y respuestas de red</span><span class="sxs-lookup"><span data-stu-id="a9b9c-246">Search network headers and responses</span></span>   

<span data-ttu-id="a9b9c-247">Use el panel de **búsqueda** cuando necesite buscar en los encabezados y las respuestas http de todos los recursos para una cadena determinada o una expresión normal.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-247">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="a9b9c-248">Por ejemplo, supongamos que desea comprobar que los recursos usan **directivas de caché**razonables.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-248">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="a9b9c-249">Seleccione búsqueda de **búsqueda** ![ ][ImageSearchIcon] .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-249">Select **Search** ![Search][ImageSearchIcon].</span></span>  <span data-ttu-id="a9b9c-250">El panel de búsqueda se abre a la izquierda del registro de red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-250">The Search pane opens to the left of the Network log.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-251">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="a9b9c-251">Figure 18</span></span>  
    > <span data-ttu-id="a9b9c-252">El panel de búsqueda</span><span class="sxs-lookup"><span data-stu-id="a9b9c-252">The Search pane</span></span>  
    > <span data-ttu-id="a9b9c-253">! [Panel de búsqueda] [ImagesTutorialSearch]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-253">![The Search pane][ImagesTutorialSearch]</span></span>  

1.  <span data-ttu-id="a9b9c-254">Escriba `Cache-Control` y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-254">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="a9b9c-255">El panel de búsqueda muestra todas las instancias de las `Cache-Control` que encuentra en los encabezados de recursos o en el contenido.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-255">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-256">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="a9b9c-256">Figure 19</span></span>  
    > <span data-ttu-id="a9b9c-257">Resultados de búsqueda de </span><span class="sxs-lookup"><span data-stu-id="a9b9c-257">Search results for</span></span> `Cache-Control`  
    > <span data-ttu-id="a9b9c-258">! [Resultados de la búsqueda de control de caché] [ImagesTutorialResults]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-258">![Search results for Cache-Control][ImagesTutorialResults]</span></span>  

1.  <span data-ttu-id="a9b9c-259">Seleccione un resultado para ver el recurso en el que se encontró el resultado.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-259">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="a9b9c-260">Si está viendo los detalles del recurso, seleccione un resultado para ir directamente a él.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-260">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="a9b9c-261">Por ejemplo, si la consulta se encuentra en un encabezado, se abre la pestaña encabezados.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-261">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="a9b9c-262">Si la consulta se encuentra en el contenido, se abre la pestaña **respuesta** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-262">If the query was found in content, the **Response** tab opens.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-263">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="a9b9c-263">Figure 20</span></span>  
    > <span data-ttu-id="a9b9c-264">Un resultado de búsqueda resaltado en la pestaña encabezados</span><span class="sxs-lookup"><span data-stu-id="a9b9c-264">A search result highlighted in the Headers tab</span></span>  
    > <span data-ttu-id="a9b9c-265">! [Resultado de la búsqueda resaltado en la pestaña encabezados] [ImagesTutorialCache]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-265">![A search result highlighted in the Headers tab][ImagesTutorialCache]</span></span>  
    
1.  <span data-ttu-id="a9b9c-266">Cierre el panel de búsqueda y la pestaña encabezados.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-266">Close the Search pane and the Headers tab.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-267">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="a9b9c-267">Figure 21</span></span>  
    > <span data-ttu-id="a9b9c-268">Los botones cerrar</span><span class="sxs-lookup"><span data-stu-id="a9b9c-268">The Close buttons</span></span>  
    > <span data-ttu-id="a9b9c-269">! [Los botones cerrar] [ImagesTutorialCloseButtons]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-269">![The Close buttons][ImagesTutorialCloseButtons]</span></span>  
    
## <span data-ttu-id="a9b9c-270">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="a9b9c-270">Filter resources</span></span>   

<span data-ttu-id="a9b9c-271">DevTools proporciona numerosos flujos de trabajo para filtrar recursos que no son relevantes para la tarea que está realizando.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-271">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

> ##### <span data-ttu-id="a9b9c-272">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="a9b9c-272">Figure 22</span></span>  
> <span data-ttu-id="a9b9c-273">La barra de herramientas filtros</span><span class="sxs-lookup"><span data-stu-id="a9b9c-273">The Filters toolbar</span></span>  
> <span data-ttu-id="a9b9c-274">! [La barra de herramientas filtros] [ImagesTutorialFilters]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-274">![The Filters toolbar][ImagesTutorialFilters]</span></span>  

<span data-ttu-id="a9b9c-275">La barra de herramientas **filtros** debería estar habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-275">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="a9b9c-276">De lo contrario:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-276">If not:</span></span>  

1.  <span data-ttu-id="a9b9c-277">Seleccione filtro de **filtro** ![ ][ImageFilterIcon] para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-277">Select **Filter** ![Filter][ImageFilterIcon] to show it.</span></span>  

### <span data-ttu-id="a9b9c-278">Filtrar por cadena, expresión regular o propiedad</span><span class="sxs-lookup"><span data-stu-id="a9b9c-278">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="a9b9c-279">El cuadro de texto **filtro** admite muchos tipos de filtrado diferentes.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-279">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="a9b9c-280">Escriba `png` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-280">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="a9b9c-281">Solo se muestran los archivos que contienen el texto `png` .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-281">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="a9b9c-282">En este caso, los únicos archivos que coinciden con el filtro son las imágenes PNG.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-282">In this case the only files that match the filter are the PNG images.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-283">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="a9b9c-283">Figure 23</span></span>  
    > <span data-ttu-id="a9b9c-284">Un filtro de cadena</span><span class="sxs-lookup"><span data-stu-id="a9b9c-284">A string filter</span></span>  
    > <span data-ttu-id="a9b9c-285">! [Un filtro de cadena] [ImagesTutorialPNG]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-285">![A string filter][ImagesTutorialPNG]</span></span>  

1.  <span data-ttu-id="a9b9c-286">Escribe `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-286">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="a9b9c-287">DevTools filtra cualquier recurso con un nombre de archivo que no termina con un `j` o a `c` , seguido de 1 o más `s` caracteres.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-287">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-288">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="a9b9c-288">Figure 24</span></span>  
    > <span data-ttu-id="a9b9c-289">Filtro de expresión regular</span><span class="sxs-lookup"><span data-stu-id="a9b9c-289">A regular expression filter</span></span>  
    > <span data-ttu-id="a9b9c-290">! [Un filtro de expresiones regulares] [ImagesTutorialRegEx]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-290">![A regular expression filter][ImagesTutorialRegEx]</span></span>  
    
1.  <span data-ttu-id="a9b9c-291">Escribe `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-291">Type `-main.css`.</span></span>  <span data-ttu-id="a9b9c-292">DevTools filtra `main.css` .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-292">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="a9b9c-293">Si cualquier otro archivo coincide con el patrón, también se filtrarían.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-293">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-294">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="a9b9c-294">Figure 25</span></span>  
    > <span data-ttu-id="a9b9c-295">Un filtro negativo</span><span class="sxs-lookup"><span data-stu-id="a9b9c-295">A negative filter</span></span>  
    > <span data-ttu-id="a9b9c-296">! [Un filtro negativo] [ImagesTutorialNegative]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-296">![A negative filter][ImagesTutorialNegative]</span></span>  
    
1.  <span data-ttu-id="a9b9c-297">Escriba `domain:cdn.glitch.com` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-297">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="a9b9c-298">DevTools filtra cualquier recurso con una dirección URL que no coincida con este dominio.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-298">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-299">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="a9b9c-299">Figure 26</span></span>  
    > <span data-ttu-id="a9b9c-300">Un filtro de propiedad</span><span class="sxs-lookup"><span data-stu-id="a9b9c-300">A property filter</span></span>  
    > <span data-ttu-id="a9b9c-301">! [Un filtro de propiedad] [ImagesTutorialProperty]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-301">![A property filter][ImagesTutorialProperty]</span></span>  

    <span data-ttu-id="a9b9c-302">Vea [filtrar solicitudes por propiedades][DevtoolsReferenceProperty] para obtener una lista completa de las propiedades que se pueden filtrar.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-302">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
    
1.  <span data-ttu-id="a9b9c-303">Borre el cuadro de texto de **filtro** de cualquier texto.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-303">Clear the **Filter** text box of any text.</span></span>  

### <span data-ttu-id="a9b9c-304">Filtrar por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="a9b9c-304">Filter by resource type</span></span>   

<span data-ttu-id="a9b9c-305">Para centrarse en un determinado tipo de archivo, como las hojas de estilos:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-305">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="a9b9c-306">Seleccione **CSS**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-306">Select **CSS**.</span></span>  <span data-ttu-id="a9b9c-307">Se filtran todos los demás tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-307">All other file types are filtered out.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-308">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="a9b9c-308">Figure 27</span></span>  
    > <span data-ttu-id="a9b9c-309">Mostrar solo archivos CSS</span><span class="sxs-lookup"><span data-stu-id="a9b9c-309">Showing CSS files only</span></span>  
    > <span data-ttu-id="a9b9c-310">! [Solo mostrar archivos CSS] [ImagesTutorialCSS]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-310">![Showing CSS files only][ImagesTutorialCSS]</span></span>  
    
1.  <span data-ttu-id="a9b9c-311">Para ver también las secuencias de comandos, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione **JS**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-311">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-312">Ilustración 28</span><span class="sxs-lookup"><span data-stu-id="a9b9c-312">Figure 28</span></span>  
    > <span data-ttu-id="a9b9c-313">Mostrar solo archivos CSS y JS</span><span class="sxs-lookup"><span data-stu-id="a9b9c-313">Showing CSS and JS files only</span></span>  
    > <span data-ttu-id="a9b9c-314">! [Solo mostrar archivos CSS y JS] [ImagesTutorialCSSJS]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-314">![Showing CSS and JS files only][ImagesTutorialCSSJS]</span></span>  
    
1.  <span data-ttu-id="a9b9c-315">Seleccione **todo** para quitar los filtros y volver a ver todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-315">Select **All** to remove the filters and see all resources again.</span></span>  

<span data-ttu-id="a9b9c-316">Consulte [filtrar solicitudes][DevtoolsNetworkReferenceFilter] para otros flujos de trabajo de filtrado.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-316">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="a9b9c-317">Solicitudes de bloqueo</span><span class="sxs-lookup"><span data-stu-id="a9b9c-317">Block requests</span></span>   

<span data-ttu-id="a9b9c-318">¿Cómo se ve y se comporta una página cuando algunos de los recursos de la página no están disponibles?</span><span class="sxs-lookup"><span data-stu-id="a9b9c-318">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="a9b9c-319">¿Se produce un error completamente o aún es funcional?</span><span class="sxs-lookup"><span data-stu-id="a9b9c-319">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="a9b9c-320">Bloquear solicitudes para averiguar:</span><span class="sxs-lookup"><span data-stu-id="a9b9c-320">Block requests to find out:</span></span>  

1.  <span data-ttu-id="a9b9c-321">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-321">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-322">Ilustración 29</span><span class="sxs-lookup"><span data-stu-id="a9b9c-322">Figure 29</span></span>  
    > <span data-ttu-id="a9b9c-323">El menú de comandos</span><span class="sxs-lookup"><span data-stu-id="a9b9c-323">The Command Menu</span></span>  
    > <span data-ttu-id="a9b9c-324">! [El menú comando] [ImagesTutorialCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-324">![The Command Menu][ImagesTutorialCommandMenu]</span></span>  
    
1.  <span data-ttu-id="a9b9c-325">Escriba `block` , seleccione **Mostrar bloqueo de solicitud**y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-325">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-326">Ilustración 30</span><span class="sxs-lookup"><span data-stu-id="a9b9c-326">Figure 30</span></span>  
    > <span data-ttu-id="a9b9c-327">Mostrar bloqueo de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9b9c-327">Show Request Blocking</span></span>  
    > <span data-ttu-id="a9b9c-328">! [Mostrar bloqueo de solicitudes] [ImagesTutorialBlock]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-328">![Show Request Blocking][ImagesTutorialBlock]</span></span>  

1.  <span data-ttu-id="a9b9c-329">Seleccione **Agregar** patrón de adición de patrón ![ ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-329">Select **Add Pattern** ![Add Pattern][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="a9b9c-330">Escribe `main.css`.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-330">Type `main.css`.</span></span>  
    
    > ##### <span data-ttu-id="a9b9c-331">Ilustración 31</span><span class="sxs-lookup"><span data-stu-id="a9b9c-331">Figure 31</span></span>  
    > <span data-ttu-id="a9b9c-332">Bugs</span><span class="sxs-lookup"><span data-stu-id="a9b9c-332">Blocking</span></span> `main.css`  
    > <span data-ttu-id="a9b9c-333">! [Bloqueo de Main. CSS] [ImagesTutorialAddBlock]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-333">![Blocking main.css][ImagesTutorialAddBlock]</span></span>  
    
1.  <span data-ttu-id="a9b9c-334">Seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-334">Select **Add**.</span></span>  
1.  <span data-ttu-id="a9b9c-335">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-335">Reload the page.</span></span>  <span data-ttu-id="a9b9c-336">Como se espera, el estilo de la página está ligeramente desordenado porque la hoja de estilos principal ha sido bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-336">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a9b9c-337">La `main.css` fila en el registro de red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-337">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="a9b9c-338">El texto en rojo significa que el recurso se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-338">The red text means that the resource was blocked.</span></span>
    
    > ##### <span data-ttu-id="a9b9c-339">Ilustración 32</span><span class="sxs-lookup"><span data-stu-id="a9b9c-339">Figure 32</span></span>  
    > `main.css` <span data-ttu-id="a9b9c-340">ha sido bloqueado</span><span class="sxs-lookup"><span data-stu-id="a9b9c-340">has been blocked</span></span>  
    > <span data-ttu-id="a9b9c-341">! [se ha bloqueado Main. CSS] [ImagesTutorialBlockedStyles]</span><span class="sxs-lookup"><span data-stu-id="a9b9c-341">![main.css has been blocked][ImagesTutorialBlockedStyles]</span></span>  

1.  <span data-ttu-id="a9b9c-342">Anule la selección de la casilla de verificación **Activar bloqueo de solicitud** .</span><span class="sxs-lookup"><span data-stu-id="a9b9c-342">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="a9b9c-343">Conclusión</span><span class="sxs-lookup"><span data-stu-id="a9b9c-343">Conclusion</span></span>  

<span data-ttu-id="a9b9c-344">Enhorabuena, ha completado el tutorial.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-344">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="a9b9c-345">Ahora ya sabe cómo usar el panel red en el DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-345">You now know how to use the Network panel in the Microsoft Edge DevTools!</span></span>






<span data-ttu-id="a9b9c-346">Consulte la [referencia de red][DevtoolsNetworkReference] para descubrir más características de DevTools relacionadas con la inspección de la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="a9b9c-346">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Ilustración 1: la demostración"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Console.msft.png "Ilustración 2: la consola"  
[ImagesTutorialDocked]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Console-Bottom.msft.png "Ilustración 3: DevTools acoplado a la parte inferior de la ventana"  
[ImagesTutorialNetwork]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Bottom.msft.png "Ilustración 4: DevTools acoplada a la parte inferior de la ventana"  
[ImagesTutorialLog]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network.msft.png "Figura 5: el registro de red"  
[ImagesTutorialRuntime]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-New-Resource.msft.png "Ilustración 6: un nuevo recurso en el registro de red"  
[ImagesTutorialDomain]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Edit-Column.msft.png "Ilustración 7: habilitar la columna dominio"  
[ImagesTutorialThrottling]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-throttling.msft.png "Ilustración 8: habilitar la limitación de peticiones"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-throttling-Slow-3G.msft.png "Ilustración 9: selección de 3G lento"  
[ImagesTutorialHardReload]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Empty-cache-and-Hard-Reset.msft.png "Figura 10: memoria caché vacía y recarga en disco"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-screenshots.msft.png "ilustración 11: capturas de pantallas de la carga de la página"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-screenshots-First.msft.png "Ilustración 12: la actividad de red que se estaba realizando durante la primera captura de pantalla"  
[ImagesTutorialHeaders]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-headers.msft.png "ilustración 13: la pestaña encabezados"  
[ImagesTutorialPreview]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Preview.msft.png "Ilustración 14: ficha vista previa"  
[ImagesTutorialResponse]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Response.msft.png "Ilustración 15: la pestaña respuesta"  
[ImagesTutorialTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Timing.msft.png "Ilustración 16: ficha intervalos"  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Close-Tabs.msft.png "Ilustración 17: botón Cerrar"  
[ImagesTutorialSearch]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-Empty.msft.png "ilustración 18: el panel de búsqueda"  
[ImagesTutorialResults]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-cache-control.msft.png "Ilustración 19: resultados de la búsqueda de control de caché"  
[ImagesTutorialCache]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-cache-control-headers-Response-headers.msft.png "figura 20: un resultado de búsqueda resaltado en la pestaña encabezados"  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Search-Close.msft.png "ilustración 21: los botones cerrar"  
[ImagesTutorialFilters]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Empty.msft.png "Ilustración 22: la barra de herramientas filtros"  
[ImagesTutorialPNG]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-PNG.msft.png "Ilustración 23: un filtro de cadena"  
[ImagesTutorialRegEx]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Regex.msft.png "Ilustración 24: un filtro de expresiones regulares"  
[ImagesTutorialNegative]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-negative-Statement.msft.png "Ilustración 25: un filtro negativo"  
[ImagesTutorialProperty]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Property-Value.msft.png "ilustración 26: un filtro de propiedad"  
[ImagesTutorialCSS]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-file-type-CSS.msft.png "Ilustración 27: mostrar solo archivos CSS"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-Filter-file-type-CSS-JS.msft.png "Ilustración 28: mostrar solo archivos CSS y JS"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Empty.msft.png "Ilustración 29: el menú de comandos"  
[ImagesTutorialBlock]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block.msft.png "figura 30: mostrar el bloqueo de solicitudes"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Add-pattern.msft.png "Ilustración 31: bloqueo de Main. css"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Main-CSS.msft.png "ilustración 32: Main. CSS se ha bloqueado"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Referencia de análisis de red"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Solicitudes de filtro-referencia de análisis de red"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Ocultar el panel de información general: referencia de análisis de red"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Solicitudes de filtro por propiedades-referencia de análisis de red"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspeccionar demostración actividad de red"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="a9b9c-388">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9b9c-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a9b9c-389">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a9b9c-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a9b9c-391">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9b9c-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
