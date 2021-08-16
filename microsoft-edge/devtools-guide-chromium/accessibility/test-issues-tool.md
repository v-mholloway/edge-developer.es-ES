---
description: Pruebe automáticamente una página web para detectar problemas de accesibilidad mediante la sección Accesibilidad de la herramienta Problemas.
title: Probar automáticamente una página web para problemas de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: a70336b26184b81bb9f3db34d81e50a0c77fb6de
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893026"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a>Probar automáticamente una página web para problemas de accesibilidad

La **herramienta Problemas** incluye una sección **Accesibilidad** que notifica automáticamente problemas como la falta de texto alternativo en las imágenes, la falta de etiquetas en los campos de formulario y el contraste insuficiente de los colores del texto.  La **herramienta** Problemas se encuentra en el **cajón** en la parte inferior de DevTools.  En este artículo se usa la página web de demostración de pruebas de accesibilidad para realizar un paso adelante con la sección **Accesibilidad** de la **herramienta** Problemas.

Hay varias maneras de abrir la **herramienta Problemas,** como:
*  Seleccione el **contador de problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \) en la parte superior derecha de DevTools.
*  En la **herramienta Elementos,** en el árbol DOM, **pulse Mayús y** haga clic en un subrayado ondulado en un elemento.
*  En el **menú comando**, escriba `issues` y, a continuación, **seleccione Mostrar problemas**.


## <a name="view-the-accessibility-section-of-the-issues-tool"></a>Ver la sección Accesibilidad de la herramienta Problemas

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.  En la parte superior derecha, aparece **el contador de problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \).  El **contador de problemas** es un icono de burbuja de voz junto con el número de problemas detectados automáticamente.

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="El contador Problemas de DevTools, que indica cuántos problemas hay en el documento actual" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        El **contador Problemas** de DevTools, que indica cuántos problemas hay en el documento actual
    :::image-end:::

1.  Actualice la página, ya que algunos problemas se notifican en función de las solicitudes de red.  Observe el recuento actualizado en el **contador Problemas**.

1.  Seleccione el **contador Problemas**.  Se **abre** la herramienta Problemas, en el **cajón** situado en la parte inferior de DevTools.

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Advertencias de accesibilidad mostradas en la herramienta Problemas" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        Advertencias de accesibilidad mostradas en la herramienta Problemas
    :::image-end:::

1.  En la **pestaña Problemas,** expanda la **sección Accesibilidad.**


## <a name="verify-that-input-fields-have-labels"></a>Comprobar que los campos de entrada tienen etiquetas

Para comprobar si los campos de entrada **** tienen etiquetas conectadas, use la herramienta Problemas, que comprueba automáticamente toda la página web e informa de este problema en la **sección Accesibilidad.**

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  En la parte superior derecha, seleccione el **contador de problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \).  Se **abre** la herramienta Problemas, en el **cajón** situado en la parte inferior de DevTools.

1.  En la **pestaña Problemas,** expanda la **sección Accesibilidad.**

1.  Expanda la **advertencia** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .

1. Seleccione el **vínculo Abrir en elementos.**

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Herramienta Elementos que muestra el HTML problemático después de seleccionar el vínculo en la herramienta Problemas" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        Herramienta Elementos que muestra el HTML problemático después de seleccionar el vínculo en la **herramienta** Problemas :::image-end:::

    Se **abre** la herramienta Elementos, con el elemento resaltado en el árbol DOM.  El **panel Estilos** muestra las reglas CSS aplicadas para el elemento.  Ahora se muestra el siguiente código.

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    En el código anterior, el elemento se usa incorrectamente, ya que no hay conexión `label` entre el elemento y un elemento `label` `input` determinado.  Para conectar el `label` elemento a un elemento `input` específico, use cualquiera de las siguientes opciones.
    *   Anide `input` el elemento dentro del `label` elemento.
    *   En el `label` elemento, agregue un `for` atributo que coincida con un atributo del `id` `input` elemento.

    También hay otra forma de probar la falta de conexiones entre elementos. En la **herramienta Elementos,** seleccione el `<label>Search</label>` elemento en el árbol DOM.  En la página web, observe que el foco solo aparece en la **etiqueta de** búsqueda y no en el cuadro de texto de entrada.  La implementación correcta se centraría en el `search` cuadro de texto de entrada y la **etiqueta** de búsqueda.

1.  Como ejemplo de una conexión correcta, seleccione la **etiqueta Otro** en el formulario de donación.  Un cuadro de indicador de foco aparece correctamente **** en el cuadro de texto de entrada junto a la etiqueta Otros, ya que hay valores de atributo `for` y `id` coincidencia.

1.  En la **herramienta Problemas,** seleccione **Más lectura** para obtener más información sobre el problema.  Para abrir el vínculo en una nueva pestaña, **haga**clic en el vínculo en Windows/Linux o comando haga clic en + **** el vínculo en **** + **** macOS.

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Vínculo en la pestaña Problemas que apunta a información más detallada sobre el problema" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        Vínculo en la **pestaña Problemas** que apunta a información más detallada sobre el problema
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a>Comprobar que las imágenes tienen texto alternativo

Las pruebas básicas de accesibilidad requieren asegurarse de que se proporciona texto alternativo (también denominado _texto_alternativo) para las imágenes.

Para comprobar automáticamente si se proporciona texto alternativo para imágenes, use la herramienta **Problemas,** que tiene una sección **Accesibilidad.**  La **herramienta** Problemas se encuentra en el **cajón** en la parte inferior de DevTools.

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Para abrir la **herramienta Problemas,** seleccione el contador **Problemas** en la esquina superior derecha de DevTools.

1.  En la **pestaña Problemas,** expanda la advertencia `Images must have alternate text: Element has no title attribute` .  Hay cuatro instancias de imágenes que carecen de texto alternativo.

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="Las imágenes de informes de la herramienta Problemas a las que les falta texto alternativo" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        Las imágenes de informes de la herramienta Problemas a las que les falta texto alternativo
    :::image-end:::

Para obtener más información, vaya [a Imágenes debe tener texto alternativo.](https://dequeuniversity.com/rules/axe/4.1/image-alt)


## <a name="verify-that-text-colors-have-enough-contrast"></a>Comprobar que los colores de texto tienen suficiente contraste

Para comprobar automáticamente si los colores de texto tienen suficiente contraste, use la **herramienta Problemas,** que tiene una sección **Accesibilidad.**  La **herramienta** Problemas se encuentra en el **cajón** en la parte inferior de DevTools.

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Para abrir la **herramienta Problemas,** seleccione el contador **Problemas** en la esquina superior derecha de DevTools.  Es posible que recibas advertencias de que dos elementos de la página web de demostración no tienen suficiente contraste.

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problemas de contraste notificados en la herramienta Problemas" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        Problemas de contraste notificados en la herramienta Problemas
    :::image-end:::

1.  Según la configuración, la pestaña **Problemas** puede tener una advertencia como que los usuarios pueden tener dificultades para leer contenido de texto debido a un contraste de **color insuficiente.**   Puede expandir esa advertencia y, a continuación, expandir **Recursos afectados**.  Aparece una lista de elementos con una lista de elementos que no tienen suficiente contraste.


1.  Seleccione el `li.high` elemento.  En la página web que se representa, se resalta el vínculo **Perros** de la sección **Donar,** que muestra una pequeña superposición de información.  Esta es la misma superposición que aparece al pasar el puntero sobre un elemento del árbol DOM de la **herramienta** Elementos.

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Elemento de la página web resaltado después de seleccionar un vínculo en la sección Recursos afectados" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        Elemento de la página web resaltado después de seleccionar un vínculo en la **sección Recursos afectados**
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Los subrayados ondulados en el árbol DOM indican problemas detectados automáticamente 

El árbol DOM de la **herramienta Elementos** marca los problemas directamente en el HTML con subrayados ondulados.  La herramienta **Problemas** notifica estos problemas.  Al **mayús+clic en** cualquier elemento con un subrayado ondulado, se muestra **la herramienta** Problemas.

1.  En la **herramienta Elementos,** en el árbol DOM, **pulse Mayús y** haga clic en el elemento , que tiene una línea `<input type="search">` ondulada debajo `input` de .  Se **muestra la herramienta** Problemas y se muestra el problema de ese elemento.

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Un elemento que tiene un subrayado ondulado en la vista DOM tiene un problema" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        Un elemento que tiene un subrayado ondulado en la vista DOM tiene un problema
    :::image-end:::


## <a name="see-also"></a>Vea también

*  [Buscar y corregir problemas con la herramienta Problemas][DevToolsIssuesTool]
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
