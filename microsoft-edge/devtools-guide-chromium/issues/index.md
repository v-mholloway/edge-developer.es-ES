---
description: Use la herramienta Problemas para identificar y solucionar problemas con la página web actual.
title: Buscar y corregir problemas con la herramienta Problemas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 5e0147ae53f39d107be0f129793b2970676f213125dc38f3dfd5db971fe938b4
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11809876"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a>Buscar y corregir problemas con la herramienta Problemas

En Microsoft Edge DevTools, la **** herramienta Problemas analiza automáticamente la página web actual, informa de los problemas agrupados por tipo y proporciona documentación para ayudar a explicar y resolver los problemas.

La **herramienta Problemas** proporciona comentarios en las siguientes categorías:
*  Accesibilidad.
*  Compatibilidad entre exploradores.
*  Rendimiento.
*  Aplicaciones web progresivas.
*  Security.
*  Otros.

Varios orígenes **proporcionan** comentarios en la herramienta Problemas, como la plataforma Chromium, El eje Deque, los datos de compatibilidad del explorador MDN y la webhint.  Para obtener información sobre estos orígenes de comentarios que rellenan la **herramienta Problemas,** vaya a:
*  [Introducción a axe Tools][DequeAxe]
*  [repositorio browser-compat-data][MDNCompat]
*  [webhint][webhintIo]


## <a name="opening-the-issues-tool"></a>Abrir la herramienta Problemas

1.  Navegue a una página web que contenga problemas que corregir.  Por ejemplo, abra la página de demostración [de pruebas de accesibilidad][A11ytestingPagewitherrors] en una nueva pestaña o ventana.

1.  Abra DevTools.  Después de unos segundos, el contador **de** problemas \( Contador de problemas \) aparece en la ![ esquina superior derecha de ](../media/issues-counter-icon.msft.png) DevTools.

1.  Actualice la página, ya que algunos problemas se notifican en función de las solicitudes de red.  Observe el recuento actualizado en el **contador Problemas**.

1.  Seleccione el **contador Problemas**.  La **herramienta Problemas** se abre con problemas agrupados en distintas categorías.

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Categorías de problemas en la herramienta Problemas de la página de demostración" lightbox="../media/issues-tool-categories.msft.png":::
       Categorías de problemas en la herramienta Problemas de la página de demostración
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a>Otras formas de abrir la herramienta Problemas

Hay varias formas adicionales de abrir la **herramienta Problemas:**
*  Seleccione el **menú Más herramientas** ( ) en el panel principal o en el cajón y, a continuación, seleccione **+** **** **Problemas**.
*  Seleccione **Personalizar y controlar DevTools**Más  >  **herramientas**  >  **Problemas**.
*  En el árbol DOM de la **herramienta Elementos,** seleccione y, a continuación, haga clic en un nombre de elemento `Shift` ondulado subrayado.  O bien, abra el menú contextual en un elemento ondulado subrayado y, a continuación, **seleccione Ver problemas**.

### <a name="issues-are-automatically-ordered-by-severity"></a>Los problemas se ordenan automáticamente por gravedad

Dentro de cada categoría de problemas, primero se enumeran los errores, después las advertencias y, a continuación, las sugerencias.

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="La herramienta Problemas muestra problemas de rendimiento ordenados por gravedad" lightbox="../media/issues-ordered-by-severity.msft.png":::
   La **herramienta Problemas** muestra problemas de rendimiento ordenados por gravedad
:::image-end:::

### <a name="include-third-party-issues"></a>Incluir problemas de terceros

Para incluir problemas causados por sitios de terceros, **** en la parte superior de la herramienta Problemas, active la casilla Incluir problemas **de** terceros.


## <a name="expand-entries-in-the-issues-tool"></a>Expandir entradas en la herramienta Problemas

La **herramienta Problemas** presenta documentación adicional y correcciones recomendadas para aplicar a cada problema.  Para expandir un problema para obtener esta información adicional, seleccione un problema, como se muestra a continuación.

1.  Abra la [página de demostración][A11ytestingPagewitherrors] en una nueva ventana o pestaña y, a continuación, abra DevTools.

1.  Abra la **herramienta Problemas** seleccionando el **contador Problemas** \( Contador de ![ problemas ](../media/issues-counter-icon.msft.png) \).

1.  Seleccione un problema para expandir el problema.

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="La herramienta Problemas que muestra información adicional sobre cómo solucionar el problema" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       La **herramienta Problemas** que muestra información adicional sobre cómo solucionar el problema
    :::image-end:::

Cada problema mostrado tiene los siguientes componentes:
*   Un titular que describe el problema.
*   Una descripción que proporciona más contexto y soluciones propuestas.
*   Sección **RECURSOS AFECTADOS que** se vincula a recursos de DevTools, como la herramienta **Elementos,** **Orígenes** **o** Red.
*   Vínculos a documentación adicional.


## <a name="view-issues-in-context-of-an-associated-tool"></a>Ver problemas en el contexto de una herramienta asociada

Un problema en la **herramienta Problemas** puede incluir uno o más vínculos que abran distintas herramientas, como la **herramienta Elementos,** **Orígenes** **o** Red. Puede abrir una de estas herramientas para realizar pasos de solución de problemas adicionales. Para abrir una herramienta vinculada desde la **herramienta Problemas,** siga estos pasos.

1.  Como se describe en la sección anterior, abra la página de demostración y, a continuación, expanda un problema en la **herramienta** Problemas.

1.  En **RECURSOS AFECTADOS**Abra  >  **en**, seleccione el nombre de la herramienta.  El recurso afectado se muestra en la herramienta seleccionada.

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Seleccionar una herramienta para abrir un recurso afectado desde dentro de la herramienta Problemas" lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       Seleccionar una herramienta para abrir un recurso afectado desde dentro de la herramienta Problemas
    :::image-end:::

    Un problema expandido puede tener un **vínculo Red** para mostrar el recurso afectado en la **herramienta Red.**

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="La herramienta Red se abre al seleccionar un vínculo de recurso Red" lightbox="../media/issues-tab-view-issue.msft.png":::
    La **herramienta Red** se abre al seleccionar un vínculo de **recurso** Red
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a>Abrir problemas desde el árbol DOM

Si un elemento tiene un problema asociado, el árbol DOM de la **herramienta Elementos** muestra un subrayado ondulado bajo el nombre del elemento.  Puede abrir el menú contextual (hacer clic con el botón secundario) en el elemento y, a continuación, seleccionar Ver problemas **o**seleccionar y hacer clic izquierdo en el elemento con el `Shift` subrayado ondulado.

Para mostrar un problema para los elementos con subrayados ondulados en el árbol DOM, siga estos pasos.

1.  Abra una página, como la página [de demostración,][A11ytestingPagewitherrors]en una nueva pestaña o ventana.

1.  Abra DevTools y, a continuación, seleccione la **pestaña** Elementos.

1.  En el árbol DOM, expanda `<body>`  >  `<header>`  >  `<form>` .  Observe que el `<input>` elemento tiene un subrayado ondulado.

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Problemas con subrayado ondulado en el árbol DOM de la herramienta Elementos" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       Problemas con subrayado ondulado en el **árbol DOM** de la **herramienta** Elementos
    :::image-end:::

1.  Mantenga el mouse sobre el `<input>` elemento.  Una información sobre herramientas muestra información sobre el problema.

1.  Abra el menú contextual del elemento con el subrayado ondulado y, a continuación, **seleccione Ver problemas**.  La **herramienta** Problemas se abre y muestra el problema asociado con ese elemento.

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Detalles sobre los problemas de un elemento ondulado subrayado en el árbol DOM" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       Detalles sobre los problemas de un elemento ondulado subrayado en el **árbol DOM**
    :::image-end:::


## <a name="see-also"></a>Consulte también

* [Probar automáticamente una página web para problemas de accesibilidad](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página de demostración de pruebas de accesibilidad | Microsoft Docs"
[DequeAxe]: https://www.deque.com/axe "Axe Tools Overview | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "Datos de compatibilidad del explorador MDN | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/issues/index) y es creado por [Sam Dutton][SamDutton] \(Developer Advocate\).
[ ![ Creative Commons License][CCby4Image]][CCA4IL] Este trabajo se concede bajo una licencia de Creative Commons [Attribution 4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
