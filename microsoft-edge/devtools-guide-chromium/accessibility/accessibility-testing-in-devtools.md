---
description: Introducción a las pruebas de problemas de accesibilidad con DevTools
title: Información general sobre las pruebas de accesibilidad con DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 3630d8bf51a5b56ac4fd5d2ddbe56243b765660201286956f0c89cb75f3bf1cb
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803272"
---
# <a name="overview-of-accessibility-testing-using-devtools"></a>Información general sobre las pruebas de accesibilidad con DevTools

En este artículo, tratamos algunas de las características que puede usar en DevTools para probar problemas de accesibilidad.  Vamos a través del uso de diferentes características de DevTools para detectar los problemas de accesibilidad en una página de demostración y analizamos cómo solucionarlos.  Abre la [página de demostración][DevToolsA11yErrorsDemopage] en una pestaña nueva para probarla tú mismo y puedes probarla.

:::image type="complex" source="../media/a11y-testing-basics-demopage.msft.png" alt-text="La página de demostración usada en este artículo con algunos problemas de accesibilidad" lightbox="../media/a11y-testing-basics-demopage.msft.png":::
    La página de demostración usada en este artículo con algunos problemas de accesibilidad
:::image-end:::


## <a name="automated-testing-by-using-the-issues-tool"></a>Pruebas automatizadas mediante la herramienta Problemas

Cuando abra la página de demostración en el explorador y abra DevTools, observe que algunos problemas se detectan automáticamente en el **contador de problemas**.  Seleccione el **contador de problemas** \( Contador de problemas \) para abrir la herramienta ![ ](../media/issues-counter-icon.msft.png) [Problemas][DevToolsIssuesTool] para ver los problemas y obtener más información.

:::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="El contador De problemas muestra cuántos problemas hay en la página web actual y abre la herramienta Problemas" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
    El contador De problemas muestra cuántos problemas hay en la página web actual y abre la herramienta Problemas
:::image-end:::

Para este artículo, nos centraremos en la sección **Accesibilidad** de la **herramienta Problemas.**

:::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Advertencias de accesibilidad mostradas en la herramienta Problemas" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
    Advertencias de accesibilidad mostradas en la herramienta Problemas
:::image-end:::

Para ver los pasos detallados del tutorial, vaya [a Ver la sección Accesibilidad de la herramienta Problemas][DevToolsAccessibilityTestIssuesToolViewAccSection].


### <a name="automatically-checking-that-input-fields-have-labels"></a>Comprobar automáticamente que los campos de entrada tienen etiquetas

La primera advertencia que se muestra es `Form elements must have labels: Element has no title attribute. Element has no placeholder attribute` .  Al expandir esta sección y, a continuación, seleccionar el vínculo Abrir en elementos, se abre la herramienta **Elementos,** con el elemento resaltado en el árbol DOM. ****  La **pestaña Estilos** muestra el CSS que se aplica al elemento.

Para ver los pasos detallados del tutorial, vaya [a Comprobar que los campos de entrada tienen etiquetas][DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels].

:::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Herramienta Elementos que muestra el HTML problemático después de seleccionar el vínculo en la herramienta Problemas" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
    Herramienta Elementos que muestra el HTML problemático después de seleccionar el vínculo en la herramienta Problemas
:::image-end:::

En este caso, el HTML tiene un `label` elemento que no funciona.

```html
<label>Search</label>
<input type="search">
<input type="submit" value="go">
```

El uso del elemento aquí es incorrecto, ya que no hay `label` ninguna conexión entre el elemento y el `label` `input` elemento.  Una etiqueta HTML válida colocaría el foco en el cuadro de texto de entrada de búsqueda al seleccionar la **etiqueta** de búsqueda. 

Puede solucionar este problema anidando el elemento en un elemento o agregando un atributo que señala `input` a un atributo del `label` `for` `id` `input` elemento.  Para ver una conexión correcta, seleccione la **etiqueta Otro** en el formulario de donación.

También puede seleccionar los vínculos explicativos de la **herramienta Problemas** para obtener esta información.

:::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Vínculos en la herramienta Problemas que apuntan a información más detallada sobre el problema" lightbox="../media/a11y-testing-more-information-links.msft.png":::
    Vínculos en la **herramienta Problemas** que apuntan a información más detallada sobre el problema
:::image-end:::


### <a name="automatically-checking-that-images-have-alt-text"></a>Comprobar automáticamente que las imágenes tienen texto alternativo

El otro problema detectado automáticamente es que muchas de las imágenes de la página no tienen texto alternativo.  Si expandes la `Images must have alternate text: Element has no title attribute` advertencia, obtienes cuatro instancias de imágenes con ese problema.

:::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="La herramienta Problemas, reporting images with missing alternative text" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
    La **herramienta Problemas,** reporting images with missing alternative text
:::image-end:::

Para ver los pasos detallados del tutorial, vaya a [Comprobar que las imágenes tienen texto alternativo][DevtoolsAccessibilityTestIssuesToolCheckAltText].


### <a name="automatically-checking-that-text-colors-have-enough-contrast"></a>Comprobar automáticamente que los colores de texto tienen suficiente contraste

La **herramienta Problemas** también informa cuando dos elementos de la página no tienen suficiente contraste.

:::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problemas de contraste notificados en la herramienta Problemas" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
    Problemas de contraste notificados en la **herramienta** Problemas
:::image-end:::

La **herramienta Problemas** proporciona explicaciones detalladas de la advertencia.  Al explorar en profundidad, obtiene una lista de los elementos que tienen este problema.  En la **herramienta Problemas,** al seleccionar un vínculo que apunta a un elemento, se resaltará ese elemento en la página representada.

:::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Elemento de la página resaltado después de seleccionar el vínculo a él" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
    Elemento de la página resaltado después de seleccionar el vínculo a él
:::image-end:::

Para ver los pasos detallados del tutorial, vaya a [Comprobar que los colores del texto tienen suficiente contraste][DevtoolsAccessibilityTestIssuesToolCheckContrast].


### <a name="verify-that-the-webpage-layout-is-usable-when-narrow"></a>Comprobar que el diseño de la página web es utilizable cuando es estrecho

<!-- by design, this section doesn't have a corresponding how-to article -->

Una parte importante de la accesibilidad es asegurarse de que los productos web funcionan bien en una ventanilla estrecha. Muchos usuarios necesitan acercar la página para poder usarla, lo que significa que no queda mucho espacio. Cuando no hay suficiente espacio, el diseño de varias columnas debe convertirse en un diseño de una sola columna, con contenido colocado en un orden comprensible. Esto significa colocar el contenido más importante en la parte superior de la página y colocar contenido adicional más abajo en la página.

Al restringir la ventana del explorador y usar las teclas de flecha para desplazarse por la página, puede ver que la barra de navegación superior de la página de demostración tiene algunos problemas de accesibilidad.  La barra de navegación superior se superpone al **formulario** de búsqueda, como se muestra en la imagen anterior, y ese problema debe solucionarse.

Puedes simular una ventanilla estrecha al cambiar el tamaño de la ventana del explorador, pero una mejor manera de probar la capacidad de respuesta del diseño es usar la herramienta **emulación de** dispositivos.  Estas son algunas características de la herramienta **emulación de** dispositivos que te ayudan a encontrar problemas de accesibilidad de cualquier sitio web:

*  Sin cambiar el tamaño de la ventana del explorador, cambie el tamaño de la página y compruebe si las consultas multimedia [CSS][DevToolsMediaQueries] desencadenan un cambio en el diseño.
*  Compruebe las dependencias que usan un mouse. De forma predeterminada, la emulación del dispositivo supone que es un dispositivo táctil. Esto significa que las funciones del producto que se basen en la interacción del mouse no funcionarán. 
*  Realice pruebas visuales simulando diferentes dispositivos, niveles de zoom y relaciones de píxeles.
*  Pruebe cómo se comporta el producto en conexiones no confiables o cuando el usuario está sin conexión.  Mostrar las interacciones más importantes para un usuario en una conexión lenta también es una consideración de accesibilidad.

Para obtener más información sobre la **herramienta emulación de** dispositivos, vaya a [Emular dispositivos móviles en Microsoft Edge DevTools][DevToolsDeviceModeIndex].


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Los subrayados ondulados en el árbol DOM indican problemas detectados automáticamente

El árbol DOM de la **herramienta Elementos** marca automáticamente los problemas directamente en el HTML agregando un subrayado ondulado.  Si tiene `Shift` + `click` algún elemento que tenga un subrayado ondulado, se abrirá **la herramienta** Problemas.

:::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Un elemento que se muestra con subrayado ondulado en el árbol DOM tiene problemas.  Mayús y haga clic en el elemento para llegar directamente al problema" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
    Un elemento que se muestra con subrayado ondulado en el árbol DOM tiene problemas.  `Shift`+`click` el elemento para obtener directamente al problema.
:::image-end:::

Estos problemas encontrados por la herramienta **Problemas** son algunos problemas de accesibilidad relativamente obvios que se pueden evitar.  El uso **de la herramienta** Problemas y sus explicaciones guiadas para solucionarlos te pone en camino hacia un producto accesible.


## <a name="limits-of-automated-testing"></a>Límites de las pruebas automatizadas

Las [herramientas Problemas,][DevToolsIssuesTool] [Accesibilidad Ideas][AccessibilityInsights]y [Faro][Lighthouse] son herramientas que generan automáticamente un informe de accesibilidad para una página web.  Obtener un informe automatizado de estas herramientas es solo el principio del recorrido de pruebas de accesibilidad.

La accesibilidad se trata de la interacción humana: personas con necesidades diferentes que usan sus productos en distintos entornos técnicos.  Esta prueba no se puede automatizar por completo, pero necesita la comprobación de un usuario que navega por el producto.  En el mejor escenario, tendrías acceso a evaluadores con diferentes necesidades de accesibilidad y evaluadores con diversos entornos.  Pero ya puedes hacer mucho tú mismo usando el teclado para navegar e inspeccionando diferentes partes de la página.

En la página de demostración, hay problemas adicionales que las pruebas automatizadas no pueden detectar, como: 

*  Problemas que surgen después de interactuar con la página. 
*  Problemas relacionados con los cambios en la pantalla, como restringir la ventana.

Uno de esos problemas es el formulario de donación.  Cuando usas un mouse, puedes hacer clic en las distintas opciones para donar dinero.  Pero cuando intentas usar el teclado para acceder al formulario de donación, no pasa nada. Para solucionar este problema, debe usar la **herramienta Inspeccionar.**

:::image type="complex" source="../media/a11y-testing-basics-donation-form-issue.msft.png" alt-text="Se resalta el formulario de donación en la página de demostración" lightbox="../media/a11y-testing-basics-donation-form-issue.msft.png":::
    Se resalta el formulario de donación en la página de demostración
:::image-end:::


## <a name="using-the-inspect-tool-to-detect-accessibility-issues"></a>Uso de la herramienta Inspeccionar para detectar problemas de accesibilidad

Usa la **herramienta Inspeccionar** para detectar problemas de accesibilidad al pasar el mouse sobre partes de la página web.  La **herramienta Inspeccionar** \( Inspeccionar \) se encuentra en la esquina superior izquierda de ![ ](../media/inspect-icon.msft.png) DevTools.  Active la herramienta Inspeccionar seleccionando el **botón Inspeccionar** herramienta.

:::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Active la herramienta Inspeccionar seleccionando el botón Inspeccionar herramienta" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
    Active la herramienta **Inspeccionar** seleccionando el **botón Inspeccionar** herramienta
:::image-end:::

Después de seleccionar el **botón Inspeccionar** herramienta, puede mover el puntero sobre cualquier elemento de la página representada.  La herramienta Inspeccionar muestra el diseño del elemento como una superposición de flexbox multicolor y muestra los detalles del elemento como una superposición de información similar a una información sobre herramientas.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Superposición de flexbox multicolor y superposición de información al usar la herramienta Inspeccionar" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Superposición de flexbox multicolor y superposición de información al usar **la herramienta Inspeccionar**
:::image-end:::

La sección Accesibilidad de la herramienta **Inspeccionar** incluye una **línea contraste,** cuando corresponda.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="La sección Accesibilidad de la herramienta Inspeccionar incluye una línea de contraste, cuando corresponda" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    La sección Accesibilidad de la herramienta **Inspeccionar** incluye una **línea de** contraste, cuando corresponda
:::image-end:::

Para ver los pasos detallados del tutorial, vaya a [Identificar regiones anidadas mediante el resaltado de color][DevtoolsAccessibilityTestInspectToolColorHighlighting].
<!-- = test-inspect-tool.md##identify-nested-regions-using-color-highlighting -->

La sección superior de la **superposición de** información de la herramienta Inspeccionar muestra la siguiente información:

* Tipo de diseño; si el elemento se coloca mediante un flexbox o una cuadrícula, verá un icono adecuado \(![Icono de diseño de cuadrícula](../media/grid-icon.msft.png)\).
* El nombre del elemento, como **,** **h1**o **div**.
* Las dimensiones del elemento, en píxeles.
* El color, como una muestra de color (un cuadrado pequeño y coloreado) y como un valor con formato (como `#336699` ).
* Información de fuente (familias de fuentes y tamaño).
* Margen y relleno, en píxeles.

La **parte accesibilidad** de la **superposición Inspeccionar** se describe en la sección siguiente.


### <a name="checking-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Comprobación de elementos individuales para contraste de texto, texto del lector de pantalla y compatibilidad con teclado

La **sección Accesibilidad** de la **superposición Inspeccionar** contiene las siguientes filas:

*   **El** contraste define si un elemento puede ser comprendido por personas con visión deficiente.
    *   La [relación de contraste][W3CContrastRatio] definida por las Directrices de [WCAG][WCAG] indica si hay suficiente contraste entre el texto y los colores de fondo.  Un icono de marca de verificación verde indica que hay suficiente contraste y un icono de signo de exclamación naranja indica que no hay suficiente contraste.

*   **Name** y **Role indican** qué tecnología de asistencia de información, como los lectores de pantalla, informarán sobre el elemento.
    *   Name **es** el contenido de texto de un `a` elemento.  Para el elemento `<a href="/">About Us</a>` , el nombre **que** se muestra en la herramienta Inspeccionar es "Acerca de nosotros".
    *   Role **** del elemento.  El **rol** suele ser el nombre del elemento, como `article` , , o `img` `link` `heading` .  Los `div` elementos y se representan como `span` `generic` .

*   **El enfoque de teclado** indica si los usuarios pueden llegar al elemento con dispositivos de entrada distintos de un mouse.
    *   Un icono de marca de verificación verde indica que el elemento se puede centrar en el teclado.
    *   Un círculo gris con línea diagonal indica que el elemento no se puede centrar en el teclado.

Para ver los pasos detallados del tutorial, vaya a Comprobar elementos individuales para el contraste de texto, el texto del lector de [pantalla y la compatibilidad con el teclado.][DevtoolsAccessibilityTestInspectToolIndivElems]
<!-- = test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support -->


### <a name="using-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Uso de la herramienta Inspeccionar para desplazarse por la página web para resaltar el DOM y CSS

Al usar la **herramienta Inspeccionar,** al seleccionar un elemento en la página representada se abre la **herramienta** Elementos.  El árbol DOM muestra el HTML del elemento y **Styles** muestra las propiedades CSS que se aplican al elemento.

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Detalles sobre el elemento seleccionado que se muestra en la herramienta Elementos" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Detalles sobre el elemento seleccionado que se muestra en la herramienta Elementos
:::image-end:::

Al usar la **herramienta Inspeccionar,** al pasar el mouse sobre distintas partes de la página renderizada con **elementos** abiertos, observará que el árbol DOM se actualiza automáticamente.

Para ver los pasos detallados del tutorial, vaya a Usar la herramienta Inspeccionar para [desplazarse][DevtoolsAccessibilityTestInspectToolDomCss]por la página web para resaltar el DOM y CSS .
<!-- = test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css -->


## <a name="verify-keyboard-support-by-using-the-tab-and-enter-keys"></a>Comprobar la compatibilidad con el teclado con las teclas Tab y Enter

No todas las personas usan dispositivos táctiles o de puntero, y algunas personas pueden tener una visión baja. Para satisfacer estos escenarios, asegúrese de que las URI funcionan con teclados.

Puede probar con un teclado para navegar por la página mediante `Tab` o para saltar de un elemento a `Shift+Tab` otro.  Si presiona en `Tab` la página de demostración, lo primero que recibe el foco es el **formulario de** búsqueda en el encabezado de página.  Presionar incluso permite enviar el formulario, de modo que funcione, a pesar del problema de etiqueta que descubrimos anteriormente al `Enter` usar la **herramienta** Problemas.

Para ver los pasos detallados del tutorial, vaya a Comprobar la compatibilidad con el teclado mediante las [teclas Tab y Enter](test-tab-enter-keys.md).

Al presionar en lugar de , el siguiente elemento que obtiene el foco es el primer vínculo Más de la sección de contenido de la página, tal como se indica `Tab` `Enter` en un esquema. ****

:::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navegar por la página mediante la tecla Tab.  El foco se muestra en un vínculo Más de la página." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
    Navegar por la página mediante la `Tab` clave.  El foco se muestra en un **vínculo Más** de la página.
:::image-end:::

Después de pasar por el último vínculo **Más,** la página se desplaza hacia arriba y no está claro qué elemento tiene el foco.

Si observa la parte inferior izquierda de la pantalla o si usa un lector de pantalla, puede saber que el vínculo **azul Gatos** del menú de navegación de la barra lateral tiene el foco, ya que el explorador muestra la dirección URL `#cats` .

:::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="La falta de estilo de foco hace imposible saber dónde se encuentra actualmente en la página.  La única sugerencia es la presentación del destino del vínculo en la parte inferior izquierda de la ventana." lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
    La falta de estilo de foco hace imposible saber dónde se encuentra actualmente en la página.  La única sugerencia es la presentación del destino del vínculo en la parte inferior izquierda de la ventana.
:::image-end:::

La selección `Tab` de nuevo te lleva al cuadro de texto de entrada del formulario de donación.  Sin embargo, no puede alcanzar los **50**, **100** **o 200** botones encima del cuadro de texto de entrada.  Además, cuando el foco está en ese cuadro de texto de entrada, la selección `Enter` no envía el formulario.

:::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="El único elemento accesible para teclado en el formulario de donación es el campo de texto de entrada" lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
    El único elemento accesible con teclado en el formulario de donación es el campo de texto
:::image-end:::

La selección vuelve a poner el foco en la barra de navegación superior, donde puede seleccionar ir a una sección diferente de la página o a otra página `Tab` `Enter` del sitio.  Sabes en qué elemento estás, porque hay un esquema de enfoque.  Para seleccionar un vínculo en la barra de navegación superior, use `Tab` o ponga el foco en un vínculo y, a `Shift+Tab` continuación, seleccione `Enter` .

:::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="La barra de navegación superior tiene un resaltado y un esquema de enfoque, por lo que es accesible con teclado" lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
    La barra de navegación superior tiene un resaltado y un esquema de enfoque, por lo que es accesible con teclado
:::image-end:::

Hemos encontrado algunos problemas aquí para solucionar:

* El menú de navegación de la barra lateral no muestra a los usuarios dónde está el foco, al usar `Tab` teclados para moverse por la página.
* En el formulario de donación, los botones **50, 100, ** y **200** y la funcionalidad de envío de formulario no funcionan al usar el teclado.
* El orden de tabulación del teclado es incorrecto. La `Tab` tecla navega por todos los vínculos **Más** de la página antes del menú de navegación de la barra lateral.  Este orden no es útil porque la navegación de la barra lateral está diseñada para llevarte a `Tab` las diferentes secciones de esa página. 

Analicemos estos problemas con DevTools.


## <a name="analyze-keyboard-accessibility-issues-using-devtools"></a>Analizar problemas de accesibilidad de teclado con DevTools


### <a name="analyzing-the-lack-of-indication-of-keyboard-focus-in-the-sidebar-menu"></a>Analizar la falta de indicación del foco del teclado en el menú lateral

Para averiguar por qué la navegación de la barra lateral no está optimizada como se esperaba para su uso con teclados, comience con la herramienta **Inspeccionar** para resaltar un vínculo en el menú de navegación de la barra lateral y, a continuación, explore el árbol DOM para el `a` elemento. 

:::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspeccionar el código fuente y los estilos aplicados de un vínculo en el menú de navegación de la barra lateral" lightbox="../media/a11y-testing-menu-link.msft.png":::
    Inspeccionar el código fuente y los estilos aplicados de un vínculo en el menú de navegación de la barra lateral
:::image-end:::

En la **pestaña Estilos,** puede ver el CSS que se aplica al vínculo y, si selecciona el vínculo a , el archivo se abrirá en la `styles.css` **herramienta** Orígenes.

:::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Los estilos que se aplican al vínculo, que se muestran en la herramienta Orígenes" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
    Los estilos que se aplican al vínculo, que se muestran en la herramienta Orígenes
:::image-end:::

En el ejemplo anterior, los estilos de la página incluyen un estado en el elemento de menú cuando se usa un mouse, pero no hay ningún estado en el CSS para los usuarios `hover` `focus` de teclado.  

Además, en este ejemplo, los vínculos usan `outline: none` . Este estilo se usa para quitar el esquema que los exploradores agregan automáticamente a los elementos cuando tienen foco y se usan teclados.  Para evitar este problema, no use `outline: none` .

Para ver los pasos detallados del tutorial, vaya a Analizar la falta de indicación del foco [del teclado en un menú de la barra lateral.](test-analyze-no-focus-indicator.md)


### <a name="analyzing-the-lack-of-keyboard-support-in-the-donation-form"></a>Analizar la falta de compatibilidad con teclado en el formulario de donación

Los botones del formulario de donación se implementan con el elemento, que las herramientas de prueba automatizadas no reconocen como `div` control en un formulario.

Para investigar esto, puedes usar la herramienta **Inspeccionar** para pasar el puntero sobre los botones del formulario de donación.  El resultado es que ninguno de ellos es accesible para teclado, como indica el anillo gris de la línea que se puede centrar en el teclado de la superposición de información. ****  Como se muestra **** en las líneas **Nombre** y Rol de la superposición de información, los botones del formulario de donación tampoco tienen nombre y tienen un rol de (representación o elementos), lo que significa que no son accesibles para la tecnología de `generic` `div` `span` asistencia.

:::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Al inspeccionar los botones del formulario, se muestra que no son accesibles con teclado" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
    Al inspeccionar los botones del formulario, se muestra que no son accesibles con teclado
:::image-end:::

Para ver los pasos detallados del tutorial, vaya a Analizar la falta de compatibilidad [con el teclado en un formulario](test-analyze-no-keyboard-support.md).

Si selecciona el botón **Donar,** la herramienta **Inspeccionar** le llevará a la **herramienta Elementos** y le mostrará el HTML del formulario.

```HTML
<div class="donationrow">
    <div class="donationbutton">50</div>
    <div class="donationbutton">100</div>
    <div class="donationbutton">200</div>
</div>
<div class="donationrow">
    <label for="freedonation">Other</label>
    <input id="freedonation" class="smallinput">
</div>
<div class="donationrow">
    <div class="submitbutton">Donate</div>
</div>
```

El uso de los elementos and es válido, lo que hace que la etiqueta funcione como se pretende y el cuadro de `label` texto es accesible con `input` `input` teclado.  El resto del formulario usa `div` elementos, que son fáciles de aplicar pero que no tienen ningún significado semántico.

A continuación, vamos a analizar la funcionalidad de JavaScript del formulario. En **Elementos,** seleccione la **pestaña Escuchas de eventos** para analizar el JavaScript del formulario.

:::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="La pestaña Escuchas de eventos, con un vínculo al JavaScript para el formulario" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
    La **pestaña Escuchas de eventos,** con un vínculo al JavaScript para el formulario
:::image-end:::

En la **pestaña Escuchas de** eventos, seleccione el vínculo para abrir la herramienta Orígenes y, a continuación, inspeccione el JavaScript responsable de la funcionalidad `buttons.js:18` del formulario. ****

:::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="JavaScript responsable de la funcionalidad del formulario de donación, que se muestra en la herramienta Orígenes" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
    JavaScript responsable de la funcionalidad del formulario de donación, que se muestra en la **herramienta Orígenes**
:::image-end:::

Se recomienda usar eventos con botones porque los eventos funcionan `click` `click` con punteros del mouse y teclados.  Sin embargo, dado que un elemento no es accesible para teclado y el botón Donar se implementa como elemento, este JavaScript solo se ejecuta cuando se usa `div` un **** `div` mouse.

El uso de un botón como un es un ejemplo clásico donde se necesita JavaScript adicional `div` para crear la funcionalidad que proporcionan los `button` elementos. Como resultado, esto conduce a una experiencia que es inaccesible.


### <a name="checking-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Comprobar la compatibilidad con el teclado y el lector de pantalla en el árbol de accesibilidad

El uso **de la herramienta Inspeccionar** para comprobar individualmente cada elemento de la página requiere mucho tiempo.  En su lugar, use **la pestaña Accesibilidad** para navegar por el árbol **de accesibilidad de la página.**  El Árbol de accesibilidad indica qué información proporciona la página a la tecnología de asistencia, como los lectores de pantalla.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Botón formulario de donación en el árbol de accesibilidad" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Botón formulario de donación en el **árbol de accesibilidad**
:::image-end:::

Cualquier elemento del árbol que no tenga un nombre o que tenga un rol de , es un problema, ya que ese elemento no estará disponible para los usuarios del teclado ni para las personas que usan tecnología de `generic` asistencia.

Para ver los pasos detallados del tutorial, vaya a [Comprobar el árbol de accesibilidad](test-accessibility-tree.md)para la compatibilidad con el teclado y el lector de pantalla.


### <a name="analyzing-the-order-of-keyboard-access-to-sections-of-the-page"></a>Análisis del orden de acceso de teclado a las secciones de la página

Otro problema es el orden de tabulación no claro en la página.  Los usuarios de teclado llegan al menú de navegación de la barra lateral solo después de realizar tabulaciones a través de todos los **vínculos Más** de toda la página.  En este ejemplo, el menú de navegación de la barra lateral está pensado para ser un acceso directo a distintas secciones de esa página.  Este orden de tabulación lleva a una mala experiencia del usuario. 

La razón del orden `Tab` confuso es que está determinado por el orden de origen del documento.  El orden de tabulación también se puede modificar mediante el atributo de un elemento que quita ese `tabindex` elemento del orden de origen predeterminado.

En el código fuente del documento, el menú de navegación de la barra lateral aparece después del contenido principal de la página.  El menú de navegación de la barra lateral aparece encima del contenido principal de la página solo porque el menú de navegación de la barra lateral se ha posicionado mediante CSS.

El orden de origen de un documento es importante para la tecnología de asistencia y puede ser diferente del orden en que aparecen los elementos en la página representada.  Con CSS, puede volver a ordenar los elementos de página de forma visual, pero eso no significa que la tecnología de asistencia, como los lectores de pantalla, represente los elementos de página en el mismo orden que ese CSS.

Puede probar el orden de los elementos de página mediante el Visor de pedidos **de origen** en la **pestaña Accesibilidad.**  Desplácese hacia abajo hasta el final y active la **casilla Mostrar orden de** origen.  Ahora, al navegar por el árbol DOM en la herramienta **Elementos,** como seleccionar el elemento, las superposiciones numéricas se muestran en secciones de la página que representan el orden `header` de origen. 

:::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Al activar el Visor de pedidos de origen se muestra el orden de los elementos del código fuente como superposiciones numéricas en la página" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
    Al activar el **Visor de pedidos de** origen se muestra el orden de los elementos del código fuente como superposiciones numéricas en la página
:::image-end:::

Para ver los pasos detallados del tutorial, vaya a Probar compatibilidad [con teclado mediante el Visor de pedidos de origen](test-tab-key-source-order-viewer.md).


## <a name="testing-contrast-of-text-colors-in-various-states"></a>Probar el contraste de colores de texto en varios estados

La **herramienta Inspeccionar** informa de problemas de accesibilidad de un estado a la vez.  En primer lugar, describiremos la limitación de usar la herramienta Inspeccionar para ver solo el estado estático de un elemento page.  A continuación, explicaremos cómo inspeccionar otros estados de un elemento de página **seleccionando \:hov (Toggle Element State)** en la **pestaña Estilos.**

### <a name="checking-text-color-contrast-in-the-default-state"></a>Comprobar el contraste de color del texto en el estado predeterminado

Además de las pruebas automáticas de contraste de color en la herramienta **Problemas,** también puede usar la herramienta **Inspeccionar** para comprobar si los elementos de página individuales tienen suficiente contraste.  Si la información de contraste está disponible, la superposición **Inspeccionar** muestra la relación de contraste y un elemento de casilla.  Un icono de marca de verificación verde indica que hay suficiente contraste y un icono de alerta amarilla indica que no hay suficiente contraste.

Por ejemplo, los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, pero el elemento verde de la lista **Perros** de la sección Estado **de** donación no lo hace.  Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la **superposición Inspeccionar.**

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, como se muestra en la superposición Inspeccionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, como se muestra en **la superposición Inspeccionar** :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la superposición Inspeccionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la **superposición Inspeccionar** :::image-end:::
    :::column-end:::
:::row-end:::

El uso **de la** herramienta Inspeccionar de esta manera no prueba completamente los elementos. Los elementos de la página pueden tener estados diferentes, todos los cuales deben probarse. Por ejemplo, si mantienes el mouse sobre el menú de navegación de la barra lateral, observa la animación que cambia el color de los vínculos.

:::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Elemento de menú que muestra diferentes colores cuando el puntero del mouse está sobre él" lightbox="../media/a11y-testing-hover.msft.png":::
    Elemento de menú que muestra diferentes colores cuando el puntero del mouse está sobre él
:::image-end:::

### <a name="verify-accessibility-of-all-states-of-elements-such-as-the-contrast-on-hover"></a>Comprobar la accesibilidad de todos los estados de elementos, como el contraste al mantener el mouse

Al usar DevTools, deberás simular todos los estados del elemento, ya que la herramienta **Inspeccionar** no muestra información para todos los estados al mismo tiempo. En este ejemplo, al usar la herramienta **Inspeccionar,** no se puede alcanzar el estado del vínculo Gatos en el menú de navegación de la barra lateral para analizar la relación de contraste en un estado, ya que el estado de los estilos no se `hover` **** `hover` `hover` desencadena.  En su lugar, debe simular el estado del elemento de menú **Gatos** mediante la simulación de estado en la **pestaña** Estilos.

Para ver los pasos detallados del tutorial, vaya a [Comprobar la accesibilidad de todos los estados de elementos](test-inspect-states.md).

Activa la herramienta **Inspeccionar** y, a continuación, en la página representada, selecciona el vínculo **azul Gatos** en el menú de navegación de la barra lateral.  Se **abre** la herramienta Elementos, con `a` el elemento seleccionado en el árbol DOM.  Si es necesario, en el árbol DOM, vaya al elemento que tiene un `hover` estado en el CSS.  En este caso, el `a` elemento tiene un `hover` estado.

:::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspeccionar el elemento que tiene un estado de puntero en la herramienta Elementos" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
    Inspeccionar el elemento que tiene un estado de puntero en la herramienta Elementos
:::image-end:::

En la **pestaña Estilos,** seleccione el **botón \:hov (Toggle Element State).**  A continuación, use **las casillas de verificación** Forzar estado del elemento para elegir el estado que se va a simular.

:::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="La característica de simulación de estado que muestra todas las opciones" lightbox="../media/a11y-testing-state-simulation.msft.png":::
    La característica de simulación de estado que muestra todas las opciones
:::image-end:::

Active la **casilla \:hover.**  Ahora aparece un punto amarillo junto al elemento DOM, que indica que el elemento DOM tiene un estado simulado.  Además, el **vínculo Gatos** del menú de navegación de la barra lateral ahora está resaltado en la página, como si el puntero del mouse estuviera sobre él.

:::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulando un estado de puntero" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
    DevTools simulando un estado de puntero
:::image-end:::

Después de aplicar el estado simulado, puede volver a usar la herramienta **Inspeccionar** para comprobar el contraste del elemento cuando el usuario mantiene el mouse sobre él.  En este caso, el contraste no es lo suficientemente alto.

:::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Probar el contraste de un elemento en un estado de puntero simulado" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
    Probar el contraste de un elemento en un estado de puntero simulado
:::image-end:::

La simulación de estado también es una buena manera de comprobar si se han considerado diferentes necesidades de usuario.  En el menú de navegación de la barra lateral, puede detectar que el `:focus` estado tiene un problema de contraste.


## <a name="use-the-rendering-tool-to-test-accessibility-for-visual-impairment"></a>Usar la herramienta de representación para probar la accesibilidad en caso de discapacidad visual

### <a name="check-contrast-issues-with-dark-theme-and-light-themes"></a>Comprobar problemas de contraste con temas oscuros y claros

Otra consideración cuando se trata de la accesibilidad de color es que puede haber diferentes temas que necesita probar para problemas de contraste.  La mayoría de los sistemas operativos tienen un modo oscuro y un modo claro.  La página web puede reaccionar a estas distintas configuraciones mediante consultas multimedia CSS.

Esta página de demostración tiene un tema claro y oscuro.  Puede probar ambos temas sin cambiar el sistema operativo mediante la simulación de combinación de [colores][DevToolsColorSchemeSimulation] oscuros o claros en la herramienta **de** representación.  Hasta ahora, este artículo ha visto la página de demostración con un sistema operativo con una configuración de tema oscuro.  Si en su lugar simulamos un esquema de luz y, a continuación, actualizamos la página, la herramienta **Problemas** muestra seis problemas de contraste de color en lugar de dos.

Para ver los pasos detallados del tutorial, vaya a Comprobar si hay problemas de [contraste con el tema oscuro y el tema claro.](test-dark-mode.md)


Al cambiar a un tema claro en la herramienta **Representación,** observe los siguientes elementos.

*  Se detectan nuevos problemas de contraste debido al cambio al tema claro.
*  Toda la **sección Estado de** donación de la página es ilegible en modo claro.

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Nuevos problemas de contraste detectados debido al cambio al tema claro" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
            Nuevos problemas de contraste detectados debido al cambio al tema claro :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="Los elementos de estado de donación marcados como problemas de contraste cuando están en modo claro" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
            Los elementos de estado de donación marcados como problemas de contraste cuando están en modo claro :::image-end:::
    :::column-end:::
:::row-end:::


### <a name="verify-that-the-webpage-is-usable-by-people-with-color-blindness"></a>Comprobar que la página web es utilizable por personas con ceguera de color

Los distintos estados de donación usan el color (rojo, verde, amarillo) como único medio para diferenciar entre los estados de financiación.  Sin embargo, no puede esperar que todos los usuarios experimente estos colores según lo previsto.  Si usa la característica [de emulación][DevToolsVisionDeficiencies] de deficiencias de visión de DevTools, puede averiguar que esto no es lo suficientemente bueno, simulando cómo las personas con visión diferente perciben su diseño.
Para ver los pasos detallados del tutorial, vaya a Comprobar que las personas con [ceguera de color](test-color-blindness.md)puedan usar la página.
:::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Mostrar la página como alguien con protanopia (ceguera de color rojo) la vería" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
    Mostrar la página como si alguien con protanopia (ceguera de color rojo) la vería
:::image-end:::



### <a name="verify-that-the-webpage-is-usable-with-blurred-vision"></a>Comprobar que la página web es utilizable con la visión borrosa

Otra característica interesante de la herramienta **de** representación es que puedes simular la visión borrosa.  Si elegimos la opción **** **Visión** borrosa de la lista desplegable Emular deficiencias de visión, podemos ver que la sombra paralela en el texto del menú superior dificulta la lectura de los elementos del menú.
Para ver los pasos detallados del tutorial, vaya a Comprobar que la página se puede [usar con la visión borrosa.](test-blurred-vision.md)

:::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="La simulación de una página borrosa puede revelar problemas de accesibilidad" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
    La simulación de una página borrosa puede revelar problemas de accesibilidad
:::image-end:::


### <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off-reduced-motion"></a>Comprobar que la página se puede usar con la animación de la interfaz de usuario desactivada (movimiento reducido)

Otra configuración que los sistemas operativos vienen con estos días es una forma de desactivar las animaciones.  Las animaciones pueden ayudar a la facilidad de uso de un producto, pero también pueden causar muchos problemas, que van desde la confusión hasta las náuseas. Es por eso que los productos no deben mostrar animaciones a los usuarios que las desactivaron en el sistema operativo.  Al usar una consulta multimedia CSS, puede comprobar si el usuario desea ver animaciones y desactivarlas en consecuencia.  Y, al igual que con el modo oscuro y claro, hay una forma de simular [el movimiento reducido con DevTools][DevToolsReducedMotion].

En la página de demostración aquí, desactivar las animaciones detendrá el desplazamiento suave de la página al seleccionar diferentes partes del menú de navegación de la barra lateral.  Esto se logra ajustando la configuración de desplazamiento suave en CSS en una consulta multimedia:

:::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulación de movimiento reducido y CSS que asegura que el desplazamiento suave solo se produce cuando el usuario lo desea" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
    Simulación de movimiento reducido y CSS que asegura que el desplazamiento suave solo se produce cuando el usuario lo desea
:::image-end:::

```css
@media (prefers-reduced-motion: no-preference) {
  html {
    scroll-behavior: smooth;
  }
}
```

Esta consulta de medios CSS ejecuta condicionalmente la animación de "desplazamiento suave".  Pero la animación de la barra de navegación superior, el menú de navegación de la barra lateral y **Más** vínculos aún se ejecutan, incluso cuando el usuario no quiere ver animaciones. Esas otras animaciones deben ejecutarse condicionalmente, por ejemplo agregando consultas multimedia adicionales.

Para ver los pasos detallados del tutorial, vaya a Comprobar que la página se puede usar con la animación de [la interfaz de usuario desactivada.](test-reduced-ui-motion.md)


## <a name="what-to-do-next"></a>¿Qué hacer a continuación?

Hemos cubierto varias herramientas que puede usar para asegurarse de que detecta problemas de accesibilidad en sus productos.  Estas herramientas van desde comprobaciones automatizadas y comprobaciones de detalles manuales hasta la simulación de diferentes estados y entornos.  Estas herramientas se resumen en Características de prueba [de accesibilidad en DevTools](reference.md).  Las herramientas automatizadas no pueden encontrar todos los problemas de un producto, ya que muchas de las barreras de accesibilidad solo se muestran durante el uso interactivo.

Ninguna de estas herramientas puede reemplazar una ronda adecuada de pruebas de sus productos con personas que usan tecnologías de asistencia y siguiendo un plan para comprobar todas las pruebas necesarias. También puede usar la característica [Evaluaciones][AccessibilityInsightsAssessment] de [accesibilidad Ideas][AccessibilityInsights].  Es posible que deba realizar comprobaciones adicionales, como:

* Probar al acercarse.
* Pruebas con lectores de pantalla.
* Pruebas con reconocimiento de voz.
* Pruebas en modo de contraste alto.

Otra forma de averiguar qué hacer para mejorar el producto web es usar la extensión [webhint para Visual Studio Code][WebhintForCode].  Esta extensión marca los problemas de accesibilidad fácilmente detectables en el código fuente y proporciona información sobre cómo solucionarlos.

:::image type="complex" source="../media/a11y-testing-webhint-in-vs-code.msft.png" alt-text="Webhint en Visual Studio Code, mostrando un problema de accesibilidad al mostrar el elemento HTML y mostrando una explicación del problema" lightbox="../media/a11y-testing-webhint-in-vs-code.msft.png":::
    Webhint en Visual Studio Code, mostrando un problema de accesibilidad al mostrar el elemento HTML y mostrando una explicación del problema
:::image-end:::

Estamos trabajando constantemente en nuevas características de accesibilidad para DevTools.  Si falta algo, envíenos un mensaje y díganos lo que podemos hacer.


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]


<!-- links -->
[DevToolsMediaQueries]: ../device-mode/index.md#show-media-queries "Mostrar consultas multimedia: emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"
[DevToolsDeviceModeIndex]: ../device-mode/index.md "Emulación de dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsAccessibilityReference]: reference.md "Características de prueba de accesibilidad en DevTools | Microsoft Docs"
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Emular esquemas oscuros o claros en la página | Microsoft Docs"
[DevToolsIssuesTool]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"
[DevToolsReducedMotion]: ./reduced-motion-simulation.md "Reducción de la simulación de movimiento | Microsoft Docs"
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emular las deficiencias de | Microsoft Docs"
<!-- links into test-issues-tool.md -->
[DevToolsAccessibilityTestIssuesToolViewAccSection]: test-issues-tool.md#view-the-accessibility-section-of-the-issues-tool "Ver la sección Accesibilidad de la herramienta Problemas: probar automáticamente una página web para problemas de accesibilidad | Microsoft Docs"
[DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels]: test-issues-tool.md#verify-that-input-fields-have-labels "Comprobar que los campos de entrada tienen etiquetas: pruebe automáticamente una página web para detectar problemas de accesibilidad | Microsoft Docs" 
[DevtoolsAccessibilityTestIssuesToolCheckAltText]: test-issues-tool.md#verify-that-images-have-alt-text "Comprobar que las imágenes tienen texto alternativo: pruebe automáticamente una página web en busca de problemas de accesibilidad | Microsoft Docs "
[DevtoolsAccessibilityTestIssuesToolCheckContrast]: test-issues-tool.md#verify-that-text-colors-have-enough-contrast "Comprobar que los colores de texto tienen suficiente contraste: pruebe automáticamente una página web para detectar problemas de accesibilidad | Microsoft Docs"
<!-- links into test-inspect-tool.md -->
[DevtoolsAccessibilityTestInspectToolColorHighlighting]: test-inspect-tool.md#identify-nested-regions-using-color-highlighting "Identificar regiones anidadas mediante resaltado de color: use la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el puntero sobre la página | Microsoft Docs"
[DevtoolsAccessibilityTestInspectToolIndivElems]: test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support "Comprobar los elementos individuales para el contraste de texto, el texto del lector de pantalla y la compatibilidad con el teclado: use la herramienta Inspeccionar para detectar problemas de accesibilidad al desplazarse sobre la página web | Microsoft Docs"
[DevtoolsAccessibilityTestInspectToolDomCss]: test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css "Use la herramienta Inspeccionar para desplazarse por la página web para resaltar el DOM y CSS: use la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el puntero sobre la página web | Microsoft Docs"
<!-- external links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "relación de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Directrices de accesibilidad de contenido web | W3C"
[AccessibilityInsightsAssessment]: https://accessibilityinsights.io/docs/en/web/getstarted/assessment/ "Evaluación en Accessibility Ideas para web | Accesibilidad Ideas"
[AccessibilityInsights]: https://accessibilityinsights.io "Accesibilidad Ideas"
[Lighthouse]: https://developers.google.com/web/tools/lighthouse/ "| Google"
[WebhintForCode]:https://aka.ms/webhint4code "webhint | Visual Studio Marketplace"
