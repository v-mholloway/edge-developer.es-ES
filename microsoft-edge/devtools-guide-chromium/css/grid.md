---
description: Aprenda a usar Microsoft Edge DevTools para ver y cambiar la CSS de una página CSS.
title: Inspeccionar cuadrícula CSS en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1fe6bd1c8efd244315fb9a38777df6ea3e9b1a4d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231100"
---
# Inspeccionar cuadrícula CSS  

Este artículo le muestra cómo identificar las cuadrículas CSS en un sitio web y cómo depurar problemas de diseño de cuadrícula con superposiciones de cuadrícula personalizables.  

Los ejemplos que se usan en las figuras de este artículo se han tomado de las siguientes páginas Web.  

*   [Cuadro de frutas][JecFyiDemoCssGridFruit]  
*   [Cuadro de bocadillo][JecFyiDemoCssGridSnack]  

## Antes de comenzar  

CSS Grid es un versátil paradigma de diseño para la Web.  Un excelente lugar para comenzar a aprender sobre CSS Grid y las numerosas características es la [Guía de diseño de cuadrícula CSS][MdnCssGridLayout] en MDN.  

## Descubrir cuadrículas CSS  

Cuando un elemento HTML de la página se tiene o se le `display: grid` `display: inline-grid` aplica, `grid` se muestra un distintivo junto a él en el panel [elementos][DevtoolsGuideChromiumOpen] .  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-discover-grid.msft.png":::
   Descubrir cuadrícula  
:::image-end:::  

Seleccione el distintivo para alternar la visualización de una superposición de cuadrícula en la página.  La superposición aparece sobre el elemento, dispuestos como una cuadrícula para mostrar la posición de las líneas de la cuadrícula y las pistas:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Activar distintivo de cuadrícula" lightbox="../media/grid-highlight-grid.msft.png":::
   Activar distintivo de cuadrícula  
:::image-end:::  

Abrir el panel **diseño** .  Cuando se incluyen cuadrículas en una página, el panel de **diseño** incluye una sección de **cuadrícula** que contiene varias opciones para ver las cuadrículas.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Panel de diseño" lightbox="../media/grid-layout-pane.msft.png":::
   Panel de **diseño**  
:::image-end:::  

La sección de **cuadrícula** en el panel de **diseño** contiene las siguientes 2 subsecciones.  

*   Configuración de superposición  
*   Superposiciones de cuadrícula  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## Configuración de superposición  

La **configuración de la pantalla de superposición** consta de dos partes:  

*   Elija una de las siguientes opciones en el menú desplegable.  
    
    | Opción de línea | Detalles |  
    |:--- |:--- |  
    | **Ocultar etiquetas de línea** | Oculte las etiquetas de las líneas de cada superposición de cuadrícula. |  
    | **Mostrar números de línea** | Mostrar los números de las líneas de cada superposición de cuadrícula \ (seleccionado de forma predeterminada \). |  
    | **Mostrar nombres de línea** | Mostrar los nombres de las líneas de cada cuadrícula superpuestas cuando se proporcionen nombres. |  
    
*  Seleccione la casilla junto a las siguientes opciones.  
    
    | Opción | Detalles |  
    |:--- |:--- |  
    | **Mostrar tamaños de seguimiento**  | Mostrar \ (u ocultar \) el tamaño de las pistas. |  
    | **Mostrar nombres de área** | Mostrar \ (u ocultar \) los nombres del área, cuando se proporcionen nombres. |  
    | **Extender las líneas de la cuadrícula** | Muestra \ (u oculta \) las extensiones de las dimensiones de la cuadrícula a lo largo de cada eje.  De forma predeterminada, las líneas de cuadrícula solo se muestran dentro del elemento con `display: grid` o `display: inline-grid` CSS establecido. |  
    
En las siguientes secciones se proporcionan detalles para cada una de las **Opciones de superposición de pantalla**.  

### Mostrar números de línea  

De forma predeterminada, los números de línea positivos y negativos se muestran en la superposición de la cuadrícula.  

Para obtener más información sobre números negativos en la superposición de cuadrícula, vaya a [ubicación basada en líneas con cuadrícula CSS][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Mostrar números de línea" lightbox="../media/grid-show-line-numbers.msft.png":::
   Mostrar números de línea  
:::image-end:::  

### Ocultar etiquetas de línea  

Seleccione **ocultar etiquetas de línea** para ocultar los números de línea.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ocultar etiquetas de línea" lightbox="../media/grid-hide-line-labels.msft.png":::
   Ocultar etiquetas de línea  
:::image-end:::  

### Mostrar nombres de línea  

Para obtener más información sobre los nombres de línea en la superposición de cuadrícula, desplácese al [diseño mediante líneas de cuadrícula con nombre][MdnLayoutUsingNamedGridLines].  

Seleccione **Mostrar nombres de línea** para ver los nombres de línea en lugar de los números.  En el ejemplo, cuatro líneas tienen nombres: `left` , `middle1` , `middle2` y `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Mostrar nombres de línea" lightbox="../media/grid-show-line-names.msft.png":::
   **Mostrar nombres de línea**  
:::image-end:::  

### Mostrar tamaños de seguimiento  

Active la casilla **Mostrar tamaños de seguimiento** para ver los tamaños de las pistas de la cuadrícula.  

DevTools muestra `[authored size]` y `[computed size]` en cada etiqueta de línea.  

| Tamaño | Detalles |  
|:--- |:--- |  
| **tamaño creado** | El tamaño definido en la hoja de estilos \ (se omite si no se define \). |  
| **tamaño calculado** | Tamaño real en pantalla. |  

En la demostración, el `snack-box` tamaño de las columnas se define en la `grid-template-columns:1fr 2fr;` CSS.  Por lo tanto, las etiquetas de las líneas de columna muestran tanto los tamaños de los usuarios como los calculados.  

| Tamaño de la pista | Tamaño creado | Tamaño calculado |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96.66 PX** | 1fr | 96.66 PX |  
| **2fr** &#x2022; **193.32 PX** | 2fr | 193.32 PX |  

Las etiquetas de línea de fila muestran solo los tamaños calculados, ya que no hay tamaños de fila definidos en la hoja de estilos.  

| Tamaño de la pista | Tamaño creado | Tamaño calculado |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Mostrar tamaños de seguimiento" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Mostrar tamaños de seguimiento**  
:::image-end:::  

### Mostrar nombres de área  

Para ver los nombres de las áreas, active la casilla **Mostrar nombres de área** .  En el ejemplo, hay 3 áreas en la cuadrícula: **Top**, **bottom1** y **bottom2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Mostrar nombres de área" lightbox="../media/grid-show-area-names.msft.png":::
   **Mostrar nombres de área**  
:::image-end:::  

### Extender las líneas de la cuadrícula  

Active la casilla **extender líneas de cuadrícula** para extender las líneas de la cuadrícula al borde de la ventanilla a lo largo de cada eje.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Extender las líneas de la cuadrícula" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Extender las líneas de la cuadrícula**  
:::image-end:::  

## Superposiciones de cuadrícula  

La sección de **superposiciones de cuadrícula** contiene una lista de cuadrículas que están presentes en la página, cada una con una casilla, junto con varias opciones.  

### Habilitar vistas superpuestas de varias cuadrículas  

Para mostrar la cuadrícula de superposición para varias cuadrículas, seleccione la casilla junto a cada nombre de la cuadrícula.  En el ejemplo, se han habilitado dos superposiciones de cuadrícula que se representan con distintos colores.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Habilitar vistas superpuestas de varias cuadrículas" lightbox="../media/grid-grid-overlays.msft.png":::
   Habilitar vistas superpuestas de varias cuadrículas  
:::image-end:::  

### Personalizar el color de superposición de cuadrícula  

Para abrir el selector de colores y personalizar el color de superposición de cuadrícula, seleccione el cuadro situado junto al nombre de la superposición de cuadrícula.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personalizar el color de superposición de cuadrícula" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Personalizar el color de superposición de cuadrícula  
:::image-end:::  

### Resaltar la cuadrícula  

Para resaltar el elemento HTML en el panel **elementos** y desplazarse hasta él en la página web, elija el **elemento Mostrar en el panel elementos** \ ( ![ elemento Mostrar en el icono del panel elementos ][ImageShowElementInElementsPanelIcon] ).  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Resaltar la cuadrícula" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Resaltar la cuadrícula  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Cuadrícula CSS | JEC. FYI"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Cuadrícula CSS | JEC. FYI"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Diseño de cuadrícula CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Diseño usando líneas de cuadrícula con nombre | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Ubicación basada en líneas con CSS Grid | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/grid) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
