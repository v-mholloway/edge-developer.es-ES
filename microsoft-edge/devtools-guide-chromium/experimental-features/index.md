---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: c76830cb8bbcc597aa026f58e1926cd2f9bc2d62
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439587"
---
# <a name="experimental-features"></a><span data-ttu-id="cdc21-104">Características experimentales</span><span class="sxs-lookup"><span data-stu-id="cdc21-104">Experimental features</span></span>  

<span data-ttu-id="cdc21-105">Microsoft Edge DevTools proporciona acceso a características experimentales que aún están en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="cdc21-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="cdc21-106">Puede probar y [proporcionar comentarios antes](#providing-feedback-on-experimental-features) de publicar cada característica.</span><span class="sxs-lookup"><span data-stu-id="cdc21-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="cdc21-107">Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtenga las características experimentales más recientes con el canal de Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="cdc21-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="cdc21-108">Activar características experimentales</span><span class="sxs-lookup"><span data-stu-id="cdc21-108">Turn on experimental features</span></span>  

<span data-ttu-id="cdc21-109">Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="cdc21-110">[Abra DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="cdc21-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="cdc21-111">Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="cdc21-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="cdc21-112">Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].</span><span class="sxs-lookup"><span data-stu-id="cdc21-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="cdc21-113">Abra el [panel][DevToolsCustomizeIndexSettings] Configuración.</span><span class="sxs-lookup"><span data-stu-id="cdc21-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="cdc21-114">Seleccione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="cdc21-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="cdc21-115">Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].</span><span class="sxs-lookup"><span data-stu-id="cdc21-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="cdc21-116">En el lado izquierdo del **panel Configuración,** elija la **sección** Experimentos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos en Configuración" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="cdc21-118">La **página Experimentos** en **Configuración**</span><span class="sxs-lookup"><span data-stu-id="cdc21-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cdc21-119">En la **página Experimentos,** desplácese por la lista de todas las características experimentales disponibles y elija la casilla junto a cada característica que desee probar.</span><span class="sxs-lookup"><span data-stu-id="cdc21-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="cdc21-120">Cierre y vuelva a abrir Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="cdc21-121">Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="cdc21-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="cdc21-122">Para desactivar una característica experimental, abra la página **Experimentos** y desactive la casilla de la característica experimental que desea desactivar.</span><span class="sxs-lookup"><span data-stu-id="cdc21-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="cdc21-123">Características experimentales resaltadas</span><span class="sxs-lookup"><span data-stu-id="cdc21-123">Highlighted experimental features</span></span>  

<span data-ttu-id="cdc21-124">En las secciones siguientes se describen las nuevas características experimentales que están disponibles en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cdc21-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="cdc21-125">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="cdc21-125">Experimental feature</span></span> | <span data-ttu-id="cdc21-126">Versión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cdc21-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | <span data-ttu-id="cdc21-127">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-127">85 or later</span></span> |  
| [Enable Network Console](#enable-network-console) | <span data-ttu-id="cdc21-128">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-128">85 or later</span></span> |  
| [Source Order Viewer](#source-order-viewer) | <span data-ttu-id="cdc21-129">86 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-129">86 or later</span></span> |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | <span data-ttu-id="cdc21-130">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-130">87 or later</span></span> |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="cdc21-131">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-131">89 or later</span></span> |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="cdc21-132">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-132">89 or later</span></span> |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="cdc21-133">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-133">89 or later</span></span> |  
| [Enable Welcome tab](#enable-welcome-tab) | <span data-ttu-id="cdc21-134">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="cdc21-134">89 or later</span></span> |  

### Enable webhint  

<span data-ttu-id="cdc21-135">[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.</span><span class="sxs-lookup"><span data-stu-id="cdc21-135">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="cdc21-136">El tipo de comentarios proporcionados [por webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="cdc21-136">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="cdc21-137">accesibilidad</span><span class="sxs-lookup"><span data-stu-id="cdc21-137">accessibility</span></span>  
*   <span data-ttu-id="cdc21-138">compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="cdc21-138">cross-browser compatibility</span></span>  
*   <span data-ttu-id="cdc21-139">seguridad</span><span class="sxs-lookup"><span data-stu-id="cdc21-139">security</span></span>  
*   <span data-ttu-id="cdc21-140">rendimiento</span><span class="sxs-lookup"><span data-stu-id="cdc21-140">performance</span></span>  
*   <span data-ttu-id="cdc21-141">Aplicaciones web progresivas (PWA)</span><span class="sxs-lookup"><span data-stu-id="cdc21-141">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="cdc21-142">otros problemas comunes de desarrollo web</span><span class="sxs-lookup"><span data-stu-id="cdc21-142">other common web development issues</span></span>  
    
<span data-ttu-id="cdc21-143">El [experimento webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="cdc21-143">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="cdc21-144">Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="cdc21-144">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="cdc21-145">Elija un vínculo de recurso para abrir el panel **Network**, **Sources**o **Elements** relevante en DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-145">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="cdc21-147">comentarios de webhint en el panel **Problemas**</span><span class="sxs-lookup"><span data-stu-id="cdc21-147">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

<span data-ttu-id="cdc21-148">**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="cdc21-148">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="cdc21-149">Puede usar el experimento **consola de** red para enviar solicitudes de API web.</span><span class="sxs-lookup"><span data-stu-id="cdc21-149">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="cdc21-150">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-150">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="cdc21-151">Para usar la **consola de red,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-151">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="cdc21-152">Abra el **panel** Red.</span><span class="sxs-lookup"><span data-stu-id="cdc21-152">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="cdc21-153">Busque la solicitud de red que desea cambiar y reenviar.</span><span class="sxs-lookup"><span data-stu-id="cdc21-153">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="cdc21-154">Abra el menú contextual \(right-click\) y elija **Editar y reproducir**.</span><span class="sxs-lookup"><span data-stu-id="cdc21-154">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="cdc21-155">Cuando se **abra la consola de** red, edite la información de solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="cdc21-155">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="cdc21-156">Elija **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="cdc21-156">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="cdc21-158">**Consola de red** en el **cajón de la** consola</span><span class="sxs-lookup"><span data-stu-id="cdc21-158">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

<span data-ttu-id="cdc21-159">**Source Order Viewer** es un experimento que muestra el orden de los elementos en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="cdc21-159">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="cdc21-160">El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde el lector de pantalla y los usuarios de teclado.</span><span class="sxs-lookup"><span data-stu-id="cdc21-160">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="cdc21-161">Use el experimento para encontrar las diferencias entre el orden de visualización en pantalla **Source Order Viewer** y el orden del origen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-161">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="cdc21-162">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-162">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="cdc21-163">Para usar **Source Order Viewer** , complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="cdc21-163">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="cdc21-164">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-164">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="cdc21-165">Abra el **panel Accesibilidad** en el panel \(bottom\) del cajón.</span><span class="sxs-lookup"><span data-stu-id="cdc21-165">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="cdc21-166">En la **Source Order Viewer** sección, seleccione la casilla **Mostrar orden de origen.**</span><span class="sxs-lookup"><span data-stu-id="cdc21-166">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="cdc21-167">Resalte cualquier elemento HTML para mostrar una superposición que el orden en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="cdc21-167">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text=":::<span data-ttu-id="cdc21-168">no-loc(Source Order Viewer)::: en el panel Accesibilidad" lightbox=".. /media/experiments-source-order-viewer.msft.png":: **Source Order Viewer** en el panel **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="cdc21-168">no-loc(Source Order Viewer)::: in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png"::: **Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

<span data-ttu-id="cdc21-169">Ahora puede visualizar capas junto con índices z y el modelo de objetos de documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="cdc21-169">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="cdc21-170">Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cdc21-170">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="cdc21-171">Identificó que la reducción del cambio de contexto era un punto de dolor importante.</span><span class="sxs-lookup"><span data-stu-id="cdc21-171">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="cdc21-172">No siempre está claro cómo el código que escribe afecta a la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="cdc21-172">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="cdc21-173">Para una experiencia de depuración visual completa, ahora se combinan las capas 3D View compuestas y las capas compuestas.</span><span class="sxs-lookup"><span data-stu-id="cdc21-173">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="cdc21-174">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-174">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="cdc21-175">Para usar **capas compuestas,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-175">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="cdc21-176">En el cajón, elija la **3D View** herramienta.</span><span class="sxs-lookup"><span data-stu-id="cdc21-176">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="cdc21-177">Abra el **panel Capas compuestas.**</span><span class="sxs-lookup"><span data-stu-id="cdc21-177">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="cdc21-178">Se muestran todas las capas pintadas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdc21-178">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="cdc21-179">Pruebe esta característica con sus propias aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="cdc21-179">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="cdc21-181">Panel **Capas compuestas**</span><span class="sxs-lookup"><span data-stu-id="cdc21-181">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

<span data-ttu-id="cdc21-182">Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.</span><span class="sxs-lookup"><span data-stu-id="cdc21-182">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="cdc21-183">Úselo para definir fuentes y características de fuente.</span><span class="sxs-lookup"><span data-stu-id="cdc21-183">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="cdc21-184">El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="cdc21-184">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="cdc21-185">Cambiar entre unidades para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="cdc21-185">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="cdc21-186">Cambiar entre palabras clave para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="cdc21-186">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="cdc21-187">Convertir unidades</span><span class="sxs-lookup"><span data-stu-id="cdc21-187">Convert units</span></span>  
*   <span data-ttu-id="cdc21-188">Generar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="cdc21-188">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="cdc21-189">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-189">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="cdc21-190">Para usar el nuevo Editor de **fuentes visuales,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-190">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="cdc21-191">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-191">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="cdc21-192">Abra el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="cdc21-192">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="cdc21-193">Elija el **icono Editor de** fuentes.</span><span class="sxs-lookup"><span data-stu-id="cdc21-193">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="cdc21-194">Para obtener más información sobre el nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuentes CSS en el panel Estilos [en DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="cdc21-194">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Se resalta el panel Editor de fuentes visuales" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="cdc21-196">Se resalta **el panel Editor de** fuentes visuales</span><span class="sxs-lookup"><span data-stu-id="cdc21-196">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

<span data-ttu-id="cdc21-197">Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños de CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="cdc21-197">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="cdc21-198">Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-198">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="cdc21-199">Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="cdc21-199">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="cdc21-200">La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de CSS Flexbox en un sitio web activando el mouse sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-200">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="cdc21-201">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-201">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="cdc21-202">A continuación, mientras depura el sitio web, mantenga el mouse en un contenedor flexible para mostrar los contornos alrededor del contenedor flexible.</span><span class="sxs-lookup"><span data-stu-id="cdc21-202">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="cdc21-204">Mostrar contenedores de Flexbox con **la herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="cdc21-204">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="cdc21-205">Mostrar superposiciones persistentes en diseños de Flexbox</span><span class="sxs-lookup"><span data-stu-id="cdc21-205">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="cdc21-206">En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="cdc21-206">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="cdc21-207">Las superposiciones persistentes proporcionan las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="cdc21-207">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="cdc21-208">Las superposiciones persistentes permanecen visibles en la página web a medida que se desplaza, mueve el mouse y usa otras características de DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-208">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="cdc21-209">Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.</span><span class="sxs-lookup"><span data-stu-id="cdc21-209">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="cdc21-210">Las superposiciones persistentes ofrecen opciones de configuración de color.</span><span class="sxs-lookup"><span data-stu-id="cdc21-210">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="cdc21-211">Para alternar las superposiciones persistentes en el diseño de Flexbox, use una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="cdc21-211">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="cdc21-212">Elija el **icono oval de Flexbox** junto a cualquier contenedor de Flexbox que se muestre en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="cdc21-212">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="cdc21-213">Abra el nuevo panel **Diseño** ubicado en la **herramienta Elementos** y seleccione la casilla situada junto a cada contenedor de Flexbox que desee resaltar.</span><span class="sxs-lookup"><span data-stu-id="cdc21-213">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos de Flex y panel Diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="cdc21-215">Iconos de Flex y panel **Diseño** en DevTools</span><span class="sxs-lookup"><span data-stu-id="cdc21-215">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="cdc21-216">Configurar superposiciones persistentes</span><span class="sxs-lookup"><span data-stu-id="cdc21-216">Configure persistent overlays</span></span>  

<span data-ttu-id="cdc21-217">Para configurar opciones para superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, use el **panel** Diseño.</span><span class="sxs-lookup"><span data-stu-id="cdc21-217">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="cdc21-218">El **panel** Diseño se encuentra en la **herramienta Elementos** junto a los paneles **Estilos** **y** Calculados.</span><span class="sxs-lookup"><span data-stu-id="cdc21-218">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel Diseño" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="cdc21-220">Panel Diseño</span><span class="sxs-lookup"><span data-stu-id="cdc21-220">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

<span data-ttu-id="cdc21-221">Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="cdc21-221">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="cdc21-222">Después de activar el experimento y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de pestañas en la parte superior **Enable + button tab menus to open more tools** `+` de DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-222">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="cdc21-223">Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="cdc21-223">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="cdc21-225">**Más herramientas** en el panel superior</span><span class="sxs-lookup"><span data-stu-id="cdc21-225">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

<span data-ttu-id="cdc21-226">Este experimento reemplaza la herramienta **Novedades** por la nueva **herramienta De** bienvenida.</span><span class="sxs-lookup"><span data-stu-id="cdc21-226">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="cdc21-227">Muestra un diseño actualizado para el siguiente contenido.</span><span class="sxs-lookup"><span data-stu-id="cdc21-227">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="cdc21-228">Vínculos a documentos para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="cdc21-228">Links to developer docs</span></span>  
*   <span data-ttu-id="cdc21-229">las características más recientes</span><span class="sxs-lookup"><span data-stu-id="cdc21-229">the latest features</span></span>  
*   <span data-ttu-id="cdc21-230">notas de la versión</span><span class="sxs-lookup"><span data-stu-id="cdc21-230">release notes</span></span>  
*   <span data-ttu-id="cdc21-231">Opción para ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cdc21-231">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="cdc21-232">La **herramienta De** bienvenida se abre automáticamente después de cada actualización de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cdc21-232">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="cdc21-233">Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña Abrir después de cada **actualización** en el **título de** la herramienta de bienvenida.</span><span class="sxs-lookup"><span data-stu-id="cdc21-233">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="cdc21-234">Si prefiere la herramienta original **Novedades,** vaya a Experimentos de [][DevtoolsCustomizeIndexSettings]  >  **configuración** y quite la casilla situada junto a **Enable Welcome tab** .</span><span class="sxs-lookup"><span data-stu-id="cdc21-234">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="cdc21-236">**Herramienta de** bienvenida</span><span class="sxs-lookup"><span data-stu-id="cdc21-236">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="cdc21-237">Características experimentales anteriores</span><span class="sxs-lookup"><span data-stu-id="cdc21-237">Previous experimental features</span></span>  

*   <span data-ttu-id="cdc21-238">[3D View][Devtools3dViewIndex] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 83 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cdc21-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="cdc21-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cdc21-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="cdc21-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cdc21-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="cdc21-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cdc21-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="cdc21-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cdc21-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="cdc21-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 90 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cdc21-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="cdc21-244">Proporcionar comentarios sobre características experimentales</span><span class="sxs-lookup"><span data-stu-id="cdc21-244">Providing feedback on experimental features</span></span>  

<span data-ttu-id="cdc21-245">Para proporcionar comentarios sobre los experimentos de Microsoft Edge DevTools o cualquier otra cosa relacionada con DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdc21-245">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="cdc21-246">Enviar sus comentarios con el icono **Enviar comentarios** en DevTools</span><span class="sxs-lookup"><span data-stu-id="cdc21-246">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="cdc21-247">Tweet en [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="cdc21-247">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="cdc21-249">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cdc21-249">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Vista 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspeccionar CSS Grid en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edit keyboard shortcuts for any action in the DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos y configuraciones de fuentes CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
