---
description: Probar el contraste de color de texto con el Selector de colores.
title: Probar el contraste de color de texto con el Selector de colores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f4ba5f3706460c443ae06a393e5ef63e5d336229
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597722"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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
# <a name="test-text-color-contrast-using-the-color-picker"></a>Probar el contraste de color de texto con el Selector de colores

Es posible que las personas con visión baja no vean áreas muy brillantes o muy oscuras.  Todo tiende a aparecer en el mismo nivel de brillo, lo que hace que sea difícil distinguir contornos y bordes.  

La relación de contraste mide la diferencia de brillo entre el primer plano y el fondo del texto.  Si el texto tiene una relación de contraste baja, las personas con visión baja pueden experimentar el sitio como una pantalla en blanco.  

En DevTools, una forma de ver la relación de contraste de un elemento de texto es usar el Selector de colores, desde la **pestaña Estilos.**  El Selector de colores te ayuda a comprobar que el texto cumple los niveles de relación de contraste recomendados.

**Para comprobar el contraste de color de texto con el Selector de colores:**

1.  En DevTools, seleccione la **herramienta** Elementos.  
1.  En el **árbol DOM,** seleccione el elemento de texto que desea inspeccionar.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspeccionar un párrafo en el árbol DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspeccionar un párrafo en el **árbol DOM**  
    :::image-end:::  
    
1.  En la **pestaña Estilos,** busque la **propiedad color** que se aplica al elemento y, a continuación, seleccione el cuadrado de color junto a la **propiedad color.**
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="La propiedad color del elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       La `color` propiedad del elemento  
    :::image-end:::  
    
1.  Examine la **sección Relación de contraste** del Selector de colores.  Una marca de verificación significa que el elemento cumple la [recomendación mínima][W3CContrastMinimum].  Dos marcas de verificación significan que cumple la [recomendación mejorada][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La sección Relación de contraste del selector de colores muestra 2 marcas de verificación y un valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       La **sección Relación de contraste** del selector de colores muestra 2 marcas de verificación y un valor de `13.97`  
    :::image-end:::  
    
1.  Para obtener más información, seleccione la **sección Relación de contraste** para expandirla.  En el selector visual de la parte superior del Selector de colores, aparecen dos líneas que se ejecutan en el selector visual, junto con un círculo para el color actual.  Si el color actual cumple las recomendaciones, cualquier cosa del mismo lado de la línea también cumple las recomendaciones.  Si el color actual no cumple las recomendaciones, cualquier cosa del mismo lado tampoco cumple las recomendaciones.  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Línea de relación de contraste en el selector visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Línea **de relación de** contraste en el selector visual  
    :::image-end:::  

1. Para probar diferentes colores, seleccione dentro del selector visual o seleccione una muestra de color en la parte inferior del Selector de colores.
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (mejorado) Nivel AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nivel AA | W3C"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
