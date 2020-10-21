---
description: Un tutorial sobre las características más populares relacionadas con la red en Microsoft Edge DevTools.
title: Inspeccionar la actividad de la red en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125429"
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

# <span data-ttu-id="e0380-104">Inspeccionar la actividad de la red en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e0380-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="e0380-105">Este es un tutorial práctico de algunas de las características de DevTools más usadas relacionadas con la inspección de la actividad de red de una página.</span><span class="sxs-lookup"><span data-stu-id="e0380-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="e0380-106">Consulte [referencia de red][DevtoolsNetworkReference] si desea examinar las características en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e0380-106">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="e0380-107">Cuándo usar el panel red</span><span class="sxs-lookup"><span data-stu-id="e0380-107">When to use the Network panel</span></span>  

<span data-ttu-id="e0380-108">En general, use el panel red cuando necesite asegurarse de que los recursos se van a descargar o cargar según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="e0380-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="e0380-109">Los casos de uso más comunes para el panel red son:</span><span class="sxs-lookup"><span data-stu-id="e0380-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="e0380-110">Asegurándote de que los recursos se carguen o descarguen realmente.</span><span class="sxs-lookup"><span data-stu-id="e0380-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="e0380-111">Inspeccione las propiedades de un recurso individual, como los encabezados HTTP, el contenido, el tamaño, etc.</span><span class="sxs-lookup"><span data-stu-id="e0380-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="e0380-112">Si está buscando formas de mejorar el rendimiento de la carga de páginas, **no** empiece por el panel red.</span><span class="sxs-lookup"><span data-stu-id="e0380-112">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="e0380-113">Hay muchos tipos de problemas de rendimiento de la carga que no están relacionados con la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="e0380-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="e0380-114">Comience con el panel auditorías porque le ofrece sugerencias específicas sobre cómo mejorar la página.</span><span class="sxs-lookup"><span data-stu-id="e0380-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="e0380-115">Consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="e0380-115">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="e0380-116">Abrir el panel de red</span><span class="sxs-lookup"><span data-stu-id="e0380-116">Open the Network panel</span></span>  

<span data-ttu-id="e0380-117">Para sacar el máximo provecho de este tutorial, abra la demostración y pruebe las características de la página de demostración.</span><span class="sxs-lookup"><span data-stu-id="e0380-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="e0380-118">Abra la [demostración introducción][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="e0380-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="e0380-120">La demostración</span><span class="sxs-lookup"><span data-stu-id="e0380-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="La demostración" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="e0380-121">[Abra DevTools][DevToolsOpen] presionando `Control` + `Shift` + `J` \ (Windows, Linux \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e0380-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="e0380-122">Se abre el panel de la **consola** .</span><span class="sxs-lookup"><span data-stu-id="e0380-122">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="e0380-124">La **consola**</span><span class="sxs-lookup"><span data-stu-id="e0380-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e0380-125">Es posible que prefiera [acoplar DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e0380-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="e0380-127">DevTools acoplado en la parte inferior de la ventana</span><span class="sxs-lookup"><span data-stu-id="e0380-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-128">Seleccione la pestaña **red** .  Se abre el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="e0380-128">Select the **Network** tab.  The **Network** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="e0380-130">Herramienta de **consola** en el DevTools acoplado en la parte inferior de la ventana</span><span class="sxs-lookup"><span data-stu-id="e0380-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e0380-131">Ahora el panel red está vacío.</span><span class="sxs-lookup"><span data-stu-id="e0380-131">Right now the Network panel is empty.</span></span>  <span data-ttu-id="e0380-132">DevTools solo registra la actividad de la red después de abrirla y no se ha producido ninguna actividad de red desde que abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="e0380-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="e0380-133">Registrar actividad de la red</span><span class="sxs-lookup"><span data-stu-id="e0380-133">Log network activity</span></span>  

<span data-ttu-id="e0380-134">Para ver la actividad de red que provoca una página:</span><span class="sxs-lookup"><span data-stu-id="e0380-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="e0380-135">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="e0380-135">Reload the page.</span></span>  <span data-ttu-id="e0380-136">El panel red registra toda la actividad de la red en el **registro de red**.</span><span class="sxs-lookup"><span data-stu-id="e0380-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="e0380-138">El **registro de red**</span><span class="sxs-lookup"><span data-stu-id="e0380-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e0380-139">Cada fila del **registro de red** representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="e0380-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="e0380-140">De forma predeterminada, los recursos se muestran cronológicamente.</span><span class="sxs-lookup"><span data-stu-id="e0380-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="e0380-141">El recurso superior suele ser el documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="e0380-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="e0380-142">El recurso inferior es el último que se solicitó.</span><span class="sxs-lookup"><span data-stu-id="e0380-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="e0380-143">Cada columna representa información acerca de un recurso.</span><span class="sxs-lookup"><span data-stu-id="e0380-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="e0380-144">En la ilustración anterior se muestran las columnas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="e0380-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="e0380-145">**Estado**.</span><span class="sxs-lookup"><span data-stu-id="e0380-145">**Status**.</span></span>  <span data-ttu-id="e0380-146">El código de Estado HTTP para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0380-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="e0380-147">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="e0380-147">**Type**.</span></span>  <span data-ttu-id="e0380-148">El tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e0380-148">The resource type.</span></span>  
    *   <span data-ttu-id="e0380-149">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="e0380-149">**Initiator**.</span></span>  <span data-ttu-id="e0380-150">La causa de la solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0380-150">The cause of the resource request.</span></span>  <span data-ttu-id="e0380-151">Al seleccionar un vínculo en la columna iniciador, se le lleva al código fuente que causó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0380-151">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="e0380-152">**Momento**.</span><span class="sxs-lookup"><span data-stu-id="e0380-152">**Time**.</span></span>  <span data-ttu-id="e0380-153">La duración de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0380-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="e0380-154">**Cascada**.</span><span class="sxs-lookup"><span data-stu-id="e0380-154">**Waterfall**.</span></span>  <span data-ttu-id="e0380-155">Una representación gráfica de las distintas etapas de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0380-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="e0380-156">Desplace el puntero sobre una cascada para ver un desglose.</span><span class="sxs-lookup"><span data-stu-id="e0380-156">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e0380-157">El gráfico que se encuentra sobre el registro de red se denomina Descripción general.</span><span class="sxs-lookup"><span data-stu-id="e0380-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="e0380-158">No usará el gráfico de información general en este tutorial, por lo que puede ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="e0380-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="e0380-159">Vea [ocultar el panel de información general][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="e0380-159">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="e0380-160">Después de abrir DevTools, registra la actividad de la red en el registro de red.</span><span class="sxs-lookup"><span data-stu-id="e0380-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="e0380-161">Para demostrarlo, primero mire la parte inferior del **registro de red** y tome nota mental de la última actividad.</span><span class="sxs-lookup"><span data-stu-id="e0380-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="e0380-162">Ahora, seleccione el botón **obtener datos** en la demostración.</span><span class="sxs-lookup"><span data-stu-id="e0380-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="e0380-163">Vuelva a mirar la parte inferior del **registro de red** .</span><span class="sxs-lookup"><span data-stu-id="e0380-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="e0380-164">Debería ver un nuevo recurso denominado `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="e0380-164">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="e0380-165">Si selecciona el botón **obtener datos** , la página solicitará este archivo.</span><span class="sxs-lookup"><span data-stu-id="e0380-165">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="e0380-167">Un nuevo recurso en el **registro de red**</span><span class="sxs-lookup"><span data-stu-id="e0380-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0380-168">Mostrar más información</span><span class="sxs-lookup"><span data-stu-id="e0380-168">Show more information</span></span>  

<span data-ttu-id="e0380-169">Las columnas del registro de red se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="e0380-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="e0380-170">Puede ocultar las columnas que no está usando.</span><span class="sxs-lookup"><span data-stu-id="e0380-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="e0380-171">También hay muchas columnas que están ocultas de forma predeterminada, que pueden resultarle útiles.</span><span class="sxs-lookup"><span data-stu-id="e0380-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="e0380-172">Haga clic con el botón derecho en el encabezado de la tabla registro de red y elija **dominio**.</span><span class="sxs-lookup"><span data-stu-id="e0380-172">Right-click the header of the Network Log table and choose **Domain**.</span></span>  <span data-ttu-id="e0380-173">Ahora se muestra el dominio de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="e0380-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="e0380-175">Habilitar la columna dominio</span><span class="sxs-lookup"><span data-stu-id="e0380-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e0380-176">Vea la dirección URL completa de un recurso colocando el puntero sobre la celda en la columna **nombre** .</span><span class="sxs-lookup"><span data-stu-id="e0380-176">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="e0380-177">Simular una conexión de red más lenta</span><span class="sxs-lookup"><span data-stu-id="e0380-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="e0380-178">Es probable que la conexión de red del equipo que use para crear sitios sea más rápida que las conexiones de red de los dispositivos móviles de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e0380-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="e0380-179">Al limitar la página, se obtiene una idea más extensa de cuánto tarda una página en cargarse en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="e0380-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="e0380-180">Seleccione la lista desplegable **límite** , que está establecida en **conectado** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e0380-180">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="e0380-182">Habilitar límite</span><span class="sxs-lookup"><span data-stu-id="e0380-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-183">Elige **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="e0380-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="e0380-185">Seleccionar 3G lento</span><span class="sxs-lookup"><span data-stu-id="e0380-185">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-186">Pulse volver a **cargar** \ ( ![ volver a cargar ][ImageRefreshIcon] \) y, a continuación, elija **vaciar caché y recargar de disco**.</span><span class="sxs-lookup"><span data-stu-id="e0380-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="e0380-188">Memoria caché vacía y recarga duro</span><span class="sxs-lookup"><span data-stu-id="e0380-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="e0380-189">En las visitas repetidas, el explorador generalmente sirve algunos archivos de la [caché][MDNHTTPCache], lo que acelera la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e0380-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="e0380-190">**Vaciar la memoria caché y la recarga de disco** obliga al explorador a dirigirse a la red para todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="e0380-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="e0380-191">Esto es útil cuando desea ver cómo experimenta un primer visitante la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e0380-191">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e0380-192">El flujo de trabajo **vacío y la recarga de disco duro** solo está disponible cuando DevTools está abierto.</span><span class="sxs-lookup"><span data-stu-id="e0380-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="e0380-193">Capturar capturas de pantallas</span><span class="sxs-lookup"><span data-stu-id="e0380-193">Capture screenshots</span></span>  

<span data-ttu-id="e0380-194">Las capturas de pantallas le permiten ver cómo se ha enviado una página a lo largo del tiempo mientras se cargaba.</span><span class="sxs-lookup"><span data-stu-id="e0380-194">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="e0380-195">Seleccione \ ( ![ configuración ][ImageSettingsIcon] de red \) y seleccione la casilla **capturar capturas de pantallas** .</span><span class="sxs-lookup"><span data-stu-id="e0380-195">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="e0380-196">Vuelva a cargar la página a través del flujo de trabajo **vacío y de recarga de disco** .</span><span class="sxs-lookup"><span data-stu-id="e0380-196">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="e0380-197">Consulte [simular una conexión más lenta](#simulate-a-slower-network-connection) si necesita un aviso sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e0380-197">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="e0380-198">El panel capturas de pantallas proporciona miniaturas de la apariencia de la página en varios puntos durante el proceso de carga.</span><span class="sxs-lookup"><span data-stu-id="e0380-198">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="e0380-200">Capturas de pantallas de la carga de la página</span><span class="sxs-lookup"><span data-stu-id="e0380-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-201">Seleccionar la primera miniatura.</span><span class="sxs-lookup"><span data-stu-id="e0380-201">Select the first thumbnail.</span></span>  <span data-ttu-id="e0380-202">DevTools muestra qué actividad de la red tuvo lugar en ese momento.</span><span class="sxs-lookup"><span data-stu-id="e0380-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="e0380-204">La actividad de red que se produjo durante la primera captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="e0380-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-205">Seleccione \ ( ![ configuración de red ][ImageSettingsIcon] \) de nuevo y anule la selección de la casilla de verificación **capturar capturas** de pantallas para cerrar el panel capturas de pantallas.</span><span class="sxs-lookup"><span data-stu-id="e0380-205">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="e0380-206">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="e0380-206">Reload the page again.</span></span>  
    
## <span data-ttu-id="e0380-207">Inspeccionar los detalles del recurso</span><span class="sxs-lookup"><span data-stu-id="e0380-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="e0380-208">Seleccione un recurso para obtener más información sobre él.</span><span class="sxs-lookup"><span data-stu-id="e0380-208">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="e0380-209">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="e0380-209">Try it now:</span></span>  

1.  <span data-ttu-id="e0380-210">Seleccione `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="e0380-210">Select `getstarted.html`.</span></span>  <span data-ttu-id="e0380-211">Se muestra la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="e0380-211">The **Headers** tab is shown.</span></span>  <span data-ttu-id="e0380-212">Use esta pestaña para inspeccionar los encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0380-212">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="e0380-214">La pestaña **encabezados**</span><span class="sxs-lookup"><span data-stu-id="e0380-214">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-215">Seleccione la pestaña **vista previa** .  Se muestra una representación básica del HTML.</span><span class="sxs-lookup"><span data-stu-id="e0380-215">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="e0380-217">La ficha **vista previa**</span><span class="sxs-lookup"><span data-stu-id="e0380-217">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e0380-218">Esta pestaña es útil cuando una API devuelve un código de error en HTML.</span><span class="sxs-lookup"><span data-stu-id="e0380-218">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="e0380-219">Es posible que le resulte más fácil leer el código HTML representado que el código fuente HTML o cuando Inspeccione imágenes.</span><span class="sxs-lookup"><span data-stu-id="e0380-219">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="e0380-220">Seleccione la pestaña **respuesta** .  Se muestra el código fuente HTML.</span><span class="sxs-lookup"><span data-stu-id="e0380-220">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="e0380-222">La ficha **respuesta**</span><span class="sxs-lookup"><span data-stu-id="e0380-222">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e0380-223">Cuando se minified un archivo, al seleccionar el botón **formato** \ ( ![ formato ][ImageFormatIcon] \) en la parte inferior de la pestaña **respuesta** , se cambia el formato del contenido para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e0380-223">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="e0380-224">Seleccione la pestaña **intervalos** .  Se muestra un desglose de la actividad de red de este recurso.</span><span class="sxs-lookup"><span data-stu-id="e0380-224">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="e0380-226">La ficha **intervalos**</span><span class="sxs-lookup"><span data-stu-id="e0380-226">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-227">Elija **cerrar** \ ( ![ cerrar ][ImageCloseIcon] \) para volver a ver el registro de red.</span><span class="sxs-lookup"><span data-stu-id="e0380-227">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="e0380-229">Botón **cerrar**</span><span class="sxs-lookup"><span data-stu-id="e0380-229">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0380-230">Buscar encabezados y respuestas de red</span><span class="sxs-lookup"><span data-stu-id="e0380-230">Search network headers and responses</span></span>  

<span data-ttu-id="e0380-231">Use el panel de **búsqueda** cuando necesite buscar en los encabezados y las respuestas http de todos los recursos para una cadena determinada o una expresión normal.</span><span class="sxs-lookup"><span data-stu-id="e0380-231">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="e0380-232">Por ejemplo, supongamos que desea comprobar que los recursos usan **directivas de caché**razonables.</span><span class="sxs-lookup"><span data-stu-id="e0380-232">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="e0380-233">Elija **Buscar** \ ( ![ Buscar ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e0380-233">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="e0380-234">El panel de búsqueda se abre a la izquierda del registro de red.</span><span class="sxs-lookup"><span data-stu-id="e0380-234">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="e0380-236">El panel de **búsqueda**</span><span class="sxs-lookup"><span data-stu-id="e0380-236">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-237">Escriba `Cache-Control` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e0380-237">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="e0380-238">El panel de búsqueda muestra todas las instancias de las `Cache-Control` que encuentra en los encabezados de recursos o en el contenido.</span><span class="sxs-lookup"><span data-stu-id="e0380-238">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="e0380-240">Resultados de búsqueda de </span><span class="sxs-lookup"><span data-stu-id="e0380-240">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-241">Seleccione un resultado para ver el recurso en el que se encontró el resultado.</span><span class="sxs-lookup"><span data-stu-id="e0380-241">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="e0380-242">Si está viendo los detalles del recurso, seleccione un resultado para ir directamente a él.</span><span class="sxs-lookup"><span data-stu-id="e0380-242">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="e0380-243">Por ejemplo, si la consulta se encuentra en un encabezado, se abre la pestaña encabezados.</span><span class="sxs-lookup"><span data-stu-id="e0380-243">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="e0380-244">Si la consulta se encuentra en el contenido, se abre la pestaña **respuesta** .</span><span class="sxs-lookup"><span data-stu-id="e0380-244">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="e0380-246">Un resultado de búsqueda resaltado en la pestaña **encabezados**</span><span class="sxs-lookup"><span data-stu-id="e0380-246">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-247">Cierre el panel de búsqueda y la pestaña encabezados.</span><span class="sxs-lookup"><span data-stu-id="e0380-247">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="e0380-249">Los botones **cerrar**</span><span class="sxs-lookup"><span data-stu-id="e0380-249">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e0380-250">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="e0380-250">Filter resources</span></span>  

<span data-ttu-id="e0380-251">DevTools proporciona numerosos flujos de trabajo para filtrar recursos que no son relevantes para la tarea que está realizando.</span><span class="sxs-lookup"><span data-stu-id="e0380-251">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="e0380-253">La barra de herramientas **filtros**</span><span class="sxs-lookup"><span data-stu-id="e0380-253">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="e0380-254">La barra de herramientas **filtros** debería estar habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e0380-254">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="e0380-255">De lo contrario:</span><span class="sxs-lookup"><span data-stu-id="e0380-255">If not:</span></span>  

1.  <span data-ttu-id="e0380-256">Elija **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="e0380-256">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="e0380-257">Filtrar por cadena, expresión regular o propiedad</span><span class="sxs-lookup"><span data-stu-id="e0380-257">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="e0380-258">El cuadro de texto **filtro** admite muchos tipos de filtrado diferentes.</span><span class="sxs-lookup"><span data-stu-id="e0380-258">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="e0380-259">Escriba `png` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="e0380-259">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="e0380-260">Solo se muestran los archivos que contienen el texto `png` .</span><span class="sxs-lookup"><span data-stu-id="e0380-260">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="e0380-261">En este caso, los únicos archivos que coinciden con el filtro son las imágenes PNG.</span><span class="sxs-lookup"><span data-stu-id="e0380-261">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="e0380-263">Un filtro de cadena</span><span class="sxs-lookup"><span data-stu-id="e0380-263">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-264">Escribe `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="e0380-264">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="e0380-265">DevTools filtra cualquier recurso con un nombre de archivo que no termina con un `j` o a `c` , seguido de 1 o más `s` caracteres.</span><span class="sxs-lookup"><span data-stu-id="e0380-265">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="e0380-267">Filtro de expresión regular</span><span class="sxs-lookup"><span data-stu-id="e0380-267">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-268">Escribe `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="e0380-268">Type `-main.css`.</span></span>  <span data-ttu-id="e0380-269">DevTools filtra `main.css` .</span><span class="sxs-lookup"><span data-stu-id="e0380-269">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="e0380-270">Si cualquier otro archivo coincide con el patrón, también se filtrarían.</span><span class="sxs-lookup"><span data-stu-id="e0380-270">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="e0380-272">Un filtro negativo</span><span class="sxs-lookup"><span data-stu-id="e0380-272">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-273">Escriba `domain:cdn.glitch.com` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="e0380-273">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="e0380-274">DevTools filtra cualquier recurso con una dirección URL que no coincida con este dominio.</span><span class="sxs-lookup"><span data-stu-id="e0380-274">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="e0380-276">Un filtro de propiedad</span><span class="sxs-lookup"><span data-stu-id="e0380-276">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e0380-277">Vea [filtrar solicitudes por propiedades][DevtoolsReferenceProperty] para obtener una lista completa de las propiedades que se pueden filtrar.</span><span class="sxs-lookup"><span data-stu-id="e0380-277">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="e0380-278">Borre el cuadro de texto de **filtro** de cualquier texto.</span><span class="sxs-lookup"><span data-stu-id="e0380-278">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="e0380-279">Filtrar por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="e0380-279">Filter by resource type</span></span>  

<span data-ttu-id="e0380-280">Para centrarse en un determinado tipo de archivo, como las hojas de estilos:</span><span class="sxs-lookup"><span data-stu-id="e0380-280">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="e0380-281">Elija **CSS**.</span><span class="sxs-lookup"><span data-stu-id="e0380-281">Choose **CSS**.</span></span>  <span data-ttu-id="e0380-282">Se filtran todos los demás tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e0380-282">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="e0380-284">Mostrar solo archivos CSS</span><span class="sxs-lookup"><span data-stu-id="e0380-284">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-285">Para ver también las secuencias de comandos, mantenga `Control` \ (Windows, Linux \) o `Command` \ (MacOS \) y, a continuación, elija **JS**.</span><span class="sxs-lookup"><span data-stu-id="e0380-285">To also see scripts, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="e0380-287">Mostrar solo archivos CSS y JS</span><span class="sxs-lookup"><span data-stu-id="e0380-287">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-288">Seleccione **todo** para quitar los filtros y volver a ver todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="e0380-288">Choose **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="e0380-289">Consulte [filtrar solicitudes][DevtoolsNetworkReferenceFilter] para otros flujos de trabajo de filtrado.</span><span class="sxs-lookup"><span data-stu-id="e0380-289">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="e0380-290">Solicitudes de bloqueo</span><span class="sxs-lookup"><span data-stu-id="e0380-290">Block requests</span></span>  

<span data-ttu-id="e0380-291">¿Cómo se ve y se comporta una página cuando algunos de los recursos de la página no están disponibles?</span><span class="sxs-lookup"><span data-stu-id="e0380-291">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="e0380-292">¿Se produce un error completamente o aún es funcional?</span><span class="sxs-lookup"><span data-stu-id="e0380-292">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="e0380-293">Bloquear solicitudes para averiguar:</span><span class="sxs-lookup"><span data-stu-id="e0380-293">Block requests to find out:</span></span>  

1.  <span data-ttu-id="e0380-294">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="e0380-294">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="e0380-296">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="e0380-296">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-297">Escriba `block` , elija **Mostrar bloqueo de solicitud**y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e0380-297">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="e0380-299">Mostrar bloqueo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0380-299">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-300">Elija **Agregar patrón** \ ( ![ Agregar patrón ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e0380-300">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="e0380-301">Escribe `main.css`.</span><span class="sxs-lookup"><span data-stu-id="e0380-301">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="e0380-303">Bugs</span><span class="sxs-lookup"><span data-stu-id="e0380-303">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-304">Elija **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="e0380-304">Choose **Add**.</span></span>  
1.  <span data-ttu-id="e0380-305">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="e0380-305">Reload the page.</span></span>  <span data-ttu-id="e0380-306">Como se espera, el estilo de la página está ligeramente desordenado porque la hoja de estilos principal ha sido bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e0380-306">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e0380-307">La `main.css` fila en el registro de red.</span><span class="sxs-lookup"><span data-stu-id="e0380-307">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="e0380-308">El texto en rojo significa que el recurso se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e0380-308">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="e0380-310">ha sido bloqueado</span><span class="sxs-lookup"><span data-stu-id="e0380-310">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e0380-311">Anule la selección de la casilla de verificación **Activar bloqueo de solicitud** .</span><span class="sxs-lookup"><span data-stu-id="e0380-311">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="e0380-312">Conclusión</span><span class="sxs-lookup"><span data-stu-id="e0380-312">Conclusion</span></span>  

<span data-ttu-id="e0380-313">Enhorabuena, ha completado el tutorial.</span><span class="sxs-lookup"><span data-stu-id="e0380-313">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="e0380-314">Ahora ya sabe cómo usar el panel **red** en el DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e0380-314">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="e0380-315">Vaya a la [referencia de red][DevtoolsNetworkReference] para descubrir más características de DevTools relacionadas con la inspección de la actividad de la red.</span><span class="sxs-lookup"><span data-stu-id="e0380-315">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <span data-ttu-id="e0380-316">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e0380-316">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de DevTools de Microsoft Edge | Microsoft docs"  
[DevtoolsNetworkReference]: ./reference.md "Referencia de análisis de red | Microsoft docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Solicitudes de filtro: referencia de análisis de red | Microsoft docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar el panel de información general: referencia de análisis de red | Microsoft docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitudes por propiedades-referencia de análisis de red | Microsoft docs"
[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools | Microsoft docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Comprobar actividad de la red demo | Intento"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché de HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="e0380-326">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e0380-326">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e0380-327">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e0380-327">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e0380-329">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e0380-329">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
