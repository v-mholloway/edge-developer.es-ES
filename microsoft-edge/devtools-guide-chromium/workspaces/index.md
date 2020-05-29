---
title: Editar archivos con áreas de trabajo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601855"
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







# Editar archivos con áreas de trabajo   



> [!NOTE]
> El objetivo de este tutorial es proporcionar práctica práctica para configurar y usar áreas de trabajo, de modo que pueda usar áreas de trabajo en sus propios proyectos.  Puede guardar los cambios en el código fuente, en el equipo local, que ha hecho dentro de DevTools después de habilitar las áreas de trabajo.  

> [!CAUTION]
> **Requisitos previos**: antes de comenzar con este tutorial, debe saber cómo:  
> *   [Usar HTML, CSS y JavaScript para crear una página web][MDNWebGettingStarted]  
> *   [Usar DevTools para realizar cambios básicos en CSS][DevToolsCssIndex]  
> *   [Ejecutar un servidor Web HTTP local][MDNSimpleLocalHTTPServer]  

## Introducción   

Las áreas de trabajo le permiten guardar un cambio que realiza en DevTools en una copia local del mismo archivo de su equipo.  Por ejemplo, supongamos que:  

*   Tiene el código fuente de su sitio en el escritorio.  
*   Está ejecutando un servidor Web local desde el directorio de código fuente, de modo que el sitio sea accesible en `localhost:8080` .  
*   Has abierto `localhost:8080` en Microsoft Edge y estás usando DevTools para cambiar las CSS del sitio.  

Con las áreas de trabajo habilitadas, los cambios de CSS que realice dentro de DevTools se guardan en el código fuente de su escritorio.  

## Limitaciones   

Si está usando un marco moderno, probablemente transforme el código fuente desde un formato que sea fácil de mantener en un formato optimizado para ejecutarse lo antes posible.  
Las áreas de trabajo suelen poder asignar el código optimizado de nuevo al código fuente original con la ayuda de [mapas de origen][TreehouseBlogSourceMaps].  Sin embargo, hay una gran variación entre los marcos sobre cómo usan mapas de origen.  DevTools simplemente admite todas las variantes.  

Las áreas de trabajo no funcionan con estos marcos:  

*   Crear una aplicación de reAct  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## Característica relacionada: reemplazos locales   

Los **reemplazos locales** son otra característica de DevTools similar a las áreas de trabajo.  Use reemplazos locales cuando desee experimentar con los cambios realizados en una página y necesite ver los cambios en todas las páginas, pero no le importa asignar los cambios al código fuente de la página.  

<!--Todo: add section when content is ready  -->  

## Paso 1: configuración   

Complete este tutorial para obtener experiencia práctica con áreas de trabajo.  

### Configurar la demostración   

1.  [Abra la demostración][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### Figura 1  
    > Un proyecto de problema en ![ un proyecto de problema][ImageGlitchProject]  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  Cree un `app` directorio en el escritorio.  Guarde copias de los archivos en el `workspaces-demo` directorio.  Para el resto de este tutorial, este directorio se conoce como `~/Desktop/app` .  
1.  Inicie un servidor Web local en `~/Desktop/app` .  A continuación encontrará código de ejemplo para el inicio `SimpleHTTPServer` , pero puede usar cualquier servidor que prefiera.  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  Abra una pestaña en Microsoft Edge y vaya a la versión hospedada localmente del sitio.  Debería poder acceder a ella usando una dirección URL como `localhost:8080` o `http://0.0.0.0:8080` .  El [número de Puerto][WikiPortURLs] exacto puede ser diferente.  
    
    > ##### Figura 2  
    > La demostración  
    > ! [Demostración] [ImageDemo]  

### Configurar DevTools   

1.  Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir el panel de **consola** de DevTools.  
    
    > ##### Imagen 3  
    > Panel de **consola**  
    > ! [Panel de consola] [ImageConsolePanel]  

1.  Haga clic en la pestaña **orígenes** .  
1.  Haga clic en la pestaña **sistema de archivos** .  
    
    > ##### Imagen 4  
    > Ficha **filesystem**  
    > ! [Ficha filesystem] [ImageFilesystem]  

1.  Haga clic en **Agregar carpeta al área de trabajo**.  
1.  Seleccione `~/Desktop/app` .  
1.  Haga clic en **permitir** para dar a DevTools permiso de lectura y escritura en el directorio.  
    En la ficha **filesystem** , ahora hay un punto verde junto a `index.html` , `script.js` y `styles.css` .  Estos puntos verdes indican que DevTools ha establecido una asignación entre los recursos de red de la página y los archivos de `~/Desktop/app` .  
    
    > ##### Imagen 5  
    > La ficha **filesystem** ahora muestra una asignación entre los archivos locales y los de red  
    > ! [La ficha filesystem ahora muestra una asignación entre los archivos locales y las redes] [ImageMapping]  

## Paso 2: guardar un cambio de CSS en disco   

1.  Abra `styles.css` .  
    
    > [!NOTE]
    >La `color` propiedad de `h1` elementos se establece en `fuchsia` .
    
    > ##### Imagen 6  
    > Ver `styles.css` en un editor de texto  
    > ! [Visualizando Styles. CSS en un editor de texto] [ImageStylesFuchsia]  


1.  Haga clic en la pestaña **elementos** .  
1.  Cambie el valor de la `color` propiedad del `<h1>` elemento a su color favorito.  
    Recuerde que debe hacer clic en el `<h1>` elemento del **árbol DOM** para ver las reglas de CSS que se aplican en el panel **estilos** .  El punto verde junto a `styles.css:1` significa que todos los cambios que realice se asignan a `~/Desktop/app/styles.css` .  
    
    > ##### Imagen 7  
    > El indicador verde indica que el archivo está vinculado  
    > ! [El indicador verde indica que el archivo está vinculado] [ImageStylesGreen]  

1.  `styles.css`Vuelva a abrir en un editor de texto.  La `color` propiedad ya está configurada con su color favorito.  
1.  Vuelva a cargar la página.  El color del `<h1>` elemento se mantiene establecido en el color que prefiera.  Esto funciona porque, al realizar el cambio, DevTools guardado el cambio en el disco.  Y después, cuando vuelva a cargar la página, el servidor local sirvió la copia modificada del archivo desde el disco.  

## Paso 3: guardar un cambio HTML en el disco   

### Cambiar HTML desde el panel elementos  

Puede realizar cambios en el HTML desde el panel elemento, pero sus cambios en el árbol DOM no se guardan en el disco y solo afectan a la sesión actual del explorador.  
El árbol DOM no es HTML.  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### Cambiar HTML desde el panel orígenes   

Si desea guardar un cambio en el código HTML de la página, hágalo usando el panel **fuentes** .  

1.  Haga clic en la pestaña **orígenes** .  
1.  Haga clic en la pestaña **Página** .  
1.  Haga clic en **(índice)**.  Se abrirá el código HTML de la página.  
1.  Reemplazar `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .  Consulte la [figura 8](#figure-8).  
1.  Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.  
1.  Vuelva a cargar la página.  El `<h1>` elemento aún muestra el nuevo texto.  
    
    > ##### Imagen 8  
    > La línea 12 se ha configurado en `I ❤️  Cake`  
    > ! [Cambiar HTML desde el panel orígenes] [ImageSourcesCakeHTML]  

1.  Abra `~/Desktop/app/index.html` .  El `<h1>` elemento contiene el nuevo texto.  

## Paso 4: guardar un cambio de JavaScript en el disco   

El panel **orígenes** también es el lugar donde se pueden realizar cambios en JavaScript.  Sin embargo, a veces necesita acceder a otros paneles, como el panel **elementos** o el panel de **consola** , mientras realiza cambios en su sitio.  Hay una forma de abrir el panel **fuentes** junto con otros paneles.  

1.  Haga clic en la pestaña **elementos** .  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).  Se abrirá el **menú de comandos** .  
1.  Escriba `QS` y, a continuación, seleccione **Mostrar fuente rápida**.  En la parte inferior de la ventana de DevTools ahora hay una ficha de **fuente rápida** .  La pestaña muestra el contenido de `index.html` , que es el último archivo editado en el panel **fuentes** .  La pestaña **origen rápido** le ofrece el editor del panel **fuentes** , de modo que pueda editar archivos mientras tiene otros paneles abiertos.  
    
    > ##### Imagen 9  
    > Abrir la pestaña de **origen rápido** con el **menú de comandos**  
    > ! [Abrir la pestaña de origen rápido mediante el menú de comandos] [ImageCommandMenuQuickSource]  

1.  Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \) para abrir el cuadro de diálogo **Abrir archivo** .  Consulte la [figura 10](#figure-10).  
1.  Escriba `script` y, a continuación, seleccione **App/script. js**.  
    
    > ##### Imagen 10  
    > Abrir `script.js` con el cuadro de diálogo **Abrir archivo**  
    > ! [Abriendo script. js con el cuadro de diálogo Abrir archivo] [ImageOpenFileDialog]  
    
    > [!NOTE]
    > El `Save Changes To Disk With Workspaces` vínculo de la demostración se ha estilo regularmente.  
    
1.  Agregue el código siguiente en la parte inferior de **script. js** con la pestaña de **origen rápido** .  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.  
1.  Vuelva a cargar la página.  
    
    > [!NOTE]
    > El vínculo de la página ahora está en cursiva.
    
    > ##### Imagen 11  
    > El vínculo de la página ahora está en cursiva  
    > ! [El vínculo de la página ahora está en cursiva] [ImageScriptItalic]  

## Pasos siguientes   

Use lo que ha aprendido en este tutorial para configurar áreas de trabajo en su propio proyecto.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Ilustración 1: un proyecto de problema con un nombre generado aleatoriamente"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo.msft.png "Ilustración 2: la demostración"  
[ImageConsolePanel]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Console.msft.png "Ilustración 3: el panel de consola"  
[ImageFilesystem]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-filesystem.msft.png "Ilustración 4: la ficha filesystem"  
[ImageMapping]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-filesystem-Folder.msft.png "Figura 5: la ficha filesystem ahora muestra una asignación entre los archivos locales y los de red"  
[ImageStylesFuchsia]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-filesystem-CSS.msft.png "Ilustración 6: visualización de estilos. CSS en un editor de texto"  
[ImageStylesGreen]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Elements-Styles-CSS.msft.png "Ilustración 7: el indicador verde que está vinculado al archivo"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-Page-H1.msft.png "Ilustración 8: cambiar HTML desde el panel orígenes"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Search-show-Quick-Source.msft.png "Ilustración 9: abrir la pestaña de origen rápido con el menú de comandos"  
[ImageOpenFileDialog]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Search-script.msft.png "Figura 10: abrir script. js con el cuadro de diálogo Abrir archivo"  
[ImageScriptItalic]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Elements-Styles-Quick-Source-script.msft.png "ilustración 11: el vínculo de la página ahora está en cursiva"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Archivos de demostración de áreas de trabajo | Intento"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Contenido-CSS: hojas de estilos en cascada | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Introducción a la web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ejecutando un servidor HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM-API Web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Introducción a los mapas de origen | Blog de Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Puerto \ (red del equipo \)-Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
