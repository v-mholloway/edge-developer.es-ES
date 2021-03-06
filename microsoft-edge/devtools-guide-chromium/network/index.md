---
description: Tutorial sobre las características más populares relacionadas con la red en Microsoft Edge DevTools.
title: Inspeccionar la actividad de red en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 16b60716c91d2f4ce778f1fac37afc0e73e30ab6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398661"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a><span data-ttu-id="e11dc-104">Inspeccionar la actividad de red en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e11dc-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="e11dc-105">Este es un tutorial práctica de algunas de las características de DevTools más usadas relacionadas con la inspección de la actividad de red de una página.</span><span class="sxs-lookup"><span data-stu-id="e11dc-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="e11dc-106">Si desea examinar las características, vaya a [Referencia de red][DevtoolsNetworkReference].</span><span class="sxs-lookup"><span data-stu-id="e11dc-106">If you want to browse features, navigate to [Network Reference][DevtoolsNetworkReference].</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a><span data-ttu-id="e11dc-107">Cuándo usar el panel Red</span><span class="sxs-lookup"><span data-stu-id="e11dc-107">When to use the Network panel</span></span>  

<span data-ttu-id="e11dc-108">En general, use el panel Red cuando necesite asegurarse de que los recursos se descargan o cargan según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="e11dc-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="e11dc-109">Los casos de uso más comunes para el panel Red son:</span><span class="sxs-lookup"><span data-stu-id="e11dc-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="e11dc-110">Asegurarse de que los recursos se cargan o descargan realmente.</span><span class="sxs-lookup"><span data-stu-id="e11dc-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="e11dc-111">Inspeccionar las propiedades de un recurso individual, como los encabezados HTTP, el contenido, el tamaño, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="e11dc-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="e11dc-112">Si está buscando formas de mejorar el rendimiento de carga de página, **no empiece** con la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-112">If you are looking for ways to improve page load performance, **do not** start with the **Network** tool.</span></span>  <span data-ttu-id="e11dc-113">Hay muchos tipos de problemas de rendimiento de carga que no están relacionados con la actividad de red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="e11dc-114">Comience con el panel Auditorías porque le ofrece sugerencias dirigidas sobre cómo mejorar la página.</span><span class="sxs-lookup"><span data-stu-id="e11dc-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="e11dc-115">Vaya a [Optimizar velocidad del sitio web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="e11dc-115">Navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <a name="open-the-network-panel"></a><span data-ttu-id="e11dc-116">Abrir el panel Red</span><span class="sxs-lookup"><span data-stu-id="e11dc-116">Open the Network panel</span></span>  

<span data-ttu-id="e11dc-117">Para sacar el máximo partido a este tutorial, abra la demostración y pruebe las características de la página de demostración.</span><span class="sxs-lookup"><span data-stu-id="e11dc-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="e11dc-118">Abra la [Demostración de introducción][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="e11dc-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="La demostración" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="e11dc-120">La demostración</span><span class="sxs-lookup"><span data-stu-id="e11dc-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="e11dc-121">Para [abrir DevTools,][DevToolsOpen]seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e11dc-121">To [Open DevTools][DevToolsOpen], select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="e11dc-122">Se **abre la herramienta** Consola.</span><span class="sxs-lookup"><span data-stu-id="e11dc-122">The **Console** tool opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="La consola" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="e11dc-124">La **consola**</span><span class="sxs-lookup"><span data-stu-id="e11dc-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e11dc-125">Es posible que prefiera [acoplar DevTools a la parte inferior de la ventana][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e11dc-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools acoplada a la parte inferior de la ventana" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="e11dc-127">DevTools acoplada a la parte inferior de la ventana</span><span class="sxs-lookup"><span data-stu-id="e11dc-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-128">Abra la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-128">Open the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Herramienta de consola en DevTools acoplada a la parte inferior de la ventana" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="e11dc-130">**Herramienta** de consola en DevTools acoplada a la parte inferior de la ventana</span><span class="sxs-lookup"><span data-stu-id="e11dc-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e11dc-131">En este momento, **la herramienta Red** está vacía.</span><span class="sxs-lookup"><span data-stu-id="e11dc-131">Right now the **Network** tool is empty.</span></span>  <span data-ttu-id="e11dc-132">DevTools solo registra la actividad de red después de abrirlo y no se ha producido ninguna actividad de red desde que abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="e11dc-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <a name="log-network-activity"></a><span data-ttu-id="e11dc-133">Registrar actividad de red</span><span class="sxs-lookup"><span data-stu-id="e11dc-133">Log network activity</span></span>  

<span data-ttu-id="e11dc-134">Para ver la actividad de red que provoca una página:</span><span class="sxs-lookup"><span data-stu-id="e11dc-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="e11dc-135">Actualice la página web.</span><span class="sxs-lookup"><span data-stu-id="e11dc-135">Refresh the webpage.</span></span>  <span data-ttu-id="e11dc-136">El panel Red registra toda la actividad de red en el **registro de red**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="El registro de red" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="e11dc-138">El **registro de red**</span><span class="sxs-lookup"><span data-stu-id="e11dc-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e11dc-139">Cada fila del registro **de red** representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="e11dc-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="e11dc-140">De forma predeterminada, los recursos se enumeran cronológicamente.</span><span class="sxs-lookup"><span data-stu-id="e11dc-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="e11dc-141">El recurso superior suele ser el documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="e11dc-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="e11dc-142">El recurso inferior es lo que se solicitó por última vez.</span><span class="sxs-lookup"><span data-stu-id="e11dc-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="e11dc-143">Cada columna representa información sobre un recurso.</span><span class="sxs-lookup"><span data-stu-id="e11dc-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="e11dc-144">En la figura anterior se muestran las columnas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="e11dc-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="e11dc-145">**Estado**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-145">**Status**.</span></span>  <span data-ttu-id="e11dc-146">El código de estado HTTP para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e11dc-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="e11dc-147">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-147">**Type**.</span></span>  <span data-ttu-id="e11dc-148">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e11dc-148">The resource type.</span></span>  
    *   <span data-ttu-id="e11dc-149">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-149">**Initiator**.</span></span>  <span data-ttu-id="e11dc-150">La causa de la solicitud de recurso.</span><span class="sxs-lookup"><span data-stu-id="e11dc-150">The cause of the resource request.</span></span>  <span data-ttu-id="e11dc-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span><span class="sxs-lookup"><span data-stu-id="e11dc-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="e11dc-152">**Hora**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-152">**Time**.</span></span>  <span data-ttu-id="e11dc-153">Duración de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e11dc-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="e11dc-154">**Cascada**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-154">**Waterfall**.</span></span>  <span data-ttu-id="e11dc-155">Representación gráfica de las distintas fases de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e11dc-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="e11dc-156">Para mostrar un desglose, mantenga el mouse en una cascada.</span><span class="sxs-lookup"><span data-stu-id="e11dc-156">To display a breakdown, hover on a Waterfall.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e11dc-157">El gráfico que se encuentra encima del registro de red se denomina Información general.</span><span class="sxs-lookup"><span data-stu-id="e11dc-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="e11dc-158">No usará el gráfico Información general en este tutorial, por lo que puede ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="e11dc-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="e11dc-159">Vaya a [Ocultar el panel Información general][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="e11dc-159">Navigate to [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="e11dc-160">Después de abrir DevTools, registra la actividad de red en el registro de red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="e11dc-161">Para demostrar esto, primero mire la parte inferior **del** registro de red y tome nota mental de la última actividad.</span><span class="sxs-lookup"><span data-stu-id="e11dc-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="e11dc-162">Ahora, seleccione el **botón Obtener datos** en la demostración.</span><span class="sxs-lookup"><span data-stu-id="e11dc-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="e11dc-163">Vuelva a mirar la parte inferior del **registro de** red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="e11dc-164">Se muestra un nuevo `getstarted.json` recurso denominado.</span><span class="sxs-lookup"><span data-stu-id="e11dc-164">A new resource named `getstarted.json` is displayed.</span></span>  <span data-ttu-id="e11dc-165">Para hacer que la página web solicite el archivo, elija el **botón Obtener** datos.</span><span class="sxs-lookup"><span data-stu-id="e11dc-165">To cause the webpage to request the file, choose the **Get Data** button.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Un nuevo recurso en el registro de red" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="e11dc-167">Un nuevo recurso en el registro **de red**</span><span class="sxs-lookup"><span data-stu-id="e11dc-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <a name="show-more-information"></a><span data-ttu-id="e11dc-168">Mostrar más información</span><span class="sxs-lookup"><span data-stu-id="e11dc-168">Show more information</span></span>  

<span data-ttu-id="e11dc-169">Las columnas del registro de red se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="e11dc-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="e11dc-170">Puede ocultar columnas que no está usando.</span><span class="sxs-lookup"><span data-stu-id="e11dc-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="e11dc-171">También hay muchas columnas ocultas de forma predeterminada que puede resultar útil.</span><span class="sxs-lookup"><span data-stu-id="e11dc-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="e11dc-172">Mantenga el mouse en el encabezado de la tabla Registro de red, abra el menú contextual \(haga clic con el botón secundario\) y elija **Dominio**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-172">Hover on the header of the Network Log table, open the contextual menu \(right-click\), and choose **Domain**.</span></span>  <span data-ttu-id="e11dc-173">Ahora se muestra el dominio de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="e11dc-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Habilitar la columna Dominio" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="e11dc-175">Habilitar la columna Dominio</span><span class="sxs-lookup"><span data-stu-id="e11dc-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e11dc-176">Para revisar la dirección URL completa de un recurso, mantenga el mouse en la celda de la **columna** Nombre.</span><span class="sxs-lookup"><span data-stu-id="e11dc-176">To review the full URL of a resource, hover on the cell in the **Name** column.</span></span>  
    
## <a name="simulate-a-slower-network-connection"></a><span data-ttu-id="e11dc-177">Simular una conexión de red más lenta</span><span class="sxs-lookup"><span data-stu-id="e11dc-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="e11dc-178">La conexión de red del equipo que usa para crear sitios es probablemente más rápida que las conexiones de red de los dispositivos móviles de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e11dc-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="e11dc-179">Al limitación de la página, obtienes una mejor idea del tiempo que tarda una página en cargarse en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="e11dc-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="e11dc-180">Elija el **desplegable Limitación,** que se establece en **Línea de** forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e11dc-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Habilitar la limitación" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="e11dc-182">Habilitar la limitación</span><span class="sxs-lookup"><span data-stu-id="e11dc-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-183">Elija **Lento 3G**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Elija Lento 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="e11dc-185">Elija Lento 3G</span><span class="sxs-lookup"><span data-stu-id="e11dc-185">Choose Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-186">Presione durante mucho **tiempo Reload** \( ![ Reload \) y, a ][ImageRefreshIcon] continuación, elija **Empty Cache and Hard Reload**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Caché vacía y recarga dura" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="e11dc-188">Caché vacía y recarga dura</span><span class="sxs-lookup"><span data-stu-id="e11dc-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="e11dc-189">En las visitas repetidas, el explorador normalmente sirve algunos archivos de la [memoria caché,][MDNHTTPCache]lo que acelera la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="e11dc-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="e11dc-190">**La caché vacía y la recarga dura** fuerzan al explorador a ir a la red para todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="e11dc-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="e11dc-191">Úselo para mostrar cómo un visitante por primera vez experimenta una carga de página.</span><span class="sxs-lookup"><span data-stu-id="e11dc-191">Use it to display how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e11dc-192">El **flujo de trabajo Caché vacía y Recarga** dura solo está disponible cuando DevTools está abierto.</span><span class="sxs-lookup"><span data-stu-id="e11dc-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <a name="capture-screenshots"></a><span data-ttu-id="e11dc-193">Capturar capturas de pantalla</span><span class="sxs-lookup"><span data-stu-id="e11dc-193">Capture screenshots</span></span>  

<span data-ttu-id="e11dc-194">Las capturas de pantalla muestran cómo se ve una página web con el tiempo mientras se carga.</span><span class="sxs-lookup"><span data-stu-id="e11dc-194">Screenshots display how a webpage looks over time while it loads.</span></span>  

1.  <span data-ttu-id="e11dc-195">Elija \( ![ Configuración de red ][ImageSettingsIcon] \) y active la casilla Capturar **capturas de** pantalla.</span><span class="sxs-lookup"><span data-stu-id="e11dc-195">Choose \(![Network settings][ImageSettingsIcon]\) and turn on the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="e11dc-196">Actualice la página de nuevo con el **flujo de trabajo Caché vacía y Recarga dura.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-196">Refresh the page again using the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="e11dc-197">Navegue hasta [Simular una conexión más lenta](#simulate-a-slower-network-connection) si necesita un aviso sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e11dc-197">Navigate to [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="e11dc-198">El panel Capturas de pantalla proporciona miniaturas del aspecto de la página en varios puntos durante el proceso de carga.</span><span class="sxs-lookup"><span data-stu-id="e11dc-198">The Screenshots panel provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Capturas de pantalla de la carga de página" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="e11dc-200">Capturas de pantalla de la carga de página</span><span class="sxs-lookup"><span data-stu-id="e11dc-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-201">Elija la primera miniatura.</span><span class="sxs-lookup"><span data-stu-id="e11dc-201">Choose the first thumbnail.</span></span>  <span data-ttu-id="e11dc-202">DevTools muestra qué actividad de red se estaba produciendo en ese momento.</span><span class="sxs-lookup"><span data-stu-id="e11dc-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="La actividad de red que se estaba produciendo durante la primera captura de pantalla" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="e11dc-204">La actividad de red que se estaba produciendo durante la primera captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="e11dc-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-205">Vuelva a elegir \( Configuración de red \) y desactive la casilla Capturar capturas de pantalla ![ para cerrar el panel Capturas de ][ImageSettingsIcon] pantalla. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e11dc-205">Choose \(![Network settings][ImageSettingsIcon]\) again and turn off the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="e11dc-206">Actualice la página de nuevo.</span><span class="sxs-lookup"><span data-stu-id="e11dc-206">Refresh the page again.</span></span>  
    
## <a name="inspect-the-details-of-the-resource"></a><span data-ttu-id="e11dc-207">Inspeccionar los detalles del recurso</span><span class="sxs-lookup"><span data-stu-id="e11dc-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="e11dc-208">Elija un recurso para obtener más información sobre él.</span><span class="sxs-lookup"><span data-stu-id="e11dc-208">Choose a resource to learn more information about it.</span></span>  <span data-ttu-id="e11dc-209">Pruébalo ahora:</span><span class="sxs-lookup"><span data-stu-id="e11dc-209">Try it now:</span></span>  

1.  <span data-ttu-id="e11dc-210">Elija `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="e11dc-210">Choose `getstarted.html`.</span></span>  <span data-ttu-id="e11dc-211">Se **muestra** el panel Encabezados.</span><span class="sxs-lookup"><span data-stu-id="e11dc-211">The **Headers** panel is shown.</span></span>  <span data-ttu-id="e11dc-212">Use este panel para inspeccionar los encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="e11dc-212">Use this panel to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Panel Encabezados" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="e11dc-214">Panel **Encabezados**</span><span class="sxs-lookup"><span data-stu-id="e11dc-214">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-215">Elija el panel **Vista** previa.</span><span class="sxs-lookup"><span data-stu-id="e11dc-215">Choose the **Preview** panel.</span></span>  <span data-ttu-id="e11dc-216">Se muestra una representación básica del HTML.</span><span class="sxs-lookup"><span data-stu-id="e11dc-216">A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="El panel Vista previa" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="e11dc-218">El panel **Vista** previa</span><span class="sxs-lookup"><span data-stu-id="e11dc-218">The **Preview** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e11dc-219">El panel es útil cuando una API devuelve un código de error en HTML.</span><span class="sxs-lookup"><span data-stu-id="e11dc-219">The panel is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="e11dc-220">Es posible que le resulte más fácil leer el HTML representado que el código fuente HTML, o al inspeccionar imágenes.</span><span class="sxs-lookup"><span data-stu-id="e11dc-220">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="e11dc-221">Elija **el** panel Respuesta.</span><span class="sxs-lookup"><span data-stu-id="e11dc-221">Choose the **Response** panel.</span></span>  <span data-ttu-id="e11dc-222">Se muestra el código fuente HTML.</span><span class="sxs-lookup"><span data-stu-id="e11dc-222">The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="El panel Respuesta" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="e11dc-224">El panel **Respuesta**</span><span class="sxs-lookup"><span data-stu-id="e11dc-224">The **Response** panel</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e11dc-225">Cuando se minifica un archivo, elija el botón **Formato** \( Formato \) situado en la parte inferior del panel Respuesta para volver a aplicar formato al contenido del archivo para que sea ![ ][ImageFormatIcon] legible. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e11dc-225">When a file is minified, choose the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** panel to re-format the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="e11dc-226">Elija \*\*\*\* el panel Temporización.</span><span class="sxs-lookup"><span data-stu-id="e11dc-226">Choose the **Timing** panel.</span></span>  <span data-ttu-id="e11dc-227">Se muestra un desglose de la actividad de red del recurso.</span><span class="sxs-lookup"><span data-stu-id="e11dc-227">A breakdown of the network activity for the resource is displayed.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="El panel Temporización" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="e11dc-229">El panel **Temporización**</span><span class="sxs-lookup"><span data-stu-id="e11dc-229">The **Timing** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-230">Elija **Cerrar** \( ![ Cerrar ][ImageCloseIcon] \) para volver a ver el registro de red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-230">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="El botón Cerrar" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="e11dc-232">El **botón** Cerrar</span><span class="sxs-lookup"><span data-stu-id="e11dc-232">The **Close** button</span></span>  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a><span data-ttu-id="e11dc-233">Buscar respuestas y encabezados de red</span><span class="sxs-lookup"><span data-stu-id="e11dc-233">Search network headers and responses</span></span>  

<span data-ttu-id="e11dc-234">Use el **panel** Búsqueda cuando necesite buscar en los encabezados HTTP y las respuestas de todos los recursos una determinada cadena o expresión regular.</span><span class="sxs-lookup"><span data-stu-id="e11dc-234">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="e11dc-235">Por ejemplo, supongamos que desea comprobar que los recursos usan directivas de **caché razonables.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-235">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="e11dc-236">Elija **Buscar** \( ![ Buscar ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e11dc-236">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="e11dc-237">El panel Búsqueda se abre a la izquierda del registro de red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-237">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Panel de búsqueda" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="e11dc-239">Panel **de** búsqueda</span><span class="sxs-lookup"><span data-stu-id="e11dc-239">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-240">Escriba `Cache-Control` y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e11dc-240">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="e11dc-241">El panel Búsqueda enumera todas las instancias que encuentra `Cache-Control` en los encabezados de recursos o el contenido.</span><span class="sxs-lookup"><span data-stu-id="e11dc-241">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Resultados de búsqueda para Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="e11dc-243">Resultados de búsqueda de </span><span class="sxs-lookup"><span data-stu-id="e11dc-243">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-244">Elija un resultado para ver el recurso en el que se encontró el resultado.</span><span class="sxs-lookup"><span data-stu-id="e11dc-244">Choose a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="e11dc-245">Si está viendo los detalles del recurso, seleccione un resultado para ir directamente a él.</span><span class="sxs-lookup"><span data-stu-id="e11dc-245">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="e11dc-246">Por ejemplo, si la consulta se encontró en un encabezado, se abrirá el panel **Encabezados.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-246">For example, if the query was found in a header, the **Headers** panel opens.</span></span>   <span data-ttu-id="e11dc-247">Si la consulta se encontró en el contenido, se **abrirá el** panel Respuesta.</span><span class="sxs-lookup"><span data-stu-id="e11dc-247">If the query was found in content, the **Response** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Un resultado de búsqueda resaltado en el panel Encabezados" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="e11dc-249">Un resultado de búsqueda resaltado en el panel **Encabezados**</span><span class="sxs-lookup"><span data-stu-id="e11dc-249">A search result highlighted in the **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-250">Cierre el panel Búsqueda y el panel **Encabezados.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-250">Close the Search pane and the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Los botones Cerrar" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="e11dc-252">Los **botones Cerrar**</span><span class="sxs-lookup"><span data-stu-id="e11dc-252">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <a name="filter-resources"></a><span data-ttu-id="e11dc-253">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="e11dc-253">Filter resources</span></span>  

<span data-ttu-id="e11dc-254">DevTools proporciona numerosos flujos de trabajo para filtrar recursos que no son relevantes para la tarea en cuestión.</span><span class="sxs-lookup"><span data-stu-id="e11dc-254">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="La barra de herramientas Filtros" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="e11dc-256">La **barra de herramientas Filtros**</span><span class="sxs-lookup"><span data-stu-id="e11dc-256">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="e11dc-257">La **barra de** herramientas Filtros debe estar activada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e11dc-257">The **Filters** toolbar should be turned on by default.</span></span>  <span data-ttu-id="e11dc-258">Si no es así:</span><span class="sxs-lookup"><span data-stu-id="e11dc-258">If not:</span></span>  

1.  <span data-ttu-id="e11dc-259">Elija **Filter** \( ![ Filter ][ImageFilterIcon] \) para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="e11dc-259">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <a name="filter-by-string-regular-expression-or-property"></a><span data-ttu-id="e11dc-260">Filtrar por cadena, expresión regular o propiedad</span><span class="sxs-lookup"><span data-stu-id="e11dc-260">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="e11dc-261">El **cuadro de** texto Filtrar admite muchos tipos diferentes de filtrado.</span><span class="sxs-lookup"><span data-stu-id="e11dc-261">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="e11dc-262">Escriba `png` en el cuadro **de** texto Filtrar.</span><span class="sxs-lookup"><span data-stu-id="e11dc-262">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="e11dc-263">Solo se muestran los archivos que contienen `png` el texto.</span><span class="sxs-lookup"><span data-stu-id="e11dc-263">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="e11dc-264">En este caso, los únicos archivos que coinciden con el filtro son las imágenes PNG.</span><span class="sxs-lookup"><span data-stu-id="e11dc-264">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Un filtro de cadena" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="e11dc-266">Un filtro de cadena</span><span class="sxs-lookup"><span data-stu-id="e11dc-266">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-267">Escribe `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="e11dc-267">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="e11dc-268">DevTools filtra cualquier recurso con un nombre de archivo que no termine con un o un seguido `j` `c` de 1 o más `s` caracteres.</span><span class="sxs-lookup"><span data-stu-id="e11dc-268">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filtro de expresiones regulares" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="e11dc-270">Filtro de expresiones regulares</span><span class="sxs-lookup"><span data-stu-id="e11dc-270">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-271">Escribe `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="e11dc-271">Type `-main.css`.</span></span>  <span data-ttu-id="e11dc-272">DevTools filtra `main.css` .</span><span class="sxs-lookup"><span data-stu-id="e11dc-272">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="e11dc-273">Si algún archivo coincide con el patrón, tit también se filtra.</span><span class="sxs-lookup"><span data-stu-id="e11dc-273">If any file matches the pattern, tit is also filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Un filtro negativo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="e11dc-275">Un filtro negativo</span><span class="sxs-lookup"><span data-stu-id="e11dc-275">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-276">Escriba `domain:cdn.glitch.com` en el cuadro **de** texto Filtrar.</span><span class="sxs-lookup"><span data-stu-id="e11dc-276">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="e11dc-277">DevTools filtra cualquier recurso con una dirección URL que no coincida con este dominio.</span><span class="sxs-lookup"><span data-stu-id="e11dc-277">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Filtro de propiedades" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="e11dc-279">Filtro de propiedades</span><span class="sxs-lookup"><span data-stu-id="e11dc-279">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e11dc-280">Para obtener la lista completa de propiedades filtrables, vaya a [Filtrar solicitudes por propiedades][DevtoolsReferenceProperty].</span><span class="sxs-lookup"><span data-stu-id="e11dc-280">For the full list of filterable properties, navigate to [Filter requests by properties][DevtoolsReferenceProperty].</span></span>  
    
1.  <span data-ttu-id="e11dc-281">Desactive el **cuadro de** texto Filtrar de cualquier texto.</span><span class="sxs-lookup"><span data-stu-id="e11dc-281">Clear the **Filter** text box of any text.</span></span>  
    
### <a name="filter-by-resource-type"></a><span data-ttu-id="e11dc-282">Filtrar por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="e11dc-282">Filter by resource type</span></span>  

<span data-ttu-id="e11dc-283">Para centrarse en un determinado tipo de archivo, como hojas de estilos:</span><span class="sxs-lookup"><span data-stu-id="e11dc-283">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="e11dc-284">Elija **CSS**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-284">Choose **CSS**.</span></span>  <span data-ttu-id="e11dc-285">El resto de tipos de archivo se filtran.</span><span class="sxs-lookup"><span data-stu-id="e11dc-285">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Mostrar solo archivos CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="e11dc-287">Mostrar solo archivos CSS</span><span class="sxs-lookup"><span data-stu-id="e11dc-287">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-288">Para mostrar también scripts, seleccione y mantenga presionado `Control` \(Windows, Linux\) o `Command` \(macOS\) y, a continuación, **elija JS**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-288">To also display scripts, select and hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Mostrar solo archivos CSS y JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="e11dc-290">Mostrar solo archivos CSS y JS</span><span class="sxs-lookup"><span data-stu-id="e11dc-290">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-291">Para quitar los filtros y volver a mostrar todos los recursos, elija **All**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-291">To remove the filters and display all resources again, choose **All**.</span></span>  
    
<span data-ttu-id="e11dc-292">Para otros flujos de trabajo de filtrado, vaya [a Filtrar solicitudes][DevtoolsNetworkReferenceFilter].</span><span class="sxs-lookup"><span data-stu-id="e11dc-292">For other filtering workflows, navigate to [Filter requests][DevtoolsNetworkReferenceFilter].</span></span>  

## <a name="block-requests"></a><span data-ttu-id="e11dc-293">Bloquear solicitudes</span><span class="sxs-lookup"><span data-stu-id="e11dc-293">Block requests</span></span>  

<span data-ttu-id="e11dc-294">¿Cómo se ve y se comporta una página cuando algunos de los recursos de página no están disponibles?</span><span class="sxs-lookup"><span data-stu-id="e11dc-294">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="e11dc-295">¿Falla completamente o todavía es algo funcional?</span><span class="sxs-lookup"><span data-stu-id="e11dc-295">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="e11dc-296">Bloquear solicitudes para averiguar:</span><span class="sxs-lookup"><span data-stu-id="e11dc-296">Block requests to find out:</span></span>  

1.  <span data-ttu-id="e11dc-297">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-297">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Menú comando" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="e11dc-299">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="e11dc-299">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-300">Escriba `block` , elija Mostrar bloqueo de **solicitudes**y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e11dc-300">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Mostrar bloqueo de solicitudes" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="e11dc-302">Mostrar bloqueo de solicitudes</span><span class="sxs-lookup"><span data-stu-id="e11dc-302">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-303">Elija **Agregar patrón** \( Agregar patrón ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e11dc-303">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="e11dc-304">Escribe `main.css`.</span><span class="sxs-lookup"><span data-stu-id="e11dc-304">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Bloqueo de main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="e11dc-306">Bloqueo</span><span class="sxs-lookup"><span data-stu-id="e11dc-306">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-307">Elija **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="e11dc-307">Choose **Add**.</span></span>  
1.  <span data-ttu-id="e11dc-308">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="e11dc-308">Refresh the page.</span></span>  <span data-ttu-id="e11dc-309">Como se esperaba, el estilo de la página está ligeramente desordenado porque la hoja de estilos principal se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e11dc-309">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e11dc-310">Fila `main.css` del registro de red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-310">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="e11dc-311">El texto rojo significa que el recurso se bloqueó.</span><span class="sxs-lookup"><span data-stu-id="e11dc-311">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css se ha bloqueado" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="e11dc-313">se ha bloqueado</span><span class="sxs-lookup"><span data-stu-id="e11dc-313">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e11dc-314">Anule la selección **de la casilla Habilitar bloqueo de solicitudes.**</span><span class="sxs-lookup"><span data-stu-id="e11dc-314">Deselect the **Enable request blocking** checkbox.</span></span>  

## <a name="conclusion"></a><span data-ttu-id="e11dc-315">Conclusión</span><span class="sxs-lookup"><span data-stu-id="e11dc-315">Conclusion</span></span>  

<span data-ttu-id="e11dc-316">Enhorabuena, ha completado el tutorial.</span><span class="sxs-lookup"><span data-stu-id="e11dc-316">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="e11dc-317">Ahora ya sabes cómo usar la herramienta **Red** en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e11dc-317">You now know how to use the **Network** tool in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="e11dc-318">Vaya a [la Referencia de red para][DevtoolsNetworkReference] descubrir más características de DevTools relacionadas con la inspección de la actividad de red.</span><span class="sxs-lookup"><span data-stu-id="e11dc-318">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e11dc-319">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e11dc-319">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReference]: ./reference.md "Referencia de análisis de red | Microsoft Docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Solicitudes de filtro: referencia de análisis de red | Microsoft Docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar el panel Información general: referencia de análisis de red | Microsoft Docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitudes por propiedades: referencia de análisis de red | Microsoft Docs"
[DevToolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools | Microsoft Docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspeccionar la demostración de actividad de red | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Almacenamiento en caché HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="e11dc-329">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e11dc-329">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e11dc-330">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e11dc-330">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e11dc-332">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e11dc-332">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
