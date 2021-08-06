---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para ver y cambiar el CSS de una página CSS.
title: Inspeccionar cuadrícula CSS en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 143d17fb577d89d4b675e78eff15af26be5746c53f75b03769e00d42bc270268
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11801211"
---
# <a name="inspect-css-grid"></a>Inspeccionar cuadrícula CSS  

En este artículo se le guía a través de la identificación de cuadrículas CSS en un sitio web y la depuración de problemas de diseño de cuadrícula mediante superposiciones de cuadrícula personalizables.  

Los ejemplos usados en las figuras de este artículo se toman de las siguientes páginas web.  

*   [Cuadro de frutas][JecFyiDemoCssGridFruit]  
*   [Caja de refrigerio][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a>Antes de empezar  

CSS Grid es un poderoso paradigma de diseño para la web.  Un excelente lugar para empezar a aprender sobre CSS Grid y las muchas características es la [guía css grid layout][MdnCssGridLayout] en MDN.  

## <a name="discover-css-grids"></a>Detectar cuadrículas CSS  

Cuando un elemento HTML de la página tiene o se ha aplicado, se muestra un distintivo junto a él `display: grid` `display: inline-grid` en el panel `grid` [Elementos.][DevtoolsGuideChromiumOpen]  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-discover-grid.msft.png":::
   Descubrir cuadrícula  
:::image-end:::  

Elija el distintivo para alternar la visualización de una superposición de cuadrícula en la página.  La superposición aparece sobre el elemento, establecida como una cuadrícula para mostrar la posición de las líneas de cuadrícula y las pistas:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Distintivo de cuadrícula de alternancia" lightbox="../media/grid-highlight-grid.msft.png":::
   Distintivo de cuadrícula de alternancia  
:::image-end:::  

Abra el **panel Diseño.**  Cuando se incluyen cuadrículas en **** una página, el panel Diseño incluye una sección **Cuadrícula** que contiene varias opciones para ver las cuadrículas.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Panel Diseño" lightbox="../media/grid-layout-pane.msft.png":::
   **Panel Diseño**  
:::image-end:::  

La **sección Cuadrícula** del panel **Diseño** contiene las 2 subsecciones siguientes.  

*   Configuración de visualización de superposición  
*   Superposiciones de cuadrícula  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a>Configuración de visualización de superposición  

La **configuración de visualización de superposición** consta de 2 partes siguientes.  

*   Elija una de las siguientes opciones en el menú desplegable.  
    
    | Opción Línea | Detalles |  
    |:--- |:--- |  
    | **Ocultar etiquetas de línea** | Ocultar las etiquetas de las líneas de cada superposición de cuadrícula. |  
    | **Mostrar números de línea** | Muestra los números de las líneas de cada superposición de cuadrícula \(seleccionada de forma predeterminada\). |  
    | **Mostrar nombres de línea** | Muestra los nombres de las líneas de cada superposición de cuadrícula cuando se proporcionan nombres. |  
    
*  Seleccione la casilla siguiente de las siguientes opciones.  
    
    | Opción | Detalles |  
    |:--- |:--- |  
    | **Mostrar tamaños de pista**  | Muestra \(u hide\) los tamaños de las pistas. |  
    | **Mostrar nombres de área** | Muestra \(u hide\) los nombres del área, cuando se proporcionan nombres. |  
    | **Ampliar líneas de cuadrícula** | Muestra \(u oculta\) las extensiones de las dimensiones de cuadrícula a lo largo de cada eje.  De forma predeterminada, las líneas de cuadrícula solo se muestran dentro del elemento con `display: grid` o CSS establecido en `display: inline-grid` él. |  
    
En las secciones siguientes se proporcionan detalles para cada una de las **opciones de visualización De superposición.**  

### <a name="show-line-numbers"></a>Mostrar números de línea  

De forma predeterminada, los números de línea positivos y negativos se muestran en la superposición de cuadrícula.  

Para obtener más información acerca de los números negativos en la superposición de cuadrícula, vaya a [Ubicación basada en línea con CSS Grid][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Mostrar números de línea" lightbox="../media/grid-show-line-numbers.msft.png":::
   Mostrar números de línea  
:::image-end:::  

### <a name="hide-line-labels"></a>Ocultar etiquetas de línea  

Elija **Ocultar etiquetas de línea** para ocultar los números de línea.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ocultar etiquetas de línea" lightbox="../media/grid-hide-line-labels.msft.png":::
   Ocultar etiquetas de línea  
:::image-end:::  

### <a name="show-line-names"></a>Mostrar nombres de línea  

Para obtener más información acerca de los nombres de línea en la superposición de cuadrícula, vaya a [Diseño con líneas de cuadrícula con nombre.][MdnLayoutUsingNamedGridLines]  

Elija **Mostrar nombres de línea** para ver los nombres de línea en lugar de números.  En el ejemplo, 4 líneas tienen nombres: `left` , `middle1` , y `middle2` `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Mostrar nombres de línea" lightbox="../media/grid-show-line-names.msft.png":::
   **Mostrar nombres de línea**  
:::image-end:::  

### <a name="show-track-sizes"></a>Mostrar tamaños de pista  

Active la casilla **Mostrar tamaños de** pista para ver los tamaños de pista de la cuadrícula.  

DevTools muestra `[authored size]` y en cada etiqueta de `[computed size]` línea.  

| Tamaño | Detalles |  
|:--- |:--- |  
| **tamaño de autor** | El tamaño definido en la hoja de estilos \(omitido si no está definido\). |  
| **tamaño calculado** | Tamaño real en pantalla. |  

En la demostración, los tamaños de columna `snack-box` se definen en el `grid-template-columns:1fr 2fr;` CSS.  Por lo tanto, las etiquetas de línea de columna muestran tamaños escritos y calculados.  

| Tamaño de la pista | Tamaño de creación | Tamaño calculado |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96,66px** | 1fr | 96,66 píxeles |  
| **2fr** &#x2022; **193,32px** | 2fr | 193,32px |  

Las etiquetas de línea de fila solo muestran tamaños calculados, ya que no hay ningún tamaño de fila definido en la hoja de estilos.  

| Tamaño de la pista | Tamaño de creación | Tamaño calculado |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Mostrar tamaños de pista" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Mostrar tamaños de pista**  
:::image-end:::  

### <a name="show-area-names"></a>Mostrar nombres de área  

Para ver los nombres de área, active la casilla **Mostrar nombres de** área.  En el ejemplo, hay 3 áreas en la cuadrícula: **superior**, **inferior1** e **inferior2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Mostrar nombres de área" lightbox="../media/grid-show-area-names.msft.png":::
   **Mostrar nombres de área**  
:::image-end:::  

### <a name="extend-grid-lines"></a>Ampliar líneas de cuadrícula  

Active la **casilla Extender líneas de cuadrícula** para extender las líneas de cuadrícula al borde de la ventanilla a lo largo de cada eje.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Ampliar líneas de cuadrícula" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Ampliar líneas de cuadrícula**  
:::image-end:::  

## <a name="grid-overlays"></a>Superposiciones de cuadrícula  

La **sección Superposiciones de cuadrícula** contiene una lista de cuadrículas que están presentes en la página, cada una con una casilla, junto con varias opciones.  

### <a name="enable-overlay-views-of-multiple-grids"></a>Habilitar vistas superpuestas de varias cuadrículas  

Para mostrar la cuadrícula superpuesta para varias cuadrículas, elija la casilla situada junto a cada nombre de la cuadrícula.  En el ejemplo, hay 2 superposiciones de cuadrícula habilitadas que se representan con colores diferentes.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Habilitar vistas superpuestas de varias cuadrículas" lightbox="../media/grid-grid-overlays.msft.png":::
   Habilitar vistas superpuestas de varias cuadrículas  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a>Personalizar el color de superposición de cuadrícula  

Para abrir el selector de color y personalizar el color de superposición de cuadrícula, elija el cuadro situado junto al nombre de la superposición de cuadrícula.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personalizar el color de superposición de cuadrícula" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Personalizar el color de superposición de cuadrícula  
:::image-end:::  

### <a name="highlight-the-grid"></a>Resaltar la cuadrícula  

Para resaltar el elemento HTML en la herramienta **Elementos** y desplazarse hasta él en la página web, elija el elemento **Mostrar** en el panel Elementos \( Mostrar elemento en el icono del panel Elementos ![ ](../media/show-element-in-element-panel-icon.msft.png) \).  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Resaltar la cuadrícula" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Resaltar la cuadrícula  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Cuadrícula CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Cuadrícula CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Css Grid Layout | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Diseño con líneas de cuadrícula con nombre | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Colocación basada en línea con css grid | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/grid) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
