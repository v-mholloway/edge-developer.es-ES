---
title: 'DevTools para principiantes: Introducción a CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882740"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# DevTools para principiantes: Introducción a CSS   

En este tutorial, aprenderá a usar CSS para aplicar un estilo a una página web.  También aprenderá a usar Microsoft Edge DevTools para experimentar con cambios de CSS.  

Este es el segundo tutorial de una serie de tutoriales que le enseñan los conceptos básicos del desarrollo web y Microsoft Edge DevTools.  Ganas experiencia práctica creando tu propio sitio Web.  No es necesario que completes el primer tutorial antes de hacerlo.  Puedes empezar aquí.  [Configurar el código](#set-up-your-code) le muestra cómo realizar la configuración.  

> [!NOTE]
> Este tutorial está diseñado para principiantes y se centra en los **conceptos básicos del desarrollo web** y en los conceptos básicos del uso de DevTools para experimentar con CSS.  Si desea un tutorial que solo se Centre en DevTools, consulte Introducción [a la visualización y el cambio de CSS][DevtoolsCssIndex].  

Actualmente su sitio tiene el siguiente aspecto:  

> ##### Figura 1  
> El aspecto de tu sitio en este momento  
> ![El aspecto de tu sitio en este momento][ImageCssIntro1]  

Después de completar el tutorial, tendrá el siguiente aspecto:  

> ##### Figura 2  
> El aspecto del sitio al final del tutorial  
> ![El aspecto del sitio al final del tutorial][ImageCssIntro2]  

## Principales   

Al final de este tutorial, comprenderá lo siguiente:  

*   Cómo usar CSS para aplicar un estilo a una página web.  
*   Cómo usar Microsoft Edge DevTools para experimentar con CSS.  
*   La diferencia entre los marcos CSS y CSS.  

También tendrá un sitio web real.  

## Requisitos previos   

Antes de intentar este tutorial, complete los siguientes requisitos previos:  

*   Complete Introducción [a HTML y el Dom][DevToolsBeginnersHtml] , o asegúrese de que tiene conocimientos de HTML y Dom parecidos a los impartidos en ese tutorial.  
*   Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .  En este tutorial se usa un conjunto de herramientas de desarrollo web, denominado Microsoft Edge DevTools, que está integrado en Microsoft Edge.  

## Configurar el código   

Para empezar a crear su sitio, debe configurar el código:  

1.  **Si ya ha completado el primer tutorial de esta serie, omita esta sección.  Continúa usando el código del último tutorial, [Introducción a HTML y el Dom][DevToolsBeginnersHtml].**  
1.  Abra el [código fuente][GlitchCookedAmphibianIndex].  Esta pestaña del explorador se llamará la **pestaña edición**.  
    
    > ##### Imagen 3  
    > La ficha edición  
    > ![La ficha edición][ImageCssSetup1]  
    
1.  Haga clic en **cocinada-Amphibian**.  Aparece un menú.  
    
    > ##### Imagen 4  
    > El menú opciones del proyecto  
    > ![El menú opciones del proyecto][ImageCssSetup2]  

1.  Haga clic en **Remix proyecto**.  Problema crea una copia del proyecto que se puede editar.  
    
    > [!NOTE]
    > El problema genera un nombre aleatorio para el nuevo proyecto.  
    
1.  Haga clic en **Mostrar** y seleccione **en una ventana nueva**.  Se abre otra pestaña con una vista en vivo de su sitio.  Esta pestaña del explorador se llamará la **ficha en vivo**.  
    
    > ##### Imagen 5  
    > La ficha en vivo  
    > ![La ficha en vivo][ImageCssSetup3]  

## Comprender CSS   

**CSS** es un lenguaje de equipos que determina el diseño y el estilo de las páginas Web.  Por ejemplo, a continuación se muestra un párrafo con un borde:  

> ##### Imagen 6  
> Esto se ha aplicado con estilo CSS  
> ![Esto se ha aplicado con estilo CSS][ImageCssStyled]  

Este es el código HTML y CSS usado para crear ese párrafo:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` probablemente te parezcan.  El resto debería ser familiar.  Si no es así, completa introducción [a HTML y al Dom][DevToolsBeginnersHtml] antes de intentar este tutorial.  

## Agregar estilos en línea   

Use **estilos en línea** cuando desee aplicar estilos a un solo elemento.  Pruébelo ahora:  

1.  Vuelva a la pestaña edición y Abra `index.html` .  
    
    > ##### Imagen 7  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  Añadir `style="background-color: aliceblue;"` a tu `<nav>` .  En el bloque de código siguiente, la cuarta línea de código es la que tiene que cambiar.  El resto es solo allí para que puedas asegurarte de que el nuevo código está en el lugar correcto.  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  Vaya a la **pestaña en vivo** para ver los cambios.  El fondo de la `<nav>` sección ahora es azul.  
    
    > ##### Imagen 8  
    > El color de fondo de la Página principal y los vínculos de contacto ahora es azul  
    > ![El color de fondo de la Página principal y los vínculos de contacto ahora es azul][ImageCssInline2]  

## Volver a usar estilos en una sola página con hojas de estilo internas   

Anteriormente, vimos un estilo en línea que aplicaba un estilo a una sola `<p>` etiqueta como esta:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

¿Qué ocurre si desea que todos los `<p>` elementos de la página web tengan el mismo estilo?  Tendría que copiar y pegar el código en cada `<p>` etiqueta del sitio.  Eso es mucho tiempo y esfuerzo.  Y, si necesitara realizar una edición, deberás volver a cambiar todas las etiquetas.  Las **hojas de estilos internas** permiten escribir una CSS una vez para que se aplique a varios elementos.  Pruébelo ahora:  

1.  En la ficha en vivo, haga clic en **contacto** para ir a la página de contacto.  Observe la fuente de **Inicio** y de **contacto**.  
    
    > ##### Imagen 9  
    > La página de contacto  
    > ![La página de contacto][ImageCssInternal1]  

1.  En la **pestaña Editor**, vaya a `contact.html` .  
1.  Agregue el código siguiente a `contact.html` .  Recuerde que las líneas que comienzan con `<style>` y terminan con `</style>` son lo que necesita sumar.  El otro código está allí para que sepa dónde colocar el nuevo código.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Volver a la **ficha en vivo**.  
1.  Haga clic en **contacto** para volver a la página de contacto.  La fuente de **Inicio** y de **contacto** ha cambiado.  
    
    > ##### Imagen 10  
    > La fuente de los vínculos de contactos y de inicio ha cambiado  
    > ![La fuente de los vínculos de contactos y de inicio ha cambiado][ImageCssInternal2]  
    
### Comprender las hojas de estilos internas   

Las hojas de estilo internas aplican estilos mediante **selectores**.  Los selectores son patrones que pueden aplicarse a uno o varios elementos HTML.  Por ejemplo, en el código anterior:  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` es un selector que se traduce en "any `<li>` que contiene un `<a>` ".  El explorador cambia la fuente de los vínculos de **contactos** y de **Inicio** porque coinciden con este patrón.  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` es una **declaración**.  Una declaración consta de dos partes: una **propiedad** y un **valor**.  `font-family` es la propiedad y `'Courier New', Courier, serif` es el valor de esa propiedad.  La propiedad describe una forma general de cambiar el estilo del elemento y el valor indica qué debe cambiar exactamente.  Por ejemplo, `font-family: 'Courier New', Courier, serif` ofrece al explorador estas instrucciones: "establecer la fuente de los elementos que coinciden con el patrón `li a` `'Courier New'` .  Si la fuente no está disponible, use `Courier` .  Si no está disponible, use `serif` ".  

### Agregar varios selectores a un conjunto de reglas   

Un conjunto de códigos CSS, como el que se muestra a continuación, se denomina conjunto de **reglas**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Use comas para agregar varios selectores a un conjunto de reglas.  Pruébelo ahora:  

1.  En la **pestaña Editor**, Abra `contact.html` .  
1.  Después del `li a` tipo `, h1` .  

    ```html
    ...
        ...
            ...
            <style>
                li a, h1 {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        ...
    ...
    ```  

    Esto indica al explorador que debe aplicar estilo a los `<h1>` elementos de la misma manera en que estilos de los elementos que coinciden con el patrón `li a` .  
    
1.  Ir a la **ficha en vivo**.  
1.  Haga clic en el vínculo de **contacto** para volver a la página de contacto.  Ahora, **póngase en contacto conmigo.** tiene la misma fuente que los vínculos de navegación.  
    
    > ##### Imagen 11  
    > El texto ' contactme! ' ahora tiene la misma fuente que los vínculos de contactos y de inicio  
    > ![El texto contactar conmigo.  ahora tiene la misma fuente que los vínculos de contactos y de inicio][ImageCssMultiple1]  

## Experimentar con DevTools   

Mientras continúa con el desarrollo web maestro, encontrarás que CSS puede ser complicado.  Escribirás algunas CSS y esperamos que se muestre de una forma, pero el explorador hace algo totalmente diferente.  Con Microsoft Edge DevTools es fácil experimentar con los cambios y ver inmediatamente cómo afectan esos cambios a la página.  

### Agregar una declaración a un Ruler existente en DevTools   

Cuando desee iterar en el estilo de un elemento existente, agregue una declaración a un conjunto de reglas existente.  Pruébelo ahora:  

1.  Haga clic con el botón derecho en el vínculo **Inicio** y seleccione **inspeccionar**.  
    
    > ##### Imagen 12  
    > Inspeccionar el vínculo Inicio  
    > ![Inspeccionar el vínculo Inicio][ImageCssAdd1]  
    
    DevTools se abre junto a la página.  El código que representa el vínculo de inicio, `<a href="/">Home</a>` está resaltado en azul en el árbol DOM.  Debe estar familiarizado [con la introducción a HTML y el Dom][DevToolsBeginnersHtml].  En la pestaña **estilos** , debajo del árbol DOM puede ver la `font-family: 'Courier New', Courier, serif` declaración que agregó a la `contact.html` anterior.  
    
    > ##### Imagen 13  
    > La pestaña estilos está debajo del árbol DOM  
    > ![La pestaña estilos está debajo del árbol DOM][ImageCssAdd2]  
    
    Si la ventana de DevTools es ancha, la pestaña estilos está a la derecha del árbol DOM.  
    
    > ##### Imagen 14  
    > La pestaña estilos está a la derecha del árbol DOM  
    > ![La pestaña estilos está a la derecha del árbol DOM][ImageCssAdd3]  
    
1.  Haga clic en el espacio en blanco a continuación `font-family: 'Courier New', Courier, Serif` para agregar una declaración nueva.  
    
    > ##### Imagen 15  
    > Agregar una declaración nueva  
    > ![Agregar una declaración nueva][ImageCssAdd4]  
    
1.  Escriba `color` y, a continuación, presione `Enter` .  La interfaz de usuario de autocompletar sugiere opciones mientras escribe.  
    
    > ##### Imagen 16  
    > Escritura `color`  
    > ![Color de escritura][ImageCssAdd5]  

1.  Escriba `magenta` y, a continuación, `Enter` vuelva a presionar.  Todo el texto de la página de contacto ahora es magenta.  
    
    > ##### Imagen 17  
    > Escritura `magenta`  
    > ![Escribir magenta][ImageCssAdd6]  
    
### Editar una declaración en DevTools   

También puede editar las declaraciones existentes en DevTools.  Pruébelo ahora:  

1.  Haga clic en el cuadrado magenta junto a `magenta` .  Aparece un selector de color.  
    
    > ##### Ilustración 18  
    > El selector de colores  
    > ![El selector de colores][ImageCssEdit1]  
    
1.  Use el selector de colores para cambiar el texto de la fuente a un color que le guste.  
    
    > ##### Ilustración 19  
    > Cambiar el color de la fuente a púrpura con el selector de colores  
    > ![Cambiar el color de la fuente a púrpura con el selector de colores][ImageCssEdit2]  

### Agregar un nuevo conjunto de reglas en DevTools   

También puede agregar nuevos conjuntos de conjuntos en DevTools.  Pruébelo ahora:  

1.  Haga clic en **nueva regla de estilo** ![ nueva regla ][ImageNewStyleRuleIcon] de estilo que está junto a **. CLS**.  Aparece un conjunto de reglas vacío con `a` el selector.  
    
    > ##### Ilustración 20  
    > Agregar una nueva regla  
    > ![Agregar una nueva regla][ImageCssRule1]  
    
1.  Reemplazar `a` por `a:hover` .  
    
    > ##### Ilustración 21  
    > Reemplazar `a` por `a:hover`  
    > ![Reemplazar un con a:hover][ImageCssRule2]  
    
    `:hover` es una **seudoclase**.  Use las pseudo-clases para aplicar estilo a los elementos cuando entran en Estados especiales.  Por ejemplo, el `a:hover` estilo solo surte efecto cuando se coloca el puntero sobre un `<a>` elemento.  
    
1.  Haga clic entre los corchetes para agregar una declaración nueva.  
1.  Escriba `background-color` el nombre de la declaración y, a continuación, pulse `Enter` .  
    
    > ##### Ilustración 22  
    > Escritura `background-color`  
    > ![Escribir el color de fondo][ImageCssRule3]  
    
1.  Escriba `green` el valor de la declaración y, a continuación, presione `Enter` .  
    
    > ##### Ilustración 23  
    > Escritura `green`  
    > ![Escritura de color verde][ImageCssRule4]  
    
1.  Mantenga el mouse sobre el vínculo **Inicio** .  El fondo del vínculo se vuelve de color verde.  
    
    > ##### Ilustración 24  
    > Situar el puntero sobre el vínculo de inicio para mostrar su fondo verde  
    > ![Situar el puntero sobre el vínculo de inicio para mostrar su fondo verde][ImageCssRule5]  
    
## Volver a usar estilos entre páginas con hojas de estilo externas   

Anteriormente, agregó esta hoja de estilos interna a `contact.html` :  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

¿Qué sucede si desea aplicar estilo `index.html` de la misma manera?  ¿Qué sucede si tenía *miles* de páginas y desea aplicar estos estilos a todas?  Tendría que copiar y pegar esta hoja de estilos interna en todas las páginas web del sitio.  Las **hojas de estilo externas** le permiten escribir la CSS una vez, la aplica a varias páginas.  Pruébelo ahora:  

1.  En primer lugar, vuelva a cargar la ficha en vivo para quitar los cambios que realizó en DevTools.  
    
    > ##### Ilustración 25  
    >  Después de volver a cargar la página, los cambios realizados en DevTools desaparecen  
    > ![ Después de volver a cargar la página, los cambios realizados en DevTools desaparecen][ImageCssExternal01]  
    
1.  Vuelva a la **pestaña Editor** y Abra `contact.html` .  
    
    > ##### Ilustración 26  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  Elimine todo lo que hay entre `<style>` y `</style>` , incluidos `<style>` y `</style>` .  
    
    > ##### Ilustración 27  
    > Se ha quitado la etiqueta de estilo  
    > ![Se ha quitado la etiqueta de estilo][ImageCssExternal03]  
    
1.  Ir a `index.html` y quitar `style="background-color: aliceblue;"` de la `<nav>` etiqueta.  Ahora ha quitado todas las CSS que agregó previamente a su sitio.  
    
    > ##### Ilustración 28  
    > El estilo insertado se ha quitado del elemento NAV  
    > ![El estilo insertado se ha quitado del elemento NAV][ImageCssExternal04]  

1.  Haga clic en **nuevo archivo**.  
    
    > ##### Ilustración 29  
    > El cuadro de diálogo nuevo archivo  
    > ![El cuadro de diálogo nuevo archivo][ImageCssExternal05]  
    
1.  Reemplazar `cool-file.js` por `style.css` y, a continuación, haga clic en **Agregar archivo**.  
    
    > ##### Ilustración 30  
    > Escritura `style.css`  
    > ![Escribir Style. CSS][ImageCssExternal06]  
    
1.  Pega este código en `style.css` :  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    > ##### Ilustración 31  
    > Agregar código a `style.css`  
    > ![Agregar código a Style. CSS][ImageCssExternal07]  
    
    En este momento, ha creado una hoja de estilos externa, pero el código HTML no sabe que ya existe.  
    
1.  Abra `index.html` .  
1.  Agrega `<link rel="stylesheet" href="style.css">` a tu HTML.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### Ilustración 32  
    > Vincular a `style.css`  
    > ![Vincular a Style. CSS][ImageCssExternal08]  

1.  Vaya a `contact.html` y agregue el vínculo allí.  
    
    > ##### Ilustración 33  
    > Vincular a `style.css` en `contact.html`  
    > ![Vincular a Style. CSS en contact.html][ImageCssExternal09]  

1.  Ir a la **ficha en vivo**.  La Página principal ahora tiene la misma fuente de la última sección y una sección de navegación azul.  
    
    > ##### Ilustración 34  
    > La Página principal  
    > ![La Página principal][ImageCssExternal10]  
    
1.  Haga clic en el vínculo de **contacto** para ir a la página de contacto.  La página de contacto tiene el mismo formato que la Página principal.  
    
    > ##### Ilustración 35  
    > La página de contacto  
    > ![La página de contacto][ImageCssExternal11]  
    
## Usar un marco CSS   

Los **Marcos CSS** son colecciones de estilos creados por otros programadores que facilitan la creación de atractivos sitios Web.  En lugar de definir estilos usted mismo, un marco de trabajo le proporciona una colección de estilos que puede usar en los elementos de la página.  

1.  Copie el siguiente código:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Vaya a la pestaña edición y pegue el código en `contact.html` .  
    
    > ##### Ilustración 36  
    > Vinculación a Framework en `contact.html`  
    > ![Vinculación al marco en contact.html][ImageCssFramework1]  
    
1.  Pega también el código `index.html` .  
    
    > ##### Ilustración 37  
    > Vinculación a Framework en `index.html`  
    > ![Vinculación al marco en index.html][ImageCssFramework2]  
    
1.  Vuelva a la pestaña en vivo para ver los cambios.  Aunque el color de fondo del `<nav>` y de la fuente de los `li a` elementos es el mismo, la fuente de los demás elementos ha cambiado.  
    
    > ##### Ilustración 38  
    > Algunas de las fuentes de la Página principal han cambiado debido al marco de trabajo  
    > ![Algunas de las fuentes de la Página principal han cambiado debido al marco de trabajo][ImageCssFramework3]  

### Usar una clase   

En la última sección, agregó bootstrap a sus páginas web, que cambió las fuentes de algunos de los elementos de su sitio.  Los marcos CSS pueden ayudarle a hacer cambios importantes en la página con muy poco código.  Pruébelo ahora cambiando el encabezado:  

1.  Copia este código:  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Agrega este código a tu `<header>` etiqueta en `index.html` .  
    
    > ##### Ilustración 39  
    > Agregar clases en `index.html`  
    > ![Agregar clases en index.html][ImageCssJumbotron1]  
    
1.  También puedes agregar el código a la `<header>` etiqueta `contact.html` .  
    
    > ##### Ilustración 40  
    > Agregar clases en `contact.html`  
    > ![Agregar clases en contact.html][ImageCssJumbotron2]  
    
1.  Ver los cambios en la ficha en vivo.  Ahora hay un gran cuadro gris en la parte de tu encabezado.  
    
    > ##### Ilustración 41  
    > El encabezado ahora tiene un gran cuadro gris a su lado  
    > ![El encabezado ahora tiene un gran cuadro gris a su lado][ImageCssJumbotron3]  
    
### Comprender las clases   

Las clases permiten asignar colecciones de estilos a elementos arbitrarios.  Por ejemplo, establecer el `class` atributo de las `<header>` etiquetas para `jumbotron` aplicar los estilos siguientes:  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Una ventaja de las clases es que permiten aplicar estilos a cualquier elemento que desee.  Por ejemplo, suponga que desea establecer el color de fondo de *algunos* `<p>` elementos en púrpura, pero no en *todos* .  Puede definir el estilo en una clase:  

```css
.custom-background {
  background-color: purple;
}
```  

Y, a continuación, aplique la clase solo a los `<p>` elementos a los que quiere aplicar un estilo:  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### Alinear elementos   

Bootstrap también proporciona clases para alinear elementos.  Pruébelo ahora:  

1.  Vuelva a la pestaña Editor y Abra `index.html` .  
1.  Agregar `class="container-fluid"` a la `<body>` etiqueta.  
    
    > ##### Ilustración 42  
    > Agregar la `container-fluid` clase  
    > ![Agregar la clase de fluidos contenedor][ImageCssAlign1]  

1.  Ajustar los `<nav>` `<main>` elementos y en `<div class="row">` .  Asegúrate `</div>` de poner después `</main>` para cerrar correctamente la nueva etiqueta.  
    
    > ##### Ilustración 43  
    > Agregar una fila  
    > ![Agregar una fila][ImageCssAlign2]  
    
1.  Agregar `class="col-3"` a la `<nav>` etiqueta y `class="col-9"` a la `<main>` etiqueta.  
    
    > ##### Ilustración 44  
    > Agregar las `col-3` `col-9` clases y  
    > ![Agregar las clases col-3 y col-9][ImageCssAlign3]  
    
1.  Ver los cambios en la ficha en vivo.  
    
    > ##### Ilustración 45  
    > Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal.  
    > ![Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal.][ImageCssAlign4]  
    
## Pasos siguientes   

¡Enhorabuena!  ¡Has terminado!  

*   La mejor manera de mejorar el desarrollo web es crear más sitios.  No te preocupes por la rotura de cosas.  Divertirte y aprender todo lo que puedes a lo largo del camino.  
*   Consulte [Introducción a CSS][MDNCssFirstSteps] para obtener más información sobre cómo aplicar estilos a páginas Web.  
*   Siga nuestros tutoriales Introducción a la [visualización y el cambio de CSS][DevtoolsCssIndex] para obtener más información sobre cómo puede usar DevTools para experimentar con la CSS de una página.  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Ilustración 1: el aspecto de su sitio en este momento"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Ilustración 2: el aspecto que tendrá su sitio al final del tutorial"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Ilustración 3: la pestaña edición"  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Ilustración 4: el menú de opciones del proyecto"  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Ilustración 5: la ficha en vivo"  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Ilustración 6: esto se ha aplicado con estilo CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Ilustración 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Ilustración 8: el color de fondo de la Página principal y de los vínculos de contacto ahora es azul"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Ilustración 9: la página de contacto"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Ilustración 10: la fuente de los vínculos Home y Contact ha cambiado"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Ilustración 11: el texto ' contactme! ' ahora tiene la misma fuente que los vínculos Home y Contact"  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Ilustración 12: inspeccionar el vínculo de inicio"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Ilustración 13: la pestaña estilos está debajo del árbol DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Ilustración 14: la pestaña estilos está a la derecha del árbol DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Ilustración 15: agregar una declaración nueva"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Ilustración 16: escribir color"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Ilustración 17: escribir magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Ilustración 18: el selector de colores"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Ilustración 19: cambiar el color de la fuente a púrpura con el selector de colores"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Ilustración 20: agregar una nueva regla"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Ilustración 21: reemplazar un por a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Ilustración 22: escribir color de fondo"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Ilustración 23: escribir en verde"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Ilustración 24: mantener el puntero sobre el vínculo de inicio para mostrar su fondo verde"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Ilustración 25: después de volver a cargar la página, los cambios realizados en DevTools ya no están"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Ilustración 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Ilustración 27: se ha quitado la etiqueta Style"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Ilustración 28: el estilo insertado se ha quitado del elemento NAV"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Ilustración 29: el cuadro de diálogo nuevo archivo"  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Ilustración 30: escribir Style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Ilustración 31: agregar código a Style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Ilustración 32: vincular a Style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Ilustración 33: vincular a Style. CSS en contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Ilustración 34: la Página principal"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Ilustración 35: la página de contacto"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Ilustración 36: vinculación al marco en contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Ilustración 37: vinculación al marco en index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Ilustración 38: algunas de las fuentes de la Página principal han cambiado debido al marco de trabajo"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Ilustración 39: agregar clases en index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Ilustración 40: agregar clases en contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Ilustración 41: el encabezado ahora tiene un gran cuadro gris a su lado"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Ilustración 42: agregar la clase de fluidos contenedor"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Ilustración 43: agregar una fila"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Ilustración 44: agregar las clases col-3 y col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Ilustración 45: el contenido de NAV ahora está a la izquierda del contenido principal"  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools para principiantes: Introducción a HTML y el DOM"  
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cocinada-Amphibian | Intento"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeros pasos de CSS | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/css) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
