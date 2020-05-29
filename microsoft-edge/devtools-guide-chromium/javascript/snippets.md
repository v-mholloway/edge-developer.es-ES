---
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581820"
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





# Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools   



Si tienes que ejecutar el mismo código de forma repetida en la [consola][DevtoolsConsoleIndex] , considera la posibilidad de guardar el código como un fragmento de código.  Los fragmentos de código son scripts que se crean en el [panel **fuentes** ][DevToolsSourcesPanel].  Tienen acceso al contexto de JavaScript de la página y puede ejecutarlos en cualquier página.  Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet].  
Firefox DevTools tiene una característica similar a la de los fragmentos de código denominado [Bloc][MDNScratchpad]dedo.  

Por ejemplo, la [**figura 1**](#figure-1) muestra la página de inicio de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.  

> ##### Figura 1  
> Aspecto de la página antes de ejecutar el fragmento de código  
> ![Aspecto de la página antes de ejecutar el fragmento de código][ImageSnippetSplitScreen]  

El código fuente del fragmento de código de la [**Ilustración 1**](#figure-1):  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

La [**ilustración 2**](#figure-2) muestra el aspecto que tendrá la página después de ejecutar el fragmento de código.  El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el recorte y el contenido de la página cambian por completo.  

> ##### Figura 2  
> Aspecto de la página después de ejecutar el fragmento de código  
> ![Aspecto de la página después de ejecutar el fragmento de código][ImageSnippetSplitScreenAfter]  

## Abrir el panel de fragmentos   

El panel de **fragmentos de código** muestra los fragmentos de código.  Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .  

> ##### Imagen 3  
> El panel de **fragmentos**  
> ![El panel de fragmentos][ImageSnippetsPane]  

### Abrir el panel de fragmentos de código con un mouse   

1.  Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .  El panel de **páginas** suele abrirse de forma predeterminada.  

    > ##### Imagen 4  
    > Panel **orígenes** con el panel de **páginas** abierto a la izquierda  
    > ![Panel orígenes con el panel de páginas abierto a la izquierda][ImageSourcesPageEmpty]  

1.  Haga clic en la pestaña **fragmentos** para abrir el panel **fragmentos de código** .  Es posible que tenga que hacer clic en **más pestañas** ![ más pestañas ][ImageMoreTabsIcon] para acceder a la opción **fragmentos** .  

### Abrir el panel de fragmentos de código con el menú de comandos   

1.  Centre el cursor en algún lugar dentro de DevTools.  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Comience `Snippets` a escribir, seleccione **Mostrar fragmentos**y, a continuación, presione `Enter` para ejecutar el comando.  

    > ##### Imagen 5  
    > El comando **Mostrar fragmentos**  
    > ![El comando Mostrar fragmentos][ImageShowSnippetsSearch]  

## Crear fragmentos   

### Crear un fragmento de código a través del panel orígenes   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic en **nuevo fragmento de código**.  
1.  Escriba un nombre para el fragmento de código y, a continuación, presione `Enter` para guardar.  

    > ##### Imagen 6  
    > Asignar un nombre a un fragmento  
    > ![Asignar un nombre a un fragmento][ImageSnippetName]  

### Crear un fragmento de código mediante el menú de comandos   

1.  Centre el cursor en algún lugar dentro de DevTools.  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Comience `Snippet` a escribir, seleccione **crear nuevo fragmento**y, a continuación, presione `Enter` para ejecutar el comando.  

    > ##### Imagen 7  
    > Comando para crear un nuevo fragmento de código  
    > ![Comando para crear un nuevo fragmento de código][ImageCreateSnippetSearch]  

Consulte cambiar [el nombre](#rename-snippets) de los fragmentos de código si desea asignar un nombre personalizado al nuevo fragmento de código.  

## Editar fragmentos de código   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  En el panel **fragmentos** de código, haga clic en el nombre del fragmento de código que desea editar para abrirlo en el **Editor de código**.  

    > ##### Imagen 8  
    > El editor de código  
    > ![El editor de código][ImageSnippetEditor]  

1.  Use el **Editor de código** para agregar JavaScript al fragmento de código.  
1.  Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado. Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.  

    > ##### Imagen 9  
    > Un asterisco junto al nombre del fragmento de código, que indica código no guardado  
    > ![Un asterisco junto al nombre del fragmento de código, que indica código no guardado][ImageUnsavedSnippet]  

## Ejecutar fragmentos de código   

### Ejecutar un recorte desde el panel fuentes   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic en el nombre del fragmento de código que desea ejecutar.  El fragmento de código se abre en el **Editor de código**.  
1.  Haga clic en **Ejecutar** ![ fragmento ][ImageRunSnippetIcon] de código de ejecución o pulse `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \).  

### Ejecutar un fragmento de código con el menú de comandos   

1.  Centre el cursor en algún lugar dentro de DevTools.  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.  

    > ##### Imagen 10  
    > Ejecución de un fragmento de código desde el menú de comandos  
    > ![Ejecución de un fragmento de código desde el menú de comandos][ImageRunSnippetCommand]  

1.  Pulse `Enter` para ejecutar el fragmento de código.  

## Cambiar el nombre de los fragmentos de código   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic con el botón derecho en el nombre del fragmento y seleccione cambiar **nombre**.  

## Eliminar fragmentos de código   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic con el botón derecho en el nombre del fragmento y seleccione **quitar**.  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Ilustración 1: aspecto de la página antes de ejecutar el fragmento de código"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Ilustración 2: el aspecto de la página después de ejecutar el fragmento de código"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Ilustración 3: el panel de fragmentos de código"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Ilustración 4: el panel orígenes con el panel de páginas abierto a la izquierda"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Ilustración 5: el comando Mostrar fragmentos"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Ilustración 6: asignar un nombre a un fragmento de código"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Ilustración 7: el comando para crear un nuevo fragmento de código"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Ilustración 8: el editor de código"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Ilustración 9: un asterisco junto al nombre del fragmento de código, que indica que el código no se ha guardado"  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Ilustración 10: ejecutar un recorte desde el menú de comandos"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola"  
[DevToolsSourcesPanel]: ../sources.md "Información general del panel orígenes"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet, Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
