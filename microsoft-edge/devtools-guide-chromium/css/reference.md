---
description: Descubra nuevos flujos de trabajo para ver y cambiar CSS en Microsoft Edge DevTools.
title: Referencia de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a99cf46c4c0a6c6f14892268a30f8aab471e919d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399144"
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

# <a name="css-reference"></a>Referencia de CSS  

Descubra nuevos flujos de trabajo en la siguiente referencia completa de las características de Microsoft Edge DevTools relacionadas con la visualización y el cambio de CSS.  

Para obtener información básica, vaya a [Introducción a Ver y cambiar CSS][DevToolsCSSGetStarted].  

## <a name="choose-an-element"></a>Elegir un elemento  

La **herramienta Elementos** de DevTools permite ver o cambiar el CSS de un elemento a la vez.  El elemento seleccionado se resalta en el **árbol DOM**.  Los estilos del elemento se muestran en el **panel Estilos.**  Para obtener un tutorial, vaya [a Ver el CSS de un elemento][DevToolsCSSGetStartedTutorial].  

> [!NOTE]
> En la siguiente figura, el elemento que se resalta `h1` en el árbol **DOM** es el elemento seleccionado.  A la derecha, los estilos del elemento se muestran en el **panel Estilos.**  A la izquierda, el elemento se resalta en la ventanilla, pero solo porque el mouse está activando el mouse sobre él en el **árbol DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Un ejemplo de un elemento seleccionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   Un ejemplo de un elemento seleccionado  
:::image-end:::  

Use una de las siguientes acciones para seleccionar un elemento.  

*   En la ventanilla, mantenga el mouse sobre el elemento, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Inspeccionar**.  
*   En DevTools, elija **Seleccionar** un elemento \( Seleccionar un elemento \) o seleccione ![ ][ImageSelectAnElementIcon] `Control` + `Shift` + `C` \(Windows, Linux\) o `Command` + `Shift` + `C` \(macOS\) y, a continuación, elija el elemento en la ventanilla.  
*   En DevTools, elija el elemento en el **árbol DOM**.  
*   En DevTools, ejecute una consulta como en la consola , mantenga el mouse sobre el resultado, abra el menú contextual \(haga clic con el botón secundario en\) y elija Mostrar en el `document.querySelector('p')` **panel Elementos**. ****  

## <a name="view-css"></a>Ver CSS  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a>Ver la hoja de estilos externa donde se define una regla  

En el **panel Estilos,** elija el vínculo junto a una regla CSS para abrir la hoja de estilos externa que define la regla.  

Si la hoja de estilos está minificada, vaya a Hacer que un archivo [minificado sea legible.][DevToolsJavascriptReferenceFormat]  

> [!NOTE]
> En la siguiente figura, después de elegir, se le toma a la línea 2 de , donde se define la `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` regla `.content h1:first-of-type` CSS.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Visualización de la hoja de estilos donde se define una regla" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Visualización de la hoja de estilos donde se define una regla  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a>Ver solo el CSS que se aplica realmente a un elemento  

El panel **Estilos** muestra todas las reglas que se aplican a un elemento, incluidas las declaraciones que se han invalidado.  Cuando no esté interesado en las declaraciones invalidadas, use el **panel** Calculado para ver solo el CSS que realmente se está aplicando a un elemento.  

1.  [Seleccione un elemento](#choose-an-element).  
1.  Vaya al panel **Calculado** de la **herramienta** Elementos.  

> [!NOTE]
> En una ventana de DevTools amplia, el panel **Calculado** no existe.  El contenido del panel **Calculado** se muestra en el panel **Estilos.**  

Las propiedades heredadas son opacas.  Para mostrar todos los valores heredados, active la **casilla Mostrar todo.**  

> [!NOTE]
> En la siguiente figura, el panel **Calculado** muestra las propiedades CSS que se aplican al elemento seleccionado `h1` actualmente.  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Panel calculado" lightbox="../media/css-elements-computed-h1.msft.png":::
   Panel **calculado**  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a>Ver propiedades CSS en orden alfabético  

Use el panel **Calculado.**  Navegue a [Ver solo el CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### <a name="view-inherited-css-properties"></a>Ver propiedades CSS heredadas  

Active la **casilla Mostrar todo** en el panel **Calculado.**  Navegue a [Ver solo el CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### <a name="view-the-box-model-for-an-element"></a>Ver el modelo de cuadro de un elemento  

Para ver [el modelo de cuadro][MDNBoxModel] de un elemento, vaya al panel **Estilos.**  Si la ventana DevTools es estrecha, el diagrama **modelo** de cuadro se encuentra en la parte inferior del panel.  

Elija y edite en un valor para cambiar un valor.  

> [!NOTE]
> En la siguiente figura, el diagrama **Modelo de** cuadro del panel **Estilos** muestra el modelo de cuadro para el elemento `h1` seleccionado actualmente.  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagrama del modelo de cuadro" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Diagrama **del modelo de** cuadro  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a>Buscar y filtrar el CSS de un elemento  

Use el **cuadro de** texto Filtrar de los paneles **Estilos** y **Calculados** para buscar valores o propiedades CSS específicos.  

Para buscar también propiedades heredadas en el panel **Calculado,** active la casilla **Mostrar todo.**  

> [!NOTE]
> En la siguiente figura, el panel **Estilos** se filtra para mostrar solo las reglas que incluyen la consulta de búsqueda `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar el panel Estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtrar el panel **Estilos**  
:::image-end:::  

> [!NOTE]
> En la siguiente figura, **el** panel Calculado se filtra para mostrar solo las declaraciones que incluyen la consulta de búsqueda `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar el panel calculado" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtrar el panel **calculado**  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a>Alternar una pseudo-clase  

Complete las siguientes acciones para alternar una pseudo-clase como `:active` , `:focus` , o `:hover` `:visited` .  

1.  [Seleccione un elemento](#choose-an-element).  
1.  En la **herramienta Elementos,** vaya al panel **Estilos.**  
1.  Elija **:hov**.  
1.  Compruebe la pseudo-clase que desea habilitar.  

> [!NOTE]
> En la siguiente figura, alterna la `:hover` pseudo-clase.  En la ventanilla, compruebe que la declaración se aplica al elemento, aunque el elemento no `background-color: cornflowerblue` esté activando.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Alternar la pseudo-clase :hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Alternar la `:hover` pseudo-clase  
:::image-end:::  

Para obtener un tutorial interactivo, vaya [a Agregar un pseudoestado a una clase][DevToolsCSSGetStartedAddPseudoState].  

### <a name="view-a-page-in-print-mode"></a>Ver una página en modo de impresión  

Complete las siguientes acciones para ver una página en modo de impresión.  

1.  [Abra el menú de comandos][DevToolsCommandMenu].  
1.  Comience a escribir `Rendering` y seleccione `Show Rendering` .  
1.  Para el desplegable **Emular medios CSS,** elija **imprimir**.  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a>Ver CSS usado y sin usar con la herramienta Cobertura  

La **herramienta Cobertura** muestra qué CSS usa realmente una página.  

1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) mientras DevTools [][DevToolsCommandMenu]está centrado para abrir el menú de comandos .  
1.  Empiece a escribir `coverage` y elija Mostrar **cobertura**.  Aparece **la herramienta** Cobertura.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrir la herramienta Cobertura desde el menú comando" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Abra la **herramienta Cobertura** desde el **menú Comando**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="La herramienta Cobertura" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             La **herramienta Cobertura**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Elija **Iniciar la cobertura de instrumentación y actualizar la página** \( Iniciar la ![ instrumentación de la cobertura y actualizar la página ][ImageRefreshIcon] \).  La página se actualiza y la herramienta **Cobertura** proporciona una introducción a la cantidad de CSS \(y JavaScript\) que se usa en cada archivo que carga el explorador.  El color verde representa CSS usado.  El rojo representa CSS sin usar.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Información general sobre la cantidad de CSS (y JavaScript) que se usa y no se usa" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Información general sobre la cantidad de CSS \(y JavaScript\) que se usa y no se usa.  
    :::image-end:::  

1.  Para mostrar un desglose línea por línea de lo que se usa CSS, elija un archivo CSS.  
    
    > [!NOTE]
    > En la siguiente figura, no se usan las líneas 145 a 147 y de 149 a 151, mientras que se usan las líneas `b66bc881.site-ltr.css` 163 a 166.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Desglose línea por línea de CSS usado y no usado" lightbox="../media/css-sources-css-coverage.msft.png":::
       Desglose línea por línea de CSS usado y no usado  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a>Forzar el modo de vista previa de impresión  

Vaya a [Forzar DevTools al modo de vista previa de impresión.][DevToolsCssPrintPreview]  

## <a name="change-css"></a>Cambiar CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a>Agregar una declaración CSS a un elemento  

El orden de las declaraciones afecta al estilo de un elemento, use la siguiente lista para ayudarle a agregar declaraciones de diferentes maneras.  

*   [Agregue una declaración en línea](#add-an-inline-declaration).  Equivale a agregar `style` un atributo al HTML de un elemento.  
*   [Agregar una declaración a una regla de estilo](#add-a-declaration-to-a-style-rule).  

**¿Qué flujo de trabajo debe usar?** Para la mayoría de los escenarios, probablemente quiera usar el flujo de trabajo de declaración en línea.  Las declaraciones en línea tienen mayor especificidad que las externas, por lo que el flujo de trabajo en línea garantiza que los cambios tengan efecto en el elemento esperado.  Para obtener más información acerca de la especificidad, vaya a [Tipos de selector][MDNSelectorTypes].  

Si va a depurar cualquier estilo del elemento y necesita probar específicamente lo que sucede cuando una declaración se define en lugares diferentes, use el otro flujo de trabajo.  

#### <a name="add-an-inline-declaration"></a>Agregar una declaración en línea  

Complete las siguientes acciones para agregar una declaración en línea.  

1.  [Seleccione un elemento](#choose-an-element).  
1.  En el **panel Estilos,** elija entre los corchetes de la **sección element.style.**  El cursor se centra, lo que permite escribir texto.  
1.  Escriba un nombre de propiedad y seleccione `Enter` .  
1.  Escriba un valor válido para esa propiedad y seleccione `Enter` .  En el **árbol DOM**, compruebe que se ha agregado un atributo `style` al elemento.  

> [!NOTE]
> En la siguiente figura, las `margin-top` propiedades y se han aplicado al elemento `background-color` seleccionado.  En el **árbol DOM,** compruebe que las declaraciones se reflejan en el `style` atributo de un elemento.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Agregar declaraciones en línea" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Agregar declaraciones en línea  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a>Agregar una declaración a una regla de estilo  

Complete las siguientes acciones para agregar una declaración a una regla de estilo existente.  

1.  [Seleccione un elemento](#choose-an-element).  
1.  En el **panel Estilos,** elija entre los corchetes de la regla de estilo a la que desea agregar la declaración.  El cursor se centra, lo que permite escribir texto.  
1.  Escriba un nombre de propiedad y seleccione `Enter` .  
1.  Escriba un valor válido para esa propiedad y seleccione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Agregar una declaración a una regla de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Agregar la `border-bottom-style:groove` declaración a una regla de estilo  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a>Cambiar un nombre o valor de declaración  

Elija y edite el nombre o el valor de una declaración para cambiarla.  Para obtener accesos directos para incrementar o disminuir rápidamente un valor por , , , o unidades, vaya a Cambiar valores de declaración con `0.1` `1` `10` `100` [métodos abreviados de teclado.](#change-declaration-values-with-keyboard-shortcuts)  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Cambiar el valor de una declaración" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Cambiar el valor de la `border-bottom-style` declaración  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a>Cambiar valores de declaración con métodos abreviados de teclado  

Al editar el valor de una declaración, puede usar los siguientes métodos abreviados de teclado para incrementar el valor en una cantidad específica.  

*   Seleccione `Alt` + `Up` \(Windows, Linux\) o `Option` + `Up` \(macOS\) para incrementar por `0.1` .  
*   Seleccione `Up` para cambiar el valor por , o por si el valor actual está entre y `1` `0.1` `-1` `1` .  
*   Seleccione `Shift` + `Up` para incrementar por `10` .  
*   Seleccione `Shift` + `Page Up` \(Windows, Linux\) o `Shift` + `Command` + `Up` \(macOS\) para incrementar el valor por `100` .  

La decrementación también funciona.  Solo tiene que reemplazar cada instancia de `Up` la mencionada anteriormente por `Down` .  

### <a name="add-a-class-to-an-element"></a>Agregar una clase a un elemento  

Complete las siguientes acciones para agregar una clase a un elemento.  

1.  [Seleccione el elemento](#choose-an-element) en el **árbol DOM**.  
1.  Elija **.cls**.  
1.  Escriba el nombre de la clase en el **cuadro de** texto Agregar nueva clase.  
1.  Seleccione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Panel Clases de elementos" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Panel **Clases de** elementos  
:::image-end:::  

### <a name="toggle-a-class"></a>Alternar una clase  

Complete las siguientes acciones para habilitar o deshabilitar una clase en un elemento.  

1.  [Seleccione el elemento](#choose-an-element) en el **árbol DOM**.  
1.  Abra el **panel Clases de** elementos.  Vaya [a Agregar una clase a un elemento](#add-a-class-to-an-element).  Debajo **del cuadro de texto Agregar** nueva clase se encuentran todas las clases aplicadas al elemento específico.  
1.  Activa o desactiva la casilla situada junto a la clase que quieras activar o desactivar.  

### <a name="add-a-style-rule"></a>Agregar una regla de estilo  

Complete las siguientes acciones para agregar una nueva regla de estilo.  

1.  [Seleccione un elemento](#choose-an-element).  
1.  Elija **Nueva regla de estilo** \( Nueva regla de estilo ![ ][ImageNewStyleRuleIcon] \).  DevTools inserta una nueva regla debajo de la **regla element.style.**  

> [!NOTE]
> En la siguiente figura, DevTools agrega la regla `h1.devsite-page-title` de estilo después de elegir Nueva regla de **estilo**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Agregar una nueva regla de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Agregar una nueva regla de estilo  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a>Elegir la hoja de estilos a la que se va a agregar una regla  

Al [agregar una nueva regla de estilo,](#add-a-style-rule)elija y mantenga presionada nueva regla de estilo **\(** Nueva regla de estilo \) para elegir a qué hoja de estilos agregar la ![ regla de ][ImageNewStyleRuleIcon] estilo.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Elegir una hoja de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Elegir una hoja de estilos  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a>Agregar una regla de estilo a una ubicación específica  

Complete las siguientes acciones para agregar una regla de estilo a una ubicación específica en el panel **Estilos.**  

1.  Mantenga el mouse sobre la regla de estilo que está directamente encima de donde desea agregar la nueva regla de estilo.  
1.  [Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).  
1.  Elija **Insertar regla de estilo debajo** \( Insertar regla de estilo ![ debajo del icono ][ImageNewStyleRuleIcon] \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insertar regla de estilo a continuación" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Insertar regla de estilo a continuación**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a>Mostrar la barra de herramientas Más acciones  

La **barra de herramientas** Más acciones le permite realizar las siguientes acciones.  

*   Inserte una regla de estilo directamente debajo de la que está centrado.  
*   Agregue una , , o declaración a la regla de estilo en la `background-color` `color` que está `box-shadow` `text-shadow` centrado.  

Complete las siguientes acciones para mostrar la **barra de herramientas Más** acciones.  

1.  En el panel **Estilos,** mantenga el mouse sobre una regla de estilo.  **Más acciones** \( `...` \) se muestra en la parte inferior derecha de la sección de regla de estilo.  
    
    > [!NOTE]
    > En la siguiente figura, mantenga el puntero sobre la regla de estilo y Más acciones se muestra en la parte inferior derecha de la sección `.header-holder.has-default-focus` regla de estilo. ****  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Revelar más acciones" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Mostrar **más acciones** \( `...` \)  
    :::image-end:::  
    
1.  Mantenga el **mouse en Más acciones** \( `...` \) para mostrar las acciones mencionadas anteriormente.  
    
    > [!NOTE]
    > La **acción Insertar regla de** estilo debajo se muestra después de pasar el puntero sobre Más **acciones**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="La barra de herramientas Más acciones" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       La **barra de herramientas Más** acciones  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a>Alternar una declaración  

Complete las acciones de folllwoing para alternar una sola declaración en \(or off\).  

1.  [Seleccione un elemento](#choose-an-element).  
1.  En el **panel Estilos,** mantenga el mouse sobre la regla que define la declaración.  Aparece una casilla junto a cada declaración.  
1.  Active \(o desactive\) la casilla situada junto a la declaración.  Al desactivar una declaración, DevTools la cruza para indicar que ya no está activa.  

> [!NOTE]
> En la siguiente figura, se ha desactivado la propiedad del elemento `margin-top` seleccionado actualmente.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Alternar una declaración" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Alternar una declaración  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a>Agregar una declaración de color de fondo  

Complete las siguientes acciones para agregar una declaración a `background-color` un elemento.  

1.  Mantenga el mouse sobre la regla de estilo a la que desea agregar `background-color` la declaración.  
1.  [Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).  
1.  Elija **Agregar color de fondo** \( Icono Agregar color de fondo ![ ][ImageAddBackgroundColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Agregar color de fondo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Agregar color de fondo**  
:::image-end:::  

### <a name="add-a-color-declaration"></a>Agregar una declaración de color  

Complete las siguientes acciones para agregar una declaración a `color` un elemento.  

1.  Mantenga el mouse sobre la regla de estilo a la que desea agregar `color` la declaración.  
1.  [Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).  
1.  Elija **Agregar color** \( Icono Agregar color ![ ][ImageAddColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Agregar color" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Agregar color**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a>Agregar una declaración de sombra de cuadro  

Complete las siguientes acciones para agregar una declaración a `box-shadow` un elemento.  

1.  Mantenga el mouse sobre la regla de estilo a la que desea agregar `box-shadow` la declaración.  
1.  [Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).  
1.  Elija **Agregar sombra de cuadro** \( Agregar icono de sombra de cuadro ![ ][ImageAddBoxShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Agregar sombra de cuadro" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Agregar sombra de cuadro**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a>Agregar una declaración de sombra de texto  

Complete las siguientes acciones para agregar una declaración a `text-shadow` un elemento.  

1.  Mantenga el mouse sobre la regla de estilo a la que desea agregar `text-shadow` la declaración.  
1.  [Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).  
1.  Elija **Agregar sombra de texto** \( Agregar icono sombra de texto ![ ][ImageAddTextShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Agregar sombra de texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Agregar sombra de texto**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a>Cambiar colores con el Selector de colores  

El **selector de colores** proporciona una GUI para cambiar y las `color` `background-color` declaraciones.  

Complete las siguientes acciones para abrir el **Selector de colores**.  

1.  [Seleccione un elemento](#choose-an-element).  
1.  En el panel **Estilos,** busque la `color` declaración , o similar que desea `background-color` cambiar.  A la izquierda del `color` valor `background-color` , o similar, hay un cuadrado pequeño que es una vista previa del color.  
    
    > [!NOTE]
    > En la siguiente figura, el pequeño cuadrado situado a la izquierda de `rgba(0, 0, 0, 0.7)` es una vista previa de ese color.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Vista previa del color" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Vista previa del color  
    :::image-end:::  
    
1.  Elija la vista previa para abrir el **Selector de colores**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Selector de colores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       Selector **de colores**  
    :::image-end:::  
    
La siguiente figura y enumerar descries de cada uno de los elementos de la interfaz de usuario del **Selector de colores**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Selector de colores, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   Selector **de colores**, anotado  
:::image-end:::  

:::row:::
   :::column span="1":::
      1  
   :::column-end:::
   :::column span="1":::
      **Sombras**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      2  
   :::column-end:::
   :::column span="1":::
      **Cuentagotas**  
   :::column-end:::
   :::column span="2":::
      Para obtener más información, vaya [a Muestra de un color fuera de la página con cuentagotas](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3  
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
      4  
   :::column-end:::
   :::column span="1":::
      **Valor para mostrar**  
   :::column-end:::
   :::column span="2":::
      La representación RGBA, HSLA o Hexadecimal del color.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
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
      **Tono**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      7  
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
      8  
   :::column-end:::
   :::column span="1":::
      **Modificador de valor para mostrar**  
   :::column-end:::
   :::column span="2":::
      Alterna entre las representaciones RGBA, HSLA y Hex del color actual.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      9  
   :::column-end:::
   :::column span="1":::
      **Conmutador de paleta de colores**  
   :::column-end:::
   :::column span="2":::
      Alterna entre la paleta [Diseño de materiales,][MaterialDesignColorSystem]una paleta personalizada o una paleta de colores de página.  DevTools genera la paleta de colores de página en función de los colores que encuentre en las hojas de estilos.  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a>Muestrear un color fuera de la página con el cuentagotas  

Al abrir el **Selector de colores**, el **cuentagotas** \( Cuentagotas ![ ][ImageEyedropperIcon] \) está en la opción predeterminada.  Complete las siguientes acciones para cambiar el color seleccionado a otro color de la página.  

1.  Mantenga el mouse sobre el color de destino en la ventanilla.  
1.  Elija confirmar.  
    
    > [!NOTE]
    > En la siguiente figura, el **Selector** de colores muestra un valor de color actual de `rgba(0,0,0,0.7)` , que está cerca del negro.  El color específico debe cambiar a la versión de negro que está resaltada actualmente en la ventanilla después de elegirlo.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Uso del cuentagotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Uso del cuentagotas  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

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

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Agregar un pseudoestado a una clase: introducción a ver y cambiar css | Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Ver el CSS de un elemento: introducción a la visualización y cambio de css | Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forzar las DevTools de Microsoft Edge al modo de vista previa de impresión (tipo de medios de impresión CSS) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Hacer que un archivo minificado sea legible: referencia de depuración de JavaScript | Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "El sistema de colores: diseño de material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "El modelo de cuadro | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de selector: especificación | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  