---
description: Introducción a CSS
title: 'DevTools para principiantes: Introducción a CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 62821084af8c22809f6e14ca4038ee173efd964a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125338"
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

El siguiente artículo es el segundo tutorial de una serie de tutoriales que le enseñan los conceptos básicos del desarrollo web y Microsoft Edge DevTools.  Ganas experiencia práctica creando tu propio sitio Web.  No es necesario completar el primer tutorial antes de seguir con el segundo.  [Configurar el código](#set-up-your-code) le muestra cómo realizar la configuración.  

> [!NOTE]
> Este tutorial está diseñado para principiantes y se centra en los **conceptos básicos del desarrollo web** y en los conceptos básicos del uso de DevTools para experimentar con CSS.  Si desea un tutorial que solo se Centre en DevTools, vaya a [Introducción a la visualización y el cambio de CSS][DevtoolsCssIndex].  

Al principio del tutorial, el sitio debe tener un aspecto similar al de la siguiente ilustración.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-intro1.msft.png":::
   El aspecto de tu sitio en este momento  
:::image-end:::  

Después de completar el tutorial, el sitio debe tener una apariencia similar a la de la siguiente ilustración.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-intro2.msft.png":::
   Aspecto del sitio al final del tutorial  
:::image-end:::  

## Principales  

Siga este tutorial para comprender mejor los conceptos y las tareas siguientes.  

*   Cómo usar CSS para aplicar un estilo a una página web.  
*   Cómo usar Microsoft Edge DevTools para experimentar con CSS.  
*   La diferencia entre los marcos CSS y CSS.  

Estás creando un sitio web real.  

## Requisitos previos  

Antes de intentar este tutorial, complete los siguientes requisitos previos.  

*   Complete Introducción [a HTML y el Dom][DevtoolsBeginnersHtml] , o asegúrese de que tiene conocimientos de HTML y Dom parecidos a los impartidos en ese tutorial.  
*   Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .  El siguiente tutorial usa un conjunto de herramientas de desarrollo web, llamadas Microsoft Edge DevTools, que están integradas en Microsoft Edge.  

## Configurar el código  

Para crear su sitio, primero debe completar las siguientes acciones para configurar su código.  

> [!NOTE]
> Si ya ha completado el primer tutorial de la serie, vaya a la sección siguiente.  Continúa usando el código del último tutorial, [Introducción a HTML y el Dom][DevtoolsBeginnersHtml].  

1.  Abra el [código fuente][GlitchCookedAmphibianIndex].  Se hace referencia a la pestaña de foco del explorador como la **pestaña edición**.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-setup1.msft.png":::
       La ficha **edición**  
    :::image-end:::  
    
1.  Seleccione **cocido-Amphibian**.  Aparece un menú.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-setup2.msft.png":::
       El menú opciones del proyecto  
    :::image-end:::  

1.  Elija **Remix Project**.  Problema crea una copia del proyecto que se puede editar.  
    
    > [!NOTE]
    > El problema genera un nombre aleatorio para el nuevo proyecto.  
    
1.  Elija **Mostrar** y elija **una nueva ventana**.  Se abre otra pestaña con una vista en vivo de su sitio.  Se hace referencia a la pestaña en el foco del explorador como la **pestaña en vivo**.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-setup3.msft.png":::
       La **ficha en vivo**  
    :::image-end:::  

## Comprender CSS  

**CSS** es un lenguaje de equipos que determina el diseño y el estilo de las páginas Web.  La siguiente ilustración es un párrafo con borde.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   El texto se ha aplicado con estilo CSS  
:::image-end:::  

El siguiente fragmento de código es el código HTML y CSS utilizado para crear el párrafo en la ilustración anterior.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` probablemente te parezcan.  El resto debería ser familiar.  Si no es así, complete Introducción [a HTML y al Dom][DevtoolsBeginnersHtml] antes de intentar las siguientes secciones.  

## Agregar estilos en línea  

Complete las siguientes acciones para usar **estilos alineados** para aplicar estilos a un solo elemento.  

1.  Vuelva a la pestaña edición y Abra `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-inline1.msft.png":::
       Abrir `index.html` en la pestaña edición  
    :::image-end:::  
    
1.  Añadir `style="background-color: aliceblue;"` a tu `<nav>` .  En el bloque de código siguiente, la cuarta línea de código es la que tiene que cambiar.  El resto solo está allí, por lo que puedes asegurarte de poner el nuevo código en el lugar correcto.  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  Vaya a la **pestaña en vivo** para ver los cambios.  El fondo de la `<nav>` sección ahora es azul.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-inline2.msft.png":::
       El color de fondo de la **Página principal** y los vínculos de **contacto** ahora es azul  
    :::image-end:::  
    
## Volver a usar estilos en una sola página con hojas de estilo internas  

En un fragmento de código anterior, un estilo en línea aplicó un estilo a una sola `<p>` etiqueta.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

¿Qué ocurre si desea que todos los `<p>` elementos de la página web tengan el mismo estilo?  Tendría que copiar y pegar el código en cada `<p>` etiqueta del sitio.  Eso es mucho tiempo y esfuerzo.  Y, si necesita realizar una edición, tendrá que volver a cambiar todas las etiquetas.  Complete las siguientes acciones para usar una **hoja de estilos interna** para escribir la CSS una vez, de modo que se aplique a varios elementos.  

1.  En la ficha en vivo, elija **contacto** para ir a la página de contacto.  Observe la fuente de **Inicio** y de **contacto**.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-internal1.msft.png":::
       La página de contacto  
    :::image-end:::  
    
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
1.  Elija **contacto** para volver a la página de contacto.  La fuente de **Inicio** y de **contacto** ha cambiado.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-internal2.msft.png":::
       La fuente de los vínculos de **contactos** y de **Inicio** ha cambiado  
    :::image-end:::  
    
### Comprender las hojas de estilos internas  

Las hojas de estilo internas aplican estilos mediante **selectores**.  Los selectores son patrones que pueden aplicarse a uno o varios elementos HTML.  El fragmento de código anterior agregó el siguiente estilo.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` es un selector que se traduce en "cualquier `<li>` elemento que contiene un `<a>` elemento".  El explorador cambia la fuente de los vínculos de **contactos** y de **Inicio** , ya que cada uno de los grupos de etiquetas coincide con el patrón.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` es una **declaración**.  Una declaración consta de dos partes siguientes:  

:::row:::
   :::column span="1":::
      **propiedad**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      La propiedad describe una forma general de cambiar el estilo del elemento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **value**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      El valor describe exactamente cómo debe cambiar el estilo del elemento.  
   :::column-end:::
:::row-end:::  

Por ejemplo, `font-family: 'Courier New', Courier, serif` proporciona al explorador las siguientes instrucciones: "establecer la fuente de los elementos que coinciden con el patrón `li a` `'Courier New'` .  Si esa fuente no está disponible, use `Courier` .  Si no está disponible, use `serif` ".  

### Agregar varios selectores a un conjunto de reglas  

Un conjunto de códigos CSS, como el que se muestra a continuación, se denomina conjunto de **reglas**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Complete las siguientes acciones para usar comas para agregar varios selectores a un conjunto de reglas.  

1.  En la **pestaña Editor**, Abra `contact.html` .  
1.  Después del `li a` tipo `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    El fragmento de código anterior indica al explorador que debe aplicar estilo a los elementos `<h1>` de la misma manera en que estilos de los elementos que coinciden con el patrón `li a` .  
    
1.  Ir a la **ficha en vivo**.  
1.  Elija el vínculo de **contacto** para volver a la página de contacto.  Ahora, **póngase en contacto conmigo.** tiene la misma fuente que los vínculos de navegación.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-multiple1.msft.png":::
       El texto **contactar conmigo.** ahora tiene la misma fuente que los vínculos de **contactos** y de **Inicio**  
    :::image-end:::  
    
## Experimentar con DevTools  

A medida que continúe con el camino para convertirse en un experto en el desarrollo web, puede encontrarse con que CSS es complicado.  Puede escribir algo de CSS y esperar que se muestre de una forma, pero el explorador hace algo totalmente diferente.  Microsoft Edge DevTools permite experimentar con los cambios y ver inmediatamente cómo afectan los cambios a la página.  

### Agregar una declaración a un Ruler existente en DevTools  

Complete las siguientes acciones para iterar en el estilo de un elemento existente, agregue una declaración a un conjunto de reglas existente.  

1.  Desplace el puntero en el vínculo **Inicio** , abra el menú contextual \ (haga clic con el botón derecho \) y elija **inspeccionar**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-add1.msft.png":::
       Inspeccionar el vínculo de inicio  
    :::image-end:::  
    
    DevTools se abre junto a la página.  El código que representa el vínculo de inicio, `<a href="/">Home</a>` está resaltado en azul en el árbol DOM.  El fragmento de código y la vista previa deben conocer la [Introducción a HTML y el Dom][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          En la siguiente ilustración, la `font-family: 'Courier New', Courier, serif` declaración a la que ha agregado previamente `contact.html` se ve en la pestaña **estilos** , debajo del árbol DOM.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-add2.msft.png":::
             La pestaña **estilos** está debajo del árbol DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si la ventana de DevTools es ancha, la pestaña estilos está a la derecha del árbol DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-add3.msft.png":::
             La pestaña **estilos** está a la derecha del árbol DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Elija la línea vacía a continuación `font-family: 'Courier New', Courier, Serif` para agregar una declaración nueva.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-add4.msft.png":::
       Agregar una declaración nueva  
    :::image-end:::  
    
1.  Escriba `color` y seleccione `Enter` .  La interfaz de usuario de autocompletar sugiere opciones mientras escribe.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-add5.msft.png":::
       Tipo `color`  
    :::image-end:::  
    
1.  Escriba `magenta` y seleccione `Enter` .  Todo el texto de la página de contacto ahora es magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-add6.msft.png":::
       Tipo `magenta`  
    :::image-end:::  
    
### Editar una declaración en DevTools  

Complete las siguientes acciones para editar las declaraciones existentes en DevTools.  

1.  Elija el cuadrado magenta junto a `magenta` .  Aparece un selector de color.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-edit1.msft.png":::
       El selector de colores  
    :::image-end:::  
    
1.  Use el selector de colores para cambiar el texto de la fuente a un color que le guste.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-edit2.msft.png":::
       Cambiar el color de la fuente a púrpura con el selector de colores  
    :::image-end:::  
    
### Agregar un nuevo conjunto de reglas en DevTools  

Complete las acciones siguientes para agregar nuevos conjuntos de DevTools.  

1.  Elija **nueva regla de estilo** \ ( ![ nueva regla de estilo ][ImageNewStyleRuleIcon] \) que está junto a **. CLS**.  Aparece un conjunto de reglas vacío con `a` el selector.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-rule1.msft.png":::
       Agregar una nueva regla  
    :::image-end:::  
    
1.  Reemplazar `a` por `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-rule2.msft.png":::
       Reemplazar `a` por `a:hover`  
    :::image-end:::  
    
    `:hover` es una **seudoclase**.  Use las pseudo-clases para los elementos de estilo que pueden entrar en Estados especiales.  Por ejemplo, el `a:hover` estilo solo surte efecto cuando se coloca el puntero sobre un `<a>` elemento.  
    
1.  Elija entre los corchetes para agregar una declaración nueva.  
1.  Escriba `background-color` el nombre de la declaración y seleccione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-rule3.msft.png":::
       Tipo `background-color`  
    :::image-end:::  
    
1.  Escriba `green` el valor de declaración y seleccione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-rule4.msft.png":::
       Tipo `green`  
    :::image-end:::  
    
1.  Mantenga el mouse sobre el vínculo **Inicio** .  El fondo del vínculo se vuelve de color verde.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-rule5.msft.png":::
       Desplace el puntero sobre el vínculo Inicio para mostrar su fondo verde  
    :::image-end:::  
    
## Volver a usar estilos entre páginas con hojas de estilo externas  

En un paso anterior, agregó el siguiente fragmento de código como una hoja de estilos interna `contact.html` .  

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

¿Qué sucede si desea aplicar estilo `index.html` de la misma manera?  ¿Qué ocurre si tiene una gran cantidad de páginas a las que desea aplicar los estilos?  Tendría que copiar y pegar la hoja de estilos interna en todas las páginas web del sitio.  Complete las siguientes acciones para agregar una **hoja de estilos externa** que le permita escribir una vez su CSS y aplicarlo a varias páginas.  

1.  En primer lugar, vuelva a cargar la ficha en vivo para quitar los cambios que realizó en DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external1.msft.png":::
        Después de actualizar la página, los cambios realizados en DevTools desaparecen  
    :::image-end:::  
    
1.  Vuelva a la **pestaña Editor** y Abra `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Elimine todo lo que hay entre `<style>` y `</style>` , incluidos `<style>` y `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external3.msft.png":::
       Se ha quitado la etiqueta de estilo  
    :::image-end:::  
    
1.  Ir a `index.html` y quitar `style="background-color: aliceblue;"` de la `<nav>` etiqueta.  Ahora ha quitado todas las CSS que agregó previamente a su sitio.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external4.msft.png":::
       El estilo insertado se ha quitado del elemento NAV  
    :::image-end:::  
    
1.  Elija **nuevo archivo**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external5.msft.png":::
       El cuadro de diálogo nuevo archivo  
    :::image-end:::  
    
1.  Reemplazar `cool-file.js` por `style.css` y elija **Agregar archivo**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external6.msft.png":::
       Tipo `style.css`  
    :::image-end:::  
    
1.  Agregue el siguiente fragmento de código al `style.css` archivo.  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external7.msft.png":::
       Agregar código a `style.css`  
    :::image-end:::  
    
    Asegúrese de haber creado una hoja de estilos externa. El código HTML no es consciente de que existe.  
    
1.  Abra `index.html` .  
1.  Agrega `<link rel="stylesheet" href="style.css">` a tu HTML.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external8.msft.png":::
       Vínculo a `style.css`  
    :::image-end:::  
    
1.  Abra el `contact.html` archivo y agregue el vínculo.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external9.msft.png":::
       Vincular a `style.css` en `contact.html`  
    :::image-end:::  
    
1.  Ir a la **ficha en vivo**.  La Página principal ahora tiene la misma fuente de la última sección y una sección de navegación azul.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external10.msft.png":::
       La Página principal  
    :::image-end:::  
    
1.  Elija el vínculo de **contacto** para ir a la página de contacto.  La página de contacto tiene el mismo formato que la Página principal.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-external11.msft.png":::
       La página de contacto  
    :::image-end:::  
    
## Usar un marco CSS  

Los **Marcos CSS** son colecciones de estilos creados por otros programadores que facilitan la creación de atractivos sitios Web.  En lugar de definir estilos usted mismo, un marco de trabajo le proporciona una colección de estilos que puede usar en los elementos de la página.  

1.  Copie el siguiente código:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Vaya a la pestaña edición y pegue el código en `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-framework1.msft.png":::
       Vínculo al marco en `contact.html`  
    :::image-end:::  
    
1.  Abra el `index.html` archivo y agregue el código allí.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-framework2.msft.png":::
       Vínculo al marco en `index.html`  
    :::image-end:::  
    
1.  Vuelva a la pestaña en vivo para ver los cambios.  Aunque el color de fondo del `<nav>` elemento y la fuente de los `<li>` `<a>` elementos y son iguales, la fuente del resto de los elementos ha cambiado.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-framework3.msft.png":::
       Se cambió parte de la fuente de la Página principal a causa del marco de trabajo  
    :::image-end:::  
    
### Usar una clase  

En la última sección, agregó bootstrap a sus páginas web, que cambió las fuentes de algunos de los elementos de su sitio.  Los marcos CSS le ayudan a hacer cambios importantes en la página con muy poco código.  Complete las acciones siguientes para cambiar el encabezado.  

1.  Copie el siguiente fragmento de código.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Agregue el fragmento de código anterior a la `<header>` etiqueta en `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Agregar clases en `index.html`  
    :::image-end:::  
    
1.  Agrega el código a tu `<header>` etiqueta en `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Agregar clases en `contact.html`  
    :::image-end:::  
    
1.  Ver los cambios en la ficha en vivo.  Hay un cuadro gris grande en el encabezado.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       El encabezado ahora tiene un gran cuadro gris a su lado  
    :::image-end:::  
    
### Comprender las clases  

Las clases permiten asignar colecciones de estilos a elementos arbitrarios.  Use el siguiente fragmento de código para aplicar varios estilos al `<header>` elemento después de establecer el `class` atributo en `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Una de las ventajas de una clase es que le permite aplicar estilos a cualquier elemento que desee.  Por ejemplo, suponga que desea establecer el color de fondo de algunos `<p>` elementos en morado, pero no en todos los `<p>` elementos.  Use el siguiente fragmento de código para definir el estilo de una clase.  

```css
.custom-background {
  background-color: purple;
}
```  

A continuación, aplique la clase solo a los `<p>` elementos a los que quiere aplicar un estilo.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### Alinear elementos  

Complete las siguientes acciones para iniciar y proporcionar clases para alinear elementos.  

1.  Vuelva a la pestaña Editor y Abra `index.html` .  
1.  Agregar `class="container-fluid"` a la `<body>` etiqueta.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-align1.msft.png":::
       Agregar la `container-fluid` clase  
    :::image-end:::  
    
1.  Ajustar los `<nav>` `<main>` elementos y en `<div class="row">` .  Asegúrate `</div>` de poner después `</main>` para cerrar correctamente la nueva etiqueta.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-align2.msft.png":::
       Agregar una fila  
    :::image-end:::  
    
1.  Agregar `class="col-3"` a la `<nav>` etiqueta y `class="col-9"` a la `<main>` etiqueta.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-align3.msft.png":::
       Agregar las `col-3` `col-9` clases y  
    :::image-end:::  
    
1.  Ver los cambios en la ficha en vivo.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="El aspecto de tu sitio en este momento" lightbox="../media/beginners-css-align4.msft.png":::
       Ahora, el contenido de NAV se encuentra a la izquierda del contenido principal.  
    :::image-end:::  
    
## Pasos siguientes  

Ya ha terminado.  

*   La mejor manera de mejorar el desarrollo web es crear más sitios.  No te preocupes por la rotura de cosas.  Divertirte y aprender lo máximo posible en el camino.  
*   Para obtener más información sobre cómo aplicar estilos a páginas web, vaya a [Introducción a CSS][MDNCssFirstSteps].  
*   Para obtener más información sobre cómo usar DevTools para experimentar con el CSS de una página, vaya a [Introducción a la visualización y el cambio de CSS][DevtoolsCssIndex].  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para principiantes: Introducción a HTML y DOM | Microsoft docs"  
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

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
