---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
ms.openlocfilehash: 612b3b83aee1ee9035982e58e008395ec3645b2b
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408307"
---
# <a name="experimental-features"></a><span data-ttu-id="643a9-104">Características experimentales</span><span class="sxs-lookup"><span data-stu-id="643a9-104">Experimental features</span></span>  

<span data-ttu-id="643a9-105">Microsoft Edge DevTools proporciona acceso a características experimentales que aún están en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="643a9-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="643a9-106">Puede probar y [proporcionar comentarios antes](#providing-feedback-on-experimental-features) de publicar cada característica.</span><span class="sxs-lookup"><span data-stu-id="643a9-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="643a9-107">Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtenga las características experimentales más recientes con el canal de Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="643a9-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="643a9-108">Activar características experimentales</span><span class="sxs-lookup"><span data-stu-id="643a9-108">Turn on experimental features</span></span>  

<span data-ttu-id="643a9-109">Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="643a9-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="643a9-110">[Abra DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="643a9-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="643a9-111">Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="643a9-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="643a9-112">Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].</span><span class="sxs-lookup"><span data-stu-id="643a9-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="643a9-113">Abra el [panel][DevToolsCustomizeIndexSettings] Configuración.</span><span class="sxs-lookup"><span data-stu-id="643a9-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="643a9-114">Seleccione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="643a9-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="643a9-115">Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].</span><span class="sxs-lookup"><span data-stu-id="643a9-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="643a9-116">En el lado izquierdo del **panel Configuración,** elija la **sección** Experimentos.</span><span class="sxs-lookup"><span data-stu-id="643a9-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos en Configuración" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="643a9-118">La **página Experimentos** en **Configuración**</span><span class="sxs-lookup"><span data-stu-id="643a9-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="643a9-119">En la **página Experimentos,** desplácese por la lista de todas las características experimentales disponibles y elija la casilla junto a cada característica que desee probar.</span><span class="sxs-lookup"><span data-stu-id="643a9-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="643a9-120">Cierre y vuelva a abrir Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="643a9-121">Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="643a9-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="643a9-122">Para desactivar una característica experimental, abra la página **Experimentos** y desactive la casilla de la característica experimental que desea desactivar.</span><span class="sxs-lookup"><span data-stu-id="643a9-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="643a9-123">Características experimentales resaltadas</span><span class="sxs-lookup"><span data-stu-id="643a9-123">Highlighted experimental features</span></span>  

<span data-ttu-id="643a9-124">En las secciones siguientes se describen las nuevas características experimentales que están disponibles en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="643a9-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="643a9-125">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="643a9-125">Experimental feature</span></span> | <span data-ttu-id="643a9-126">Versión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="643a9-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="643a9-127">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="643a9-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="643a9-128">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-128">85 or later</span></span> |  
| [<span data-ttu-id="643a9-129">Habilitar consola de red</span><span class="sxs-lookup"><span data-stu-id="643a9-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="643a9-130">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-130">85 or later</span></span> |  
| [<span data-ttu-id="643a9-131">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="643a9-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="643a9-132">86 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-132">86 or later</span></span> |  
| [<span data-ttu-id="643a9-133">Habilitar capas compuestas en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="643a9-133">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="643a9-134">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-134">87 or later</span></span> |  
| [<span data-ttu-id="643a9-135">Habilitar la nueva herramienta Editor de fuentes en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="643a9-135">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="643a9-136">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-136">89 or later</span></span> |  
| [<span data-ttu-id="643a9-137">Habilitar nuevas características de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="643a9-137">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="643a9-138">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-138">89 or later</span></span> |  
| [<span data-ttu-id="643a9-139">Habilitar menús de pestañas + botón para abrir más herramientas</span><span class="sxs-lookup"><span data-stu-id="643a9-139">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="643a9-140">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-140">89 or later</span></span> |  
| [<span data-ttu-id="643a9-141">Pestaña Habilitar bienvenida</span><span class="sxs-lookup"><span data-stu-id="643a9-141">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="643a9-142">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="643a9-142">89 or later</span></span> |  

### <a name="enable-webhint"></a><span data-ttu-id="643a9-143">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="643a9-143">Enable webhint</span></span>  

<span data-ttu-id="643a9-144">[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.</span><span class="sxs-lookup"><span data-stu-id="643a9-144">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="643a9-145">El tipo de comentarios proporcionados [por webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="643a9-145">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="643a9-146">accesibilidad</span><span class="sxs-lookup"><span data-stu-id="643a9-146">accessibility</span></span>  
*   <span data-ttu-id="643a9-147">compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="643a9-147">cross-browser compatibility</span></span>  
*   <span data-ttu-id="643a9-148">seguridad</span><span class="sxs-lookup"><span data-stu-id="643a9-148">security</span></span>  
*   <span data-ttu-id="643a9-149">rendimiento</span><span class="sxs-lookup"><span data-stu-id="643a9-149">performance</span></span>  
*   <span data-ttu-id="643a9-150">Aplicaciones web progresivas (PWA)</span><span class="sxs-lookup"><span data-stu-id="643a9-150">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="643a9-151">otros problemas comunes de desarrollo web</span><span class="sxs-lookup"><span data-stu-id="643a9-151">other common web development issues</span></span>  
    
<span data-ttu-id="643a9-152">El [experimento webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="643a9-152">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="643a9-153">Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="643a9-153">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="643a9-154">Elija un vínculo de recurso para abrir el panel **Network**, **Sources**o **Elements** relevante en DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-154">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="643a9-156">comentarios de webhint en el panel **Problemas**</span><span class="sxs-lookup"><span data-stu-id="643a9-156">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="643a9-157">Habilitar consola de red</span><span class="sxs-lookup"><span data-stu-id="643a9-157">Enable Network Console</span></span>  

<span data-ttu-id="643a9-158">**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="643a9-158">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="643a9-159">Puede usar el experimento **consola de** red para enviar solicitudes de API web.</span><span class="sxs-lookup"><span data-stu-id="643a9-159">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="643a9-160">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-160">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="643a9-161">Para usar la **consola de red,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="643a9-161">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="643a9-162">Abra el **panel** Red.</span><span class="sxs-lookup"><span data-stu-id="643a9-162">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="643a9-163">Busque la solicitud de red que desea cambiar y reenviar.</span><span class="sxs-lookup"><span data-stu-id="643a9-163">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="643a9-164">Abra el menú contextual \(right-click\) y elija **Editar y reproducir**.</span><span class="sxs-lookup"><span data-stu-id="643a9-164">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="643a9-165">Cuando se **abra la consola de** red, edite la información de solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="643a9-165">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="643a9-166">Elija **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="643a9-166">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="643a9-168">**Consola de red** en el **cajón de la** consola</span><span class="sxs-lookup"><span data-stu-id="643a9-168">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="643a9-169">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="643a9-169">Source Order Viewer</span></span>  

<span data-ttu-id="643a9-170">**El Visor de pedidos de** origen es un experimento que muestra el orden de los elementos en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="643a9-170">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="643a9-171">El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde el lector de pantalla y los usuarios de teclado.</span><span class="sxs-lookup"><span data-stu-id="643a9-171">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="643a9-172">Use el **experimento Visor de pedidos de** origen para encontrar las diferencias entre el orden de visualización en pantalla y el orden del origen.</span><span class="sxs-lookup"><span data-stu-id="643a9-172">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="643a9-173">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-173">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="643a9-174">Para usar **el Visor de pedidos de origen,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="643a9-174">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="643a9-175">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="643a9-175">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="643a9-176">Abra el **panel Accesibilidad** en el panel \(bottom\) del cajón.</span><span class="sxs-lookup"><span data-stu-id="643a9-176">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="643a9-177">En la **sección Visor de pedidos de** origen, elija la casilla Mostrar orden **de** origen.</span><span class="sxs-lookup"><span data-stu-id="643a9-177">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="643a9-178">Resalte cualquier elemento HTML para mostrar una superposición que el orden en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="643a9-178">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visor de pedidos de origen en el panel Accesibilidad" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="643a9-180">**Visor de pedidos de origen** en el panel **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="643a9-180">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="643a9-181">Habilitar capas compuestas en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="643a9-181">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="643a9-182">Ahora puede visualizar capas junto con índices z y el modelo de objetos de documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="643a9-182">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="643a9-183">Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.</span><span class="sxs-lookup"><span data-stu-id="643a9-183">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="643a9-184">Identificó que la reducción del cambio de contexto era un punto de dolor importante.</span><span class="sxs-lookup"><span data-stu-id="643a9-184">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="643a9-185">No siempre está claro cómo el código que escribe afecta a la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="643a9-185">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="643a9-186">Para obtener una experiencia de depuración visual completa, ahora se combinan la vista 3D y las Capas compuestas.</span><span class="sxs-lookup"><span data-stu-id="643a9-186">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="643a9-187">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-187">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="643a9-188">Para usar **capas compuestas,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="643a9-188">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="643a9-189">En el cajón, elija la **herramienta Vista 3D.**</span><span class="sxs-lookup"><span data-stu-id="643a9-189">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="643a9-190">Abra el **panel Capas compuestas.**</span><span class="sxs-lookup"><span data-stu-id="643a9-190">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="643a9-191">Se muestran todas las capas pintadas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="643a9-191">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="643a9-192">Pruebe esta característica con sus propias aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="643a9-192">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="643a9-194">Panel **Capas compuestas**</span><span class="sxs-lookup"><span data-stu-id="643a9-194">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="643a9-195">Habilitar la nueva herramienta Editor de fuentes en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="643a9-195">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="643a9-196">Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.</span><span class="sxs-lookup"><span data-stu-id="643a9-196">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="643a9-197">Úselo para definir fuentes y características de fuente.</span><span class="sxs-lookup"><span data-stu-id="643a9-197">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="643a9-198">El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="643a9-198">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="643a9-199">Cambiar entre unidades para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="643a9-199">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="643a9-200">Cambiar entre palabras clave para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="643a9-200">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="643a9-201">Convertir unidades</span><span class="sxs-lookup"><span data-stu-id="643a9-201">Convert units</span></span>  
*   <span data-ttu-id="643a9-202">Generar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="643a9-202">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="643a9-203">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-203">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="643a9-204">Para usar el nuevo Editor de **fuentes visuales,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="643a9-204">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="643a9-205">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="643a9-205">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="643a9-206">Abra el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="643a9-206">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="643a9-207">Elija el **icono Editor de** fuentes.</span><span class="sxs-lookup"><span data-stu-id="643a9-207">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="643a9-208">Para obtener más información sobre el nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuentes CSS en el panel Estilos [en DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="643a9-208">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Se resalta el panel Editor de fuentes visuales" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="643a9-210">Se resalta **el panel Editor de** fuentes visuales</span><span class="sxs-lookup"><span data-stu-id="643a9-210">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="643a9-211">Habilitar nuevas características de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="643a9-211">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="643a9-212">Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños de CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="643a9-212">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="643a9-213">Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-213">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="643a9-214">Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="643a9-214">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="643a9-215">La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de CSS Flexbox en un sitio web activando el mouse sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="643a9-215">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="643a9-216">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-216">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="643a9-217">A continuación, mientras depura el sitio web, mantenga el mouse en un contenedor flexible para mostrar los contornos alrededor del contenedor flexible.</span><span class="sxs-lookup"><span data-stu-id="643a9-217">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="643a9-219">Mostrar contenedores de Flexbox con **la herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="643a9-219">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="643a9-220">Mostrar superposiciones persistentes en diseños de Flexbox</span><span class="sxs-lookup"><span data-stu-id="643a9-220">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="643a9-221">En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="643a9-221">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="643a9-222">Las superposiciones persistentes proporcionan las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="643a9-222">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="643a9-223">Las superposiciones persistentes permanecen visibles en la página web a medida que se desplaza, mueve el mouse y usa otras características de DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-223">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="643a9-224">Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.</span><span class="sxs-lookup"><span data-stu-id="643a9-224">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="643a9-225">Las superposiciones persistentes ofrecen opciones de configuración de color.</span><span class="sxs-lookup"><span data-stu-id="643a9-225">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="643a9-226">Para alternar las superposiciones persistentes en el diseño de Flexbox, use una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="643a9-226">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="643a9-227">Elija el **icono oval de Flexbox** junto a cualquier contenedor de Flexbox que se muestre en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="643a9-227">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="643a9-228">Abra el nuevo panel **Diseño** ubicado en la **herramienta Elementos** y seleccione la casilla situada junto a cada contenedor de Flexbox que desee resaltar.</span><span class="sxs-lookup"><span data-stu-id="643a9-228">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos de Flex y panel Diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="643a9-230">Iconos de Flex y panel **Diseño** en DevTools</span><span class="sxs-lookup"><span data-stu-id="643a9-230">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="643a9-231">Configurar superposiciones persistentes</span><span class="sxs-lookup"><span data-stu-id="643a9-231">Configure persistent overlays</span></span>  

<span data-ttu-id="643a9-232">Para configurar opciones para superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, use el **panel** Diseño.</span><span class="sxs-lookup"><span data-stu-id="643a9-232">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="643a9-233">El **panel** Diseño se encuentra en la **herramienta Elementos** junto a los paneles **Estilos** **y** Calculados.</span><span class="sxs-lookup"><span data-stu-id="643a9-233">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel Diseño" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="643a9-235">Panel Diseño</span><span class="sxs-lookup"><span data-stu-id="643a9-235">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="643a9-236">Habilitar menús de pestañas + botón para abrir más herramientas</span><span class="sxs-lookup"><span data-stu-id="643a9-236">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="643a9-237">Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="643a9-237">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="643a9-238">Después de activar los menús de la pestaña Habilitar + botón para abrir más herramientas experimentar y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de **pestañas** en la parte superior `+` de DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-238">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="643a9-239">Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="643a9-239">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="643a9-241">**Más herramientas** en el panel superior</span><span class="sxs-lookup"><span data-stu-id="643a9-241">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="643a9-242">Habilitar herramienta de bienvenida</span><span class="sxs-lookup"><span data-stu-id="643a9-242">Enable Welcome tool</span></span>

<span data-ttu-id="643a9-243">Este experimento reemplaza la herramienta **Novedades** por la nueva **herramienta De** bienvenida.</span><span class="sxs-lookup"><span data-stu-id="643a9-243">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="643a9-244">Muestra un diseño actualizado para el siguiente contenido.</span><span class="sxs-lookup"><span data-stu-id="643a9-244">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="643a9-245">Vínculos a documentos para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="643a9-245">Links to developer docs</span></span>  
*   <span data-ttu-id="643a9-246">las características más recientes</span><span class="sxs-lookup"><span data-stu-id="643a9-246">the latest features</span></span>  
*   <span data-ttu-id="643a9-247">notas de la versión</span><span class="sxs-lookup"><span data-stu-id="643a9-247">release notes</span></span>  
*   <span data-ttu-id="643a9-248">Opción para ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="643a9-248">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="643a9-249">La **herramienta De** bienvenida se abre automáticamente después de cada actualización de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="643a9-249">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="643a9-250">Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña Abrir después de cada **actualización** en el **título de** la herramienta de bienvenida.</span><span class="sxs-lookup"><span data-stu-id="643a9-250">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="643a9-251">Si prefiere la herramienta **novedades** original, [][DevtoolsCustomizeIndexSettings]vaya a Experimentos de configuración y quite la casilla situada junto a  >  \*\*\*\* La pestaña Habilitar **bienvenida**.</span><span class="sxs-lookup"><span data-stu-id="643a9-251">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="643a9-253">**Herramienta de** bienvenida</span><span class="sxs-lookup"><span data-stu-id="643a9-253">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="643a9-254">Características experimentales anteriores</span><span class="sxs-lookup"><span data-stu-id="643a9-254">Previous experimental features</span></span>  

*   <span data-ttu-id="643a9-255">[La vista 3D][Devtools3dViewIndex] ya está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.</span><span class="sxs-lookup"><span data-stu-id="643a9-255">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="643a9-256">[Activar la compatibilidad para mover pestañas][DevtoolsCustomizeIndex] entre paneles ya está disponible y activada de forma predeterminada en Microsoft Edge versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="643a9-256">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="643a9-257">[Hacer coincidir los métodos abreviados][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] de teclado en DevTools con Microsoft Visual Studio Code ya está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="643a9-257">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="643a9-258">[Editar métodos abreviados de][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] teclado para cualquier acción en DevTools ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="643a9-258">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="643a9-259">[Activar nuevas características de depuración de][DevtoolsCssGrid] cuadrícula CSS ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="643a9-259">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="643a9-260">[Emulación: el modo de pantalla dual ya][DevtoolsDeviceModeDualScreenAndFoldables] está disponible y activado de forma predeterminada en Microsoft Edge versión 90 o posterior.</span><span class="sxs-lookup"><span data-stu-id="643a9-260">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="643a9-261">Proporcionar comentarios sobre características experimentales</span><span class="sxs-lookup"><span data-stu-id="643a9-261">Providing feedback on experimental features</span></span>  

<span data-ttu-id="643a9-262">Para proporcionar comentarios sobre los experimentos de Microsoft Edge DevTools o cualquier otra cosa relacionada con DevTools.</span><span class="sxs-lookup"><span data-stu-id="643a9-262">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="643a9-263">Enviar sus comentarios con el icono **Enviar comentarios** en DevTools</span><span class="sxs-lookup"><span data-stu-id="643a9-263">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="643a9-264">Tweet en [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="643a9-264">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="643a9-266">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="643a9-266">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
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
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edite los métodos abreviados de teclado para cualquier acción en el archivo DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Coincidencia de métodos abreviados de teclado en devTools a Microsoft Visual Studio código | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos y configuraciones de fuentes CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
