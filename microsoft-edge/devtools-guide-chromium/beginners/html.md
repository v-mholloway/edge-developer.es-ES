---
title: DevTools para principiantes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581590"
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

# DevTools para principiantes: Introducción a HTML y el DOM   

Este es el primero de una serie de tutoriales que enseñan los conceptos básicos del desarrollo web.  También aprenderá un conjunto de herramientas para desarrolladores web denominado Microsoft Edge DevTools, que puede aumentar su productividad.  

En este tutorial en particular, obtendrá información sobre HTML y DOM.  HTML es una de las tecnologías básicas de desarrollo web.  Es el lenguaje que controla la estructura y el contenido de las páginas Web.  El DOM también está relacionado con la estructura y el contenido de las páginas web, pero obtendrá más información sobre esto más adelante.  

## Principales   

Va a aprender a usar el desarrollo web creando su propio sitio Web.  Cuando complete todos los tutoriales de la serie *DevTools para principiantes* , el sitio finalizado tendrá el aspecto que se muestra en la **Ilustración 1**.  

> ##### Figura 1  
> El sitio finalizado  
> ![El sitio finalizado][ImageHtmlFinished]  

Al final de este tutorial, comprenderá lo siguiente:  

*   Cómo los HTML y el DOM crean el contenido que se ve en las páginas Web.  
*   Cómo puede ayudarte Microsoft Edge DevTools a experimentar con los cambios de HTML y DOM.  
*   La diferencia entre HTML y DOM.  

También tendrá un sitio web real.  Puede usar este sitio para hospedar su currículum o su blog.  

## Requisitos previos   

Antes de intentar este tutorial, complete los siguientes requisitos previos:  

*   Si no está familiarizado con HTML, lea [Introducción a HTML][MDNGettingStartedHtml].  
*   Descarga el explorador Web [Microsoft Edge][MicrosoftEdgeInsider] .  En este tutorial se usa un conjunto de herramientas de desarrollo web, denominado Microsoft Edge DevTools, que está integrado en Microsoft Edge.  

## Configurar el código   

Va a crear su sitio en un editor de código en línea denominado problema.  

1.  Abra el [código fuente][GlitchAlluringShockIndex].  Esta pestaña se denomina la **pestaña Editor** a lo largo de este tutorial.  
    > ##### Figura 2  
    > Ficha Editor  
    > ![Ficha Editor][ImageHtmlSetup1]  

1.  Haga clic en **alluring-shock**.  El menú opciones de proyecto se abre en la esquina superior izquierda.  
    
    > #### Imagen 3  
    > El menú opciones del proyecto  
    > ![El menú opciones del proyecto][ImageHtmlSetup2]  
    
1.  Haga clic en **Remix proyecto**.  Problema crea una copia del proyecto que puede editar y genera de forma aleatoria un nombre nuevo para el proyecto.  El contenido es el mismo que antes.  
    
    > ##### Imagen 4  
    > El proyecto remixto  
    > ![El proyecto remixto][ImageHtmlSetup3]  
    
1.  Si planea completar el siguiente tutorial de esta serie, haga clic en **iniciar sesión** e inicie sesión en un problema con su cuenta de Github o Facebook.  Si no inicia sesión, perderá la posibilidad de editar este proyecto una vez que cierre la pestaña edición.  
1.  Haga clic en **Mostrar** y seleccione **en una ventana nueva**.  Se abre una nueva pestaña, que muestra la página en vivo.  Esta pestaña se denominará **pestaña en vivo** en este tutorial.  
    
    > ##### Imagen 5  
    > La ficha en vivo  
    > ![La ficha en vivo][ImageHtmlSetup4]  
    
## Agregar contenido   

Tu sitio está vacío.  Siga los pasos que se indican a continuación para agregar algo de contenido.  

1.  En la **pestaña Editor**, reemplace `<!-- You're "About Me" will go here.  -->` con `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### Imagen 6  
    > El nuevo código está resaltado en la pestaña Editor  
    > ![El nuevo código está resaltado en la pestaña Editor][ImageHtmlAdd1]  
    
1.  Ver los cambios en la **ficha en vivo**.  El texto `About Me` está visible en la página.  Es más grande que el resto del texto, porque el `<h1>` elemento representa un encabezado de sección.  El explorador Web estilos automáticamente los títulos en tamaños de fuente mayores.  
    
    > ##### Imagen 7  
    > El nuevo título está visible en la pestaña en vivo  
    > ![El nuevo título está visible en la pestaña en vivo][ImageHtmlAdd2]  
    
1.  De nuevo en la **pestaña Editor**, inserte `<p>I am learning HTML.  Recent accomplishments:</p>` en la línea debajo de la cual acaba de colocar `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### Imagen 8  
    > El nuevo código está resaltado en la pestaña Editor  
    > ![El nuevo código está resaltado en la pestaña Editor][ImageHtmlAdd3]  
    
1.  Ver el cambio en la **ficha en vivo**.  
1.  En la **pestaña Editor**, agregue una lista de sus logros:  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### Imagen 9  
    > El nuevo código está resaltado en la pestaña Editor  
    > ![El nuevo código está resaltado en la pestaña Editor][ImageHtmlAdd4]  
    
1.  De nuevo, vuelva a la **pestaña en vivo** para asegurarse de que el nuevo contenido se muestra correctamente.  
    
    > ##### Imagen 10  
    > La nueva lista está visible en la pestaña en vivo  
    > ![La nueva lista está visible en la pestaña en vivo][ImageHtmlAdd5]  
    
## Experimentar con los cambios de contenido en Microsoft Edge DevTools   

Si estuviera desarrollando una gran página con un gran número de HTML, puede imaginarse que es algo tedioso de volver y adelante entre la pestaña Editor y la ficha en vivo centenares de veces para ver los cambios, sobre todo si no está seguro de lo que debe colocar exactamente en la página.  Microsoft Edge DevTools puede ayudarte a experimentar con los cambios de contenido sin salir de la ficha en vivo.  

### Obtener información sobre la diferencia entre HTML y DOM   

Antes de empezar a editar el contenido desde Microsoft Edge DevTools, resulta útil comprender la diferencia entre HTML y DOM.  La mejor manera de aprender es por ejemplo:  

1.  Ir a la **ficha en vivo**.  En la parte inferior de la página verá el texto `A new element!?!` .  
    
    > ###### Imagen 11  
    > En la parte inferior de la página `A new element!?!` se puede ver el texto.  
    > ![En la parte inferior de la página, el texto de un nuevo elemento!?! se puede ver][ImageHtmlDom1]  
    
1.  Vuelva a la **pestaña Editor** y busque este texto `index.html` .  ¡ No está allí!  
    
    > ##### Imagen 12  
    > El misterio `A new element!?!` no se encuentra en ningún `index.html`  
    > ![El dedo texto un elemento nuevo!?! no se encuentra en el índice. html][ImageHtmlDom2]  
    
1.  Vuelva a la **ficha en vivo**, haga clic con el botón derecho `A new element!?!` y seleccione **inspeccionar**.  
    
    > ##### Imagen 13  
    > Inspeccionar texto  
    > ![Inspeccionar texto][ImageHtmlDom3]  
    
    DevTools se abre junto a la página.  `<div>A new element!?!</div>` está resaltado en azul.  Aunque esta estructura de DevTools se parece al código HTML, realmente es el **árbol DOM**.  
    
    > ##### Imagen 14  
    > DevTools está abierto junto a la página  
    > ![DevTools está abierto junto a la página][ImageHtmlDom4]  
    
Cuando se carga la página, el explorador toma el código HTML para crear el contenido *inicial* de la página.  DOM representa el contenido *actual* de la página, que puede cambiar a lo largo del tiempo.  El `<div>A new element!?!</div>` contenido misterioso se agrega a tu página debido a la `<script src="new.js"></script>` etiqueta de la parte inferior de tu HTML.  Esta etiqueta hace que se ejecute código JavaScript.  Obtendrá más información sobre JavaScript en un tutorial posterior, pero por ahora piense en él como un lenguaje de programación que puede cambiar el contenido de la página.  En este caso en particular, el código de JavaScript `<div>A new element!?!</div>` se agrega a la página.  Este es el motivo por el que este texto de misterios está visible en tu página en vivo, pero no en tu HTML.  

### Editar el DOM   

Si desea experimentar rápidamente cambios de contenido sin salir de la pestaña en vivo, pruebe DevTools.  

1.  En DevTools, haga clic con el botón derecho `Your site!` y seleccione **Editar como html**.  

    > ##### Imagen 15  
    > Editar el nodo como HTML  
    > ![Editar el nodo como HTML][ImageHtmlEdit1]  
    
1.  Reemplaza `<p>Your site!</p>` con el código a continuación.  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### Imagen 16  
    > Editar el nodo como HTML  
    > ![Editar el nodo como HTML][ImageHtmlEdit2]  
    
1.  Pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para guardar los cambios, o haga clic fuera del cuadro.  Los cambios se muestran automáticamente en la vista en vivo de la página.  El texto `Your site!` ha sido reemplazado por el nuevo contenido.  
    
    > ##### Imagen 17  
    > El nuevo contenido se muestra inmediatamente en la página  
    > ![El nuevo contenido se muestra inmediatamente en la página][ImageHtmlEdit3]  
    
Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido.  Si vuelve a cargar la página o cierra la pestaña, los cambios desaparecerán para siempre.  Si está usando este flujo de trabajo y quiere guardar los cambios, debe copiar manualmente esos cambios en el código HTML.  El siguiente par de secciones le muestran algunas formas más de cambiar el contenido del árbol DOM.  

## Reordenar nodos   

También puede cambiar el orden de los nodos DOM.  Por ejemplo, en la página web el menú de navegación está cerca de la parte inferior.  Para moverlo a la parte superior:  

1.  Busque el `<nav>` nodo en el **árbol DOM** de DevTools.  
    
    > ##### Ilustración 18  
    > El nodo NAV está resaltado en azul en DevTools  
    > ![El nodo NAV está resaltado en azul en DevTools][ImageHtmlReorder1]  
    
1.  Arrastre el `<nav>` nodo a la parte superior, de modo que sea el primer secundario debajo `<body>` del nodo.  
    > ##### Ilustración 19  
    > Arrastrar el nodo NAV a la parte superior  
    > ![Arrastrar el nodo NAV a la parte superior][ImageHtmlReorder2]  
    
    El `<nav>` nodo se muestra ahora en la parte superior de la página.  
    
    > ##### Ilustración 20  
    > El nodo NAV está en la parte superior de la página  
    > ![El nodo NAV está en la parte superior de la página][ImageHtmlReorder3]  
    
### Eliminar un nodo   

También puede quitar nodos del árbol DOM.  

1.  En el **árbol DOM**, haga clic en `<div>A new element!?!</div>` .  DevTools resalta el nodo azul.  
    
    > ##### Ilustración 21  
    > Selección del nodo que se va a eliminar  
    > ![Selección del nodo que se va a eliminar][ImageHtmlDelete1]  
    
1.  Presione la `Delete` tecla del teclado.  El `<div>A new element!?!</div>` nodo se elimina del árbol DOM.  
    
    > ##### Ilustración 22  
    > El nodo ha sido eliminado  
    > ![El nodo ha sido eliminado][ImageHtmlDelete2]  
    
## Copiar los cambios   

Ya casi lo ha hecho.  Ha realizado algunos cambios en la página en DevTools, pero aún no se han guardado en el código fuente.  

1.  Actualice la **ficha en vivo**.  Los cambios que realizó en el árbol DOM desaparecen.  En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto `A new element!?!` vuelve a la parte inferior.  
    
    > ##### Ilustración 23  
    > Los cambios que ha realizado han desaparecido  
    > ![Los cambios que ha realizado han desaparecido][ImageHtmlCopy1]  

1.  Copia el siguiente código.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  Vuelva a la **pestaña Editor** y reemplace el contenido del `index.html` archivo por el que acaba de copiar.  
    
    > ##### Ilustración 24  
    > Aspecto del `index.html` archivo  
    > ![Cómo debería tener el archivo index. html][ImageHtmlCopy2]  
    
## Pasos siguientes   

*   Complete el siguiente tutorial de esta serie, [Introducción a CSS][DevToolsBeginnersCss], para obtener información sobre cómo aplicar un estilo a la página y probar los cambios de estilo en Microsoft Edge DevTools.  
*   Lea [la introducción al Dom][MDNIntroductionDom] para obtener más información sobre el Dom.  
*   Consulta un curso como la [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia de desarrollo web de manos libres.  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Ilustración 1: el sitio finalizado"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Ilustración 2: la ficha Editor"  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Ilustración 3: el menú de opciones del proyecto"  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Ilustración 4: el proyecto remixto"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Ilustración 5: la ficha en vivo"  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Ilustración 6: el nuevo código está resaltado en la pestaña Editor"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Ilustración 7: el nuevo título está visible en la pestaña en vivo"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Ilustración 8: el nuevo código está resaltado en la pestaña Editor"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Ilustración 9: el nuevo código está resaltado en la pestaña Editor"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Ilustración 10: la nueva lista está visible en la pestaña en vivo"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Ilustración 11: en la parte inferior de la página el texto de un nuevo elemento!?! se puede ver"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Ilustración 12: el dedo texto un elemento nuevo!?! no se encuentra en el índice. html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Ilustración 13: inspeccionar texto"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Ilustración 14: DevTools está abierto junto a la página"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Ilustración 15: editar el nodo como HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Ilustración 16: editar el nodo como HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Ilustración 17: el nuevo contenido se muestra inmediatamente en la página"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Ilustración 18: el nodo NAV está resaltado en azul en DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Ilustración 19: arrastrar el nodo NAV a la parte superior"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Ilustración 20: el nodo NAV se encuentra en la parte superior de la página"  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Ilustración 21: selección del nodo que se va a eliminar"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Ilustración 22: el nodo se ha eliminado"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Ilustración 23: los cambios que ha realizado han desaparecido"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Ilustración 24: el aspecto del archivo index. html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools para principiantes: Introducción a CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. html-alluring-shock | Intento"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y está creada por [Katherine Jackson][KatherineJackson] \ (redactor técnico interno, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
