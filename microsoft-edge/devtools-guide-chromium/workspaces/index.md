---
description: Obtenga información sobre cómo guardar los cambios realizados en DevTools en el disco.
title: Editar archivos con Áreas de trabajo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 69b9e4566324234afdaaa2670642b9fb454ebf2c3ccabe5ada1c569370f8e6bd
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798420"
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
# <a name="edit-files-with-workspaces"></a>Editar archivos con Áreas de trabajo  

Este tutorial proporciona prácticas para configurar y usar un área de trabajo.  Después de agregar archivos a un área de trabajo, los cambios realizados en el código fuente dentro de DevTools se guardan en el equipo local y se conservan después de actualizar la página web.  

> [!IMPORTANT]
> **Requisitos previos:** antes de comenzar este tutorial, debe saber cómo realizar las siguientes acciones.  
> 
> *   [Usar html, CSS y JavaScript para crear una página web][MDNWebGettingStarted]  
> *   [Usar DevTools para realizar cambios básicos en CSS][DevToolsCssIndex]  
> *   [Ejecutar un servidor web HTTP local][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a>Información general  

Las áreas de trabajo permiten guardar un cambio que realice en Devtools en una copia local del mismo archivo en el equipo.  Para este tutorial, debe tener la siguiente configuración en el equipo.  

*   Tiene el código fuente del sitio en el escritorio.  
*   Está ejecutando un servidor web local desde el directorio de código fuente, de modo que el sitio sea accesible en `localhost:8080` .  
*   Se abrió `localhost:8080` en Microsoft Edge y está usando DevTools para cambiar el CSS del sitio.  

Con Workspaces habilitado, los cambios CSS que realices en DevTools se guardan en el código fuente del escritorio.  

## <a name="limitations"></a>Limitaciones  

Si usa un marco moderno, probablemente transforme el código fuente de un formato fácil de mantener en un formato optimizado para ejecutarse lo más rápido posible.  

Las áreas de trabajo normalmente pueden asignar el código optimizado al código fuente original con la ayuda de [mapas de origen.][TreehouseBlogSourceMaps]  Pero hay mucha variación entre marcos sobre cómo cada marco usa mapas de origen.  Devtools no admite todas las variaciones.  

Se sabe que las áreas de trabajo no funcionan con el siguiente marco.  

*   Crear React app  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a>Característica relacionada: invalidaciones locales  

**Invalidaciones locales es** otra característica de DevTools similar a Workspaces.  Usa Invalidaciones locales cuando quieras experimentar con los cambios en una página web y debes mostrar los cambios en las cargas de páginas web, pero no te importa asignar los cambios al código fuente de la página web.  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a>Paso 1: Configurar  

Complete las siguientes acciones para obtener experiencia práctica con Workspaces.  

### <a name="set-up-the-demo"></a>Configurar la demostración  

1.  [Abra la demostración][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Un proyecto de glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Un proyecto de glitch  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Cree un `app` directorio en el escritorio.  Guarde copias de los archivos del `workspaces-demo` directorio en el `app` directorio.  Para el resto del tutorial, el directorio se conoce como `~/Desktop/app` .  
1.  Inicie un servidor web local en `~/Desktop/app` .  A continuación se muestra un código de ejemplo para iniciar, pero `SimpleHTTPServer` puede usar el servidor que prefiera.  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  Abra una pestaña en Microsoft Edge y vaya a la versión hospedada localmente del sitio.  Debe tener acceso a ella mediante una dirección URL como `localhost:8080` o `http://0.0.0.0:8080` .  El número [de puerto exacto][WikiPortURLs] puede ser diferente.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="La demostración" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       La demostración  
    :::image-end:::  
    
### <a name="set-up-devtools"></a>Configurar DevTools  

1.  Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\) **** para abrir el panel Consola de DevTools.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Panel consola" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       Panel **consola**  
    :::image-end:::  
    
1.  Vaya a la **herramienta Orígenes.**  
1.  En el **panel Navegador** (a la izquierda), elija la pestaña **Sistema de** archivos.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Ficha Sistema de archivos" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       Ficha **Sistema de** archivos  
    :::image-end:::  
    
1.  Elija **Agregar carpeta al área de trabajo**.  
1.  Escriba `~/Desktop/app`.  
1.  Elija **Permitir** para conceder permiso a DevTools para leer y escribir en el directorio.  
    En la **pestaña Sistema de** archivos, ahora aparece un punto verde junto a , y `index.html` `script.js` `styles.css` .  Un punto verde indica que DevTools ha establecido una asignación entre un recurso de red de la página y el archivo en `~/Desktop/app` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="La pestaña Sistema de archivos ahora indica una asignación entre los archivos locales y los de red" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       La **pestaña Sistema de** archivos ahora indica una asignación entre los archivos locales y los de red  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a>Paso 2: Guardar un cambio css en disco  

1.  Abra `styles.css` .  
    
    > [!NOTE]
    > La `color` propiedad de los elementos se establece en `h1` `fuchsia` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Ver styles.css en un editor de texto" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Ver `styles.css` en un editor de texto  
    :::image-end:::  
    
1.  Elija la **herramienta** Elementos.  
1.  Cambia el valor de la `color` propiedad del elemento a tu color `<h1>` favorito.  
    Recuerde que debe elegir el elemento en el árbol DOM para mostrar las reglas CSS que se le aplican `<h1>` en el panel **Estilos.** ****  El punto verde junto `styles.css:1` a significa que cualquier cambio que realice se asigna a `~/Desktop/app/styles.css` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="El indicador verde de que el archivo está vinculado" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       El indicador verde de que el archivo está vinculado  
    :::image-end:::  
    
1.  Abra `styles.css` de nuevo en un editor de texto.  La `color` propiedad ahora está establecida en el color favorito.  
1.  Actualiza la página.  El color del `<h1>` elemento aún está establecido en el color favorito.  El cambio permanece en una actualización, porque al realizar el cambio DevTools guardó el cambio en el disco.  Después, al actualizar la página, el servidor local sirvió la copia modificada del archivo desde el disco.  
    
## <a name="step-3-save-an-html-change-to-disk"></a>Paso 3: Guardar un cambio HTML en disco  

### <a name="change-html-from-the-elements-panel"></a>Cambiar HTML desde el Panel de elementos  

Puede realizar cambios en el html desde el Panel de elementos, pero los cambios realizados en el árbol DOM no se guardan en el disco y solo tienen efecto en la sesión del explorador actual.  

El árbol DOM no es html.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-tool"></a>Cambiar HTML desde la herramienta Orígenes  

Si desea guardar un cambio en el HTML de la página web, use la **herramienta** Orígenes.  

1.  Vaya a la **herramienta Orígenes.**  
1.  En el **panel** Navegador (a la izquierda), elija la **pestaña** Página.  
1.  Elija **(índice)**.  Se abre el CÓDIGO HTML de la página.  
1.  Reemplace `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .  Revise la siguiente figura.  
1.  Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.  
1.  Actualiza la página.  El `<h1>` elemento sigue mostrando el texto nuevo después de actualizar la página.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Cambiar HTML desde la herramienta Orígenes" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Cambiar HTML desde la **herramienta Orígenes**  
    :::image-end:::  
    
1.  Abra `~/Desktop/app/index.html` .  El `<h1>` elemento contiene el texto nuevo.  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a>Paso 4: Guardar un cambio de JavaScript en disco  

El lugar principal para usar el editor de código de DevTools es la **herramienta Orígenes.**  Pero a veces es necesario tener acceso a otras herramientas, como la **herramienta Elementos** o el panel **Consola,** mientras se editan archivos.  La **herramienta Origen rápido** le proporciona solo el editor de la herramienta **Orígenes,** mientras que cualquier herramienta está abierta.  

Para abrir el editor de código DevTools junto con otras herramientas, haga lo siguiente:  

1.  Vaya a la **herramienta** Elementos.  
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  Se **abre el menú** comando.  
1.  Escriba `Quick Source` y, a continuación, **elija Mostrar origen rápido**.  En la parte inferior de la ventana DevTools, aparece la herramienta **Origen** rápido, que muestra el contenido de , que es el último archivo que editó `index.html` en la **herramienta** Orígenes.    
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Abra la herramienta Origen rápido mediante el menú Comando" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Abra la **herramienta Origen rápido** mediante el menú **Comando**  
    :::image-end:::  
    
1.  Seleccione `Control` + `P` \(Windows, Linux\) o `Command` + `P` \(macOS\) para **** abrir el cuadro de diálogo Abrir archivo.  Revise la siguiente figura.  
1.  Escriba `script` , luego elija **app/script.js**.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Abra script.js mediante el cuadro de diálogo Abrir archivo" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       Abrir `script.js` con el cuadro de diálogo **Abrir** archivo  
    :::image-end:::  
    
    > [!NOTE]
    > El `Save Changes To Disk With Workspaces` vínculo de la demostración tiene un estilo regular.  
    
1.  Agregue el siguiente código a la parte inferior de **script.js** mediante la **herramienta Origen** rápido.  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.  
1.  Actualiza la página.  
    
    > [!NOTE]
    > El vínculo de la página ahora está en cursiva.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="El vínculo de la página ahora está en cursiva" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       El vínculo de la página ahora está en cursiva  
    :::image-end:::  
    
## <a name="next-steps"></a>Pasos siguientes  

Usa lo que has aprendido en este tutorial para configurar áreas de trabajo en tu propio proyecto.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Workspaces Archivos de demostración | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Contenido : CSS: hojas de estilos en cascada | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Introducción al sitio web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ejecutar un servidor HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM: API web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Una introducción al origen Mapas | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(computer networking\) - Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
