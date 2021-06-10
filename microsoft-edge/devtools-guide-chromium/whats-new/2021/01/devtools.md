---
description: La herramienta Novedades ahora es Bienvenida, Editor de fuentes visuales en el panel Estilos, herramientas de depuración de CSS Flexbox y más.
title: Novedades de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 9eb9f35427829dbe262b4c71d8ff5474b28eae77
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597158"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a><span data-ttu-id="d6ad5-104">Novedades de DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="d6ad5-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a><span data-ttu-id="d6ad5-105">Novedades ahora es Bienvenida</span><span class="sxs-lookup"><span data-stu-id="d6ad5-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="d6ad5-106">La herramienta **Novedades** en DevTools de Microsoft Edge ahora tiene una nueva apariencia y un nuevo nombre: **Bienvenida**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="d6ad5-107">La herramienta **Bienvenida** sigue mostrando las últimas noticias y actualizaciones de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="d6ad5-108">Ahora también incluye vínculos a la documentación de Microsoft Edge DevTools, otras formas de enviar sus comentarios y mucho más.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="d6ad5-109">Para mostrar la herramienta **Bienvenida** después de cada actualización Microsoft Edge, active la casilla junto a **Abrir pestaña después de cada actualización**, debajo del título.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="d6ad5-110">Para cerrar la herramienta **Bienvenida**, seleccione la **X** en la parte derecha de la pestaña de título.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="d6ad5-111">Si prefiere la herramienta original **Novedades**, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y desactive la casilla junto a **Habilitar pestaña de Bienvenida**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="La herramienta Bienvenida está resaltada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="d6ad5-113">La herramienta **Bienvenida** está resaltada</span><span class="sxs-lookup"><span data-stu-id="d6ad5-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a><span data-ttu-id="d6ad5-114">Editor de fuentes visuales en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="d6ad5-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="d6ad5-115">Cuando trabaje con fuentes en CSS, use el nuevo [Editor de fuentes visuales][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="d6ad5-116">Puede definir las fuentes de reserva y usar los controles deslizantes para definir el grosor, el tamaño, el alto de la línea y el espaciado de la fuente.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="d6ad5-117">El **Editor de fuentes** le ayuda a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="d6ad5-118">Cambiar entre unidades para las diferentes propiedades de la fuente</span><span class="sxs-lookup"><span data-stu-id="d6ad5-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="d6ad5-119">Cambiar entre palabras clave para las diferentes propiedades de la fuente</span><span class="sxs-lookup"><span data-stu-id="d6ad5-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="d6ad5-120">Convertir unidades</span><span class="sxs-lookup"><span data-stu-id="d6ad5-120">Convert units</span></span>  
*   <span data-ttu-id="d6ad5-121">Generar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="d6ad5-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="d6ad5-122">Para activar este experimento, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y active la casilla junto a **Habilitar las herramientas del nuevo Editor de fuentes en el panel Estilos**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="d6ad5-123">Para obtener más información, vaya a [Editar la configuración y los estilos de fuente CSS en el panel Estilos, en DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="d6ad5-124">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1093229][CR1093229].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="El Editor de fuentes visual está resaltado en el panel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="d6ad5-126">El **Editor de fuentes** visual está resaltado en el panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a><span data-ttu-id="d6ad5-127">Herramientas de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="d6ad5-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="d6ad5-128">Las características de depuración de Flexbox están en desarrollo activo.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="d6ad5-129">Para activar el experimento de las dos características siguientes, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y active la casilla junto a **Habilitar las nuevas características de depuración de CSS Flexbox**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="d6ad5-130">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a los problemas [1136394][CR1136394] y [1139949][CR1139949].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a><span data-ttu-id="d6ad5-131">El nuevo icono de Flexbox (flex) le ayuda a identificar y a visualizar los contenedores flexibles.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-131">New Flexbox (flex) icon helps identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="d6ad5-132">En la herramienta **Elementos**, el nuevo icono de Flexbox (flex) le ayuda a identificar los contenedores de Flexbox en el código.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="d6ad5-133">Seleccione el icono de Flexbox \(flex\) para activar o desactivar el efecto de superposición que resalta al contenedor de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="d6ad5-134">Puede personalizar el color de la superposición en el panel **Diseño**, que se encuentra junto a **Estilos** y **Calculado**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d6ad5-135">Para activar y desactivar el efecto de superposición que resalta al contenedor de Flexbox, seleccione el icono de Flexbox \(`flex`\).</span><span class="sxs-lookup"><span data-stu-id="d6ad5-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d6ad5-136">Puede personalizar el color de la superposición en el panel **Diseño**, junto a **Estilos** y **Calculado**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Icono de Flexbox (flex) y página web resaltados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="d6ad5-138">Icono de **Flexbox** \(`flex`\) y página web resaltados</span><span class="sxs-lookup"><span data-stu-id="d6ad5-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Flexbox se superpone cuando se resalta en el panel Diseño" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="d6ad5-140">Las **superposiciones de Flexbox** se resaltan en el panel de **Diseño**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-visual-guides-when-flexbox-layouts-change-using-css-properties"></a><span data-ttu-id="d6ad5-141">Mostrar los iconos de alineación y las guías visuales cuando los diseños de Flexbox cambien mediante propiedades CSS</span><span class="sxs-lookup"><span data-stu-id="d6ad5-141">Display alignment icons and visual guides when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and visual guides for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="d6ad5-142">Cuando edita CSS para su diseño de Flexbox, CSS se autocompleta en el panel **Estilos** y muestra iconos útiles junto a las propiedades relevantes de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="d6ad5-143">Para probar esta nueva característica, abra la herramienta **Elementos** y seleccione un contenedor flexible.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="d6ad5-144">Luego, agregue o cambie alguna propiedad en ese contenedor en el panel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d6ad5-145">En el menú Autocompletar ahora se muestran iconos que indican el efecto de las propiedades de alineación, como `align-content` y `align-items`.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d6ad5-146">Además, DevTools ahora muestra una línea de guía para ayudarle a revisar mejor la propiedad CSS `align-items`.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="d6ad5-147">La propiedad CSS `gap` también es compatible.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="d6ad5-148">En la siguiente ilustración, la propiedad CSS `gap` está establecida en `gap: 12px;` y se muestra el patrón de sombreado para cada separación.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menú Autocompletar resaltado para las propiedades CSS que comienzan con alinear" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="d6ad5-150">Menú Autocompletar resaltado para las propiedades CSS que comienzan con</span><span class="sxs-lookup"><span data-stu-id="d6ad5-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Separación de Flexbox en las propiedades CSS y página web resaltadas" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="d6ad5-152">Flexbox `gap` en las propiedades CSS y página web resaltados</span><span class="sxs-lookup"><span data-stu-id="d6ad5-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a><span data-ttu-id="d6ad5-153">Agregar herramientas rápidamente con el nuevo botón Más herramientas</span><span class="sxs-lookup"><span data-stu-id="d6ad5-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="d6ad5-154">Ahora tiene una nueva forma de abrir más herramientas en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="d6ad5-155">Después de activar este experimento, el icono **Más herramientas** se muestra como un signo más (`+`) a la derecha del panel principal.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="d6ad5-156">Para mostrar una lista de otras herramientas para agregar al panel principal, seleccione el icono **Más herramientas** \(`+`\).</span><span class="sxs-lookup"><span data-stu-id="d6ad5-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="d6ad5-157">Para activar este experimento, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y luego, active la casilla junto a **Habilitar menús de la pestaña del botón + para abrir más herramientas**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Más herramientas resaltadas en DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="d6ad5-159">**Más herramientas** resaltadas de DevTools</span><span class="sxs-lookup"><span data-stu-id="d6ad5-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a><span data-ttu-id="d6ad5-160">Las tecnologías de asistencia ahora anuncian la posición y el recuento de sugerencias de CSS</span><span class="sxs-lookup"><span data-stu-id="d6ad5-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="d6ad5-161">Al editar CSS, obtendrá una lista desplegable de características.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="d6ad5-162">Esta característica no estaba disponible para los usuarios de tecnologías de asistencia, ya que se anuncia en la versión 89 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="d6ad5-163">El usuario de tecnologías de asistencia ahora puede navegar por las sugerencias de CSS en el panel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="d6ad5-164">En la versión 88 de Microsoft Edge y en las versiones anteriores, la tecnología de asistencia anuncia `Suggestion` como un usuario que navega por la lista de sugerencias al editar CSS en el panel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="d6ad5-165">En la versión 89 de Microsoft Edge, el usuario de tecnologías de asistencia ahora escuchará la posición y el recuento de la sugerencia actual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="d6ad5-166">Cada sugerencia se anuncia a medida que el usuario navega por la lista de sugerencias, como Sugerencia 3 de 5.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="d6ad5-167">Para obtener más información sobre cómo escribir CSS en DevTools, vaya a [Cambiar CSS][DevtoolsCssReferenceChangeCss].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="d6ad5-168">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1157329][CR1157329].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<span data-ttu-id="d6ad5-169">Para ver un vídeo que muestra y lee en voz alta varias sugerencias con este experimento activado, vaya a [Opciones de devtools anunciadas por VoiceOver](https://youtu.be/9TcUpleEwwA) en YouTube.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-169">To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.</span></span>  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Sugerencia resaltada en el panel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   <span data-ttu-id="d6ad5-171">Lista `suggestion` resaltada en el panel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-171">The `suggestion` list highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="d6ad5-172">Emular Surface Duo y Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="d6ad5-172">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="d6ad5-173">Pruebe la apariencia de su sitio web o aplicación en los siguientes dispositivos en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-173">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="d6ad5-174">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="d6ad5-174">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="d6ad5-175">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="d6ad5-175">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="d6ad5-176">Active las **Características experimentales de la plataforma web** para acceder a la nueva [Característica para expandir la pantalla de los medios CSS][DualScreenWebCssMediaSpanning] y a la [API de JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-176">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="d6ad5-177">Vaya a `edge://flags` y cambie la marca junto a las **Características de la plataforma web experimental**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-177">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="d6ad5-178">Para ayudar a mejorar su sitio web o aplicación para dispositivos plegables y de pantalla doble, use las siguientes características al [emular el dispositivo][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-178">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="d6ad5-179">[Expandir][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], que es cuando su sitio web \(o aplicación\) se extiende por las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="d6ad5-180">[Representación de la unión][DualScreenIntroductionHowToWorkWithSeam], que es el espacio entre las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-180">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="d6ad5-181">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1054281][CR1054281].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-181">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular la pantalla doble" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="d6ad5-183">Emular la pantalla doble</span><span class="sxs-lookup"><span data-stu-id="d6ad5-183">Emulate dual-screen</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a><span data-ttu-id="d6ad5-184">Herramientas para desarrollador de Microsoft Edge para Visual Studio Code versión 1.1.2</span><span class="sxs-lookup"><span data-stu-id="d6ad5-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="d6ad5-185">La versión de extensión 1.1.2 de las [Herramientas de desarrollador de Microsoft Edge para Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] para Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-185">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="d6ad5-186">Microsoft Visual Studio Code actualiza las extensiones automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-186">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="d6ad5-187">Para actualizar manualmente a la versión 1.1.2, vaya a [Actualizar extensión manualmente][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-187">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="d6ad5-188">Se agregó un botón de **Instancia de cierre** a cada elemento de la lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span><span class="sxs-lookup"><span data-stu-id="d6ad5-188">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="d6ad5-189">Cambio de [Microsoft Edge DevTools][DevtoolsIndex] de la versión 84.0.522.63 a la [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="d6ad5-189">Bumped [Microsoft Edge DevTools][DevtoolsIndex] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="d6ad5-190">Se incluye el [Depurador para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como dependencia \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="d6ad5-190">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="d6ad5-191">Se implementó la opción de configuración para cambiar los temas de la extensión \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="d6ad5-191">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="d6ad5-192">Puede archivar los problemas y contribuir con la extensión en el [repositorio de GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="d6ad5-193">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="d6ad5-193">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a><span data-ttu-id="d6ad5-194">Capturar nodo como captura de pantalla más allá de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="d6ad5-194">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="d6ad5-195">En la versión 89 de Microsoft Edge, la captura de nodos como captura de pantalla es más precisa, capturando el nodo completo incluso si su contenido no es visible en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-195">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="d6ad5-196">En la herramienta **Elementos**, mantenga el puntero sobre un elemento, abra el menú contextual \(clic con el botón derecho\) y seleccione **Capturar nodo como captura de pantalla**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-196">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="d6ad5-197">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1003629][CR1003629].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-197">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de nodo como captura de pantalla resaltado en el menú contextual de la herramienta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="d6ad5-199">**Captura de nodo como captura de pantalla** resaltado en el menú contextual en la herramienta **Elementos**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-199">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="d6ad5-200">Actualizaciones de la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="d6ad5-200">Elements tool updates</span></span>  

#### <a name="support-forcing-the-target-css-state"></a><span data-ttu-id="d6ad5-201">Compatibilidad para forzar el estado CSS :target</span><span class="sxs-lookup"><span data-stu-id="d6ad5-201">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="d6ad5-202">Ahora puede usar DevTools para forzar la seudoclase CSS [:target][MdnDocsWebCssTarget].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-202">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="d6ad5-203">La seudoclase `:target` se desencadena cuando un elemento único \(el elemento de destino\) tiene un `id` que coincide con un fragmento de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-203">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="d6ad5-204">Por ejemplo, la dirección URL `http://www.example.com/index.html#section1` activa la seudoclase `:target` en un elemento HTML con `id="section1"`.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-204">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="d6ad5-205">Para probar una demostración con la sección 1 resaltada, vaya a [demostración de CSS :target][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-205">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="d6ad5-206">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1156628][CR1156628].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-206">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Página web resaltada sin forzar CSS" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="d6ad5-208">Página web resaltada sin forzar CSS</span><span class="sxs-lookup"><span data-stu-id="d6ad5-208">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text="CSS :target forzado y página web resaltados" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="d6ad5-210">CSS forzado y página web resaltada</span><span class="sxs-lookup"><span data-stu-id="d6ad5-210">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a><span data-ttu-id="d6ad5-211">Usar Duplicar elementos para copiar elementos</span><span class="sxs-lookup"><span data-stu-id="d6ad5-211">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="d6ad5-212">Use el nuevo acceso directo **Duplicar elemento** para clonar un elemento.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-212">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="d6ad5-213">En la herramienta **Elementos**, mantenga el puntero sobre un elemento, abra el menú contextual \(clic con el botón derecho\) y elija **Duplicar elemento**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-213">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="d6ad5-214">Se creará un nuevo elemento en el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-214">A new element is created under the selected element.</span></span>  <span data-ttu-id="d6ad5-215">Para duplicar el elemento con un método abreviado de teclado, seleccione `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) o `Shift`+`Option`+`Down Arrow` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="d6ad5-215">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="d6ad5-216">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1150797][CR1150797].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-216">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Duplicar elemento se resalta en el menú contextual de un elemento de la herramienta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="d6ad5-218">**Duplicar elemento** se resalta en el menú contextual en un elemento de la herramienta **Elementos**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-218">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a><span data-ttu-id="d6ad5-219">Selector de colores para las propiedades CSS personalizadas</span><span class="sxs-lookup"><span data-stu-id="d6ad5-219">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="d6ad5-220">El panel **Estilos** ahora muestra selectores de color para las propiedades CSS personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-220">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="d6ad5-221">Para cambiar entre los formatos RGBA, HSLA y Hex del valor de color, mantenga presionado `Shift` y elija el Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-221">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="d6ad5-222">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1147016][CR1147016].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-222">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Selector de colores para las propiedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="d6ad5-224">Selector de colores para las propiedades CSS personalizadas</span><span class="sxs-lookup"><span data-stu-id="d6ad5-224">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a><span data-ttu-id="d6ad5-225">Copiar las clases y propiedades CSS</span><span class="sxs-lookup"><span data-stu-id="d6ad5-225">Copy CSS classes and properties</span></span>  

<span data-ttu-id="d6ad5-226">Ahora puede copiar las propiedades CSS más rápidamente con algunas opciones nuevas en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-226">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="d6ad5-227">En la herramienta **Elementos**, elija un elemento.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-227">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="d6ad5-228">Para copiar el valor, en el panel **Estilos**, mantenga el puntero sobre una clase o propiedad CSS, abra un menú contextual \(clic con el botón derecho\) y elija la opción de copiar.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-228">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d6ad5-229">Opciones de copia para una clase CSS.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-229">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="d6ad5-230">Opción</span><span class="sxs-lookup"><span data-stu-id="d6ad5-230">Option</span></span> | <span data-ttu-id="d6ad5-231">Detalles</span><span class="sxs-lookup"><span data-stu-id="d6ad5-231">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="d6ad5-232">Selector de copia</span><span class="sxs-lookup"><span data-stu-id="d6ad5-232">Copy selector</span></span>** | <span data-ttu-id="d6ad5-233">Copiar el nombre del selector actual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-233">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="d6ad5-234">Copiar regla</span><span class="sxs-lookup"><span data-stu-id="d6ad5-234">Copy rule</span></span>** | <span data-ttu-id="d6ad5-235">Copiar la regla del selector actual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-235">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="d6ad5-236">Copiar todas las declaraciones</span><span class="sxs-lookup"><span data-stu-id="d6ad5-236">Copy all declarations</span></span>** | <span data-ttu-id="d6ad5-237">Copiar todas las declaraciones en la regla actual, incluidas las propiedades no válidas y con prefijo.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-237">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d6ad5-238">Opciones de copia para una propiedad CSS.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-238">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="d6ad5-239">Opción</span><span class="sxs-lookup"><span data-stu-id="d6ad5-239">Option</span></span> | <span data-ttu-id="d6ad5-240">Detalles</span><span class="sxs-lookup"><span data-stu-id="d6ad5-240">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="d6ad5-241">Copiar declaración</span><span class="sxs-lookup"><span data-stu-id="d6ad5-241">Copy declaration</span></span>** | <span data-ttu-id="d6ad5-242">Copia la declaración de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-242">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="d6ad5-243">Copiar propiedad</span><span class="sxs-lookup"><span data-stu-id="d6ad5-243">Copy property</span></span>** | <span data-ttu-id="d6ad5-244">Copia la propiedad de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-244">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="d6ad5-245">Copiar valor</span><span class="sxs-lookup"><span data-stu-id="d6ad5-245">Copy value</span></span>** | <span data-ttu-id="d6ad5-246">Copiar el valor de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-246">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Opciones de copia para una clase CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="d6ad5-248">Opciones de copia para una clase CSS en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="d6ad5-248">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opciones de copia para una propiedad CSS en el menú contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="d6ad5-250">Opciones de copia para una propiedad CSS en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="d6ad5-250">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d6ad5-251">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1152391][CR1152391].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-251">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <a name="cookies-updates"></a><span data-ttu-id="d6ad5-252">Actualizaciones de cookies</span><span class="sxs-lookup"><span data-stu-id="d6ad5-252">Cookies updates</span></span>  

#### <a name="new-option-to-display-url-decoded-cookies"></a><span data-ttu-id="d6ad5-253">Nueva opción para mostrar cookies descodificadas por URL</span><span class="sxs-lookup"><span data-stu-id="d6ad5-253">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="d6ad5-254">Ahora puede optar por mostrar el valor de las cookies descodificadas por URL en el panel **Cookies**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-254">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="d6ad5-255">Para mostrar la cookie descodificada, vaya al panel **Aplicación** > **Cookies**, elija cualquier cookie de la lista y active la casilla junto a **Mostrar dirección URL descodificada**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-255">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="d6ad5-256">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [997625][CR997625].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-256">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opción para mostrar cookies descodificadas por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="d6ad5-258">Opción para mostrar cookies descodificadas por URL</span><span class="sxs-lookup"><span data-stu-id="d6ad5-258">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a><span data-ttu-id="d6ad5-259">Filtrar y borrar las cookies visibles</span><span class="sxs-lookup"><span data-stu-id="d6ad5-259">Filter and clear visible cookies</span></span>  

<span data-ttu-id="d6ad5-260">En la versión 88 de Microsoft Edge o anteriores, la herramienta **Aplicación** solo proporciona una manera de borrar todas las cookies con el botón **Borrar todas las cookies**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-260">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="d6ad5-261">En la versión 89 de Microsoft Edge, ahora puede elegir **Borrar las cookies filtradas** para eliminar solo las cookies filtradas.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-261">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="d6ad5-262">Para filtrar las cookies, vaya a **Aplicación** > **Cookies** y escriba en el cuadro de texto de **Filtrar**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-262">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="d6ad5-263">Para eliminar las cookies mostradas, seleccione el botón **Borrar cookies filtradas**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-263">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="d6ad5-264">Para mostrar las demás cookies, borre el texto del filtro.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-264">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="d6ad5-265">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [978059][CR978059].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-265">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Borrar solo las cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="d6ad5-267">Borrar solo las cookies visibles</span><span class="sxs-lookup"><span data-stu-id="d6ad5-267">Clear only visible cookies</span></span>  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a><span data-ttu-id="d6ad5-268">Nueva opción para borrar cookies de terceros en el panel de Almacenamiento</span><span class="sxs-lookup"><span data-stu-id="d6ad5-268">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="d6ad5-269">Ahora, DevTools solo borrará las cookies de origen de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-269">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="d6ad5-270">Para borrar solo los datos del sitio web y las cookies de origen, vaya a **Aplicación** > **Almacenamiento**y luego, seleccione **Borrar los datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-270">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="d6ad5-271">Para borrar los datos del sitio web y todas las cookies, vaya a **Aplicación** > **Almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-271">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="d6ad5-272">Active la casilla junto a **incluso las cookies de terceros** y luego, **Borrar datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-272">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="d6ad5-273">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1012337][CR1012337].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opción para borrar las cookies de terceros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="d6ad5-275">Opción para borrar las cookies de terceros</span><span class="sxs-lookup"><span data-stu-id="d6ad5-275">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <a name="network-tool-updates"></a><span data-ttu-id="d6ad5-276">Actualizaciones de las herramientas de red</span><span class="sxs-lookup"><span data-stu-id="d6ad5-276">Network tool updates</span></span>  

#### <a name="persist-record-network-log-setting"></a><span data-ttu-id="d6ad5-277">Configuración de registro de red de registro persistente</span><span class="sxs-lookup"><span data-stu-id="d6ad5-277">Persist Record network log setting</span></span>  

<span data-ttu-id="d6ad5-278">En la versión 88 de Microsoft Edge o versiones anteriores, DevTools restablece la configuración **Registro de red de registro** cuando se actualiza una página web.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-278">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="d6ad5-279">En la versión 89 de Microsoft Edge, DevTools conserva la configuración de **Registro de red de registro**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-279">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="d6ad5-280">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1122580][CR1122580].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registro de red de registro" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="d6ad5-282">Registro de red de registro</span><span class="sxs-lookup"><span data-stu-id="d6ad5-282">Record network log</span></span>  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a><span data-ttu-id="d6ad5-283">La opción En línea ahora es la opción Sin limitación</span><span class="sxs-lookup"><span data-stu-id="d6ad5-283">Online option is now No throttling option</span></span>  

<span data-ttu-id="d6ad5-284">La opción de emulación de red **En línea** ahora se denomina **Sin limitación**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-284">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="d6ad5-285">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1028078][CR1028078].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-285">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Opción Sin limitación" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="d6ad5-287">Opción **Sin limitación**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-287">**No throttling** option</span></span>  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a><span data-ttu-id="d6ad5-288">Hay nuevas opciones de copiado en la herramienta Consola, la herramienta Orígenes y el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="d6ad5-288">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <a name="copy-object-in-the-console-and-sources-tool"></a><span data-ttu-id="d6ad5-289">Copiar objeto en las herramientas Consola y Orígenes</span><span class="sxs-lookup"><span data-stu-id="d6ad5-289">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="d6ad5-290">Ahora puede copiar los valores del objeto en las herramientas **Consola** y **Orígenes**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-290">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="d6ad5-291">La capacidad de copiar los valores del objeto es útil cuando se trabaja con objetos grandes.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-291">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="d6ad5-292">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1148353][CR1148353] y [1149859][CR1149859].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-292">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d6ad5-293">En la herramienta **Consola**, mantenga el puntero sobre un objeto, abra el menú contextual \(clic con el botón derecho\) y luego, seleccione **Copiar objeto**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-293">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d6ad5-294">En la herramienta **Orígenes**, en un punto de interrupción, mantenga el puntero sobre un objeto y, en la ventana emergente del **Objeto**, resalte un objeto, abra el menú contextual \(clic con el botón derecho\) y luego, seleccione **Copiar objeto**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-294">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copiar objeto en la Consola" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="d6ad5-296">Copiar objeto en la **Consola**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-296">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copiar un objeto en Orígenes" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="d6ad5-298">Copiar objeto en **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-298">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a><span data-ttu-id="d6ad5-299">Copiar el nombre de archivo en la herramienta Orígenes y en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="d6ad5-299">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="d6ad5-300">Ahora puede copiar un nombre de archivo mediante el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-300">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="d6ad5-301">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-301">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d6ad5-302">En la herramienta **Orígenes**, mantenga el puntero sobre un nombre de archivo, abra el menú contextual \(clic con el botón derecho\) y después, seleccione **Copiar nombre de archivo**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-302">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d6ad5-303">En la herramienta **Elementos** > panel **Estilos**, mantenga el puntero sobre un nombre de archivo, abra el menú contextual \(clic con el botón derecho\) y luego, seleccione **Copiar nombre del archivo**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-303">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar el nombre de archivo en Orígenes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="d6ad5-305">Copiar el nombre de archivo en **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-305">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar el nombre de archivo en el panel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="d6ad5-307">Copiar el nombre de archivo en el panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-307">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a><span data-ttu-id="d6ad5-308">Actualizaciones para Detalles del marco</span><span class="sxs-lookup"><span data-stu-id="d6ad5-308">Updates to Frame details</span></span>  

#### <a name="service-workers-information-in-frame-details"></a><span data-ttu-id="d6ad5-309">Información de los trabajos de servicio en Detalles del marco</span><span class="sxs-lookup"><span data-stu-id="d6ad5-309">Service Workers information in Frame details</span></span>  

<span data-ttu-id="d6ad5-310">DevTools ahora muestra un trabajo de servicio dedicado en el marco principal.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-310">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="d6ad5-311">En la siguiente ilustración, se muestran los detalles del trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-311">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="d6ad5-312">Para mostrar los detalles del trabajo de servicio, vaya a **Aplicación** > **Marcos** > `top` > **Trabajos de servicio** y después, seleccione un trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-312">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="d6ad5-313">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1122507][CR1122507].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-313">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Información de los Trabajos de servicio en Detalles del marco" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="d6ad5-315">Información de los **Trabajos de servicio** en **Detalles del marco**</span><span class="sxs-lookup"><span data-stu-id="d6ad5-315">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a><span data-ttu-id="d6ad5-316">Medir información de la memoria en Detalles del marco</span><span class="sxs-lookup"><span data-stu-id="d6ad5-316">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="d6ad5-317">El estatus de la API `performance.measureMemory()` ahora se muestra en la sección **Disponibilidad de la API**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-317">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="d6ad5-318">La nueva API `performance.measureMemory()` calcula el uso de memoria de toda la página web.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-318">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="d6ad5-319">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-319">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memoria" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="d6ad5-321">Medir memoria</span><span class="sxs-lookup"><span data-stu-id="d6ad5-321">Measure Memory</span></span>  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a><span data-ttu-id="d6ad5-322">Fotogramas descartados en la herramienta Rendimiento</span><span class="sxs-lookup"><span data-stu-id="d6ad5-322">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="d6ad5-323">Al [analizar el rendimiento de carga en la herramienta Rendimiento][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], la sección **Marcos** ahora marca los fotogramas eliminados en rojo.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-323">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="d6ad5-324">Para mostrar la velocidad de fotogramas, mantenga el puntero sobre algún fotograma descartado.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-324">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="d6ad5-325">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1075865][CR1075865].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-325">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Fotogramas descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="d6ad5-327">Fotogramas descartados</span><span class="sxs-lookup"><span data-stu-id="d6ad5-327">Dropped frames</span></span>  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a><span data-ttu-id="d6ad5-328">Nuevo cálculo de contraste de color: Algoritmo de contraste perceptual avanzado (APCA)</span><span class="sxs-lookup"><span data-stu-id="d6ad5-328">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="d6ad5-329">El [Algoritmo de contraste perceptual avanzado (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] reemplaza la relación de contraste de las directrices [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] en el [Selector de colores][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-329">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="d6ad5-330">APCA es la nueva forma de calcular el contraste.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-330">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="d6ad5-331">Se basa en las investigaciones modernas sobre la percepción del color.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-331">It is based on modern research on color perception.</span></span>  <span data-ttu-id="d6ad5-332">En comparación con las directrices AA/AAA, APCA depende más del contexto.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-332">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="d6ad5-333">El contraste se calcula de acuerdo con las siguientes propiedades espaciales de texto, color y contexto.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-333">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="d6ad5-334">Propiedades espaciales del texto que incluyen el grosor y el tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-334">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="d6ad5-335">Propiedades espaciales de color que incluyen contraste percibido entre el texto y el fondo.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-335">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="d6ad5-336">Propiedades espaciales del contexto que incluyen luz ambiental, alrededores y un propósito previsto.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-336">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="d6ad5-337">Para activar este experimento, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y active la casilla junto a **Habilitar el nuevo Algoritmo de contraste perceptual avanzado (APCA) para reemplazar la relación de contraste y las directrices AA/AAA anteriores**.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-337">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="d6ad5-338">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1121900][CR1121900].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-338">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA en el Selector de colores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="d6ad5-340">APCA en el Selector de colores</span><span class="sxs-lookup"><span data-stu-id="d6ad5-340">APCA in the Color Picker</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="d6ad5-341">Descargar los canales de versión preliminar de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d6ad5-341">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="d6ad5-342">Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-342">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="d6ad5-343">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6ad5-343">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="d6ad5-344">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d6ad5-344">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: ../../../accessibility/color-picker.md "Probar el contraste de color de texto con el Selector de colores | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: ../../../css/reference.md#change-css "Cambiar CSS: Referencias CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configuración: Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalización de accesos rápidos de teclado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices]: ../../../device-mode/dual-screen-and-foldables.md#test-on-foldable-and-dual-screen-devices "Prueba en dispositivos plegables y de doble pantalla: emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular una ventanilla móvil: Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: ../../../evaluate-performance/reference.md#record-load-performance "Registrar el rendimiento de carga: referencia del análisis de rendimiento | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Introducción a Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: ../../../inspect-styles/edit-fonts.md "Editar la configuración y los estilos de fuente CSS en el panel Estilos en DevTools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la unión: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla expandida para medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API de JavaScript de getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Sección 1: Demostración CSS :target para las Novedades en DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementar la lista desplegable en la configuración para cambiar los temas | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Incluir depurador para Microsoft Edge como dependencia | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Actualización de Edge DevTools a la versión 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Agregar botones de cierre único a las instancias del panel | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Seleccionar las características de la fuente y los colores de fondo para proporcionar suficiente contraste para facilitar la lectura | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos de confianza | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nuevo Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de versiones preliminares de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: Eliminar las cookies al filtrarlas, eliminar todas las cookies y no solo las filtradas | Errores de Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Solicitud de característica nueva | Se necesita la opción para ver el valor descodificado por URL en las cookies | Errores de Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: El nodo de captura ya no hace la captura de pantalla del nodo que está debajo del pliegue | Errores de Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: Borrar los datos del sitio destruye la sesión de Google en los sitios que no son de Google | Errores de Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: Poner los estados En línea y Sin conexión contiguamente en la lista | Errores de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitud de características: DevTools debe emular dispositivos plegables y de pantalla doble | Errores de Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: Mostrar fotogramas descartados en la línea de tiempo de devtools | Errores de Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: ofrecer un editor de tipo de letra especializado en la interfaz de usuario | Errores de Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: actualizar la lógica de cálculo de contraste por especificación | Errores de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: Información de los trabajos de Surface en la vista de árbol de marcos | Errores de Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: Imposible deshabilitar la grabación de red al volver a cargar | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: Herramientas de Flexbox | Errores de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: Informar la disponibilidad de la API validada en la vista de detalles del marco | Errores de Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: Superposición de Flexbox | Errores de Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: El Selector de colores no se muestra en la función var() | Errores de Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: Solicitud de característica: Copiar objeto desde la consola de devtools | Errores de Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitud de característica][Consola] agregar un objeto de copia al elemento del Portapapeles en el menú contextual | Errores de Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: Agregar el menú contextual del Elemento duplicado en el panel Elemento | Errores de Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: Compatibilidad para copiar el menú contextual CSS en el panel de Estilos | Errores de Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Compatibilidad para copiar el nombre de archivo y el número de línea | Errores de Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: agregar compatibilidad con :target en la característica de estado de forzar elemento | Errores de Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Accesibilidad - Narrador: El narrador no anuncia el recuento y la posición de las sugerencias disponibles para el código en la pestaña Estilos | Errores de Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung Estados Unidos"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (mejorado): Cómo cumplir los requisitos WCAG (referencia rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo): Cómo cumplir los requisitos WCAG (referencia rápida) | W3C"  

> [!NOTE]
> <span data-ttu-id="d6ad5-399">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d6ad5-400">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-89) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="d6ad5-400">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-89) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d6ad5-402">Este trabajo dispone de una [Licencia internacional de Atribución de Creative Commons 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6ad5-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen

[SpanningPlaceholder]: link-t-b-d "Expandir el marcador de posición"  
