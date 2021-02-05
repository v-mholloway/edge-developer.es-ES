---
description: La herramienta Novedades ahora es Welcome, Visual Font Editor en el panel Estilos, herramientas de depuración css Flexbox y mucho más.
title: Novedades de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0a8a5e69281ced9421733059b554bd8cb997c7cd
ms.sourcegitcommit: 085046a5885c68243b763aaf6809fea43452403a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313779"
---
# <span data-ttu-id="448a4-104">Novedades de DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="448a4-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="448a4-105">What's New is now Welcome</span><span class="sxs-lookup"><span data-stu-id="448a4-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="448a4-106">La **herramienta Novedades de** Microsoft Edge DevTools ahora tiene una nueva apariencia y un nuevo nombre: **Bienvenido.**</span><span class="sxs-lookup"><span data-stu-id="448a4-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="448a4-107">La **herramienta de** bienvenida aún muestra las últimas noticias y actualizaciones de DevTools.</span><span class="sxs-lookup"><span data-stu-id="448a4-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="448a4-108">Ahora también incluye vínculos a la documentación de Microsoft Edge DevTools, formas de enviar comentarios y mucho más.</span><span class="sxs-lookup"><span data-stu-id="448a4-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="448a4-109">Para mostrar la **herramienta de** bienvenida después de cada actualización a Microsoft Edge, seleccione la casilla situada junto a la pestaña Abrir después de cada **actualización** bajo el título.</span><span class="sxs-lookup"><span data-stu-id="448a4-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="448a4-110">Para cerrar la **herramienta de** bienvenida, elija la **X** en el lado derecho del título de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="448a4-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="448a4-111">Si prefieres la **herramienta** Novedades original, ve a Experimentos de configuración y quita la casilla junto a [][DevtoolsCustomizeIndexSettings]  >  \*\*\*\* Habilitar **pestaña de bienvenida.**</span><span class="sxs-lookup"><span data-stu-id="448a4-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="La herramienta de bienvenida está resaltada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="448a4-113">La **herramienta de** bienvenida está resaltada</span><span class="sxs-lookup"><span data-stu-id="448a4-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <span data-ttu-id="448a4-114">Editor de fuentes visuales en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="448a4-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="448a4-115">Cuando trabaje con fuentes en CSS, use el nuevo Editor de [fuentes visual.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="448a4-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="448a4-116">Puedes definir fuentes de reserva y usar controles deslizantes para definir el grosor, el tamaño, el alto de línea y el espaciado de la fuente.</span><span class="sxs-lookup"><span data-stu-id="448a4-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="448a4-117">El **Editor de** fuentes le ayuda a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="448a4-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="448a4-118">Cambiar entre unidades para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="448a4-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="448a4-119">Cambiar entre palabras clave para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="448a4-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="448a4-120">Convertir unidades</span><span class="sxs-lookup"><span data-stu-id="448a4-120">Convert units</span></span>  
*   <span data-ttu-id="448a4-121">Generar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="448a4-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="448a4-122">Para activar este experimento, [][DevtoolsCustomizeIndexSettings]ve a Experimentos de configuración y elige la casilla junto a Habilitar nuevas herramientas del Editor de fuentes  >  \*\*\*\* en el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="448a4-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="448a4-123">Para obtener más información, vaya a Editar estilos y configuraciones de fuente CSS en [el panel Estilos de DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="448a4-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="448a4-124">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1093229][CR1093229].</span><span class="sxs-lookup"><span data-stu-id="448a4-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="El editor de fuentes visuales se resalta en el panel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="448a4-126">El editor **de fuentes visuales** se resalta en el panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="448a4-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="448a4-127">Herramientas de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="448a4-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="448a4-128">Las características de depuración de Flexbox están en desarrollo activo.</span><span class="sxs-lookup"><span data-stu-id="448a4-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="448a4-129">Para activar el experimento para las dos [][DevtoolsCustomizeIndexSettings]características siguientes, ve a Experimentos de configuración y elige la casilla junto a Habilitar nuevas características  >  \*\*\*\* **de depuración de CSS Flexbox**.</span><span class="sxs-lookup"><span data-stu-id="448a4-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="448a4-130">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a los problemas [1136394][CR1136394] y [1139949.][CR1139949]</span><span class="sxs-lookup"><span data-stu-id="448a4-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <span data-ttu-id="448a4-131">El nuevo icono de Flexbox (flex) ayuda a identificar y mostrar contenedores flex</span><span class="sxs-lookup"><span data-stu-id="448a4-131">New Flexbox (flex) icon helps identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="448a4-132">En la **herramienta Elementos,** el nuevo icono de Flexbox (flex) te ayuda a identificar contenedores de Flexbox en el código.</span><span class="sxs-lookup"><span data-stu-id="448a4-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="448a4-133">Elige el icono de Flexbox \(flex\) para activar o desactivar el efecto de superposición que describe un contenedor de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="448a4-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="448a4-134">Puede personalizar el color de la superposición en **el** panel Diseño, que se encuentra junto **a Estilos** y **Calculado.**</span><span class="sxs-lookup"><span data-stu-id="448a4-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="448a4-135">Para activar y desactivar el efecto de superposición que describe el contenedor de Flexbox, elija el icono Flexbox \( `flex` \).</span><span class="sxs-lookup"><span data-stu-id="448a4-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="448a4-136">Puede personalizar el color de la superposición en el panel **Diseño** junto **a Estilos** y **Calculado.**</span><span class="sxs-lookup"><span data-stu-id="448a4-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="El icono de Flexbox (flex) y la página web resaltados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="448a4-138">El **icono de Flexbox** \( `flex` \) y la página web resaltados</span><span class="sxs-lookup"><span data-stu-id="448a4-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Las superposiciones de Flexbox resaltadas en el panel Diseño" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="448a4-140">Las **superposiciones de Flexbox resaltadas** en el **panel Diseño**</span><span class="sxs-lookup"><span data-stu-id="448a4-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="448a4-141">Mostrar iconos de alineación y líneas de cuadrícula cuando los diseños de Flexbox cambian mediante propiedades CSS</span><span class="sxs-lookup"><span data-stu-id="448a4-141">Display alignment icons and gridlines when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="448a4-142">Al editar CSS para el diseño de Flexbox, CSS se autocompleta en el panel Estilos ahora muestra iconos útiles junto a las propiedades pertinentes de Flexbox. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="448a4-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="448a4-143">Para probar esta nueva característica, abra la herramienta **Elementos** y seleccione un contenedor flexible.</span><span class="sxs-lookup"><span data-stu-id="448a4-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="448a4-144">A continuación, agregue o cambie una propiedad en ese contenedor en el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="448a4-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="448a4-145">El menú Autocompletar ahora muestra iconos que indican el efecto de propiedades de alineación como `align-content` y `align-items` .</span><span class="sxs-lookup"><span data-stu-id="448a4-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="448a4-146">Además, DevTools ahora muestra una línea de guidación para ayudarte a revisar mejor la `align-items` propiedad CSS.</span><span class="sxs-lookup"><span data-stu-id="448a4-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="448a4-147">También `gap` se admite la propiedad CSS.</span><span class="sxs-lookup"><span data-stu-id="448a4-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="448a4-148">En la figura siguiente, la propiedad CSS se establece en y se muestra el patrón de trama `gap` `gap: 12px;` de cada intervalo.</span><span class="sxs-lookup"><span data-stu-id="448a4-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menú Autocompletar resaltado para las propiedades CSS que comienzan con align-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="448a4-150">Menú Autocompletar resaltado para las propiedades CSS que empiezan por</span><span class="sxs-lookup"><span data-stu-id="448a4-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Diferencia de Flexbox en propiedades CSS y página web resaltada" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="448a4-152">Flexbox `gap` en propiedades CSS y página web resaltadas</span><span class="sxs-lookup"><span data-stu-id="448a4-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="448a4-153">Agregar herramientas rápidamente con el nuevo botón Más herramientas</span><span class="sxs-lookup"><span data-stu-id="448a4-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="448a4-154">Ahora tienes una nueva forma de abrir más herramientas en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="448a4-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="448a4-155">Después de activar este \*\*\*\* experimento, el icono Más herramientas se muestra como un signo más ( ) a la derecha `+` del panel principal.</span><span class="sxs-lookup"><span data-stu-id="448a4-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="448a4-156">Para mostrar una lista de otras herramientas para agregar al panel principal, elija el icono **Más** herramientas \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="448a4-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="448a4-157">Para activar este experimento, [][DevtoolsCustomizeIndexSettings]ve a Experimentos de configuración y, a continuación, selecciona la casilla junto a Habilitar + menús de pestaña de botón  >  \*\*\*\* para abrir **más herramientas.**</span><span class="sxs-lookup"><span data-stu-id="448a4-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Más herramientas resaltadas en DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="448a4-159">**Más herramientas** resaltadas en DevTools</span><span class="sxs-lookup"><span data-stu-id="448a4-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="448a4-160">Las tecnologías de asistencia ahora anuncian la posición y el recuento de sugerencias css</span><span class="sxs-lookup"><span data-stu-id="448a4-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="448a4-161">Cuando edita CSS, obtiene un desplegable de características.</span><span class="sxs-lookup"><span data-stu-id="448a4-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="448a4-162">Esta característica no estaba disponible para los usuarios de tecnologías de asistencia, ya que se anuncia en la versión 89 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="448a4-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="448a4-163">Un usuario de tecnologías de asistencia ahora puede navegar por sugerencias css en el **panel** Estilos.</span><span class="sxs-lookup"><span data-stu-id="448a4-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="448a4-164">En La versión 88 de Microsoft Edge y versiones anteriores, la tecnología de asistencia anunciada como un usuario navegaba por la lista de sugerencias al editar CSS en el panel `Suggestion` Estilos. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="448a4-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="448a4-165">En la versión 89 de Microsoft Edge, un usuario de tecnología de asistencia ahora escucha la posición y el recuento de la sugerencia actual.</span><span class="sxs-lookup"><span data-stu-id="448a4-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="448a4-166">Cada sugerencia se anuncia a medida que el usuario navega por la lista de sugerencias, como sugerencia 3 de 5.</span><span class="sxs-lookup"><span data-stu-id="448a4-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="448a4-167">Para obtener más información sobre cómo escribir CSS en DevTools, vaya [a Cambiar CSS.][DevtoolsCssReferenceChangeCss]</span><span class="sxs-lookup"><span data-stu-id="448a4-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="448a4-168">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1157329.][CR1157329]</span><span class="sxs-lookup"><span data-stu-id="448a4-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<span data-ttu-id="448a4-169">Para ver un vídeo que muestra y lee en voz alta varias sugerencias con este experimento activado, ve a Voiceover anunciando opciones [de devtools](https://youtu.be/9TcUpleEwwA) en YouTube.</span><span class="sxs-lookup"><span data-stu-id="448a4-169">To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.</span></span>  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Sugerencia resaltada en el panel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   <span data-ttu-id="448a4-171">La `suggestion` lista resaltada en el panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="448a4-171">The `suggestion` list highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="448a4-172">Emular Surface Duo y El plegado Desaplicación de Samsung</span><span class="sxs-lookup"><span data-stu-id="448a4-172">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="448a4-173">Prueba la apariencia de tu sitio web o aplicación en los siguientes dispositivos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="448a4-173">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="448a4-174">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="448a4-174">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="448a4-175">Redoblón Desdeso</span><span class="sxs-lookup"><span data-stu-id="448a4-175">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="448a4-176">Active las **características de la plataforma web experimental** para obtener acceso a la nueva característica de pantalla multimedia [CSS][DualScreenWebCssMediaSpanning] y obtener la API de JavaScript de [WindowsSegments.][DualScreenWebJavascriptGetwindowsegments]</span><span class="sxs-lookup"><span data-stu-id="448a4-176">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="448a4-177">Navegue hasta `edge://flags` y cambie la marca junto a las características de la plataforma web **experimental.**</span><span class="sxs-lookup"><span data-stu-id="448a4-177">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="448a4-178">Para ayudar a mejorar tu sitio web o aplicación para la pantalla doble y los dispositivos plegados, usa las siguientes características [al emular el dispositivo.][DevtoolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="448a4-178">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="448a4-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], que es cuando el sitio web \(o app\) aparece en ambas pantallas.</span><span class="sxs-lookup"><span data-stu-id="448a4-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="448a4-180">[Representación de la mosca][DualScreenIntroductionHowToWorkWithSeam], que es el espacio entre las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="448a4-180">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="448a4-181">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1054281][CR1054281].</span><span class="sxs-lookup"><span data-stu-id="448a4-181">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular la pantalla doble" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="448a4-183">Emular la pantalla doble</span><span class="sxs-lookup"><span data-stu-id="448a4-183">Emulate dual-screen</span></span>  
:::image-end:::  

## <span data-ttu-id="448a4-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span><span class="sxs-lookup"><span data-stu-id="448a4-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="448a4-185">Microsoft [Edge Developer Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span><span class="sxs-lookup"><span data-stu-id="448a4-185">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="448a4-186">Microsoft Visual Studio Code actualiza las extensiones automáticamente.</span><span class="sxs-lookup"><span data-stu-id="448a4-186">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="448a4-187">Para actualizar manualmente a la versión 1.1.2, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="448a4-187">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="448a4-188">Se agregó **un botón Cerrar instancia** a cada elemento de la lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span><span class="sxs-lookup"><span data-stu-id="448a4-188">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="448a4-189">Versión mejorada de [Microsoft Edge DevTools][DevtoolsMain] de 84.0.522.63 a [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="448a4-189">Bumped [Microsoft Edge DevTools][DevtoolsMain] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="448a4-190">Depurador [incluido para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como dependencia \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="448a4-190">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="448a4-191">Opción de configuración implementada para cambiar los temas de extensión \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="448a4-191">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="448a4-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="448a4-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <span data-ttu-id="448a4-193">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="448a4-193">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="448a4-194">Captura de pantalla de nodo más allá de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="448a4-194">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="448a4-195">En La versión 89 de Microsoft Edge, las capturas de pantalla de nodo son más precisas, capturando el nodo completo incluso si el contenido del nodo no está visible en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="448a4-195">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="448a4-196">En la **herramienta Elementos,** mantenga el mouse sobre un elemento, abra el menú contextual \(haga clic con el botón secundario\) y elija **Captura de pantalla del nodo**.</span><span class="sxs-lookup"><span data-stu-id="448a4-196">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="448a4-197">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1003629.][CR1003629]</span><span class="sxs-lookup"><span data-stu-id="448a4-197">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de pantalla de nodo resaltada en el menú contextual de la herramienta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="448a4-199">**Captura de pantalla de nodo** resaltada en el menú contextual de la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="448a4-199">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <span data-ttu-id="448a4-200">Actualizaciones de herramientas de elementos</span><span class="sxs-lookup"><span data-stu-id="448a4-200">Elements tool updates</span></span>  

#### <span data-ttu-id="448a4-201">Compatibilidad con la fuerza del estado CSS :target</span><span class="sxs-lookup"><span data-stu-id="448a4-201">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="448a4-202">Ahora puedes usar DevTools para forzar la pseudo-clase CSS [:target.][MdnDocsWebCssTarget]</span><span class="sxs-lookup"><span data-stu-id="448a4-202">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="448a4-203">La pseudo class se desencadena cuando un elemento único \(el elemento de destino\) tiene un fragmento de `:target` `id` la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="448a4-203">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="448a4-204">Por ejemplo, la `http://www.example.com/index.html#section1` dirección URL desencadena la pseudo class en un elemento HTML con `:target` `id="section1"` .</span><span class="sxs-lookup"><span data-stu-id="448a4-204">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="448a4-205">Para probar una demostración con la sección 1 resaltada, vaya a [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span><span class="sxs-lookup"><span data-stu-id="448a4-205">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="448a4-206">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1156628.][CR1156628]</span><span class="sxs-lookup"><span data-stu-id="448a4-206">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Página web resaltada sin CSS forzada" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="448a4-208">Página web resaltada sin CSS forzada</span><span class="sxs-lookup"><span data-stu-id="448a4-208">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forzado y página web resaltada" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="448a4-210">CSS forzada y página web resaltada</span><span class="sxs-lookup"><span data-stu-id="448a4-210">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="448a4-211">Usar elementos duplicados para copiar elementos</span><span class="sxs-lookup"><span data-stu-id="448a4-211">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="448a4-212">Usa el nuevo **acceso directo de elemento duplicado** para clonar un elemento.</span><span class="sxs-lookup"><span data-stu-id="448a4-212">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="448a4-213">En la **herramienta Elementos,** mantenga el mouse sobre un elemento, abra el menú contextual \(haga clic con el botón secundario\), elija **Duplicar elemento**.</span><span class="sxs-lookup"><span data-stu-id="448a4-213">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="448a4-214">Se crea un nuevo elemento en el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="448a4-214">A new element is created under the selected element.</span></span>  <span data-ttu-id="448a4-215">Para duplicar el elemento con un método abreviado de teclado, selecciona `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) o `Shift` + `Option` + `Down Arrow` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="448a4-215">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="448a4-216">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1150797.][CR1150797]</span><span class="sxs-lookup"><span data-stu-id="448a4-216">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="El elemento Duplicado se resalta en el menú contextual de un elemento de la herramienta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="448a4-218">El **elemento Duplicado** se resalta en el menú contextual de un elemento de la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="448a4-218">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-219">Selectores de colores para propiedades CSS personalizadas</span><span class="sxs-lookup"><span data-stu-id="448a4-219">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="448a4-220">El **panel Estilos** ahora muestra los selectores de color para las propiedades CSS personalizadas.</span><span class="sxs-lookup"><span data-stu-id="448a4-220">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="448a4-221">Para recorrer los formatos RGBA, HSLA y Hexadecimal del valor de color, mantenga presionado y `Shift` elija el selector de color.</span><span class="sxs-lookup"><span data-stu-id="448a4-221">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="448a4-222">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1147016.][CR1147016]</span><span class="sxs-lookup"><span data-stu-id="448a4-222">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Selectores de colores para propiedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="448a4-224">Selectores de colores para propiedades CSS personalizadas</span><span class="sxs-lookup"><span data-stu-id="448a4-224">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-225">Copiar clases y propiedades CSS</span><span class="sxs-lookup"><span data-stu-id="448a4-225">Copy CSS classes and properties</span></span>  

<span data-ttu-id="448a4-226">Ahora puede copiar las propiedades CSS más rápido con algunas opciones nuevas en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="448a4-226">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="448a4-227">En la **herramienta Elementos,** elija un elemento.</span><span class="sxs-lookup"><span data-stu-id="448a4-227">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="448a4-228">Para copiar el valor, en el panel Estilos, mantenga el mouse sobre una clase CSS o una propiedad CSS, abra un menú contextual \(haga clic con el botón secundario\) y elija la opción de copia. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="448a4-228">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="448a4-229">Opciones de copia para una clase CSS.</span><span class="sxs-lookup"><span data-stu-id="448a4-229">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="448a4-230">Opción</span><span class="sxs-lookup"><span data-stu-id="448a4-230">Option</span></span> | <span data-ttu-id="448a4-231">Detalles</span><span class="sxs-lookup"><span data-stu-id="448a4-231">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="448a4-232">Selector de copia</span><span class="sxs-lookup"><span data-stu-id="448a4-232">Copy selector</span></span>** | <span data-ttu-id="448a4-233">Copie el nombre del selector actual.</span><span class="sxs-lookup"><span data-stu-id="448a4-233">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="448a4-234">Regla de copia</span><span class="sxs-lookup"><span data-stu-id="448a4-234">Copy rule</span></span>** | <span data-ttu-id="448a4-235">Copie la regla del selector actual.</span><span class="sxs-lookup"><span data-stu-id="448a4-235">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="448a4-236">Copiar todas las declaraciones</span><span class="sxs-lookup"><span data-stu-id="448a4-236">Copy all declarations</span></span>** | <span data-ttu-id="448a4-237">Copie todas las declaraciones en la regla actual, incluidas las propiedades no válidas y con prefijo.</span><span class="sxs-lookup"><span data-stu-id="448a4-237">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="448a4-238">Opciones de copia de una propiedad CSS.</span><span class="sxs-lookup"><span data-stu-id="448a4-238">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="448a4-239">Opción</span><span class="sxs-lookup"><span data-stu-id="448a4-239">Option</span></span> | <span data-ttu-id="448a4-240">Detalles</span><span class="sxs-lookup"><span data-stu-id="448a4-240">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="448a4-241">Copiar declaración</span><span class="sxs-lookup"><span data-stu-id="448a4-241">Copy declaration</span></span>** | <span data-ttu-id="448a4-242">Copie la declaración de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="448a4-242">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="448a4-243">Copy (propiedad)</span><span class="sxs-lookup"><span data-stu-id="448a4-243">Copy property</span></span>** | <span data-ttu-id="448a4-244">Copie la propiedad de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="448a4-244">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="448a4-245">Valor de copia</span><span class="sxs-lookup"><span data-stu-id="448a4-245">Copy value</span></span>** | <span data-ttu-id="448a4-246">Copie el valor de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="448a4-246">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Opciones de copia para una clase CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="448a4-248">Opciones de copia para una clase CSS en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="448a4-248">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opciones de copia de una propiedad CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="448a4-250">Opciones de copia de una propiedad CSS en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="448a4-250">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="448a4-251">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1152391.][CR1152391]</span><span class="sxs-lookup"><span data-stu-id="448a4-251">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <span data-ttu-id="448a4-252">Actualizaciones de cookies</span><span class="sxs-lookup"><span data-stu-id="448a4-252">Cookies updates</span></span>  

#### <span data-ttu-id="448a4-253">Nueva opción para mostrar cookies descodificadas por URL</span><span class="sxs-lookup"><span data-stu-id="448a4-253">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="448a4-254">Ahora puede optar por mostrar el valor de cookies descodificadas por URL en el **panel Cookies.**</span><span class="sxs-lookup"><span data-stu-id="448a4-254">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="448a4-255">Para mostrar la cookie descodificada, vaya al panel \*\*\*\* Cookies de aplicación, elija cualquier cookie de la lista y seleccione la casilla situada junto a  >  \*\*\*\* Mostrar url **descodificada.**</span><span class="sxs-lookup"><span data-stu-id="448a4-255">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="448a4-256">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [997625.][CR997625]</span><span class="sxs-lookup"><span data-stu-id="448a4-256">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opción para mostrar cookies descodificadas por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="448a4-258">Opción para mostrar cookies descodificadas de url</span><span class="sxs-lookup"><span data-stu-id="448a4-258">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-259">Filtrar y borrar las cookies visibles</span><span class="sxs-lookup"><span data-stu-id="448a4-259">Filter and clear visible cookies</span></span>  

<span data-ttu-id="448a4-260">En Microsoft Edge versión 88 \*\*\*\* o anterior, la herramienta de aplicación solo proporcionaba una forma de borrar todas las cookies con el botón Borrar **todas las cookies.**</span><span class="sxs-lookup"><span data-stu-id="448a4-260">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="448a4-261">En La versión 89 de Microsoft Edge, ahora puede elegir Borrar **cookies** filtradas para eliminar solo las cookies filtradas.</span><span class="sxs-lookup"><span data-stu-id="448a4-261">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="448a4-262">Para filtrar las cookies, vaya **a**  >  **Cookies de**aplicación y escriba el **cuadro de texto** Filtro.</span><span class="sxs-lookup"><span data-stu-id="448a4-262">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="448a4-263">Para eliminar las cookies mostradas, elija el botón Borrar **cookies filtradas.**</span><span class="sxs-lookup"><span data-stu-id="448a4-263">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="448a4-264">Para mostrar todas las demás cookies, borre el texto del filtro.</span><span class="sxs-lookup"><span data-stu-id="448a4-264">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="448a4-265">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [978059][CR978059].</span><span class="sxs-lookup"><span data-stu-id="448a4-265">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Borrar solo las cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="448a4-267">Borrar solo las cookies visibles</span><span class="sxs-lookup"><span data-stu-id="448a4-267">Clear only visible cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-268">Nueva opción para borrar cookies de terceros en el panel almacenamiento</span><span class="sxs-lookup"><span data-stu-id="448a4-268">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="448a4-269">DevTools ahora borra solo las cookies de origen de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="448a4-269">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="448a4-270">Para borrar solo los datos del sitio \*\*\*\* web y las cookies de origen, vaya a Almacenamiento de aplicaciones y, a continuación,  >  \*\*\*\* elija Borrar datos **del sitio.**</span><span class="sxs-lookup"><span data-stu-id="448a4-270">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="448a4-271">Para borrar los datos del sitio web y todas las cookies, vaya **a Almacenamiento de**  >  **aplicaciones.**</span><span class="sxs-lookup"><span data-stu-id="448a4-271">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="448a4-272">Seleccione la casilla situada junto a **la inclusión de cookies de**terceros y, a continuación, elija Borrar datos del **sitio.**</span><span class="sxs-lookup"><span data-stu-id="448a4-272">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="448a4-273">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1012337][CR1012337].</span><span class="sxs-lookup"><span data-stu-id="448a4-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opción para borrar cookies de terceros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="448a4-275">Opción para borrar cookies de terceros</span><span class="sxs-lookup"><span data-stu-id="448a4-275">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <span data-ttu-id="448a4-276">Actualizaciones de herramientas de red</span><span class="sxs-lookup"><span data-stu-id="448a4-276">Network tool updates</span></span>  

#### <span data-ttu-id="448a4-277">Configuración de registro de red de registro de registro persistente</span><span class="sxs-lookup"><span data-stu-id="448a4-277">Persist Record network log setting</span></span>  

<span data-ttu-id="448a4-278">En Microsoft Edge versión 88 o anterior, DevTools restablece la configuración de registro de red **de** registro cuando se actualiza una página web.</span><span class="sxs-lookup"><span data-stu-id="448a4-278">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="448a4-279">En La versión 89 de Microsoft Edge, DevTools ahora conserva la configuración de registro de **red de** registro.</span><span class="sxs-lookup"><span data-stu-id="448a4-279">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="448a4-280">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1122580][CR1122580].</span><span class="sxs-lookup"><span data-stu-id="448a4-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registro de registro de red" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="448a4-282">Registro de registro de red</span><span class="sxs-lookup"><span data-stu-id="448a4-282">Record network log</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-283">La opción en línea ahora no es ninguna opción de limitación</span><span class="sxs-lookup"><span data-stu-id="448a4-283">Online option is now No throttling option</span></span>  

<span data-ttu-id="448a4-284">La opción de emulación de red **Online** ahora se ha cambiado a **Sin limitación.**</span><span class="sxs-lookup"><span data-stu-id="448a4-284">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="448a4-285">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1028078.][CR1028078]</span><span class="sxs-lookup"><span data-stu-id="448a4-285">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Sin opción de limitación" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="448a4-287">**Sin opción de limitación**</span><span class="sxs-lookup"><span data-stu-id="448a4-287">**No throttling** option</span></span>  
:::image-end:::  

### <span data-ttu-id="448a4-288">Nuevas opciones de copia en la herramienta Consola, la herramienta Orígenes y el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="448a4-288">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <span data-ttu-id="448a4-289">Copiar objeto en la herramienta Consola y orígenes</span><span class="sxs-lookup"><span data-stu-id="448a4-289">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="448a4-290">Ahora puede copiar los valores de objeto en las **herramientas Consola** **y** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="448a4-290">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="448a4-291">La capacidad de copiar valores de objeto es útil cuando se trabaja con objetos grandes.</span><span class="sxs-lookup"><span data-stu-id="448a4-291">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="448a4-292">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a los problemas [1148353][CR1148353] y [1149859][CR1149859].</span><span class="sxs-lookup"><span data-stu-id="448a4-292">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="448a4-293">En la **herramienta Consola,** mantenga el mouse sobre un objeto, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, **elija Copiar objeto**.</span><span class="sxs-lookup"><span data-stu-id="448a4-293">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="448a4-294">En \*\*\*\* la herramienta Orígenes, en un punto de \*\*\*\* interrupción, mantenga el mouse sobre un objeto, en la ventana emergente Objeto, resalte un objeto, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, elija **Copiar objeto**.</span><span class="sxs-lookup"><span data-stu-id="448a4-294">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copiar objeto en la consola" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="448a4-296">Copiar objeto en la **consola**</span><span class="sxs-lookup"><span data-stu-id="448a4-296">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copiar objeto en orígenes" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="448a4-298">Copiar objeto en **orígenes**</span><span class="sxs-lookup"><span data-stu-id="448a4-298">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="448a4-299">Copiar el nombre de archivo en la herramienta Orígenes y en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="448a4-299">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="448a4-300">Ahora puede copiar un nombre de archivo mediante el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="448a4-300">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="448a4-301">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a Problemas [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="448a4-301">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="448a4-302">En la **herramienta Orígenes,** mantenga el mouse sobre un nombre de archivo, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, **elija Copiar nombre de archivo**.</span><span class="sxs-lookup"><span data-stu-id="448a4-302">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="448a4-303">En la **herramienta Elementos** > **panel** Estilos, mantenga el mouse sobre un nombre de archivo, abra el menú contextual \(right-click\) y, a continuación, elija Copiar nombre **de archivo**.</span><span class="sxs-lookup"><span data-stu-id="448a4-303">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar el nombre de archivo en Orígenes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="448a4-305">Copiar el nombre de archivo en **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="448a4-305">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar nombre de archivo en el panel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="448a4-307">Copiar nombre de archivo en el **panel Estilos**</span><span class="sxs-lookup"><span data-stu-id="448a4-307">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="448a4-308">Actualizaciones de detalles de Frame</span><span class="sxs-lookup"><span data-stu-id="448a4-308">Updates to Frame details</span></span>  

#### <span data-ttu-id="448a4-309">Información de los trabajadores de servicio en los detalles de Frame</span><span class="sxs-lookup"><span data-stu-id="448a4-309">Service Workers information in Frame details</span></span>  

<span data-ttu-id="448a4-310">DevTools ahora muestra un trabajador de servicio dedicado en el marco primario.</span><span class="sxs-lookup"><span data-stu-id="448a4-310">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="448a4-311">En la figura siguiente, se muestran los detalles del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="448a4-311">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="448a4-312">Para mostrar los detalles del trabajador del servicio, vaya a **Trabajadores de**servicio de marcos de  >  \*\*\*\*  >  `top`  >  \*\*\*\* aplicación y, a continuación, elija un trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="448a4-312">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="448a4-313">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1122507.][CR1122507]</span><span class="sxs-lookup"><span data-stu-id="448a4-313">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Información de los trabajadores de servicio en los detalles de marcos" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="448a4-315">**Información de los trabajadores** de servicio en los **detalles de marcos**</span><span class="sxs-lookup"><span data-stu-id="448a4-315">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-316">Medir la información de memoria en detalles del marco</span><span class="sxs-lookup"><span data-stu-id="448a4-316">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="448a4-317">El `performance.measureMemory()` estado de la API ahora se muestra en la sección de disponibilidad de la **API.**</span><span class="sxs-lookup"><span data-stu-id="448a4-317">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="448a4-318">La nueva `performance.measureMemory()` API calcula el uso de memoria de toda la página web.</span><span class="sxs-lookup"><span data-stu-id="448a4-318">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="448a4-319">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1139899.][CR1139899]</span><span class="sxs-lookup"><span data-stu-id="448a4-319">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memoria" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="448a4-321">Medir memoria</span><span class="sxs-lookup"><span data-stu-id="448a4-321">Measure Memory</span></span>  
:::image-end:::  

### <span data-ttu-id="448a4-322">Fotogramas descartados en la herramienta Rendimiento</span><span class="sxs-lookup"><span data-stu-id="448a4-322">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="448a4-323">Al analizar [el rendimiento de carga en la herramienta Rendimiento,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]la sección **Marcos** marca ahora los marcos descartados como rojo.</span><span class="sxs-lookup"><span data-stu-id="448a4-323">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="448a4-324">Para mostrar la velocidad de fotogramas, mantenga el puntero sobre un fotograma descartado.</span><span class="sxs-lookup"><span data-stu-id="448a4-324">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="448a4-325">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1075865][CR1075865].</span><span class="sxs-lookup"><span data-stu-id="448a4-325">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Fotogramas descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="448a4-327">Fotogramas descartados</span><span class="sxs-lookup"><span data-stu-id="448a4-327">Dropped frames</span></span>  
:::image-end:::  

#### <span data-ttu-id="448a4-328">Nuevo cálculo de contraste de color: algoritmo de contraste perceptivo avanzado (APCA)</span><span class="sxs-lookup"><span data-stu-id="448a4-328">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="448a4-329">El [algoritmo de contraste perceptual avanzado (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] reemplaza la relación de contraste de las directrices [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] en el [selector de colores.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]</span><span class="sxs-lookup"><span data-stu-id="448a4-329">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="448a4-330">APCA es una nueva forma de calcular el contraste.</span><span class="sxs-lookup"><span data-stu-id="448a4-330">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="448a4-331">Se basa en la investigación moderna sobre la percepción del color.</span><span class="sxs-lookup"><span data-stu-id="448a4-331">It is based on modern research on color perception.</span></span>  <span data-ttu-id="448a4-332">En comparación con las directrices AA/AAA, APCA depende más del contexto.</span><span class="sxs-lookup"><span data-stu-id="448a4-332">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="448a4-333">El contraste se calcula en función de las siguientes propiedades espaciales del texto, el color y el contexto.</span><span class="sxs-lookup"><span data-stu-id="448a4-333">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="448a4-334">Propiedades espaciales del texto que incluyen el grosor y el tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="448a4-334">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="448a4-335">Propiedades espaciales de color que incluyen contraste percibido entre texto y fondo.</span><span class="sxs-lookup"><span data-stu-id="448a4-335">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="448a4-336">Propiedades espaciales de contexto que incluyen luz ambiental, entorno y propósito previsto.</span><span class="sxs-lookup"><span data-stu-id="448a4-336">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="448a4-337">Para activar este experimento, [][DevtoolsCustomizeIndexSettings]ve a Experimentos de configuración y elige la casilla junto a Habilitar el nuevo algoritmo de contraste perceptual avanzado (APCA) que reemplaza la relación de contraste anterior y las directrices  >  \*\*\*\* **AA/AAA.**</span><span class="sxs-lookup"><span data-stu-id="448a4-337">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="448a4-338">Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [1121900][CR1121900].</span><span class="sxs-lookup"><span data-stu-id="448a4-338">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA en el selector de colores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="448a4-340">APCA en el selector de colores</span><span class="sxs-lookup"><span data-stu-id="448a4-340">APCA in the Color Picker</span></span>  
:::image-end:::  

## <span data-ttu-id="448a4-341">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="448a4-341">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="448a4-342">Si está en Windows, Linux o macOS, considere la posibilidad de usar los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="448a4-342">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="448a4-343">Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="448a4-343">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="448a4-344">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="448a4-344">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Ver la relación de contraste de un elemento de texto en el selector de colores: referencia de accesibilidad | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Cambiar CSS: referencia css | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en las DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de doble pantalla y plegado: emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular una ventanilla móvil: emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Rendimiento de carga de registros: referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Edite la configuración y los estilos de fuente CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Introducción a las herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la seam: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla multimedia CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Sección 1: demostración css :target para novedades de DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementing dropdown in settings to change themes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Including Debugger for Microsoft Edge as a dependency | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrading Edge DevTools version to 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Add single close buttons to instances panel | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Seleccione las características de fuente y los colores de fondo para proporcionar suficiente contraste para la legibilidad | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos de confianza | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nueva versión de Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Catálogo de soluciones de | Visual Studio código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador de microsoft edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: Eliminar cookies al filtrarlas, eliminar todas las cookies no solo las filtradas | Errores de Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Nueva solicitud de | Opción de necesidad para ver el valor descodificado de url en las cookies | Errores de Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: Capture Node ya no captura de pantalla el nodo debajo del plegado. | Errores de Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: Borrar datos del sitio destruye la sesión de Google en sitios que no son de Google | Errores de Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: Poner en línea y sin conexión entre sí en la lista | Errores de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitud de característica: DevTools debe emular dispositivos de doble pantalla y plegados | Errores de Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: Mostrar fotogramas descartados en la escala de tiempo de las devtools | Errores de Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: ofrecer una interfaz de usuario de editor de tipo de letra especializada | Errores de Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: actualizar la lógica de cálculo de contraste por cada nueva especificación | Errores de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: información de los trabajos superficiales en la vista de árbol de marcos | Errores de Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: Imposible deshabilitar la grabación de red al volver a cargar | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: herramientas de la caja flexible | Errores de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: informar la disponibilidad de la API validada en la vista detalles del marco | Errores de Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: Superposición de Flexbox | Errores de Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: El selector de colores no se muestra en la función var(). | Errores de Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: Solicitud de característica: Copiar objeto desde la consola de devtools | Errores de Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitud de característica][Consola] agregar objeto de copia al elemento del Portapapeles al menú contextual | Errores de Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: Agregar menú contextual de elemento duplicado en el panel de | Errores de Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: Compatibilidad con copiar el menú contextual CSS en el panel de estilos | Errores de Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Support copy file name and line number | Errores de Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: agregar compatibilidad para la característica de estado de elemento :target in force | Errores de Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Accesibilidad - Narrador: Narrador no anuncia el recuento y la posición de las sugerencias disponibles para el código en la pestaña Estilos | Errores de Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "| Samsung (Ee. UU.)"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (mejorado): cómo reunirse con WCAG (referencia rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo): cómo reunirse con WCAG (referencia rápida) | W3C"  

> [!NOTE]
> <span data-ttu-id="448a4-399">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="448a4-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="448a4-400">La página original se encuentra [aquí](https://developers.google.com/web/updates/2021/01/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="448a4-400">The original page is found [here](https://developers.google.com/web/updates/2021/01/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="448a4-402">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="448a4-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Marcador de posición de expansión"  
