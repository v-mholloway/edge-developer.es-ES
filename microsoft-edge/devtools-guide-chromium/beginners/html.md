---
description: Introducción a HTML y el DOM
title: 'DevTools para principiantes: Introducción a HTML y el DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, devtools para principiantes, devtools de HTML para principiantes, devtools del DOM para principiantes, tutorial de devtools de html, tutorial de devtools del DOM, tutorial de devtools del document object model
ms.openlocfilehash: 184d6b9d130e7052a4f0d479e4837fa84281c6983ca50ab17d508b5a2f9cbe75
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802164"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools para principiantes: Introducción a HTML y el DOM  

Este es el primero de una serie de tutoriales que le enseñarán los conceptos básicos del desarrollo web. Obtenga información sobre un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, que pueden aumentar su productividad.  

En este tutorial se describe HTML y el [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\). HTML es una de las tecnologías principales del desarrollo web. Es el lenguaje que controla la estructura y el contenido de las páginas web. El DOM también está relacionado con la estructura y el contenido de las páginas web, sobre los que aprenderemos más adelante.

## <a name="goals"></a>Objetivos  

Aprenderá desarrollo web mediante la creación de un sitio web.  Cuando complete todos los tutoriales de la serie **DevTools para principiantes**, el sitio terminado puede tener un aspecto similar al de la siguiente figura.  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="El sitio terminado" lightbox="media/beginners-html-finished.msft.png":::
   El sitio terminado  
:::image-end:::  

Al final de este tutorial, debe comprender los siguientes conceptos.  

*   Cómo HTML y el DOM crean el contenido que se muestra en las páginas web.  
*   Cómo Microsoft Edge DevTools puede ayudarle a experimentar con los cambios de HTML y DOM.  
*   Diferencia entre HTML y el DOM.  

También tendrá un sitio web en funcionamiento. Puede usar el sitio para hospedar su currículo o blog.  

## <a name="prerequisites"></a>Requisitos previos  

Antes de iniciar este tutorial, complete los siguientes requisitos previos:  

*   Si no está familiarizado con HTML, lea [Tareas iniciales con HTML][MDNGettingStartedHtml].  
*   Descargue el explorador web [Microsoft Edge][MicrosoftEdgeInsider].  En este tutorial se usa un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, que están integradas en Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurar el código  

Va a crear un sitio en el editor de código en línea Glitch.  

1.  Abra el [código fuente][GlitchAlluringShockIndex]. Esta pestaña se denomina **pestaña del editor** a lo largo de este tutorial.  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="La pestaña del editor" lightbox="media/beginners-html-setup1.msft.png":::
       La pestaña del editor  
    :::image-end:::  
    
1.  Elija **alluring-shock**. Se abre el menú**Opciones del proyecto**.  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menú Opciones del proyecto" lightbox="media/beginners-html-setup2.msft.png":::
       Menú Opciones del proyecto  
    :::image-end:::  
    
1.  Elija **Replicar proyecto**. Glitch crea una copia del proyecto que puede editar y genera aleatoriamente un nuevo nombre para el proyecto. El contenido es el mismo que antes.  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="El proyecto replicado" lightbox="media/beginners-html-setup3.msft.png":::
       El proyecto replicado  
    :::image-end:::  
    
1.  Si tiene previsto completar el siguiente tutorial de esta serie, elija **Iniciar sesión** en Glitch con su cuenta de Facebook, GitHub o Google; o envíese un vínculo mágico por correo electrónico. Si decide no iniciar sesión en una cuenta, no podrá editar el proyecto después de cerrar la pestaña del editor.

1.  Elija **Mostrar** \> **En una nueva ventana**.  Se abre una nueva pestaña que muestra la página en tiempo real. Esta pestaña se denomina **pestaña en tiempo real** a lo largo de este tutorial.  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="La pestaña en tiempo real" lightbox="media/beginners-html-setup4.msft.png":::
       La pestaña en tiempo real  
    :::image-end:::  
    
## <a name="add-content"></a>Agregar contenido  

El sitio necesita más información. Complete los siguientes pasos para agregar contenido.  

1. En la **pestaña del editor**, reemplace `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>`.  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="El nuevo código está resaltado en la pestaña del editor" lightbox="media/beginners-html-add1.msft.png":::
        El nuevo código está resaltado en la pestaña del editor  
    :::image-end:::  
    
1. Vea los cambios en la **pestaña en tiempo real**. El texto `About Me` está visible en la página. El texto es mayor que el texto adyacente porque el elemento `<h1>` representa un Título 1.  El explorador web aplica estilos automáticamente a los títulos en tamaños de fuente más grandes.  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="El nuevo título está visible en la pestaña en tiempo real" lightbox="media/beginners-html-add2.msft.png":::
       El nuevo título está visible en la pestaña en tiempo real  
    :::image-end:::  
    
1. De nuevo en la **pestaña del editor**, inserte `<p>I am learning web development. Recent accomplishments:</p>` en la línea después de  `<h1>About Me</h1>`.  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="El código actualizado está resaltado en la pestaña del editor" lightbox="media/beginners-html-add3.msft.png":::
        El código actualizado está resaltado en la pestaña del editor  
    :::image-end:::  
    
1. Vea el cambio en la **pestaña en tiempo real**.

1. De nuevo en la **pestaña del editor**, agregue una lista de sus logros con el código siguiente.
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="El código actualizado también está resaltado en la pestaña del editor" lightbox="media/beginners-html-add4.msft.png":::
        El código actualizado también está resaltado en la pestaña del editor  
    :::image-end:::  

1. Vea la **pestaña en tiempo real** para asegurarse de que el nuevo contenido se muestra correctamente.  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="La nueva lista está visible en la pestaña en tiempo real" lightbox="media/beginners-html-add5.msft.png":::
       La nueva lista está visible en la pestaña en tiempo real  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Experimentar con los cambios de contenido en Microsoft Edge DevTools  

Si está desarrollando una página con mucho HTML, resulta tedioso ir y retroceder entre la pestaña del editor y la pestaña en tiempo real para ver los cambios. Microsoft Edge DevTools le ayuda a experimentar con los cambios de contenido sin salir de la **pestaña en tiempo real**.  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Conozca la diferencia entre HTML y el DOM  

Antes de editar el contenido de Microsoft Edge DevTools, vamos a comprender la diferencia entre HTML y el DOM. Continúe con los siguientes pasos para aprender a partir de un ejemplo.

1. Vaya a la **pestaña en tiempo real**. En la parte inferior de la página, se mostrará el texto `A new element!?!`.  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. Abra la **pestaña del editor** e intente encontrar el texto en `index.html`. El texto no se muestra en esta vista.  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. Abra la **pestaña en tiempo real**, mantenga el puntero sobre `A new element!?!`, abra el menú contextual (haga clic con el botón derecho) y, a continuación, elija **Inspeccionar**.  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Inspeccionando texto" lightbox="media/beginners-html-dom3.msft.png":::
       Inspeccionando texto  
    :::image-end:::  
    
    DevTools se abrirá junto a la página. `<div>A new element!?!</div>` está resaltado. Aunque esta estructura de DevTools se parece a HTML, es el **árbol del DOM**.  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools está abierto junto a la página" lightbox="media/beginners-html-dom4.msft.png":::
       DevTools está abierto junto a la página  
    :::image-end:::  
    
Cuando se carga la página, el explorador usa el código HTML para crear el contenido inicial de la página. El DOM representa el contenido actual de la página, que puede cambiar con el tiempo. 

El contenido de `<div>A new element!?!</div>` se agrega a la página debido a la etiqueta `<script src="new.js"></script>` en la parte inferior del código HTML. Esta etiqueta hace que se ejecute algún código JavaScript. Obtenga más información sobre JavaScript en un [tutorial posterior](../javascript/index.md).

Por ahora, piense en él como un lenguaje de computación que puede cambiar el contenido de la página. En este caso, el código JavaScript agrega `<div>A new element!?!</div>` a la página. Este es el motivo por el que este texto se muestra en la pestaña **en tiempo real**, pero no en el código HTML.  

### <a name="edit-the-dom"></a>Edición del DOM  

Si quiere experimentar rápidamente con los cambios de contenido sin salir de la pestaña en tiempo real, pruebe DevTools.  

1.  En DevTools, mantenga el puntero sobre `Your site!`, abra el menú contextual (clic con el botón derecho) y elija **Editar como HTML**.  
    
1.  Reemplace `<p>Your site!</p>` por el siguiente código.  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Actualización del nodo como HTML" lightbox="media/beginners-html-edit2.msft.png":::
    Actualización del nodo como HTML  
::image-end:::  

1.  Seleccione `Control`+`Enter` \(Windows, Linux\) o `Command`+`Enter` \(macOS\) para guardar los cambios, o seleccione fuera del cuadro. Los cambios se muestran automáticamente en la vista en tiempo real de la página. El texto `Your site!` se ha reemplazado por el nuevo contenido.  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="El nuevo contenido se muestra inmediatamente en la página" lightbox="media/beginners-html-edit3.msft.png":::
       El nuevo contenido se muestra inmediatamente en la página  
    :::image-end:::  
    
Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido. Si actualiza la página o cierra la pestaña, se perderán los cambios. Si desea guardar los cambios, copie manualmente el código en el archivo HTML. En las dos secciones siguientes se muestran otras formas de cambiar el contenido del árbol del DOM.  

## <a name="reorder-nodes"></a>Reordenar nodos

También puede cambiar el orden de los nodos del DOM. Por ejemplo, en la página web, el menú de navegación está cerca de la parte inferior. Para moverlo a la parte superior, realice los siguientes pasos.  

1.  Busque el nodo `<nav>` en el **árbol del DOM** de DevTools.  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="El nodo de navegación está resaltado en DevTools" lightbox="media/beginners-html-reorder1.msft.png":::
       El nodo de navegación está resaltado en DevTools  
    :::image-end:::  
    
1.  Arrastre el nodo `<nav>` a la parte superior para que el nodo sea el primer elemento secundario después del nodo `<body>`.  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="El nodo de navegación está en la parte superior de la página" lightbox="media/beginners-html-reorder3.msft.png":::
        El nodo de navegación está en la parte superior de la página  
    :::image-end:::  
    
### <a name="delete-a-node"></a>Eliminación de un nodo

También puede quitar nodos del árbol del DOM. Para ello, realice los siguientes pasos:

1.  En el **árbol del DOM**, elija `<div>A new element!?!</div>`. DevTools resaltará el nodo. 
    
1.  Seleccione la tecla `Delete` del teclado.  El nodo `<div>A new element!?!</div>` se quitará del árbol del DOM.  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="El nodo se ha eliminado" lightbox="media/beginners-html-delete2.msft.png":::
       El nodo se ha eliminado  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Copie los cambios  

Ya casi ha terminado. Ha realizado algunos cambios a la página en DevTools, pero estos no se guardan en el código fuente.  

1.  Actualice la **pestaña en tiempo real**. Los cambios realizados en el árbol DOM desaparecerán. En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto `A new element!?!` vuelve a la parte inferior.  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Los cambios realizados han desaparecido" lightbox="media/beginners-html-copy1.msft.png":::
       Los cambios realizados han desaparecido  
    :::image-end:::  
    
1.  Copie el siguiente código.  
    
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
    
1.  Vuelva a la **pestaña del editor** y reemplace el contenido del archivo `index.html` por el código que copió.  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Aspecto que debería tener el archivo index.html" lightbox="media/beginners-html-copy2.msft.png":::
       El aspecto que debería tener el archivo `index.html`  
    :::image-end:::  
    
## <a name="next-steps"></a>Pasos siguientes  

*   Complete el siguiente tutorial en esta serie, [Introducción a CSS][DevToolsBeginnersCss], para aprender a aplicar estilo a la página y experimentar con cambios de estilo en Microsoft Edge DevTools.  
*   Lea [Introducción al DOM][MDNIntroductionDom] para obtener más información sobre el DOM.  
*   Consulte un curso como [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia práctica de desarrollo web.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para principiantes: Introducción a CSS | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - alluring-shock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción al DOM | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encontró [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y fue creada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
