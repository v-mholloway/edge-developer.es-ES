---
description: Introducción con CSS
title: 'DevTools para principiantes: Introducción a CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/26/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 99e8c525f910e42c1b58aed83bd25ef1229627cc6d42150516c9a0aa1589d95f
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802921"
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

# <a name="devtools-for-beginners-get-started-with-css"></a>DevTools para principiantes: Introducción a CSS  

En este tutorial, aprenderá a usar CSS para dar estilo a una página web.  También aprenderá a usar Microsoft Edge DevTools para experimentar con cambios CSS.  

Este artículo forma parte de una serie de tutoriales que le enseñarán los conceptos básicos del desarrollo web y Microsoft Edge DevTools.  Para obtener experiencia práctica, cree su propio sitio web.  No tiene que completar los tutoriales anteriores antes de hacerlo.  [Configurar el código muestra](#set-up-your-code) cómo configurarse.  

> [!NOTE]
> Este tutorial está diseñado para principiantes absolutos y se centra en los **conceptos básicos** del desarrollo web y los conceptos básicos del uso de DevTools para experimentar con CSS.  Si desea un tutorial que solo se centre en DevTools, vaya a [Introducción con Ver y cambiar CSS][DevtoolsCssIndex].  

Al principio del tutorial, el sitio debe ser parecido a la siguiente figura.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Cómo es el sitio actualmente" lightbox="../media/beginners-css-intro1.msft.png":::
   Cómo es el sitio actualmente  
:::image-end:::  

Después de completar el tutorial, el sitio debe tener el aspecto siguiente.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Cómo debe ser el sitio al final del tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   Cómo debe ser el sitio al final del tutorial  
:::image-end:::  

## <a name="goals"></a>Objetivos  

Siga este tutorial para comprender mejor los siguientes conceptos y tareas.  

*   Cómo usar CSS para dar estilo a una página web.  
*   Cómo usar Microsoft Edge DevTools para experimentar con CSS.  
*   La diferencia entre los marcos CSS y CSS.  

Está creando un sitio web real.  

## <a name="prerequisites"></a>Requisitos previos  

Complete los siguientes requisitos previos antes de realizar este tutorial.  

*   Complete [Introducción html y dom][DevtoolsBeginnersHtml] o asegúrese de que ya conoce HTML y DOM.  
*   Descargue el explorador web [Microsoft Edge][MicrosoftEdgeInsider].  En el siguiente tutorial se usa un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, integradas en Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurar el código  

Para crear el sitio, realice primero los siguientes pasos para configurar el código.  

> [!NOTE]
> Si ya ha completado el primer tutorial de la serie, vaya a la siguiente sección.  Siga usando el código del último tutorial, [Introducción con HTML y dom][DevtoolsBeginnersHtml].  

1.  Abra el [código fuente][GlitchCookedAmphibianIndex].  La pestaña del explorador que está seleccionado actualmente se denomina pestaña **de edición**.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="La pestaña de edición" lightbox="../media/beginners-css-setup1.msft.png":::
       La **pestaña de** edición  
    :::image-end:::  
    
1.  Seleccione **cooked-amphibian**.  Aparece un menú.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menú Opciones del proyecto" lightbox="../media/beginners-css-setup2.msft.png":::
       Menú Opciones del proyecto  
    :::image-end:::  

1.  Seleccione **Remezcla Project**.  Glitch crea una copia del proyecto que puede editar.  
    
    > [!NOTE]
    > Glitch genera un nombre aleatorio para el nuevo proyecto.  
    
1.  Seleccione **Mostrar** y, a continuación, **seleccione En una nueva ventana**.  Se abre otra pestaña con una vista en directo del sitio.  La pestaña del explorador que está seleccionado actualmente se denomina pestaña **activa**.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="La pestaña en tiempo real" lightbox="../media/beginners-css-setup3.msft.png":::
       La **pestaña activa**  
    :::image-end:::  

## <a name="understand-css"></a>Comprender CSS  

**CSS** es un lenguaje de equipo que controla el diseño y el estilo de las páginas web.  La siguiente figura es un párrafo con un borde.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="El texto se ha estilo con CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   El texto se ha estilo con CSS  
:::image-end:::  

El siguiente fragmento de código es el código HTML y CSS usado para crear el párrafo de la figura anterior.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Es posible que el atributo HTML `style="border: 1px dashed red; padding: 5px;"` tenga un aspecto nuevo.  El resto debería ser familiar.  Si no es así, [Introducción con HTML y dom][DevtoolsBeginnersHtml] antes de intentar las siguientes secciones.  

## <a name="add-inline-styles"></a>Agregar estilos en línea  

Puede usar estilos **en línea para** aplicar estilos a un solo elemento.  

1.  Vuelva a la pestaña de edición y abra `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       Abrir `index.html` en la pestaña de edición  
    :::image-end:::  
    
1.  Agregue el atributo `style="background-color: aliceblue;"` en el `<nav>` elemento.  En el bloque de código siguiente, la cuarta línea de código es la única que necesita cambiar.  Las otras líneas de código se muestran aquí para ayudarle a colocar el nuevo atributo en el lugar correcto.  
    
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
    
1.  Para mostrar los cambios, vaya a la **pestaña activa**.  El fondo de la `<nav>` sección es ahora azul.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="El color de fondo detrás de los vínculos Inicio y Contacto ahora es azul" lightbox="../media/beginners-css-inline2.msft.png":::
       El color de fondo detrás de los **vínculos Inicio** **y** Contacto ahora es azul  
    :::image-end:::  
    
## <a name="reuse-styles-on-a-single-page-with-internal-stylesheets"></a>Reutilizar estilos en una sola página con hojas de estilos internas  

En un fragmento de código anterior, un estilo en línea aplicó un estilo a una sola `<p>` etiqueta.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

¿Qué sucede si desea que todos los elementos de la página web se den el mismo `<p>` estilo?  Tendrías que copiar y pegar el código en cada etiqueta del sitio, lo que requeriría `<p>` mucho tiempo y esfuerzo.  Si necesita realizar una edición, tendrá que cambiar todas las etiquetas de nuevo.  En su lugar, en los pasos siguientes, se usa una **hoja** de estilos Interna para escribir el CSS una vez, de modo que se aplique a varios elementos.  

1.  En la pestaña activa, seleccione **Contacto** para navegar a la página de contacto.  Observe la fuente de los **vínculos Inicio** **y** Contacto.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="La página Contacto" lightbox="../media/beginners-css-internal1.msft.png":::
       La página Contacto  
    :::image-end:::  
    
1.  En la **pestaña editor**, abra `contact.html` .  
1.  Agregue el siguiente código a `contact.html` .  Recuerde que las líneas que comienzan `<style>` con y terminan con son las que necesita `</style>` agregar.  El otro código se muestra aquí para que sepa dónde colocar el nuevo código.  
    
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
    
1.  Vuelva a la **pestaña activa**.  
1.  Seleccione **Contacto** para volver a la página de contacto.  Observe que la fuente de los **vínculos Inicio** **y** Contacto ha cambiado.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La fuente de los vínculos Inicio y Contacto ha cambiado" lightbox="../media/beginners-css-internal2.msft.png":::
       La fuente de los **vínculos Inicio** **y** Contacto ha cambiado  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a>Comprender hojas de estilos internas  

Las hojas de estilos internas aplican estilos mediante **selectores**.  Los selectores son patrones que pueden aplicarse a uno o varios elementos HTML.  El fragmento de código anterior agregó el siguiente estilo.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` es un selector que se traduce a "cualquier `<li>` elemento que contenga un `<a>` elemento".  El explorador cambia la fuente de los vínculos **Inicio** y **Contacto** porque cada uno de los grupos de etiquetas coincide con el patrón.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` es una **declaración**.  Se realiza una declaración de dos partes siguientes.  

:::row:::
   :::column span="1":::
      **propiedad**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      La propiedad describe qué estilo del elemento debe cambiarse.  
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

Por ejemplo, `font-family: 'Courier New', Courier, serif` proporciona al explorador la siguiente instrucción: "Establecer la fuente de los elementos que coinciden con el patrón en `li a` `'Courier New'` .  Si esa fuente no está disponible, use `Courier` .  Si eso no está disponible, use `serif` ."  

### <a name="add-multiple-selectors-to-a-ruleset"></a>Agregar varios selectores a un conjunto de reglas  

El siguiente fragmento de código CSS se denomina **conjunto de reglas**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

En los pasos siguientes se describe cómo usar comas para agregar varios selectores a un conjunto de reglas.  

1.  En la **pestaña editor**, abra `contact.html` .  
1.  Después `li a` del tipo `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    El fragmento de código anterior indica al explorador que le de estilo a los elementos de la misma forma que estilos `<h1>` de elementos que coinciden con el patrón `li a` .  
    
1.  Vaya a la **pestaña activa**.  
1.  Seleccione el **vínculo** Contacto para volver a la página de contacto.  Ahora, **Póngase en contacto conmigo.** tiene la misma fuente que los vínculos de navegación.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="¡El texto Póngase en contacto conmigo!  ahora tiene la misma fuente que los vínculos Inicio y Contacto" lightbox="../media/beginners-css-multiple1.msft.png":::
       ¡El texto **Póngase en contacto conmigo!** ahora tiene la misma fuente que los vínculos **Inicio** **y** Contacto  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a>Experimentar con DevTools  

A medida que continúa su viaje para convertirse en un experto en desarrollo web, puede que encuentre que CSS es complicado.  Es posible que escribas algún código que no muestre lo que pretendías.  Microsoft Edge DevTools facilita la experimentación mostrando los cambios en la página en tiempo real.  

### <a name="add-a-declaration-to-an-existing-ruleset-in-devtools"></a>Agregar una declaración a un conjunto de reglas existente en DevTools  

Para agregar una declaración a un conjunto de reglas existente  

1.  Mantenga el mouse en **el vínculo** Inicio, abra el menú contextual \(haga clic con el botón secundario\) y seleccione **Inspeccionar**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspeccionar el vínculo Inicio" lightbox="../media/beginners-css-add1.msft.png":::
       Inspeccionar el vínculo Inicio  
    :::image-end:::  
    
    DevTools se abrirá junto a la página.  El código que representa el vínculo Inicio, `<a href="/">Home</a>` se resalta en azul en el árbol DOM.  El fragmento de código y la vista previa deben estar familiarizados [Introducción html y dom][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          En la siguiente figura, la declaración que agregó anteriormente se muestra en la pestaña Estilos debajo `font-family: 'Courier New', Courier, serif` `contact.html` del árbol DOM. ****  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="La pestaña Estilos está debajo del árbol DOM" lightbox="../media/beginners-css-add2.msft.png":::
             La **pestaña Estilos** está debajo del árbol DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si la ventana DevTools es amplia, la pestaña Estilos está a la derecha del árbol DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="La pestaña Estilos está a la derecha del árbol DOM" lightbox="../media/beginners-css-add3.msft.png":::
             La **pestaña Estilos** está a la derecha del árbol DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Seleccione la línea vacía siguiente `font-family: 'Courier New', Courier, Serif` para agregar una nueva declaración.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Agregar una nueva declaración" lightbox="../media/beginners-css-add4.msft.png":::
       Agregar una nueva declaración  
    :::image-end:::  
    
1.  Escriba `color` y seleccione `Enter` .  La interfaz de usuario de autocompletar sugiere opciones a medida que escribe.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Color de tipo" lightbox="../media/beginners-css-add5.msft.png":::
       Tipo `color`  
    :::image-end:::  
    
1.  Escriba `magenta` y seleccione `Enter` .  Todo el texto de la página de contacto ahora es magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Tipo magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Tipo `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a>Editar una declaración en DevTools  

Para editar declaraciones existentes en DevTools  

1.  Seleccione el cuadrado magenta junto a `magenta` .  Aparece un selector de colores.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Selector de colores" lightbox="../media/beginners-css-edit1.msft.png":::
       Selector de colores  
    :::image-end:::  
    
1.  Use el selector de colores para cambiar el texto de fuente a un color que quiera.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Cambiar el color de fuente a púrpura con el Selector de colores" lightbox="../media/beginners-css-edit2.msft.png":::
       Cambiar el color de fuente a púrpura con el Selector de colores  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a>Agregar un nuevo conjunto de reglas en DevTools  

Para agregar nuevos conjuntos de reglas en DevTools  

1.  Seleccione **Nueva regla de estilo** \( Nueva regla de estilo ![ ](../media/new-style-rule-icon.msft.png) \) que está junto a **.cls**.  Aparece un conjunto de reglas vacío `a` con como selector.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Agregar una nueva regla" lightbox="../media/beginners-css-rule1.msft.png":::
       Agregar una nueva regla  
    :::image-end:::  
    
1.  Reemplace `a` por `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Reemplazar a con a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       Reemplazar `a` por `a:hover`  
    :::image-end:::  
    
    `:hover` es una **pseudo-clase**.  Use pseudo-clases para elementos de estilo que puedan entrar en estados especiales.  Por ejemplo, el estilo solo tiene efecto cuando se pasa el `a:hover` mouse sobre un `<a>` elemento.  
    
1.  Seleccione el área vacía entre corchetes para agregar una nueva declaración.  

1.  Escriba `background-color` el nombre de declaración y seleccione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Tipo de fondo-color" lightbox="../media/beginners-css-rule3.msft.png":::
       Tipo `background-color`  
    :::image-end:::  
    
1.  Escriba `green` para el valor de declaración y seleccione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Escriba verde" lightbox="../media/beginners-css-rule4.msft.png":::
       Tipo `green`  
    :::image-end:::  
    
1.  Mantenga el mouse sobre el **vínculo** Inicio.  El fondo del vínculo se vuelve verde.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Mantenga el mouse en el vínculo Inicio para mostrar su fondo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       Mantenga el mouse en el vínculo Inicio para mostrar su fondo verde  
    :::image-end:::  
    
## <a name="reuse-styles-across-pages-with-external-stylesheets"></a>Reutilizar estilos en páginas con hojas de estilos externas  

En un paso anterior, agregó el siguiente fragmento de código como hoja de estilos interna a `contact.html` .  

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

¿Qué sucede si quieres dar `index.html` el mismo estilo?  ¿Qué sucede si tuviera un gran número de páginas a las que desea aplicar sus estilos?  Tendría que copiar y pegar la hoja de estilos interna en cada página web del sitio.  En los pasos siguientes se describe cómo agregar una hoja de estilos **externa** para que pueda escribir el CSS una vez y aplicarlo a varias páginas.  

1.  En primer lugar, actualice la pestaña activa para quitar los cambios realizados en DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Después de actualizar la página, los cambios realizados en DevTools han desaparecido" lightbox="../media/beginners-css-external1.msft.png":::
        Después de actualizar la página, los cambios realizados en DevTools han desaparecido  
    :::image-end:::  
    
1.  Vuelva a la **pestaña editor y** abra `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Elimine todo lo `<style>` que esté entre y , `</style>` `<style>` incluidos y `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Se ha quitado la etiqueta de estilo" lightbox="../media/beginners-css-external3.msft.png":::
       Se ha quitado la etiqueta de estilo  
    :::image-end:::  
    
1.  Abra `index.html` y quite de la `style="background-color: aliceblue;"` `<nav>` etiqueta.  Ahora ha quitado todo el CSS que agregó anteriormente al sitio.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="El estilo en línea se ha quitado del elemento nav" lightbox="../media/beginners-css-external4.msft.png":::
       El estilo en línea se ha quitado del elemento nav  
    :::image-end:::  
    
1.  Seleccione **Nuevo archivo**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="El nuevo cuadro de diálogo de archivo" lightbox="../media/beginners-css-external5.msft.png":::
       El nuevo cuadro de diálogo de archivo  
    :::image-end:::  
    
1.  Reemplace `cool-file.js` por y seleccione Agregar `style.css` **archivo**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Tipo style.css" lightbox="../media/beginners-css-external6.msft.png":::
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Agregar código a style.css" lightbox="../media/beginners-css-external7.msft.png":::
       Agregar código a `style.css`  
    :::image-end:::  
    
    Asegúrese de que ha creado una hoja de estilos externa. El HTML no es consciente de que existe.  
    
1.  Abra `index.html` .  
1.  Agregue `<link rel="stylesheet" href="style.css">` a su HTML.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Vínculo a style.css" lightbox="../media/beginners-css-external8.msft.png":::
       Vínculo a `style.css`  
    :::image-end:::  
    
1.  Abra el `contact.html` archivo y agregue el vínculo allí.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Vínculo a style.css en contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Vincular a `style.css` en `contact.html`  
    :::image-end:::  
    
1.  Vaya a la **pestaña activa**.  La página principal ahora tiene la misma fuente de la última sección y una sección de navegación azul.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="La página principal" lightbox="../media/beginners-css-external10.msft.png":::
       La página principal  
    :::image-end:::  
    
1.  Seleccione el **vínculo** Contacto para navegar a la página de contacto.  La página de contacto tiene el mismo formato que la página principal.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="La página de contacto" lightbox="../media/beginners-css-external11.msft.png":::
       La página de contacto  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a>Usar un marco CSS  

**Los marcos CSS** son colecciones de estilos creados por otros desarrolladores que facilitan la creación de sitios web atractivos.  En lugar de definir estilos usted mismo, un marco le proporciona una colección de estilos que puede usar en los elementos de la página.  

Siga estos pasos para agregar el marco CSS de Bootstrap a la página.  

1.  Copie el código siguiente:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Abra la pestaña de edición y pegue el código en `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Vínculo al marco en contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Vínculo al marco en `contact.html`  
    :::image-end:::  
    
1.  Abra el `index.html` archivo y agregue el código allí.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Vínculo al marco en index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Vínculo al marco en `index.html`  
    :::image-end:::  
    
1.  Vuelva a la pestaña activa para ver los cambios.  Aunque el color de fondo del elemento y la fuente de los elementos y son los mismos, la fuente `<nav>` de los otros elementos ha `<li>` `<a>` cambiado.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Parte de la fuente de la página principal ha cambiado debido al marco" lightbox="../media/beginners-css-framework3.msft.png":::
       Parte de la fuente de la página principal ha cambiado debido al marco  
    :::image-end:::  
    
### <a name="use-a-class"></a>Usar una clase  

En la última sección, agregó Bootstrap a las páginas web, lo que cambió las fuentes de algunos de los elementos del sitio.  Los marcos CSS le ayudan a realizar cambios importantes en la página con muy poco código.  Siga estos pasos para usar una de las clases de Bootstrap para cambiar el encabezado.  

1.  Copie el siguiente fragmento de código.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Agregue el fragmento de código anterior a la `<header>` etiqueta en `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Agregar clases en index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Agregar clases `index.html`  
    :::image-end:::  
    
1.  Agregue el código a la `<header>` etiqueta en `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Agregar clases en contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Agregar clases `contact.html`  
    :::image-end:::  
    
1.  Ver los cambios en la pestaña activa.  Hay un cuadro grande y gris alrededor del encabezado.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="El encabezado ahora tiene un cuadro gris grande alrededor de él" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       El encabezado ahora tiene un cuadro gris grande alrededor de él  
    :::image-end:::  
    
### <a name="understand-classes"></a>Comprender clases  

Las clases permiten asignar colecciones de estilos a elementos arbitrarios.  Use el siguiente fragmento de código para aplicar varios estilos al `<header>` elemento después de establecer el atributo en `class` `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Una ventaja de una clase es que le permite aplicar estilos a los elementos que desee.  Por ejemplo, supongamos que desea establecer el color de fondo de algunos `<p>` elementos en púrpura, pero no todos los `<p>` elementos.  Use el siguiente fragmento de código para definir el estilo de una clase.  

```css
.my-class-name {
  background-color: purple;
}
```  

A continuación, aplique la clase solo a los `<p>` elementos que desee aplicar estilo.  

```html
<p>The text is not purple.</p>
<p class="my-class-name">The text is purple.</p>
<p>The text is not purple.</p>
<p class="my-class-name">The text is purple.</p>
```  

### <a name="align-elements"></a>Alinear elementos  

Complete los pasos siguientes para usar otras clases de Bootstrap que sean útiles para alinear elementos.  

1.  Vuelva a la pestaña editor y abra `index.html` .  
1.  Agregue `class="container-fluid"` a la `<body>` etiqueta.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Agregar la clase container-fluid" lightbox="../media/beginners-css-align1.msft.png":::
       Agregar la `container-fluid` clase  
    :::image-end:::  
    
1.  Ajuste los `<nav>` elementos `<main>` y en `<div class="row">` .  Asegúrese de colocar `</div>` después `</main>` para cerrar correctamente la nueva etiqueta.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Agregar una fila" lightbox="../media/beginners-css-align2.msft.png":::
       Agregar una fila  
    :::image-end:::  
    
1.  Agregue `class="col-3"` a la etiqueta y a la `<nav>` `class="col-9"` `<main>` etiqueta.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Agregar las clases col-3 y col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Agregar las `col-3` clases y `col-9`  
    :::image-end:::  
    
1.  Ver los cambios en la pestaña activa.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="El contenido de navegación está ahora a la izquierda del contenido principal" lightbox="../media/beginners-css-align4.msft.png":::
       El contenido de navegación está ahora a la izquierda del contenido principal  
    :::image-end:::  
    
## <a name="next-steps"></a>Pasos siguientes  

Enhorabuena, ha terminado.  

*   La mejor forma de mejorar el desarrollo web es crear más sitios.  No te preocupes por las cosas que se rompen.  Simplemente diviértase y aprenda lo más posible a lo largo del camino.  
*   Para obtener más información sobre el estilo de páginas web, vaya a [Introducción a CSS][MDNCssFirstSteps].  
*   Para obtener más información sobre cómo experimentar con CSS en DevTools, vaya a [Introducción con Ver y cambiar CSS][DevtoolsCssIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para principiantes: Introducción con HTML y el dom | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Introducción Con vista y cambio de CSS | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html- cocinado-anfibio | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeros pasos de CSS | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encontró [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/css) y fue creada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
