---
description: Una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.
title: Referencia de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fce6dec3883cbcc758780a9fedb4c0fb2a8d0a4c
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439257"
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

# <a name="accessibility-reference"></a>Referencia de accesibilidad  

Esta página es una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.  Está pensado para desarrolladores web que:  

*   Tenga una comprensión básica de DevTools, como cómo abrirlo.  
*   Están familiarizados [con los principios de accesibilidad y los procedimientos recomendados.][MDNAccessibility]  
    
El propósito de esta referencia es ayudarle a descubrir todas las herramientas disponibles en DevTools que le ayudarán a examinar la accesibilidad de una página.  

Si está buscando ayuda para navegar por DevTools con una tecnología de asistencia como un lector de pantalla, vaya a Navegación por [Microsoft Edge DevTools con][DevtoolsAccessibilityNavigation]tecnología de asistencia .  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a>Información general sobre las características de accesibilidad en Microsoft Edge DevTools  

En esta sección se explica cómo DevTools se adapta a su kit de herramientas de accesibilidad general.  

Al determinar si una página es accesible, debe tener 2 preguntas generales en mente:  

1.  ¿Puede navegar por la página con un teclado o un [lector de pantalla?][MDNScreenReader]  
1.  ¿Los elementos de la página están correctamente marcados para los lectores de pantalla?  
    
En general, DevTools debe ayudarle a corregir errores relacionados con la pregunta #2, ya que estos errores son fáciles de detectar de forma automatizada.  La #1 preguntas es igual de importante, pero desafortunadamente DevTools no le ayuda allí.  La única forma de encontrar errores relacionados con la pregunta #1 es intentar usar una página con un teclado o un lector de pantalla.  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a>Auditar la accesibilidad de una página  

> [!NOTE]
> La **herramienta Auditorías** proporciona vínculos al contenido hospedado en sitios web de terceros.  Microsoft no es responsable y no tiene control sobre el contenido de estos sitios ni sobre los datos que se puedan recopilar.  

En general, use el panel Auditorías para determinar si:  

*   Una página está correctamente marcada para lectores de pantalla.  
*   Los elementos de texto de una página tienen suficientes relaciones de contraste.  Desplácese [hasta Ver la relación de contraste de un elemento de texto en el Selector de colores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

Para auditar una página:  

1.  Vaya a la dirección URL que desea auditar.  
1.  En DevTools, elija la **herramienta Auditorías.**  DevTools muestra varias opciones de configuración.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-audits-pane.msft.png":::
       Configurar auditorías  
    :::image-end:::  
    
    > [!NOTE]
    > Las capturas de pantalla de esta sección se tomaron con Microsoft Edge versión 79.  Puede comprobar la versión que está ejecutando en `edge://version` .  La interfaz de usuario de la herramienta **Auditorías** tiene un aspecto diferente en versiones anteriores de Microsoft Edge, pero el flujo de trabajo general es el mismo.  
    
1.  Para **Dispositivo,** elija **Móvil** si desea simular un dispositivo móvil.  Esta opción cambia la cadena del agente de usuario y cambia el tamaño de la ventanilla.  Si la versión móvil de la página se muestra de forma diferente a la versión de escritorio, esta opción puede tener un efecto significativo en los resultados de la auditoría.  
1.  En la **sección Auditorías,** asegúrese de que **la accesibilidad** está habilitada.  Deshabilite las otras categorías si desea excluirlas del informe.  Déjelos habilitados si desea descubrir otras formas de mejorar la calidad de la página.  
1.  La **sección Limitación permite** limitar la red y la CPU, lo que resulta útil al analizar el rendimiento de la carga.  Esta opción debe ser irrelevante para la puntuación de accesibilidad, por lo que puedes usar lo que prefieras.  
1.  La **casilla Borrar almacenamiento** permite borrar todo el almacenamiento antes de cargar la página o conservar el almacenamiento entre cargas de página.  Esta opción también es probablemente irrelevante para la puntuación de accesibilidad, por lo que puede usar lo que prefiera.  
1.  Elija **Ejecutar auditorías**. Después de 10 a 30 segundos, DevTools proporciona un informe.  El informe le ofrece varias sugerencias sobre cómo mejorar la accesibilidad de la página.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un informe" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Un informe  
    :::image-end:::  
    
1.  Elija una auditoría para obtener más información sobre ella.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Más información sobre una auditoría" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Más información sobre una auditoría  
    :::image-end:::  
    
1.  Elija **Obtener más información** para ver la documentación de esa auditoría.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Ver la documentación de una auditoría" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Ver la documentación de una auditoría  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a>Vea también: extensión aXe  

Es posible que prefiera usar la [extensión aXe en][ChromeWebStoreAxe] lugar de la **herramienta Auditorías.**  
La extensión aXe generalmente proporciona la misma información, ya que es el motor subyacente el que impulsa el panel Auditorías.  La extensión aXe tiene una interfaz de usuario diferente y describe las auditorías de forma ligeramente diferente.  
Una ventaja que la extensión aXe tiene sobre la herramienta **Auditorías** es que le permite inspeccionar y resaltar nodos con errores.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="La extensión aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   La extensión aXe  
:::image-end:::  

## <a name="the-accessibility-panel"></a>Panel accesibilidad  

El **panel Accesibilidad** es donde se ve el árbol de accesibilidad, los atributos ARIA y las propiedades de accesibilidad calculada de los nodos DOM.  

Para abrir el panel **Accesibilidad:**  

1.  Elija la **herramienta** Elementos.  
1.  En el **árbol DOM,** seleccione el elemento que desea inspeccionar.  
1.  Elija el panel **Accesibilidad.**  Este panel puede estar oculto detrás del **botón Más pestañas** \( ![ Más pestañas ](../media/more-tabs-icon.msft.png) \).  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspeccionar el elemento h1 de la página principal de DevTools en el panel Accesibilidad" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspeccionar el `h1` elemento de la página principal de DevTools en el panel **Accesibilidad**  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Ver la posición de un elemento en el árbol de accesibilidad  

El [árbol de accesibilidad][MDNAccessibilityTree] es un subconjunto del árbol DOM.  Solo contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página en un lector de pantalla.  

Inspeccione la posición de un elemento en el árbol de accesibilidad desde el panel [Accesibilidad.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Sección Árbol de accesibilidad" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Sección **Árbol de accesibilidad**  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a>Ver los atributos ARIA de un elemento  

Los atributos ARIA garantizan que los lectores de pantalla tengan toda la información que necesitan para representar correctamente el contenido de una página.  

Vea los atributos ARIA de un elemento en el panel [Accesibilidad.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Sección Atributos de ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Sección **Atributos de ARIA**  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a>Ver las propiedades de accesibilidad calculadas de un elemento  

> [!NOTE]
> Si está buscando propiedades CSS calculadas, vaya al panel [Calculado.][DevtoolsCssReferenceViewActuallyAppliedElements]  

El explorador calcula dinámicamente algunas propiedades de accesibilidad.  Estas propiedades se muestran en la **sección Propiedades calculadas** del panel **Accesibilidad.**  

Vea las propiedades de accesibilidad calculadas de un elemento en el panel [Accesibilidad.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Sección Propiedades calculadas del panel Accesibilidad" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Sección **Propiedades calculadas** del panel **Accesibilidad**  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a>Ver la relación de contraste de un elemento de texto en el Selector de colores  

Algunas personas con visión baja no ven áreas como muy brillantes o muy oscuras.  Todo tiende a aparecer con aproximadamente el mismo brillo, lo que hace que sea difícil distinguir contornos y bordes.  

La relación de contraste mide la diferencia de brillo entre el primer plano y el fondo del texto.  Si el texto tiene una relación de contraste baja, estos usuarios de visión baja pueden experimentar literalmente el sitio como una pantalla en blanco.  

El Selector de colores te ayuda a comprobar que el texto cumple los niveles de relación de contraste recomendados:  

1.  Elija la **herramienta** Elementos.  
1.  En el **árbol DOM,** seleccione el elemento de texto que desea inspeccionar.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspeccionar un párrafo en el árbol DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspeccionar un párrafo en el **árbol DOM**  
    :::image-end:::  
    
1.  En el panel **Estilos,** elija el cuadrado de color junto al `color` valor del elemento.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="La propiedad color del elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       La `color` propiedad del elemento  
    :::image-end:::  
    
1.  Compruebe la **sección Relación de contraste** del Selector de colores.  Una marca de verificación significa que el elemento cumple la [recomendación mínima][W3CContrastMinimum].  Dos marcas de verificación significa que cumple la [recomendación mejorada][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La sección Relación de contraste del Selector de colores muestra 2 marcas de verificación y un valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       La **sección Relación de contraste** del selector de colores muestra 2 marcas de verificación y un valor de `13.97`  
    :::image-end:::  
    
1.  Para obtener más información, elija la **sección Relación de** contraste.  Aparece una línea en el selector visual en la parte superior del Selector de colores.  Si el color actual cumple las recomendaciones, cualquier cosa del mismo lado de la línea también cumple las recomendaciones.  Si el color actual no cumple las recomendaciones, cualquier cosa del mismo lado tampoco cumple las recomendaciones.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Línea de relación de contraste en el selector visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Línea **de relación de** contraste en el selector visual  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegar por Microsoft Edge DevTools con tecnología de asistencia | Microsoft Docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Ver solo el CSS que realmente se aplica a un elemento: referencia CSS | Microsoft Docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Pruebas de accesibilidad web - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árbol de accesibilidad (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accesibilidad | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lector de pantalla | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (mejorado) Nivel AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nivel AA | W3C"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
