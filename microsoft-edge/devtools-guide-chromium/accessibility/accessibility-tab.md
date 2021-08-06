---
description: Probar la accesibilidad mediante la pestaña Accesibilidad.
title: Probar la accesibilidad con la pestaña Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 4e31b1f1a30c1328b6ef60bbe1b7c6d4c5a602859dee12ad45d0d3bd1cc9b387
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798503"
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
# <a name="test-accessibility-using-the-accessibility-tab"></a>Probar la accesibilidad con la pestaña Accesibilidad

La **pestaña Accesibilidad** es donde se ve el árbol de accesibilidad, los atributos ARIA y las propiedades de accesibilidad calculada de los nodos DOM.  

Para abrir la **pestaña Accesibilidad:**

1.  Seleccione la **herramienta** Elementos.  
1.  En el **árbol DOM,** seleccione el elemento que desea inspeccionar.  
1.  Seleccione la **pestaña Accesibilidad.**  Es posible que deba seleccionar primero el botón **Más pestañas** \( el botón Más pestañas \) a la derecha ![ de la ](../media/more-tabs-icon.msft.png) **pestaña** Estilos.

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspeccionar el elemento h1 de la página principal de DevTools en la pestaña Accesibilidad" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspeccionar el `h1` elemento de la página principal de DevTools en la pestaña **Accesibilidad**
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Ver la posición de un elemento en el árbol de accesibilidad

El [árbol de accesibilidad][MDNAccessibilityTree] es un subconjunto del árbol DOM.  El árbol de accesibilidad solo contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página a través de tecnologías de asistencia, como lectores de pantalla.

Inspeccione la posición de un elemento en el árbol de accesibilidad desde la **pestaña Accesibilidad.**  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Sección Árbol de accesibilidad" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Sección **Árbol de accesibilidad**  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a>Ver los atributos ARIA de un elemento  

Los atributos ARIA garantizan que las tecnologías de asistencia, como los lectores de pantalla, tengan toda la información que necesitan para representar correctamente el contenido de una página.  

Vea los atributos ARIA de un elemento en la **pestaña Accesibilidad.**

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Sección Atributos de ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Sección **Atributos de ARIA**  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a>Ver las propiedades de accesibilidad calculadas de un elemento  


El explorador calcula dinámicamente algunas propiedades de accesibilidad.  Estas propiedades se muestran en la **sección Propiedades calculadas** de la **pestaña Accesibilidad.**  

Vea las propiedades de accesibilidad calculadas de un elemento en la **pestaña Accesibilidad.**

> [!NOTE]
> Para las propiedades CSS calculadas, use la [pestaña Calculado.][DevtoolsCssReferenceViewActuallyAppliedElements]

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="La sección Propiedades calculadas de la pestaña Accesibilidad" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   La **sección Propiedades calculadas** de la **pestaña Accesibilidad**  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Ver solo el CSS que realmente se aplica a un elemento: referencia CSS | Microsoft Docs"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árbol de accesibilidad (AOM) | MDN"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
