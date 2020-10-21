---
description: Una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.
title: Referencia de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: de8f4bee6fef7725af9b97fb80ab45582dfa2286
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125317"
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

# Referencia de accesibilidad  

Esta página es una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.  Está destinada a los programadores web que:  

*   Tener un conocimiento básico de DevTools, como, por ejemplo, cómo abrirlo.  
*   Está familiarizado con los [principios de accesibilidad y los procedimientos recomendados][MDNAccessibility].  
    
El propósito de esta referencia es ayudarle a descubrir todas las herramientas disponibles en DevTools que le ayudan a examinar la accesibilidad de una página.  

Consulte [navegar por Microsoft Edge DevTools con tecnología de asistencia][DevtoolsAccessibilityNavigation] si necesita ayuda para navegar por DevTools con una tecnología de asistencia, como un lector de pantalla.  

## Información general sobre las características de accesibilidad en Microsoft Edge DevTools  

En esta sección se explica cómo DevTools encaja en el conjunto de herramientas general de accesibilidad.  

Al determinar si una página es accesible, debe tener en cuenta dos preguntas generales:  

1.  ¿Puede navegar por la página con un teclado o un [lector de pantalla][MDNScreenReader]?  
1.  ¿Están los elementos de la página correctamente marcados para los lectores de pantalla?  
    
En general, DevTools debería ayudarle a corregir los errores relacionados con preguntas #2, porque estos errores son fáciles de detectar de forma automática.  La pregunta #1 es tan importante, pero lamentablemente DevTools no le ayuda a usted.  La única forma de buscar errores relacionados con la pregunta #1 es intentar usar una página con un teclado o lector de pantalla.  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## Auditar la accesibilidad de una página  

> [!NOTE]
> El panel **Auditoría** proporciona vínculos a contenido hospedado en sitios web de terceros.  Microsoft no se responsabiliza y no tiene ningún control sobre el contenido de estos sitios y los datos que se pueden recopilar.  

En general, use el panel auditorías para determinar si:  

*   Una página se marcó correctamente para los lectores de pantalla.  
*   Los elementos de texto de una página tienen relaciones de contraste suficientes.  Consulte [ver la relación de contraste de un elemento de texto en el selector de colores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

Para auditar una página:  

1.  Vaya a la dirección URL que desea auditar.  
1.  En DevTools, haga clic en la pestaña **auditorías** .  En DevTools se muestran varias opciones de configuración.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-audits-pane.msft.png":::
       Configurar auditorías  
    :::image-end:::  
    
    > [!NOTE]
    > Las capturas de pantallas de esta sección se han tomado con la versión 79 de Microsoft Edge.  Puede consultar qué versión está ejecutando `edge://version` .  La interfaz de usuario del panel **auditorías** tiene un aspecto diferente en versiones anteriores de Microsoft Edge, pero el flujo de trabajo general es el mismo.  
    
1.  En **dispositivo**, elija **móvil** si quiere simular un dispositivo móvil.  Esta opción cambia la cadena de agente de usuario y cambia el tamaño de la ventanilla.  Si la versión móvil de la página se muestra de forma diferente a la de la versión de escritorio, esta opción podría tener un efecto significativo en los resultados de la auditoría.  
1.  En la sección **auditorías** , asegúrese de que **accesibilidad** está habilitada.  Deshabilite las otras categorías si desea excluirlas de su informe.  Déjelas habilitadas si deseas descubrir otras formas de mejorar la calidad de la página.  
1.  La sección de **limitación** le permite limitar la red y la CPU, lo cual es útil al analizar el rendimiento de la carga.  Esta opción no debe ser relevante para la puntuación de accesibilidad, por lo que puede usar lo que prefiera.  
1.  La casilla **Borrar almacenamiento** le permite borrar todo el almacenamiento antes de cargar la página o conservar el almacenamiento entre cargas de páginas.  Esta opción también probablemente es irrelevante para la puntuación de accesibilidad, por lo que puede usar lo que prefiera.  
1.  Elija **Ejecutar Auditorías**. Después de 10 a 30 segundos, DevTools proporciona un informe.  El informe le ofrece varias sugerencias para mejorar la accesibilidad de la página.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Un informe  
    :::image-end:::  
    
1.  Haga clic en una auditoría para obtener más información sobre ella.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Más información sobre una auditoría  
    :::image-end:::  
    
1.  Elija más **información** para ver la documentación de esa auditoría.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Ver la documentación de una auditoría  
    :::image-end:::  
    
### Vea también: extensión aXe  

Es posible que prefiera usar la [extensión de aXe][ChromeWebStoreAxe] en lugar del panel **auditorías** .  
La extensión aXe generalmente proporciona la misma información, ya que es el motor subyacente que alimenta el panel auditorías.  La extensión de aXe tiene una interfaz de usuario diferente y describe las auditorías de forma ligeramente distinta.  
Una de las ventajas de que la extensión aXe está en el panel **Auditoría** es que le permite inspeccionar y resaltar los nodos con errores.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   La extensión de aXe  
:::image-end:::  

## El panel Accesibilidad  

El panel de **accesibilidad** es el lugar donde se ve el árbol de accesibilidad, los atributos de Aria y las propiedades de accesibilidad calculadas de los nodos DOM.  

Para abrir el panel **accesibilidad** :  

1.  Haga clic en la pestaña **elementos** .  
1.  En el **árbol DOM**, seleccione el elemento que desea inspeccionar.  
1.  Haga clic en la pestaña **accesibilidad** .  Es posible que esta pestaña esté oculta detrás del botón **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \).  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspeccionar el `h1` elemento de la Página principal de DevTools en el panel **accesibilidad**  
:::image-end:::  

### Ver la posición de un elemento en el árbol de accesibilidad  

El [árbol de accesibilidad][MDNAccessibilityTree] es un subconjunto del árbol DOM.  Solo contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página en un lector de pantalla.  

Inspeccione la posición de un elemento en el árbol de accesibilidad en el [panel Accesibilidad](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Sección de **árbol de accesibilidad**  
:::image-end:::  

### Ver los atributos de ARIA de un elemento  

Los atributos de ARIA garantizan que los lectores de pantalla tengan toda la información que necesitan para representar correctamente el contenido de una página.  

Ver los atributos de ARIA de un elemento en el [Panel de accesibilidad](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   La sección de **atributos de Aria**  
:::image-end:::  

### Ver las propiedades de accesibilidad calculadas de un elemento  

> [!NOTE]
> Si está buscando propiedades calculadas de CSS, vaya a la [pestaña calculada][DevtoolsCssReferenceViewActuallyAppliedElements].  

El explorador calcula dinámicamente algunas propiedades de accesibilidad.  Estas propiedades se muestran en la sección **propiedades calculadas** del panel **accesibilidad** .  

Ver las propiedades de accesibilidad calculadas de un elemento en el [Panel de accesibilidad](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Sección **propiedades calculadas** del panel **accesibilidad**  
:::image-end:::  

## Ver la relación de contraste de un elemento de texto en el selector de colores  

Algunas personas con deficiencias visuales no ven las áreas muy claras o muy oscuras.  Todo tiende a aparecer sobre el mismo brillo, lo que hace que sea difícil distinguir los esquemas y los bordes.  

La relación de contraste mide la diferencia de brillo entre el primer plano y el fondo del texto.  Si el texto tiene una relación de contraste baja, es posible que los usuarios de estas deficiencias experimenten literalmente su sitio como pantalla en blanco.  

El selector de colores le ayuda a comprobar que el texto cumple los niveles de proporción de contraste recomendados:  

1.  Haga clic en la pestaña **elementos** .  
1.  En el **árbol DOM**, seleccione el elemento de texto que desea inspeccionar.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspeccionar un párrafo del **árbol DOM**  
    :::image-end:::  
    
1.  En el panel **estilos** , haga clic en el cuadrado de color situado junto al `color` valor del elemento.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       La `color` propiedad del elemento  
    :::image-end:::  
    
1.  Compruebe la sección **relación de contraste** del selector de colores.  Una marca de verificación significa que el elemento cumple con la [recomendación mínima][W3CContrastMinimum].  Dos marcas de verificación significa que cumple con la [Recomendación mejorada][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       La sección de **relación de contraste** del selector de color muestra 2 marcas de verificación y un valor de `13.97`  
    :::image-end:::  
    
1.  Haga clic en la sección **relación de contraste** para ver más información.  Aparece una línea en el selector visual en la parte superior del selector de colores.  Si el color actual cumple con las recomendaciones, cualquier cosa en el mismo lado de la línea también se ajusta a las recomendaciones.  Si el color actual no cumple con las recomendaciones, entonces cualquier cosa en el mismo lado no cumple con las recomendaciones.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       La línea de **proporción de contraste** en el selector visual  
    :::image-end:::  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegar por Microsoft Edge DevTools con tecnología de asistencia | Microsoft docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Ver solo la CSS que se aplica realmente a una referencia CSS de elemento | Microsoft docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe-pruebas de accesibilidad web-tienda web de Chrome"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árbol de accesibilidad (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accesibilidad | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lector de pantalla | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Nivel de contraste (mejorado) AAA AAA | RELATIVA"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nivel AA | RELATIVA"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
