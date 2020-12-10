---
description: Descubra nuevos flujos de trabajo para ver y cambiar CSS en Microsoft Edge DevTools.
title: Referencia de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 83edc15549b4f8e668af99a4d95966736aaa0992
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204015"
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

# Referencia de CSS  

Descubra nuevos flujos de trabajo en la siguiente referencia completa de las características de Microsoft Edge DevTools relacionadas con la visualización y el cambio de CSS.  

Consulte Introducción a la [visualización y el cambio de CSS][DevToolsCSSGetStarted] para conocer los conceptos básicos.  

## Seleccionar un elemento  

El panel **elementos** de DevTools le permite ver o cambiar la CSS de un elemento a la vez.  El elemento seleccionado está resaltado en el **árbol DOM**.  Los estilos del elemento se muestran en el panel **estilos** .  Vea [ver las CSS de un elemento][DevToolsCSSGetStartedTutorial] para obtener un tutorial.  

> [!NOTE]
> En la siguiente ilustración, el `h1` elemento que está resaltado en el **árbol DOM** es el elemento seleccionado.  A la derecha, los estilos del elemento se muestran en el panel **estilos** .  A la izquierda, el elemento se resalta en la ventanilla, pero solo porque el mouse se desplaza en el **árbol DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Ejemplo de un elemento seleccionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   Ejemplo de un elemento seleccionado  
:::image-end:::  

Use una de las siguientes acciones para seleccionar un elemento.  

*   En su ventanilla, desplace el puntero sobre el elemento, abra el menú contextual \ (haga clic con el botón derecho \) y elija **inspeccionar**.  
*   En DevTools, elija **seleccionar un elemento** \ ( ![ Seleccione un elemento ][ImageSelectAnElementIcon] \) o \ `Control` + `Shift` + `C` (Windows, Linux \) o `Command` + `Shift` + `C` \ (MacOS \) y, a continuación, elija el elemento en la ventanilla.  
*   En DevTools, elija el elemento en el **árbol DOM**.  
*   En DevTools, ejecuta una consulta como `document.querySelector('p')` en la **consola**, coloca el puntero en el resultado, abre el menú contextual \ (Haz clic con el botón derecho del ratón \) y elige **Mostrar en el panel de elementos**.  

## Ver CSS  

### Ver la hoja de estilos externa donde se define una regla  

En el panel **estilos** , elija el vínculo junto a una regla CSS para abrir la hoja de estilos externa que define la regla.  

Si la hoja de estilos es minified, desplácese para [hacer que un archivo minified sea legible][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> En la siguiente ilustración, después de elegir, `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` se le dirigirá a la línea 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , donde `.content h1:first-of-type` se define la regla CSS.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Ver la hoja de estilos donde se define una regla" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Ver la hoja de estilos donde se define una regla  
:::image-end:::  

### Ver solo la CSS que se aplica realmente a un elemento  

La pestaña **estilos** muestra todas las reglas que se aplican a un elemento, incluidas las declaraciones que se han reemplazado.  Si no está interesado en las declaraciones reemplazadas, use la pestaña **calculada** para ver solo la CSS que se está aplicando realmente a un elemento.  

1.  [Seleccione un elemento](#select-an-element).  
1.  Vaya a la pestaña **calculada** en el panel **elementos** .  

> [!NOTE]
> En una ventana de DevTools ancha, la pestaña **calculada** no existe.  El contenido de la pestaña **calculada** se muestra en la pestaña **estilos** .  

Las propiedades heredadas son opacas.  Active la casilla **Mostrar todo** para ver todos los valores heredados.  

> [!NOTE]
> En la siguiente ilustración, la pestaña **calculada** muestra las propiedades de CSS que se aplican al elemento seleccionado actualmente `h1` .  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="La pestaña calculada" lightbox="../media/css-elements-computed-h1.msft.png":::
   La pestaña **calculada**  
:::image-end:::  

### Ver las propiedades de CSS por orden alfabético  

Use la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Ver las propiedades heredadas de CSS  

Active la casilla **Mostrar todo** en la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Ver el modelo de cuadro de un elemento  

Para ver [el modelo de cuadro][MDNBoxModel] de un elemento, vaya a la pestaña **estilos** .  Si la ventana de DevTools es estrecha, el diagrama de **modelo de cuadro** se encuentra en la parte inferior de la pestaña.  

Elija y edite en un valor para cambiar un valor.  

> [!NOTE]
> En la siguiente ilustración, el diagrama de **modelo de cuadro** de la pestaña **estilos** muestra el modelo de cuadro para el elemento seleccionado actualmente `h1` .  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="El diagrama de modelo de cuadro" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   El diagrama de **modelo de cuadro**  
:::image-end:::  

### Buscar y filtrar la CSS de un elemento  

Use el cuadro de texto **filtrar** en los **estilos** y las pestañas **calculadas** para buscar propiedades o valores específicos de CSS.  

Para buscar también las propiedades heredadas en la pestaña **calculada** , active la casilla **Mostrar todo** .  

> [!NOTE]
> En la siguiente ilustración, la pestaña **estilos** se filtra para mostrar únicamente las reglas que incluyen la consulta de búsqueda `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar la pestaña estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtrar la pestaña **estilos**  
:::image-end:::  

> [!NOTE]
> En la siguiente ilustración, la pestaña **calculada** se filtra para mostrar únicamente las declaraciones que incluyen la consulta de búsqueda `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar la pestaña calculada" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtrar la pestaña **calculada**  
:::image-end:::  

### Alternar una seudoclase  

Complete las acciones siguientes para cambiar una seudoclase como `:active` ,, `:focus` `:hover` o `:visited` .  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **elementos** , vaya a la pestaña **estilos** .  
1.  Elija **: HOV**.  
1.  Compruebe la pseudo-clase que desea habilitar.  

> [!NOTE]
> En la siguiente ilustración, alterne la `:hover` pseudo-clase.  En la ventanilla, compruebe que la `background-color: cornflowerblue` declaración se aplica al elemento, aunque no se esté colocando el elemento en realidad.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Activar o desactivar la seudoclase: hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Activar o desactivar la `:hover` seudoclase  
:::image-end:::  

Para un tutorial interactivo, navegue para [Agregar un PseudoState a una clase][DevToolsCSSGetStartedAddPseudoState].  

### Ver una página en modo de impresión  

Complete las acciones siguientes para ver una página en modo de impresión.  

1.  [Abrir el menú de comandos][DevToolsCommandMenu].  
1.  Empiece `Rendering` a escribir y seleccione `Show Rendering` .  
1.  Para la lista desplegable **emular multimedia de CSS** , seleccione **Imprimir**.  

### Ver las CSS usadas y sin usar con la pestaña cobertura  

La pestaña cobertura le muestra qué CSS usa una página en realidad.  

1.  Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) mientras DevTools el foco para [abrir el menú de comandos][DevToolsCommandMenu].  
1.  Empiece `coverage` a escribir y seleccione **Mostrar cobertura**.  Aparece la ficha cobertura.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrir la ficha cobertura desde el menú de comandos" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Abrir la pestaña **cobertura** desde el **menú de comandos**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="La ficha cobertura" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             La ficha **cobertura**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Elija **iniciar la cobertura de la instrumentación y actualice la página** \ ( ![ empezar la cobertura de la instrumentación y actualizar la página ][ImageRefreshIcon] \).  La página se actualiza y la pestaña cobertura proporciona una descripción general de la cantidad de CSS \ (y JavaScript \) que se usa en cada archivo que carga el explorador.  El verde representa CSS usado.  Rojo representa un CSS no usado.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Información general sobre la cantidad de CSS \ (y JavaScript \) que se usa y que no se usa  
    :::image-end:::  

1.  Elija un archivo CSS para ver un desglose línea por línea de qué usa CSS.  
    
    > [!NOTE]
    > En la siguiente ilustración, las líneas 145 a 147 y 149 a 151 de no `b66bc881.site-ltr.css` se usan, mientras que las líneas 163 a 166 se usan.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Un desglose línea a línea de CSS utilizadas y sin usar" lightbox="../media/css-sources-css-coverage.msft.png":::
       Un desglose línea a línea de CSS utilizadas y sin usar  
    :::image-end:::  
    
### Forzar el modo vista previa de impresión  

Consulte [forzar DevTools en el modo de vista previa de impresión][DevToolsCssPrintPreview].  

## Cambiar CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### Agregar una declaración CSS a un elemento  

El orden de las declaraciones afecta a la forma en que se aplica el estilo de un elemento, use la siguiente lista para ayudarle a agregar declaraciones de diferentes maneras.  

*   [Agregue una declaración en línea](#add-an-inline-declaration).  Es equivalente a agregar un `style` atributo al código HTML de un elemento.  
*   [Agregue una declaración a una regla de estilo](#add-a-declaration-to-a-style-rule).  

**¿Qué flujo de trabajo debe usar?** En la mayoría de los casos, probablemente quieras usar el flujo de trabajo de declaración en línea.  Las declaraciones en línea tienen una mayor especificidad que las externas, por lo que el flujo de trabajo insertado garantiza que los cambios se apliquen en el elemento esperado.  Para obtener más información sobre la especificidad, vaya a [tipos de selector][MDNSelectorTypes].  

Si depura cualquier estilo del elemento y necesita comprobar específicamente lo que ocurre cuando se define una declaración en distintos lugares, use el otro flujo de trabajo.  

#### Agregar una declaración en línea  

Complete las acciones siguientes para agregar una declaración en línea.  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **estilos** , elija entre los corchetes del **elemento. sección Style** .  El cursor se centra, lo que le permite escribir texto.  
1.  Escriba un nombre de propiedad y seleccione `Enter` .  
1.  Escriba un valor válido para esa propiedad y seleccione `Enter` .  En el **árbol DOM**, compruebe que se ha `style` agregado un atributo al elemento.  

> [!NOTE]
> En la siguiente ilustración, `margin-top` se han `background-color` aplicado las propiedades y al elemento seleccionado.  En el **árbol DOM** , compruebe que las declaraciones se reflejan en el `style` atributo de un elemento.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Agregar declaraciones en línea" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Agregar declaraciones en línea  
:::image-end:::  

#### Agregar una declaración a una regla de estilo  

Complete las siguientes acciones para agregar una declaración a una regla de estilo existente.  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **estilos** , elija entre los corchetes de la regla de estilo a los que desea agregar la declaración.  El cursor se centra, lo que le permite escribir texto.  
1.  Escriba un nombre de propiedad y seleccione `Enter` .  
1.  Escriba un valor válido para esa propiedad y seleccione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Agregar una declaración a una regla de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Agregar la `border-bottom-style:groove` declaración a una regla de estilo  
:::image-end:::  

### Cambiar un nombre o valor de declaración  

Elija y edite el nombre o el valor de una declaración para cambiarlo.  Vea [cambiar valores de declaración con métodos abreviados de teclado](#change-declaration-values-with-keyboard-shortcuts) para métodos abreviados para aumentar o disminuir rápidamente un valor por `0.1` `1` unidades,, `10` o `100` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Cambiar el valor de una declaración" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Cambiar el valor de la `border-bottom-style` declaración  
:::image-end:::  

### Cambiar los valores de declaración con métodos abreviados de teclado  

Al editar el valor de una declaración, puede usar los siguientes métodos abreviados de teclado para incrementar el valor en una cantidad específica.  

*   Seleccione `Alt` + `Up` \ (Windows, Linux \) o `Option` + `Up` \ (MacOS \) para incrementarlo `0.1` .  
*   Seleccione `Up` para cambiar el valor por `1` , o por `0.1` si el valor actual se encuentra entre `-1` y `1` .  
*   Seleccione `Shift` + `Up` para incrementar `10` .  
*   Seleccione `Shift` + `Page Up` \ (Windows, Linux \) o `Shift` + `Command` + `Up` \ (MacOS \) para incrementar el valor `100` .  

También funciona la reducción.  Solo tiene que reemplazar cada instancia de la `Up` mencionada anteriormente con `Down` .  

### Agregar una clase a un elemento  

Complete las siguientes acciones para agregar una clase a un elemento.  

1.  [Seleccione el elemento](#select-an-element) en el **árbol DOM**.  
1.  Elija **. CLS**.  
1.  Escriba el nombre de la clase en el cuadro de texto **Agregar nueva clase** .  
1.  Seleccione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Panel clases de elementos" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Panel **clases de elementos**  
:::image-end:::  

### Activar o desactivar una clase  

Complete las siguientes acciones para habilitar o deshabilitar una clase en un elemento.  

1.  [Seleccione el elemento](#select-an-element) en el **árbol DOM**.  
1.  Abra el panel **clases de elementos** .  Vea [Agregar una clase a un elemento](#add-a-class-to-an-element).  Debajo del cuadro de texto **Agregar nueva clase** se encuentran todas las clases que se están aplicando al elemento específico.  
1.  Active la casilla situada junto a la clase que desea habilitar o deshabilitar.  

### Agregar una regla de estilo  

Complete las siguientes acciones para agregar una nueva regla de estilo.  

1.  [Seleccione un elemento](#select-an-element).  
1.  Elija **nueva regla de estilo** \ ( ![ nueva regla de estilo ][ImageNewStyleRuleIcon] \).  DevTools inserta una nueva regla debajo del **elemento.** regla de estilo.  

> [!NOTE]
> En la siguiente ilustración, DevTools agrega la `h1.devsite-page-title` regla de estilo después de elegir **nueva regla de estilo**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Agregar una nueva regla de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Agregar una nueva regla de estilo  
:::image-end:::  

#### Elegir la hoja de estilos a la que se va a agregar una regla  

Al [Agregar una nueva regla de estilo](#add-a-style-rule), seleccione y mantenga presionada la **nueva** regla de estilo \ ( ![ nueva regla de estilo ][ImageNewStyleRuleIcon] \) para elegir a qué hoja de estilos desea agregar la regla de estilo.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Elegir una hoja de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Elegir una hoja de estilos  
:::image-end:::  

#### Agregar una regla de estilo a una ubicación específica  

Complete las siguientes acciones para agregar una regla de estilo a una ubicación específica en la pestaña **estilos** .  

1.  Desplace el puntero sobre la regla de estilo que está justo encima del lugar donde desea agregar la nueva regla de estilo.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Elija **Insertar regla de estilo a continuación** \ ( ![ Insertar regla de estilo debajo ][ImageNewStyleRuleIcon] del icono \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insertar regla de estilo a continuación" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Insertar regla de estilo a continuación**  
:::image-end:::  

### Mostrar la barra de herramientas más acciones  

La barra de herramientas **más acciones** le permite realizar las siguientes acciones.  

*   Inserte una regla de estilo directamente debajo de la que se le está concentrando.  
*   Agregue una `background-color` `color` declaración, `box-shadow` o `text-shadow` a la regla de estilo en la que se concentra.  

Complete las siguientes acciones para mostrar la barra de herramientas **más acciones** .  

1.  En la pestaña **estilos** , desplace el puntero sobre una regla de estilo.  **Más acciones** \ ( `...` \) se muestra en la parte inferior derecha de la sección regla de estilo.  
    
    > [!NOTE]
    > En la siguiente ilustración, desplace el puntero sobre la `.header-holder.has-default-focus` regla de estilo y se revelarán **más acciones** en la parte inferior derecha de la sección regla de estilo.  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Mostrar más acciones" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Mostrar **más acciones** \ ( `...` \)  
    :::image-end:::  
    
1.  Mantenga el mouse sobre **más acciones** \ ( `...` \) para mostrar las acciones mencionadas anteriormente.  
    
    > [!NOTE]
    > La acción **Insertar regla de estilo se muestra** después de mantener el mouse sobre **más acciones**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="La barra de herramientas más acciones" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       La barra de herramientas **más acciones**  
    :::image-end:::  
    
### Activar o desactivar una declaración  

Completa las acciones de folllwoing para cambiar una única declaración de \ (o desactivada).  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **estilos** , desplace el puntero sobre la regla que define la declaración.  Aparece una casilla de verificación junto a cada declaración.  
1.  Active \ (o desactive \) la casilla junto a la declaración.  Al desactivar una declaración, DevTools la cruza para indicar que ya no está activa.  

> [!NOTE]
> En la siguiente ilustración, se `margin-top` ha desactivado la propiedad del elemento seleccionado actualmente.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Activar o desactivar una declaración" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Activar o desactivar una declaración  
:::image-end:::  

### Agregar una declaración de color de fondo  

Complete las siguientes acciones para agregar una `background-color` declaración a un elemento.  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `background-color` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Elija **agregar color de fondo** \ ( ![ agregar color de fondo, icono ][ImageAddBackgroundColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Agregar color de fondo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Agregar color de fondo**  
:::image-end:::  

### Agregar una declaración de color  

Complete las siguientes acciones para agregar una `color` declaración a un elemento.  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `color` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Elija **agregar color** \ ( ![ Agregar icono de color ][ImageAddColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Agregar color" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Agregar color**  
:::image-end:::  

### Agregar una declaración de sombra de cuadro  

Complete las siguientes acciones para agregar una `box-shadow` declaración a un elemento.  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `box-shadow` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Elija **Agregar cuadro sombra** \ ( ![ icono de sombra del cuadro de agregar ][ImageAddBoxShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Cuadro Agregar sombra" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Cuadro Agregar sombra**  
:::image-end:::  

### Agregar una declaración de sombra de texto  

Complete las siguientes acciones para agregar una `text-shadow` declaración a un elemento.  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `text-shadow` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Elija **Agregar sombra de texto** \ ( ![ icono Agregar sombra de texto ][ImageAddTextShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Agregar sombra de texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Agregar sombra de texto**  
:::image-end:::  

### Cambiar los colores con el selector de colores  

El **selector de colores** proporciona una interfaz gráfica de usuario para el cambio `color` y las `background-color` declaraciones.  

Complete las siguientes acciones para abrir el **selector de colores**.  

1.  [Seleccione un elemento](#select-an-element).  
1.  En la pestaña **estilos** , busque la `color` `background-color` declaración similar que desea cambiar.  A la izquierda del `color` valor, `background-color` o similar, hay un pequeño cuadrado, que es una vista previa del color.  
    
    > [!NOTE]
    > En la siguiente ilustración, el pequeño cuadrado situado a la izquierda de `rgba(0, 0, 0, 0.7)` es una versión preliminar de ese color.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Vista previa del color" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Vista previa del color  
    :::image-end:::  
    
1.  Elija la vista previa para abrir el **selector de colores**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="El selector de colores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       El **selector de colores**  
    :::image-end:::  
    
En la siguiente ilustración se muestra una lista de descries de cada uno de los elementos de la interfaz de usuario del **selector de colores**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="El selector de color, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   El **selector de color**, anotado  
:::image-end:::  

:::row:::
   :::column span="1":::
      uno  
   :::column-end:::
   :::column span="1":::
      **Grada**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      1  
   :::column-end:::
   :::column span="1":::
      **Cuentagotas**  
   :::column-end:::
   :::column span="2":::
      Para obtener más información, vaya a [la muestra de un color fuera de la página con el cuentagotas](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      2  
   :::column-end:::
   :::column span="1":::
      **Copiar en el portapapeles**  
   :::column-end:::
   :::column span="2":::
      Copie el **valor para mostrar** en el portapapeles.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      cuatro  
   :::column-end:::
   :::column span="1":::
      **Valor para mostrar**  
   :::column-end:::
   :::column span="2":::
      La representación RGBA, HSLA o hexadecimal del color.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      4  
   :::column-end:::
   :::column span="1":::
      **Paleta de colores**  
   :::column-end:::
   :::column span="2":::
      Elija uno de los cuadrados para cambiar el color a ese cuadrado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
   :::column-end:::
   :::column span="1":::
      **Altera**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      siete  
   :::column-end:::
   :::column span="1":::
      **Opacity**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      4,8  
   :::column-end:::
   :::column span="1":::
      **Display Value Switcher**  
   :::column-end:::
   :::column span="2":::
      Alternar entre las representaciones RGBA, HSLA y hexadecimal del color actual.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      99,999  
   :::column-end:::
   :::column span="1":::
      **Conmutador de paleta de colores**  
   :::column-end:::
   :::column span="2":::
      Cambiar entre la [paleta de diseño de material][MaterialDesignColorSystem], una paleta personalizada o una paleta de colores de página.  DevTools genera la paleta de colores de la página en función de los colores que encuentre en las hojas de estilo.  
   :::column-end:::
:::row-end:::  

#### Muestra un color de la página con el cuentagotas  

Al abrir el **selector de color**, el **cuentagotas** \ ( ![ cuentagotas ][ImageEyedropperIcon] \) está activado de forma predeterminada.  Complete las acciones siguientes para cambiar el color seleccionado a otro color de la página.  

1.  Desplace el puntero sobre el color de destino en la ventanilla.  
1.  Elija confirmar.  
    
    > [!NOTE]
    > En la siguiente ilustración, el **selector de colores** muestra un valor de color actual de `rgba(0,0,0,0.7)` , que está cerca del negro.  El color específico debe cambiar a la versión de negro que está resaltada en la ventanilla después de elegirla.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Usar el cuentagotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Usar el cuentagotas  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Agregar un PseudoState a una clase: Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Ver las CSS de un elemento: Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión) | Microsoft docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Hacer un archivo minified legible: referencia de depuración de JavaScript | Microsoft docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "El diseño de material del sistema de colores"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "El modelo de cuadro | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Especificidad de los tipos de selector | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  