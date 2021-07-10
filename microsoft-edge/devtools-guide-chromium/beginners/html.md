---
description: Introducción con HTML y DOM
title: 'DevTools para principiantes: Introducción a HTML y DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, devtools for beginners, devtools HTML for beginners, devtools DOM for beginners, devtools html tutorial, devtools DOM tutorial, devtools document object model tutorial
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643572"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools para principiantes: Introducción a HTML y DOM  

Este es el primero de una serie de tutoriales que le enseñarán los conceptos básicos del desarrollo web. Obtenga información sobre un conjunto de herramientas de desarrollador web, denominadas Microsoft Edge DevTools, que pueden aumentar su productividad.  

En este tutorial se describe HTML y [el modelo de objetos de documento](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\). HTML es una de las tecnologías principales del desarrollo web. Es el idioma que controla la estructura y el contenido de las páginas web. El DOM también está relacionado con la estructura y el contenido de las páginas web, de los que más información nos enteramos más adelante.

## <a name="goals"></a>Objetivos  

Va a aprender el desarrollo web mediante la creación de un sitio web.  Para cuando complete todos los tutoriales de la serie **DevTools para** principiantes, el sitio terminado puede tener el aspecto siguiente.  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="El sitio terminado" lightbox="media/beginners-html-finished.msft.png":::
   El sitio terminado  
:::image-end:::  

Al final de este tutorial, debe comprender los siguientes conceptos.  

*   Cómo HTML y DOM crean el contenido que se muestra en las páginas web.  
*   How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.  
*   La diferencia entre HTML y DOM.  

También tendrá un sitio web de trabajo. Puede usar el sitio para hospedar su currículum vitae o blog.  

## <a name="prerequisites"></a>Requisitos previos  

Antes de intentar este tutorial, complete los siguientes requisitos previos:  

*   Si no está familiarizado con HTML, lea [Introducción a HTML][MDNGettingStartedHtml].  
*   Descargue el [Microsoft Edge][MicrosoftEdgeInsider] web.  Este tutorial usa un conjunto de herramientas de desarrollo web, denominadas Microsoft Edge DevTools, integradas en Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurar el código  

Va a crear un sitio en el editor de código de Glitch online.  

1.  Abra el [código fuente][GlitchAlluringShockIndex]. Esta pestaña se denomina pestaña **editor a** lo largo de este tutorial.  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="Pestaña editor" lightbox="media/beginners-html-setup1.msft.png":::
       Pestaña editor  
    :::image-end:::  
    
1.  Elija **alluring-shock**. Se **abre Project menú Opciones** de configuración.  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menú Project opciones" lightbox="media/beginners-html-setup2.msft.png":::
       Menú Project opciones  
    :::image-end:::  
    
1.  Elija **Remezcla Project**. Glitch crea una copia del proyecto que puede editar y genera aleatoriamente un nuevo nombre para el proyecto. El contenido es el mismo que antes.  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="El proyecto remezclado" lightbox="media/beginners-html-setup3.msft.png":::
       El proyecto remezclado  
    :::image-end:::  
    
1.  Si tienes previsto completar el siguiente tutorial de esta serie, elige **Iniciar** sesión en Glitch con tu cuenta de Facebook, GitHub o Google; o envíate un vínculo mágico. Si decide no iniciar sesión en una cuenta, no podrá editar el proyecto después de cerrar la pestaña editor.

1.  Elija **Mostrar**  \>  **en una nueva ventana**.  Se abre una pestaña nueva que muestra la página activa. Esta pestaña se denomina pestaña **activa a** lo largo de este tutorial.  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="La pestaña activa" lightbox="media/beginners-html-setup4.msft.png":::
       La pestaña activa  
    :::image-end:::  
    
## <a name="add-content"></a>Agregar contenido  

El sitio necesita más información. Complete los pasos siguientes para agregar contenido.  

1. En la **pestaña editor**, reemplace `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="El nuevo código se resalta en la pestaña editor" lightbox="media/beginners-html-add1.msft.png":::
        El nuevo código se resalta en la pestaña editor  
    :::image-end:::  
    
1. Ver los cambios en la **pestaña activa**. El texto `About Me` está visible en la página. El texto es mayor que el texto circundante porque `<h1>` el elemento representa un encabezado 1.  El explorador web aplica estilos automáticamente a los encabezados en tamaños de fuente más grandes.  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="El nuevo encabezado está visible en la pestaña activa" lightbox="media/beginners-html-add2.msft.png":::
       El nuevo encabezado está visible en la pestaña activa  
    :::image-end:::  
    
1. Vuelva a la **pestaña editor**, inserte en la línea `<p>I am learning web development. Recent accomplishments:</p>` siguiente  `<h1>About Me</h1>` .  
    
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

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="El código actualizado se resalta en la pestaña editor" lightbox="media/beginners-html-add3.msft.png":::
        El código actualizado se resalta en la pestaña editor  
    :::image-end:::  
    
1. Ver el cambio en la **pestaña activa**.

1. De vuelta en la **pestaña editor,** agregue una lista de sus logros con el siguiente código.
    
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

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="El código actualizado también se resalta en la pestaña editor" lightbox="media/beginners-html-add4.msft.png":::
        El código actualizado también se resalta en la pestaña editor  
    :::image-end:::  

1. Vea la **pestaña activa para** asegurarse de que el nuevo contenido se muestra correctamente.  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="La nueva lista está visible en la pestaña activa" lightbox="media/beginners-html-add5.msft.png":::
       La nueva lista está visible en la pestaña activa  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Experimentar con cambios de contenido en Microsoft Edge DevTools  

Si está desarrollando una página con mucho HTML, se vuelve tedioso ir y venir entre la pestaña editor y la pestaña activa para ver los cambios. Microsoft Edge DevTools le ayuda a experimentar con los cambios de contenido sin salir nunca de **la pestaña en directo.**  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Obtenga información sobre la diferencia entre HTML y DOM  

Antes de editar contenido Microsoft Edge DevTools, vamos a comprender la diferencia entre HTML y DOM. Siga los pasos siguientes para obtener información de un ejemplo.

1. Vaya a la **pestaña activa**. En la parte inferior de la página, se muestra el `A new element!?!` texto.  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. Abra la **pestaña editor** e intente buscar el texto en `index.html` . El texto no se muestra en esta vista.  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. Abra la **pestaña activa**, mantenga el mouse sobre , abra el menú contextual (haga clic con el botón `A new element!?!` secundario) y, a continuación, elija **Inspeccionar**.  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Inspección de texto" lightbox="media/beginners-html-dom3.msft.png":::
       Inspección de texto  
    :::image-end:::  
    
    DevTools se abre junto a la página. `<div>A new element!?!</div>` está resaltado. Aunque esta estructura en DevTools tiene un aspecto similar a HTML, es el **árbol DOM**.  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools está abierto junto a la página" lightbox="media/beginners-html-dom4.msft.png":::
       DevTools está abierto junto a la página  
    :::image-end:::  
    
Cuando se carga la página, el explorador usa el CÓDIGO HTML para crear el contenido inicial de la página. El DOM representa el contenido actual de la página, que puede cambiar con el tiempo. 

El `<div>A new element!?!</div>` contenido se agrega a la página debido a la etiqueta en la parte inferior del `<script src="new.js"></script>` HTML. Esta etiqueta hace que se ejecute algún código JavaScript. Obtenga más información sobre JavaScript en un [tutorial posterior](../javascript/index.md).

Por ahora, piense en él como un lenguaje de scripting que puede cambiar el contenido de la página. En este caso, el código JavaScript se `<div>A new element!?!</div>` agrega a la página. Es por ello que este texto se muestra en la **pestaña** activa, pero no en el HTML.  

### <a name="edit-the-dom"></a>Editar el DOM  

Si quieres experimentar rápidamente con cambios de contenido sin salir de la pestaña en directo, prueba DevTools.  

1.  En DevTools, mantenga el mouse sobre , abra el menú contextual (haga clic con el botón `Your site!` secundario) y **elija Editar como HTML**.  
    
1.  Reemplace `<p>Your site!</p>` por el código siguiente.  

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

1.  Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\) para guardar los cambios o seleccione fuera del cuadro. Los cambios se muestran automáticamente en la vista en directo de la página. El texto `Your site!` se ha reemplazado por el nuevo contenido.  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="El nuevo contenido se muestra inmediatamente en la página" lightbox="media/beginners-html-edit3.msft.png":::
       El nuevo contenido se muestra inmediatamente en la página  
    :::image-end:::  
    
Este flujo de trabajo solo es adecuado para experimentar con cambios de contenido. Si actualiza la página o cierra la pestaña, los cambios se perderán. Si desea guardar los cambios, copie manualmente el código en el archivo HTML. En las dos secciones siguientes se muestran más formas de cambiar el contenido del árbol DOM.  

## <a name="reorder-nodes"></a>Reordenar nodos

También puede cambiar el orden de los nodos DOM. Por ejemplo, en la página web, el menú de navegación está cerca de la parte inferior. Para moverlo a la parte superior, siga estos pasos.  

1.  Busque el `<nav>` nodo en el árbol **DOM** de DevTools.  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="El nodo de navegación se resalta en DevTools" lightbox="media/beginners-html-reorder1.msft.png":::
       El nodo de navegación se resalta en DevTools  
    :::image-end:::  
    
1.  Arrastre el nodo a la parte superior, de modo `<nav>` que el nodo sea el primer elemento secundario después del `<body>` nodo.  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="El nodo de navegación está en la parte superior de la página" lightbox="media/beginners-html-reorder3.msft.png":::
        El nodo de navegación está en la parte superior de la página  
    :::image-end:::  
    
### <a name="delete-a-node"></a>Eliminar un nodo

También puede quitar nodos del árbol DOM. Realice los pasos siguientes.

1.  En el **árbol DOM,** elija `<div>A new element!?!</div>` . DevTools resalta el nodo. 
    
1.  Seleccione la `Delete` tecla del teclado.  El `<div>A new element!?!</div>` nodo se quita del árbol DOM.  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="El nodo se ha eliminado" lightbox="media/beginners-html-delete2.msft.png":::
       El nodo se ha eliminado  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Copiar los cambios  

Casi ha terminado. Ha realizado algunos cambios en la página en DevTools, pero no se guardan en el código fuente.  

1.  Actualice la **pestaña activa**. Los cambios realizados en el árbol DOM desaparecen. En concreto, el texto `Your site!` vuelve a la parte superior de la página y el texto vuelve a la parte `A new element!?!` inferior.  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Los cambios que ha realizado han desaparecido" lightbox="media/beginners-html-copy1.msft.png":::
       Los cambios que ha realizado han desaparecido  
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
    
1.  Vuelva a la **pestaña editor y** reemplace el contenido del archivo por el código que `index.html` copió.  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Cómo debe index.htmel archivo l" lightbox="media/beginners-html-copy2.msft.png":::
       Aspecto del `index.html` archivo  
    :::image-end:::  
    
## <a name="next-steps"></a>Pasos siguientes  

*   Complete el siguiente tutorial de esta serie, [Introducción con CSS][DevToolsBeginnersCss], para aprender a dar estilo a su página y experimentar con los cambios de estilo en Microsoft Edge DevTools.  
*   Lea [Introducción al DOM][MDNIntroductionDom] para obtener más información sobre el DOM.  
*   Consulte un curso como [Introducción al desarrollo web][CourseraIntroductionToWebDevelopment] para obtener más experiencia práctica en el desarrollo web.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para principiantes: Introducción con CSS | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introducción al desarrollo web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html- alluring-shock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introducción a html | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción al dom | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encontró [aquí](https://developers.google.com/web/tools/chrome-devtools/beginners/html) y fue creado por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
