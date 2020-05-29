---
title: Referencia de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 005d2650a1633d49a8c6c2550c4b2c0c2e3f3be6
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601850"
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



Descubra nuevos flujos de trabajo en esta referencia completa de las características de Microsoft Edge DevTools relacionadas con la visualización y el cambio de CSS.  

Consulte Introducción a la [visualización y el cambio de CSS][DevToolsCSSGetStarted] para conocer los conceptos básicos.  

## Seleccionar un elemento   

El panel **elementos** de DevTools le permite ver o cambiar la CSS de un elemento a la vez.  El elemento seleccionado está resaltado en el **árbol DOM**.  Los estilos del elemento se muestran en el panel **estilos** .  Vea [ver las CSS de un elemento][DevToolsCSSGetStartedTutorial] para obtener un tutorial.  

> [!NOTE]
> En la [Ilustración 1](#figure-1), el `h1` elemento que está resaltado en el **árbol DOM** es el elemento seleccionado.  A la derecha, los estilos del elemento se muestran en el panel **estilos** .  A la izquierda, el elemento se resalta en la ventanilla, pero solo porque el mouse se desplaza en el **árbol DOM**.  

> ##### Figura 1  
> Ejemplo de un elemento seleccionado  
> ![Ejemplo de un elemento seleccionado][ImageSelectedElement]  

Hay muchas maneras de seleccionar un elemento:  

*   En su ventanilla, haga clic con el botón derecho en el elemento y seleccione **inspeccionar**.  
*   En DevTools, haga clic en **seleccionar un elemento** , ![ Seleccione un elemento ][ImageSelectAnElementIcon] o pulse `Control` + `Shift` + `C` \ (Windows \) o `Command` + `Shift` + `C` \ (MacOS \) y, a continuación, haga clic en el elemento de la ventanilla.  
*   En DevTools, haga clic en el elemento del **árbol DOM**.  
*   En DevTools, ejecute una consulta como `document.querySelector('p')` en la **consola**, haga clic con el botón derecho en el resultado y, a continuación, seleccione **Mostrar en el panel elementos**.  

## Ver CSS   

### Ver la hoja de estilos externa donde se define una regla   

En el panel **estilos** , haga clic en el vínculo junto a una regla CSS para abrir la hoja de estilos externa que define la regla.  

Si la hoja de estilos es minified, vea [hacer que un archivo minified sea legible][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> En la [ilustración 2](#figure-2), al hacer clic se `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` le lleva a la línea 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , donde `.content h1:first-of-type` se define la regla CSS.  

> ##### Figura 2  
> Ver la hoja de estilos donde se define una regla  
> ![Ver la hoja de estilos donde se define una regla][ImageViewRuleStylesheet]  

### Ver solo la CSS que se aplica realmente a un elemento   

La pestaña **estilos** muestra todas las reglas que se aplican a un elemento, incluidas las declaraciones que se han reemplazado.  Si no está interesado en las declaraciones reemplazadas, use la pestaña **calculada** para ver solo la CSS que se está aplicando realmente a un elemento.  

1.  [Seleccione un elemento](#select-an-element).  
1.  Vaya a la pestaña **calculada** en el panel **elementos** .  

> [!NOTE]
> En una ventana de DevTools ancha, la pestaña **calculada** no existe.  El contenido de la pestaña **calculada** se muestra en la pestaña **estilos** .  

Las propiedades heredadas son opacas.  Active la casilla **Mostrar todo** para ver todos los valores heredados.  

> [!NOTE]
> En la [figura 3](#figure-3), la pestaña **calculada** muestra las propiedades de CSS que se están aplicando al elemento actualmente seleccionado `h1` .  

> ##### Imagen 3  
> La pestaña **calculada**  
> ![La pestaña calculada][ImageComputedTab]  

### Ver las propiedades de CSS por orden alfabético   

Use la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Ver las propiedades heredadas de CSS   

Active la casilla **Mostrar todo** en la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Ver el modelo de cuadro de un elemento   

Para ver [el modelo de cuadro][MDNBoxModel] de un elemento, vaya a la pestaña **estilos** .  Si la ventana de DevTools es estrecha, el diagrama de **modelo de cuadro** se encuentra en la parte inferior de la pestaña.  

Para cambiar un valor, haga doble clic en él.  

> [!NOTE]
> En la [figura 4](#figure-4), el diagrama de **modelo de cuadro** de la pestaña **estilos** muestra el modelo de cuadro para el elemento seleccionado actualmente `h1` .  

> ##### Imagen 4  
> El diagrama de **modelo de cuadro**  
> ![El diagrama de modelo de cuadro][ImageBoxModel]  

### Buscar y filtrar la CSS de un elemento   

Use el cuadro de texto **filtrar** en los **estilos** y las pestañas **calculadas** para buscar propiedades o valores específicos de CSS.  

Para buscar también las propiedades heredadas en la pestaña **calculada** , active la casilla **Mostrar todo** .  

> [!NOTE]
> En la [figura 5](#figure-5), la pestaña **estilos** se filtra para mostrar únicamente las reglas que incluyen la consulta de búsqueda `color` .  

> ##### Imagen 5  
> Filtrar la pestaña **estilos**  
> ![Filtrar la pestaña estilos][ImageStylesFilter]  

> [!NOTE]
> En la [figura 6](#figure-6), la pestaña **calculada** se filtra para mostrar únicamente las declaraciones que incluyen la consulta de búsqueda `100%` .  

> ##### Imagen 6  
> Filtrar la pestaña **calculada**  
> ![Filtrar la pestaña calculada][ImageComputerFilter]  

### Alternar una seudoclase   

Para alternar una seudoclase como,, `:active` `:focus` `:hover` o `:visited` :  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **elementos** , vaya a la pestaña **estilos** .  
1.  Haga clic en **: HOV**.  
1.  Compruebe la pseudo-clase que desea habilitar.  

> [!NOTE]
> En la [figura 7](#figure-7), alterne la `:hover` pseudo-clase.  En la ventanilla, compruebe que la `background-color: cornflowerblue` declaración se aplica al elemento, aunque no se esté colocando el elemento en realidad.  

> ##### Imagen 7  
> Alternar la `:hover` pseudo-clase  
> ![Alternar la seudoclase: hover][ImagePseudoClass]  

Consulte [Agregar un PseudoState a una clase][DevToolsCSSGetStartedAddPseudoState] para obtener un tutorial interactivo. 

### Ver una página en modo de impresión   

Para ver una página en modo impresión:  

1.  [Abrir el menú de comandos][DevToolsCommandMenu].  
1.  Empiece `Rendering` a escribir y seleccione `Show Rendering` .  
1.  Para la lista desplegable **emular multimedia de CSS** , seleccione **Imprimir**.  

### Ver las CSS usadas y sin usar con la pestaña cobertura   

La pestaña cobertura le muestra qué CSS usa una página en realidad.  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) mientras DevTools el foco para abrir el menú de comandos.  
1.  Empiece `coverage` a escribir y seleccione **Mostrar cobertura**.  Aparece la ficha cobertura.  
    
    > ##### Imagen 8  
    > Abrir la ficha cobertura desde el menú de comandos  
    > ![Abrir la ficha cobertura desde el menú de comandos][ImageCommandMenu]  
    
    > ##### Imagen 9  
    > La ficha cobertura  
    > ![La ficha cobertura][ImageCoverageEmpty]  
    
1.  Haga clic en **iniciar cobertura de instrumentación y actualice la página** ![ comenzar la cobertura de la instrumentación y actualice la página ][ImageRefreshIcon] .  La página se actualiza y la pestaña cobertura proporciona una descripción general de la cantidad de CSS \ (y JavaScript \) que se usa en cada archivo que carga el explorador.  El verde representa CSS usado.  Rojo representa un CSS no usado.  
    
    > ##### Imagen 10  
    > Información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa  
    > ![Información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa][ImageCoverageOverview]  

1.  Haga clic en un archivo CSS para ver un desglose línea por línea de qué usa CSS.  
    
    > [!NOTE]
    > En la [ilustración 11](#figure-11), las líneas 145 a 147 y 149 a 151 de `b66bc881.site-ltr.css` no se usan, mientras que las líneas 163 a 166 se usan.  
    
    > ##### Imagen 11  
    > Un desglose línea a línea de CSS utilizadas y sin usar  
    > ![Un desglose línea a línea de CSS utilizadas y sin usar][ImageCoverageDetail]  
    
### Forzar el modo vista previa de impresión   

Consulte [forzar DevTools en el modo de vista previa de impresión][DevToolsCssPrintPreview].  

## Cambiar CSS   

<!-- todo s/CSS declaration/declaration/ -->  

### Agregar una declaración CSS a un elemento   

Dado que el orden de las declaraciones afecta a la forma en que se aplica el estilo de un elemento, puede Agregar declaraciones de varias maneras:  

*   [Agregue una declaración en línea](#add-an-inline-declaration).  Es equivalente a agregar un `style` atributo al código HTML de un elemento.  
*   [Agregue una declaración a una regla de estilo](#add-a-declaration-to-a-style-rule).  

**¿Qué flujo de trabajo debe usar?** En la mayoría de los casos, probablemente quieras usar el flujo de trabajo de declaración en línea.  Las declaraciones en línea tienen una mayor especificidad que las externas, por lo que el flujo de trabajo insertado garantiza que los cambios se apliquen en el elemento como cabría esperar.  Para obtener más información sobre la especificidad, consulta [tipos de selector][MDNSelectorTypes] .  

Si depura cualquier estilo del elemento y necesita comprobar específicamente lo que ocurre cuando se define una declaración en distintos lugares, use el otro flujo de trabajo.  

#### Agregar una declaración en línea   

Para agregar una declaración en línea:  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **estilos** , haga clic entre los corchetes del **elemento. sección Style** .  El cursor se centra, lo que le permite escribir texto.  
1.  Escriba un nombre de propiedad y presione `Enter` .  
1.  Escriba un valor válido para esa propiedad y presione `Enter` .  En el **árbol DOM**, compruebe que se ha `style` agregado un atributo al elemento.  

> [!NOTE]
> En la [figura 12](#figure-12), `margin-top` `background-color` se han aplicado las propiedades y al elemento seleccionado.  En el **árbol DOM** , compruebe que las declaraciones se reflejan en el `style` atributo de un elemento.  

> ##### Imagen 12  
> Agregar declaraciones en línea  
> ![Agregar declaraciones en línea][ImageInlineDeclarations]  

#### Agregar una declaración a una regla de estilo   

Para agregar una declaración a una regla de estilo existente:  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **estilos** , haga clic entre los corchetes de la regla de estilo a los que desea agregar la declaración.  El cursor se centra, lo que le permite escribir texto.  
1.  Escriba un nombre de propiedad y presione `Enter` .  
1.  Escriba un valor válido para esa propiedad y presione `Enter` .  

> ##### Imagen 13  
> Agregar la `border-bottom-style:groove` declaración a una regla de estilo  
> ![Agregar una declaración a una regla de estilo][ImageAddDeclarationExistingRule]  

### Cambiar un nombre o valor de declaración   

Haga doble clic en el nombre o valor de una declaración para cambiarlo.  Vea [cambiar valores de declaración con métodos abreviados de teclado](#change-declaration-values-with-keyboard-shortcuts) para métodos abreviados para aumentar o disminuir rápidamente un valor por `0.1` `1` unidades,, `10` o `100` .  

> ##### Imagen 14  
> Cambiar el valor de la `border-bottom-style`  
> ![Cambiar el valor de una declaración][ImageAddDeclarationExistingRule2]  

### Cambiar los valores de declaración con métodos abreviados de teclado   

Al editar el valor de una declaración, puede usar los siguientes métodos abreviados de teclado para incrementar el valor en una cantidad fija:  

*   Pulsa `Alt` + `Up` \ (Windows \) o `Option` + `Up` \ (MacOS \) para incrementar `0.1` .  
*   Pulse `Up` para cambiar el valor por `1` , o bien, `0.1` si el valor actual está comprendido entre `-1` y `1` .  
*   Pulsa `Shift` + `Up` para incrementar `10` .  
*   Pulse `Shift` + `Page Up` \ (Windows \) o `Shift` + `Command` + `Up` \ (MacOS \) para incrementar el valor `100` .  

También funciona la reducción.  Solo tiene que reemplazar cada instancia de la `Up` mencionada anteriormente con `Down` .  

### Agregar una clase a un elemento   

Para agregar una clase a un elemento:  

1.  [Seleccione el elemento](#select-an-element) en el **árbol DOM**.  
1.  Haga clic en **. CLS**.  
1.  Escriba el nombre de la clase en el cuadro de texto **Agregar nueva clase** .  
1.  Presione `Enter` .  

> ##### Imagen 15  
> Panel **clases de elementos**  
> ![Panel clases de elementos][ImageElementClasses]  

### Activar o desactivar una clase   

Para habilitar o deshabilitar una clase en un elemento:  

1.  [Seleccione el elemento](#select-an-element) en el **árbol DOM**.  
1.  Abra el panel **clases de elementos** .  Vea [Agregar una clase a un elemento](#add-a-class-to-an-element).  Debajo del cuadro de texto **Agregar nueva clase** se encuentran todas las clases que se están aplicando a este elemento.  
1.  Active la casilla situada junto a la clase que desea habilitar o deshabilitar.  

### Agregar una regla de estilo   

Para agregar una nueva regla de estilo:  

1.  [Seleccione un elemento](#select-an-element).  
1.  Haga clic en **nueva regla de estilo** nueva ![ regla de estilo ][ImageNewStyleRuleIcon] .  DevTools inserta una nueva regla debajo del **elemento.** regla de estilo.  

> [!NOTE]
> En la [figura 16](#figure-16), DevTools agrega la `h1.devsite-page-title` regla de estilo después de hacer clic en **nueva regla de estilo**.  

> ##### Imagen 16  
> Agregar una nueva regla de estilo  
> ![Agregar una nueva regla de estilo][ImageStyleRule]  

#### Elegir la hoja de estilos a la que se va a agregar una regla   

Al [Agregar una nueva regla de estilo](#add-a-style-rule), haga clic en nueva regla **de estilo Nueva** regla de estilo ![ ][ImageNewStyleRuleIcon] para elegir la hoja de estilos a la que desea agregar la regla de estilo.  

> ##### Imagen 17  
> Elegir una hoja de estilos  
> ![Elegir una hoja de estilos][ImageChooseStylesheet]  

#### Agregar una regla de estilo a una ubicación específica   

Para agregar una regla de estilo a una ubicación específica en la pestaña **estilos** :  

1.  Desplace el puntero sobre la regla de estilo que está justo encima del lugar donde desea agregar la nueva regla de estilo.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Haga clic en **Insertar regla de estilo debajo** de ![ Insertar regla de estilo ][ImageNewStyleRuleIcon] .  

> ##### Ilustración 18  
> **Insertar regla de estilo a continuación**  
> ![Insertar regla de estilo a continuación][ImageInsertStyleRuleBelow]  

### Mostrar la barra de herramientas más acciones   

La barra de herramientas **más acciones** le permite:  

*   Inserte una regla de estilo directamente debajo de la que se le está concentrando.  
*   Agregue una `background-color` `color` declaración, `box-shadow` o `text-shadow` a la regla de estilo en la que se concentra.  

Para mostrar la barra de herramientas **más acciones** :  

1.  En la pestaña **estilos** , desplace el puntero sobre una regla de estilo.  **Más acciones** `...` se revela en la parte inferior derecha de la sección regla de estilo.  
    
    > [!NOTE]
    > En la [Ilustración 19](#figure-19), desplace el puntero sobre la `.header-holder.has-default-focus` regla de estilo y se revela **más acciones** en la parte inferior derecha de la sección regla de estilo.  
    
    > ##### Ilustración 19  
    > Mostrar **más acciones**  
    > ![Mostrar más acciones][ImageRevealMore]  
    
1.  Mantenga el mouse sobre **más acciones** `...` para mostrar las acciones mencionadas anteriormente.  
    
    > [!NOTE]
    > La acción **Insertar regla de estilo se muestra** después de mantener el mouse sobre **más acciones**.  
    
    > ##### Ilustración 20  
    > La barra de herramientas **más acciones**  
    > ![La barra de herramientas más acciones][ImageInsertStyleRuleBelow2]  
    
### Activar o desactivar una declaración   

Para activar o desactivar una única declaración:  

1.  [Seleccione un elemento](#select-an-element).  
1.  En el panel **estilos** , desplace el puntero sobre la regla que define la declaración.  Las casillas aparecerán junto a cada declaración.  
1.  Active o desactive la casilla situada junto a la declaración.  Al desactivar una declaración, DevTools la cruza para indicar que ya no está activa.  

> [!NOTE]
> En la [figura 21](#figure-21), la `margin-top` propiedad del elemento seleccionado está desactivada.  

> ##### Ilustración 21  
> Alternar una declaración  
> ![Alternar una declaración][ImageToggleDeclaration]  

### Agregar una declaración de color de fondo   

Para agregar una `background-color` declaración a un elemento:  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `background-color` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Haga clic en **agregar color de fondo** para ![ agregar color de fondo ][ImageAddBackgroundColorIcon] .  

> ##### Ilustración 22  
> **Agregar color de fondo**  
> ![Agregar color de fondo][ImageAddBackgroundColor]  

### Agregar una declaración de color   

Para agregar una `color` declaración a un elemento:  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `color` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Haga clic en **Agregar** color ![ agregar color ][ImageAddColorIcon] .  

> ##### Ilustración 23  
> **Agregar color**  
> ![Agregar color][ImageAddColor]  

### Agregar una declaración de sombra de cuadro   

Para agregar una `box-shadow` declaración a un elemento:  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `box-shadow` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Haga clic en **Agregar cuadro** sombra del ![ cuadro Agregar sombra ][ImageAddBoxShadowIcon] .  

> ##### Ilustración 24  
> **Cuadro Agregar sombra**  
> ![Cuadro Agregar sombra][ImageAddBoxShadow]  

### Agregar una declaración de sombra de texto   

Para agregar una `text-shadow` declaración a un elemento:  

1.  Pase el puntero sobre la regla de estilo a la que desea agregar la `text-shadow` declaración.  
1.  [Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).  
1.  Haga clic en **Agregar sombra de texto** y ![ agregue sombra de texto ][ImageAddTextShadowIcon] .  

> ##### Ilustración 25  
> **Agregar sombra de texto**  
> ![Agregar sombra de texto][ImageAddTextShadow]  

### Cambiar los colores con el selector de colores   

El **selector de colores** proporciona una interfaz gráfica de usuario para el cambio `color` y las `background-color` declaraciones.  

Para abrir el **selector de colores**:  

1.  [Seleccione un elemento](#select-an-element).  
1.  En la pestaña **estilos** , busque la `color` `background-color` declaración similar que desea cambiar.  A la izquierda del `color` valor, `background-color` o similar, hay un pequeño cuadrado, que es una vista previa del color.  
    
    > [!NOTE]
    > En la [ilustración 26](#figure-26), el pequeño cuadrado a la izquierda de `rgba(0, 0, 0, 0.7)` es una versión preliminar de ese color.  
    
    > ##### Ilustración 26  
    > Vista previa del color  
    > ![Vista previa del color][ImageColorPreview]  
    
1.  Haga clic en la vista previa para abrir el **selector de color**.  
    
    > ##### Ilustración 27  
    > El **selector de colores**  
    > ![El selector de colores][ImageColorPicker]  
    
A continuación se muestra una descripción de cada uno de los elementos de la interfaz de usuario del **selector de colores**:  

> ##### Ilustración 28  
> El selector de color, anotado  
> ![El selector de color, anotado][ImageColorPickerAnnotated]  

1.  **Sombras**.  
1.  **Cuentagotas**.  Vea [el ejemplo de color en la página con el cuentagotas](#sample-a-color-off-the-page-with-the-eyedropper).  
1.  **Copiar al portapapeles**.  Copie el **valor para mostrar** en el portapapeles.  
1.  **Valor para mostrar**.  La representación RGBA, HSLA o hexadecimal del color.  
1.  **Paleta de colores**.  Haga clic en uno de estos cuadrados para cambiar el color de ese cuadrado.  
1.  **Matiz**.  
1.  **Opacidad**.  
1.  **Display Value Switcher**.  Alternar entre las representaciones RGBA, HSLA y hexadecimal del color actual.  
1.  **Conmutador de paleta de colores**.  Cambiar entre la [paleta de diseño de material][MaterialDesignColorSystem], una paleta personalizada o una paleta de colores de página.  DevTools genera la paleta de colores de la página en función de los colores que encuentre en las hojas de estilo.  

#### Muestra un color de la página con el cuentagotas   

Al abrir el **selector de colores**, el cuentagotas **cuentagotas** ![ ][ImageEyedropperIcon] está activado de forma predeterminada.  Para cambiar el color seleccionado a otro color de la página:  

1.  Desplace el puntero sobre el color de destino en la ventanilla.  
1.  Haga clic para confirmar.  
    
    > [!NOTE]
    > En la [ilustración 29](#figure-29), el **selector de colores** muestra un valor de color actual de `rgba(0,0,0,0.7)` , que está cerca del negro.  Este color debe cambiar al negro que está resaltado en la ventanilla cuando se hizo clic en el negro.  
    
    > ##### Ilustración 29  
    > Usar el cuentagotas  
    > ![Usar el cuentagotas][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Ilustración 1: un ejemplo de un elemento seleccionado"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Ilustración 2: ver la hoja de estilos donde se define una regla"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Ilustración 3: la pestaña calculada"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Ilustración 4: el diagrama de modelo de cuadro"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Ilustración 5: filtrar la pestaña estilos"  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Ilustración 6: filtrar la pestaña calculada"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Ilustración 7: alternar la seudoclase: hover"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Ilustración 8: abrir la pestaña cobertura desde el menú de comandos"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Ilustración 9: la pestaña cobertura"  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Ilustración 10: información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Ilustración 11: División línea a línea de CSS utilizadas y sin usar"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Ilustración 12: agregar declaraciones en línea"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Ilustración 13: agregar una declaración a una regla de estilo"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Ilustración 14: cambiar el valor de una declaración"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Ilustración 15: el panel clases de elementos"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Ilustración 16: agregar una nueva regla de estilo"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Ilustración 17: elegir una hoja de estilos"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Ilustración 18: insertar regla de estilo a continuación"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Ilustración 19: revelar más acciones"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Ilustración 20: la barra de herramientas más acciones"  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Ilustración 21: cambiar una declaración"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Ilustración 22: agregar color de fondo"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Ilustración 23: agregar color"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Ilustración 24: sombra del cuadro Agregar"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Ilustración 25: agregar sombra de texto"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Ilustración 26: vista previa del color"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Ilustración 27: el selector de colores"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Ilustración 28: el selector de color, anotado"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Ilustración 29: uso del cuentagotas"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Agregar un PseudoState a una clase: Introducción a la visualización y el cambio de CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Ver las CSS de un elemento: Introducción a la visualización y el cambio de CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Hacer que un archivo minified sea legible: referencia de depuración de JavaScript"  

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
